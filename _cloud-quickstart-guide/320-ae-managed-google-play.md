---
title: "Managed Google Playでアプリを配布する"
permalink: /cloud-quickstart-guide/ae-managed-goole-play/
---

Android Enterpriseにおいて仕事領域へのアプリの配布にはManaged Google Playを利用します。Managed Google Playは、通常個人で利用するGoogle Playとは別に、お客様組織専用に用意されたGoogle Playで、企業で利用したいパブリックアプリとインハウスアプリを登録して配布することができます。  
なおMobileIron CloudにおいてはManaged Google Playの管理画面を直接利用することはありません。全ての操作はMobileIron Cloudの管理コンソール上からできるようになっています。

Chromeを仕事領域に配布してみましょう。Chromeは個人領域に既にインストールされていますが、Android Enterpriseでは仕事領域にもChromeをインストールし、個人領域のChromeとは別のアプリ（アイコン）として利用することができます。

［アプリ］>［アプリカタログ］>［+追加］> Google Playを選択し、Chromeを検索  
![](/assets/cloud-quickstart-guide/images/3A7FD612-85C0-4B19-967A-83C4CB0D09AE.png)

<div class="notice--info">
<p><strong>ヒント</strong> もしこの画面の検索でうまく目的のアプリが見つけられない場合、アプリの名前ではなくIDを使って検索すると確実です。アプリのIDは下図のようにGoogle PlayのWebサイトで目的のアプリを検索し、そのページのURLから確認できます。</p>
<p><img src="/assets/cloud-quickstart-guide/images/CE8C3A92-3392-4AAD-B4F3-616BB16B913F.png"></p>
</div>

目的のアプリを選択し、［承認］ボタンをクリック。  
![](/assets/cloud-quickstart-guide/images/B9BEA9B9-A06F-47BF-96FD-012710B6CCBA.png)

アプリが要求する権限を確認し、［承認］をクリック。  
![](/assets/cloud-quickstart-guide/images/27189953-B391-4460-AF6D-16E8621D353B.png)

アプリが将来のバージョンで新しい権限を要求するようになった場合の取り扱いを決めておきます。信頼できる開発元であれば承認を維持して問題ないでしょう。［完了］をクリック。  
![](/assets/cloud-quickstart-guide/images/AAC605AF-B4E4-483E-9B73-D048D7B93263.png)

［次へ］をクリック。  
![](/assets/cloud-quickstart-guide/images/47A27472-D6CE-4FAC-B953-475A65713551.png)

必要に応じてApp Catalog上でのカテゴリを設定します。デフォルトではGoogle Playで設定されているカテゴリが適用されます。  
![](/assets/cloud-quickstart-guide/images/40E0D834-298C-4EA8-8FCA-F0E7F7B49355.png)

［次へ］をクリック。  
![](/assets/cloud-quickstart-guide/images/2E2C65EE-9FB2-45B9-92E7-1EDD3F3F625C.png)

このアプリの配布対象とするユーザーを選択します。特定のユーザーグループにのみ配布したい場合には「カスタム」を選択し、対象ユーザーグループを指定します。次へをクリック。  
![](/assets/cloud-quickstart-guide/images/12032BB1-66C2-4DE2-BFD6-82732BD906F0.png)

## アプリの設定

アプリによってはMobileIron Cloudから設定を配布できるものがあります。Google Chromeもその一つです。

Android用マネージド構成を［ + ］ボタンで追加します。  
![](/assets/cloud-quickstart-guide/images/D680FCE5-4F03-46CF-82C9-9264165255FF.png)

アプリの開発者が設定項目を用意している場合、マネージド構成の設定フォームが表示されます。  
![](/assets/cloud-quickstart-guide/images/6F5F6571-EA8F-4BEB-9BEE-3743FEA15689.png)

ブックマークを追加してみましょう。  
![](/assets/cloud-quickstart-guide/images/D86F7F8E-507D-4114-B359-31E43390EB39.png)

Google ChromeのブックマークはJSON形式で記述します。階層構造を持たせることもできます。またMobileIron Cloudのユーザー属性やデバイス属性を利用することもできます。

**例：** [ { "name": "MobileIron", "url": "https://www.mobileiron.com/" }, { "name": "マイデバイス", "url": "https://ap1.mobileiron.com/user/login.html?uid=${userUID}" }, { "name": "社内", "children": [ { "name": "サイト1", "url": "http://site1.yourdomain.com" }, { "name": "サイト2", "url": "http://site2.yourdomain.com" } ] } ]
{: .notice}

一番下までスクロールすると、アプリ設定の配布対象ユーザーを指定することができます。アプリを利用する全員、またはカスタムでユーザーグループを選択し、次へ。  
![](/assets/cloud-quickstart-guide/images/0883805F-9DA1-4363-85DE-8350762247A7.png)

## 自動インストール

アプリのインストールは、デフォルトの設定ではユーザーが仕事用のGoogle Playからインストール操作を行う必要がありますが、自動インストールに設定しておくこともできます。

「デバイスにインストール」の設定を開きます。デフォルトで１つの設定が作成されています。  
![](/assets/cloud-quickstart-guide/images/0BA9BF72-C51E-4842-A4CB-17F544FD618E.png)

デフォルトでは「デバイスにインストール」がOFFになっています。Chromeを自動でインストールさせたい場合、ONに変更して［次へ］をクリック。  
![](/assets/cloud-quickstart-guide/images/D99174CF-1EFB-4E02-B7ED-9015723B5CED.png)

［完了］をクリック。  
![](/assets/cloud-quickstart-guide/images/1FC07BA3-A259-4C31-8760-152254CA155F.png)

以上でGoogle ChromeアプリをMobileIron CloudのApp Catalogにインポートし、Android Enterpriseデバイスが登録された際には自動的にManaged Google Playを通じて仕事領域にインストールする設定が完了しました。またマネージド構成として配布したブックマークもChromeアプリで利用できるようになります。
