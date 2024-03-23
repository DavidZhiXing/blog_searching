# Twitter高级搜索技巧

如果偶尔使用Twitter的搜索，你有可能会跟我当初一样，觉得Twitter的搜索功能极其难用，尤其是对中文的搜索非常不友好。不过，掌握一些基本的搜索指令之后，你会发现情况大不相同。

Twitter在[这里](https://developer.twitter.com/en/docs/twitter-api/v1/rules-and-filtering/search-operators)列出了他支持的搜索指令，本文我选择一些我认为比较常用的指令做讲解，如果想获取全部指令，可以去官网。

1、匹配方式与基本运算符

搜索多个单词，默认是“与”/And的关系，这个和主流搜索引擎是一样的。比如搜索 tequila sunrise ，则会搜索同时包括“tequila”以及“sunrise”的推，二者位置可以任意。

如果希望包含其中任一词，则可使用“**OR**”指令，如 tequila OR sunrise，则会搜索包含任一或者二者的推文。

排除可以使用减号“**–**”指令，比如搜索 tequila -sunrise，则搜索只包含tequila而没有sunrise的推文。

如果给搜索词加上双引号，**“**tequila sunrise**“** ，则属于词组匹配，只会搜索到完全包含这个词组的推文。

2、高级指令

**#**，这个是hashtag标签，搜索加了对应hashtag的推文，如 #tequila

**from:**，指定发推的人，只搜索指定人发出的推文，如 [china from:elonmusk](https://twitter.com/search?q=china from%3Aelonmusk)

**list:**，搜索某个list里面的推文，比如 [![🙂](https://s.w.org/images/core/emoji/14.0.0/svg/1f642.svg) list:1318663032717922304](https://twitter.com/search?q=%3A) list%3A1318663032717922304)，笑脸符号是Twitter认为表达了开心这种情绪的推文。list后面的长串数字是list的ID，这个可以在查看list时的URL上找到

**to:**，跟from同一个逻辑，是发送给某个指定用户的推文，比如 [![🙁](https://s.w.org/images/core/emoji/14.0.0/svg/1f641.svg) to:elonmusk](https://twitter.com/search?q=%3A( to%3Aelonmusk)，哭脸符号表达悲伤的情绪。

**@**，这个表示提到了某个人的推文，比如 [? @elonmusk](https://twitter.com/search?q=%3F %40elonmusk)，问号表示了该推文包含一个问句。

**filter:**，这个后面可以接一些具体的内容，比如：

- filter:media，搜索只包含有媒体的推文，媒体包括图片和视频；
- -filter:retweets，排除转推；
- filter:native_video，包含自己上传的视频，Amplify video, Periscope, 或者 Vine 内容；
- filter:images，包含图片的推文，包括被鉴定为图片的网址，所以包含了instagram的图片链接，也是可以识别到的；
- filter:twimg，twitter自己的图片服务器上的图片，pic.twitter.com
- filter:links，包含了网址的推文

**url:**，推文指向的网址中包含了某个关键字。比如 [url:amazon](https://twitter.com/search?q=url%3Aamazon)，搜索链接中包含amazon的推文。

**since:**，从哪个日期起搜索，格式 年-月-日，比如 [web3 since:2022-01-01](https://twitter.com/search?q=web3 since%3A2022-01-01)

**until:**，跟since一样，表示截止日期。需要注意的是，until会限制搜索截止日期前7天的结果，也就是说最多显示指定日期前一个星期的推文

**lang:**，指定搜索语言。比如只搜索中文结果，[nft lang:zh](https://twitter.com/search?q=nft lang%3Azh)，twitter支持的语种指令遵从[ISO 639-1 codes](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)，都是两位的

**result_type:**，结果排序，有三个选项，result_type:recent 表示显示最新，result_type:popular 表示显示最热，result_type:mixed 混合以上两种

**count:**，一页展示多少条搜索结果，默认15，最大100



以上指令可以混合使用，多重限定，如此应可找到你想要的大部分搜索内容。

我希望Twitter可以更多加入用户相关的指令，比如国别、性别、年龄、行业、偏好etc，当然是在尊重用户隐私的前提下。

原文 [Twitter高级搜索技巧](https://midstarter.com/tech/65/)
