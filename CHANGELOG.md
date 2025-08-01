# 更新日志

## v1.1.0 (2024-01)

### 新增功能
- 🚀 **并发同步模式** - 支持多线程同步，性能提升3-5倍
  - 新增 `--mode=concurrent` 参数
  - 可通过 `--workers` 参数自定义线程数
- 🔐 **环境变量配置** - 支持通过环境变量管理敏感信息
  - 所有配置项均可通过环境变量覆盖
  - 提供 `.env.example` 模板文件
- 🛡️ **敏感信息保护** - 自动过滤日志中的密码和令牌
  - 新增 `log_utils.py` 安全日志模块
  - 自动识别并掩码敏感信息
- 🔒 **SSL证书控制** - 可配置SSL证书验证
  - 新增 `verify_ssl` 配置项
  - 默认启用SSL验证，提升安全性
- ⚡ **批量图片处理** - 并发处理多张图片
  - 新增 `process_images_batch` 方法
  - 大幅提升图片处理效率

### 代码优化
- 重构 `_remove_title_duplication` 方法，提高可读性
- 添加基础接口定义 `interfaces.py`
- 改进异常处理和错误提示
- 优化并发控制和线程安全

### 安全增强
- 移除全局SSL验证禁用
- 支持配置级别的SSL控制
- 日志自动脱敏处理
- 环境变量优先级高于配置文件

### 配置变更
- WordPress配置新增 `verify_ssl` 字段（可选，默认true）
- 支持所有配置项的环境变量覆盖

## v1.0.0 (2024-01)

### 初始版本
- 核心同步功能
- 支持全量和增量同步
- 七牛云图片上传
- 智能内容类型映射
- 状态管理和断点续传
- 配置验证工具
- 一键启动脚本