## 模块功能介绍

### CodeAudit模块

此AuditScan没必要使用Go语言改写。
```
─CodeAudit 白盒代码审计模块
  ├─StaticAudit 静态代码扫描审计功能
  |    ├─lib
  |    |    ├─analyzer.php
  |    |    ├─constructer.php
  |    |    ├─filer.php
  |    |    ├─function.php
  |    |    ├─printer.php
  |    |    ├─scanner.php
  |    |    ├─searcher.php
  |    |    ├─setting.php
  |    |    └─tokenizer.php
  |    ├─logs
  |    ├─reports
  |    ├─rules
  |    |    ├─normal
  |    |    |    ├─...xml
  |    |    |    └─...xml
  |    |    └─special
  |    |    |    ├─CodeIgniter
  |    |    |    ├─Drupal
  |    |    |    ├─Joomla
  |    |    |    ├─Laravel
  |    |    |    ├─ThinkPHP
  |    |    |    └─Wordpress
  |    ├─staticaudit
  |    |    |    ├─...py
  |    |    |    └─...py
  |    ├─tests
  |    |    ├─example
  |    |    ├─tests
  |    |    └─vulnerabilities
  |    └─web
  └─DynamicAudit 动态代码跟踪审计功能
```

- lib 脚本文件目录,配合DynamicAudit使用
- logs 日志输出目录
- reports 报告输出目录
- rules 规则目录
  - normal 一般通用规则目录
  - special 三大框架和三大CMS优化专用版规则目录
- staticaudit 核心代码目录
- tests 测试用例目录
  - example 测试样例目录
  - tests 单元测试目录
  - vulnerabilities 有漏洞的php文件目录
- web webui目录（空目录 未写功能）

### 已经支持漏洞类型：
```
           OWASP正式名称                 中文命名
----------------------------------++--------------------
Misconfiguration                      	错误的配置
Server-Side Forge	                    服务端伪造
Cross-Site Script	                    跨站脚本
Cross-Site Request Forge	            跨站请求伪造
SQL Injection	                        SQL注入
Xpath Injection	                    Xpath注入
LDAP Injection	                        LDAP注入
XML External Entity Injection	        XML实体注入
Local/Remote File Inclusion	        文件包含漏洞
Code Injection                       	代码注入
Command Injection                    	命令注入
Information Exposure	                信息泄露
Predictable Pseudorandom Generator   	可预测的伪随机数生成器
Session Fixation	                    SESSION固定
unSerialize	                        反序列化漏洞
Variables Override	                    变量覆盖漏洞
Weak Function	                        不安全的函数

```
