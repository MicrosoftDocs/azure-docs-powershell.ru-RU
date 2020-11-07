---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
ms.openlocfilehash: 77b12c17f46c9a04d1166b3066fa5ea9c2df1d74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557436"
---
# <span data-ttu-id="4cee3-101">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="4cee3-101">Get-AzureRmDataFactorySlice</span></span>

## <span data-ttu-id="4cee3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4cee3-102">SYNOPSIS</span></span>
<span data-ttu-id="4cee3-103">Получает срезы данных для набора данных в фабрике данных Azure.</span><span class="sxs-lookup"><span data-stu-id="4cee3-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cee3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4cee3-104">SYNTAX</span></span>

### <span data-ttu-id="4cee3-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4cee3-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4cee3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4cee3-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cee3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4cee3-107">DESCRIPTION</span></span>
<span data-ttu-id="4cee3-108">Командлет **Get-AzureRmDataFactorySlice** получает срезы данных для набора данных в службе фабрики данных Azure.</span><span class="sxs-lookup"><span data-stu-id="4cee3-108">The **Get-AzureRmDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="4cee3-109">Укажите время начала и время окончания, чтобы определить диапазон срезов данных для просмотра.</span><span class="sxs-lookup"><span data-stu-id="4cee3-109">Specify a start time and an end time to define a range of data slices to view.</span></span>

<span data-ttu-id="4cee3-110">Состояние среза данных — одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="4cee3-110">The status of a data slice is one of the following values:</span></span> 

- <span data-ttu-id="4cee3-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="4cee3-111">PendingExecution.</span></span>
<span data-ttu-id="4cee3-112">Обработка данных не начата.</span><span class="sxs-lookup"><span data-stu-id="4cee3-112">Data processing has not started.</span></span> 
- <span data-ttu-id="4cee3-113">Выполняется.</span><span class="sxs-lookup"><span data-stu-id="4cee3-113">InProgress.</span></span>
<span data-ttu-id="4cee3-114">Выполняется обработка данных.</span><span class="sxs-lookup"><span data-stu-id="4cee3-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="4cee3-115">Начать.</span><span class="sxs-lookup"><span data-stu-id="4cee3-115">Ready.</span></span>
<span data-ttu-id="4cee3-116">Обработка данных завершена.</span><span class="sxs-lookup"><span data-stu-id="4cee3-116">Data processing is completed.</span></span>
<span data-ttu-id="4cee3-117">Срез данных готов к зависимым сегментам, чтобы использовать его.</span><span class="sxs-lookup"><span data-stu-id="4cee3-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="4cee3-118">Ошибкой.</span><span class="sxs-lookup"><span data-stu-id="4cee3-118">Failed.</span></span>
<span data-ttu-id="4cee3-119">Не удалось выполнить вызов, создающий срез.</span><span class="sxs-lookup"><span data-stu-id="4cee3-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="4cee3-120">Пуст.</span><span class="sxs-lookup"><span data-stu-id="4cee3-120">Skip.</span></span>
<span data-ttu-id="4cee3-121">Фабрика данных пропускает обработку среза.</span><span class="sxs-lookup"><span data-stu-id="4cee3-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="4cee3-122">Повторить.</span><span class="sxs-lookup"><span data-stu-id="4cee3-122">Retry.</span></span>
<span data-ttu-id="4cee3-123">Фабрика данных повторяет запуск, создающий срез.</span><span class="sxs-lookup"><span data-stu-id="4cee3-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="4cee3-124">Время ожидания истекло. Превышено время ожидания обработки данных.</span><span class="sxs-lookup"><span data-stu-id="4cee3-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="4cee3-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="4cee3-125">PendingValidation.</span></span>
<span data-ttu-id="4cee3-126">Срез данных ожидает подтверждения перед обработкой.</span><span class="sxs-lookup"><span data-stu-id="4cee3-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="4cee3-127">Повторите проверку.</span><span class="sxs-lookup"><span data-stu-id="4cee3-127">Retry Validation.</span></span>
<span data-ttu-id="4cee3-128">Фабрика данных повторяет проверку среза.</span><span class="sxs-lookup"><span data-stu-id="4cee3-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="4cee3-129">Проверка не удалась.</span><span class="sxs-lookup"><span data-stu-id="4cee3-129">Failed Validation.</span></span>
<span data-ttu-id="4cee3-130">Проверка среза завершилась ошибкой.</span><span class="sxs-lookup"><span data-stu-id="4cee3-130">Validation of the slice failed.</span></span>

<span data-ttu-id="4cee3-131">Для каждого сектора вы можете просмотреть дополнительные сведения о запуске, который создает срез с помощью командлета Get-AzureRmDataFactoryRun.</span><span class="sxs-lookup"><span data-stu-id="4cee3-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzureRmDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="4cee3-132">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4cee3-132">EXAMPLES</span></span>

### <span data-ttu-id="4cee3-133">Пример 1: получение срезов данных для набора данных</span><span class="sxs-lookup"><span data-stu-id="4cee3-133">Example 1: Get data slices for a dataset</span></span>
```
PS C:\>Get-AzureRmDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 1:00:00 AM
End               : 5/21/2014 2:00:00 AM
RetryCount        : 0
Status            : Ready

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 2:00:00 AM
End               : 5/21/2014 3:00:00 AM
RetryCount        : 0
Status            : Ready

. . . 

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 8:00:00 PM
End               : 5/21/2014 9:00:00 PM
RetryCount        : 0
Status            : PendingExecution

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 9:00:00 PM
End               : 5/21/2014 10:00:00 PM
RetryCount        : 0
Status            : PendingExecution

. . .
```

