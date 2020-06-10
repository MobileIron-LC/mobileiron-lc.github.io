---
title: "Windows10デバイスを登録する"
permalink: /technotes/windows-quickstart/device-registration/
sidebar:
    nav: "windows-quickstart"
---

これからMobileIron Cloudに登録して管理するWindows10デバイスで、スタートメニューの歯車アイコンをクリックし、設定アプリを起動します。  
![](/assets/technotes/windows-quickstart/04EF4856-134F-46F1-8462-236063312817.jpg)

［アカウント］＞［職場または学校にアクセスする］を開き、［デバイス管理のみに登録する］で登録を開始します。  
![](/assets/technotes/windows-quickstart/E70C9D7E-FDEE-4896-AC46-3B8F53792EB4.png)

アカウント情報の欄にMobileIron CloudのユーザーIDを入力し、［次へ］をクリックします。  
![](/assets/technotes/windows-quickstart/9fb605fe-8553-4c07-a77e-ef279e46a736.png)

自動エンロールメントの設定がAzure AD（Premium必須）にされていない環境では、自動検出に失敗して以下の画面になります。

MDMサーバURLの項目に「login.mobileiron.com」と入力し、［次へ］をクリックします。  
![](/assets/technotes/windows-quickstart/D2AD95B3-B8DF-41DF-AFBE-AFADDA77EB08.png)

MobileIron Cloudへのログイン画面が表示されますので、パスワードを入力し、［サインイン］をクリックします。  
![](/assets/technotes/windows-quickstart/27932174-857F-4401-8ABA-4869B5FE43B5.png)

サインインに成功すると、「デバイスをセットアップしています」と表示されますので、［OK］をクリックします。  
![](/assets/technotes/windows-quickstart/8f107e90-25c2-4d8e-b98d-33eda22547e3.png)

登録が成功すると、「職場、または学校にアクセスする」にMDMに接続済みの表示がされます。  
ここまでで、登録作業は完了です。  

MobileIron Cloudの管理画面で、登録したデバイスを見つけることができます。  
![](/assets/technotes/windows-quickstart/E3607B70-2050-46DD-82F1-828269AEE9E8.png)

Windows10 MDMでは、MobileIron Cloudからの要求によるチェックインの他に、デバイス側から手動でチェックインさせることができます。「〜MDMに接続済み」と表示されているカバンマークの辺りをクリックすると、［情報］と［切断］のボタンが表示されるので、［情報］をクリックします。  
![](/assets/technotes/windows-quickstart/9ba53152-e963-4d1d-9969-7a2a9b631142.png)

「デバイスの同期状態」の最後に［同期］ボタンがあるのでクリックします。  
![](/assets/technotes/windows-quickstart/2EDAD8E3-242A-4B94-9E49-7ED2ECB0833D.png)  
「前回試行した同期」の日時が更新され、「正しく同期されました」と表示されれば同期成功です。

Windows10デバイスの登録は以上です。