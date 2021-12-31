<!--
 * @Author: HK560
 * @Date: 2021-12-25 13:34:04
 * @LastEditTime: 2021-12-31 12:00:10
 * @LastEditors: HK560
 * @Description:
 * @FilePath: \NorthStarCN_WIKIh:\github\ttf\NorthStarCNLauncherFile\README.md
 * My Blog: https://blog.hk560.top
-->
# NorthStarCNLauncherFile
NorthStarCN客户端 1.3.0 更新
- 基於NorthStar版本 1.3.0‘

NorthstarLauncher:
- 避免密码空请求
- 添加一些崩溃处理的堆栈跟踪
- 改为服务器token验证系统来验证游戏服务器信息，而不是以前的IP验证

NorthstarMasterServer:
- 修复当服务器描述为空参数的错误
- 添加 可选的env变量来信任代理
- 改为服务器token验证系统来验证游戏服务器信息，而不是以前的IP验证

NorthstarMods:
- 飞船信息更改，修复了当跳机时候无限强化武器的bug
- 修复 `ns_private_match_only_host_can_start`
- 修复了当玩家从泰坦下机丢失`menu_category`武器装备继而引发的游戏错误
- 修复了烈火战场夺旗之后断连造成的游戏崩溃
- 修复当玩家未死亡的时候`classic_mp 0`造成的游戏崩溃
- 修复ctf模式中当玩家夺旗后离开造成的问题
- 修复 burnmeter 和 fastball 造成的崩溃
- 阻止铁驭对铁驭中撤离阶段仍能得分
- 阻止小规模冲突中撤离阶段仍能得分
- 阻止泰坦争斗中如果tits打开了撤离阶段仍能得分
- 修复全图永久声纳问题
- 整合 Better.serverbrowser
- 修改了面板
- 修复在`EvacEpilogue` 和 `Postmatch`游戏状态下丢失重生期限的问题
- 修复speedball和空投造成的崩溃
- 修复4:3屏幕ui布局问题
- 使用`GetPrivateMatchModes`取代硬编码的serverbrowserModes
- 防止在新玩家加入时候再次设置最后一名幸存者
- 修复超出数组访问的问题，添加服务器计数
- 优化ui
- 修复一些其他杂七杂八的问题


原文：

NorthstarLauncher:
- escape password entry request
- add proper stack traces to crash handler
- move to server auth token system for verifying gameserver auth messages, rather than ip


NorthstarMasterServer:
- Fix error when server description is empty
- adds optional env variable to trust proxy
- move to server auth token system for verifying gameserver auth messages, rather than ip

NorthstarLauncher:
- dropship intro changes and fix for infinite amped weapons on disembark
- fix ns_private_match_only_host_can_start
- Fixed the game erroring when disembarking from a titan and the player has a weapon missing "menu_category" equipped (like titan weapons).
- Add portuguese translations
- fix crash when disconnecting from livefire with flag held
- fix classic_mp 0 crashing if players are alive
- fix ctf if a player leaves when holding the flag
- fix burnmeter and fastball crashes
- Stop Pilots vs Pilots from scoring during the epilogue
- Stop Skirmish from scoring during the epilogue
- Stop Skirmish from scoring during the epilogue
- Stop Titan Brawl from scoring during the epilogue if tits turned on lol
- Add northstar_client_localisation_german.txt
- fixed map hack permanent sonar (real)!!!
- Commit Better.serverbrowser
- Change panel
- Fix missing respawn grace during EvacEpilogue and Postmatch gamestate
- speedball and dropship crash fixes
- Fix #17
- Merge pull request #34 from abarichello/fix/dropship-offhand-weapon
- use GetPrivateMatchModes rather than hardcoding serverbrowser modes
- Prevents setting last survivor again when new player connects
- Add Russian locals
- Fix out of range array access; add server count
- Add server count; improve UI