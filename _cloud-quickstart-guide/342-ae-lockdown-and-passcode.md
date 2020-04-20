---
title: "機能制限と高度なパスコードポリシー"
permalink: /cloud-quickstart-guide/ae-lockdown-and-passcode/
---
## 機能制限（ロックダウン）

ロックダウンの構成を使って、Androidデバイスの機能や操作を一部制限することができます。

「ロックダウン＆キオスク：Androidエンタープライズ」の構成を新しく追加します。MobileIron CloudがサポートしているAndroid Enterprise以外の（現在ではあまり使われない）管理フレームワーク向けのロックダウン構成も見つかりますので、間違わないようにして下さい。  
![](/assets/cloud-quickstart-guide/images/23288ABF-FC61-4BE8-A7E6-46463F894E17.png)

Android Enterprise向けのロックダウン構成は、管理モードごとに設定できる項目が異なりますので、モード毎に別々の構成を作成する必要があります。たとえばWork Profile向けに作成したロックダウン構成は、Fully ManagedやFully Managed + Work Profileモードのデバイスには適用されません。  
![](/assets/cloud-quickstart-guide/images/83512BCF-D326-4BED-8061-9DF2A54D75DA.png)

適用先の管理モードを選択すると、ロックダウンの設定項目が表示されます。どんな項目が設定できるかは実際の管理画面をご覧下さい。基本的に **Work Profile** に対しては、Work Profile（内のアプリ）の動作に対する機能制限が設定できます。特定のハードウェア機能をデバイス全体で無効にするなど、個人領域のアプリの利用が制限されるようなロックダウン項目はありません。ただし、仕事領域のセキュリティにも関わる「デバッグ機能の禁止」や「アプリ検証を確認」（Google Play プロテクト）についてのロックダウン設定はデバイス全体に影響します。 **Fully Managed** なデバイス対しては、デバイス全体に影響するハードウェア機能の無効化などを含む強い制約が設定できます。 **Fully Managed + Work Profile** のデバイスについてはデバイス全体に影響するロックダウンと、Work Profileに影響するロックダウンの両方が設定できます。

![](/assets/cloud-quickstart-guide/images/4066239D-893A-4D13-BD61-B1196D0433F9.png)

![](/assets/cloud-quickstart-guide/images/A8AAE034-200A-4743-A3C4-A04C11FB1139.png)

### 仕事と個人の領域を分ける「プロファイル間のコピー貼り付けを禁止」

「プロファイル間のコピー貼り付けを禁止」のロックダウン項目を有効にすることで、仕事のアプリで扱っているファイルを個人のアプリに共有する（複製して渡す）ことができなくなります。また仕事のアプリで開いているドキュメントからテキストの一部をコピーして、個人のアプリで開いているドキュメントに貼り付けする操作も、この項目によって禁止されます。

「プロファイル間のコピー貼り付けを禁止」を設定しても、「個人のアプリ → 仕事のアプリ」方向の共有は禁止されません。Android 9以降に適用できる「プロファイルへの共有を禁止」によって個人のアプリから仕事のアプリへの共有を禁止できます。

### 必ず設定しよう、「アカウントの変更禁止」

「アカウントの変更禁止」のロックダウンはかならず設定しましょう。この項目は３つの管理モードすべてにおいて設定できます。

以下は「アカウントの変更禁止」を設定しなかった場合のリスクの説明です。  
仕事のPlayアプリを開いたとき、管理者が配布しているアプリだけが表示されていますが、よく見るとアカウントの切替ボタンが表示されています。  
![](/assets/cloud-quickstart-guide/images/CEF9650F-A9E2-4B3B-B170-06E1B886D8E8.png)

アカウントの切替ボタンをタップすると、現在仕事のPlayにログイン中のGoogleアカウントが表示され、  
&lt;ランダムな数字のID&gt;@android-for-work.gserviceaccount.com  
の形式のIDが使われていることがわかります。

このIDをManaged Google Play Accountといい、MobileIron Cloudのユーザーと対応しています。Managed Google Play Accountの管理はMobileIron Cloudがバックグラウンドで行いますので、管理者やデバイスのユーザーが意識する必要はありません。
{: .notice--info}

「アカウントの変更禁止」を設定していない場合、下図のように「別のアカウントを追加」で仕事のPlayに個人のGoogleアカウント追加できてしまいます。  
![](/assets/cloud-quickstart-guide/images/086876A3-0DDD-4DDF-8396-F813B100248D.png)

仕事のPlayでGoogleアカウントを個人アカウントに切り替えると、公開のPlayストアから任意のアプリがダウンロードできます。  
![](/assets/cloud-quickstart-guide/images/3629E45D-AFD2-47FD-A837-4C262B510D98.png)

仕事のPlayを使って、個人のGoogleアカウントに切り替えてダウンロードしたアプリは、仕事のアプリとしてインストールされます。これでは問題がありますね。  
![](/assets/cloud-quickstart-guide/images/26F0E579-5798-44E3-8DDF-7077792B97A4.png)

### ロックダウン構成の割り当て

ロックダウン構成をデバイスに割り当てる際には、特定のAndroid Enterprise管理モードのデバイスのみに割り当てるようなグルーピングを考える必要はありません。下図の例では各モード用にロックダウン構成を作成し、いずれも全てのAndroid Enterpriseを対象に割り当てていますが、たとえばWork ProfileのデバイスにはWork Profile向けのロックダウン構成のみしか実際には適用されませんので、構成同士が競合する心配はありません。  
![](/assets/cloud-quickstart-guide/images/663294D8-62A7-473C-B0DC-5DCCCD519392.png)

## Android向け高度なポスコードポリシー

MobileIron Cloudの初期セットアップウィザードの途中で、パスコードの桁数を設定する画面がありました。そこでの設定は「パスコード」の構成として既に保存されており、Androidを含む全てのOSプラットフォームを対象とする設定して割り当てられていますが、Android Enterpriseにおいては「高度なAndroidパスコードおよびロック画面」の構成で、より細かな設定が可能です。  
![](/assets/cloud-quickstart-guide/images/603A9E41-60E0-4B25-99BC-95542D521C9C.png)

また「Work Profile」または「Fully Managed + Work Profile」のデバイスでは、デバイスのロック画面のためのパスコードとは別に、仕事のアプリを開くためのパスコードを要求することができます。  
![](/assets/cloud-quickstart-guide/images/0E8A8058-1FF1-4739-91A1-A8869FABA942.png)

「デバイスのパスコード」と「仕事用プロファイルのパスコード」は、デバイスの設定アプリからそれぞれに設定ができます。多くのデバイスでは仕事用プロファイルのセキュリティについてデフォルトで「統一ロックを使用」の設定になっています。別々にすることもできますが、ユーザーが混乱する可能性がありますので注意しましょう。  
![](/assets/cloud-quickstart-guide/images/CD23CBB6-A9EC-49B8-91EF-15535C43299D.png)
