---
title: "テナントのアクティベーション"
permalink: /cloud-quickstart-guide/
---

## 新規MobileIron Cloudテナント発行の通知

お客様のMobileIron Cloudテナントが利用可能になると、次のようなアクティベーションを求めるメールが届きます。アクティベーションはできるだけ早く行なって下さい。１週間以上放置するとテナントが無効化され、アクティベーションできなくなる場合があります。  
![](/assets/cloud-quickstart-guide/images/224ADB9A-27CE-4FD1-81DC-C128654B8A34.png)

## サポートされるWebブラウザと言語

MobileIron Cloud管理コンソールは次のいずれかのWebブラウザでご利用下さい。

- Firefox (Windows/Mac)
- Chrome (Windows/Mac)
- Safari (Mac)

また管理コンソールは多言語対応となっており、ブラウザの言語設定に合わせた言語で表示されます。日本語、英語などに対応しています。

## アクティベーション

Webブラウザで「Activate Now」のリンクを開きます。テナント管理者のユーザー名は申込時のEメールアドレスのローカル部に"-emmadmin"を付加したものになっています。はじめにパスワードを再設定してください。  
![](/assets/cloud-quickstart-guide/images/8109B867-A19A-4EFF-AC5A-7E0DEA95CD71.png)

ログインし直すと、初期設定ウィザードが始まります。  
![](/assets/cloud-quickstart-guide/images/3BB23D22-C85B-49B6-BC8F-07F1CA31F7A0.png)

## 初期設定ウィザード

利用者情報を入力し、利用規約に同意します。  
![](/assets/cloud-quickstart-guide/images/1385478E-DCFB-49F7-BA79-494E387EF53F.png)

### Apple MDM

iOS / iPadOS /macOS デバイスの管理は、Appleが定めるApple MDMのしくみに従って行います。Apple MDMでは、MDMサーバ（MobileIron Cloud）からデバイスを呼び出すためにAPNS（Apple Push Notification Service）を利用しますが、このときMDMサーバからAPNSへの接続に必要な証明書の発行をAppleから受ける必要があります。

初期設定ウィザードからMDM証明書のインストールを行うことができます。本書では後で設定しますので、続行をクリックして次の画面に進みます。  
![](/assets/cloud-quickstart-guide/images/7F0D17CA-C9CC-47C8-8A8C-5099BA23871E.png)

MDM証明書は後でインストールしますので、このステップをスキップします。  
![](/assets/cloud-quickstart-guide/images/3EB247FE-547C-4254-92DC-C4A8AA2FF257.png)

![](/assets/cloud-quickstart-guide/images/DBCB0D45-88B5-416B-84B3-7D3826C27EC3.png)

### Android Enterprise

Androidデバイスは、Googleが定めるAndroid Enterpriseのしくみに従って管理します。Android Enterpriseを利用するために、組織のGoogle Play（Managed Google Play）アカウントを作成し、MobileIron Cloudと接続する必要があります。

初期設定ウィザードから組織のGoogle Playアカウントとの接続を行うことができます。本書では後で設定します。このステップをスキップします。  
![](/assets/cloud-quickstart-guide/images/07B32250-AFB3-4FCA-A464-6907843C5313.png)

![](/assets/cloud-quickstart-guide/images/C1970516-2883-4A90-B9D2-CA2743612B38.png)

### メールアカウント

初期設定ウィザードからメールアカウントの配布設定を作成することができます。本書では後で設定しますので、このステップをスキップします。  
![](/assets/cloud-quickstart-guide/images/155AB72C-B141-42C8-88D8-435F3BA6A28B.png)


### パスコードポリシー

初期設定ウィザードからパスコードポリシー作成することができます。4桁、6桁、またはパスコード不要から好みの設定を選んで続行します。この設定は後で変更できます。  
![](/assets/cloud-quickstart-guide/images/6D780153-A450-4F1F-81F2-BF5B0C45A015.png)


### アプリの追加

初期設定ウィザードからユーザーのデバイスに配布したいアプリを追加することができます。本書では後で設定しますので、このステップをスキップします。  
![](/assets/cloud-quickstart-guide/images/BF6A85A0-A174-4B01-A88F-34A2F63DED56.png)


### ユーザーを招待

初期設定ウィザードからデバイス利用者のユーザーを作成し、デバイス登録の招待メールを送信することができます。本書では後で設定しますので、このステップをスキップします。  
![](/assets/cloud-quickstart-guide/images/EA560C7E-4AD5-49B5-B03E-413F67C86852.png)

### 初期設定ウィザードを完了

完了をクリックします。
![](/assets/cloud-quickstart-guide/images/DE53960E-AFD6-4F43-B9AE-480F8D932543.png)


## ダッシュボード

初期設定ウィザードが完了すると、ダッシュボードが表示されます。画面右上の「最新！」で画面構成を新しいものに切り替えることができます。新しい画面構成は横長のディスプレイに適しています。  
![](/assets/cloud-quickstart-guide/images/4DD313D1-F20A-433E-92D2-B486D562DE63.png)

![](/assets/cloud-quickstart-guide/images/DE265801-4C71-4A98-8A24-E46249B4A176.png)
