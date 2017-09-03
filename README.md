# PythonTools
描述：
这个项目只是一个带IoC、模板引擎、ORM的MVC框架！！
只是写了一个用于加密，hash，和根据模板生成带动态参数的url工具页面。

用到的主要三方框架：
模板引擎用了Iinja2，
数据库驱动用了pymssql，
http服务用了aiohttp，
协程用了asyncio，

目的：
最终我希望把它改造成一个Wechat接口程序+后台程序。

其他：
我的第一个python项目，基本参考了廖雪峰大牛的文档（<a href="https://www.liaoxuefeng.com/wiki/0014316089557264a6b348958f449949df42a6d3a2e542c000">python教程</a>）,他的文档很有条理，料也很足，很适合初学者进行一个全面的摸底。
我挺佩服他，个人觉得一个能将一个复杂的知识领域有取舍、有条理的写出高可读性的Doc，需要很大的知识量、熟练度，和对技术执着。
当然他的文档只是入门和启迪的作用，最重要的还是得从官方文档和技术社区寻找更专一的，优雅的实现。

项目说明：
这个项目框架我用了很久，可扩展性很强，复杂度很低。较适合中等大小的项目开发。
依赖关系：
  Common：不依赖任何其他模块；
  Entity：不依赖任何其他模块；
  Model：不依赖与任何其他模块；
  Services：依赖于Common；
  Decorator：依赖于Common；
  Repository：依赖于Entity，和Common；
  Buiness：依赖于Repository，Entity，Model，Common；
  MVC：依赖于其他的所有模块；
  
这个项目从目录上来看->
  Common模块：通用的工具类，
  Entity模块：作为数据库对象容器，
  Model模块：作为View的数据源，有时Entity的字段和类型并不适合直接返回给View使用，
  Services模块：用于与外部接口打交道，依赖于Common，有自己的Model与外界进行通讯，
  Decorator模块：对我来说这一层应该分配到View层更合适，但是因为不同于Asp.Net程序的过滤器，Decorato可以用于所有的class和function，所以我抽出来作为         单独的一层使用，
   Repository模块：直接与数据库打交道，
   Buiness模块：用于处理业务，Model与Entity之间的转换等作用，
   MVC模块：最终输出的一层，没有逻辑，至于简单的数据操作。
  
  
