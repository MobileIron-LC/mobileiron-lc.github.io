---
title: "Microsoft OutlookアプリにOffice 365を設定する"
permalink: /cloud-quickstart-guide/ios-o365-ms-outlook/
---
Office 365をMicrosoft Outlookアプリで使えるようにする設定を解説します。OutlookアプリをMobileIron Cloudから管理アプリとして配布し、さらにアカウント設定も配布できます。

MobileIron Cloudの［アプリ］→［アプリカタログ］を開きます。  
![](/assets/cloud-quickstart-guide/images/00028D14-1562-471A-9367-BE95FD3BFEFB.png)

［+追加］をクリックします。  
![](/assets/cloud-quickstart-guide/images/890D3E11-65EA-4911-A198-2CFF112D3DB4.png)

［Microsoft Outlook］アプリを検索します。選択したら［次へ］をクリックします。  
![](/assets/cloud-quickstart-guide/images/9233BA99-1C7F-4866-83DD-4BEE1A988A96.png)

「アプリ情報」画面に切り替わります。そのまま［次へ］をクリックしてください。  
![](/assets/cloud-quickstart-guide/images/C79AA7C6-BF86-4FF1-BB45-6F96E6534789.png)

「アプリ委譲」画面に切り替わります。そのまま［次へ］をクリックしてください。  
![](/assets/cloud-quickstart-guide/images/588023F1-A803-418B-96D9-91B4E84A8882.png)

アプリ配布の画面に切り替わります。［全員］を選び、［追加］をクリックします。  
![](/assets/cloud-quickstart-guide/images/C5AFADCC-4940-457B-834D-0AD29747E37D.png)

「アプリ構成」画面に切り替わります。ここで「iOSマネージドアプリの構成」を追加します。同項目の右側にある［+］をクリックしてください。  
![](/assets/cloud-quickstart-guide/images/974F6E13-BC94-44BA-B32F-115431EAD364.png)

「構成設定」画面に切り替わります。「名前」のボックスに任意の名前を入力します。続けて、「Account settings」セクションにある「Account type」のドロップダウンから、［Office 365 or Hybrid（Modern Authentication）］を選んでください。またUser Logon Nameに"${userUID}"を設定します。  
![](/assets/cloud-quickstart-guide/images/9DEC8A03-1E7B-4FDD-88E9-3A40708FF3E4.png)

画面をスクロールし、「Account restrictions」セクションにある「Allowed accounts only」のドロップダウンから、［Enabled］を選んでください。またUPNにも"${userUID}"を設定します。［次へ］をクリックしてください。  
![](/assets/cloud-quickstart-guide/images/F66F1A76-9BF5-42B2-998E-25C3C8876FFE.png)

「アプリ構成」画面に戻ります。「iOSマネージドアプリの構成」に追加した構成が表示されていることを確認したら、［完了］をクリックしてください。  
![](/assets/cloud-quickstart-guide/images/D682C0E7-4FB4-42BC-8B00-EF8FFBCF8B2D.png)

「アプリカタログ」画面に戻ります。Outlookが追加されたことが確認できます。  
![](/assets/cloud-quickstart-guide/images/2A1050A8-5621-45EA-894B-37DCCF7052B5.png)

これで管理画面での作業は完了です。

次に、iOSデバイスでOutlookをインストールしましょう。「App Catalog」を開いてください。「新規リリース」に「Microsoft Outlook」が追加されているので、［インストール］をタップします。  
![](/assets/cloud-quickstart-guide/images/0CF0F02B-CD16-4757-891E-9AD447E5E277.png)

確認ダイアログが表示されるので、［インストール］をタップしてください。すると、インストールが始まります。  
![](/assets/cloud-quickstart-guide/images/7B3FB086-A307-4460-8D9E-8BD63E97B4ED.png)

インストールが終わるとOutlookアプリのアイコンがホーム画面に表示されます。アイコンをタップします。  
![](/assets/cloud-quickstart-guide/images/AE717FFC-C4B2-4276-9BF6-8E4462E8E0A9.png)

Outlookアプリが起動すると、Office 365のアカウントが自動で設定されており、「１個のアカウントが見つかりました」と表示されます。［職場のアカウントの追加］をタップしてください。  
![](/assets/cloud-quickstart-guide/images/1C6EF8D2-A714-4A7B-945F-9FC7B7A7C1D1.png)

Office 365のパスワードが求められるので、入力して［サインイン］をタップします。もし、「詳細情報が必要」という画面が表示されたら［次へ］をタップし、画面の指示に従って「追加のセキュリティ」を設定してください。  
![](/assets/cloud-quickstart-guide/images/52757D80-C94D-4269-A940-0776562F15CE.png)

これでOffice 365のメールがOutlookアプリで使えるようになりました。  
![](/assets/cloud-quickstart-guide/images/26311DA8-F2E2-42D7-AE94-E1DD3B0EC052.png)

MobileIron Cloudから配布した「Allowed accounts only」の設定に従って、Outlookアプリ内でのアカウント追加が禁止されています。実際に禁止されるか試してみましょう。Outlookアプリのサイドメニューから「設定」画面を開き、［職場のメールアドレスの追加］をタップしてください。  
![](/assets/cloud-quickstart-guide/images/E38A1B3F-E241-42FD-8E51-CE2108D27B16.png)

続けて、［メールアカウントの追加］をタップしてください。  
![](/assets/cloud-quickstart-guide/images/8CB43206-7700-418A-AFCE-0398A6D72CDC.png)

すると、「アカウントを追加できません」というメッセージが表示されます。［OK］をタップして、メッセージを閉じてください。  
![](/assets/cloud-quickstart-guide/images/D4BA9D25-B4DF-417B-A02E-3439E9C0480A.png)

これで、Outlookアプリ内でアカウントを追加できないことが確認できました。
