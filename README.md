# mall 电商系统

> 基于 Spring Boot + MyBatis + Spring Security + Redis + RabbitMQ + Elasticsearch 构建的前后台分离电商项目，适合作为 Java 后端项目实战与简历作品展示。

## 项目亮点

- 前后台分离电商系统，覆盖后台管理、前台商城、商品搜索三大核心场景
- 基于 Spring Security + JWT 实现管理员与会员认证鉴权
- 基于 Redis 实现缓存、验证码存储与订单号生成
- 基于 RabbitMQ 实现订单超时取消与库存释放
- 基于 Elasticsearch 实现商品搜索、排序与聚合筛选
- 基于 MongoDB 实现收藏、浏览记录、品牌关注等会员行为数据存储
- 支持 Docker 容器化部署，具备较完整的工程化结构

## 技术栈

**后端：** Spring Boot 2.7、Spring Security、JWT、MyBatis、MyBatis Generator、PageHelper、Swagger

**中间件：** MySQL、Redis、RabbitMQ、MongoDB、Elasticsearch、Logstash、Kibana

**部署运维：** Docker、Nginx、Jenkins、Maven

**对象存储：** OSS、MinIO

## 项目结构

```text
mall
├── mall-common    # 通用工具与公共能力
├── mall-mbg       # MyBatis Generator 生成代码
├── mall-security  # Spring Security 与 JWT 封装
├── mall-admin     # 后台管理系统接口
├── mall-portal    # 前台商城系统接口
├── mall-search    # 商品搜索系统
└── mall-demo      # 测试与示例代码
```

## 核心功能

### 后台管理系统 mall-admin
- 商品管理：品牌、分类、属性、SKU、商品上下架
- 订单管理：订单查询、发货、退货申请、订单设置
- 营销管理：优惠券、秒杀活动、首页推荐、广告配置
- 权限管理：管理员、角色、菜单、资源访问控制
- 文件上传：支持 OSS / MinIO 对象存储

### 前台商城系统 mall-portal
- 会员体系：注册登录、验证码、地址管理、会员中心
- 商品能力：首页推荐、商品详情、品牌与分类浏览
- 交易链路：购物车、订单确认、优惠券、积分抵扣、支付回调
- 订单能力：超时取消、确认收货、退货申请
- 用户行为：商品收藏、品牌关注、浏览历史

### 搜索系统 mall-search
- 商品导入 Elasticsearch
- 关键字搜索、品牌/分类过滤
- 按相关度、销量、价格排序
- 聚合返回品牌、分类、属性筛选信息

## 快速开始

### 环境要求
- JDK 8
- Maven 3.6+
- MySQL 5.7+
- Redis 7+
- RabbitMQ 3.10+
- MongoDB 5+
- Elasticsearch 7.17+

### 配置说明
仓库中的配置文件已替换为**示例占位符**，使用前请根据本地环境修改以下文件：

- `mall-admin/src/main/resources/application-dev.yml`
- `mall-portal/src/main/resources/application-dev.yml`
- `mall-search/src/main/resources/application-dev.yml`
- `mall-mbg/src/main/resources/generator.properties`

请重点替换：
- 数据库地址、用户名、密码
- Redis / RabbitMQ / MongoDB / Elasticsearch 连接信息
- MinIO / OSS / 支付宝等第三方配置

### 启动顺序建议
1. 启动 MySQL、Redis、RabbitMQ、MongoDB、Elasticsearch
2. 导入数据库脚本：`document/sql/mall.sql`
3. 按需启动服务：
   - `mall-admin`
   - `mall-portal`
   - `mall-search`

## 简历项目描述示例

**项目名称：** mall 电商系统
**技术栈：** Spring Boot、Spring Security、JWT、MyBatis、Redis、RabbitMQ、MongoDB、Elasticsearch、Docker
**简介：** 基于 Spring Boot 搭建的前后台分离电商系统，覆盖商品管理、订单管理、会员体系、购物车、优惠券、积分、商品搜索等核心业务，具备缓存、异步消息、搜索引擎和容器化部署能力。

## 说明

- 本仓库主要用于项目学习、后端能力展示与简历项目沉淀
- 当前提交中的配置均为示例占位符，不包含真实生产密钥
- 前端项目可根据需要自行对接后台接口

## License

[Apache License 2.0](./LICENSE)
