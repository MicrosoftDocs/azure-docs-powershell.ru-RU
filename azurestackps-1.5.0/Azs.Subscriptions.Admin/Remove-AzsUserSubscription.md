---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d76356e99419ff345e2eccc025c91637417de1a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555487"
---
# <span data-ttu-id="1d88f-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="1d88f-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="1d88f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1d88f-102">SYNOPSIS</span></span>
<span data-ttu-id="1d88f-103">Удаляет указанную подписку клиента.</span><span class="sxs-lookup"><span data-stu-id="1d88f-103">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="1d88f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1d88f-104">SYNTAX</span></span>

```
Remove-AzsUserSubscription [-SubscriptionId] <Guid> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d88f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d88f-105">DESCRIPTION</span></span>
<span data-ttu-id="1d88f-106">Удаляет указанную подписку клиента.</span><span class="sxs-lookup"><span data-stu-id="1d88f-106">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="1d88f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1d88f-107">EXAMPLES</span></span>

### <span data-ttu-id="1d88f-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1d88f-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="1d88f-109">Удалите указанную подписку клиента.</span><span class="sxs-lookup"><span data-stu-id="1d88f-109">Remove the specified tenant subscription.</span></span>

## <span data-ttu-id="1d88f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1d88f-110">PARAMETERS</span></span>

### <span data-ttu-id="1d88f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="1d88f-111">-Force</span></span>
<span data-ttu-id="1d88f-112">Пометка для удаления элемента без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1d88f-112">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="1d88f-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1d88f-113">-SubscriptionId</span></span>
<span data-ttu-id="1d88f-114">Параметр идентификатора подписки.</span><span class="sxs-lookup"><span data-stu-id="1d88f-114">Subscription Id parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d88f-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d88f-115">-Confirm</span></span>
<span data-ttu-id="1d88f-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1d88f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d88f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d88f-117">-WhatIf</span></span>
<span data-ttu-id="1d88f-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1d88f-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d88f-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1d88f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d88f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d88f-120">CommonParameters</span></span>
<span data-ttu-id="1d88f-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1d88f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d88f-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d88f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d88f-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1d88f-123">INPUTS</span></span>

## <span data-ttu-id="1d88f-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d88f-124">OUTPUTS</span></span>

## <span data-ttu-id="1d88f-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="1d88f-125">NOTES</span></span>

## <span data-ttu-id="1d88f-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d88f-126">RELATED LINKS</span></span>
