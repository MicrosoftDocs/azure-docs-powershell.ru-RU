---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac33f0feae7d54798753637f8f7898ab796f0939
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555920"
---
# <span data-ttu-id="cf46a-101">Get-AzsQueueServiceMetric</span><span class="sxs-lookup"><span data-stu-id="cf46a-101">Get-AzsQueueServiceMetric</span></span>

## <span data-ttu-id="cf46a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf46a-102">SYNOPSIS</span></span>
<span data-ttu-id="cf46a-103">Возвращает список метрик для службы очереди.</span><span class="sxs-lookup"><span data-stu-id="cf46a-103">Returns a list of metrics for the queue service.</span></span>

## <span data-ttu-id="cf46a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf46a-104">SYNTAX</span></span>

```
Get-AzsQueueServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf46a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf46a-105">DESCRIPTION</span></span>
<span data-ttu-id="cf46a-106">Возвращает список метрик для службы очереди.</span><span class="sxs-lookup"><span data-stu-id="cf46a-106">Returns a list of metrics for the queue service.</span></span>

## <span data-ttu-id="cf46a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf46a-107">EXAMPLES</span></span>

### <span data-ttu-id="cf46a-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cf46a-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsQueueServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="cf46a-109">Получите список метрик для службы очереди.</span><span class="sxs-lookup"><span data-stu-id="cf46a-109">Get the list of metrics for queue service.</span></span>

## <span data-ttu-id="cf46a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf46a-110">PARAMETERS</span></span>

### <span data-ttu-id="cf46a-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="cf46a-111">-FarmName</span></span>
<span data-ttu-id="cf46a-112">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="cf46a-112">Farm Id.</span></span>

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

### <span data-ttu-id="cf46a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf46a-113">-ResourceGroupName</span></span>
<span data-ttu-id="cf46a-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cf46a-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf46a-115">-Skip</span><span class="sxs-lookup"><span data-stu-id="cf46a-115">-Skip</span></span>
<span data-ttu-id="cf46a-116">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="cf46a-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="cf46a-117">-Top</span><span class="sxs-lookup"><span data-stu-id="cf46a-117">-Top</span></span>
<span data-ttu-id="cf46a-118">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="cf46a-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="cf46a-119">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="cf46a-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="cf46a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf46a-120">CommonParameters</span></span>
<span data-ttu-id="cf46a-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf46a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf46a-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf46a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf46a-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf46a-123">INPUTS</span></span>

## <span data-ttu-id="cf46a-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf46a-124">OUTPUTS</span></span>

### <span data-ttu-id="cf46a-125">Microsoft. AzureStack. Management. Storage. admin. Models. Metric</span><span class="sxs-lookup"><span data-stu-id="cf46a-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="cf46a-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf46a-126">NOTES</span></span>

## <span data-ttu-id="cf46a-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf46a-127">RELATED LINKS</span></span>
