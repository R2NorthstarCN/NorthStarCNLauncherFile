<!--
 * @Author: HK560
 * @Date: 2021-12-25 13:34:04
 * @LastEditTime: 2022-01-06 21:43:11
 * @LastEditors: HK560
 * @Description:
 * @FilePath: \NorthStarCN_WIKIh:\github\ttf\NorthStarCNLauncherFile\README.md
 * My Blog: https://blog.hk560.top
-->
# NorthStarCNLauncherFile
NorthStarCN客户端 1.4.0 更新
- 基於NorthStar版本 1.4.0

NorthstarLauncher:
- 添加版本来源信息
- 强制IPV4，目前IPV6仍然不支持
- 弃用```Tier0_InitOrigin hook```
- 在InitialiseNorthstar中初始化crul避免引发其他问题
- 分隔出通用crul设置，再次添加`-msinsecure`设置
- 为大多数安装错误添加更多清晰的错误信息
- 启用curl日志输出到windows的控制台
- 修复语言选择问题，减少“files corrupted”错误，现在会尽可能的清晰显示Origin错误信息
- 启用rpak文件系统的hooks
- 不再强制netchan在Level Transitions期间受到限制，现在可以为该限制进行设置
- 初步完成封禁系统
- 移除覆写`max_players`的日志信息
- 添加关闭spewfunc日志的选项
- 为封禁系统增加断连功能
- 增加`unban`命令
- 添加 wsock32 代理！（用起来真的不错）
- 同样存储`ShouldLoadNorthstar()`到wsock32代理
- 使wsock3代理成为可用选项
- 添加`clearbanlist`命令
- 添加聊天频率限制和抓取聊天信息系统
- 更改部分架构修复win7错误问题
- 重构以允许服务器使用心跳包重新注册它们

NorthstarMods:
- 修复私人房间的模式偏移
- 修复游戏结束时候重播视角和能够重生的问题
- 删除显示刷新表的垃圾控制台信息
- 禁用战争游戏开始时的副手武器
- 为泰坦和铁驭装备返回时增加计数器检查
- 修复私人比赛模式被服务器浏览器影响的问题
- 允许烈火战场模式游玩非烈火战场地图
- 修复战争游戏开头动作问题
- 修复比赛设置的一些问题
- 修复飞船跳机阶段复活在错误的队伍
- 添加关闭铁驭内部碰撞的设置
- 修复一些非法字符
- 修复离开泰坦后空速重置问题
- 修复泰坦争斗开头可能会引发崩溃的问题
- 集成最后一发和幽灵猎杀模式
- 更新了_ai_mp.gnut文件
- 确保完全经过验证之后才解锁北极星启动按钮
- 天幕骇客增加可用地图
- 修复禁用武器时候切换装备造成的问题
- 在重新计算连杀之前重置连杀数
- 强化修复

NorthstarMasterServer:
- 重构以允许服务器使用心跳包重新注册它们

原文：

NorthstarLauncher:
- add version resource
- force ipv4 while ipv6 is still unsupported
- 弃用```Tier0_InitOrigin hook```
- 在InitialiseNorthstar种初始化crul避免引发其他问题
- Isolate out common curl options and add -msinsecure option again
- Add more clear error message for the most common install mistake
- log curl output to the windows console
- Language selection/detection fixes, no more "files corrupted" error, will throw the proper Origin error now :D
- setup for rpak filesystem hooks
- don't enforce netchan limits during level transitions, change how limit mode works
- initial work for ban system
- remove logging for overwriting max_players
- add the ability to disable spewfunc logging
- add disconnects to ban system
- add unban command
- add wsock32 proxy!!! (it works quite nicely)
- restore ShouldLoadNorthstar() to wsock32 proxy as well
- make wsock32 proxy opt-in
- add clearbanlist command
- add chat ratelimits and system for hooking chat messages
- Merge pull request #19 from p0358/main
- change -waitfordebugger check to use CommandLine()
- refactor to allow servers to reregister themselves in heartbeat


NorthstarMods:
- fix modes being offset in private match
- fix end of game replay perspective and repsawns during replays
- Remove printt refresh table; spams console
- Disable offhand weapons during wargames intro
- Added a pro screen check to titan to pilot loadout retrieval.
- fix private match modes being affected by server browser
- allow lf to work on non-lf maps
- Update northstar_client_localisation_japanese.txt
- Sync wargames intro animations
- add fd boost shop boosts
- fix race condition with games being won in a death callback for roundwinning killreplays
- Fix portuguese localisation line endings
- Add .gitattributes
- fix dropship intro using the wrong team's spawns
- add the ability to disable inter-pilot collision
- Translate coop portuguese strings
- Reencode translations as UTF-16 little endian
- Fix whitespace
- Fix airaccel reset on leaving titan (#51)
- fix potential crash in ttdm intro
- adds OITC and Hidden gamemodes
- adds hidden and OITC localisation
- Adds OITC and Hidden to playlist
- adds OITC and Hidden to mod.json
- Update _ai_mp.gnut
- ensure game is fully authenticated before unlocking launch northstar button
- added fastball config for map complex
- added fastball config for map forwardbase kodai
- added fastball config for map colony
- [feat] adding translations for hidden game mode
- [feat] adding translation for 'one in the chamber' game mode
- [feat] no_pilot_collision key
- Fix changing loadouts bypassing restricted weapons (#52)
- Resets killstreak first before calculating kills.
- Big Boost/Earn Meter Fixes!

NorthstarMasterServer:
- refactor to allow preexisting gameservers to register in heartbeat