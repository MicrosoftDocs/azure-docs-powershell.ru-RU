---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/export-azurermloganalyticrequestratebyinterval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticRequestRateByInterval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Export-AzureRmLogAnalyticRequestRateByInterval.md
ms.openlocfilehash: b5e087bf42a2cb7f19980621c6dd0606471374d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564991"
---
# <span data-ttu-id="d2b2f-101">Export-AzureRmLogAnalyticRequestRateByInterval</span><span class="sxs-lookup"><span data-stu-id="d2b2f-101">Export-AzureRmLogAnalyticRequestRateByInterval</span></span>

## <span data-ttu-id="d2b2f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2b2f-102">SYNOPSIS</span></span>
<span data-ttu-id="d2b2f-103">Экспортируйте журналы, в которых на заданном временном экране отображаются запросы API, сделанные данной подпиской, чтобы показать действия по регулированию.</span><span class="sxs-lookup"><span data-stu-id="d2b2f-103">Export logs that show Api requests made by this subscription in the given time window to show throttling activities.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2b2f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2b2f-104">SYNTAX</span></span>

```
Export-AzureRmLogAnalyticRequestRateByInterval [-FromTime] <DateTime> [-GroupByOperationName]
 [-IntervalLength] <IntervalInMins> [-GroupByThrottlePolicy] [-BlobContainerSasUri] <String>
 [-GroupByResourceName] [-ToTime] <DateTime> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2b2f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2b2f-105">DESCRIPTION</span></span>
<span data-ttu-id="d2b2f-106">Это экспортирует Объединенные числа вызовов API Microsoft. COMPUTE, разделенных на успех, сбой или отрегулированный вывод в интервалах времени.</span><span class="sxs-lookup"><span data-stu-id="d2b2f-106">This exports aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled displayed in time intervals.</span></span>
<span data-ttu-id="d2b2f-107">Журналы можно дополнительно сгруппировать по трем параметрам: GroupByOperationName, GroupByThrottlePolicy или GroupByResourceName.</span><span class="sxs-lookup"><span data-stu-id="d2b2f-107">The logs can be further grouped by three parameters: GroupByOperationName, GroupByThrottlePolicy, or GroupByResourceName.</span></span>
<span data-ttu-id="d2b2f-108">Обратите внимание, что этот командлет собирает только CRP журналы.</span><span class="sxs-lookup"><span data-stu-id="d2b2f-108">Note that this cmdlet collects only CRP logs.</span></span>

## <span data-ttu-id="d2b2f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2b2f-109">EXAMPLES</span></span>

### <span data-ttu-id="d2b2f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d2b2f-110">Example 1</span></span>
```
PS C:\> Export-AzureRmLogAnalyticRequestRateByInterval -Location 'West Central US' -FromTime '2018-02-20T17:54:14.8806951-08:00' -ToTime '2018-02-22T17:54:17.5832413-08:00' -BlobContainerSasUri 'https://wkuotest1.blob.core.windows.net/mylogs?someSasUri' -IntervalLength ThirtyMins -GroupByOperationName
```

<span data-ttu-id="d2b2f-111">Эта команда хранит объединенные числа вызовов API Microsoft. COMPUTE, разделенных на успех, сбой или отрегулированный интервал между 2018-02-20T17:54:14 и 2018-02-22T17:54:17 в указанном URI SAS, агрегированный по имени операции.</span><span class="sxs-lookup"><span data-stu-id="d2b2f-111">This command stores the aggregated numbers of Microsoft.Compute API calls separated by Success, Failure, or Throttled between 2018-02-20T17:54:14 and 2018-02-22T17:54:17 in the given SAS URI, aggregated by operation name.</span></span>

## <span data-ttu-id="d2b2f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2b2f-112">PARAMETERS</span></span>

### <span data-ttu-id="d2b2f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2b2f-113">-AsJob</span></span>
<span data-ttu-id="d2b2f-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d2b2f-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b2f-115">-BlobContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="d2b2f-115">-BlobContainerSasUri</span></span>
<span data-ttu-id="d2b2f-116">Универсальный код ресурса (URI) SAS контейнера BLOB-объектов для ведения журнала, на который LogAnalytics API записывает выходные файлы.</span><span class="sxs-lookup"><span data-stu-id="d2b2f-116">SAS Uri of the logging blob container to which LogAnalytics Api writes output logs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b2f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2b2f-117">-DefaultProfile</span></span>
<span data-ttu-id="d2b2f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2b2f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b2f-119">-FromTime</span><span class="sxs-lookup"><span data-stu-id="d2b2f-119">-FromTime</span></span>
<span data-ttu-id="d2b2f-120">Время выполнения запроса</span><span class="sxs-lookup"><span data-stu-id="d2b2f-120">From time of the query</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b2f-121">-GroupByOperationName</span><span class="sxs-lookup"><span data-stu-id="d2b2f-121">-GroupByOperationName</span></span>
<span data-ttu-id="d2b2f-122">Результат запроса группировки по имени операции.</span><span class="sxs-lookup"><span data-stu-id="d2b2f-122">Group query result by Operation Name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b2f-123">-GroupByResourceName</span><span class="sxs-lookup"><span data-stu-id="d2b2f-123">-GroupByResourceName</span></span>
<span data-ttu-id="d2b2f-124">Результат запроса Group по названию ресурса.</span><span class="sxs-lookup"><span data-stu-id="d2b2f-124">Group query result by Resource Name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b2f-125">-GroupByThrottlePolicy</span><span class="sxs-lookup"><span data-stu-id="d2b2f-125">-GroupByThrottlePolicy</span></span>
<span data-ttu-id="d2b2f-126">Результаты запроса на группировку по политике регулирования.</span><span class="sxs-lookup"><span data-stu-id="d2b2f-126">Group query result by Throttle Policy applied.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b2f-127">-IntervalLength</span><span class="sxs-lookup"><span data-stu-id="d2b2f-127">-IntervalLength</span></span>
<span data-ttu-id="d2b2f-128">Интервал времени (в минутах), используемый для создания журналов LogAnalytics звонков.</span><span class="sxs-lookup"><span data-stu-id="d2b2f-128">Interval value in minutes used to create LogAnalytics call rate logs.</span></span>

```yaml
Type: IntervalInMins
Parameter Sets: (All)
Aliases:
Accepted values: ThreeMins, FiveMins, ThirtyMins, SixtyMins

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b2f-129">-Location</span><span class="sxs-lookup"><span data-stu-id="d2b2f-129">-Location</span></span>
<span data-ttu-id="d2b2f-130">Место, на которое запрашивается аналитический журнал.</span><span class="sxs-lookup"><span data-stu-id="d2b2f-130">The location upon which log analytic is queried.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2b2f-131">-ToTime</span><span class="sxs-lookup"><span data-stu-id="d2b2f-131">-ToTime</span></span>
<span data-ttu-id="d2b2f-132">Время запроса</span><span class="sxs-lookup"><span data-stu-id="d2b2f-132">To time of the query</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b2f-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2b2f-133">-Confirm</span></span>
<span data-ttu-id="d2b2f-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d2b2f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2b2f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2b2f-135">-WhatIf</span></span>
<span data-ttu-id="d2b2f-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d2b2f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2b2f-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d2b2f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2b2f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2b2f-138">CommonParameters</span></span>
<span data-ttu-id="d2b2f-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2b2f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2b2f-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2b2f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2b2f-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2b2f-141">INPUTS</span></span>

### <span data-ttu-id="d2b2f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d2b2f-142">System.String</span></span>

## <span data-ttu-id="d2b2f-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2b2f-143">OUTPUTS</span></span>

### <span data-ttu-id="d2b2f-144">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSLogAnalyticsOperationResult</span><span class="sxs-lookup"><span data-stu-id="d2b2f-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSLogAnalyticsOperationResult</span></span>

## <span data-ttu-id="d2b2f-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2b2f-145">NOTES</span></span>

## <span data-ttu-id="d2b2f-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2b2f-146">RELATED LINKS</span></span>