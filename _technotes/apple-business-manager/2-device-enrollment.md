---
title: "自動デバイス登録"
permalink: /technotes/apple-business-manager/device-enrollment/
sidebar:
    nav: "apple-business-manager"
---

組織で購入したiOS(iPadOS)デバイス,macOSデバイスを、自動的に組織のMDMに登録するための設定について解説します。ABM以前には DEP: Device Enrollment Program の名称で提供されていた機能です。

## Apple Business ManagerとMobileIron Cloudを連携する

自動デバイス登録を利用するために、Apple Business ManagerとMDMサーバ（MobileIron Cloud）を連携します。MobileIron CloudとABMからそれぞれキー（トークン）をダウンロードし、互いのキーをアップロードすることで連携ができます。MobileIron Cloud側から設定を開始します。

［管理］＞［Apple］＞［Device Enrollment］  
![](/assets/technotes/apple-business-manager/95CA68C7-8F18-4B14-A101-533E2B0916D1.png)  
［開始］ボタンをクリックします。  

![](/assets/technotes/apple-business-manager/5D374610-2BE9-4ABD-8C38-363268D84851.png)  
［キーをダウンロード］をクリックし、.pem ファイルを保存します。

キーを保存したら［business.apple.com］ボタンをクリックします。Webブラウザの新しいタブでApple Business Managerが開きますので、ABMの管理者となっているApple IDでサインインします。

［設定］＞［デバイス管理の設定］を開き、「MDMサーバを追加」します。  
![](/assets/technotes/apple-business-manager/6B2EAD99-1BCB-449E-9BE9-10F3DDFEA38B.png)  

任意のMDMサーバ名を付け、先ほどMobileIron Cloudからダウンロードしたキーをアップロードして［保存］します。  
![](/assets/technotes/apple-business-manager/6E053FF5-8A36-4A30-9875-97E7D441763E.png)  

ABMに新しい名前でMDMサーバが作成されました。このMDMサーバのための「トークンをダウンロード」します。  
![](/assets/technotes/apple-business-manager/178AB39E-BDF8-4C8C-870B-CEE2C3ECD955.png)  

![](/assets/technotes/apple-business-manager/CE0B7942-7085-4535-AB63-1593E2733891.png)  
サーバトークンは拡張子 .p7m のファイルとしてダウンロードされます。  

MobileIron Cloudの管理画面に戻ります。  
［アップロード］ボタンをクリックし、ABMからダウンロードしたトークンファイルをアップロードします。  
![](/assets/technotes/apple-business-manager/5817F97C-4972-4FA2-AE0D-E5D11ECED4CD.png)  

![](/assets/technotes/apple-business-manager/015326E0-8522-4685-AF6F-57ED77EB8B33.png)  
ABMとの接続が確認できました。［次へ→］をクリックします。

自動デバイス登録時の認証方法を設定します。デフォルトではMobileIron Cloudのユーザーでの認証を要求します。この設定は後から変更できます。  
![](/assets/technotes/apple-business-manager/07EDD385-1976-450D-B252-E92232D86A83.png)  
［次へ→］をクリックします。

自動デバイス登録の実行時にデバイスの監視モードやアクティベーションのユーザー体験を決定する「Enrollmentプロファイル」を設定します。  

組織で購入したデバイスをMDMに自動登録するユースケースでは、多くの場合「監視モード」を有効化するとともに、MDMを必須かつ削除不可能としてユーザーが勝手にデバイスをMDM管理から外すことを防ぎます。  
![](/assets/technotes/apple-business-manager/81207AFE-C4C1-4014-81E3-BB86A44B1AD2.png)  

画面を下にスクロールしてEnrollmentプロファイルのその他の項目を設定していきます。

**サポート電話番号とサポートメールアドレス**  
IT部門やヘルプデスクなど、組織内の適切な連絡先を入力します。

**カスタム登録Webページ**  
デバイスに表示される登録認証画面をカスタマイズする設定です。デフォルトの設定では、デバイスに組み込まれたベーシック認証画面（ID・パスワード）ですが、下のように設定することでMobileIron Cloudの認証画面が利用できます。またMobileIron Cloudのユーザー認証を「PIN+パスワード」や「SAML認証」としている場合にも対応できます。  
![](/assets/technotes/apple-business-manager/05EA1872-7E9B-4693-934E-6AE29027C039.png)

