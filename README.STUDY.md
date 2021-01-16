###以下是在localhost进行学习的记录：

####1.  localhost环境下运行/scripts/sql的两个sql脚本
####2.  修改/scripts/build.bat(Linux更改build.sh)文件，将数据库连接信息更换为localhost的信息
####3.  运行build.bat文件，生成jar包
####4.  分别进入adminservice、configservice、portal的target目录，使用java -jar命令，分别运行对应jar包
####5.  查找portal的端口，使用localhost:****访问apollo的管理界面，账号密码都为apollo

######在portal端管理员工具中，可以创建不同的部门和用户，以进行不同project在同一apollo环境下的权限分配和项目管理
######同一个项目可以创建多个namespace，其中application为各namespace默认的私有空间

####6.  在需要使用apollo的项目中，加入如下配置，其他的配置一律放置在对应id的namespace中
######app.id = XXL-ADMIN-EXECUTOR   #和portal端配置的id保持一致
######apollo.meta = http://localhost:****   #apollo-configservice地址
######apollo.bootstrap.enabled = true
######apollo.bootstrap.namespaces = application,XXL-JOB.DATABASE