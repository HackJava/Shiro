# HackShiro

本项目创建于2020年8月11日。记录自己在学习Shiro漏洞过程中遇到的一些知识。本项目会持续更新，最近的一次更新时间为2020年10月09日。

- [0x01-Shiro基础知识](https://github.com/0e0w/HackShiro#%E4%B8%80shiro%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86)
- [0x02-Shiro漏洞汇总](https://github.com/0e0w/HackShiro#%E4%BA%8Cshiro%E6%BC%8F%E6%B4%9E%E6%B1%87%E6%80%BB)
- [0x03-Shiro框架识别](https://github.com/0e0w/HackShiro#%E4%B8%89shiro%E6%A1%86%E6%9E%B6%E8%AF%86%E5%88%AB)
- [0x04-Shiro漏洞检测](https://github.com/0e0w/HackShiro#%E5%9B%9Bshiro%E6%BC%8F%E6%B4%9E%E6%A3%80%E6%B5%8B)
- [0x05-Shiro漏洞利用](https://github.com/0e0w/HackShiro#%E4%BA%94shiro%E6%BC%8F%E6%B4%9E%E5%88%A9%E7%94%A8)
- [0x06-Shiro靶场环境](https://github.com/0e0w/HackShiro#%E5%85%ADshiro%E9%9D%B6%E5%9C%BA%E7%8E%AF%E5%A2%83)

## 一、Shiro基础知识
- http://greycode.github.io/shiro/doc/reference.html

## 二、Shiro漏洞汇总

本项目注重漏洞利用效果。详细的漏洞分析请参考本站的关于Shiro分析的文章。

- Shiro rememberMe反序列化漏洞：CVE-2016-4437（Shiro-550）
- Shiro Padding Oracle Attack：Shiro-721
- Apache Shiro身份验证绕过漏洞：CVE-2020-11989

## 三、Shiro框架识别

- 请求包的cookie中存在rememberMe字段。
- 响应包中存在rememberMe=deleteMe字段。
- 请求包中存在rememberMe=x时，响应包中存在rememberMe=deleteMe。

## 四、Shiro漏洞检测

## 五、Shiro漏洞利用

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
- https://github.com/pmiaowu/BurpShiroPassiveScan
- https://github.com/feihong-cs/ShiroExploit
- https://github.com/potats0/shiroPoc
- https://github.com/tangxiaofeng7/Shiroexploit
- https://github.com/fupinglee/ShiroScan

## 六、Shiro靶场环境

Shiro命令回显最早是Xray高级版的利用方式。此后一些安全研究人员根据Xray的相关思路编写出了课直接回显的漏洞利用程序。比如下面这些项目。

## 七、Shiro参考资源

- https://paper.seebug.org/1290/
- https://koalr.me/post/shiro-lou-dong-jian-ce/