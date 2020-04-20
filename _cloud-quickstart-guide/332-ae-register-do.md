---
title: "デバイスを登録する（Fully Managed）"
permalink: /cloud-quickstart-guide/ae-register-do/
---
Android Enterpriseの Fully Managed モードでは、会社指定のアプリのみが利用できます。ユーザーが自由にアプリをインストールして利用できる個人領域はありません。

Fully Managed モードでのデバイス登録は、Fully Managed + Work Profile モードの場合と同様に、デバイスを工場出荷時にリセットした状態から行いますが、その前にMobileIron Cloud側の設定変更が必要になります。

## MobileIron Cloudの設定を変更

MobileIron CloudにはAndroid Enterpriseの３つのモードに対応する構成が予め用意されており、この構成をデバイスに割り当てることでモードが決定します。デフォルトの状態では、いずれの構成も全てのAndroidデバイスが配布先になっていることがわかります。なおWork ManagedはFully Managedは同じ意味です。  
![](/assets/cloud-quickstart-guide/images/7988AA6A-1215-4D52-BD69-37142CEFA09B.png)

デバイスで「ようこそ」画面からFully Managedとなりうるセットアップ手順を開始した場合、Managed Device with Work Profile (Fully Managed + Work Profile) の構成と Work Managed Device (Fully Managed) の両方が割り当てられていると、Managed Device with Work Profileが優先します。したがってこれから登録するデバイスにManaged Device with Work Profileの構成が割り当たらないように配布先から除外することで、Work Managed Device (Fully Managed)の構成が適用されます。

「Managed Device with Work Profile」の構成を開き、編集ボタン（鉛筆のアイコン）をクリックします。  
![](/assets/cloud-quickstart-guide/images/767E0C95-23D9-4496-8071-E6DD891405CF.png)

設定の内容はありませんので、そのまま［次へ］ボタンをクリックします。  
![](/assets/cloud-quickstart-guide/images/DE1EFC74-028A-4A04-8CC6-084DC6646B6A.png)

配布先を「デバイスなし」に設定し、［完了］ボタンをクリックします。  
![](/assets/cloud-quickstart-guide/images/BC6B6AA7-F8D9-47F0-AEC9-40432D838F4D.png)

これで優先度の低い「Work Managed Device」構成が割り当たるようになりました。  
![](/assets/cloud-quickstart-guide/images/FAFCE05E-8AFB-48DA-A54C-8A982B85D37E.png)

**ヒント** 今回は「Managed Device with Work Profile」が全く割り当たらないように配布先を「なし」にしてしまいましたが、特定のユーザーや特定のデバイスの種類などを条件としたデバイスグループを作成して割り当てることもできます。
{: .notice--info}

## デバイスの登録

Fully Managedモードのデバイス登録手順は、Fully Managed + Work Profileの場合と全く同じです。

MobileIron Goの登録後にホーム画面を確認すると、アイコンに鞄のマークは付いていません。Fully Managedモードのデバイスには仕事の領域しか無いため、鞄マークで分けて表示する必要が無いためです。  
![](/assets/cloud-quickstart-guide/images/D68E3A9D-E22A-468F-8A87-41B32BC48F1D.png)
