<!--
 * @Author: HK560
 * @Date: 2021-12-25 13:34:04
 * @LastEditTime: 2021-12-29 11:26:23
 * @LastEditors: HK560
 * @Description:
 * @FilePath: \NorthStarCN_WIKIh:\github\ttf\NorthStarCNLauncherFile\README.md
 * My Blog: https://blog.hk560.top
-->
# NorthStarCNLauncherFile
NorthStarCN客户端 1.2.0
基於NorthStar版本 1.2.0

- 加入简体中文聊天MOD，现在您可以在聊天框输入简体中文，同样装了该MOD的玩家便能看到发送的简中信息
- 修复主界面右侧面板不能打开链接问题
- 修改了主界面样式
- 添加了服务器浏览器mod

1.2.0 更新：
- 添加更多AddSelfToServerList失败的描述信息
- 添加更多简单的崩溃日志信息和转储文件
- 确保使用添加debugger时候不会出现异常日志
- 支持 setplaylistvaroverride 多次覆盖 因为用命令行太烦了
- 支持只playlist中控制服务器最大玩家数
- 添加对于服务器请求的重试逻辑
- 对于MasterServer使用libcurl 因为libhttp看起来有问题而且有严重错误报告

- 给枪械模式添加更多细节翻译（指的是给国际版英语的）
- 添加 ns_private_match_countdown_length 并修复了布局和运输撤离存在的问题
- 修复了自动地图轮换在地图改变之后不会返回
- 修复了一些崩溃问题和在泰坦争斗中的撤离问题
- 修复了击杀回放奇奇怪怪的问题
- 设置撤离船的伤害类型为`DF_GIB`
- 修复了追迷藏的噪音太频繁还有一些断连检测
- 添加日语法语文本（国际服的，我们不需要）
- 修复了切换铁驭装备可能会让你从操控泰坦变成操控铁驭形态的泰坦并造成崩溃
- 修复0xc0000005错误，和橘子可能导致的问题

已知问题：
- 拖动服务器列表滚动条可能会导致崩溃，是服务器浏览器插件导致的

1.2.0 Org：
- add more descriptive message for AddSelfToServerList failure
- add better native crash logging and minidump creation
- ensure exception logging doesn't happen when a debugger is attached
- make setplaylistvaroverride support multiple overrides since commandline is weird
- control server max players in playlist
- add retry logic to masterserver requests
- move to libcurl for masterserver as libhttp seems to be buggy and has bad error reporting

 NorthstarMods:
- [fix] adding details to gungame translation
- add ns_private_match_countdown_length and fix flyout and evac issue
- fix automatic map rotation not returning after map change
- fix some crashes and evac playing in ttdm
- fix general killreplay weirdness
- set evac ship destruction damage type to DF_GIB
- fix hide and seek noises being too common and some general disconnection checks
- Create northstar_client_localisation_japanese.txt
- Merge pull request #5 from Alystrasz/chore/french-translations
- Merge pull request #18 from Zetryox/main
- Merge pull request #11 from greishuhs/main

