## 这是一个HTTP服务器

### Version-0.3

> 2016-03-20
> 
> 正在重写中，最初版本的代码过乱，不宜维护

- 高性能高并发
- C语言开发
- `epoll` + 多线程
- `Linux` 环境，不跨平台
- `gcc -std=gnu99`
- 使用`CMake-3.3`。 可以直接修改版本号搭配自己平台的使用，当前`apt`上的版本为`2.8`
- 英文注释

### 配置文件

- 可以在 `config` 文件夹下的 `wsx.conf` 修改配置，当前支持的配置选项只有四个
- 详见配置文件
- 以 `#` 开头的为注释，单行有效
- 使用

### 进度
- 完成总体程序框架的编写
- 正在编写 处理HTTP请求的模块