# scoop-backup-pwsh
* scoop backup PowerShell script

### 简介

* 因为scoop 至今没有一个很好的备份方法，所以把现有的方法分享出来，虽然也没有达到完美的效果

* 到目前为止，一共只有两个备份脚本
  * [KNOXDEV/scoop-backup](https://git.irs.sh/KNOXDEV/scoop-backup)
    * 此脚本在使用Ash258的scoop-core之后报错
    * 本脚本基于此脚本修改了错误内容
  * [Cologler](https://github.com/Cologler)/**[ScoopBackup-pwsh](https://github.com/Cologler/ScoopBackup-pwsh)**
    * 此脚本虽然能够正常运行，但是根据测试，目前只能备份bucket，不能备份app了
    * 这个脚本的好处是在任何地方都能运行，但是因为对powershell不熟悉，不大会做修改

### 使用

* 先安装错误的scoop-backup
  * `scoop bucket add knox-scoop https://git.irs.sh/KNOXDEV/knox-scoop`
  * `scoop install scoop-backup`
* 进入`apps/scoop-backup`文件夹中替换`scoop-backup.ps1`脚本
* 备份：`scoop-backup`
* 导入：在powershell中直接执行备份的脚本

