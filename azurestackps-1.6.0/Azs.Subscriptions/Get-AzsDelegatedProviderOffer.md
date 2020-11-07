---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8034887f8b44bef5c3dd59f73186027af1a1e5eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555668"
---
# <span data-ttu-id="92010-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="92010-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="92010-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92010-102">SYNOPSIS</span></span>
<span data-ttu-id="92010-103">Получение списка предложенных для указанного поставщика делегированных данных.</span><span class="sxs-lookup"><span data-stu-id="92010-103">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="92010-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92010-104">SYNTAX</span></span>

### <span data-ttu-id="92010-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="92010-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="92010-106">Получить</span><span class="sxs-lookup"><span data-stu-id="92010-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -Name <String> -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="92010-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92010-107">DESCRIPTION</span></span>
<span data-ttu-id="92010-108">Получение списка предложенных для указанного поставщика делегированных данных.</span><span class="sxs-lookup"><span data-stu-id="92010-108">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="92010-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92010-109">EXAMPLES</span></span>

### <span data-ttu-id="92010-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="92010-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d | fl
```

<span data-ttu-id="92010-111">Получение списка предложенных для указанного поставщика делегированных данных.</span><span class="sxs-lookup"><span data-stu-id="92010-111">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="92010-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92010-112">PARAMETERS</span></span>

### <span data-ttu-id="92010-113">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="92010-113">-DelegatedProviderId</span></span>
<span data-ttu-id="92010-114">Идентификатор поставщика делегирования.</span><span class="sxs-lookup"><span data-stu-id="92010-114">Id of the delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92010-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="92010-115">-Name</span></span>
<span data-ttu-id="92010-116">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="92010-116">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: OfferName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92010-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="92010-117">-Skip</span></span>
<span data-ttu-id="92010-118">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="92010-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92010-119">-Top</span><span class="sxs-lookup"><span data-stu-id="92010-119">-Top</span></span>
<span data-ttu-id="92010-120">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="92010-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="92010-121">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="92010-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92010-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92010-122">CommonParameters</span></span>
<span data-ttu-id="92010-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92010-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92010-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92010-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92010-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92010-125">INPUTS</span></span>

## <span data-ttu-id="92010-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92010-126">OUTPUTS</span></span>

### <span data-ttu-id="92010-127">Microsoft. AzureStack. Management. Subscription. Models. Offer</span><span class="sxs-lookup"><span data-stu-id="92010-127">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="92010-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="92010-128">NOTES</span></span>

## <span data-ttu-id="92010-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92010-129">RELATED LINKS</span></span>