**ビジネス用の共有iPad**  
iPadデバイスをビジネス用の共有iPadとしてセットアップするための項目です。

**各種設定オプションのスキップ**  
自動デバイス登録では、アクティベーション中にユーザーが同意や設定を求められる様々な項目をスキップし、よりシンプルなユーザー体験を提供することができます。可能な限りの項目をスキップして問題ありませんが、例えばiOSデバイスの位置情報を取得したい場合、ここでスキップしてもいずれユーザーが位置情報サービスを有効にしなければならず、アクティベーション中に設定させる方が簡単です。

**macOSの管理アカウントおよびプライマリユーザーアカウントの作成**  
このmacOSのための設定は必須項目となっていますが、iOSデバイスのみをこのEnrollmentプロファイルの対象とする場合には「管理アカウント作成をスキップ」にチェックを入れたのみの設定としておけば大丈夫です。
![](/assets/technotes/apple-business-manager/597FD2D7-B187-4D52-83E4-05AFB241E31A.png)

macOSにおいてはアクティベーション中に管理権限を持つユーザーアカウントを必ず作成する必要があります。  
以下の設定例では、MobileIron Cloudユーザーと同名のユーザーを、管理権限を持つプライマリとして作成するものです。このようにユーザー属性（変数）の利用が可能です。  
![](/assets/technotes/apple-business-manager/A9A402E6-93D3-43B2-AE17-8D13C930F4A9.png)

最後に［保存］ボタンをクリックしてEnrollmentプロファイルを保存します。

![](/assets/technotes/apple-business-manager/6A88E0FD-28AA-4AF3-9182-23D82AF71FC4.png)

以上で自動デバイス登録を利用するためのABMとMobileIron Cloudの連携設定は完了です。


## ABMでデフォルトのMDMサーバを設定する

今後新規に購入し、ABMに登録されるデバイスを自動的にデフォルトのMDMサーバに割り当てるには、  
［設定］＞［デバイス管理の設定］でデバイスの種類ごとにデフォルトのMDMサーバを選択します。  
![](/assets/technotes/apple-business-manager/E0BE26AC-0360-4E0F-BB15-816E8CF1FEBF.png)  

## ABMに登録済みのデバイスに割り当てるMDMサーバを変更する

既にABMに登録済みのデバイスを、新しいMDMサーバに再割り当てすることも簡単にできます。  
［デバイス］画面からシリアル番号、注文番号、デバイスの種類などで対象のデバイスを検索し「デバイス管理を編集」します。下図のように複数のデバイスを抽出すると、まとめて新しいMDMサーバに割り当てることができます。  
![](/assets/technotes/apple-business-manager/8040F4D6-2050-4F3D-919E-5CF8929649B3.png)

「デバイス管理を編集」をクリックして、対象のデバイスに対する新しいMDMサーバを選択します。

![](/assets/technotes/apple-business-manager/2609DA78-FFE7-487C-B4E0-61A38ECB1EE8.png)  

![](/assets/technotes/apple-business-manager/EDB5300C-AC67-4F73-A169-64359A6CEEBC.png)

ABMでのデバイス管理の変更が、割り当て先のMobileIron Cloudで認識されると、デバイス数のカウントが変化します。  
![](/assets/technotes/apple-business-manager/8DCCBEAC-6EA6-490D-A310-13543439C8CB.png)

割り当て先となったMDMサーバへの自動デバイス登録は、対象デバイスの次のアクティベーション時に行われます。デバイスが既にアクティベーション済みの場合には、一度ワイプが必要です。
{: .notice--info}

## トークンの更新を忘れずに！

ABMからダウンロードするMDMサーバのトークンには１年の有効期限が設定されており、毎年ABMから新しいトークンをダウンロードしてMobileIron Cloudにアップロードする更新作業が必要です。（初めにMobileIron CloudからダウンロードしてABMにアップロードしたキーについては更新の必要はありません。）  
トークンの更新は、ABMの［設定］＞ 該当のMDMサーバから「トークンをダウンロード」し、MobileIron Cloudに「新規トークンをアップロード」するだけです。  
![](/assets/technotes/apple-business-manager/E9BA523F-A080-481E-B884-AB8FCCEC0808.png)
