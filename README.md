# scoop-backup
* scoop backup **PowerShell** script

# 注意
* [KNOXDEV/scoop-backup](https://git.irs.sh/KNOXDEV/scoop-backup)问题最近基本修复完毕，即使是使用Ash258的scoop-core也可以备份

### 简介

* 因为scoop 至今没有一个很好的备份方法，所以把现有的方法分享出来

* 到目前为止，一共只有两个备份脚本
  * [KNOXDEV/scoop-backup](https://git.irs.sh/KNOXDEV/scoop-backup)
    * 此脚本在使用Ash258的scoop-core之后报错
      * 但是即使是原生的scoop内核，也会一直有警告
    * 本脚本基于此脚本修改了错误内容
  * [Cologler](https://github.com/Cologler)/**[ScoopBackup-pwsh](https://github.com/Cologler/ScoopBackup-pwsh)**
    * 此脚本虽然能够正常运行，但是根据测试，目前只能备份bucket，不能备份app了
    * 这个脚本的好处是在任何地方都能运行，但是因为对powershell不熟悉，不大会做修改

### 使用

* 安装我的bucket：`scoop bucket add diklios https://github.com/diklios5768/diklios-scoop-bucket`
* 安装备份脚本：`scoop install diklios/scoop-backup`
* 备份：`scoop-backup`
  * 备份完会提示备份文件位置
* 重新安装：直接执行PowerShell脚本即可

### 注意
* 如果安装了main bucket中的 scoop-search，请注意千万别加hooks，因为[#13](https://github.com/shilangyu/scoop-search/issues/13)，所以不仅命令行中的help会报错，这个备份脚本也会出错
  * 建议用别名，或者直接手输`scoop-search`，这问题暂时不好解决
