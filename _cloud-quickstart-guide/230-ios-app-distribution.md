---
title: "仕事のアプリを配布する"
permalink: /cloud-quickstart-guide/ios-app-distribution/
---
Apple AppStoreで公開されているアプリも、企業が自社内で開発したインハウスアプリも、MobileIronのアプリカタログ機能を使ってiOS端末に配布することで、企業の管理対象のアプリ（以下、「管理アプリ」）として管理することができます。「管理アプリ」にすると、個人用アプリ（非管理アプリ）へのデータ受け渡しの禁止などの制御をはじめ、さまざまな管理が可能となります。本ガイドではAppStore上の公開アプリを管理アプリとして配布する方法を解説します。

## アプリカタログのデフォルト設定

管理者は配布したいアプリを予めMobileIron Cloudの「アプリカタログ」に取り込みます。この際のデフォルト動作をはじめに設定しておきます。

MobileIron Cloud管理画面の［アプリ］→［カタログ設定］を開きます。
![](/assets/cloud-quickstart-guide/images/1BC07BC1-82A9-47BF-9A46-4F01D0C4A4C8.png)

「デフォルトのApp Storeの地域」のボックスで［Japan］を選びます。また「登録解除時にアプリを削除」を有効にしておくと、デバイスを管理から外す「撤去」のMDMアクションを行った場合に、仕事のアプリとそのアプリ内に保存されたデータが削除されます。設定を変更したら［保存］をクリックしてください。
![](/assets/cloud-quickstart-guide/images/BB7FA30D-1955-441B-8B12-DB36F2F3E3FE.png)

## AppStore上の公開アプリをカタログに追加する

仕事で利用したいアプリをアプリカタログに追加しましょう。ここではSalesforceアプリの追加を例に解説します。

MobileIron Cloud管理画面の［アプリ］→［アプリカタログ］を開きます。現在登録されている管理アプリが一覧表示されます。追加するには［+追加］をクリックします。
![](/assets/cloud-quickstart-guide/images/89F500D9-DDFD-4C4C-8336-DB1585B3CBB9.png)

いくつかのMobileIron製アプリが一覧表示されていますが、上部の検索ボックスに目的のアプリ名を入力するとAppStoreから任意のアプリを検索することができます。※検索ボックスの左側のアイコンがApple AppStoreのものになっていることを確認して下さい。
![](/assets/cloud-quickstart-guide/images/CDB92510-162F-46B2-A637-8FFBCCEBBEF7.png)

検索結果が表示されたら、目的のアプリをクリックして選択し、画面右下の［次へ］をクリックしてください。
![](/assets/cloud-quickstart-guide/images/D982CD74-81A0-4003-B2E4-DECAC774AA0D.png)

<div class="notice--info">
<p><strong>ヒント</strong> もしこの画面の検索でうまく目的のアプリが見つけられない場合、アプリの名前ではなく固有の識別子であるBundle IDを使って検索すると確実です。たとえばMobileIron GoアプリのBundle IDは"com.mobileiron.anyware.ios"です。</p>
<p>Bundle IDを見つけるのは少々面倒です。まずAppStoreのWebサイトで目的のアプリを探し、そのURLを確認します。たとえばMobileIron Goの場合は</p>
<p>https://apps.apple.com/jp/app/mobileiron-go/id672836503</p>
<p>です。このURLに含まれるidを使って、次の検索サービスのURLでアプリの情報を習得します。※idの引数を目的のアプリのものに変えて下さい。</p>
<p>http://itunes.apple.com/JP/lookup?id=672836503</p>
<p>検索結果はテキストファイルでダウンロードされ、中に含まれる"bundleId"の値でBundle IDを知ることができます。</p>
</div>

AppStoreから取り込まれたアプリの情報が表示されます。そのまま［次へ］をクリックしてください。
![](/assets/cloud-quickstart-guide/images/B20D3300-BDEF-4EE9-8013-A350D43D9CC8.png)

「アプリ委譲」の設定画面が表示されます。本ガイドでは使用しませんのでデフォルトの設定（［このアプリを委譲しない］）のまま、［次へ］をクリックしてください。
![](/assets/cloud-quickstart-guide/images/F3FB1313-7B7C-421E-8B24-CB3D3FCC8547.png)

配布先の設定画面が表示されます。デフォルトの設定（［全員］）のまま、［次へ］をクリックしてください。配布先をカスタム設定することで、特定のユーザーグループだけにこのアプリを配布することもできます。
![](/assets/cloud-quickstart-guide/images/7DC44B71-96B5-4050-A0DF-470C8DE864E5.png)

「アプリ構成」画面が表示されます。追加した管理アプリをインストールするようユーザーに要求するようにオプションを設定しましょう。デフォルトで作成されている「デバイスにインストール」の構成を編集するか、［+］をクリックして新規作成します。ここでは新規作成します。
![](/assets/cloud-quickstart-guide/images/6B10D577-56A9-47CD-B3A2-4EA2BB54A287.png)

「構成設定」画面が表示されます。まずは「名前」のボックスに任意の名前を入力します。続けて、［デバイスのインストール］のスライドスイッチをクリックしてオンにしたら、［次へ］をクリックしてください。
![](/assets/cloud-quickstart-guide/images/02D58960-C1AB-4796-BB22-8024F2E6156A.png)

これで「デバイスにインストール」オプションを設定できました。最後に［完了］をクリックしてください。
![](/assets/cloud-quickstart-guide/images/BE841849-CE01-4FE5-B34F-2108810A43BE.png)

「アプリカタログ」画面に自動で切り替わります。追加したアプリが一覧に表示されたことが確認できます。アプリのアイコンには「新着！」マークが付きます。
![](/assets/cloud-quickstart-guide/images/607FDB61-96E1-4644-95FD-104BE4A7852C.png)

これで目的のアプリを「アプリカタログ」に管理アプリとして追加できました。ユーザーはiOSデバイス上の「App Catalog」から手動でインストールできるようになります。さらに「デバイスにインストール」オプションが有効化されていると、デバイスのチェックイン時にインストール命令が送られます。この場合、ユーザーは「App Catalog」から手動でインストールする必要はありません。

チェックインとは、デバイスがMobileIron Cloudからの呼び出しを受けてMobileIron Cloudに接続し、命令を受け取る動作です。
{: .notice}

なお、「アプリ構成」の「iOSアプリの設定」に自動で追加される設定「iOSアプリケーション管理構成の設定。」に、［登録解除時にアプリを削除］という設定項目があり、デバイス撤去時にアプリとそのデータを自動で削除するのか、アプリごとに設定できます。この設定はアプリカタログの全体設定（［アプリ］→［カタログ設定］）にある同項目よりも優先されます。
