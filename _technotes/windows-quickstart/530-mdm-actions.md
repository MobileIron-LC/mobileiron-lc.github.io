---
title: "MDMアクション"
permalink: /technotes/windows-quickstart/mdm-actions/
sidebar:
    nav: "windows-quickstart"
---

Windows10における ワイプ / 撤去 の各MDMアクションの動作と影響範囲について解説します。  
ロックはWindows10プラットフォームでは利用できません。

MDMアクションはデバイスの詳細画面から実行できます。  
![](/assets/technotes/windows-quickstart/F2A328F4-2895-4328-BD54-65CD28C7859B.png)

### ワイプ

Windows10デバイスをワイプすると、回復イメージからの初期化（再インストール）が行われます。

![](/assets/technotes/windows-quickstart/6f28ae9a-fbdf-4248-bf87-fecf5300b20a.png)

### 撤去

MDM登録が解除され、MobileIron CloudからWindows MDMプロトコルによって配布された設定が解除されます。
但し、インストールされていたアプリケーションや、アプリケーションが作成したデータファイルなどはドライブに残ります。
iOSのように企業領域が完全に消えるわけではないので注意が必要です。