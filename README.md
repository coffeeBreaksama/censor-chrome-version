# censor-chrome-version
信息审核部门用

有事请POPO我。下载在右上角clone and download按钮。历史版本下载在左上角commits。<br>
**通用模块要点链接时，按小键盘1关掉鼠标动作再点就行！再按打开！**<br>

`2017/7/11`<br>
优化邮件位置跳转逻辑，刷新页面时，第一条时自动选中但不跳转到位置上，方便修改选中类别。<br>
切换页面，点击正文等丢失焦点的行为时，重新获得焦点时也不再跳转位置。<br>
修复一些小BUG。<br>


`2017/7/15`<br>
给小模块计时器添加声音提醒以便中午休息时候睡觉，自用型功能，只有小模块的通知才会有，POPUP页面可关闭。<br>
针对易盾模块文本审核添加自动查删脚本，为保证准确率就不开放使用了，仅在出现某一固定类型固定关键字时使用。<br>


`2017/7/9`<br>
popup界面增加小模块/易盾切换刷新按钮，在打开计时器按钮下面：<br>
在游览器切换页面标签时，若切换到的标签属于通用、易盾的域名，自动刷新页面。<br>

`2017/7/8`<br>
修改优化快捷键，这是hxf敲定的按键版本，用着觉得不舒服找他。或者自己单独想用其他的按键的，联系我给你单独改一版本<br>
修复提交换页后，定位仍在最后一条的问题。<br>
**keydown改成keyup! 也就是说按键松开的时候才生效，避免按住按键时连续不断的审核过去**<br>
目前按键表：<br>
`空格`   忽略 按下后将跳转并选中至下一条目<br>
`R`   正常 按下后将跳转并选中至下一条目<br>
`W`   广告邮件 按下后将跳转并选中至下一条目<br>
`E`   订阅邮件 按下后将跳转并选中至下一条目<br>
`Q`   垃圾邮件 按下后将跳转并选中至下一条目<br>
`1` 标题聚类/URL/概要标题/趋势分析/文本 <br>
`3` 选中文本(上面没有标题聚类时)<br>
`2` 不入库<br>
`D`   封禁 按下后将跳转并选中至下一条目，强制封禁为防止误点不设快捷键<br>
`D`   拒收 按下后将跳转并选中至下一条目<br>
`↑,↓` 选中上一条,下一条<br>

`2017/7/8`<br>
优化邮件审核判断生效逻辑，增加生效标签：低分聚类审核与邮件标注审核<br>
在popup界面增加一个打开所有小模块的按钮，更换通知图标<br>
出现清原创漫画的通知时，点击通知打开原创页面，若以打开则跳转<br>

`2017/7/4`<br>
优化邮件审核判断生效逻辑，仅对审核的两个标签生效。质检标签不生效<br>

`2017/6/28`<br>
邮件审核增加适配封禁`D`与垃圾`Q`，适配企业邮，vip，发信模块。<br>
在切换窗口时下取消选中邮件，具体表现为选中邮件失去背景色，需重新选中邮件。<br>
**用鼠标选中邮件时,请不要点邮件的正文区域！点击正文区域意味着取消选中！**<br>


`2017/6/24`<br>
修改邮件审核模式，增加邮件审核快捷键。<br>
此版本为初稿测试版本，正在和hxf敲定具体快捷键。<br>
**鼠标点击邮件条目（除邮件正文区域）以选中邮件，选中之后邮件变色代表此封邮件已选中。<br>
在选中邮件的前提下，按以下快捷键审核(比如说按5选中"标题聚类"，再按2选中"正常"并自动调至下一条)：<br>
以下数字均为字母键上的数字键，快捷键仅对当前选中条目生效。**<br>
`空格`   忽略 按下后将跳转并选中至下一条目<br>
`R`   正常 按下后将跳转并选中至下一条目<br>
`W`   广告邮件 按下后将跳转并选中至下一条目<br>
`E`   订阅邮件 按下后将跳转并选中至下一条目<br>
`Q`   垃圾邮件 按下后将跳转并选中至下一条目<br>
`1` 标题聚类/URL/概要标题/趋势分析/文本 <br>
`3` 选中文本(上面没有标题聚类时)<br>
`2` 不入库<br>
`D`   封禁 按下后将跳转并选中至下一条目，强制封禁为防止误点不设快捷键<br>
`D`   拒收 按下后将跳转并选中至下一条目<br>
`↑,↓` 选中上一条,下一条




`2017/6/11`<br>
云音乐消息，看着某些音乐人天天给人私信发自己的歌单广告，心中真的是一万只草泥马奔腾。老子在这删，你在那边发，还TM的每天都坚持不懈的发，拉黑又来投诉又导致我被领导骂。我真的是要被气死了。<br>
So,增加一键自动删除`（快捷键小数字键盘2）`，在未审核中自动按列表搜索关键字并且删除相关私信，列表搜索完自动停止。关键字列表暂时不开放编辑省得你们瞎搞乱删。以下为目前关键词列表：<br>
	delWord[0] = "做不一样的音乐";//对就是这个罗傻X，我无数次强忍着把他拉黑永久的冲动。<br>
	delWord[1] = "精液";<br>
	delWord[2] = "这是本人真的私信！";//这B我也见过很多次了。<br>
	delWord[3] = "kg2";<br>
	delWord[4] = "kugou";<br>

`2017/6/10`<br>
修复某些地方无法在设置栏目打字的BUG。

`2017/6/5`<br>
护眼模式适配文本标注，取消右键提交按钮。有输入框的时候，空格确定，右键打*号，屏蔽1234按钮防止乱提交。

`2017/6/4`<br>
因为发现偶尔有时候要加黑用户时，鼠标就不管用的问题。现在增加鼠标动作的开关，绑定在数字键盘1上，也就是按一下关闭鼠标动作。再按开启。 

`2017/6/4`<br>
先停止增加新功能，我有新玩具了，研究ML去了，但愿剩下的3个月不到的时间内能出个版本？有BUG反馈一下，反正以后只修复BUG，省时省力嘛。

`2017/6/3`<br>
刚刚才发现的自动滚动保存时间间隔的一个BUG，现在修复了。火狐版本反正没有保存时间间隔的功能，我就懒得改了。增加小键盘0键打开小模块5个标签，在随便哪个gcweb网址内连按5次0就行。

`2017/6/3`<br>
在文字审核中，Q按钮为详细内容翻至下页，到底时按Q回顶部。使用说明里面忘了写了，应该还有其他杂七杂八我自己都忘了的功能，自行研究去吧。
