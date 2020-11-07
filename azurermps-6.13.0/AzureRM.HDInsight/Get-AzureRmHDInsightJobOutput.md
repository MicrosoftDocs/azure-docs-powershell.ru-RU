---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightJobOutput.md
ms.openlocfilehash: 94bd90b644b12723a36266dea34d9b5e9417b45b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564492"
---
# <span data-ttu-id="8ca29-101">Get-AzureRmHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="8ca29-101">Get-AzureRmHDInsightJobOutput</span></span>

## <span data-ttu-id="8ca29-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ca29-102">SYNOPSIS</span></span>
<span data-ttu-id="8ca29-103">Получает выходные данные журнала для задания из учетной записи хранения, связанной с указанным кластером.</span><span class="sxs-lookup"><span data-stu-id="8ca29-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ca29-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ca29-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ca29-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ca29-105">DESCRIPTION</span></span>
<span data-ttu-id="8ca29-106">Командлет **Get-AzureRmHDInsightJobOutput** получает выходные данные журнала для задания из учетной записи хранения, связанной с кластером HDInsight Azure.</span><span class="sxs-lookup"><span data-stu-id="8ca29-106">The **Get-AzureRmHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="8ca29-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ca29-107">EXAMPLES</span></span>

### <span data-ttu-id="8ca29-108">Пример 1: получение выходных данных журнала для задания</span><span class="sxs-lookup"><span data-stu-id="8ca29-108">Example 1: Get the log output for a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "<status folder>"
PS C:\> $query = "<query here>"

PS C:\> New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzureRmHDInsightJobOutput `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="8ca29-109">Эта команда получает выходные данные журнала из кластера с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="8ca29-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="8ca29-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ca29-110">PARAMETERS</span></span>

### <span data-ttu-id="8ca29-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="8ca29-111">-ClusterName</span></span>
<span data-ttu-id="8ca29-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="8ca29-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca29-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="8ca29-113">-DefaultContainer</span></span>
<span data-ttu-id="8ca29-114">Указывает имя контейнера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8ca29-114">Specifies the default container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca29-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ca29-115">-DefaultProfile</span></span>
<span data-ttu-id="8ca29-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8ca29-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca29-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="8ca29-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="8ca29-118">Задает ключ учетной записи хранения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8ca29-118">Specifies the default Storage account key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca29-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8ca29-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="8ca29-120">Указывает имя учетной записи хранения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8ca29-120">Specifies the default Storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca29-121">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="8ca29-121">-DisplayOutputType</span></span>
<span data-ttu-id="8ca29-122">Задает запрашиваемый тип выходных данных задания.</span><span class="sxs-lookup"><span data-stu-id="8ca29-122">Specifies the job output type being requested.</span></span>
<span data-ttu-id="8ca29-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8ca29-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8ca29-124">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="8ca29-124">StandardOutput</span></span>
- <span data-ttu-id="8ca29-125">StandardError</span><span class="sxs-lookup"><span data-stu-id="8ca29-125">StandardError</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Job.JobDisplayOutputType
Parameter Sets: (All)
Aliases:
Accepted values: StandardOutput, StandardError

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca29-126">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="8ca29-126">-HttpCredential</span></span>
<span data-ttu-id="8ca29-127">Задает учетные данные для входа в кластер (HTTP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="8ca29-127">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca29-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="8ca29-128">-JobId</span></span>
<span data-ttu-id="8ca29-129">Указывает код задания, выходные данные которого будут выбираться.</span><span class="sxs-lookup"><span data-stu-id="8ca29-129">Specifies the job ID of the job whose output will be fetched.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca29-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ca29-130">-ResourceGroupName</span></span>
<span data-ttu-id="8ca29-131">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ca29-131">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca29-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ca29-132">CommonParameters</span></span>
<span data-ttu-id="8ca29-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ca29-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ca29-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ca29-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ca29-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ca29-135">INPUTS</span></span>

### <span data-ttu-id="8ca29-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="8ca29-136">None</span></span>

## <span data-ttu-id="8ca29-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ca29-137">OUTPUTS</span></span>

### <span data-ttu-id="8ca29-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8ca29-138">System.String</span></span>

## <span data-ttu-id="8ca29-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ca29-139">NOTES</span></span>

## <span data-ttu-id="8ca29-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ca29-140">RELATED LINKS</span></span>

[<span data-ttu-id="8ca29-141">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="8ca29-141">New-AzureRmHDInsightHiveJobDefinition</span></span>](./New-AzureRmHDInsightHiveJobDefinition.md)

[<span data-ttu-id="8ca29-142">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="8ca29-142">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)

