---
title: "iOS標準アプリにOffice 365を設定する"
permalink: /cloud-quickstart-guide/ios-o365-apple-apps/
---
iOS標準のメール・カレンダー・連絡先アプリを使って、Microsoft Office 365のExchangeを利用することができます。

MobileIron CloudでiOS向けのExchangeアカウント構成を作成して配布することで、ユーザーは手作業でアカウントを追加する必要が無くなります。またMobileIron Cloudから配布したExchangeアカウントはiOS上で「管理されたアカウント」として扱われるため、個人で追加したGmailなどのアカウントとはデータが分離・保護されます。また管理されたアカウントはそこでダウンロード済みのメールや添付ファイルと共に遠隔で削除することが可能です。

Exchange構成を作成します。MobileIron Cloudの管理画面を開き、［構成］をクリックしてください。  
![](/assets/cloud-quickstart-guide/images/7D663ABB-2746-426E-8495-6AF10F6AA1FC.png)

［+追加］をクリックします。  
![](/assets/cloud-quickstart-guide/images/A7D04069-59C8-4659-A9A6-E07A6E339256.png)

［Exchange］をクリックします。見つけにくいときは上部の「構成を検索」ボックスを使って検索できます。また左側のフィルタを選択することで、特定のOSプラットフォームやバージョンに有効な構成を表示を絞り込むこともできます。  
![](/assets/cloud-quickstart-guide/images/79FF2B10-5A44-4C02-8141-A586A3BB2360.png)

「Exchange構成の作成」画面に切り替わります。「名前」に任意の名前を入力してください。この名前がiOSデバイスでのアカウント名になります。「Exchangeホスト」はOffice 365では常に"outlook.office365.com"になります。  
![](/assets/cloud-quickstart-guide/images/0D9540E8-378F-40F4-9D39-8F944ECF9632.png)

画面をスクロールし、［交換ペイロードにOAuthを有効化］にチェックを入れてください。「ユーザー」には"${userUID}"、「メールアドレス」には"${userEmailAddress}" 属性を設定します。このExchange構成をデバイスに配布する際に、ユーザー毎の属性の値が動的に設定されます。設定を終えたら［次へ］をクリックしてください。  
![](/assets/cloud-quickstart-guide/images/3A55B684-B420-4A3D-A45A-CCAC225C1CE8.png)

**ヒント** ${userUID}はMobileIron CloudのユーザーIDを示します。[ローカルユーザーの作成](/cloud-quickstart-guide/localuser/)でも少し触れましたが、多くの組織がActive Directory上のUPNをPCやOffice 365へのサインインIDとしていますので、MobileIron Cloudのユーザーとしても同じIDを使うのは良いことです。MobileIron CloudのユーザーをAD/AADと同期する場合にはデフォルトでAD/AAD上のユーザーのUPNがMobileIron CloudユーザーのUIDとなります。さらに${userUPN}属性が設定され、この値にもAD/AAD上のUPNが入ります。
{: .notice--info}

配布先のオプションに［すべてのデバイス］を選び、［完了］をクリックしてください。  
![](/assets/cloud-quickstart-guide/images/2142E514-0EDA-4694-A291-B9E73D7060B3.png)

これでExchange構成を追加できました。「構成」画面で一覧を確認できます。  
![](/assets/cloud-quickstart-guide/images/D908ECDB-CB81-4329-B53F-EC5126C176EE.png)

管理画面での作業は以上です。

iOSデバイスがチェックインすると、この構成のOffice 365のアカウントが自動で追加されます。「設定」アプリの「パスワードとアカウント」を開くと確認することができます。  
![](/assets/cloud-quickstart-guide/images/3D73741E-7AB3-4925-B087-5E1E3464BF77.png)

Office 365へのサインインIDが配布されましたが、Exchangeと同期するためには認証が必要です。アカウント名（画面では［職場のOffice 365］）をタップして開き、認証を行います。［パスワードを再入力］をタップしてください。  
![](/assets/cloud-quickstart-guide/images/40A09351-A39A-4292-A090-B57760A06DAC.png)

画面の指示に従い、アカウントとパスワードを入力して認証します。  
![](/assets/cloud-quickstart-guide/images/91A9D6DA-DDBD-447E-805F-AB55049B0462.png)

認証が完了し、同期対象や期間の選択ができるようになりました。  
![](/assets/cloud-quickstart-guide/images/E8D8DBDE-69FA-4C22-ACB3-8FC5A99799FB.png)

iOS標準の「メール」アプリを開くと、Office 365のメールボックスが追加されたことが確認できます。  
![](/assets/cloud-quickstart-guide/images/B35B44A3-D61F-4399-9A11-77A54E18288A.png)

iOS標準の「カレンダー」アプリでもOffice 365のカレンダーが追加されたことが確認できます。カレンダーアプリを起動し、画面下部の［カレンダー］をタップします。  
![](/assets/cloud-quickstart-guide/images/02937DD1-8BA6-4EDC-B9C3-C8BBF260A510.png)

カレンダーの一覧で、Office 365のカレンダーを同期していることが確認できます。  
![](/assets/cloud-quickstart-guide/images/07C97904-AD34-44CC-9345-75C9D69349A3.png)

iOS標準の「連絡先」アプリにもExchangeの連絡先が同期されています。同アプリを起動し、画面左上の［グループ］をタップします。  
![](/assets/cloud-quickstart-guide/images/326055EC-6CEA-4FBE-B7D8-74CC153A5CEA.png)

グループの一覧に、企業用の連絡先が追加されたことが確認できます。  
![](/assets/cloud-quickstart-guide/images/229B57A3-ABA1-4059-8C45-62DFA9856EA5.png)

これでiOS標準のメール・カレンダー・連絡先アプリでOffice 365のExchangeを利用するための設定は完了です。
