---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87966f8ac96ab70f7617f857d9f1d83945b5e639
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555824"
---
# <span data-ttu-id="2d487-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2d487-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="2d487-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d487-102">SYNOPSIS</span></span>
<span data-ttu-id="2d487-103">Получение списка всех подсистем балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="2d487-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="2d487-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d487-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="2d487-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d487-105">DESCRIPTION</span></span>
<span data-ttu-id="2d487-106">Получение списка всех подсистем балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="2d487-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="2d487-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d487-107">EXAMPLES</span></span>

### <span data-ttu-id="2d487-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2d487-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsLoadBalancer
```

<span data-ttu-id="2d487-109">Получение списка всех подсистем балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="2d487-109">Get a list of all load balancers.</span></span>

## <span data-ttu-id="2d487-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d487-110">PARAMETERS</span></span>

### <span data-ttu-id="2d487-111">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="2d487-111">-Filter</span></span>
<span data-ttu-id="2d487-112">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="2d487-112">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d487-113">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="2d487-113">-InlineCount</span></span>
<span data-ttu-id="2d487-114">Параметр "подсчет в строке" OData.</span><span class="sxs-lookup"><span data-stu-id="2d487-114">OData inline count parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d487-115">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="2d487-115">-OrderBy</span></span>
<span data-ttu-id="2d487-116">Параметр orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="2d487-116">OData orderBy parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d487-117">-Skip</span><span class="sxs-lookup"><span data-stu-id="2d487-117">-Skip</span></span>
<span data-ttu-id="2d487-118">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="2d487-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d487-119">-Top</span><span class="sxs-lookup"><span data-stu-id="2d487-119">-Top</span></span>
<span data-ttu-id="2d487-120">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="2d487-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="2d487-121">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="2d487-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d487-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d487-122">CommonParameters</span></span>
<span data-ttu-id="2d487-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2d487-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d487-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d487-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d487-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d487-125">INPUTS</span></span>

## <span data-ttu-id="2d487-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d487-126">OUTPUTS</span></span>

### <span data-ttu-id="2d487-127">Microsoft. AzureStack. Management. Networking. admin. Models.</span><span class="sxs-lookup"><span data-stu-id="2d487-127">Microsoft.AzureStack.Management.Network.Admin.Models.LoadBalancer</span></span>

## <span data-ttu-id="2d487-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d487-128">NOTES</span></span>

## <span data-ttu-id="2d487-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d487-129">RELATED LINKS</span></span>
