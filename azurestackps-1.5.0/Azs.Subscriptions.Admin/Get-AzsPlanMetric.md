---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cadf5ad37119ab6b50191e50e8ec281fe4bce2d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555279"
---
# <span data-ttu-id="f828f-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="f828f-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="f828f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f828f-102">SYNOPSIS</span></span>
<span data-ttu-id="f828f-103">Получение метрик плана.</span><span class="sxs-lookup"><span data-stu-id="f828f-103">Get the plan metrics.</span></span>

## <span data-ttu-id="f828f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f828f-104">SYNTAX</span></span>

```
Get-AzsPlanMetric [-ResourceGroupName] <String> [-PlanName] <String> [<CommonParameters>]
```

## <span data-ttu-id="f828f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f828f-105">DESCRIPTION</span></span>
<span data-ttu-id="f828f-106">Получение метрик плана.</span><span class="sxs-lookup"><span data-stu-id="f828f-106">Get the plan metrics.</span></span>

## <span data-ttu-id="f828f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f828f-107">EXAMPLES</span></span>

### <span data-ttu-id="f828f-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f828f-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlanMetric -ResourceGroupName rg1 -PlanName plan1
```

<span data-ttu-id="f828f-109">Получение метрик плана.</span><span class="sxs-lookup"><span data-stu-id="f828f-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="f828f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f828f-110">PARAMETERS</span></span>

### <span data-ttu-id="f828f-111">-PlanName</span><span class="sxs-lookup"><span data-stu-id="f828f-111">-PlanName</span></span>
<span data-ttu-id="f828f-112">Название плана.</span><span class="sxs-lookup"><span data-stu-id="f828f-112">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f828f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f828f-113">-ResourceGroupName</span></span>
<span data-ttu-id="f828f-114">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="f828f-114">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f828f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f828f-115">CommonParameters</span></span>
<span data-ttu-id="f828f-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f828f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f828f-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f828f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f828f-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f828f-118">INPUTS</span></span>

## <span data-ttu-id="f828f-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f828f-119">OUTPUTS</span></span>

### <span data-ttu-id="f828f-120">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="f828f-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="f828f-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="f828f-121">NOTES</span></span>

## <span data-ttu-id="f828f-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f828f-122">RELATED LINKS</span></span>
