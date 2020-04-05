---
title: "iOSデバイスを登録する"
permalink: /cloud-quickstart-guide/ios-registration/
---
お使いのiOSデバイスを登録することで、MobileIronの管理対象にすることができます。デバイスの登録は以下のいずれか方法で行うことができます。
- MobileIron Go アプリを使って
- Safari を使って
- Automated Device Enrollment

Automated Device Enrollmentは、以前はDEP: Device Enrollment Programと呼ばれていた方法で、企業で購入したiOSデバイスの最初の電源投入時あるいは初期化後に自動的にMobileIron Cloudへ登録させるものです。本ガイドでは触れませんが大変便利です。
{: .notice--info}

## MobileIron Go アプリを使ってiOSデバイスを登録する

はじめにMobileIronのクライアントアプリ「MobileIron Go」を使ってiOSデバイスを登録する方法を解説します。

iOSデバイスでAppStoreを開き、MobileIron Goを検索してインストールします（AppStoreにApple IDでログインしている必要があります）。インストールが終了したら、そのままインストール画面の［開く］をタップして「MobileIron Go」を起動してください。  
![](/assets/cloud-quickstart-guide/images/3E68E195-6450-428F-9143-2FA84C9D2028.png)

インストール画面を閉じてしまった場合は、ホーム画面のMobileIron Goのアイコンをタップして起動します。  
![](/assets/cloud-quickstart-guide/images/342969C0-7C33-43C4-B340-B18EC389A747.png)

「MobileIron Go」を初めて起動すると、免責条項が表示されるので、一読したら［続行］をタップしてください。  
![](/assets/cloud-quickstart-guide/images/9382F4ED-B27B-44D6-B183-49BE9B97DE95.png)

次にユーザー名を入力し、［次へ］をタップします。  
![](/assets/cloud-quickstart-guide/images/B1447284-5F74-4DFB-9EDF-E1943B2E4E04.png)

パスワードを入力し、［サインイン］をタップします。  
![](/assets/cloud-quickstart-guide/images/A1E9172E-F096-44FC-AAD8-3B3EE84B30D4.png)

サインインに成功すると、以下の画面が表示されます。［ありがとう、理解しました］をタップしてください。  
![](/assets/cloud-quickstart-guide/images/4D6671BB-3AD3-434C-A3A3-E6A30FC955AA.png)

続けて［OK］をタップしします。「MobileIron Go」での操作は以上です。  
![](/assets/cloud-quickstart-guide/images/BFE05BBC-A06E-4428-88B8-E6B07FD6331E.png)

Safariに自動で切り替わり、プロファイルのダウンロードの許可を求めるダイアログが表示されます。［許可］をタップしてください。  
![](/assets/cloud-quickstart-guide/images/6E65BA7C-73C7-4EBF-A0FC-90209E95E325.png)

プロファイルのダウンロードが完了したら、［閉じる］をタップしてください。  
![](/assets/cloud-quickstart-guide/images/35773E2D-FC7C-4422-B258-24E597AFCD03.png)

ダウンロードしたプロファイルは手作業でインストールする必要があります。数分以内にインストールしないと無効になるので注意しましょう。
インストールは「設定」アプリで行います。「設定」アプリを開くと、ユーザー名の下に「プロファイルがダウンロードされ…」と表示されるので、その部分をタップします。  
![](/assets/cloud-quickstart-guide/images/A6FA7CF8-6466-4779-9084-53C8540B9361.png)

プロファイルの画面が表示されます。画面右上にある［インストール］をタップします。  
![](/assets/cloud-quickstart-guide/images/C7A6A60F-B5BE-47F0-A4CC-F43D329888DA.png)

パスコードを求められるので、現在の画面ロックパスコードを入力します。  
![](/assets/cloud-quickstart-guide/images/E4403864-3F3D-4CC9-BF24-9A433350318D.png)

続けて、画面下部の［インストール］をタップします。  
![](/assets/cloud-quickstart-guide/images/5AFDEA59-34C3-4960-8EAF-72C3B8860DC1.png)

さらに画面右上の［インストール］をタップします。  
![](/assets/cloud-quickstart-guide/images/974AD3D0-DF9B-45C7-B92B-7BCDC0FC5EA1.png)

「リモート管理」の［信頼］をタップします。  
![](/assets/cloud-quickstart-guide/images/8AE4C1F8-B6CC-4106-B0AC-E1BC4673085C.png)

これでプロファイルのインストールが完了しました。［完了］をタップします。  
![](/assets/cloud-quickstart-guide/images/606C69AD-EECB-43E8-A9AB-5E8C109310F1.png)

インストールしたプロファイルは「設定」アプリの［一般］→［デバイス管理］で確認できます。  
![](/assets/cloud-quickstart-guide/images/A7B82FE8-9682-45E7-AE77-B71F05B79965.png)

これでデバイス登録は完了です。

