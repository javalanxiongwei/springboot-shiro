# springboot-shiro
##SpringBoot整合Shiro的案例
##1、项目文件分析:
项目是使用SpringBoot+Freemarker+Shiro
相关文件说明：
`DepartmentController`:部门相关的控制器
`EmployeeController`:员工相关的控制器
`LoginController`:登陆相关的控制器
`MainController`:首页相关的控制器
`UserRealm`:用户的Realm
`BootApplication`:启动类.
`login.ftl`:登陆页面
当访问`http://localhost:8088/main`的时候展示`main.ftl`的页面.
当访问`http://localhost:8088/login`的时候展示`login.ftl`的页面.
当访问`http://localhost:8088/department`的时候展示`department/list.ftl`的页面.
当访问`http://localhost:8088/employee`的时候展示`employee/list.ftl`的页面.

##2、测试
打开`BootApplication`右键run启动
当访问`http://localhost:8088/main`的时候跳转到了登陆页面.默认密码是:
使用的是静态认证.

|账号|密码
|:------:|:-----:|
|zhangsan|666
|lisi|888

`zhangsan`:用户拥有`/employee`和`/department`的请求权限
`lisi`:用户拥有`/department`的请求权限

