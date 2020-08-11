# HackShiro

本项目创建于2020年8月11日。记录自己在学习Shiro漏洞中遇到的一些知识。本项目会持续更新，最近的一次更新时间为2020年8月11日。

## 一、Shiro基础
- http://greycode.github.io/shiro/doc/reference.html

## 二、Shiro识别

- 请求包的cookie中存在rememberMe字段。
- 响应包中存在rememberMe=deleteMe字段。
- 请求包中存在rememberMe=x时，响应包中存在rememberMe=deleteMe。

## 三、Shiro漏洞

本项目注重漏洞利用效果。详细的漏洞分析请参考本站的关于Shiro分析的文章。

- Shiro rememberMe反序列化漏洞：CVE-2016-4437（Shiro-550）
- Shiro Padding Oracle Attack：Shiro-721
- Apache Shiro身份验证绕过漏洞：CVE-2020-11989

## 四、漏洞检测

## 五、漏洞利用

### HackShiro With Python
- https://github.com/sv3nbeast/ShiroScan
- https://github.com/insightglacier/Shiro_exploit
- https://github.com/3ndz/Shiro-721
- https://github.com/jas502n/SHIRO-550
- https://github.com/jas502n/SHIRO-721
- https://github.com/insightglacier/Shiro_exploit
- https://github.com/acgbfull/Apache_Shiro_1.2.4_RCE
- https://github.com/sunird/shiro_exp
- https://github.com/teamssix/shiro-check-rce
- https://github.com/wyzxxz/shiro_rce
- https://github.com/bkfish/Awesome_shiro
- https://github.com/zhzyker/shiro-1.2.4-rce

### HackShiro With Java
- https://github.com/feihong-cs/ShiroExploit
- https://github.com/potats0/shiroPoc
- https://github.com/tangxiaofeng7/Shiroexploit
- https://github.com/fupinglee/ShiroScan

## 六、命令回显

Shiro命令回显最早是Xray高级版的利用方式。此后一些安全研究人员根据Xray的相关思路编写出了课直接回显的漏洞利用程序。比如下面这些项目。

- 

## 七、参考文章

- https://paper.seebug.org/1290/
- https://koalr.me/post/shiro-lou-dong-jian-ce/