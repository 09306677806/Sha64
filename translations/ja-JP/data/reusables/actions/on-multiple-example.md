単一のイベントもしくは複数のイベントを指定できます。 たとえば、以下の`on`の値を持つワークフローは、リポジトリ内の任意のブランチにプッシュが行われたとき、あるいは誰かがリポジトリをフォークした時に実行されます。

```yaml
on: [push, fork]
```

複数のイベントを指定した場合、ワークフローがトリガされるのに必要なのはそれらのイベントの中の1つだけです。 ワークフローをトリガーする複数のイベントが同時に生じた場合、複数のワークフローの実行がトリガーされます。
