# 广州鑫宇科创官网开发约定

- 使用现有 Laravel 12、PHP 8.2、MySQL 5.7、Blade、Livewire、Alpine.js、Tailwind CSS、Filament 与 Eloquent 约定；不擅自升级依赖。
- 控制器保持薄：验证用 Form Request，权限用 Policy/Gate，API 用 JsonResource，业务规则放 Service 或 Model 查询作用域。
- 数据库改动必须含 migration、Model、Factory、Seeder、测试；不得修改已执行 migration。
- 所有写操作须服务端验证与权限检查；上传校验类型、大小、存储目录、访问权限；富文本输出必须防 XSS。
- 未确认 AI 案例仅称“行业解决方案示例”。不得写死未确认电话、地址、年份、人数或效果。
- 不提交 `.env`、密码、密钥、备份、`vendor`、`node_modules` 或缓存；不执行 push、强推、生产迁移或部署。
- PHP 命令通过 Docker 开发环境执行；修改后运行相关测试、Pint、Larastan 与前端构建。
