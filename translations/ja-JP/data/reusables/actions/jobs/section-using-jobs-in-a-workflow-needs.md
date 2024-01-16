`jobs.<job_id>.needs`を使って、このジョブを実行する前に成功して完了していなければならないジョブを特定してください。 これは文字列型または文字列の配列です。 1つのジョブが失敗した場合、失敗したジョブを続行するような条件式を使用していない限り、そのジョブを必要としている他のジョブはすべてスキップされます。 1つの実行にお互いを必要とする一連のジョブが含まれていた場合、失敗時点以降の依存関係チェーン中のすべてのジョブに失敗が適用されます。

#### 例: 依存対象のジョブの成功を必要とする

```yaml
jobs:
  job1:
  job2:
    needs: job1
  job3:
    needs: [job1, job2]
```

この例では、`job1`が正常に完了してから`job2`が始まり、`job3`は`job1`と`job2`が完了するまで待機します。

つまり、この例のジョブは逐次実行されるということです。

1. `job1`
2. `job2`
3. `job3`

#### 例: 依存対象のジョブの成功を必要としない

```yaml
jobs:
  job1:
  job2:
    needs: job1
  job3:
    if: {% raw %}${{ always() }}{% endraw %}
    needs: [job1, job2]
```

この例では、`job3`は条件式の`always()` を使っているので、`job1`と`job2`が成功したかどうかにかかわらず、それらのジョブが完了したら常に実行されます。 詳しい情報については「[式](/actions/learn-github-actions/expressions#status-check-functions)」を参照してください。