---
title: "Mobile@Workを準備する"
permalink: /technotes/macos-quickstart/
sidebar:
    nav: "macos-quickstart"
---

macOSの管理では、Apple MDMの仕組みに加えて、MobileIronのクライアントアプリである「Mobile@Work」も利用しますので、デバイスを登録する前にMobile@Workを準備しておきます。

## Mobile@Workのアプリカタログへの登録

アプリカタログの［＋追加］ボタンをクリックします。  
![](/assets/technotes/macos-quickstart/4DF286DA-A7A0-44D2-9BE1-601797AECA0F.png)

画面を下にスクロールすると、Mobile@Work (macOS) が簡単に取り込めるようにボタンになっていますので、これをクリックします。  
![](/assets/technotes/macos-quickstart/8340F80A-FC6A-417F-8044-D14FAD09E0C9.png)

このアプリについての説明、スクリーンショット、委譲の設定は、特に変更する必要が無ければそのまま［次へ］をクリックして進めていきます。  
![](/assets/technotes/macos-quickstart/a4ef9ea5-3d75-47b9-b350-853027a31102.png)

配布先の設定では「全員」を選択します。  
![](/assets/technotes/macos-quickstart/928CD39E-DF4D-4151-B434-66DE60D6F2A7.png)

アプリ構成では、念のため自動的に作成された「デバイスにインストール」の設定を確認しておきます。  
![](/assets/technotes/macos-quickstart/8F0BC721-25DA-49F9-BE66-C51C85B8FD66.png)

「デバイスにインストール」がONになっていることを確認してください。  
![](/assets/technotes/macos-quickstart/ee7eac97-ee27-46aa-a2b6-82093c711a62.png)  
［次へ］でアプリ構成の画面に戻り、［完了］をクリックします。

以上でアプリカタログにmacOS版Mobile@Workが登録できました。  
![](/assets/technotes/macos-quickstart/cc40c471-9260-403c-b092-0f66e03c4de2.png)


## Mobile@Workアプリの構成

macOS版Mobile@Workアプリにはいくつかの変更可能な設定項目があり、「macOS対応Mobile@Work」の構成で設定します。デフォルト設定の構成がすべてのデバイスに割り当てられており、通常は変更する必要はありません。  
![](/assets/technotes/macos-quickstart/52528796-1b49-4887-9847-bfa938564e48.png)


## Mobile@Workアプリのサイレント登録

この後のデバイス登録をSafariを使って行った場合に、Mobile@Workへのログインがシームレスに完了できるように、サイレント登録の設定をしておきます。

MobileIron管理画面にて［管理］>［Apple］>［設定］を選択します。  
![](/assets/technotes/macos-quickstart/37d3b9c5-f12c-49a2-977a-396610bb41fc.png)

「サイレント登録を有効化」をONに設定し、［保存］をクリックします。  
![](/assets/technotes/macos-quickstart/d77c4bfd-bcb3-42b6-aa43-08ec858b8f7b.png)

ここまでで、Mobile@Workの設定が完了しました。

