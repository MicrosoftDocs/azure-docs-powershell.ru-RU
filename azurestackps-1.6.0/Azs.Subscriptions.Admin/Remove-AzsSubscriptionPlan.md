---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b82dadf9a9e26b0023872378d41e4978e18436ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555684"
---
# <span data-ttu-id="fc9d4-101">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="fc9d4-101">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="fc9d4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fc9d4-102">SYNOPSIS</span></span>
<span data-ttu-id="fc9d4-103">Удаление плана подписки.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-103">Deletes a subscription plan.</span></span>

## <span data-ttu-id="fc9d4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fc9d4-104">SYNTAX</span></span>

### <span data-ttu-id="fc9d4-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fc9d4-105">Delete (Default)</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc9d4-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc9d4-106">ResourceId</span></span>
```
Remove-AzsSubscriptionPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc9d4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc9d4-107">DESCRIPTION</span></span>
<span data-ttu-id="fc9d4-108">Удаление плана подписки.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-108">Deletes a subscription plan.</span></span>

## <span data-ttu-id="fc9d4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fc9d4-109">EXAMPLES</span></span>

### <span data-ttu-id="fc9d4-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fc9d4-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="fc9d4-111">Удаление плана подписки.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-111">Delete a subscription plan.</span></span>

## <span data-ttu-id="fc9d4-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fc9d4-112">PARAMETERS</span></span>

### <span data-ttu-id="fc9d4-113">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="fc9d4-113">-AcquisitionId</span></span>
<span data-ttu-id="fc9d4-114">Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="fc9d4-114">The plan acquisition Identifier</span></span>

```yaml
Type: Guid
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc9d4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fc9d4-115">-Force</span></span>
<span data-ttu-id="fc9d4-116">Пометка для удаления элемента без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-116">Flag to remove the item without confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc9d4-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc9d4-117">-ResourceId</span></span>
<span data-ttu-id="fc9d4-118">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-118">The resource id.</span></span>

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

### <span data-ttu-id="fc9d4-119">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fc9d4-119">-TargetSubscriptionId</span></span>
<span data-ttu-id="fc9d4-120">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-120">The target subscription ID.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc9d4-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc9d4-121">-Confirm</span></span>
<span data-ttu-id="fc9d4-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc9d4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc9d4-123">-WhatIf</span></span>
<span data-ttu-id="fc9d4-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc9d4-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc9d4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc9d4-126">CommonParameters</span></span>
<span data-ttu-id="fc9d4-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc9d4-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc9d4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc9d4-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fc9d4-129">INPUTS</span></span>

## <span data-ttu-id="fc9d4-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc9d4-130">OUTPUTS</span></span>

## <span data-ttu-id="fc9d4-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="fc9d4-131">NOTES</span></span>

## <span data-ttu-id="fc9d4-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc9d4-132">RELATED LINKS</span></span>