<span data-ttu-id="4cee3-134">Эта команда получает все срезы данных для набора данных с именем WikiAggregatedData в фабрике данных с именем WikiADF.</span><span class="sxs-lookup"><span data-stu-id="4cee3-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="4cee3-135">Команда получает срезы, созданные после того, как указан параметр StartDateTime.</span><span class="sxs-lookup"><span data-stu-id="4cee3-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="4cee3-136">Следующий пример кода задает доступность для этого набора данных каждый час в файле нотации JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="4cee3-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>

                        availability: 
                        {
                        period: "Hour",
                        periodMultiplier: 1
                        }

                    Some of the results are Ready and others are PendingExecution.
<span data-ttu-id="4cee3-137">Готовые срезы уже запущены.</span><span class="sxs-lookup"><span data-stu-id="4cee3-137">Ready slices have already run.</span></span>
<span data-ttu-id="4cee3-138">Ожидающие отрезки выполняются в конце каждого часа в интервале, указанном в командлете Set-AzureRmDataFactoryPipelineActivePeriod.</span><span class="sxs-lookup"><span data-stu-id="4cee3-138">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzureRmDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="4cee3-139">В этом примере начальные и конечные периоды для конвейера и среза имеют значение один день (24 часа).</span><span class="sxs-lookup"><span data-stu-id="4cee3-139">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

## <span data-ttu-id="4cee3-140">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4cee3-140">PARAMETERS</span></span>

### <span data-ttu-id="4cee3-141">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="4cee3-141">-DataFactory</span></span>
<span data-ttu-id="4cee3-142">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="4cee3-142">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="4cee3-143">Этот командлет получает срезы, которые относятся к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="4cee3-143">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4cee3-144">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4cee3-144">-DataFactoryName</span></span>
<span data-ttu-id="4cee3-145">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="4cee3-145">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4cee3-146">Этот командлет получает срезы, которые относятся к фабрике данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="4cee3-146">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4cee3-147">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="4cee3-147">-DatasetName</span></span>
<span data-ttu-id="4cee3-148">Указывает имя набора данных, для которого этот командлет получает срезы.</span><span class="sxs-lookup"><span data-stu-id="4cee3-148">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

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

### <span data-ttu-id="4cee3-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cee3-149">-DefaultProfile</span></span>
<span data-ttu-id="4cee3-150">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4cee3-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cee3-151">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="4cee3-151">-EndDateTime</span></span>
<span data-ttu-id="4cee3-152">Указывает конец периода времени в качестве объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="4cee3-152">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="4cee3-153">Этот командлет получает срезы, созданные до того момента, когда этот параметр указан.</span><span class="sxs-lookup"><span data-stu-id="4cee3-153">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="4cee3-154">Чтобы получить дополнительные сведения о объектах **DateTime** , введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="4cee3-154">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="4cee3-155">*EndDateTime* должен быть указан в формате ISO8601, как показано в следующих примерах:</span><span class="sxs-lookup"><span data-stu-id="4cee3-155">*EndDateTime* must be specified in the ISO8601 format as in the following examples:</span></span> 

<span data-ttu-id="4cee3-156">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (тихоокеанское стандартное время)</span><span class="sxs-lookup"><span data-stu-id="4cee3-156">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="4cee3-157">Обозначение часового пояса по умолчанию — UTC.</span><span class="sxs-lookup"><span data-stu-id="4cee3-157">The default time zone designator is UTC.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cee3-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cee3-158">-ResourceGroupName</span></span>
<span data-ttu-id="4cee3-159">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="4cee3-159">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4cee3-160">Этот командлет получает срезы, которые относятся к группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="4cee3-160">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4cee3-161">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="4cee3-161">-StartDateTime</span></span>
<span data-ttu-id="4cee3-162">Задает начало периода времени в качестве объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="4cee3-162">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="4cee3-163">Этот командлет получает срезы, созданные после того, как указан этот параметр.</span><span class="sxs-lookup"><span data-stu-id="4cee3-163">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="4cee3-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cee3-164">CommonParameters</span></span>
<span data-ttu-id="4cee3-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4cee3-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cee3-166">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cee3-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cee3-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4cee3-167">INPUTS</span></span>

### <span data-ttu-id="4cee3-168">Ничего</span><span class="sxs-lookup"><span data-stu-id="4cee3-168">None</span></span>
<span data-ttu-id="4cee3-169">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="4cee3-169">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4cee3-170">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4cee3-170">OUTPUTS</span></span>

### <span data-ttu-id="4cee3-171">System. Collections. Generic. List ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataSlice, Microsoft. WindowsAzure. Commands. Utilities, Version = 0.8.2.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="4cee3-171">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataSlice, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="4cee3-172">Пуск</span><span class="sxs-lookup"><span data-stu-id="4cee3-172">NOTES</span></span>
* <span data-ttu-id="4cee3-173">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="4cee3-173">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4cee3-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4cee3-174">RELATED LINKS</span></span>

[<span data-ttu-id="4cee3-175">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="4cee3-175">Set-AzureRmDataFactorySliceStatus</span></span>](./Set-AzureRmDataFactorySliceStatus.md)

[<span data-ttu-id="4cee3-176">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="4cee3-176">Get-AzureRmDataFactoryRun</span></span>](./Get-AzureRmDataFactoryRun.md)

[<span data-ttu-id="4cee3-177">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="4cee3-177">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

