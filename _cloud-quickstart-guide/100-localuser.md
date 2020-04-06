---
title: "ローカルユーザーを作成する"
permalink: /cloud-quickstart-guide/localuser/
---

MobileIron Cloudでは、デバイスの登録は必ずユーザーと紐付けて行います。ユーザーは、ローカルユーザーとして作成するか、以下の種類の外部ディレクトリと同期して読み込むことができます。
- Active Directory または LDAPサーバ
- Azure Active Directory

本ガイドではローカルユーザーを作成して利用します。

［ユーザー］>［+追加］> ［ユーザー1人］  
![](/assets/cloud-quickstart-guide/images/031ECBE3-EFF2-4253-BBFD-5B6E75768E26.png)
複数のユーザーをまとめて作成、またはCSVで読み込むこともできますが、ここでは1人ずつ作成します。

MobileIron Cloudのユーザー名はEメールアドレスの形式である必要があります（Eメールアドレスと同じである必要はありません）。また全てのリージョンの全てのMobileIron Cloudテナントでユニークである必要があります。Eメールアドレスも必須ですが、ユニークである必要は無く、同じテナント内の複数のユーザーが同じEメールアドレスでも構いません。

**ヒント** Active DirectoryやAzure ADとの統合、あるいはOffice 365の利用を考えている場合、MobileIron Cloudのユーザー名はAD/AAD上のUPNと同じにしておくと良いです。MobileIron CloudのユーザーをAD/AADと同期する場合には、デフォルトでAD/AAD上のユーザーのUPNがMobileIron CloudユーザーのUIDとなります。
{: .notice--info}

設定例：
![](/assets/cloud-quickstart-guide/images/0CC1C066-653B-467C-A11A-E34CBA0B7C53.png)
ユーザーの作成画面からユーザーグループの作成や割り当てを行うこともできますが、本ガイドではユーザーグループについて次項で別途設定します。

「今すぐ招待状を送信」にチェックを入れると、作成したユーザーにデバイス登録を促すEメールが送信されます。招待状を送信しなくてもデバイスは登録できます。  
![](/assets/cloud-quickstart-guide/images/DBAA51A0-75AB-49B4-A5B6-852C06ED8D44.png)

ローカルユーザーが作成されました。  
![](/assets/cloud-quickstart-guide/images/83752F1B-5BFC-4F15-937F-4AF40E37EFAC.png)

招待状を送信した場合、ユーザーには以下のようなEメールが届きます。  
![](/assets/cloud-quickstart-guide/images/77DE9317-61B9-4525-9D8F-43916F4E01DE.png)
