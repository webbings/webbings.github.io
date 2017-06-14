# webbings.github.io

## 复习

快速排序
普通排序
冒泡排序

## structs
jsp触发action；structs拦截器拦截请求，调用后台action；action返回结果，有不同的jsp展现数据。
ActionMapper决定调用哪个Action
FilterDispatcher把请求得处理交个ActionProxy
拦截器Intercepter
配置structs.xml 配置Action类

从体系结构来看：struts2大量使用拦截器来出来请求，从而允许与业务逻辑控制器 与 servlet-api分离，避免了侵入性；而struts1.x在action中明显的侵入了servlet-api.
    从线程安全分析：struts2.x是线程安全的，每一个对象产生一个实例，避免了线程安全问题；而struts1.x在action中属于单线程。
    性能方面：struts2.x测试可以脱离web容器，而struts1.x依赖servlet-api，测试需要依赖web容器。
    请求参数封装对比：struts2.x使用ModelDriven模式，这样我们 直接 封装model对象，无需要继承任何struts2的基类，避免了侵入性。
    标签的优势：标签库几乎可以完全替代JSTL的标签库，并且 struts2.x支持强大的ognl表达式。
    当然，struts2和struts1相比，在 文件上传，数据校验 等方面也 方便了好多。在这就不详谈了

## GC
