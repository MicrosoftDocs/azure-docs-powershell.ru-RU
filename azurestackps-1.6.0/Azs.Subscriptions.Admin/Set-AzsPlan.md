---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f03365a81fc53af14e3fc9e686504ef3e4387c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555675"
---
# <span data-ttu-id="b9f26-101">Set-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="b9f26-101">Set-AzsPlan</span></span>

## <span data-ttu-id="b9f26-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9f26-102">SYNOPSIS</span></span>
<span data-ttu-id="b9f26-103">Обновляет указанный план</span><span class="sxs-lookup"><span data-stu-id="b9f26-103">Updates the specified plan</span></span>

## <span data-ttu-id="b9f26-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9f26-104">SYNTAX</span></span>

### <span data-ttu-id="b9f26-105">Обновление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b9f26-105">Update (Default)</span></span>
```
Set-AzsPlan -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-QuotaIds <String[]>]
 [-SkuIds <String[]>] [-ExternalReferenceId <String>] [-Description <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9f26-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b9f26-106">InputObject</span></span>
```
Set-AzsPlan [-ResourceGroupName <String>] -InputObject <Plan> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9f26-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9f26-107">ResourceId</span></span>
```
Set-AzsPlan -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9f26-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9f26-108">DESCRIPTION</span></span>
<span data-ttu-id="b9f26-109">Обновляет указанный план</span><span class="sxs-lookup"><span data-stu-id="b9f26-109">Updates the specified plan</span></span>

## <span data-ttu-id="b9f26-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9f26-110">EXAMPLES</span></span>

### <span data-ttu-id="b9f26-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b9f26-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -Description "This plan is meant to be used by accounting only."
```

<span data-ttu-id="b9f26-112">Обновляет указанный план</span><span class="sxs-lookup"><span data-stu-id="b9f26-112">Updates the specified plan</span></span>

## <span data-ttu-id="b9f26-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9f26-113">PARAMETERS</span></span>

### <span data-ttu-id="b9f26-114">-Описание</span><span class="sxs-lookup"><span data-stu-id="b9f26-114">-Description</span></span>
<span data-ttu-id="b9f26-115">Описание плана.</span><span class="sxs-lookup"><span data-stu-id="b9f26-115">Description of the plan.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f26-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b9f26-116">-DisplayName</span></span>
<span data-ttu-id="b9f26-117">Отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="b9f26-117">Display name.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f26-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="b9f26-118">-ExternalReferenceId</span></span>
<span data-ttu-id="b9f26-119">Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="b9f26-119">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f26-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9f26-120">-InputObject</span></span>
<span data-ttu-id="b9f26-121">Входной объект типа Microsoft. AzureStack. Management. Subscriptions. admin. Models. Plan.</span><span class="sxs-lookup"><span data-stu-id="b9f26-121">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan.</span></span>

```yaml
Type: Plan
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9f26-122">-Location</span><span class="sxs-lookup"><span data-stu-id="b9f26-122">-Location</span></span>
<span data-ttu-id="b9f26-123">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="b9f26-123">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f26-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b9f26-124">-Name</span></span>
<span data-ttu-id="b9f26-125">Название плана.</span><span class="sxs-lookup"><span data-stu-id="b9f26-125">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f26-126">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="b9f26-126">-QuotaIds</span></span>
<span data-ttu-id="b9f26-127">Идентификаторы квот в плане.</span><span class="sxs-lookup"><span data-stu-id="b9f26-127">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f26-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9f26-128">-ResourceGroupName</span></span>
<span data-ttu-id="b9f26-129">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="b9f26-129">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f26-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9f26-130">-ResourceId</span></span>
<span data-ttu-id="b9f26-131">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="b9f26-131">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9f26-132">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="b9f26-132">-SkuIds</span></span>
<span data-ttu-id="b9f26-133">Идентификаторы SKU.</span><span class="sxs-lookup"><span data-stu-id="b9f26-133">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f26-134">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="b9f26-134">-SubscriptionCount</span></span>
<span data-ttu-id="b9f26-135">Число подписок.</span><span class="sxs-lookup"><span data-stu-id="b9f26-135">Subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f26-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9f26-136">-Confirm</span></span>
<span data-ttu-id="b9f26-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b9f26-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f26-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9f26-138">-WhatIf</span></span>
<span data-ttu-id="b9f26-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b9f26-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9f26-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b9f26-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f26-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9f26-141">CommonParameters</span></span>
<span data-ttu-id="b9f26-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9f26-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9f26-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9f26-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9f26-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9f26-144">INPUTS</span></span>

## <span data-ttu-id="b9f26-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9f26-145">OUTPUTS</span></span>

### <span data-ttu-id="b9f26-146">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Plan</span><span class="sxs-lookup"><span data-stu-id="b9f26-146">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="b9f26-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9f26-147">NOTES</span></span>

## <span data-ttu-id="b9f26-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9f26-148">RELATED LINKS</span></span>
