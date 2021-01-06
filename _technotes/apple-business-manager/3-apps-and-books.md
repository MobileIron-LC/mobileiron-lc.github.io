---
title: "アプリの一括購入とMDMによるライセンス割当て"
permalink: /technotes/apple-business-manager/apps-and-books/
sidebar:
    nav: "apple-business-manager"
---

仕事で利用するiOS(iPadOS)アプリ,macOSアプリを、組織で一括購入し、そのライセンスをMDMを通じて管理対象デバイスに割り当てるための設定について解説します。ABM以前には VPP: Volume Purchase Program の名称で提供されていた機能です。

## Apple Business ManagerとMobileIron Cloudを連携する

アプリの一括購入とMDMによるライセンス割当には、ABMとMDM（MobileIron Cloud）の連携設定が必要です。この連携設定は自動デバイス登録のための連携とは別に行うものです。

はじめにABMでアプリのライセンスを利用する「場所」を作成します。ABMにおける「場所」とは、アプリを利用する組織内のあるグループを表す概念です。必ずしも物理的な場所によるグルーピングである必要はありません。ABMテナントの初期状態では、登録時に入力した組織情報を反映した場所が１つ用意されているはずです。これをそのまま利用しても構いませんし、新たに場所を作成しても構いません。  
![](/assets/technotes/apple-business-manager/EEB76EB3-604B-4691-8EF9-792294A49DA9.png)  

場所を追加する場合には右ペインの「＋」をクリックします。

![](/assets/technotes/apple-business-manager/18D0E6D1-66DD-4E14-9AE2-97326D40724F.png)

［設定］＞［Appとブック］画面から、ABMに登録されているそれぞれの場所に対応するサーバートークンのダウンロードができます。MobileIron Cloudと連携して利用したい場所のサーバートークンをダウンロードします。  
![](/assets/technotes/apple-business-manager/CB5FBE25-85CA-450C-8038-1E1DDF8D938E.png)

場所を新規追加してもすぐにこの画面に反映されない場合、一度ABMからサインアウトして、再度サインインすると表示されることがあります。
{: .notice--info}

１つの場所に対応するサーバートークンを２つ以上のMDMサーバにインストールしないで下さい。組織にMDMサーバが複数ある場合には、それぞれのMDMサーバのために場所を作成して下さい。
{: .notice--info}

MobileIron Cloudの［アプリ］＞［Apple Appとブック］＞［＋Appとブック sTokenを追加］ボタンをクリックします。  
![](/assets/technotes/apple-business-manager/8E535A8D-E6F3-4D19-B01D-8D0F90E108F6.png)

ABMからダウンロードしたサーバートークンをドラッグ&ドロップでアップロードします。  
![](/assets/technotes/apple-business-manager/5DFF3EC5-E93F-4C6C-B992-C7E7A102C095.png)

![](/assets/technotes/apple-business-manager/965E47BF-7A4D-426B-AE6D-CB0B4709ABBD.png)

以上でアプリの一括購入とMDMによるライセンス割当に必要なABMとMobileIron Cloudの連携設定は完了です。


## トークンの更新を忘れずに！

サーバートークンには１年間の期限が設定されています。期限が近くなったら、ABMから同じ場所のサーバートークンを改めてダウンロードし、MobileIron Cloudにアップロードすることで更新できます。

上の画面でセキュアトークンの「表示」をクリックします。

ABMからダウンロードした更新サーバートークンは「sTokenを更新」からアップロードできます。  
![](/assets/technotes/apple-business-manager/B00ACB4C-C95F-466F-ADF0-CCFD747C0136.png)


## ABMでアプリを購入する

それではいよいよ、ABMでアプリを購入し、MobileIron Cloudの登録デバイスに配布してみます。

ABMの［Appとブック］画面で購入したいアプリを検索します。ここではMobileIron Goアプリを検索しました。  
![](/assets/technotes/apple-business-manager/19EB20AC-A1D1-455F-A598-B2C10706C82D.png)

このアプリのライセンスを利用する「場所」を選択し、数量を入力して［入手］ボタンをクリックすると購入できます。

なお上の画面に表示されているように、複数の場所を利用している場合には、使用中（デバイスやユーザーに割り当て済み）でないライセンスは場所間で転送が可能です。

購入したアプリのライセンス数は、しばらくするとMobileIron Cloudに反映されます。  
確認するには［アプリ］＞［Apple Appとブック］画面で、該当する場所のアカウント名をクリックします。  
![](/assets/technotes/apple-business-manager/805C1DE6-CF75-4C33-B48A-EEBCD10D41C3.png)

ABMとの同期により、購入したアプリと利用可能なライセンス数が表示されています。  
![](/assets/technotes/apple-business-manager/33CBA928-3A2F-422F-AC6A-763FCFA3BE1A.png)

［アプリ］＞［アプリカタログ］から対象のアプリを選択します。まだアプリカタログに登録していない場合は登録を済ませて下さい。  
ABMでライセンスを購入しているアプリでは、ライセンスのタブが表示されます。  
![](/assets/technotes/apple-business-manager/060DF51F-5505-4A97-823C-DC9F471727DE.png)

アカウント名のリンクをクリックし、このアプリのライセンスの割り当てについて設定していきます。  
![](/assets/technotes/apple-business-manager/3DD23368-7568-4FA9-9BF0-86F8ED7B2081.png)  
［編集］ボタンをクリックすると設定が変更できます。

殆どのユースケースでは、一括購入したアプリのライセンスを全てのユーザー（All Users）で利用可能にし、さらにユーザーのApple IDが不要なデバイスベースのライセンスが適していますので、以下のような設定になります。  
![](/assets/technotes/apple-business-manager/5388CCD8-CE10-4DD9-AFFB-07D4478D5B2B.png)

上にスクロールして［保存］ボタンをクリックし、設定を完了します。
