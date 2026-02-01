FerretDB for win7

由于 MongoDB 5.0+ 对 CPU 指令集（AVX）和系统内核的限制，老旧设备常年处于数据库断档状态。本项目通过适配 FerretDB v2.7.0，为 Windows 7 提供了一个轻量级、高性能的 MongoDB 协议实现。

✨ 核心亮点 (Key Features)
无需 CGO：基于 moderncsqlite 标签编译，纯 Go 实现，免除 DLL 缺失烦恼。

SQLite 驱动：支持将 MongoDB 数据直接存储在本地 .db 文件中。

低功耗：相比原版 MongoDB，内存占用极低，非常适合工控机和旧版笔记本。

现代协议：支持最新的 MongoDB 驱动连接。

🛠 启动说明 (Quick Start)
由于 v2.x 架构变动，请通过环境变量指定 SQLite 存储路径：

DOS
:: 1. 定义存储文件
set FERRETDB_POSTGRESQL_URL=file:win7_data.db

:: 2. 启动服务
ferretdb_sqlite.exe
✅ 验证与连接
默认地址：127.0.0.1:27017

管理工具：推荐使用 MongoDB Compass 或 Robo 3T 进行连接验证。
