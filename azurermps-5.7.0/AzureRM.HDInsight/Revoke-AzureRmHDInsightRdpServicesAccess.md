---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/revoke-azurermhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: 32664beb1ffe7600756953294b1ec33f7d1d54ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567006"
---
# <span data-ttu-id="461c8-101">Revoke-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="461c8-101">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="461c8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="461c8-102">SYNOPSIS</span></span>
<span data-ttu-id="461c8-103">Запрещает RDP-доступ к кластеру Windows.</span><span class="sxs-lookup"><span data-stu-id="461c8-103">Disables RDP access to a Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="461c8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="461c8-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="461c8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="461c8-105">DESCRIPTION</span></span>
<span data-ttu-id="461c8-106">Командлет **REVOKE-AzureRmHDInsightRdpServicesAccess** отключает доступ к протоколу удаленного рабочего стола (RDP) к кластеру Azure HDInsight на базе Windows.</span><span class="sxs-lookup"><span data-stu-id="461c8-106">The **Revoke-AzureRmHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="461c8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="461c8-107">EXAMPLES</span></span>

### <span data-ttu-id="461c8-108">Пример 1: отключение доступа к указанному кластеру через RDP</span><span class="sxs-lookup"><span data-stu-id="461c8-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="461c8-109">Эта команда запрещает доступ по протоколу RDP к кластеру с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="461c8-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="461c8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="461c8-110">PARAMETERS</span></span>

### <span data-ttu-id="461c8-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="461c8-111">-ClusterName</span></span>
<span data-ttu-id="461c8-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="461c8-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="461c8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="461c8-113">-DefaultProfile</span></span>
<span data-ttu-id="461c8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="461c8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="461c8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="461c8-115">-ResourceGroupName</span></span>
<span data-ttu-id="461c8-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="461c8-116">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="461c8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="461c8-117">CommonParameters</span></span>
<span data-ttu-id="461c8-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="461c8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="461c8-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="461c8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="461c8-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="461c8-120">INPUTS</span></span>

### <span data-ttu-id="461c8-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="461c8-121">None</span></span>
<span data-ttu-id="461c8-122">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="461c8-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="461c8-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="461c8-123">OUTPUTS</span></span>

### <span data-ttu-id="461c8-124">System. void</span><span class="sxs-lookup"><span data-stu-id="461c8-124">System.Void</span></span>

## <span data-ttu-id="461c8-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="461c8-125">NOTES</span></span>

## <span data-ttu-id="461c8-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="461c8-126">RELATED LINKS</span></span>

[<span data-ttu-id="461c8-127">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="461c8-127">Grant-AzureRmHDInsightRdpServicesAccess</span></span>](./Grant-AzureRmHDInsightRdpServicesAccess.md)

