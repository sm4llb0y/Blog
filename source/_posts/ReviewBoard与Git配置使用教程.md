title: ReviewBoard与Git配置使用教程
date: 2016-04-22 18:27:11
tags: ReviewBoard, Git, CR, Gitlab
---
本文简单介绍了Reviewboard的安装以及如何跟Gitlab配合使用。
<!--more-->

1. [安装Reviewboard](https://www.reviewboard.org/docs/manual/2.5/admin/installation/creating-sites/#creating-sites)
    1.1 如果使用apache+mod_wsgi，务必启用wsgi`sudo a2enmod wsgi`
    1.2 修改ports.conf，启用你想使用的端口
    ```
    <IfModule mod_wsgi.c>
        Listen 81
    </IfModule>
    ```
2. [安装RBTools](https://www.reviewboard.org/downloads/rbtools/)
    2.1 如果使用pip安装方式，要先安装pip，`apt-get install -y python-pip`
3. 配置Reviewboard，启用Gitlab中的Repo
    ![添加Repo](/images/posts/Reviewboard-Gitlab.png)
4. 添加完成后就可以直接访问`http://reviewhost:port/r/new/`从Reviewboard看到Gitlab中的所有Commit，并创建Review了
    ![查看Repo](/images/posts/Reviewboard-Repo.png)
5. 或者当然你可以新建Branch后，通过rbt命令行提交Code Review
    ```
    rbt post
    rbt post my-branch-1..my-branch-2
    rbt post my-branch-1..HEAD
    rbt post -u
    ```
    ![rbt详细文档](https://www.reviewboard.org/docs/rbtools/dev/)