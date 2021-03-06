# 清除Win10内置应用
## 环境
- 系统：Windows 10 Enterprise
- 版本：1709
- 处理器：Intel(R) Core(TM) i7-7700K CPU @ 4.20GHz
- 内存：16.0GB
- 类型：64位操作系统 64位处理器
## 步骤
1. 使用'win+x'组合键运行"Windows PowerShell(Admin)";
2. 输入命令删除相应应用：
    - OneNote：`Get-AppxPackage *OneNote* | Remove-AppxPackage`；
    - XBox：`get-appxpackage *xbox* | remove-appxpackage`；
    - 邮件和日历：`Get-AppxPackage *communi* | Remove-AppxPackage`；
    - 人脉：`get-appxpackage *people* | remove-appxpackage`；
    - 闹钟：`get-appxpackage *alarms* | remove-appxpackage`；
    - 相机：`get-appxpackage *camera* | remove-appxpackage`；
    - 地图：`get-appxpackage *maps* | remove-appxpackage`；
    - 语音录音机：`get-appxpackage *soundrecorder* | remove-appxpackage`；
    - GetHelp：`get-appxpackage *help* | remove-appxpackage`；
    - Messaging：`get-appxpackage *messaging* | remove-appxpackage`；
3. 若要恢复内置应用，输入命令：`Get-AppxPackage -allusers | foreach {Add-AppxPackage -register "$($_.InstallLocation)appxmanifest.xml" -DisableDevelopmentMode}`。
