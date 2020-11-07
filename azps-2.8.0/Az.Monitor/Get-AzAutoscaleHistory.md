---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A70F4C03-E842-45D5-9323-DC5B14B569F1
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azautoscalehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAutoscaleHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAutoscaleHistory.md
ms.openlocfilehash: aa3c05be1aa62916ad0cf85fafcabb91fb97ff4c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720326"
---
# <span data-ttu-id="86a2a-101">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="86a2a-101">Get-AzAutoscaleHistory</span></span>

## <span data-ttu-id="86a2a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="86a2a-102">SYNOPSIS</span></span>
<span data-ttu-id="86a2a-103">Получает журнал автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="86a2a-103">Gets the Autoscale history.</span></span>

## <span data-ttu-id="86a2a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="86a2a-104">SYNTAX</span></span>

```
Get-AzAutoscaleHistory [-ResourceId <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>]
 [-Caller <String>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86a2a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86a2a-105">DESCRIPTION</span></span>
<span data-ttu-id="86a2a-106">Командлет **Get-AzAutoscaleHistory** получает историю событий, связанных с параметром автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="86a2a-106">The **Get-AzAutoscaleHistory** cmdlet gets the history of events related to an Autoscale setting.</span></span>

## <span data-ttu-id="86a2a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="86a2a-107">EXAMPLES</span></span>

### <span data-ttu-id="86a2a-108">Пример 1: получение всех событий, связанных с подпиской</span><span class="sxs-lookup"><span data-stu-id="86a2a-108">Example 1: Get all events associated with a subscription</span></span>
```
PS C:\>Get-AzAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -DetailedOutput
```

<span data-ttu-id="86a2a-109">Эта команда получает все связанные с автомасштабированием события, связанные с текущей подпиской.</span><span class="sxs-lookup"><span data-stu-id="86a2a-109">This command gets all of the Autoscale-related events associated with the current subscription.</span></span>

### <span data-ttu-id="86a2a-110">Пример 2: GetAutoscaleHistory для определенного ресурса</span><span class="sxs-lookup"><span data-stu-id="86a2a-110">Example 2: GetAutoscaleHistory for a particular resource</span></span>
```
PS C:\>Get-AzAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -ResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS" -DetailedOutput
Authorization        : 
Caller               : Microsoft.Insights/autoscaleSettings
Claims               :  http://schemas.xmlsoap.org/ws/2005/05/identity/claims/spn: Microsoft.Insights/autoscaleSettings
CorrelationId        : ac5b03ca-05d4-4811-9c27-0314a145f785
Description          : The autoscale engine attempting to scale resource '/subscriptions/a93fb07c-6c93-40be-bf3b-4f0deb
                       a10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm'
                       from 1 instances count to 2 instances count. 
EventDataId          : c554f7ed-514c-449c-9338-13e15b4b56a3
EventName            : AutoscaleAction
EventSource          : microsoft.insights/autoscalesettings
EventTimestamp       : 2/10/2015 2:38:19 AM
HttpRequest          : 
Id                   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS/events/c554f7ed-514c-4
                       49c-9338-13e15b4b56a3/ticks/635591326997519815
Level                : Informational
OperationId          : ac5b03ca-05d4-4811-9c27-0314a145f785
OperationName        : ScaleUp
Properties           : 
Description    : The autoscale engine attempting to scale resource '/subscriptions/a93fb07c-6c93
                       -40be-bf3b-4f0deba10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/De
                       faultServerFarm' from 1 instances count to 2 instances count. 
ResourceName   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-
                       EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
OldInstancesCount: 1
NewInstancesCount: 2
ActiveAutoscaleProfile: {
                         "Name": "No scheduled times",
                         "Capacity": {
                           "Minimum": "1",
                           "Maximum": "3",
                           "Default": "1"
                         },
                         "Rules": [
                           {
                             "MetricTrigger": {
                               "Name": "CpuPercentage",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT45M",
                               "TimeAggregation": "Average",
                               "Operator": "GreaterThanOrEqual",
                               "Threshold": 14.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Increase",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT5M"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "CpuPercentage",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT45M",
                               "TimeAggregation": "Average",
                               "Operator": "LessThanOrEqual",
                               "Threshold": 4.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Decrease",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT2H"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "BytesReceived",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT10M",
                               "TimeAggregation": "Average",
                               "Operator": "LessThanOrEqual",
                               "Threshold": 50.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Decrease",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT10M"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "BytesReceived",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT5M",
                               "TimeAggregation": "Average",
                               "Operator": "GreaterThanOrEqual",
                               "Threshold": 100.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Increase",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT10M"
                             }
                           }
                         ] 
                       }
