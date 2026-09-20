# 广州鑫宇科创企业官网

Laravel 12（PHP 8.2、MySQL 5.7）全栈官网：Blade/Tailwind 前台、Filament 管理后台、MySQL 数据模型与 `/api/v1` REST API。

## 本地启动

1. 复制 `.env.example` 为 `.env`，生成新的 `APP_KEY`，并仅在本地填写 `DB_PASSWORD` 与 `MYSQL_ROOT_PASSWORD`。
2. 执行 `docker compose up -d mysql`。
3. 执行 `docker compose run --rm app php artisan migrate --seed`。
4. 执行 `npm install && npm run build`，再执行 `docker compose up app`。
5. 前台为 `http://localhost:8000`，后台入口为 `/admin`，API 为 `/api/v1`。

后台首个管理员账号由部署人员通过 Laravel 安全流程创建；仓库不提供默认账号或密码。

## 验证命令

```sh
docker compose run --rm app vendor/bin/pint
docker compose run --rm app php artisan test --compact
docker compose run --rm app vendor/bin/phpstan analyse
npm run build
```

## 内容原则

案例种子均标注为“行业解决方案示例”。上线前，运营人员须在后台确认每一项案例、联系方式、品牌资料和对外承诺。

## 上线交接

生产部署、环境变量、迁移、队列、Nginx/PHP-FPM、存储、第三方适配器、备份与回滚要求见 [程序员上线交接包](docs/deployment-handoff.md)。上线前还应处理 [发布前审查](docs/release-readiness-audit.md) 的 P0/P1 项。
