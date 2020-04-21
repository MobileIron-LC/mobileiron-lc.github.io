---
title: "プロファイル間の共有の禁止動作"
permalink: /cloud-quickstart-guide/ae-sharing-restriction-experience/
---
機能制限（ロックダウン）で設定したとおり、仕事のアプリから個人のアプリへのファイルの共有やコピー＆ペーストができないことを確認しましょう。

## プロファイル間のファイル共有の禁止動作

ここではPDFファイルを使ってテストします。まだ仕事領域にPDFを閲覧するためのアプリがありませんので、「Google PDF Viewer」（com.google.android.apps.pdfviewer）をアプリカタログに追加し、仕事のアプリとして配布しておきます。※Google PDF Viewerはインストールしてもホームスクリーンにアイコンが表示されないアプリです。  
![](/assets/cloud-quickstart-guide/images/67A42C7E-CDD3-4562-BA2D-6C702E16AB99.png)

デバイスの個人領域にも、PDFを開くことのできるアプリをインストールしておきます。個人のGoogle PlayからEvernoteとAdobe Acrobat Readerをインストールしました。  
![](/assets/cloud-quickstart-guide/images/A22386DA-A769-4A22-BFA3-193BF445CA6B.png)

仕事のアプリでPDFドキュメントを開きます。ここではMicrosoft Outlookアプリを使って、メールに添付されたPDFを開きました。  
![](/assets/cloud-quickstart-guide/images/0482890B-BC1E-4001-ACE8-67B14453A978.png)

PDFドキュメントが仕事のGoogle PDF Viewerアプリで開かれます。さらにメニューから「ファイルを送信」を選択します。  
![](/assets/cloud-quickstart-guide/images/C224C6FA-D8B3-4358-AEAB-C5C493BB8E02.png)

共有先として鞄マーク付きの仕事のアプリのみが表示され、個人領域にインストールしたEvernoteやAdobe Readerにファイルを共有することはできません。しかしBluetoothで他のデバイスに送信することはできるようです。  
![](/assets/cloud-quickstart-guide/images/5FEC32DE-2A2F-444A-8C70-61307C76E04F.png)

「Fully Managed」や「Fully Managed + Work Profile」のデバイスでは、機能制限（ロックダウン）の構成を使ってデバイスのBluetoothを無効にすることができます。「Work Profile」の場合にはBluetoothを無効にする機能制限項目はありませんが、システムアプリとしてのBluetoothアプリを無効化することで同様の効果を得ることができます。  
![](/assets/cloud-quickstart-guide/images/91603053-D3AC-45E5-91E1-F6EE0F322079.png)

![](/assets/cloud-quickstart-guide/images/66A2EFB4-7B5F-4A3A-B6E7-37073C78B2D7.png)

## プロファイル間のコピー＆ペーストの禁止動作

仕事のアプリから個人のアプリへは、コピー＆ペーストの操作も禁止されます。仕事のアプリ内でメールの本文やPDFファイルのテキストを長押ししてコピーしても、個人のメモ帳アプリなどには貼り付けできません。仕事のアプリから仕事のアプリへは自由にコピー＆ペーストができます。
