---
title: "Android Enterpriseの管理モード"
permalink: /cloud-quickstart-guide/ae-intro/
---
Android Enterpriseには次の３つの管理モードがあり、ユースケースにより適したモードを選択して利用します。
- Work Profile
- Fully Managed
- Fully Managed + Work Profile

![](/assets/cloud-quickstart-guide/images/9a8d239d-1e0e-4035-b258-f8e0277afab0.png)

### Work Profile

もともと個人のGoogleアカウントを設定して利用しているAndroidデバイスを、MobileIron Cloudに登録することにより、企業の領域であるWork Profileが構成されます。以下のスクリーンショットはWork Profileが構成されたデバイスの例です。Playストアが個人用と仕事用の領域それぞれに表示されています。仕事用のPlayストアからはIT管理者が指定したパブリックアプリまたはインハウス開発アプリのみがインストール可能で、デバイス上で仕事のアプリはカバンのマークのバッジ付きで表示されます。※Androidバージョンや機種によってアイコンのレイアウトのされ方は異なります。この例では個人用アプリと仕事用アプリがタブで分けられた表示になっていますが、機種によっては仕事用アプリがフォルダに集められたり、あるいは特に分けられることなくホームスクリーンに追加されたりします。

![](/assets/cloud-quickstart-guide/images/09185833-1f2f-48a8-8c68-b49baa9f78b6.png)

![](/assets/cloud-quickstart-guide/images/2cee8080-ddb7-4223-828d-976bc9548dfc.png)

MobileIron Cloudから管理できるのは、仕事の領域とその中にインストールしたアプリのみです。企業はデバイス全体をワイプしたり、ハードウェア機能をロックダウン（無効化）したり、個人の領域にインストールされたアプリの一覧を取得したりすることはできません。

### Fully Managed

デバイス全体を企業で管理し、企業で指定したアプリのみが利用できるのがFully Managedです。ユーザーが自由にアプリをインストールして利用できる個人領域はありません。

工場出荷状態に初期化したデバイスの電源を入れると「ようこそ」画面となりますが、ここで特別なセットアップ方法をとることでFully Managed モードでセットアップできます。具体的には以下のいずれかの方法によります。
- **afw#トークン：** ようこそ画面から数ステップ先に進んだGoogleアカウントの入力画面で、Googleアカウントの代わりに"afw#mobileiron.com"と入力します。
- **QRコード：** ようこそ画面の余白を６回タップするとQRコードリーダーが起動します。別のAndroidデバイスに、Google Playで配布されている「MobileIron Provisioner」アプリをインストールし、これで表示させたQRコード撮影します。
- **NFC：** 別のAndroidデバイスにインストールした「MobileIron Provisioner」アプリでNFCによるセットアップを有効にし、これからセトアップする「ようこそ」画面の端末とNFCアンテナ同士を近づけます。
- **ゼロタッチ：** Googleのゼロタッチ対応認定リセラーを通じて企業で購入したデバイスでは、「ようこそ」画面から通常操作でセットアップを進めても自動的にFully Managedモードを構成できます。

こちらの[ビデオ](/videos/ae-registration/)ご覧くとわかりやすいです。

### Fully Managed + Work Profile

Fully Managedモードと同様にデバイス全体を企業で管理するものの、ユーザーが自由にアプリをインストールして利用できる個人領域も用意されているのがFully Managed + Work Profileモードです。

デバイスのセットアップ方法はFully Managedと同じで「ようこそ」画面から特別なセットアップ方法のいずれかを行います。

## デバイス登録時の管理モード選択のしくみ

３つの管理モードのうち、どのモードで管理されるかは、MobileIron Cloudへのデバイス登録時に決まります。通常の初期セットアップを行ったデバイスにMobileIron Goをインストールしてデバイス登録した場合には、Work Profileにしかなりません。
企業がデバイス全体の管理権限を持つ、Fully Managed または Fully Managed + Work Profile にするためには「ようこそ」画面から特別なセットアップが必要です。またこのとき Fully Managed と Fully Managed + Work Profile のどちらになるかは、MobileIron Cloud側の設定によって決定します。詳しくは後のデバイス登録のページで説明します。

![](/assets/cloud-quickstart-guide/images/A514A635-4BD9-48C1-A773-117A064F2701.png)
