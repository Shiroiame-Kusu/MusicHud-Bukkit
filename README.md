# MusicHud-Bukkit

MusicHud 的 Bukkit/Spigot/Paper 服务端插件实现。

### ***你需要先在客户端安装mod才能使用这个插件！！！***
- Mod 项目链接：**https://github.com/Etern-34520/MusicHud**
- Modrinth: **https://modrinth.com/mod/music-hud**

## 功能简介
- 与客户端 Mod 通过 Plugin Messaging 通讯并同步播放状态
- 支持点歌队列与投票切歌
- 支持空闲歌单播放
- 支持匿名/Cookie 登录

## 运行环境
- Java 21
- Spigot/Paper 1.21.*（`api-version: 1.21`）

## 安装
1. 将构建产物放入服务器 `plugins/` 目录
2. 启动服务器生成配置文件
3. 按需修改配置并重启或执行重载命令

## 配置
配置文件位置：`plugins/MusicHud-Bukkit/config.yml`

关键配置项：
- `api.base-url`：网易云音乐 API 地址（默认 `http://localhost:3000`）
- `api.timeout`：API 请求超时（毫秒）
- `playback.interval`：歌曲间隔（毫秒）
- `playback.enable-idle-playlist`：是否启用空闲歌单
- `vote-skip.enabled`：是否启用投票切歌
- `vote-skip.required-ratio`：投票切歌比例
- `vote-skip.min-votes`：最小票数
- `debug.enabled`：调试日志

## 指令
- `/musichud status`：查看当前播放状态
- `/musichud queue`：查看播放队列
- `/musichud skip`：强制跳过当前音乐（需要权限）
- `/musichud start`：启动音乐服务（需要权限）
- `/musichud stop`：停止音乐服务（需要权限）
- `/musichud reload`：重载配置（需要权限）
- `/musichud help`：显示帮助

## 权限
- `musichud.admin`：管理权限（默认 OP）
- `musichud.use`：基础使用权限
- `musichud.queue`：点歌队列权限
- `musichud.skip`：投票切歌权限
- `musichud.playlist`：空闲歌单管理权限

## 构建
- 使用 Gradle 构建：`./gradlew build`
- 产物位于：`build/libs/`

## 许可
GPL v3
