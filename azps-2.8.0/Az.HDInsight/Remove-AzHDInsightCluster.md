---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: e52d838f0aa7ce901b8099710b38f570d4285a4c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720814"
---
# <span data-ttu-id="e6cff-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e6cff-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="e6cff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6cff-102">SYNOPSIS</span></span>
<span data-ttu-id="e6cff-103">Удаляет указанный кластер HDInsight из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="e6cff-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="e6cff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6cff-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6cff-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6cff-105">DESCRIPTION</span></span>
<span data-ttu-id="e6cff-106">Командлет **Remove-AzHDInsightCluster** удаляет указанный кластер служб HDInsight из подписки.</span><span class="sxs-lookup"><span data-stu-id="e6cff-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="e6cff-107">Эта операция также удаляет все данные, хранящиеся в распределенной файловой системе Hadoop (HDFS) в кластере.</span><span class="sxs-lookup"><span data-stu-id="e6cff-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="e6cff-108">Данные, хранящиеся в связанной учетной записи хранилища Azure, не удаляются.</span><span class="sxs-lookup"><span data-stu-id="e6cff-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="e6cff-109">Данные, хранящиеся в внешних metastores, не удаляются.</span><span class="sxs-lookup"><span data-stu-id="e6cff-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="e6cff-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6cff-110">EXAMPLES</span></span>

### <span data-ttu-id="e6cff-111">Пример 1: Удаление кластера Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="e6cff-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="e6cff-112">Эта команда удаляет кластер с именем "-Hadoop-001".</span><span class="sxs-lookup"><span data-stu-id="e6cff-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="e6cff-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6cff-113">PARAMETERS</span></span>

### <span data-ttu-id="e6cff-114">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="e6cff-114">-ClusterName</span></span>
<span data-ttu-id="e6cff-115">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="e6cff-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="e6cff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6cff-116">-DefaultProfile</span></span>
<span data-ttu-id="e6cff-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e6cff-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cff-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6cff-118">-ResourceGroupName</span></span>
<span data-ttu-id="e6cff-119">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e6cff-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e6cff-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6cff-120">CommonParameters</span></span>
<span data-ttu-id="e6cff-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6cff-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6cff-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6cff-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6cff-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6cff-123">INPUTS</span></span>

### <span data-ttu-id="e6cff-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="e6cff-124">None</span></span>

## <span data-ttu-id="e6cff-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6cff-125">OUTPUTS</span></span>

### <span data-ttu-id="e6cff-126">Microsoft. Azure. Management. HDInsight. Models. ClusterGetResponse</span><span class="sxs-lookup"><span data-stu-id="e6cff-126">Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse</span></span>

## <span data-ttu-id="e6cff-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6cff-127">NOTES</span></span>

## <span data-ttu-id="e6cff-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6cff-128">RELATED LINKS</span></span>

[<span data-ttu-id="e6cff-129">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e6cff-129">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="e6cff-130">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e6cff-130">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)

