# toyProject_strapi
> 熟習 strapi

## 目標

主體參考 [🍝 Cooking a Deliveroo clone with Next.js (React), GraphQL, Strapi and Stripe - 🏗️ Setup](https://strapi.io/blog/strapi-next-setup) 

搭建 human zoo 購買系統 :)

> 注意: 因爲數據庫已從 SQLite 更換到 PostgreSQL (Docker version)，所以會有較大改動...

- [x] PM2 (進程管理工具)
- [x] Strapi
  1. Postman 與 Strapi 溝通
- [x] PM2 部署並監控 Strapi
- [x] PostgreSQL (docker)
- [x] Strapi & PostgreSQL (docker) 連接
  1. 更換 Strapi 原始數據庫 (SQLite -> PostgreSQL)
  2. CRUD container 內數據
- [ ] 學習 Tudis  serverCode (理清其中邏輯)
- [ ] Next.js (前端)
- [ ] 前後端數據連接
- [ ] Docker 微服務化全流程

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

  #### Repository:

  1. [pm2](https://github.com/Mini-Pingu/pm2)

- [x] ***Strapi*** 

  1. Postman 與 Strapi 溝通

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

  #### Repository:

  1. [toyProject_strapi](https://github.com/Mini-Pingu/toyProject_strapi)

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

- [x] ***PostgreSQL***

  #### 策略:

  1. 使用 Docker 部署 PostgreSQL
  2. 使用 pgAdmin 可視化並 CRUD 其中數據
  
  #### 結果:
  
  - [x] 部署 Pgdb docker
  - [x] pgAdmin 監視 Pgdb
  - [x] Update data
  
  #### Upcoming:
  
  1. ​	精準操控 db
  
  #### Reference:
  
  1. [PostgreSQL Tutorial](https://www.postgresqltutorial.com/)

- [x] ***Strapi & PostgreSQL***

  #### 策略:

  1. strapi 可以連接 db 並正常顯示  data
     1.  pgdb version 要 10
  2. 通過 strapi 修改  db 數據

  #### 結果:

  1. 

  #### Upcoming:

  1. 每日備份數據庫 (docker volume 方法)

  #### Reference:

  1. [How to Install & Configure Strapi with PostgreSQL](https://tute.io/install-configure-strapi-postgresql)
  2. [How To Install PostgreSQL on Ubuntu 20.04 [Quickstart]](https://www.digitalocean.com/community/tutorials/how-to-install-postgresql-on-ubuntu-20-04-quickstart)
  3. [How to Install & Configure Strapi with PostgreSQL](https://tute.io/install-configure-strapi-postgresql)
  4. [Strapi – Setup with Docker Postgres](https://danielcorcoranssql.wordpress.com/2020/04/23/strapi-setup-with-docker-postgres/)

- [ ] ***Tudis  serverCode***

  #### 策略:

  1. 理解後臺代碼整體
     1. 使用到多少個個體
     2. 各個體作用 
     3. 如何操控各個體( CRUD )
  2. 復現 strapi 和 postgresql

  #### 結果:

  #### Upcoming:

  #### Reference:

- [ ] ***Next.js ...***

- [ ] ***前後端數據連接***

- [ ] ***Docker 微服務化全流程***

## References

1. [Tutorial](https://strapi.io/documentation/3.0.0-beta.x/getting-started/quick-start-tutorial.html#_1-install-strapi-and-create-a-project)
2. [🍝 Cooking a Deliveroo clone with Next.js (React), GraphQL, Strapi and Stripe - 🏗️ Setup](https://strapi.io/blog/strapi-next-setup) 
3. [How to Install & Configure Strapi with PostgreSQL](https://tute.io/install-configure-strapi-postgresql)
4. [How To Install PostgreSQL on Ubuntu 20.04 [Quickstart]](https://www.digitalocean.com/community/tutorials/how-to-install-postgresql-on-ubuntu-20-04-quickstart)
5. [PostgreSQL Tutorial](https://www.postgresqltutorial.com/)
6. [pgAdmin](https://www.pgadmin.org/)

