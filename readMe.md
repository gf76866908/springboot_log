
## 项目介绍：

#### 本项目主要是日志处理实现多线程进行处理：

1.  **接口日志异步池化入库：** 将接口中的日志内容直接放入到队列中，不需要进行日志入库了，减少了一次数据库操作，可以提升接口的响应速度 。

2.  **库中日志多线程清理：** 当日志表中的数据量过多时，会占用很多的磁盘空间，进而可能导致磁盘空间不足的告警，此时就需要进行日志的清理，但是此时在清理时，还需要将最新多少天的数据保留，将之前的日志数据清理掉 。


## 项目结构：

#### 项目结构展示：

[点击查看结构图](https://cdn.jsdelivr.net/gh/leishen6/ImgHosting/MuZiLei_blog_img/20201227215415.png)



## 启动测试：

- 启动后测试日志异步池化入库操作的接口地址： **http://127.0.0.1:8081/v1/api/log/test**

- 项目中准备了使用的SQL脚本；在 **/resources/sql** 目录下