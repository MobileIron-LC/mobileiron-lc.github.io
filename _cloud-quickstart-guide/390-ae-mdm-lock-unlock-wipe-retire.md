---
title: "MDMアクション"
permalink: /cloud-quickstart-guide/ae-mdm-lock-unlock-wipe-retire/
---
Android Enterpriseにおける ロック / アンロック / ワイプ / 撤去 の各MDMアクションの動作と影響範囲について解説します。

MDMアクションはデバイスの詳細画面から実行できます。   
![](/assets/cloud-quickstart-guide/images/E13F5768-C936-44C0-92C1-69A79D632D66.png)

## ロック

ロックを実行するとスクリーンがロック画面となり、現在設定されているPINコードや生体認証などによって解除できます。この動作はAndroid Enterpriseの４つの管理モード全てにおいて同様です。

## アンロック

Android Enterpriseの管理モードによってアンロックの影響範囲が異なります。

<table>
<thead>
<tr><th> 管理モード </th><th> ロック画面 </th><th> アンロック動作 </th></tr>
</thead>
<tbody>
<tr><td rowspan="2"> Work Profile </td><td> デバイス </td><td> 影響なし </td></tr>
<tr><td> 仕事用プロファイル </td><td> 0000に設定 </td></tr>
<tr><td> Fully Managed </td><td> デバイス </td><td> 0000に設定 </td></tr>
<tr><td rowspan="2"> Fully Managed + Work Profile (Android 8-10) </td><td> デバイス </td><td> 0000に設定 </td></tr>
<tr><td> 仕事用プロファイル </td><td> 0000に設定 </td></tr>
<tr><td rowspan="2"> Work Profile on Company Owned Device (Android 11+) </td><td> デバイス </td><td> 影響なし </td></tr>
<tr><td> 仕事用プロファイル </td><td> 0000に設定 </td></tr>
</tbody>
</table>

Work Profileのデバイスのロック画面は企業の管理対象外であるため、MobileIron Cloudからはアンロックできません。

アンロックの動作は画面ロックPINコードを「0000」に再設定するものです。0000で画面ロックを解除すると、MobileIron Goアプリが新しい画面ロックの設定を促します。  
![](/assets/cloud-quickstart-guide/images/E033BD75-D4AD-4D06-A5C9-F2F9BC0B6BAA.png)

アンロックが成功したとき、MobileIron Cloudはユーザーが新しいパスコードを設定するまでの間、そのデバイスを「データ保護/暗号化無効」の状態と認識します。デフォルトで適用されているポリシーではこの状態に対して検疫アクションが設定されており、デバイスでは仕事のPlayからインストールしたアプリが一時的に非表示になります。  
![](/assets/cloud-quickstart-guide/images/4C491FB3-7108-4303-8583-53811AF9540B.png)

## ワイプ / 撤去

ワイプと撤去はAndroid Enterpriseにおいては同じ結果になります。

|管理モード|ワイプまたは撤去の動作|
|---|---|
|Work Profile|仕事用プロファイルのみが削除される|
|Fully Managed|デバイス全体がワイプされる|
|Fully Managed + Work Profile (Android 8-10)|デバイス全体がワイプされる|
|Work Profile on Company Owned Device (Android 11+)|デバイス全体がワイプされる|

## WPCODデバイスの所有の解除

Work Profile on Company Owned Deviceのデバイスは、「所有の解除」（Relinquish）アクションにより、Work Profileだけを撤去することができます。デバイスはワイプされず、個人領域のアプリはそのまま残ります。

各MDMアクションにおけるデバイスの動作について、こちらの[ビデオ](/videos/ae-mdm-action-in-3modes/)も参考にして下さい。
