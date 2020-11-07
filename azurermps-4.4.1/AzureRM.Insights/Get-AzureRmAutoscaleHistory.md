---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A70F4C03-E842-45D5-9323-DC5B14B569F1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAutoscaleHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAutoscaleHistory.md
ms.openlocfilehash: 12907bc7dbe7507dd12dbda13f0eb2ca722eaec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569395"
---
# <span data-ttu-id="9a793-101">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="9a793-101">Get-AzureRmAutoscaleHistory</span></span>

## <span data-ttu-id="9a793-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9a793-102">SYNOPSIS</span></span>
<span data-ttu-id="9a793-103">Получает журнал автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="9a793-103">Gets the Autoscale history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a793-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9a793-104">SYNTAX</span></span>

```
Get-AzureRmAutoscaleHistory [-ResourceId <String>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Status <String>] [-Caller <String>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a793-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a793-105">DESCRIPTION</span></span>
<span data-ttu-id="9a793-106">Командлет **Get-AzureRmAutoscaleHistory** получает историю событий, связанных с параметром автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="9a793-106">The **Get-AzureRmAutoscaleHistory** cmdlet gets the history of events related to an Autoscale setting.</span></span>

## <span data-ttu-id="9a793-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9a793-107">EXAMPLES</span></span>

### <span data-ttu-id="9a793-108">Пример 1: получение всех событий, связанных с подпиской</span><span class="sxs-lookup"><span data-stu-id="9a793-108">Example 1: Get all events associated with a subscription</span></span>
```
PS C:\>Get-AzureRmAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -DetailedOutput
```

<span data-ttu-id="9a793-109">Эта команда получает все связанные с автомасштабированием события, связанные с текущей подпиской.</span><span class="sxs-lookup"><span data-stu-id="9a793-109">This command gets all of the Autoscale-related events associated with the current subscription.</span></span>

### <span data-ttu-id="9a793-110">Пример 2: GetAutoscaleHistory для определенного ресурса</span><span class="sxs-lookup"><span data-stu-id="9a793-110">Example 2: GetAutoscaleHistory for a particular resource</span></span>
```
PS C:\>Get-AzureRmAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -ResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS" -DetailedOutput
Authorization        : 
Caller               : Microsoft.Insights/autoscaleSettings
Claims               :  http://schemas.xmlsoap.org/ws/2005/05/identity/claims/spn: Microsoft.Insights/autoscaleSettings
CorrelationId        : ac5b03ca-05d4-4811-9c27-0314a145f785
Description          : The autoscale engine attempting to scale resource '/subscriptions/a93fb07c-6c93-40be-bf3b-4f0deb
                       a10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm'
                       from 1 instances count to 2 instances count. 
EventChannels        : Admin, Operation
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

<span data-ttu-id="9a793-111">Эта команда получает все события, связанные с автомасштабированием, связанные с определенным ресурсом, определяемым ИДЕНТИФИКАТОРом ресурса (по сути, ResourceUri).</span><span class="sxs-lookup"><span data-stu-id="9a793-111">This command gets all Autoscale-related events associated with a particular resource identified by the resource's ID (essentially, the ResourceUri).</span></span>

## <span data-ttu-id="9a793-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9a793-112">PARAMETERS</span></span>

### <span data-ttu-id="9a793-113">-Вызывающий абонент</span><span class="sxs-lookup"><span data-stu-id="9a793-113">-Caller</span></span>
<span data-ttu-id="9a793-114">Задает вызывающий абонент.</span><span class="sxs-lookup"><span data-stu-id="9a793-114">Specifies a caller.</span></span>

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

### <span data-ttu-id="9a793-115">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="9a793-115">-DetailedOutput</span></span>
<span data-ttu-id="9a793-116">Указывает на то, что эта операция включает подробный вывод.</span><span class="sxs-lookup"><span data-stu-id="9a793-116">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="9a793-117">Если этот параметр не указан, выводится сводка.</span><span class="sxs-lookup"><span data-stu-id="9a793-117">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="9a793-118">-EndTime</span><span class="sxs-lookup"><span data-stu-id="9a793-118">-EndTime</span></span>
<span data-ttu-id="9a793-119">Указывает время окончания запроса в местном времени.</span><span class="sxs-lookup"><span data-stu-id="9a793-119">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="9a793-120">Значение по умолчанию — текущее время.</span><span class="sxs-lookup"><span data-stu-id="9a793-120">The default is the current time.</span></span>

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

### <span data-ttu-id="9a793-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a793-121">-ResourceId</span></span>
<span data-ttu-id="9a793-122">Указывает идентификатор ресурса, с которым связан параметр автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="9a793-122">Specifies the resource ID to which the autoscale setting is associated.</span></span>

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

### <span data-ttu-id="9a793-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9a793-123">-StartTime</span></span>
<span data-ttu-id="9a793-124">Задает время начала запроса в местном времени.</span><span class="sxs-lookup"><span data-stu-id="9a793-124">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="9a793-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9a793-125">This parameter is optional.</span></span>
<span data-ttu-id="9a793-126">По умолчанию используется текущее местное время минус один час.</span><span class="sxs-lookup"><span data-stu-id="9a793-126">The default is the current local time minus one hour.</span></span>

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

### <span data-ttu-id="9a793-127">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="9a793-127">-Status</span></span>
<span data-ttu-id="9a793-128">Задает фильтр по состоянию.</span><span class="sxs-lookup"><span data-stu-id="9a793-128">Specifies a filter by status.</span></span>
<span data-ttu-id="9a793-129">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9a793-129">This parameter is optional.</span></span>
<span data-ttu-id="9a793-130">Ошибка — пустая строка (то есть фильтр отсутствует)</span><span class="sxs-lookup"><span data-stu-id="9a793-130">The fault is an empty string (i.e. no filter)</span></span>

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

### <span data-ttu-id="9a793-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a793-131">-DefaultProfile</span></span>
<span data-ttu-id="9a793-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a793-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a793-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a793-133">CommonParameters</span></span>
<span data-ttu-id="9a793-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9a793-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a793-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a793-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a793-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9a793-136">INPUTS</span></span>

## <span data-ttu-id="9a793-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a793-137">OUTPUTS</span></span>

### <span data-ttu-id="9a793-138">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Insights. OutputClasses. IPSEventData]</span><span class="sxs-lookup"><span data-stu-id="9a793-138">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSEventData]</span></span>

## <span data-ttu-id="9a793-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="9a793-139">NOTES</span></span>

## <span data-ttu-id="9a793-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a793-140">RELATED LINKS</span></span>

[<span data-ttu-id="9a793-141">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9a793-141">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="9a793-142">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9a793-142">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="9a793-143">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9a793-143">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)

