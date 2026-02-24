# 1Panel 自定义应用仓库（Custom App Store）

本仓库用于存放 **1Panel 自定义应用**（应用商店/应用模板），可通过 1Panel 后台添加为自定义仓库，实现一键安装与管理。

---

## 自同步计划任务 Shell 脚本

```bash
wget -P /opt/1panel/resource/apps/local https://github.com/wowhao333/1panel-appstore/archive/refs/heads/main.zip
unzip -o -d /opt/1panel/resource/apps/local/ /opt/1panel/resource/apps/local/main.zip
cp -rf /opt/1panel/resource/apps/local/1panel-appstore-main/apps/* /opt/1panel/resource/apps/local/
rm -r /opt/1panel/resource/apps/local/1panel-appstore-main
rm /opt/1panel/resource/apps/local/main.zip
```