---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchlocationquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
ms.openlocfilehash: 5c20529e174e37bd4d9d5d3f60b56c448206d09e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412988"
---
# <span data-ttu-id="a8db2-101">Get-AzBatchLocationQuota</span><span class="sxs-lookup"><span data-stu-id="a8db2-101">Get-AzBatchLocationQuota</span></span>

## <span data-ttu-id="a8db2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8db2-102">SYNOPSIS</span></span>
<span data-ttu-id="a8db2-103">Получает квоты пакетных служб для подписки в заданное расположение.</span><span class="sxs-lookup"><span data-stu-id="a8db2-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

## <span data-ttu-id="a8db2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a8db2-104">SYNTAX</span></span>

```
Get-AzBatchLocationQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8db2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8db2-105">DESCRIPTION</span></span>
<span data-ttu-id="a8db2-106">Возвращает квоты пакетных служб для указанной подписки в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="a8db2-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="a8db2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a8db2-107">EXAMPLES</span></span>

### <span data-ttu-id="a8db2-108">Пример 1. Получить квоты пакетных услуг для подписки в регионе "Запад США"</span><span class="sxs-lookup"><span data-stu-id="a8db2-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzBatchLocationQuota -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="a8db2-109">Эта команда получает квоты для текущей подписки в регионе "Запад США".</span><span class="sxs-lookup"><span data-stu-id="a8db2-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="a8db2-110">Возвращаемая стоимость указывает на то, что эта подписка может создать только одну пакетную учетную запись в этом регионе.</span><span class="sxs-lookup"><span data-stu-id="a8db2-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="a8db2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8db2-111">PARAMETERS</span></span>

### <span data-ttu-id="a8db2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8db2-112">-DefaultProfile</span></span>
<span data-ttu-id="a8db2-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a8db2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8db2-114">-Location</span><span class="sxs-lookup"><span data-stu-id="a8db2-114">-Location</span></span>
<span data-ttu-id="a8db2-115">Определяет регион, для которого этот cmdlet проверяет квоты.</span><span class="sxs-lookup"><span data-stu-id="a8db2-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="a8db2-116">Дополнительные сведения см. в области Azure ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="a8db2-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8db2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8db2-117">CommonParameters</span></span>
<span data-ttu-id="a8db2-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8db2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8db2-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8db2-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8db2-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8db2-120">INPUTS</span></span>

### <span data-ttu-id="a8db2-121">System.String</span><span class="sxs-lookup"><span data-stu-id="a8db2-121">System.String</span></span>

## <span data-ttu-id="a8db2-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a8db2-122">OUTPUTS</span></span>

### <span data-ttu-id="a8db2-123">Microsoft.Azure.Commands.Batch. Models.PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="a8db2-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="a8db2-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a8db2-124">NOTES</span></span>

## <span data-ttu-id="a8db2-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8db2-125">RELATED LINKS</span></span>