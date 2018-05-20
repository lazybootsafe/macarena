# macarena
玛卡瑞纳

Go语言扫描器将于此更新。
正在coding。
今天520，我还在写代码。
原本的扫描器叫证道玉，是一个内部使用的工具，为我个人和团队获得了大量的xx。
原功能架构：
```
zhengdaoyu 证道玉扫描器

├─ActiveScan 主动扫描系统
│  │
│  ├─Infornation 信息收集模块
│  │  ├─PortScan 端口扫描功能
│  │  ├─subDomain 子域名枚举功能
│  │  ├─URLHack 搜索引擎hack功能
│  │  ├─whois whois信息收集功能
│  │  ├─whatCMS cms中间件识别功能
│  │  ├─whatWAF 探测WAF功能
│  │  └─WeakFile 敏感文件扫描功能
│  ├─Spider 爬虫模块
│  │  ├─SuperSpdier 启发式web爬虫功能
│  │  └─GamFinder 社交平台（twitter，facebook等）爬虫功能
│  ├─VulnCheck 漏洞检测模块
│  │  ├─Inject 注入检测功能
│  │  │  ├─Sqlmap-Api sqlmapapi接口调用子功能
│  │  │  ├─FingerInject 自定义根据各种情景变化注入子功能
│  │  │  └─X-waf 自动化爆破waf子功能
│  │  ├─PocScan 批量poc测试功能
│  │  ├─xss xss漏洞检测功能，包含dom检测方式
│  │  ├─RCE 命令执行/代码执行检测功能
│  │  ├─Download 下载敏感文件功能
│  │  └─Other0day 如文件操作、ssrf、0day poc等其他检测功能
│  ├─Report 报告模块
│  │  ├─HTML 导出HTML报告功能
│  │  ├─PDF 导出PDF报告功能
│  │  └─Log 扫描日志功能
│  └─WebUI （未完成）web界面模块
│
├─PassiveScan 被动扫描系统
│  │
│  ├─DataSorting 流量镜像数据源数据处理模块
│  ├─LogSorting 日志数据源数据处理模块
│  ├─SecCheck 漏洞验证模块
│  ├─Proxy 代理以及任务分发模块
│  ├─Report 被动扫描日志模块
│  └─WebUI web界面模块
│
├─AuditScan 代码审计系统
│  │
│  ├─CodeAudit 白盒代码审计模块
│  │  ├─StaticAudit 静态代码扫描审计功能（AST）
│  │  └─DynamicAudit 动态代码跟踪审计功能（仅php）
│  ├─GlassAudit 灰盒代码审计模块
│  │  ├─skywolfapi 调用360 skywolf api 进行代码追踪审计功能
│  │  └─GlassAudit 插桩式代码审计功能
│  └─Report 报告模块
│
├─F-DeepLearning 深度学习调度分发与训练系统（基于HDFS java实现）
│  │
│  ├─F-Learning 深度学习调度模块（已完成TensorFlow caffe pytorch Keras XGBoost等常用框架集成）
│  │  ├─F-DL-Master 负责输入数据分片、启动及管理Container、执行日志保存等功能
│  │  ├─F-DL-Client 负责启动作业及获取作业执行状态功能
│  │  ├─F-DL-Container 作业的实际执行者，负责启动Worker或PS进程，监控并向汇报进程状态等功能
│  │  └─WebUI web界面功能
│  ├─Rules 训练数据集及规则库模块
│  ├─PyTorch-self 定制化pytorch模块（未完成）
│  └─TensorFlow-Self 定制TF模块（定制版TensorFlow与扫描器功能接入，由TensorFlow训练出切实可行
│                              的payload规则，将规则赋予scanner测试性能。）
│
├─ControlRobot 机器人总控制系统（基于chatbot 功能未完善）
│  │
│  ├─qqapi qq接口robot
│  └─wxapi 微信接口robot

ps：其中x-waf来自于大佬 https://github.com/3xp10it/bypass_waf 的项目;
尽管我重构了相当多代码，但是依然使用大佬项目名字以示尊重。
其中被动扫描模块参考了nagascan的proxy模式。
```

现在的macarena是此扫描器的go语言版本，将逐一在此开源，学习开发过程见Go-learning项目；
如对我其他的人工智能、深度学习、算法等项目感兴趣的话，移步到另一github。
