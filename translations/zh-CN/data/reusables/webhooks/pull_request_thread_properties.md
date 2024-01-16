| 键              | 类型    | 描述                                           |
| -------------- | ----- | -------------------------------------------- |
| `action`       | `字符串` | 执行的操作内容. 可以是以下选项之一：<ul><li>“已解决” - 拉取请求上的注释线程已标记为已解决。</li><li>“未解决” - 拉取请求上以前解决的注释线程被标记为未解决。</li></ul> |
| `pull_request` | `对象`  | 与线程相关的[拉取请求](/rest/reference/pulls)。         |
| `线程`           | `对象`  | 受影响的线程。                                      |