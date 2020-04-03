---
title: "ユーザーグループ"
permalink: /cloud-quickstart-guide/usergroup/
---

それぞれのユーザーは１つ以上のユーザーグループに所属することができます。ユーザーグループには次のようなものがあります。
- 手動管理のユーザーグループ
- 外部ディレクトリと連携するユーザーグループ（AD/LDAP上のOUやグループを同期したもの）
- 属性値を条件にした動的管理のユーザーグループ

## 手動管理ユーザーグループ

手動管理のユーザーグループは素早く直感的に作成できます。

ユーザー > ユーザーグループ > +追加  
![](/assets/cloud-quickstart-guide/images/370CA652-DF96-4559-AC8F-EC446C7D5E0E.png)

手動管理タブを選択し、ユーザーを検索して追加（チェック）します。  
![](/assets/cloud-quickstart-guide/images/DC89BD85-AD6F-40B3-8485-5F6DAA540156.png)

ユーザーグループのメンバーは選択済みタブに表示されます。  
![](/assets/cloud-quickstart-guide/images/FFC56877-F682-45C7-8D53-3BF9FD5FAD83.png)

**注意** 手動管理ユーザーグループは簡単に作成できる一方で、数多くのメンバーを管理することには適していません。手動管理ユーザーグループは上の編集画面で全メンバーが容易に確認できる程度の数で利用するようにして下さい。
{: .notice--warning}

## 外部ディレクトリと連携するユーザーグループ

外部ディレクトリからグループやOUをMobileIronに同期した場合、そこに含まれるユーザーと共に、グループやOUもMobileIron Cloud上のユーザーグループとして自動的に認識します。本ガイドでは割愛します。

## 属性値を条件にした動的管理のユーザーグループ

動的管理のユーザーグループは大規模な運用に適しています。本番運用において、外部ディレクトリと連携するもの以外のユーザーグループは、手動管理ではなくこちらの属性値を条件にした動的管理のユーザーグループとして定義しておくことをお勧めします。

ユーザー > ユーザーグループ > +追加

動的管理のユーザグループは１つまたは複数の条件をANDまたはORでつないだルールによって定義します。先に作成したカスタム属性を条件に使ってユーザーグループを定義してみましょう。

カスタムユーザー属性 [isMemberOfCustomUserGroupA] は次と等しい： 1
{: .notice}

![](/assets/cloud-quickstart-guide/images/AB5CC03D-F0BE-49F4-A26A-1FEEF6410F28.png)

まだこのユーザーグループ含まれるメンバーはいません。ユーザーに属性値 isMemberOfCustomUserGroupA=1 を与えることで、そのユーザーがメンバーになります。

ユーザー > ユーザー >（ユーザーの表示名を選択して詳細表示）> 属性タブ

カスタム属性を +新規追加 します。
![](/assets/cloud-quickstart-guide/images/857B0853-BDB6-4E5C-BF7A-2F4D9DC1BD27.png)

属性名 isMemberOfCustomUserGroupA を選択し、値に 1 をセットして保存します。
![](/assets/cloud-quickstart-guide/images/AAF4BFC4-6435-4253-909D-38EEB955987B.png)

動的ユーザーグループのメンバーを確認します。

ユーザー > ユーザーグループ >（ユーザーグループの名前を選択して詳細表示）> ユーザータブ

属性値をセットしたユーザーがユーザーグループのメンバーになりました。  
![](/assets/cloud-quickstart-guide/images/2CACA068-6043-4635-8045-9C730F89526B.png)

ユーザーの一覧から複数ユーザーを選択し、カスタム属性をまとめて割り当て（または削除）することもできます。  
![](/assets/cloud-quickstart-guide/images/4CBDA8A0-CE7E-4F3D-B902-2F55854F07A1.png)

![](/assets/cloud-quickstart-guide/images/5B1FAC50-D925-4860-9A59-FEFBF821C546.png)

![](/assets/cloud-quickstart-guide/images/F5102F30-5AB3-4813-AE0A-1AD96B632918.png)
