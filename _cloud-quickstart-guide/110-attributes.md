---
title: "属性"
permalink: /cloud-quickstart-guide/attributes/
---

ユーザーの名前やEメールアドレス、デバイスのシリアル番号など、ユーザーやデバイスに固有の情報は「属性」として管理されます。これを上手く利用することで効率的な管理が可能になります。前項で作成したローカルユーザーが持つ属性とその値を見てみましょう。

ユーザー > （ユーザーを選択）> 属性タブ
![](/assets/cloud-quickstart-guide/images/F6C58EC2-826D-4B48-8357-23986E54B476.png)
例えばこのユーザーのユーザーIDを表す属性名は ${userUID} で、その値は taro@mobilefirst.jp です。

利用可能なすべての属性の種類はシステムメニューから確認することができます。

管理 > システム > 属性
![](/assets/cloud-quickstart-guide/images/D04AFF62-CD2B-4642-AAE4-70333EE14918.png)

多くの属性がシステム属性として予め定義されています。ユーザーのためのシステム属性には次のようなものがあります。Active Directoryなどの外部ディレクトリから同期したユーザーでは、外部ディレクトリ上のユーザー属性も取り込むことができます。
![](/assets/cloud-quickstart-guide/images/3495BBE1-15A0-4135-9593-D7D49472E33B.png)

ユーザーだけでなくデバイスにも多くの属性が定義されています。デバイスをMobileIron Cloudに登録することで収集されたハードウェアの情報は、ぞれぞれを表す属性の値として格納されます。
![](/assets/cloud-quickstart-guide/images/9A0FED8F-0B21-4566-8A38-E91DF774D324.png)

## カスタム属性

予め定義されているシステム属性以外に、任意のユーザー属性やデバイス属性を、カスタム属性として定義することができます。カスタム属性には管理者が自由に値をセットすることができます。

次項以降で説明する、属性値の条件を使ったグルーピングに利用することを想定して、カスタム属性を定義してみましょう。

+追加ボタンをクリックします。

isMemberOfCustomUserGroupA という名前のカスタムユーザー属性を定義します。
![](/assets/cloud-quickstart-guide/images/51AB2E47-36F2-4328-99B2-5A59D36A9288.png)

同様に isMemberOfCustomDeviceGroupX というカスタムデバイス属性を定義します。属性タイプとして今度はデバイスを指定します。
![](/assets/cloud-quickstart-guide/images/9BE343F4-0666-48D6-B482-766589DC812F.png)

![](/assets/cloud-quickstart-guide/images/D9B77533-EFFF-4A6F-93A1-2FDD0A62046B.png)

カスタム属性の定義はこれだけで完了です。実際には個々のユーザーやデバイスに対して、これらのカスタム属性とその値をセットして利用します。次項で詳しく説明します。
