---
title: "Apple MDMを有効にする"
permalink: /cloud-quickstart-guide/applemdmcert/
---

iOS (iPadOS) /macOS デバイスの管理は、Appleが定めるApple MDMのしくみに従って行います。Apple MDMでは、MobileIron CloudからiOSデバイスを呼び出すためにAPNS（Apple Push Notification Service）を利用しますが、MobileIron CloudがAPNSへ接続するために、Appleから発行されたMDM証明書をインストールする必要があります。MDM証明書はAppleから無償で発行されます。また1年毎に更新する必要があります。

MDM証明書の発行を受けるためにApple IDが必要ですので https://appleid.apple.com/ で予め作成して下さい。Apple IDの準備ができたら次の作業に進みます。

**重要** このときApple IDとなるメールアドレスには、グループアドレス（エイリアス）の利用を強くお勧めします。MDM証明書は毎年同じApple IDによって更新する必要があり、MobileIron Cloud管理者の異動や退職によって同じApple IDが使えない状況に陥ることを防ぐためです。MDM証明書の更新時に同じApple IDが利用できない場合、MobileIron Cloudに登録されている全てのiOSデバイスのコントロールを失い、再登録が必要になります。またデバイスに保存されたデータも失う可能性があります。
{: .notice--danger}

管理 > Appleの設定 > MDM証明書
![](/assets/cloud-quickstart-guide/images/14B96DC2-2A1F-40A1-B1C7-6F65DD76AD2D.png)

最初に「ファイルをダウンロード」をクリックします。MobileIron CloudがAppleの認証局へのMDM証明書発行要求を生成し、手元のPCにダウンロードされます。
![](/assets/cloud-quickstart-guide/images/7B4D0199-3D00-4325-B6E6-B5D9B0C2F999.png)
ファイルをローカルPCに保存したら、「Certificateを取得」をクリックします。

これからApple Push Certificates Portalを開き、MDM証明書の発行をリクエストしますが、利用するApple IDを次の画面で入力しておきます。この項目は任意ですが、1年後にMDM証明書をどのApple IDで行えば良いかを確実に残しておく必要があるため、とても重要です。
![](/assets/cloud-quickstart-guide/images/91A5BB2F-8407-44E4-B779-297266A14602.png)
「Apple Push Certificates Portalを開く」ボタンをクリックします。

準備しておいた組織のApple IDでサインインします。
![](/assets/cloud-quickstart-guide/images/3EBFE5BA-09A5-4EB2-9368-1601701914E8.png)

Apple Push Certificates Portalにサインインできました。Create Certificate ボタンをクリックします。
![](/assets/cloud-quickstart-guide/images/E2B0620D-14DF-41B0-A1FC-56C5DDC4EC0B.png)

Terms of Useに同意します。
![](/assets/cloud-quickstart-guide/images/AFDEA3E2-174D-4CAF-8C45-6ECBDF8F829A.png)

MobileIron CloudからダウンロードしたMDM証明書発行要求のファイルをアップロードします。またNotesにはどのMDMサーバのためのMDM証明書かが分かるようなメモを入れておくと良いでしょう。
![](/assets/cloud-quickstart-guide/images/6920EF71-2965-4AE5-8DF1-E9B6319C1736.png)

証明書が発行されたら、Downloadボタンをクリックし、ファイルをローカルPCに保存します。
![](/assets/cloud-quickstart-guide/images/EFE031AE-EDB9-4550-9672-45DB6969F662.png)

MobileIron Cloudの管理コンソールに戻り、「証明書をアップロード」ボタンをクリックします。
![](/assets/cloud-quickstart-guide/images/FAFA1A17-2A14-488A-A237-88A154837361.png)
Apple Push Certificates Portalからダウンロードした証明書ファイルを選択しアップロードすれば完了です。

Apple Push Certificates Portalに行く前にApple IDを入力しておいた場合、この画面に残ります。
![](/assets/cloud-quickstart-guide/images/BC2557B3-8322-4713-920C-3676F7AE3415.png)
