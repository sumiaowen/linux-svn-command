Linux下SVN常用命令:

=================

1、将文件checkout到本地目录

    命令：svn checkout path（path是服务器上的目录）
    例如：svn checkout svn://192.168.1.1/pro/domain
    简写：svn co

2、往版本库中添加新文件

    命令：svn add file
    例如：svn add test.php

3、将改动提交至版本库

    命令：svn commit -m 'log message'
    例如：svn commit -m 'add new file test.php'
    简写：svn ci

3、删除

    命令：svn delete file
    命令：svn delete test.php

4、更新

    1)、更新至最新版本
        命令：svn update
    2）、更新至某一个版本
        命令：svn update -r 版本号
        例如：svn update -r 11 (更新至11版本）
    简写：svn up

5、文件状态

    命令：svn status
    说明：
        1）、正常状态下无信息显示
        2）、?  不在SVN的控制中
        3）、M  内容被修改
        4）、C  方式冲突
        5）、A  添加到版本库
        6）、K  被锁定

6、查看日志

    命令：svn log

7、查看文件详细信息

    命令：svn info file

8、文件比较

    1)、将改动的文件（注：该文件未提交）与版本库进行对比
        命令：svn diff file
        例如：svn diff 2.php

    2）、对比不同版本间的差异
        命令：svn diff -r num:num file
        例如：svn diff -r 12:13 2.php  对文件版本12与版本13间的差异

9、查看帮助

    命令：svn --help
    简写：svn ? 或者 svn h

