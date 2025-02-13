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


# 授予用户标记资源的访问权
{: #access}

作为帐户所有者，您可能希望委派一些标记资源的责任。为此，您可以向帐户中其他用户授予在资源中添加和除去标记的访问权。要使帐户上的用户能够向资源添加标记，必须为其分配相应的访问权。对属于资源组的服务的访问权通过 {{site.data.keyword.Bluemix}} Identityand Access Management (IAM) 访问策略进行管理，对属于 Cloud Foundry 组织和空间的服务的访问权通过 Cloud Foundry 组织和空间角色进行管理。
{: shortdesc}

## 标记许可权
{: #tagging-permissions}

标记对帐户中的任何用户可见。标记资源后，对该资源具有读访问权的所有用户都可以看到该标记。要在资源中添加或除去标记，需要某些访问角色或许可权，具体取决于资源类型。查看下表以了解每种资源类型需要的角色。


|资源类型|角色|
|--------|---------------|
|支持 IAM|资源的“编辑者”或“管理员”|
|Cloud Foundry|资源所属空间的“开发者”角色|
|经典基础架构*|查看硬件详细信息许可权或查看虚拟服务器详细信息许可权|
|经典基础架构上的 Cloud Object Storage S3|存储管理许可权|
{: caption="表 1. 添加和除去标记需要的角色" caption-side="top"}
{: summary="This is a simple data table. However, the asterisk indicates that you must read the qualifying note after this table."}

*经典基础架构中可标记的资源包括虚拟访客、虚拟专用主机、网络应用程序交付控制器、网关成员、子网、VLAN 和 VLAN 防火墙（专用）。


## 授予标记支持 IAM 的资源的访问权
{: #iam-managed}

属于资源组的资源通过 {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) 访问策略进行管理。完成以下步骤为用户分配“编辑者”角色，以标记支持 IAM 的资源：

  1. 在{{site.data.keyword.Bluemix_notm}} 控制台中，单击**管理 > 访问权 (IAM)**，然后选择**用户**。
  2. 单击要为其授予访问权的用户的名称。
  3. 单击**访问策略** > **分配访问权**。
  4. 选择**分配对资源的访问权**选项。
  5. 从服务列表中，选择特定服务或**所有启用“身份和访问权”的服务**。
  6. 从平台访问角色列表中，选择**编辑者**。
  7. 单击**分配**。

## 授予标记 Cloud Foundry 资源的访问权
{: #cf_tag_access}

属于 Cloud Foundry 组织和空间的资源通过 Cloud Foundry 组织和空间角色进行管理。完成以下步骤为用户分配“开发者”空间角色，以标记 Cloud Foundry 资源：

 1. 单击**管理 > 访问权 (IAM)**，然后选择**用户**。
2. 选择要为其提供访问权的用户的名称。
3. 单击 **Cloud Foundry 访问权**。
4. 单击**分配组织**。
5. 展开并选择您要向用户提供其服务实例访问权的`组织`。
6. 选择区域。
7. 选择**开发者**空间角色。
8. 单击**保存角色**。

## 授予标记经典基础架构资源的访问权
{: #classic-infra}

完成以下步骤为用户分配“管理者”服务访问角色，以标记经典基础架构服务：

  1. 单击**管理 > 访问权 (IAM)**，然后选择**用户**。
  2. 单击要为其授予访问权的用户的名称。
  3. 单击**经典基础架构**。
  4. 在**许可权**选项卡中，展开**设备**类别。
  5. 选择**查看硬件详细信息**和**查看虚拟服务器详细信息**。如果需要分配对 Cloud Object Storage S3 的访问权，请分配**存储管理**许可权。
  6. 单击**保存**。
  7. 单击**设备**选项卡。
  8. 根据要标记的资源，选择**所有裸机服务器**或**所有虚拟服务器**。
