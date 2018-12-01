# 说明
这个库是基于

https://github.com/codemayq/chaotbot_corpus_Chinese

原来库把所有的文件都放在了一个压缩文件里面，并且使用的时候需要自己去生成。

我把数据下载下来，并且做了预处理。大家可以分别下载。

以下是原来的说明
----

# 生成结果
每个来源的语料分别生成一个独立的*.tsv文件，都放在新生成的clean_chat_corpus文件夹下。

生成结果格式为 tsv格式，每行是一个样本，先是query，再是answer
```
query \t answer
```

该库搜集了包含
- chatterbot
- 豆瓣多轮
- PTT八卦语料
- 青云语料
- 电视剧对白语料
- 贴吧论坛回帖语料
- 微博语料
- 小黄鸡语料

共8个公开闲聊常用语料和短信，白鹭时代问答等语料。

并对8个常见语料的数据进行了统一化规整和处理，达到直接可以粗略使用的目的。

# 数据来源及说明
语料名称 | 语料数量 | 语料来源说明 | 语料特点 | 语料样例 | 是否已分词|对应文件
---|---|---|---|---|---|---
chatterbot | 560 | 开源项目 | 按类型分类，质量较高  | Q:你会开心的 A:幸福不是真正的可预测的情绪。 | 否 |chatterbot.tsv.zip
douban（豆瓣多轮） | 352W | 来自北航和微软的paper, 开源项目 | 噪音相对较少，原本是多轮（平均7.6轮）  | Q:烟台 十一 哪 好玩 A:哪 都 好玩 · · · · | 是 |douban_single_turn.tsv.zip
ptt（PTT八卦语料） | 40W | 开源项目，台湾PTT论坛八卦版 | 繁体，语料较生活化，有噪音  | Q:为什么乡民总是欺负国高中生呢QQ	A:如果以为选好科系就会变成比尔盖兹那不如退学吧  | 否 | ptt.tsv.zip
qingyun（青云语料） | 10W | 某聊天机器人交流群 | 相对不错，生活化  | Q:看来你很爱钱 	 A:噢是吗？那么你也差不多了 | 否 | qingyun.tsv.zip
subtitle（电视剧对白语料） | 274W | 开源项目，来自爬取的电影和美剧的字幕 | 有一些噪音，对白不一定是严谨的对话，原本是多轮（平均5.3轮）  | Q:京戏里头的人都是不自由的	A:他们让人拿笼子给套起来了了 | 否 |subtitle.tsv.zip
tieba（贴吧论坛回帖语料） | 232W | 偶然找到的 | 多轮，有噪音  | Q:前排，鲁迷们都起床了吧	A:标题说助攻，但是看了那球，真是活生生的讽刺了 | 否 | tieba.tsv.zip
weibo（微博语料） | 443W | 来自华为的paper | 仍有一些噪音  | Q:北京的小纯洁们，周日见。#硬汉摆拍清纯照# A:嗷嗷大湿的左手在干嘛，看着小纯洁撸么。 | 否 |weibo.tsv.zip
xiaohuangji（小黄鸡语料） | 45W | 原人人网项目语料 | 有一些不雅对话，少量噪音 | Q:你谈过恋爱么	A:谈过，哎，别提了，伤心..。 | 否 |xiaohuangji.tsv.zip

语料名称 | 语料原始URL（即出处，尊重原始版权） 
---|---
chatterbot | https://github.com/gunthercox/chatterbot-corpus/tree/master/chatterbot_corpus/data/chinese
douban（豆瓣多轮） | https://github.com/MarkWuNLP/MultiTurnResponseSelection 
ptt（PTT八卦语料）| https://github.com/zake7749/Gossiping-Chinese-Corpus 
qingyun（青云语料） | 无 
subtitle（电视剧对白语料） | https://github.com/fateleak/dgk_lost_conv 
tieba（贴吧论坛回帖语料）  | https://pan.baidu.com/s/1mUknfwy1nhSM7XzH8xi7gQ 密码:i4si 
weibo（微博语料）  | 61.93.89.94/Noah_NRM_Data/ 
xiaohuangji（小黄鸡语料） | https://github.com/candlewill/Dialog_Corpus 


# 使用方法
链接:https://pan.baidu.com/s/1HlxwgryXZBfuVljzGxd-6A  密码:67iq

# 结果的使用
这个就根据每个人不同的情况自主使用即可

个人对于聊天机器人方向实践也不是很多，以下一篇之前写的知乎专栏供参考
**《从产品完整性的角度浅谈chatbot》**

https://zhuanlan.zhihu.com/p/34927757

文章粗略讲解了如下一些方面，介绍了聊天机器人在实际产品化过程中可能遇到的问题和解决办法。

1. chatbot自身人格的设置
1. 产品上线需要考虑的敏感词处理
1. 文本检索模型的使用
1. 文本生成模型的使用
1. 回答打分机制
1. 万能回答的使用策略
1. 多媒体消息的处理
1. 产品模型部署的问题

# 版权说明
本项目为非商业项目，为纯搜集和汇总资料，如有侵权，请在issue下留言。
