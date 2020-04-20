---
title: "GoogleのアプリでG Suiteを利用する"
permalink: /cloud-quickstart-guide/ae-gsuite-google-gmail/
---
Android Enteriseは、G Suiteととても相性の良いプラットフォームです。仕事用プロファイルにGoogleアカウント構成を配布するだけで、Googleのアプリで認識してくれます。

## Googleアカウント構成を配布する

［構成］画面で［＋ 追加］ボタンを押して「Googleアカウント」構成を追加します。  
※この構成はiOSとAndroid Enterpriseで共通です。iOS標準Mailアプリ向けのGoogleアカウント構成を作成している場合は、作成済みの構成をAndroid Enterpriseデバイスにも適用するだけで済みます。  
![](/assets/cloud-quickstart-guide/images/6BDEF438-4F6D-4990-95D0-2FEAC9A84C5E.png)

Googleアカウント構成を設定します。  
![](/assets/cloud-quickstart-guide/images/9C846032-B907-437F-81DC-511A09188263.png)

構成の割り当て先を選択し［完了］をクリックします。Googleアカウント構成はiOSとAndroid Enterpriseで共通ですので、「すべてのデバイス」に割り当てていれば両方のデバイスに配布されます。  
![](/assets/cloud-quickstart-guide/images/68C67036-91BC-446E-9CAA-14D9231254BB.png)

以上でMobileIron Cloud側の設定は完了です。

デバイスがチェックインするとMobileIron GoがポップアップしてGoogleアカウントの設定が始まります。  
![](/assets/cloud-quickstart-guide/images/36421601-373B-4D2B-8F7C-F760C378FD92.png)

![](/assets/cloud-quickstart-guide/images/B0A995D3-F3E3-49E4-8E4C-55ACC970327C.png)

![](/assets/cloud-quickstart-guide/images/7448A120-A3EA-4D71-995C-C61B55DE7F5B.png)  
認証方法や画面はお客様のG Suite環境の設定により異なります。

認証が完了すると、Android OSの「アカウント」設定画面で、G SuiteのGoogleアカウントが登録されたことが確認できます。  
![](/assets/cloud-quickstart-guide/images/F0C95198-1EE4-4D36-9420-C83109438546.png)

## 仕事のPlayでのアカウント切替に注意

ここで一点重要な注意があります。仕事のPlayを開くと追加したG SuiteのGoogleアカウントに切り替えが可能になっており、切り替えた場合には公開のPlayストアにある任意のアプリが仕事のアプリとしてダウンロードできてしまいます。  
![](/assets/cloud-quickstart-guide/images/F5D41715-7F05-4EE8-8945-9A7EA2277933.png)

![](/assets/cloud-quickstart-guide/images/2AA164AC-05B8-4BDA-96B3-98F7ABE75DD3.png)

これを防ぐためには、G Suiteの管理コンソールにログインし、［アプリ］＞［その他の Google サービス］から「Google Play」を「オフ」に設定します。  
![](/assets/cloud-quickstart-guide/images/555A338A-6CC8-44E5-B43B-5DAFCC91EB15.png)

しばらくすると、デバイスの仕事のPlayでG SuiteのGoogleアカウントを選択してもアプリが表示されなくなります。  
![](/assets/cloud-quickstart-guide/images/068B5566-4028-4441-A7C8-9DC7B5C9E6BB.png)



## Googleのアプリを仕事領域にインストールする

Googleの「Gmail、カレンダー、連絡帳」アプリをインポートし、配布します。以下は追加後の［アプリ］画面です。  
![](/assets/cloud-quickstart-guide/images/671F6754-086D-4620-ACAF-380C513CDB69.png)

なおGmailアプリには「マネージド構成」でアカウント設定の項目が定義されていますが、これはGmailアプリを使ってExchange等のメールサーバに接続せるための設定ですので使用しません。G Suiteのアカウントはアプリのマネージド構成ではなく、「Googleアカウント構成」によって既に配布済みです。

以上でMobileIron Cloud側の設定は完了です。

デバイスの仕事のPlayから「Gmail、カレンダー、連絡帳」アプリをインストールします。  
![](/assets/cloud-quickstart-guide/images/0910D1F1-1106-474C-90AC-5EF1FD06E46F.png)

Gmailアプリを開いてみましょう。G SuiteのGoogleアカウントが見つかります。［GMAILに移動］をタップします。
※「アカウントの変更禁止」のロックダウン構成が適用されていれば、［＋他のメールアドレスを追加］はブロックされます。  
![](/assets/cloud-quickstart-guide/images/E85E1EF7-8D50-424A-BC50-500A38A4DEAA.png)

このGoogleアカウントは既に認証が完了していますので、すぐにメールにアクセスすることができます。  
![](/assets/cloud-quickstart-guide/images/52E98BB8-C3FD-45AD-BCC4-01E1D0C026F7.png)

同様にGoogleの「カレンダー」アプリや「連絡帳」アプリも、開けばすぐに使える状態になっています。
