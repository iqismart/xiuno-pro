# 介绍
Xiuno PRO 是在官方git版本基础上，兼容php8；上线一起smart插件中心；一键在线升级；修复了若干bug。

## 下载安装
- 环境：php5.x-8.x、mysql5.x-8.x
- 下载：[发布页](https://github.com/iqismart/xiuno-pro/releases)
- 安装：上传到网站根目录，访问首页即可进入安装


## 我做了些什么

### 修复 
- 兼容php8.0
- 修复无法卸载插件bug等其他bug

### 插件中心
- 💄一起smart插件中心上线
![](https://img.iqismart.com/imgs/2021/11/8cbecc2f37ae981e.png)
- 支持搜索
![](http://img.iqismart.com/imgs/2021/11/e3982c51738c42b4.png)

### 一键更新
一键检查更新，在线升级

在后台首页:

![图片](https://img.iqismart.com/imgs/2021/11/5329476997e54487.png)

注意：除/conf/conf.php、/upload、/plugin目录外都将被覆盖，请谨慎操作

### 其他优化
 
## 使用
使用请下载发布版，集成较少插件。数据库请采用**utf8mb4**
插件和主题，在线下载安装或直接上传到**plugin**目录中，后台插件中心开启。

### 伪静态
后台设置开启伪静态，添加对应的伪静态规则。

<details>
<summary>Apache伪静态:</summary>

```
<IfModule mod_rewrite.c>
RewriteEngine on

# Apache 2.4
RewriteCond %{REQUEST_FILENAME} !-d 
RewriteCond %{REQUEST_FILENAME} !-f 
RewriteRule ^(.*?)([^/]*)$ $1index.php?$2 [QSA,PT,L]

# Apache other
#RewriteRule ^(.*?)([^/]*)\.htm(.*)$ $1/index.php?$2.htm$3 [L]
</IfModule>
```
</details>

<details>
<summary>Nginx伪静态:</summary>

```
location ~* \.(htm)$ {

    rewrite "^(.*)/(.+?).htm(.*?)$" $1/index.php?$2.htm$3 last;

}
```
</details>


## 插件下载

在线安装：后台主页->插件->免费插件/收费插件
离线安装：[一起smart插件中心：](https://www.iqismart.net/forum-4.htm)

## 如何发布插件到插件中心
- 前往社区 [一起smart](https://www.iqismart.net/forum-4.htm) 插件版块，发布插件即可

## 下一步
- [ ] xiuno核心：增加手机号登录、企业支付等。 
- [ ] 插件：丰富插件中心，上架更多插件。 
 
