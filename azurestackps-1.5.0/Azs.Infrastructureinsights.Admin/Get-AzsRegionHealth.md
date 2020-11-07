---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b6713b912f962a7a85627ca2280d6195cc5c5d88
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555591"
---
# <span data-ttu-id="07727-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="07727-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="07727-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07727-102">SYNOPSIS</span></span>
<span data-ttu-id="07727-103">Возвращает список состояния работоспособности области.</span><span class="sxs-lookup"><span data-stu-id="07727-103">Returns a list of region's health status.</span></span>

## <span data-ttu-id="07727-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07727-104">SYNTAX</span></span>

### <span data-ttu-id="07727-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07727-105">List (Default)</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="07727-106">Получить</span><span class="sxs-lookup"><span data-stu-id="07727-106">Get</span></span>
```
Get-AzsRegionHealth [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="07727-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="07727-107">ResourceId</span></span>
```
Get-AzsRegionHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="07727-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07727-108">DESCRIPTION</span></span>
<span data-ttu-id="07727-109">Возвращает список состояния работоспособности области.</span><span class="sxs-lookup"><span data-stu-id="07727-109">Returns a list of region's health status.</span></span>

## <span data-ttu-id="07727-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07727-110">EXAMPLES</span></span>

### <span data-ttu-id="07727-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="07727-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRegionHealth
```

<span data-ttu-id="07727-112">Возвращает список состояния работоспособности области.</span><span class="sxs-lookup"><span data-stu-id="07727-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="07727-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07727-113">PARAMETERS</span></span>

### <span data-ttu-id="07727-114">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="07727-114">-Filter</span></span>
<span data-ttu-id="07727-115">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="07727-115">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07727-116">-Location</span><span class="sxs-lookup"><span data-stu-id="07727-116">-Location</span></span>
<span data-ttu-id="07727-117">Название региона</span><span class="sxs-lookup"><span data-stu-id="07727-117">Name of the region</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07727-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07727-118">-ResourceGroupName</span></span>
<span data-ttu-id="07727-119">Имя группы ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="07727-119">Resource group name which the resource resides.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07727-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07727-120">-ResourceId</span></span>
<span data-ttu-id="07727-121">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="07727-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07727-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="07727-122">-Skip</span></span>
<span data-ttu-id="07727-123">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="07727-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07727-124">-Top</span><span class="sxs-lookup"><span data-stu-id="07727-124">-Top</span></span>
<span data-ttu-id="07727-125">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="07727-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="07727-126">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="07727-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07727-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07727-127">CommonParameters</span></span>
<span data-ttu-id="07727-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07727-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07727-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07727-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07727-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07727-130">INPUTS</span></span>

## <span data-ttu-id="07727-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07727-131">OUTPUTS</span></span>

### <span data-ttu-id="07727-132">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. RegionHealth</span><span class="sxs-lookup"><span data-stu-id="07727-132">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.RegionHealth</span></span>

## <span data-ttu-id="07727-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="07727-133">NOTES</span></span>

## <span data-ttu-id="07727-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07727-134">RELATED LINKS</span></span>
