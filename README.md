# toyProject_strapi
> 熟習 strapi

## 目標

主體參考 [🍝 Cooking a Deliveroo clone with Next.js (React), GraphQL, Strapi and Stripe - 🏗️ Setup](https://strapi.io/blog/strapi-next-setup) 

搭建 human zoo 購買系統 :)

- [x] PM2 (進程管理工具)
- [x] Strapi (後端)
- [x] PM2 部署並監控 Strapi
- [ ] PostgreSQL (數據庫)
- [ ] Strapi & PostgreSQL 連接
  1. 更換 Strapi 原始數據庫 (SQLite -> PostgreSQL)
- [ ] 學習 Tudis  serverCode (理清其中邏輯)
- [ ] Next.js (前端)
- [ ] Docker 微服務化

## 流程

- [x] ***PM2***

  #### 策略: 

  1. 搭建簡單 Express 網站，並監控

  #### 結果:

  1. 使用 PM2 的 ecosystem.json 或者 ecosystem.ymal 來對應不同環境(生產，開發，測試等) 來切換部署

  2. 監控

     ```shell
     $ pm2 monit # 優雅地監控不同應用
     ```

  3. 開機自啓動

  #### Upcoming:

  1. 重啓觸發機制
  2.  PM2編程接口

  #### Reference:

  1. [pm2 使用教程](https://www.jianshu.com/p/5f808762a71a)
  2. [PM2实用入门指南](https://www.cnblogs.com/chyingp/p/pm2-documentation.html) (大佬教程)
  3. [PM2 SINGLE PAGE DOC](https://pm2.keymetrics.io/docs/usage/pm2-doc-single-page/)
  4. [PM2 Cheatsheet](https://devhints.io/pm2) (救命手冊)
  5. [Create New Express.js Apps in Minutes with Express Generator](https://www.sitepoint.com/create-new-express-js-apps-with-express-generator/)

- [x] ***Strapi*** 

  #### 策略:

  1. 在 local 搭建 Strapi
  2. 導入數據，並設定訪問 API 規程與權限
  3. 用 Postman 測試

  #### 結果:

  1. 手動頁面輸入數據
  2. 連接表數據之間的關系

  #### Upcoming:

  1. 優化導入數據方式（非手動頁面導入)

  #### Reference:

  1. [Tutorial](https://strapi.io/documentation/3.0.0-beta.x/getting-started/quick-start-tutorial.html#_1-install-strapi-and-create-a-project)
  2. [Strapi.js Crash Course | Headless CMS](https://www.youtube.com/watch?v=6FnwAbd2SDY)
  3. [strapi入门第一篇](https://blog.csdn.net/qq_41535611/article/details/107902915)
  4. [strapi入门——第二篇](https://blog.csdn.net/qq_41535611/article/details/107912549)
  5. [Strapi 学习](https://github.com/AutumnFish/strapi_study)

- [x] ***PM2 部署並監控 Strapi***

  #### 策略: 

  1. 直接部署和監控 Strapi

  #### 結果:

  1. 使用 PM2 的 ecosystem.config.js 配置文件

     ```shell
     $ pm2 start ecosystem.config.js
     ```

  #### Upcoming:

  1. 修改 ecosystem.config.js 文件，更高級監控 Strapi
  2. \+ PM2 Upcoming

  #### Reference:

  1. N/A

- [ ] ***PostgreSQL***

  策略:

  1. 使用 Docker 部署 PostgreSQL
  2. 使用 pgAdmin 可視化並 CRUD 其中數據

---------------------------

## Undone:

- [ ] Srapi 連接 PostgreSQL

  [How to Install & Configure Strapi with PostgreSQL](https://tute.io/install-configure-strapi-postgresql)

  [How To Install PostgreSQL on Ubuntu 20.04 [Quickstart]](https://www.digitalocean.com/community/tutorials/how-to-install-postgresql-on-ubuntu-20-04-quickstart)

  PostgreSQL: [PostgreSQL Tutorial](https://www.postgresqltutorial.com/)

  **Upcoming**: 數據庫可視化: [pgAdmin](https://www.pgadmin.org/)

- [ ] Next.js 前端搭建

- [ ] 前後端關聯

## References

1. [Tutorial](https://strapi.io/documentation/3.0.0-beta.x/getting-started/quick-start-tutorial.html#_1-install-strapi-and-create-a-project)
2. [🍝 Cooking a Deliveroo clone with Next.js (React), GraphQL, Strapi and Stripe - 🏗️ Setup](https://strapi.io/blog/strapi-next-setup) 
3. [How to Install & Configure Strapi with PostgreSQL](https://tute.io/install-configure-strapi-postgresql)
4. [How To Install PostgreSQL on Ubuntu 20.04 [Quickstart]](https://www.digitalocean.com/community/tutorials/how-to-install-postgresql-on-ubuntu-20-04-quickstart)
5. [PostgreSQL Tutorial](https://www.postgresqltutorial.com/)
6. [pgAdmin](https://www.pgadmin.org/)