もう一度MobileIron Goアプリを開くと、以下のように登録済みの画面が表示されます。  
![](/assets/cloud-quickstart-guide/images/622BA4A8-1634-48FD-9F00-2241ABD00B73.png)


MobileIron Cloudの管理画面では、デバイスの登録が完了すると、［デバイス］→［デバイス］のリストに追加されます。ユーザー名やOS、デバイスの種類などを確認することができます。個々のデバイスの管理はこの画面で行います。  
![](/assets/cloud-quickstart-guide/images/928C1980-EC48-4C53-AC57-F9925B3F2DC2.png)


## Safariを使ってiOSデバイスを登録する

MobileIron Goの代わりにSafariを使ってデバイスを登録する手順を解説します。お使いのiOSデバイスでSafariを起動し、MobileIronのデバイス登録用Webページ（mobileiron.com/go）を開きます。ユーザー名を入力し、［次へ］をタップします。  
![](/assets/cloud-quickstart-guide/images/50FF167D-7249-4E4A-AC51-3B8916B47D06.png)

続けてパスワードを入力し、［サインイン］をタップします。  
![](/assets/cloud-quickstart-guide/images/C8238A83-FECA-45C5-8240-725E2982C1A1.png)

サインインに成功すると、構成プロファイルのダウンロードの許可を求めるダイアログが表示されるので、そのまま［許可］をタップします。  
![](/assets/cloud-quickstart-guide/images/C756947D-3E8F-4EBA-B279-9BB7D6C5E149.png)

プロファイルのダウンロードが完了したら、［閉じる］をタップします。Safariでの操作はここまでです。  
![](/assets/cloud-quickstart-guide/images/9187FE36-E060-4A2F-BB07-06EE83E606DF.png)

ダウンロードしたプロファイルは手作業でインストールする必要があります。数分以内にインストールしないと無効になるので注意しましょう。インストールは「設定」アプリで行います。「設定」アプリを開くと、ユーザー名の下に「プロファイルがダウンロードされ…」と表示されるので、その部分をタップします。  
![](/assets/cloud-quickstart-guide/images/7D6455C4-ED91-4067-8A0F-89E31A938241.png)  
以降のプロファイルのインストール操作は、MobileIron Goを使ってデバイス登録を始めた場合と同じです。

以上でデバイス登録は完了ですが、しばらくするとMobileIron Goアプリのインストールが促されます。「Appのインストール」ダイアログが表示されたら［インストール］をタップしてください。インストールしたMobileIron Goアプリは一度だけ手作業でタップして開いて下さい。これによりMobileIron Goアプリの登録処理が行われます。（認証は必要無く、自動的に完了します）  
![](/assets/cloud-quickstart-guide/images/342969C0-7C33-43C4-B340-B18EC389A747.png)

![](/assets/cloud-quickstart-guide/images/622BA4A8-1634-48FD-9F00-2241ABD00B73.png)

<div class="notice--info">
<p><strong>Apple MDM と MobileIron Go の関係</strong></p>

<p>上記いずれの手順でもMobileIron Goアプリのインストールを行いましたが、実はApple MDMのしくみで定義されている全てのコントロールはMobileIron Goアプリ無しで実行できます。Apple MDMとしてのデバイス登録は、MDMプロファイルをインストールすることによって完結するもので、MobileIron Goアプリとは直接関係がありません。Apple MDMを使った管理操作には、インベントリ情報の取得、アプリのインストール、Wi-Fiなどの構成プロファイルのインストール、証明書の配布、ロック、ワイプなどが含まれます。</p>

<p>ではMobileIron Goアプリは何のためにインストールするのでしょうか？
MobileIron GoアプリはApple MDMで定義されている以外の、MobileIron独自の機能を提供するもので、ユーザーへのプライバシー情報の提供、位置情報の取得、管理者からの通知メッセージの受信、モバイル脅威防御、ゼロ・サインオンなどが含まれます。</p>
</div>

<div class="notice--info">
<p><strong>MobileIron Goからデバイス登録と、Safariからデバイス登録の違い</strong></p>

<p>どちらの方法で登録を開始しても、順番が変わるだけで結果としてMDMプロファイルのインストールとMobileIron Goアプリのインストールが行われました。MobileIron Goアプリから登録を開始する場合、AppStoreからMobileIron Goアプリをダウンロードするために、ユーザーのApple IDが必ず必要になります。これは特に会社支給のデバイスでApple IDが作成されていないようなケースでは不都合です。一方Safariを使ってApple MDMとしてのデバイス登録を先に完了させた場合、MobileIron GoアプリのインストールはMDM命令として実行されています。このとき、本ガイドではやはりユーザーのApple IDが必要になりましたが、別途MobileIron CloudとApple Business Managerを連携し、アプリの一括購入とMDMによるライセンス割り当てを設定すれば、ユーザーのApple IDを使わずにMobileIron Goアプリを配布することが可能になります。</p>
</div>
