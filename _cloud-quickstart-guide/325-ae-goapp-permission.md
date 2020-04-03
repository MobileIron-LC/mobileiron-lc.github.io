---
title: "MobileIron Goアプリの権限承認設定"
permalink: /cloud-quickstart-guide/ae-goapp-permission/
---

Android Enterpriseを有効に設定して以来、次のような通知が出るようになったことに気づかれたかもしれません。
![](/assets/cloud-quickstart-guide/images/F07A057F-8584-4AED-8BFF-1E94F2C67526.png)

MobileIron GoアプリはデフォルトではApp Catalogに表示されていませんが、暗黙的にManaged Google Playにインポートされており、管理者による権限の承認が必要なため、このような通知が表示されます。この画面から「許可を承認」としても良いのですが、今後も同様の作業を行う必要を無くすために、新しい権限が自動的に承認されるように変更します。

アプリ > アプリカタログ > Google Playを選択し、MobileIron Goを検索
![](/assets/cloud-quickstart-guide/images/FDA47D4A-1024-4C51-98CB-FCCE34211923.png)

承認ボタンをクリック。
![](/assets/cloud-quickstart-guide/images/4E5C04BA-CBE4-47BD-A3D1-826955D34B3A.png)

承認ボタンをクリック。
![](/assets/cloud-quickstart-guide/images/F7EEDA93-8881-4AFB-8E16-96A410A81C49.png)

「このアプリから新しい権限をリクエストされたときにアプリの承認を維持します」を選択。完了をクリック。
![](/assets/cloud-quickstart-guide/images/F55DADFC-201C-41D6-9B2D-B2521B6D6E9C.png)
この時点でManaged Google PlayにはMobileIron Goアプリの権限承認設定が反映されています。

ここで「次へ」をクリックするとApp CatalogにMobileIron Goが表示されるようになりますが、その必要は無いので「取り消し」をクリックします。
![](/assets/cloud-quickstart-guide/images/1667D943-BB16-4F14-9B9D-E727CE889E1B.png)

![](/assets/cloud-quickstart-guide/images/6C9BE6F8-3AFA-40CC-8424-8305F65C1BB8.png)

以上で完了です。
