forkfrom 
https://github.com/li-franky/docker-svnserver


本docker file 源自 https://hub.docker.com/r/frankylee/websvn 的镜像文件

# docker-svnserver
Subversion with Apache - Image Base CentOS 7.4.1708 带WEB管理工具的SVN服务器。

启动方式：
```bash
docker run -d --name websvnser  --volume /mtdata/svnrepo:/var/www/html/data --publish 18080:80 brotherdavid/websvn:0.3
```
说明：
>* --name svnserver：容器名称
>* --volume /mtdata/svnrepo:/var/www/html/data：/mtdata/svnrepo是宿主机目录，用于持久化svn数据
>* --publish 18080:80：映射到宿主机的端口号
>* fbrotherdavid/websvn:0.3：docker镜像的名称和版本号。

访问地址 ：http://<宿主机IP>:<映射到宿主机的端口号>

默认管理密码是 admin / admin

