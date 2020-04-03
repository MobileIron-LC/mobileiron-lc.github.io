---
title: "MDMアクション（ワイプ / 撤去）"
permalink: /cloud-quickstart-guide/ios-mdm-wipe-retire/
---
## ワイプ

MobileIron Cloudからワイプを実行すると、iOSデバイスが遠隔で完全に初期化されます。ワイプを実行するには、目的のデバイスの「詳細」画面を開き、［ロック］などのアイコンの右側にあるアクションメニュー（縦並びの３つのドット）から [ワイプ] を選択します。  
![](/assets/cloud-quickstart-guide/images/03718144-25C9-4FA7-B8B7-624BC5FEDE79.png)

確認のダイアログが表示されます。［ワイプを元に戻せないことを理解します］をオンにして、［ワイプ］をクリックしてください。  
![](/assets/cloud-quickstart-guide/images/95CF7743-582E-4EB2-A1E9-2E91B278A797.png)

これでワイプが実行されました。デバイス側では、ワイプ中の画面（黒い背景画面に白いApple社ロゴが表示される画面）に切り替わり、プログレスバーで進捗が表示されます。ワイプが終わると、言語の選択をはじめ初期設定を行う状態になります。

## 撤去

撤去とは、デバイスをMobileIron Cloudによる管理から外す動作のことです。撤去の場合、MobileIron Cloudから配布した仕事のメールアカウントやWi-Fiなど全ての設定と、アプリが削除されます（アプリについては登録解除時に削除する設定でインストールした場合）。個人のアプリとその保存データ、写真などは削除されずに残ります。

撤去を実行するには、目的のデバイスの「詳細」画面を開き、アクションの詳細メニューから［撤去］をクリックします。  
![](/assets/cloud-quickstart-guide/images/DB3C7D32-7175-4719-8B4A-E6BBB015AF7F.png)

確認のダイアログが表示されます。［撤去を元に戻せないことを理解します］をオンにして、［撤去］をクリックしてください。  
![](/assets/cloud-quickstart-guide/images/8F1A58D9-3410-4958-BE4B-38E9959E9CA4.png)

これで撤去が実行されました。「詳細」画面上部の「ステータス」に「撤去済み」と表示されます。撤去してもデバイスリストに情報自体は残ります。もし、デバイスリストから削除したければ、［デバイスを削除］をクリックしてください。  
![](/assets/cloud-quickstart-guide/images/7A6A20DE-0795-4722-9073-85062344A332.png)

次に撤去時のデバイス側の挙動を見ていきます。

以下は今回の例とするデバイスの撤去前の状態です。このデバイスにはGmail, Salesforce, Outlookの３つのアプリが、管理されたアプリとしてインストールされています。アプリカタログでの設定により、Gmailアプリだけ「登録解除時にアプリを削除」が有効になった状態でインストールされました。またMobileIron Goアプリを使ってデバイス登録を行なっており、MobileIron Go自身は管理されたアプリではありません。App CatalogはアプリではなくSafariへのWebクリップです。  
![](/assets/cloud-quickstart-guide/images/8BA0FE48-C933-4833-8C5E-D85EAFBC9D0B.PNG)

管理されたアカウントとしてOffice 365（画面の「職場のOffice 365）がMobleIron Cloudから配布されています。iCloudとOutlook.com（画面の「個人のOutlook」）のアカウントがユーザーによって追加されています。
![](/assets/cloud-quickstart-guide/images/3D73741E-7AB3-4925-B087-5E1E3464BF77.png)

管理画面から撤去を実行しました。

「登録解除時にアプリを削除」が有効になっている場合、デバイス側では管理された仕事のアプリとデータが自動で削除されます。ここではGmailアプリのみ削除が有効になっているので、自動で削除されました。また管理されたWebクリップであるApp Catalogも自動で削除されました。「登録解除時にアプリを削除」を有効にしていなかったSalesforceとOutlookは、管理されていないアプリとなって引き続き残っています。MobileIron Goは元々管理されていないアプリの状態でしたので画面に残っていますが、MobileIron Cloudへの接続は解除された状態です。  
![](/assets/cloud-quickstart-guide/images/00E1FB64-FBCC-4CBB-956E-C6E1299DECE7.png)

「設定」アプリを開くと、「職場のOffice 365」アカウントが削除されたことが確認できます。またデバイス登録時にインストールされたその他のプロファイルも全て削除されます。  
![](/assets/cloud-quickstart-guide/images/5F4B16F2-A3B2-4CEC-83DD-239307CC6FB5.png)

MDMアクションの撤去を実行する方法は以上です。
