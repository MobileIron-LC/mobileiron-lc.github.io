---
title: "iOS標準アプリにG Suiteを設定する"
permalink: /cloud-quickstart-guide/ios-gsuite-apple-apps/
---
iOS標準のメール・カレンダー・連絡先アプリを使って、G Suiteを利用することができます。

MobileIron CloudでiOS向けのGoogleアカウント構成を作成して配布することで、ユーザーは手作業でアカウントを追加する必要が無くなります。またMobileIron Cloudから配布したGoogleアカウントはiOS上で「管理されたアカウント」として扱われるため、個人で追加したGmailなどのアカウントとはデータが分離・保護されます。また管理されたアカウントはそこでダウンロード済みのメールや添付ファイルと共に遠隔で削除することが可能です。

Googleアカウント構成を作成します。MobileIron Cloudの管理画面を開き、［構成］> [+追加]から［Googleアカウント］を選択します。見つけにくい場合は上部の検索ボックスを活用して下さい。  
![](/assets/cloud-quickstart-guide/images/B07A54D0-B142-469A-888B-DB67C52EDCD7.png)

「Googleアカウント構成を作成」画面に切り替わります。「名前」に任意の名前を入力してください。［次へ］をクリックしてください。また「アカウントの説明」はメール・カレンダー・連絡先アプリ上のアカウント名として表示されますので、わかりやすい名前を付けておくと良いでしょう。  
![](/assets/cloud-quickstart-guide/images/7740F0B9-061E-4C3E-89FF-B8052E3B3F10.png)

配布先のオプションに［すべてのデバイス］を選び、［完了］をクリックしてください。  
![](/assets/cloud-quickstart-guide/images/11BB3802-BE7C-436E-ADB9-C1AD4D916476.png)

これでGoogleアカウント構成を追加できました。「構成」画面で一覧を確認できます。  
![](/assets/cloud-quickstart-guide/images/0F1ACBD0-4769-4EA4-BCB2-8A9A148022E6.png)

iOSデバイスには、この構成のGoogleアカウントが自動で追加されます。「設定」アプリの「パスワードとアカウント」を開くと確認することができます。下記画面では「職場のG Suite」として追加されています。  
![](/assets/cloud-quickstart-guide/images/57664BE3-8C3E-49A2-A80B-038FBCE71E47.png)

アカウント名をタップして開き、認証を行います。［パスワードを再入力］をタップしてください。  
![](/assets/cloud-quickstart-guide/images/98645FA1-DD42-43CA-9B67-5BA4274494CE.png)

以降は画面の指示に従い、アカウントとパスワードを入力して認証します。以下のダイアログが表示されたら、［続ける］をタップしてください。  
![](/assets/cloud-quickstart-guide/images/3CA82F3D-092B-41A5-AE27-A144ABD306B0.png)

Googleのログイン画面が表示されます。メールアドレスを確認したら、［次へ］をタップしてください。  
![](/assets/cloud-quickstart-guide/images/E5729714-EF8C-4FEF-827D-8555B3D2ADD8.png)

パスワードを入力し、［次へ］をタップしてください。  
![](/assets/cloud-quickstart-guide/images/54BC8CE6-2666-4298-A15E-B6A58A98569C.png)

G Suiteの認証を組織のSAML認証サーバと連携している場合には、認証画面は異なります。
{: .notice--info}

認証が完了すると、「GMAIL」にアカウントが表示されます。これでG Suiteのメールが利用できるようになりました。  
![](/assets/cloud-quickstart-guide/images/792688F7-F167-4205-A8F4-AB0B251C355C.png)

標準のメールアプリを開くと、企業用のG Suiteのメールボックス（下記画面では「職場のG Suite」）が追加されたのを確認できます。  
![](/assets/cloud-quickstart-guide/images/06D9E33C-A43D-4AD9-9D96-78DC470BF4E7.png)

標準のカレンダーアプリでも企業用のG Suiteのカレンダーが追加されます。カレンダーアプリを起動し、画面下部の［カレンダー］をタップすれば確認できます（下記画面では「職場のG Suite」）。  
![](/assets/cloud-quickstart-guide/images/DEACCF8A-1574-4407-BFDD-322D42C4A2E2.png)

標準の連絡先アプリにも追加されます。同アプリを起動し、画面左上の［グループ］をタップすれば確認できます（下記画面では「職場のG Suiteのすべて」）。  
![](/assets/cloud-quickstart-guide/images/33AC7508-4CDB-47AB-AFC8-BF3BCF7C799F.png)

これでiOS標準アプリのメール・カレンダー・連絡先でG Suiteを利用するための設定は完了です。
