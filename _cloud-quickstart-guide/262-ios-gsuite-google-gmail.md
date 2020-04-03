---
title: "GoogleのアプリでG Suiteを利用する"
permalink: /cloud-quickstart-guide/ios-gsuite-google-gmail/
---
G SuiteをGmailなどGoogleが提供するアプリで使う場合の設定について解説します。残念ながらGmailアプリへのアカウント設定は、アプリ側に受け取る仕組みが無いため、MobileIron Cloudから配布することができません。したがってGmailアプリをMobileIron Cloudから管理アプリとして配布する設定のみを行います。

MobileIron Cloudの［アプリ］→［アプリカタログ］を開きます。  
![](/assets/cloud-quickstart-guide/images/38EE737B-41DE-41DD-8327-CD06ACADD670.png)

検索ボックスにアプリ名の一部「Gmail」を入力します。検索されたアプリ「Gmail - Eメール by Google」を選択し、［次へ］をクリックします。  
![](/assets/cloud-quickstart-guide/images/D26983DE-2917-414A-A92E-6F2BF0880307.png)

アプリの情報が表示されます。そのまま［次へ］をクリックしてください。  
![](/assets/cloud-quickstart-guide/images/3A9B2B2E-CF12-4A2F-8B67-1AB152AC15BB.png)

「アプリ委譲」の設定画面が表示されます。デフォルトの設定（［このアプリを委譲しない］）のまま、［次へ］をクリックしてください。  
![](/assets/cloud-quickstart-guide/images/2758D38D-8B1D-4FBF-A1D7-37AB2C674726.png)

配布先の設定画面が表示されます。デフォルトの設定（［全員］）のまま、［次へ］をクリックしてください。  
![](/assets/cloud-quickstart-guide/images/D2157E71-A31E-462F-AB74-C848D8C29013.png)

必要に応じてアプリ構成を追加します。たとえば、追加した管理アプリをインストールするようユーザーに要求するなら、「デバイスにインストール」オプションを設定してください。最後に［完了］をクリックしてください。  
![](/assets/cloud-quickstart-guide/images/AE1B2005-B017-43B1-AF08-833884AD2394.png)

「アプリカタログ」画面に自動で切り替わります。追加したGmailアプリが一覧に表示されたことが確認できます。  
![](/assets/cloud-quickstart-guide/images/55FDDF99-7C57-4928-86D9-6E5208789B79.png)

これで管理画面での作業は完了です。次に、iOSデバイスでGmailをインストールしましょう。

App Catalog のアイコンをタップして開きます。「新規リリース」にGmailアプリが追加されているので、［インストール］をタップします。（「デバイスにインストール」オプションを有効にしている場合は、App Catalogを開かなくてもチェックイン時にGmailアプリのインストールが促されます）  
![](/assets/cloud-quickstart-guide/images/0BD57919-2BC4-4656-89C8-29922FC95798.png)

確認ダイアログが表示されるので、［インストール］をタップしてください。  
![](/assets/cloud-quickstart-guide/images/FBD12551-D316-4D74-83F8-D186275378A1.png)

Gmailアプリがインストールされました。  
![](/assets/cloud-quickstart-guide/images/B24FD7B4-BD1B-4E39-B4C3-0F883F35048F.png)

Gmailアプリを開くとログインを求められます。このアプリにはアカウント設定が配布できないので、ここから先のG Suiteへのログイン手順はアプリのインストールにMobileIron Cloudが介在していない場合と全く同じになります。  
![](/assets/cloud-quickstart-guide/images/E31FEB93-9734-442C-ACFA-17E802E33533.png)

![](/assets/cloud-quickstart-guide/images/77FD4028-FB05-44B2-99D3-618429F0C31A.png)

![](/assets/cloud-quickstart-guide/images/DEB712F4-D3DA-4C3D-86D9-0EE1E591BE71.png)

Googleアカウントは手入力する必要があります。  
![](/assets/cloud-quickstart-guide/images/94606FE8-A695-4D27-93BE-A74DA9FFD365.png)

![](/assets/cloud-quickstart-guide/images/A3FE14DD-D595-423C-8C95-8A01F6A6522B.png)

ログインに成功するとメールにアクセスできます。  
![](/assets/cloud-quickstart-guide/images/F47134FC-FD87-4A74-8B30-D04F0E66A6EF.png)
