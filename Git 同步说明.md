# 知识库 Git 同步说明

远程仓库：https://github.com/crimson-k/myobsidianvaults

## 日常使用

1. 打开 Obsidian 后，等待 Git 拉取完成再编辑。
2. 编辑结束，按 `Ctrl+P`，运行 **Git: Commit-and-sync**，等推送完成再换设备。
3. 手动获取其他设备更新：`Ctrl+P` → **Git: Pull**。

已配置启动时拉取，每 10 分钟自动提交同步、拉取。自动操作需要 Obsidian 正在运行且网络与 GitHub 登录有效。首次使用请在「设置 → 第三方插件」确认 **Git** 已启用；安装文件后重新启动 Obsidian。

## 新电脑首次获取

安装 Git 和 Obsidian。在 PowerShell 中执行（目标文件夹应不存在或为空）：

```powershell
git clone https://github.com/crimson-k/myobsidianvaults.git "D:\obsidian\vaults\Computer Vision & Pattern Recognition"
```

然后在 Obsidian 选择「打开文件夹作为仓库」，打开上述文件夹，并启用 Git 插件。

为这份仓库设置提交身份：

```powershell
git -C "D:\obsidian\vaults\Computer Vision & Pattern Recognition" config user.name "crimson-k"
git -C "D:\obsidian\vaults\Computer Vision & Pattern Recognition" config user.email "bellianfang@163.com"
```

首次推送需要通过 Git Credential Manager 登录有写入权限的 GitHub 账号。不要将密码或 token 写入笔记。

## 命令行同步

```powershell
Set-Location "D:\obsidian\vaults\Computer Vision & Pattern Recognition"
git status
git pull --rebase
# 编辑笔记后：
git add .
git commit -m "Update literature notes"
git push
```

拉取前先提交本地修改。有冲突时暂停编辑，在冲突文件中保留正确内容，再完成合并或 rebase；不要用强制推送覆盖另一台设备。

本仓库包含文献 Markdown、主题索引与 PPT 页面图片。Zotero PDF 和原始 PPT 仍在原来的外部位置；另一台电脑需另行同步 Zotero 库及附件，才能使用相应 Zotero 链接。

插件文档：https://publish.obsidian.md/git-doc/Start+here
