# docker-phphub5
docker phphub5环境

[docker-安装phphub5](http://www.majianwei.com/archives/6356)

## 环境及版本
Nginx 1.8+

PHP 5.6+

Mysql 5.7+

Redis 3.0+

Memcached 1.4+

php memcache 扩展

Laravel 5.1


## 安装步骤
1. 安装docker、docker-compose
2. git clone https://github.com/helloMJW/phphub5
3. 进到wwwroot目录下 git clone https://github.com/summerblue/phphub5.git
4. 进入php5.6容器 composer install
5. 创建数据库
6. cp .env.example .env 并编辑相关数据库信息mysql redis 及 APP_ENV=local 和 APP_DEBUG=true //APP_ENV如果为 production侧为生产环境不会导入测试数据
7. php artisan est:install //如果出现 php artisan migrate –seed 卡住的话, 输入yes 回车
8. host 文件 对应 ip phphub5.app
9. 浏览器 phphub5.app


## 安装过程问题记录
Q: 出现500错误或白屏?

A: chmod -R ./wwwroot/phphub5 //权限导致的


## 待解决问题
[phphub5安装后报错Trying to get property of non-object (View ?](https://segmentfault.com/q/1010000011311598) [issues](https://github.com/summerblue/phphub5/issues/107)


## 相关资料
[GITHUB-phphub5](https://github.com/summerblue/phphub5)

[php artisan est:install之后在这里卡住](https://laravel-china.org/topics/3736/phphub5-installation-problem?order_by=vote_count&)

[phphub5 centos 安装](http://blog.csdn.net/robert198837/article/details/52970746)





