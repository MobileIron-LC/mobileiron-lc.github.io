---
title: "Managed Open-Inの動作"
permalink: /cloud-quickstart-guide/ios-managed-open-in-experience/
---
では実際にManaged Open-In制御の動作をデバイスで見ていきましょう。前提として、これまでの設定でiOS標準メールアプリに管理されたアカウント（ExchangeまたはGoogle）を登録済みであることとします。また管理されたアプリとしてSalesforceとOutlookがインストール済みとします。

## テストの準備

管理されていないアプリとアカウントを準備します。設定アプリからアカウントの追加を行い、GmailやOutlook.comなど個人向けメールサービスのアカウントを設定して下さい。下図の例ではOutlook.comのアカウントを追加しました。また個人のiCloudにもサインインしています。  
![](/assets/cloud-quickstart-guide/images/5F2B3C70-B2A0-46B6-A419-DE3E93D0545B.png)

管理されていないアプリとしてOpen-Inでファイルを受け取るアプリも、個人のApple IDを使って通常のAppStoreからインストールします。下図の例ではEvernoteとAcrobat Readerをインストールしました。  
![](/assets/cloud-quickstart-guide/images/8D3D5EAD-8100-4719-8B98-5E27F24F8FBC.png)

このiOSデバイスのユーザーの企業用、および個人用のメールアドレスの両方に、別のユーザーが別のPCから、以下の画面のように添付ファイル付きメールを送信したとします。「宛先」には企業用と個人用のメールアドレスの2つを指定しています。添付ファイルはPDFとします。  
![](/assets/cloud-quickstart-guide/images/8006524F-726A-4891-9E25-BD0C4ABBE653.png)

iOSデバイス側では、標準メールアプリで個人用と企業用それぞれで同じメールを受信しました。  
![](/assets/cloud-quickstart-guide/images/35CB4132-2E21-4E12-BADE-16895407DAB5.png)

## 管理されていないアカウントからのOpen-In動作

まずは個人メールアドレス宛に届いたメールを開いてみましょう。  
![](/assets/cloud-quickstart-guide/images/17A9B970-4173-404B-9EB8-08CB1828A69D.png)

メールを開き、続けて添付のPDFファイルのプレビューをタップします。  
![](/assets/cloud-quickstart-guide/images/5E9E9B69-F1D9-426A-BFCD-D0E6D32306A9.png)

添付のPDFファイルが全画面でプレビューされました。この時点ではPDFファイルはまだメールアプリの個人アカウントの中にあります。画面左下のOpen-inのボタンをタップします。  
![](/assets/cloud-quickstart-guide/images/DCAE36C5-F700-4F14-BB9F-AC111FA95C33.png)

個人用アプリが一覧表示され、Open-Inで渡すことができます。「AirDrop」も利用することが可能です。一方、SalesforceやOutlookといった企業用の管理アプリは一覧に表示されず、渡せなくなっています。  
![](/assets/cloud-quickstart-guide/images/FD1C41E9-DA03-422F-821A-2AE19EDB7213.png)
![](/assets/cloud-quickstart-guide/images/D3AEE9ED-5C69-4017-926E-6FCBD5D8A26A.png)

［"ファイル"に保存］をタップすると、「ファイル」アプリ経由で管理されていないAcrobatアプリや個人のiCloudドライブへの保存が可能です。  
![](/assets/cloud-quickstart-guide/images/0B35B672-A21A-481D-8358-C14B4B9E5F18.png)

## 管理されたアカウントからのOpen-In動作

次は仕事のメールアドレス宛に届いたメールを開いてみましょう。  
![](/assets/cloud-quickstart-guide/images/0C8A286A-578E-47CF-A89D-389B0043EC73.png)

添付ファイルのプレビューをタップします。  
![](/assets/cloud-quickstart-guide/images/4C645D51-AC05-4722-91F3-7C7DFF5B2AFB.png)

Open-Inのボタンをタップします。  
![](/assets/cloud-quickstart-guide/images/1DF3203A-9B3D-43CB-966F-DE3E2CA86F4F.png)

Open-inでファイルを渡すことができるのは企業用の管理アプリのみです。一方、EvernoteとAcrobatといった個人用の非管理アプリは一覧に表示されず、渡すことができません。また「AirDrop」も管理されていない宛先として扱われているため、アイコンが表示されず利用できません。  
![](/assets/cloud-quickstart-guide/images/BE3C5D96-6515-4007-AF45-B0DD4E16303F.png)

["ファイル"に保存] からも、管理されていないAcrobatアプリやiCloudドライブは表示されません。今回はファイルアプリに対応した「管理された」アプリもインストールされていないため、[保存] ボタンがグレーアウトしました。  
![](/assets/cloud-quickstart-guide/images/43E5C0CF-377D-4FBA-8736-60218B54BAFF.png)

このように管理された仕事のアプリと、管理されていない個人用アプリの間で、Open-Inによるデータの受け渡しを禁止することで、情報漏洩のリスクを低減しながら、仕事のアプリ間では自由にファイルをやり取りすることができます。
