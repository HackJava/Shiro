# HackShiro

本项目创建于2020年8月11日。记录自己在学习Shiro漏洞过程中遇到的一些知识。本项目会持续更新，最近的一次更新时间为2022年5月15日。作者：[0e0w](https://github.com/0e0w)

- [01-Shiro基础知识]()
- [02-Shiro框架识别]()
- [03-Shiro漏洞汇总]()
- [04-Shiro漏洞检测]()
- [05-Shiro漏洞利用]()
- [06-Shiro靶场环境]()

## 01-Shiro基础知识
- https://github.com/apache/shiro
- http://greycode.github.io/shiro/doc/reference.html

## 02-Shiro框架识别

- 请求包的cookie中存在rememberMe字段。
- 响应包中存在rememberMe=deleteMe字段。
- 请求包中存在rememberMe=x时，响应包中存在rememberMe=deleteMe。
- 检测工具：Banli.exe is shiro

## 03-Shiro漏洞汇总

- CVE-2020-17523
- CVE-2020-17510
- CVE-2020-13933
- CVE-2020-11989#Apache Shiro身份验证绕过漏洞
- CVE-2016-6802#Shiro Padding Oracle Attack
- CVE-2016-4437#Shiro rememberMe反序列化漏洞

## 04-Shiro漏洞检测

- KEYS
- GCM
- Gadget
  - CommonsBeanutils1
  - CommonsBeanutils1_192
  - CommonsBeanutilsAttrCompare
  - CommonsBeanutilsAttrCompare_192
  - CommonsBeanutilsObjectToStringComparator
  - CommonsBeanutilsObjectToStringComparator_192
  - CommonsBeanutilsPropertySource
  - CommonsBeanutilsPropertySource_192
  - CommonsBeanutilsString
  - CommonsBeanutilsString_192
  - CommonsCollections2
  - CommonsCollections3
  - CommonsCollectionsK1
  - CommonsCollectionsK2
  - CommonsBeanutils1
  - CommonsBeanutils1_192
  - CommonsBeanutilsAttrCompare
  - CommonsBeanutilsAttrCompare_192
  - CommonsBeanutilsObjectToStringComparator
  - CommonsBeanutilsObjectToStringComparator_192
  - CommonsBeanutilsPropertySource
  - CommonsBeanutilsPropertySource_192
  - CommonsBeanutilsString
  - CommonsBeanutilsString_192
  - CommonsCollections2
  - CommonsCollections3
  - CommonsCollectionsK1
  - CommonsCollectionsK2
  - [ ] 测试:CommonsBeanutils1_192  回显方式: TomcatEcho
    [x] 测试:CommonsBeanutils1_192  回显方式: SpringEcho
    [x] 测试:CommonsCollections2  回显方式: TomcatEcho
    [x] 测试:CommonsCollections2  回显方式: SpringEcho
    [x] 测试:CommonsCollections3  回显方式: TomcatEcho
    [x] 测试:CommonsCollections3  回显方式: SpringEcho
    [x] 测试:CommonsCollectionsK1  回显方式: TomcatEcho
    [x] 测试:CommonsCollectionsK1  回显方式: SpringEcho
    [x] 测试:CommonsCollectionsK2  回显方式: TomcatEcho
    [x] 测试:CommonsCollectionsK2  回显方式: SpringEcho
    [x] 测试:CommonsBeanutilsString  回显方式: TomcatEcho
    [x] 测试:CommonsBeanutilsString  回显方式: SpringEcho
    [x] 测试:CommonsBeanutilsString_192  回显方式: TomcatEcho
    [x] 测试:CommonsBeanutilsString_192  回显方式: SpringEcho
    [x] 测试:CommonsBeanutilsAttrCompare  回显方式: TomcatEcho
    [x] 测试:CommonsBeanutilsAttrCompare  回显方式: SpringEcho
    [x] 测试:CommonsBeanutilsAttrCompare_192  回显方式: TomcatEcho
    [x] 测试:CommonsBeanutilsAttrCompare_192  回显方式: SpringEcho
    [x] 测试:CommonsBeanutilsPropertySource  回显方式: TomcatEcho
    [x] 测试:CommonsBeanutilsPropertySource  回显方式: SpringEcho
    [x] 测试:CommonsBeanutilsPropertySource_192  回显方式: TomcatEcho
    [x] 测试:CommonsBeanutilsPropertySource_192  回显方式: SpringEcho
    [x] 测试:CommonsBeanutilsObjectToStringComparator  回显方式: TomcatEcho
    [x] 测试:CommonsBeanutilsObjectToStringComparator  回显方式: SpringEcho
    [x] 测试:CommonsBeanutilsObjectToStringComparator_192  回显方式: TomcatEcho
    [x] 测试:CommonsBeanutilsObjectToStringComparator_192  回显方式: SpringEcho
- 回显
  - LinuxEcho
  - SpringEcho1
  - SpringEcho2
  - TomcatEcho
  - TomcatEcho2
  - JBossEcho
  - WeblogicEcho
  - ResinEcho
  - JettyEcho
  - AutoFindRequestEcho
  - WriteFileEcho
- 可以出网
- 不可出网

## 05-Shiro漏洞利用

本项目注重漏洞利用效果。详细的漏洞分析请参考本站的关于Shiro分析的文章。Shiro命令回显最早是Xray高级版的利用方式。此后安全研究人员根据Xray的相关思路编写出了可直接回显的漏洞利用程序。

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
- https://github.com/Ares-X/shiro-exploit
- https://github.com/j1anFen/shiro_attack
- https://github.com/Veraxy01/Shiro-EXP
- https://github.com/admintony/shiro_rememberMe_Rce
- https://github.com/j1anFen/ysoserial_echo
- https://github.com/Veraxy00/Shiro-EXP
- https://github.com/mmioimm/shiro_echo
- https://github.com/dr0op/shiro-550-with-NoCC
- https://github.com/M4da0/ShiroExploit
- https://github.com/inspiringz/Shiro-721
- https://github.com/KpLi0rn/ShiroTool
- https://github.com/KpLi0rn/ShiroExploit
- https://github.com/safe6Sec/ShiroExp
- https://github.com/longofo/PaddingOracleAttack-Shiro-721
- https://github.com/myzxcg/ShiroKeyCheck

## 06-Shiro靶场环境

- https://vulhub.org
- https://fofapro.github.io/vulfocus

## 07-Shiro参考资源

- https://paper.seebug.org/1290
- https://koalr.me/post/shiro-lou-dong-jian-ce