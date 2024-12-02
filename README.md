## 项目简介

这是一个多商户 Stripe 支付数据分析看板项目，旨在帮助企业或开发者统一管理和分析多个 Stripe 账户的支付数据。项目提供直观的数据可视化界面，方便监控业务情况和收入趋势。

### 功能特性

- 多个 Stripe 账户数据的统一管理和展示
- 支持按日期查看交易数据
- 展示订单数量、收入等关键指标
- 区分一次性支付和订阅支付
- 支持明暗主题切换
- 数据可视化展示（图表等）

### 技术栈

- Next.js 14
- TypeScript
- Tailwind CSS
- Recharts (图表库)
- Stripe API
- shadcn/ui (UI组件库)

### 环境变量配置

在项目根目录创建 `.env` 文件，配置以下环境变量：

```bash
# 访问密码，用于保护数据访问
STRIPE_VIEWER_PASSWORD=your_password_here

# Stripe API Keys (可配置多个商户)
STRIPE_SECRET_KEY_1=sk_live_xxxxx
STRIPE_SECRET_KEY_2=sk_live_xxxxx
STRIPE_SECRET_KEY_3=sk_live_xxxxx
# ... 可以继续添加更多商户的 Stripe Secret Key
```

### 部署方式

项目支持多种部署方式：

1. **本地开发：**

   ```bash
   npm install
   npm run dev
   ```

2. **Docker 部署：**
   项目包含了 Dockerfile 和 docker-compose.yml，可以直接使用 Docker 部署，已配置好 Traefik 反向代理和 HTTPS 证书自动申请。