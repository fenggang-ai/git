# Git

本仓库的初始占位说明文件。

## 说明

- 这是一个空的起始仓库，通过 Git 初始化并推送到 GitHub。
- 把项目文件放进本目录后，执行 `git add .` 与 `git commit` 即可纳入版本管理。

## 常用命令

```bash
git status            # 查看改动
git add -A            # 暂存全部改动
git commit -m "msg"   # 提交
git push              # 推送到 origin
```

## 仓库信息

| 项目 | 值 |
| --- | --- |
| 远程地址 | `git@github.com:fenggang-ai/git.git` |
| 默认分支 | `main` |
| 提交身份 | `fenggang-ai <fenggang-ai@users.noreply.github.com>` |
| 托管平台 | GitHub（公开仓库） |

## 本机环境说明

推送走 SSH，私钥位于 `~/.ssh/id_ed25519`，公钥已登记到 GitHub 账号。

`~/.ssh/config` 中把 `github.com` 映射到了 `ssh.github.com:443`，用于绕开被间歇性阻断的
443 直连；主机密钥已按 GitHub 公布的指纹校验。

系统 schannel 存在异常（`SEC_E_NO_CREDENTIALS`），若改走 HTTPS 方式访问 GitHub，需要显式
指定 OpenSSL 后端：

```bash
git -c http.sslBackend=openssl clone https://github.com/fenggang-ai/git.git
```

## 目录结构

```
.
├── .gitignore    # 忽略规则（OS / 编辑器 / 密钥 / 依赖 / 日志）
└── README.md     # 本文件
```
