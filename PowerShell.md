参考：
https://blog.csdn.net/weixin_34238633/article/details/88762667
https://www.pstips.net/powershell-alias.html

1.Scoop介绍  
  window包管理器包管理器
Scoop常用命令总结
  查看已安装的包-scoop list
  更新-scoop update
自定义Scoop命令别名
  注意：对于系统默认设定的别名，不可在删除此别名之前重新对这个别名赋值，PowerShell中还有一个命令New-Alias，该命令和Set-Alias基本功能一样，只是前者不能更改别名，只能创建别名。当试图使用New-Alias命令创建已存在的别名时，会报错
  创建别名前先查看已存在的别名，确认不存在才能正确创建别名否则别名创建失败。
  Get-Alias 查看别名
  在PowerShell配置文件添加别名
  # scoop
  function sls {scoop list}
  function sud {scoop update}
  function suda {scoop update *}
  function scla {scoop cleanup *}
  function sst {scoop status}
  function scu {scoop checkup}
  function scat {scoop config aria2-enabled true}
  function scaf {scoop config aria2-enabled false}
  function scf {code $home\.config\scoop\config.json}
  function srm {remove-item -r $env:scoop\cache\*; clear}
  function sbuc {set-location $env:scoop\buckets\scoopet}
2.Powershell常用命令
  Get-Module 查看已安装的模块
  Install-Module 安装模块与Get-Module是一对
  
