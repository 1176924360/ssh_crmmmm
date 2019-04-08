# ssh_crmmmm
对于ssh中的一些之前不熟练的知识点进行了解

第一点：在编写的applicationContext.xml时，与hibernate结合时，需要导入db.properties文件，为什么用<context:property-placeholder location="classpath:db.properties"/>
有些参数在某些阶段中是常量、而这些参数在不同阶段之间又往往需要改变，这些参数由location值为参数配置文件的位置。
classpath可以加载整个classpath下（包括jar包里面）的资源文件，只会返回第一个匹配的资源，查找路径是优先在项目中存在资源文件，再查找jar包。

第二点：<bean name="dataSource" class="com.mchange.v2.c3p0.ComboPooledDataSource">
bean元素是将一个对象交给spring容器管理(IOC)
name属性：获得对象根据该名字获得，可以重复，可以使用特殊字符
class属性：被管理对象的完整类名
