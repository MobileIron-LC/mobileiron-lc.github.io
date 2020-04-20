---
title: "Microsoft OutlookアプリにOffice 365を設定する"
permalink: /cloud-quickstart-guide/ae-o365-ms-outlook/
---
Office 365をOutlookアプリで使うための設定をしていきます。

［アプリ］＞［アプリカタログ］を開き、Google PlayからMicrosoft Outlookを取り込みます。  
![](/assets/cloud-quickstart-guide/images/5F7E5B5D-0CED-49C0-B90E-CD37E6AE8484.png)

アプリが要求する権限を承認します。  
![](/assets/cloud-quickstart-guide/images/ECE41549-B6D7-46BF-98CE-A514BAB0834F.png)

![](/assets/cloud-quickstart-guide/images/CE6553EE-D82F-45D1-86B2-F9EDB93B8257.png)

![](/assets/cloud-quickstart-guide/images/593EB026-AA47-4F1F-8384-FCD3B4DA88AC.png)

右下の［次へ］をクリックして設定を進めます。  
![](/assets/cloud-quickstart-guide/images/0BC48167-1F82-49B7-A994-B141D9B07C44.png)

アプリカタログ上でのカテゴリを設定します。デフォルトではGoogle Play上のカテゴリが選択されています。  
![](/assets/cloud-quickstart-guide/images/892D31F4-96F0-4D20-A6B3-16709B990611.png)

［次へ］をクリックします。  
![](/assets/cloud-quickstart-guide/images/56F5A3F5-848E-42B1-9B7C-F7FD160E4630.png)

このアプリの配布対象を指定します。デフォルトでは全てのユーザーのAndroidデバイスに配布されます。  
![](/assets/cloud-quickstart-guide/images/69950650-BB14-4AE3-B21D-73E8061D5DE8.png)

Outlookアプリにはアカウント設定などを配布することができます。「Android用マネージド構成」を［ ＋ ］ボタンで追加します。  
![](/assets/cloud-quickstart-guide/images/2B46EA03-A6D2-4DAF-9761-E0005ECA2806.png)

Office 365に接続するためには、マネージド構成を次のように設定して下さい。（Office 365のユーザーIDとMobileIron CloudのユーザーIDが同じである場合）

| 構成名 | 値 |
|---|---|
| email address | ${userEmailAddress} |
| username | ${userUID} |
| 許可されたアカウント | ${userUID} |
| account type | ModernAuth |

![](/assets/cloud-quickstart-guide/images/BD401C94-5C67-4861-A05A-60C0D185A757.png)

{% capture notice-text %}
Outlookアプリがサポートしているマネージド構成項目についての詳細は[Microsoftのドキュメント](
https://docs.microsoft.com/ja-jp/exchange/clients-and-mobile-in-exchange-online/outlook-for-ios-and-android/outlook-for-ios-and-android-configuration-with-microsoft-intune){: target="_blank"}を参照して下さい。
なおMicrosoftのドキュメントで記載されているKeyと、MobileIron CloudのUI上の項目名は以下のように対応しています。

| **マネージド構成の設定画面に表示される項目名**<br />対応するOutlookアプリの設定Key | 適合環境 |
|---|---|
| **email address**<br />com.microsoft.outlook.EmailProfile.EmailAddress | Office 365<br />Exchange Server |
| **description for account**<br />com.microsoft.outlook.EmailProfile.EmailAccountName | Exchange Server |
| **exchange server url**<br />com.microsoft.outlook.EmailProfile.ServerHostName | Exchange Server |
| **domain of user account**<br />com.microsoft.outlook.EmailProfile.AccountDomain | Exchange Server |
| **username**<br />com.microsoft.outlook.EmailProfile.EmailUPN | Office 365<br />Exchange Server |
| **server authentication method**<br />com.microsoft.outlook.EmailProfile.ServerAuthentication | Exchange Server |
| **許可されたアカウント**<br />com.microsoft.intune.mam.AllowedAccountUPNs | Office 365 |
| **account type**<br />com.microsoft.outlook.EmailProfile.AccountType | Office 365<br />Exchange Server |
{% endcapture %}

<div class="notice">
  {{ notice-text | markdownify }}
</div>

Android用マネージド構成が登録できました。［完了］ボタンをクリックします。  
![](/assets/cloud-quickstart-guide/images/4281827A-D71B-47C4-B1B5-66867ED92A81.png)

以上でMicrosoft Outlookアプリのアプリカタログへの取り込みと設定は完了です。

デバイスで仕事のPlayを開いて、Microsoft Outlookをインストールします。  
![](/assets/cloud-quickstart-guide/images/2EBAA4E8-B835-4557-BF57-0868A80F8CEB.png)

**Tips** 新たに追加したアプリが、デバイスの仕事のPlayに表示されるようになるまで、数分から１時間程度かかる場合があります。仕事のPlayアプリへの表示の反映が未だの場合でも、アプリ構成の「デバイスにインストール」の設定を有効にしておけば、MobileIron Cloudサーバ側からアプリのインストール命令は動作しますので、テストのためにアプリをすぐにインストールできます。
{: .notice--info}

Outlookアプリがデバイスの仕事領域にインストールされました。  
![](/assets/cloud-quickstart-guide/images/DAF1E119-104F-49C3-8604-6D5BEB3E2786.png)

Outlookアプリを開き、Office 365にサインインしていきます。  
![](/assets/cloud-quickstart-guide/images/28E30497-11B5-41CF-9207-F73AAF9FF9D5.png)

アプリと一緒にアカウント構成も配布する設定も行いましたので、職場のアカウントが自動的に見つかります。そのまま［アカウントを追加］ボタンをタップします。  
![](/assets/cloud-quickstart-guide/images/97884B81-D506-437E-90B9-7E47052D0E79.png)

アカウントにサインインします。※認証方法や画面はお客様の環境により異なる場合があります。  
![](/assets/cloud-quickstart-guide/images/ECD0E610-5BB6-4C3C-B5B3-47036324E00F.png)

サインインに成功し、Office 365のメールが使えるようになりました。  
![](/assets/cloud-quickstart-guide/images/CBFDE612-008F-4790-A958-F63D172A808A.png)

ユーザーが個人のアカウントをOutlookアプリに追加できないように「許可されたアカウント」の設定をしておきました。動作を確認してみましょう。Outlookアプリのメニューから設定画面に進みます。  
![](/assets/cloud-quickstart-guide/images/0FCC303F-8BDB-49AE-80A9-9F2F601D4A47.png)

現在サインインしているOffice 365のアカウントが表示されています。［ ＋ 職場アカウントの追加 ］ボタンを押して、新しいメールアカウントの追加を試します。  
![](/assets/cloud-quickstart-guide/images/118C9BF2-1836-4DBA-8266-6861EADDD3DC.png)

![](/assets/cloud-quickstart-guide/images/BE9F1CFA-AFBF-4F40-9C26-EF1441092A94.png)

アプリの設定によりブロックされることが確認できました。  
![](/assets/cloud-quickstart-guide/images/6FE06B59-E28A-40B4-ADDF-605EF569D1EF.png)

以上でMicrosoft Outlookアプリを使ってOffice 365に接続ための設定は完了です。
