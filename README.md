# scoop-backup

- scoop backup **PowerShell** script

## 简介

- 因为 scoop 至今没有一个很好的备份方法，所以把现有的方法分享出来

- 到目前为止，一共只有两个备份脚本
  - [KNOXDEV/scoop-backup](https://git.irs.sh/KNOXDEV/scoop-backup)
    - 此脚本在使用 Ash258 的 scoop-core 之后报错
      - 但是即使是原生的 scoop 内核，也会一直有黄色的警告
    - 本脚本基于此脚本修改了错误内容
      - 2022.1.5 此脚本基本修复完毕，可以正常使用
  - [Cologler](https://github.com/Cologler)/**[ScoopBackup-pwsh](https://github.com/Cologler/ScoopBackup-pwsh)**
    - 此脚本虽然能够正常运行，但是根据测试，目前只能备份 bucket，不能备份 app 了
    - 这个脚本的好处是在任何地方都能运行，但是因为对 powershell 不熟悉，不大会做修改

### 使用

- 安装我的 bucket：`scoop bucket add diklios https://github.com/diklios5768/diklios-scoop-bucket`
- 安装备份脚本：`scoop install diklios/scoop-backup`
- 备份：`scoop-backup`
  - 备份完会提示备份文件位置
- 重新安装：直接执行 PowerShell 脚本即可

### 注意

- 如果安装了 main bucket 中的 scoop-search，请注意千万别加 hooks，因为[#13](https://github.com/shilangyu/scoop-search/issues/13)，所以不仅命令行中的 help 会报错，这个备份脚本也会出错
  - 建议用别名，或者直接手输`scoop-search`，这问题暂时不好解决
- [KNOXDEV/scoop-backup](https://git.irs.sh/KNOXDEV/scoop-backup)问题基本修复完毕，即使是使用 Ash258 的 scoop-core 也可以备份，可以使用他的脚本，也可以继续使用我修改的，不过因为功能基本已经齐全，我的后续可能不再维护了，而他的可能会增加更多的特性，推荐使用
  - 但是由于一些原因，使用他库的安装脚本好像由于网络问题基本无法安装成功，所以推荐使用我的备份脚本，已经测试如果能够登录github基本是能够成功安装使用的
  - 安装我的 bucket：`scoop bucket add diklios https://github.com/diklios5768/diklios-scoop-bucket`
  - 安装备份脚本：`scoop install diklios/scoop-backup-knox`
  - 使用：`scoop-backup-knox`
  - 可以同时安装两个脚本
    - 由于未改动原代码，所以出现scoop-backup请自行认为是scoop-backup-knox
