---
title: "macOSデバイスを登録する"
permalink: /technotes/macos-quickstart/device-registration/
sidebar:
    nav: "macos-quickstart"
---

お使いのmacOSデバイスを登録することで、MobileIronの管理対象にすることができます。
デバイスの登録は以下２種類の方法のいずれかで行います。

- SafariからWebで行う方法
- MobileIronのエージェントアプリ「Mobile@Work」を使った方法

## Safariを使った登録

ここでは、Safariから登録する手順を解説します。お使いのmacOSデバイスでSafariを起動し、MobileIronのデバイス登録用Webページ（mobileiron.com/go）を開きます。ユーザー名を入力し、［次へ］をクリックします。  
![](/assets/technotes/macos-quickstart/e4eca912-0540-446d-80ea-ae4f1dd891cf.png)

続けてパスワードを入力し、［サインイン］をクリックします。  
![](/assets/technotes/macos-quickstart/3377f964-b6ac-430a-9e9d-acd88d826e46.png)

サインインに成功すると、ファイルのダウンロードの許可を求めるダイアログが表示されるので、そのまま［許可］をクリックします。  
![](/assets/technotes/macos-quickstart/641cf2fe-e463-4208-af85-d1c961e57682.png)

プロファイルのダウンロードが行われ、プロファイルサービス登録の確認ダイアログが表示されます。  
［インストール］を選択し、プロファイルサービスを登録します。  
![](/assets/technotes/macos-quickstart/ffd2a128-92ad-49af-b0dc-9cd8478464b0.png)

続けて、”Root MDM Profile”のインストールダイアログが表示されます。 
［インストール］をクリックします。  
![](/assets/technotes/macos-quickstart/b833d531-560e-4b7a-9115-9acca3a3f9d4.png)

システムへの変更を許可する認証ダイアログが表示されますので、ユーザ名、パスワードを入力して［OK］をクリックします。  
![](/assets/technotes/macos-quickstart/bd4ad056-fa01-45ba-b5f7-7f71c491f51b.png)

プロファイルをインストールが完了すると、MobileIron Cloud で設定されているプロファイルがダウンロードされます。  
MobileIron 用のアプリカタログ「App Catalog」も自動でインストールされます。（緑のアイコン）  
企業で管理されたアプリのインストールはこのApp Catalogから行います。  
![](/assets/technotes/macos-quickstart/016f31e7-ef18-417c-becf-70b3f8d92390.png)

管理用端末のMobileIron管理画面では、デバイスの登録が完了すると、［デバイス］→［デバイス］のリストに追加されます。ユーザー名やOS、デバイスの種類などを確認することができます。個々のデバイスの管理はこの画面で行います。  
![](/assets/technotes/macos-quickstart/72416f27-1f05-4144-a6a0-6c4df0ae57a9.png)

Safariを使ったmacOSデバイスの登録は以上です。 

デバイス登録の完了後、MobileIron Cloudからの命令により、Mobile@Workが自動的にインストールされます。

## Mobile@Work を使った登録

MobileIronのクライアントアプリ「Mobile@Work」を使ってmacOSデバイスを登録する方法を解説します。

macOS版のMobile@WorkはMobileIron Cloudのアプリカタログに登録しましたが、この場合Mobile@Workを先にデバイスにインストールしておく必要があるため、MobileIronのサポートサイトからmacOS版Mobile@Workの最新パッケージをダウンロードします。購入前の検証でサポートサイトにアクセスできない方は担当の営業やSEにご連絡下さい。

Mobile@Workのダウンロード  
https://support.mobileiron.com/support/CDL.html  
IDとパスワードを入力し、ダウンロードサイトにアクセスします。  
![](/assets/technotes/macos-quickstart/7917FD29-6162-487E-B206-288404A226BB.png)  

Mobile@Works for macOSをクリックします。  
![](/assets/technotes/macos-quickstart/7B8BAB24-D304-4086-AC73-7FF1C321CA5C.png)

Mobile@Workのパッケージファイル（Mobileatwork-X.XX.X.pkg)をクリックしてダウンロードします。  
![](/assets/technotes/macos-quickstart/1713CCA2-96ED-4DB8-ACFC-9D05D32F8EDA.png)

これで、Mobile@Workのダウンロードは終了です。

登録するmacOSデバイスでMobile＠Workのインストールパッケージ（Mobileatwork-X.XX.X.pkg)を開きます。インストーラを起動すると以下のウィンドウが表示されますので、［続ける］をクリックします。  
![](/assets/technotes/macos-quickstart/6cae6afc-f0ae-443f-8b26-5af70be4620e.png)

