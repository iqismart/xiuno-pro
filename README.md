# 介绍
Xiuno PRO 是在消逝的官方git版本基础上，兼容php8；jquery、bootstrap版本升级。移除全部插件上线一起smart插件中心；修复了若干小bug。

## 我做了些什么

### 修复 
- 兼容php8.0
- 修复无法卸载插件bug
- 修复后台插件页面无法打开
### 更新
- 💄一起smart插件中心上线
- 💥采用**utf8mb4**，支持emoji 
- 💥jquery、bootstrap版本升级  
- 其他优化
 
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

## 下一步

- [x] 丰富插件中心，上架更多插件。
- [x] 对php8进行适配。
- [x] 将部分设置选项（比如开启伪静态设置）集成到后台，方便管理员使用。
- [x] 整理修复部分插件
- [ ] 添加简约风、acg风格、绿色小清新风格主题。
- [ ] 重启社区计划

## 贡献者
创始人：axiuno

感谢：cnteacher@discuz、Discuz!、Team Artery、剑心@wooyun、右键森林、吴兆焕、杨永全、郑城、大象、燃烧的冰、⭐Star本项目的您。

## Enjoy!