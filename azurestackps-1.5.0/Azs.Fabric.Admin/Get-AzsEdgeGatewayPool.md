---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67a49abc82ba1ec8d9411141d456b8f71f75600f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555168"
---
# <span data-ttu-id="16e77-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="16e77-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="16e77-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16e77-102">SYNOPSIS</span></span>
<span data-ttu-id="16e77-103">Возвращает объекты пула шлюзов в местоположении.</span><span class="sxs-lookup"><span data-stu-id="16e77-103">Returns gateway pool objects at a location.</span></span>

## <span data-ttu-id="16e77-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16e77-104">SYNTAX</span></span>

### <span data-ttu-id="16e77-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="16e77-105">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="16e77-106">Получить</span><span class="sxs-lookup"><span data-stu-id="16e77-106">Get</span></span>
```
Get-AzsEdgeGatewayPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="16e77-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="16e77-107">ResourceId</span></span>
```
Get-AzsEdgeGatewayPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="16e77-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16e77-108">DESCRIPTION</span></span>
<span data-ttu-id="16e77-109">Возвращает объекты пула Edge Gateway в местоположении.</span><span class="sxs-lookup"><span data-stu-id="16e77-109">Returns edge gateway pool objects at a location.</span></span>

## <span data-ttu-id="16e77-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16e77-110">EXAMPLES</span></span>

### <span data-ttu-id="16e77-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="16e77-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsEdgeGatewayPool
```

<span data-ttu-id="16e77-112">Получение списка всех пулов шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="16e77-112">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="16e77-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="16e77-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsEdgeGatewayPool -Name "AzS-Gwy01"
```

<span data-ttu-id="16e77-114">Получение пула шлюзов с определенным краем.</span><span class="sxs-lookup"><span data-stu-id="16e77-114">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="16e77-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16e77-115">PARAMETERS</span></span>

### <span data-ttu-id="16e77-116">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="16e77-116">-Filter</span></span>
<span data-ttu-id="16e77-117">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="16e77-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="16e77-118">-Location</span><span class="sxs-lookup"><span data-stu-id="16e77-118">-Location</span></span>
<span data-ttu-id="16e77-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="16e77-119">Location of the resource.</span></span>

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

### <span data-ttu-id="16e77-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="16e77-120">-Name</span></span>
<span data-ttu-id="16e77-121">Имя пула шлюзов Edge.</span><span class="sxs-lookup"><span data-stu-id="16e77-121">Name of the edge gateway pool.</span></span>

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

### <span data-ttu-id="16e77-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16e77-122">-ResourceGroupName</span></span>
<span data-ttu-id="16e77-123">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="16e77-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="16e77-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16e77-124">-ResourceId</span></span>
<span data-ttu-id="16e77-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="16e77-125">The resource id.</span></span>

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

### <span data-ttu-id="16e77-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="16e77-126">-Skip</span></span>
<span data-ttu-id="16e77-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="16e77-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="16e77-128">-Top</span><span class="sxs-lookup"><span data-stu-id="16e77-128">-Top</span></span>
<span data-ttu-id="16e77-129">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="16e77-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="16e77-130">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="16e77-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="16e77-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e77-131">CommonParameters</span></span>
<span data-ttu-id="16e77-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16e77-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e77-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16e77-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e77-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16e77-134">INPUTS</span></span>

## <span data-ttu-id="16e77-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16e77-135">OUTPUTS</span></span>

### <span data-ttu-id="16e77-136">Microsoft. AzureStack. Management. Fabric. admin. Models. EdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="16e77-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGatewayPool</span></span>

## <span data-ttu-id="16e77-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="16e77-137">NOTES</span></span>

## <span data-ttu-id="16e77-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16e77-138">RELATED LINKS</span></span>