インストール先のディスクに問題がなければ、［インストール］をクリックします。  
![](/assets/technotes/macos-quickstart/2832e21a-e4e7-4523-8e05-083f744d9e0c.png)

インストール実行時に管理者権限の認証ダイアログが表示されますので、パスワードを入力し、［ソフトウェアをインストール］をクリックします。  
![](/assets/technotes/macos-quickstart/a4735c2e-c1b3-4fcc-ac86-f068c72e44bd.png)

インストール処理が実行されますので、完了を待ちます。 
![](/assets/technotes/macos-quickstart/ff20dd14-4e4b-440e-b664-470da4418a0a.png)

インストール完了が表示されたら、［閉じる］をクリックしてインストーラを終了させます。 
![](/assets/technotes/macos-quickstart/35ad3522-866b-4cd7-96fd-786e0cb707f3.png)

インストールが完了すると「Mobile@Work」が起動します。EULAが表示されますので、「Don`t show this again」にチェックを入れて［I Agree］をクリックしてEULAに同意してください。  
![](/assets/technotes/macos-quickstart/60734d2c-46b8-4fcd-9076-42569cb416da.png)

MobileIronへの登録画面が表示されますので、ユーザのIDを入力して［Next］をクリックします。  
![](/assets/technotes/macos-quickstart/8da62da2-39d2-4e0f-bdab-a96e182200c8.png)

パスワードを求められますので、ユーザのパスワードを入力し、［サインイン］をクリックします。  
![](/assets/technotes/macos-quickstart/5f675e2f-0fbf-429e-85d4-103ca3ce3805.png)

認証に成功すると、以下の画面が表示され別ウィンドウでSafariが起動し、構成プロファイルがダウンロードされます。  
![](/assets/technotes/macos-quickstart/67c2e844-4a06-4a20-8a35-a4d8792d6557.png)

ダウンロード後、Mobile@Workがサーバに登録を行い、アプリケーションカタログを表示するまで待ちます。  
![](/assets/technotes/macos-quickstart/9d474c95-6751-4146-a3f8-17fa859c8011.png)

ここまで表示されたら、Mobile@Workでの作業は完了です。Mobile@Workの画面を閉じてSafariの画面に移動します。  
![](/assets/technotes/macos-quickstart/30317f3f-92f8-4bbf-90f8-36560931e207.png)

Safariのウィンドウでは、ダウンロードの許可ダイアログが表示されています。［許可］をクリックして構成プロファイルのダウンロードを許可します。  
![](/assets/technotes/macos-quickstart/cbaa808f-ec18-4834-9ab1-3af96eee46f9.png)

構成プロファイルがインストールされ、システム環境設定にプロファイルサービスを追加する確認ダイアログが表示されます。［インストール］をクリックしてインストールを許可します。  
![](/assets/technotes/macos-quickstart/69585793-e5dd-4354-9825-8c4e44cc2a77.png)

プロファイルサービスのインストール後、MDMプロファイルのインストール確認ダイアログが表示されます。［インストール］をクリックしてインストールを許可します。  
![](/assets/technotes/macos-quickstart/db840e33-666c-4b22-92cf-a47683050eb4.png)

管理者権限の認証ダイアログが表示され、変更の許可を確認します。パスワードを入力し、［OK］をクリックします。  
![](/assets/technotes/macos-quickstart/e7b9a36a-06f8-45a7-a8cb-ff29eddb85ca.png)

Root MDM Profileがインストールされたら、作業は完了です。次回、チェックインのタイミングで追加のプロファイルがダウンロードされます。  
![](/assets/technotes/macos-quickstart/30297471-c8c3-4c8f-9211-7f9ac8fedfd1.png)

参考：チェックイン後、プロファイルが追加された画面  
![](/assets/technotes/macos-quickstart/029fa630-01f2-4033-ae43-bdab0a6f6cc9.png)

※ チェックインがなかなかされない場合には、強制チェックインを管理サーバから行うか、デバイスの再起動後、再度ログインしてください。  

MobileIron管理画面にログインして、登録ができていることを確認してください。  
![](/assets/technotes/macos-quickstart/6c961dc0-38f2-49e7-8357-d5a3a031d7b8.png)

ここまでで、Mobile@Workを利用したmacOSデバイスの登録は完了です。


