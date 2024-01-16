每当工作流程中的作业开始时，都会将 `GITHUB_TOKEN` 密钥设置为仓库的访问令牌。 您应该在工作流程文件中设置此访问令牌的权限，以授予 `contents` 范围的读取访问权限，并授予 `packages` 范围的写入访问权限。 更多信息请参阅“[使用 GITHUB_TOKEN 验证身份](/actions/configuring-and-managing-workflows/authenticating-with-the-github_token)”。