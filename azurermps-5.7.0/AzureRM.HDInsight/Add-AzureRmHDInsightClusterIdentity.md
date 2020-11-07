---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: A40AB6AB-D3CB-4A6C-B614-0B22085759DA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/add-azurermhdinsightclusteridentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightClusterIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightClusterIdentity.md
ms.openlocfilehash: e4e481a7ee26be966abda3d996575ab1bbd03b42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563520"
---
# <span data-ttu-id="e3cd3-101">Add-AzureRmHDInsightClusterIdentity</span><span class="sxs-lookup"><span data-stu-id="e3cd3-101">Add-AzureRmHDInsightClusterIdentity</span></span>

## <span data-ttu-id="e3cd3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e3cd3-102">SYNOPSIS</span></span>
<span data-ttu-id="e3cd3-103">Добавляет удостоверение кластера в объект конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="e3cd3-103">Adds a cluster identity to a cluster configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3cd3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e3cd3-104">SYNTAX</span></span>

### <span data-ttu-id="e3cd3-105">CertificateFilePath (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e3cd3-105">CertificateFilePath (Default)</span></span>
```
Add-AzureRmHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3cd3-106">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="e3cd3-106">CertificateFileContents</span></span>
```
Add-AzureRmHDInsightClusterIdentity [-Config] <AzureHDInsightConfig> [-ObjectId] <Guid>
 [-CertificateFileContents] <Byte[]> [-CertificatePassword] <String> [[-AadTenantId] <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3cd3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3cd3-107">DESCRIPTION</span></span>
<span data-ttu-id="e3cd3-108">Командлет **Add-AzureRmHDInsightClusterIdentity** добавляет удостоверение кластера в объект конфигурации HDInsight Azure, созданный командлетом New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="e3cd3-108">The **Add-AzureRmHDInsightClusterIdentity** cmdlet adds a cluster identity to the Azure HDInsight configuration object created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="e3cd3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e3cd3-109">EXAMPLES</span></span>

### <span data-ttu-id="e3cd3-110">Пример 1: Добавление сведений об удостоверении кластера в объект конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="e3cd3-110">Example 1: Add Cluster Identity info to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value 
PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Cluster Identity values
PS C:\> $tenantId = (Get-AzureRmContext).Tenant.TenantId
PS C:\> $objectId = "<Azure AD Service Principal Object ID>"
PS C:\> $certificateFilePath = "<Path to Azure AD Service Principal Certificate>"
PS C:\> $certificatePassword = "<Password for Azure AD Service Principal Certificate>"

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightClusterIdentity `
                -AadTenantId $tenantId `
                -ObjectId $objectId `
                -CertificateFilePath $certificateFilePath `
                -CertificatePassword $certificatePassword `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="e3cd3-111">Эта команда добавляет сведения об удостоверении кластера в кластер с именем "-Hadoop-001", позволяя кластеру получить доступ к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e3cd3-111">This command adds Cluster Identity info to the cluster named your-hadoop-001, allowing the cluster to access Azure Data Lake Store.</span></span>

## <span data-ttu-id="e3cd3-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e3cd3-112">PARAMETERS</span></span>

### <span data-ttu-id="e3cd3-113">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="e3cd3-113">-AadTenantId</span></span>
<span data-ttu-id="e3cd3-114">Указывает идентификатор клиента Azure AD, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e3cd3-114">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3cd3-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="e3cd3-115">-CertificateFileContents</span></span>
<span data-ttu-id="e3cd3-116">Указывает содержимое файла сертификата, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e3cd3-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Byte[]
Parameter Sets: CertificateFileContents
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3cd3-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="e3cd3-117">-CertificateFilePath</span></span>
<span data-ttu-id="e3cd3-118">Задает путь к файлу сертификата, который будет использоваться для проверки подлинности участника-службы.</span><span class="sxs-lookup"><span data-stu-id="e3cd3-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="e3cd3-119">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e3cd3-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: String
Parameter Sets: CertificateFilePath
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3cd3-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="e3cd3-120">-CertificatePassword</span></span>
<span data-ttu-id="e3cd3-121">Указывает пароль сертификата, который будет использоваться для проверки подлинности в качестве субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="e3cd3-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="e3cd3-122">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e3cd3-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3cd3-123">-Config</span><span class="sxs-lookup"><span data-stu-id="e3cd3-123">-Config</span></span>
<span data-ttu-id="e3cd3-124">Указывает объект конфигурации кластера HDInsight, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e3cd3-124">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="e3cd3-125">Этот объект создается командлетом New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="e3cd3-125">This object is created by the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3cd3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3cd3-126">-DefaultProfile</span></span>
<span data-ttu-id="e3cd3-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e3cd3-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3cd3-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e3cd3-128">-ObjectId</span></span>
<span data-ttu-id="e3cd3-129">Указывает идентификатор объекта Azure AD (GUID) субъекта-службы Azure AD, который представляет этот кластер.</span><span class="sxs-lookup"><span data-stu-id="e3cd3-129">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="e3cd3-130">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e3cd3-130">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3cd3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3cd3-131">CommonParameters</span></span>
<span data-ttu-id="e3cd3-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e3cd3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3cd3-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3cd3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3cd3-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e3cd3-134">INPUTS</span></span>

### <span data-ttu-id="e3cd3-135">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="e3cd3-135">AzureHDInsightConfig</span></span>
<span data-ttu-id="e3cd3-136">Параметр config принимает значение типа "AzureHDInsightConfig" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e3cd3-136">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

### <span data-ttu-id="e3cd3-137">GUID</span><span class="sxs-lookup"><span data-stu-id="e3cd3-137">Guid</span></span>
<span data-ttu-id="e3cd3-138">Параметр "ObjectId" принимает значение типа "GUID" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e3cd3-138">Parameter 'ObjectId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="e3cd3-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3cd3-139">OUTPUTS</span></span>

### <span data-ttu-id="e3cd3-140">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="e3cd3-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="e3cd3-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="e3cd3-141">NOTES</span></span>

## <span data-ttu-id="e3cd3-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3cd3-142">RELATED LINKS</span></span>

[<span data-ttu-id="e3cd3-143">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="e3cd3-143">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)

