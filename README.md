## 这是一个HTTP服务器

### Version-1.0

> 2016-03-22
> 
> 正在重写中，最初版本的代码过乱，不宜维护

> 基本功能已经完成

- 高性能高并发
- C语言开发
- `epoll` + 线程池
- `Linux` 环境， 非跨平台
- `gcc -std=gnu99 -pthread -DWSX_DEBUG`
- 使用`CMake-3.3`。 可以直接修改版本号搭配自己平台的使用，当前`apt`上的版本为`2.8`
- 英文注释
### 模块
- 最外部为入口程序，以及读取配置的函数。
- `handle` 模块则是对于 **读/写/错误** 事件的一个控制
- `memop`模块是用来扩展内存分配的，例如`jcmalloc`，目前只是使用自带的库函数，并加一层包装。
- `config` 暂时存放配置文件
- `timer`模块(待开发，未添加)，用于无效`socket`的关闭回收
### 配置文件

- 可以在 `config` 文件夹下的 `wsx.conf` 修改配置，当前支持的配置选项只有四个
- 详见配置文件
- 以 `#` 开头的为注释，单行有效
- 使用

> 其中配置文件的路径硬编译在源码中， `../../config/wsx.conf`，意思是可执行文件在`output/Release(Debug)/`中，需要自行修改，后期会修缮。


### 进度
- 完成总体程序框架的编写
- 基本功能完成

### TODO
- `timer`模块
- **http** 请求头 : `GET POST`
- 当所请求文件过大时，分块存储