ResourceGroupName    : Default-Web-EastUS
ResourceProviderName : microsoft.insights
ResourceId           : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS
Status               : Succeeded
SubmissionTimestamp  : 2/10/2015 2:38:19 AM
SubscriptionId       : b93fb07a-6f93-30be-bf3e-4f0deca15f4f
SubStatus            :
```

<span data-ttu-id="86a2a-111">Эта команда получает все события, связанные с автомасштабированием, связанные с определенным ресурсом, определяемым ИДЕНТИФИКАТОРом ресурса (по сути, ResourceUri).</span><span class="sxs-lookup"><span data-stu-id="86a2a-111">This command gets all Autoscale-related events associated with a particular resource identified by the resource's ID (essentially, the ResourceUri).</span></span>

## <span data-ttu-id="86a2a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="86a2a-112">PARAMETERS</span></span>

### <span data-ttu-id="86a2a-113">-Вызывающий абонент</span><span class="sxs-lookup"><span data-stu-id="86a2a-113">-Caller</span></span>
<span data-ttu-id="86a2a-114">Задает вызывающий абонент.</span><span class="sxs-lookup"><span data-stu-id="86a2a-114">Specifies a caller.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86a2a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86a2a-115">-DefaultProfile</span></span>
<span data-ttu-id="86a2a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="86a2a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86a2a-117">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="86a2a-117">-DetailedOutput</span></span>
<span data-ttu-id="86a2a-118">Указывает на то, что эта операция включает подробный вывод.</span><span class="sxs-lookup"><span data-stu-id="86a2a-118">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="86a2a-119">Если этот параметр не указан, выводится сводка.</span><span class="sxs-lookup"><span data-stu-id="86a2a-119">If you do not specify this parameter, the output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86a2a-120">-EndTime</span><span class="sxs-lookup"><span data-stu-id="86a2a-120">-EndTime</span></span>
<span data-ttu-id="86a2a-121">Указывает время окончания запроса в местном времени.</span><span class="sxs-lookup"><span data-stu-id="86a2a-121">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="86a2a-122">Значение по умолчанию — текущее время.</span><span class="sxs-lookup"><span data-stu-id="86a2a-122">The default is the current time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86a2a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86a2a-123">-ResourceId</span></span>
<span data-ttu-id="86a2a-124">Указывает идентификатор ресурса, с которым связан параметр автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="86a2a-124">Specifies the resource ID to which the autoscale setting is associated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86a2a-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="86a2a-125">-StartTime</span></span>
<span data-ttu-id="86a2a-126">Задает время начала запроса в местном времени.</span><span class="sxs-lookup"><span data-stu-id="86a2a-126">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="86a2a-127">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="86a2a-127">This parameter is optional.</span></span>
<span data-ttu-id="86a2a-128">По умолчанию используется текущее местное время минус один час.</span><span class="sxs-lookup"><span data-stu-id="86a2a-128">The default is the current local time minus one hour.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86a2a-129">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="86a2a-129">-Status</span></span>
<span data-ttu-id="86a2a-130">Задает фильтр по состоянию.</span><span class="sxs-lookup"><span data-stu-id="86a2a-130">Specifies a filter by status.</span></span>
<span data-ttu-id="86a2a-131">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="86a2a-131">This parameter is optional.</span></span>
<span data-ttu-id="86a2a-132">Ошибка — пустая строка (то есть фильтр отсутствует)</span><span class="sxs-lookup"><span data-stu-id="86a2a-132">The fault is an empty string (i.e. no filter)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86a2a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86a2a-133">CommonParameters</span></span>
<span data-ttu-id="86a2a-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="86a2a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86a2a-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86a2a-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86a2a-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="86a2a-136">INPUTS</span></span>

### <span data-ttu-id="86a2a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="86a2a-137">System.String</span></span>

### <span data-ttu-id="86a2a-138">System. Nullable "1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="86a2a-138">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="86a2a-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="86a2a-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="86a2a-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="86a2a-140">OUTPUTS</span></span>

### <span data-ttu-id="86a2a-141">Microsoft. Azure. Commands. Insights. OutputClasses. PSEventData</span><span class="sxs-lookup"><span data-stu-id="86a2a-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="86a2a-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="86a2a-142">NOTES</span></span>

## <span data-ttu-id="86a2a-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86a2a-143">RELATED LINKS</span></span>

[<span data-ttu-id="86a2a-144">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="86a2a-144">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="86a2a-145">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="86a2a-145">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="86a2a-146">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="86a2a-146">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)

