# Mizuho Yukinoshita

[English](#english) · [日本語](#日本語)

![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat&logo=php&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?style=flat&logo=go&logoColor=white)
![MySQL](https://img.shields.io/badge/Aurora_MySQL-4479A1?style=flat&logo=mysql&logoColor=white)
![Memcached](https://img.shields.io/badge/Memcached-555555?style=flat)
![Valkey](https://img.shields.io/badge/Redis%20%2F%20Valkey-DC382D?style=flat&logo=redis&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonwebservices&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat&logo=terraform&logoColor=white)
![Packer](https://img.shields.io/badge/Packer-02A8EF?style=flat&logo=packer&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat&logo=jenkins&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat&logo=flutter&logoColor=white)
![Vue.js](https://img.shields.io/badge/Vue.js-4FC08D?style=flat&logo=vuedotjs&logoColor=white)

## English

Backend & Platform Engineer in Tokyo · AWS Certified DevOps Engineer – Professional

I've spent 4.5 years on the server side of a mobile game that has been running for 10 years: game APIs on sharded Aurora MySQL, performance tuning, and turning hand-run deployments and infrastructure into code. I lead a 5-person server team while still writing code every day, and I'm currently also building a live-streaming platform on AWS Lambda and Amazon IVS.

### What I've worked on

- **Database performance** — Tuned queries, indexes, caching, and transactions on sharded Aurora MySQL (a single query peaks at 5,500/s), driven by Performance Insights and slow logs. Cut overall API p95 during events by about 40% (~550 → ~330 ms) while roughly halving the web server fleet at peak, and halved p50 and p95 of a home screen API serving 300K requests a day.
- **Deployment as code** — Moved 60 Jenkins jobs to Pipeline as Code, merged a five-job, manually gated production deploy into a single pipeline, and cut staging deploys from ~25 to ~7.5 minutes.
- **Infrastructure** — Built web server infrastructure with Terraform and Packer (AMI / ALB) and migrated production ElastiCache from Redis to Valkey.
- **Quality at scale** — Introduced integration testing against a real database, automated code style enforcement, and Claude Code skills that keep AI-written code consistent with team conventions.
- **Mobile release automation** — Automated app releases with GitHub Actions and a self-hosted runner (push a tag, ship a release) and reduced secrets handed to developers from 11 to 2.

### Public work

- [**Patching a PHP security release in 40 minutes on an LB → ASG → EC2 stack**](https://dev.to/mizuho-yukinoshita/patching-a-php-security-release-in-40-minutes-on-an-lb-asg-ec2-stack-f11) — Backported upstream fixes onto Ubuntu's package and rolled them out to production the same night ([Japanese](https://qiita.com/mizuho-yukinoshita/items/70158680be6672dd357a)).
- [**infra**](https://github.com/mizuho-yukinoshita/infra) — Terraform templates with keyless auth (AWS / GCP OIDC and Workload Identity), a plan → approve → apply Jenkins pipeline, and CI with tflint and trivy.
- **OSS** — [Abedalkareem/games_services#177](https://github.com/Abedalkareem/games_services/pull/177): added an optional `forceRefreshToken` to Android `requestServerSideAccess` (merged).

### Certifications

- [AWS Certified DevOps Engineer – Professional](https://www.credly.com/badges/194317be-785f-4ce3-8f3b-6c8e33e84294) (2026)
- LPIC-1 (2024)

---

## 日本語

東京のバックエンド／基盤エンジニア · AWS Certified DevOps Engineer – Professional

運営10年目のモバイルゲームで、サーバーサイドを4年半担当しています。シャーディングされたAurora MySQL上のゲームAPI開発と性能改善、手作業だったデプロイやインフラのコード化に取り組んできました。5名のサーバーチームのリーダーを務めながら、自分も毎日コードを書いています。現在はAWS LambdaとAmazon IVSを使ったライブ配信プラットフォームの開発も並行して担当しています。

### 取り組んできたこと

- **DBの性能改善**：Performance Insightsとslow logを起点に、シャーディングされたAurora MySQL（単一クエリでピーク毎秒5,500回）のクエリ・インデックス・キャッシュ・トランザクションを見直し、イベント期間中のAPI全体のp95を約40%短縮（約550ms→約330ms）し、Webサーバー台数もほぼ半減。1日30万リクエストのマイページAPIはp50・p95を半減
- **デプロイのコード化**：Jenkinsの60ジョブをPipeline as Codeへ移行。5つのジョブと人手の承認ゲートの連鎖だった本番デプロイを1本のパイプラインに統合し、ステージングデプロイを約25分から約7.5分に短縮
- **インフラ**：Terraform・PackerでWebサーバー基盤（AMI・ALB）を構築し、本番のElastiCacheをRedisからValkeyへ移行
- **品質の仕組み化**：実DBを使う統合テスト、コード規約の自動適用、AIが書くコードもチームの規約に沿わせるClaude Codeのskillを導入
- **アプリ配布の自動化**：GitHub Actionsとself-hosted runnerで、タグを打つだけでリリースできるようにし、開発者に配る機密を11件から2件に削減

### 公開しているもの

- [**LB → ASG → EC2 構成でも PHP の脆弱性対応を 40 分で終わらせる**](https://qiita.com/mizuho-yukinoshita/items/70158680be6672dd357a)：upstreamの修正をUbuntuのパッケージに移植し、公開当日の夜のうちに本番へ適用した記録（[英語版](https://dev.to/mizuho-yukinoshita/patching-a-php-security-release-in-40-minutes-on-an-lb-asg-ec2-stack-f11)）
- [**infra**](https://github.com/mizuho-yukinoshita/infra)：Terraformテンプレート集。AWS / GCPのOIDC・Workload Identityによる鍵なし認証、plan→承認→applyのJenkinsパイプライン、tflint・trivyによるCI
- **OSS**：[Abedalkareem/games_services#177](https://github.com/Abedalkareem/games_services/pull/177)。Androidの `requestServerSideAccess` に `forceRefreshToken` のオプションを追加（マージ済み）

### 資格

- [AWS Certified DevOps Engineer – Professional](https://www.credly.com/badges/194317be-785f-4ce3-8f3b-6c8e33e84294)（2026年）
- LPIC-1（2024年）
