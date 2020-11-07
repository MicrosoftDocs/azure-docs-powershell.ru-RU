---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: fdceee36319d1c9ea950dbf5573b4ba0e3c614ee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555428"
---
# <span data-ttu-id="34b05-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="34b05-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="34b05-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="34b05-102">SYNOPSIS</span></span>
<span data-ttu-id="34b05-103">Удаление указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="34b05-103">Delete the specifed subscription.</span></span>

## <span data-ttu-id="34b05-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="34b05-104">SYNTAX</span></span>

```
Remove-AzsSubscription [-SubscriptionId] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34b05-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34b05-105">DESCRIPTION</span></span>
<span data-ttu-id="34b05-106">Удаление указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="34b05-106">Delete the specifed subscription.</span></span>

## <span data-ttu-id="34b05-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="34b05-107">EXAMPLES</span></span>

### <span data-ttu-id="34b05-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="34b05-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9
```

<span data-ttu-id="34b05-109">Удаление указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="34b05-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="34b05-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="34b05-110">PARAMETERS</span></span>

### <span data-ttu-id="34b05-111">-Force</span><span class="sxs-lookup"><span data-stu-id="34b05-111">-Force</span></span>
<span data-ttu-id="34b05-112">Удаление подписки без запроса</span><span class="sxs-lookup"><span data-stu-id="34b05-112">Remove subscription without prompting</span></span>

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

### <span data-ttu-id="34b05-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="34b05-113">-SubscriptionId</span></span>
<span data-ttu-id="34b05-114">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="34b05-114">Id of the subscription.</span></span>

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

### <span data-ttu-id="34b05-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34b05-115">-Confirm</span></span>
<span data-ttu-id="34b05-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="34b05-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34b05-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34b05-117">-WhatIf</span></span>
<span data-ttu-id="34b05-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="34b05-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34b05-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="34b05-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34b05-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34b05-120">CommonParameters</span></span>
<span data-ttu-id="34b05-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="34b05-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34b05-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34b05-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34b05-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="34b05-123">INPUTS</span></span>

## <span data-ttu-id="34b05-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="34b05-124">OUTPUTS</span></span>

## <span data-ttu-id="34b05-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="34b05-125">NOTES</span></span>

## <span data-ttu-id="34b05-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34b05-126">RELATED LINKS</span></span>
