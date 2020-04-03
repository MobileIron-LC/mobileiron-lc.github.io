---
title: "MobileIron製品アーキテクチャ"
permalink: /mobileiron/architecture/
title_nodisplay: true
---
![MobileIron製品アーキテクチャ](/assets/mobileiron/images/2020Mar/14.jpeg)

前のページまでに説明した管理とセキュリティの機能を提供するために、MobileIronは大きく４つの製品コンポーネントで構成されます。

### MobileIron UEM
UEM: Unified Endpoint Management が全てののデスクトップとモバイル、およびアプリの管理の中心となり、IT管理者への単一のコンソールを提供します。VPNやクラウドサービスへの認証のためのID証明書を発行するCA機能も標準で備えており、またActive DirectoryやAzure ADとのダイナミック連携、コンプライアンス違反デバイスへの自動アクション、管理APIなど大規模な運用で求められる機能も充実しています。UEMはクラウドサービスの **MobileIron Cloud** とオンプレミスに設置できる **MobileIron Core** 製品から選んで導入できます。  
本サイトの「[クイックスタートガイド](/cloud-quickstart-guide/activation/)」参照して、MobileIron Cloudを今すぐはじめてみて下さい。

### MobileIron Sentry
インターネットから社内システムに接続するためのVPNゲートウェイとして、必要に応じて設置します。ユーザー自身でVPNのOn/Offをユーザー自身で行う必要が無く、仕事のアプリの通信が自動的に社内に接続されます。Sentryは専用OSで動作する仮想アプライアンスとして提供され、Vmware, Hyper-V, AWS, Azureなどにインストールできます。

### MobileIron Access
デバイスとアプリの管理状況に基づいてクラウドサービスへのログインを許可する条件付きアクセスと、パスワードを使わないゼロ・サインオンを提供します。

### MobileIron Threat Defense
デバイス内やネットワーク環境を監視し、その振る舞いからデバイス、ネットワーク、アプリへの攻撃を見つけ出します。攻撃の種類や重大さに応じて管理者が定義したアクションを即座に実行することで侵害行為を食い止めるほか、フィッシングサイトのブロック機能も備えています。様々な公開・非公開アプリに関するリスク評価情報データベースの提供も行っています。
