---

copyright:

  years: 2018, 2019
lastupdated: "2019-06-03"

keywords: tagging, enabling others to tag, tagging permissions

subcollection: resources

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}


# ユーザーへのリソースのタグ付け権限の付与
{: #access}

アカウント所有者は、リソースのタグ付け操作の一部を委任することができます。 そのために、リソースへのタグの追加とリソースからのタグの削除を行うためのアクセス権限をアカウント内の他のユーザーに付与できます。 アカウントのユーザーがリソースにタグを追加するには、適切なアクセス権限が割り当てられている必要があります。 リソース・グループに属するサービスへのアクセス権限は、{{site.data.keyword.Bluemix}} Identity and Access Management (IAM) のアクセス・ポリシーによって管理され、Cloud Foundry 組織およびスペースに属するサービスへのアクセス権限は、Cloud Foundry 組織およびスペースの役割によって管理されます。
{: shortdesc}

## タグ付けの許可
{: #tagging-permissions}

タグは、アカウント内のすべてのユーザーに表示されます。 リソースにタグが付けられると、そのリソースに対する読み取り権限を持つすべてのユーザーにタグが表示されます。 リソースでタグを追加または削除するには、リソース・タイプに応じて、特定のアクセス役割または許可が必要です。 以下の表を確認して、各リソース・タイプに必要な役割を理解してください。


| リソース・タイプ | 役割 |
|--------|---------------|
| IAM 対応 | リソースのエディターまたは管理者 |
| Cloud Foundry | リソースが属するスペースの開発者役割  |
| クラシック・インフラストラクチャー*| 「ハードウェア詳細の表示 (View hardware details)」許可または「仮想サーバー詳細の表示 (view virtual server details)」許可 |
| クラシック・インフラストラクチャー上の Cloud Object Storage S3 | ストレージ管理許可 |
{: caption="表 1. タグの追加および削除に必要な役割" caption-side="top"}
{: summary="This is a simple data table. However, the asterisk indicates that you must read the qualifying note after this table."}

* クラシック・インフラストラクチャー内のタグ付け可能リソースは、仮想ゲスト、仮想専用ホスト、ネットワーク・アプリケーション配信コントローラー、ゲートウェイ・メンバー、サブネット、VLAN、および VLAN ファイアウォール (専用) です。


## IAM 対応リソースにタグを付けるためのアクセス権限の付与
{: #iam-managed}

リソース・グループに属するリソースは、{{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) アクセス・ポリシーによって管理されます。 以下のステップを実行して、ユーザーが IAM 対応リソースにタグを付けるためのエディター役割を割り当てます。

  1. {{site.data.keyword.Bluemix_notm}} コンソールで**「管理」>「アクセス (IAM)」**をクリックし、**「ユーザー」**を選択します。
  2. アクセス権限を付与するユーザーの名前をクリックします。
  3. **「アクセス・ポリシー」** > **「アクセス権限の割り当て」**をクリックします。
  4. **「リソースへのアクセス権限の割り当て」**オプションを選択します。
  5. サービスのリストから、特定のサービスまたは**「すべての ID およびアクセス対応サービス」**を選択します。
  6. プラットフォーム・アクセス役割のリストから、**「エディター」**を選択します。
  7. **「割り当て」**をクリックします。

## Cloud Foundry リソースにタグを付けるためのアクセス権限の付与
{: #cf_tag_access}

Cloud Foundry 組織およびスペースに属するリソースは、Cloud Foundry 組織およびスペースの役割によって管理されます。 以下のステップを実行して、ユーザーが Cloud Foundry リソースにタグを付けるための開発者スペース役割を割り当てます。

 1. **「管理」 > 「アクセス (IAM)」**をクリックして、**「ユーザー」**を選択します。
2. アクセス権限を付与するユーザーの名前を選択します。
3. **「Cloud Foundry アクセス権限」**をクリックします。
4. **「組織の割り当て」**をクリックします。
5. ユーザーにアクセス権限を付与するサービス・インスタンスを含む`「組織」`を展開して選択します。
6. 地域を選択します。
7. **「開発者」**スペースの役割を選択します。
8. **「役割の保存」**をクリックします。

## クラシック・インフラストラクチャー・リソースにタグを付けるためのアクセス権限の付与
{: #classic-infra}

以下のステップを実行して、ユーザーがクラシック・インフラストラクチャー・サービスにタグを付けるための管理者サービス・アクセス役割を割り当てます。

  1. **「管理」 > 「アクセス (IAM)」**をクリックして、**「ユーザー」**を選択します。
  2. アクセス権限を付与するユーザーの名前をクリックします。
  3. **「クラシック・インフラストラクチャー」**をクリックします。
  4. **「許可」**タブで、**「デバイス」**カテゴリーを展開します。
  5. **「ハードウェア詳細の表示 (View Hardware Details)」**および**「仮想サーバー詳細の表示 (View Virtual Server Details)」**を選択します。 Cloud Object Storage S3 へのアクセス権限を割り当てる必要がある場合は、**「ストレージ管理」**許可を割り当てます。
  6. **「保存」**をクリックします。
  7. **「デバイス」**タブをクリックします。
  8. タグ付けするリソースに応じて、**「すべてのベア・メタル・サーバー」**または**「すべての仮想サーバー」**を選択します。
