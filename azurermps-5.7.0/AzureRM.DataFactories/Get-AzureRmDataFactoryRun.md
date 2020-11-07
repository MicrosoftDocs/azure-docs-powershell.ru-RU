---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryRun.md
ms.openlocfilehash: a430156dcd49e9bfd69766ab4cfe112c60aef549
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565524"
---
# <span data-ttu-id="4ffc0-101">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="4ffc0-101">Get-AzureRmDataFactoryRun</span></span>

## <span data-ttu-id="4ffc0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ffc0-102">SYNOPSIS</span></span>
<span data-ttu-id="4ffc0-103">Вызывается для среза данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-103">Gets runs for a data slice of a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ffc0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ffc0-104">SYNTAX</span></span>

### <span data-ttu-id="4ffc0-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4ffc0-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ffc0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4ffc0-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ffc0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ffc0-107">DESCRIPTION</span></span>
<span data-ttu-id="4ffc0-108">Командлет **Get-AzureRmDataFactoryRun** возвращает выполнение для среза данных набора данных в службе фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-108">The **Get-AzureRmDataFactoryRun** cmdlet gets the runs for a data slice of a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="4ffc0-109">Набор данных в фабрике данных состоит из фрагментов на временной шкале.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-109">A dataset in a data factory is composed of slices over the time axis.</span></span>
<span data-ttu-id="4ffc0-110">Ширина среза определяется расписанием (ежечасно или ежедневно).</span><span class="sxs-lookup"><span data-stu-id="4ffc0-110">The width of a slice is determined by the schedule, either hourly or daily.</span></span>
<span data-ttu-id="4ffc0-111">Выполнение — это блок обработки для среза.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-111">A run is a unit of processing for a slice.</span></span>
<span data-ttu-id="4ffc0-112">Для среза может быть один или несколько запусков в случае повторных попыток или на случай, если вы перезапустите срез из-за сбоя.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-112">There could be one or more runs for a slice in case of retries or in case you rerun your slice due to failures.</span></span>
<span data-ttu-id="4ffc0-113">Срез определяется по времени начала.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-113">A slice is identified by its start time.</span></span>
<span data-ttu-id="4ffc0-114">Чтобы получить время начала среза, используйте командлет Get-AzureRmDataFactorySlice.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-114">To obtain the start time of a slice, use the Get-AzureRmDataFactorySlice cmdlet.</span></span>

<span data-ttu-id="4ffc0-115">Например, чтобы получить доступ к следующему фрагменту, используйте время запуска 2015-04-02T20:00:00.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-115">For example, to get a run for the following slice, use the start time 2015-04-02T20:00:00.</span></span>

<span data-ttu-id="4ffc0-116">ResourceGroupName: ADF DataFactoryName: SPDataFactory0924 DatasetName: MarketingCampaignEffectivenessBlobDataset Start: 5/2/2014 8:00:00 PM End: 5/3/2014 8:00:00 PM RetryCount: 0 состояние: готовый LatencyStatus:</span><span class="sxs-lookup"><span data-stu-id="4ffc0-116">ResourceGroupName  : ADF DataFactoryName : SPDataFactory0924 DatasetName : MarketingCampaignEffectivenessBlobDataset Start : 5/2/2014 8:00:00 PM End : 5/3/2014 8:00:00 PM RetryCount : 0 Status : Ready LatencyStatus :</span></span>

## <span data-ttu-id="4ffc0-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ffc0-117">EXAMPLES</span></span>

### <span data-ttu-id="4ffc0-118">Пример 1: получение набора данных</span><span class="sxs-lookup"><span data-stu-id="4ffc0-118">Example 1: Get a dataset</span></span>
```
PS C:\>Get-AzureRmDataFactoryRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z
Id                  : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ResourceGroupName   : ADF
DataFactoryName     : WikiADF
DatasetName           : DAWikiAggregatedData
PipelineName        : 249ea141-ca00-8597-fad9-a148e5e7bdba
ActivityId          : fcefe2bd-39b1-2d7a-7b35-bcc2b0432300
ResumptionToken     : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ContinuationToken   : 
ProcessingStartTime : 5/21/2014 5:02:41 PM
ProcessingEndTime   : 5/21/2014 5:04:12 PM
PercentComplete     : 100
DataSliceStart      : 5/21/2014 4:00:00 PM
DataSliceEnd        : 5/21/2014 5:00:00 PM
Status              : Succeeded
Timestamp           : 5/21/2014 5:02:41 PM
RetryAttempt        : 0
Properties          : {[errors, ]} 
ErrorMessage        :
```

