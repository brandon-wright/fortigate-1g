---

copyright:
  years: 2017,2018
lastupdated: "2018-01-16"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# FAQ

以下は、FortiGate Security Appliance (FSA) 1Gbps ファイアウォールの使用についてのよくあるご質問です。

## ファイアウォールとは何ですか?

ファイアウォールは、サーバーの上流に接続されるネットワーク・デバイスです。ファイアウォールにより、不要なトラフィックがサーバーに到達する前にブロックされます。

## なぜファイアウォールを使用する必要がありますか?

ファイアウォールを使用する主な利点は、サーバーで処理する必要があるのが「良好な」トラフィックのみになるという点です。つまり、サーバーのリソースをその本来の目的にのみ使用でき、不要なトラフィックの処理に使用せずに済みます。

## IBM はどのようなファイアウォール製品を提供していますか?
この[トピック![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.bluemix.net/docs/infrastructure/fortigate-10g/explore-firewalls.html#explore-firewalls){: new_window}を参照すると、IBM Cloud で提供されるすべてのファイアウォール製品の詳しい比較を確認できます。 

## FortiGate Security Appliance 1Gbps は IBM のロード・バランサー製品と互換性がありますか?

はい。FSA 1Gbps は、クラウド・ロード・バランシング・サービス、ローカル・ロード・バランサーと互換性があり、さらには Citrix Netscaler VPX および MPX と互換性があります。

## パブリック・トラフィックは、ロード・バランサーとファイアウォールのどちらを最初に通過しますか?

パブリック・インターネットからのトラフィックは、最初にロード・バランシング製品を通過し、次にハードウェア・ファイアウォール製品を通過し、最後に NetScaler 製品 (およびお客様のサーバー) を通過します。

## IBM ではファイアウォールの帯域幅に対して課金していますか?

FortiGate Security Appliance 1Gbps は、帯域幅では課金されません。また、FSA では、サーバーが応答する必要があるトラフィックを制限することで、総帯域幅使用率を削減できます。

## Windows ファイアウォールでグレー化されているポートは何ですか?

IBM Cloud は、Evault、SNMP、Nagios モニタリングなど、サーバーで利用できる多種多様なサービスを提供しています。これらのサービスでは、当社の内部システムがお客様のサーバーとある程度まで通信することが必要になります。例外リストに表示されるグレー化されているポートは、内部ネットワークでのみ開かれるポートです。これらは、パブリック (インターネット) ネットワーク接続ではブロックされます。内部ネットワークはセキュアなネットワークであるため、これらのポートを開くことは安全と見なされます。

これらのポートは、通常は変更できません。ただし、ファイアウォール・ルールをリセットすると、ポートは例外リストから消去されます。ファイアウォール・ルールをリセットすると、これらの追加サービスに悪い影響が及ぶ場合があり、サーバーの構成によっては他の問題も発生することがあるので注意してください。

## どの IP 範囲を、ファイアウォール通過の許可対象にしますか?

ファイアウォールを通過できるようにする IP アドレスおよび IP 範囲のリストについては、[ここ](https://console.bluemix.net/docs/infrastructure/hardware-firewall-dedicated/ips.html){: new_window}を参照してください。 

## FortiGate Security Appliance 1Gbps が保護するサーバーの最大数はどのくらいですか?

FortiGate Security Appliance 1Gbps は、パブリック VLAN 上のすべてのサーバーを保護できます。ただし、これらのファイアウォール・デバイスは 2Gbps アップリンクと接続されるため、アプリケーションのパフォーマンス・ニーズを満たすようにファイアウォール・インスタンスの数を調整することをお勧めします。これを行うには、ファイアウォールと関連する計算リソースを追加できるようにするために、ポッド内に追加のパブリック VLAN ファイアウォールをデプロイします。

## 各ファイアウォール製品には、どのような VPN オプションが含まれますか?

一部のファイアウォールのみ VPN を提供しており、また一部の VPN オプションのみ同じです。VPN の一般的なオプションを以下に示します。

* お客様はそれぞれ、当社のプライベート・ネットワークへの無制限の SSL VPN 接続を利用できます。これらの接続は、カスタマー・ポータルにログインしているときに、ページ上部の VPN リンクをクリックすることで確立できます。
* お客様は、アカウントごとに 1 つの PPTP VPN も利用できます。お客様は、$5/月の追加料金 (5 ユーザー単位) で、アカウントに PPTP VPN ユーザーを追加できます。
* IBM Cloud は、基本的なマルチテナント IPSec VPN サービスも提供します。
* FortiGate Security Appliance 1Gbps は、パブリック・ネットワーク・アクセスのみ (IBM Cloud プライベート・ネットワークへのアクセスなし) の SSL および IPSec VPN オプションを提供します。
* ネットワーク・ゲートウェイは、パブリック・ネットワークまたはプライベート・ネットワークで SSL、IPSec、および OpenVPN 機能を提供します。
* NetScaler 製品は、パブリック・ネットワークまたはプライベート・ネットワークで SSL および IPSec VPN を提供できます。
* お客様は、IBM Cloud 環境内のサーバーに VPN ソリューションをデプロイすることもできます。

## 高可用性オプションを選択した場合、この機能を活用するためにどのような手順を実行する必要がありますか?

何も実行する必要ありません。HA が注文されると、IBM Cloud は、HA 構成でアプライアンスを自動的にプロビジョンします。プライマリー・デバイスで障害が発生すると、セカンダリー・パッシブ・デバイスがプライマリー・アクティブ・インスタンスとして引き継ぎ、トラフィックの受け渡しを開始します。このフェイルオーバーは通常自動的ですが、サーバーをモニターし、トラフィックが正常に受け渡されるようにすることをベスト・プラクティスとしてお勧めします。

## どのファイアウォール製品がパブリックからプライベートへの NAT、プライベート VLAN セグメンテーション、またはこれらの両方をサポートしていますか?

どのハードウェア・ファイアウォール製品もプライベート・ネットワークへはアクセスできません。これらの機能をインラインで提供するには、ネットワーク・ゲートウェイが必要です。NetScaler 製品は、パブリック・ネットワークとプライベート・ネットワークの両方にアクセスできます。
