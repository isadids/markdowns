## 安装阶段

### 绕过联网登录

在 OOBE 阶段，按 <kbd>Shift + F10</kbd>打开 **CMD**，输入 `start ms-cxh:localonly`。

## 安装后

### 更改脚本执行策略

```pwsh
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```

### 启用 UTF-8

按 <kbd>Win + R</kbd> 输入 `intl.cpl`，依次选择【管理】→【更改系统区域设置】，勾选【Beta 版：使用 Unicode UTF-8 提供全球语言支持(U)】，然后重启。