<span data-ttu-id="4ffc0-119">Эта команда возвращает "все" для фрагментов набора данных с именем DAWikiAggregatedData в фабрике данных с именем WikiADF, которая начинается с 4 PM GMT на 05/21/2014.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-119">This command gets all runs for slices of the dataset named DAWikiAggregatedData in the data factory named WikiADF that start from 4 PM GMT on 05/21/2014.</span></span>

## <span data-ttu-id="4ffc0-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ffc0-120">PARAMETERS</span></span>

### <span data-ttu-id="4ffc0-121">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-121">-DataFactory</span></span>
<span data-ttu-id="4ffc0-122">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="4ffc0-122">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="4ffc0-123">Этот командлет запускается для фрагментов, относящихся к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-123">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ffc0-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4ffc0-124">-DataFactoryName</span></span>
<span data-ttu-id="4ffc0-125">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-125">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4ffc0-126">Этот командлет запускается для фрагментов, относящихся к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-126">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ffc0-127">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="4ffc0-127">-DatasetName</span></span>
<span data-ttu-id="4ffc0-128">Указывает имя набора данных.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-128">Specifies the name of the dataset.</span></span>
<span data-ttu-id="4ffc0-129">Этот командлет запускается для фрагментов, относящихся к набору данных, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-129">This cmdlet gets runs for slices that belong to the dataset that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ffc0-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ffc0-130">-DefaultProfile</span></span>
<span data-ttu-id="4ffc0-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4ffc0-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ffc0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ffc0-132">-ResourceGroupName</span></span>
<span data-ttu-id="4ffc0-133">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4ffc0-134">Этот командлет получает заводские запуски для фрагментов, принадлежащих к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-134">This cmdlet gets factory runs for slices that belong to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ffc0-135">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="4ffc0-135">-StartDateTime</span></span>
<span data-ttu-id="4ffc0-136">Задает начало периода времени в качестве объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="4ffc0-136">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="4ffc0-137">Этот командлет запускается для срезов данных, которые соответствуют этому периоду времени.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-137">This cmdlet gets runs for the data slices that match this time period.</span></span>

<span data-ttu-id="4ffc0-138">*StartDateTime* должен быть указан в формате ISO8601, как показано в следующих примерах:</span><span class="sxs-lookup"><span data-stu-id="4ffc0-138">*StartDateTime* must be specified in the ISO8601 format, as in the following examples:</span></span> 

<span data-ttu-id="4ffc0-139">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (тихоокеанское стандартное время)</span><span class="sxs-lookup"><span data-stu-id="4ffc0-139">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="4ffc0-140">Обозначение часового пояса по умолчанию — UTC.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-140">The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="4ffc0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ffc0-141">CommonParameters</span></span>
<span data-ttu-id="4ffc0-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ffc0-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ffc0-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ffc0-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ffc0-144">INPUTS</span></span>

### <span data-ttu-id="4ffc0-145">Ничего</span><span class="sxs-lookup"><span data-stu-id="4ffc0-145">None</span></span>
<span data-ttu-id="4ffc0-146">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="4ffc0-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4ffc0-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ffc0-147">OUTPUTS</span></span>

### <span data-ttu-id="4ffc0-148">System. Collections. Generic. List ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataSliceRun, Microsoft. WindowsAzure. Commands. Utilities, Version = 0.8.2.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="4ffc0-148">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataSliceRun, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="4ffc0-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ffc0-149">NOTES</span></span>
* <span data-ttu-id="4ffc0-150">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="4ffc0-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4ffc0-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ffc0-151">RELATED LINKS</span></span>

[<span data-ttu-id="4ffc0-152">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="4ffc0-152">Get-AzureRmDataFactorySlice</span></span>](./Get-AzureRmDataFactorySlice.md)

