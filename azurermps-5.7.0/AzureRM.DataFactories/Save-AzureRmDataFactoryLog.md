---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/save-azurermdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Save-AzureRmDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Save-AzureRmDataFactoryLog.md
ms.openlocfilehash: 696e2de560b67db78f24dea7e8512d85c3640902
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559120"
---
# <span data-ttu-id="864d2-101">Save-AzureRmDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="864d2-101">Save-AzureRmDataFactoryLog</span></span>

## <span data-ttu-id="864d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="864d2-102">SYNOPSIS</span></span>
<span data-ttu-id="864d2-103">Загружает файлы журнала из службы обработки Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="864d2-103">Downloads log files from Azure HDInsight processing.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="864d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="864d2-104">SYNTAX</span></span>

### <span data-ttu-id="864d2-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="864d2-105">ByFactoryName (Default)</span></span>
```
Save-AzureRmDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="864d2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="864d2-106">ByFactoryObject</span></span>
```
Save-AzureRmDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="864d2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="864d2-107">DESCRIPTION</span></span>
<span data-ttu-id="864d2-108">Командлет **Save-AzureRmDataFactoryLog** загружает файлы журнала, связанные с обработкой Azure HDInsight для проектов свинья или Hive, или для настраиваемых действий на локальном жестком диске.</span><span class="sxs-lookup"><span data-stu-id="864d2-108">The **Save-AzureRmDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="864d2-109">Сначала необходимо выполнить командлет Get-AzureRmDataFactoryRun, чтобы получить идентификатор для действия, выполняемого для среза данных, а затем использовать этот идентификатор для получения файлов журнала из хранилища BLOB-объектов, связанного с кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="864d2-109">You first run the Get-AzureRmDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>

<span data-ttu-id="864d2-110">Если параметр *DownloadLogs* не указан, командлет просто возвращает расположение файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="864d2-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>

<span data-ttu-id="864d2-111">Если вы укажете *DownloadLogs* без указания выходного каталога (параметр *Output* ), файлы журнала загружаются в папку документы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="864d2-111">If you specify *DownloadLogs* without specifying an output directory ( *Output* parameter), the log files are downloaded to the default Documents folder.</span></span>

<span data-ttu-id="864d2-112">Если задать *DownloadLogs* и выходную папку ( *Output* ), файлы журнала будут загружены в указанную папку.</span><span class="sxs-lookup"><span data-stu-id="864d2-112">If you specify *DownloadLogs* along with an output folder ( *Output* ), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="864d2-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="864d2-113">EXAMPLES</span></span>

### <span data-ttu-id="864d2-114">Пример 1: сохранение файлов журнала в определенной папке</span><span class="sxs-lookup"><span data-stu-id="864d2-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="864d2-115">Эта команда позволяет сохранить файлы журнала для действия с ИД 841b77c9-d56c-48d1-99a3-8c16c3e77d39, в котором действие относится к конвейеру в фабрике данных с именем LogProcessingFactory в группе ресурсов с именем ADF.</span><span class="sxs-lookup"><span data-stu-id="864d2-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="864d2-116">Файлы журнала сохраняются в папке C:\Test.</span><span class="sxs-lookup"><span data-stu-id="864d2-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="864d2-117">Пример 2: сохранение файлов журнала в папке "документы по умолчанию"</span><span class="sxs-lookup"><span data-stu-id="864d2-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="864d2-118">Эта команда позволяет сохранить файлы журнала в папке "документы" (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="864d2-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="864d2-119">Пример 3: получение расположения файлов журнала</span><span class="sxs-lookup"><span data-stu-id="864d2-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="864d2-120">Эта команда возвращает расположение файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="864d2-120">This command returns the location of log files.</span></span>
<span data-ttu-id="864d2-121">Обратите внимание, что *DownloadLogs* не указан.</span><span class="sxs-lookup"><span data-stu-id="864d2-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="864d2-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="864d2-122">PARAMETERS</span></span>

### <span data-ttu-id="864d2-123">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="864d2-123">-DataFactory</span></span>
<span data-ttu-id="864d2-124">Указывает объект **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="864d2-124">Specifies a **PSDataFactory** object.</span></span>

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

### <span data-ttu-id="864d2-125">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="864d2-125">-DataFactoryName</span></span>
<span data-ttu-id="864d2-126">Указывает имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="864d2-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="864d2-127">Этот командлет загружает файлы журнала для фабрики данных, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="864d2-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="864d2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="864d2-128">-DefaultProfile</span></span>
<span data-ttu-id="864d2-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="864d2-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="864d2-130">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="864d2-130">-DownloadLogs</span></span>
<span data-ttu-id="864d2-131">Указывает на то, что этот командлет загружает файлы журнала на локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="864d2-131">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="864d2-132">Если папка *Ouptut* не указана, файлы сохраняются в папке "документы" во вложенной папке.</span><span class="sxs-lookup"><span data-stu-id="864d2-132">If *Ouptut* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

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

### <span data-ttu-id="864d2-133">-ID</span><span class="sxs-lookup"><span data-stu-id="864d2-133">-Id</span></span>
<span data-ttu-id="864d2-134">Указывает идентификатор действия, выполняемого для среза данных.</span><span class="sxs-lookup"><span data-stu-id="864d2-134">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="864d2-135">Для получения идентификатора используйте командлет Get-AzureRmDataFactoryRun.</span><span class="sxs-lookup"><span data-stu-id="864d2-135">Use the Get-AzureRmDataFactoryRun cmdlet to get an ID.</span></span>

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

### <span data-ttu-id="864d2-136">-Output</span><span class="sxs-lookup"><span data-stu-id="864d2-136">-Output</span></span>
<span data-ttu-id="864d2-137">Указывает папку выходных данных, в которой сохраняются Скачанные файлы журнала.</span><span class="sxs-lookup"><span data-stu-id="864d2-137">Specifies the output folder in which the downloaded log files are saved.</span></span>

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

### <span data-ttu-id="864d2-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="864d2-138">-ResourceGroupName</span></span>
<span data-ttu-id="864d2-139">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="864d2-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="864d2-140">Этот командлет создает фабрику данных, принадлежащую группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="864d2-140">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="864d2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="864d2-141">CommonParameters</span></span>
<span data-ttu-id="864d2-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="864d2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="864d2-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="864d2-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="864d2-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="864d2-144">INPUTS</span></span>

### <span data-ttu-id="864d2-145">Ничего</span><span class="sxs-lookup"><span data-stu-id="864d2-145">None</span></span>
<span data-ttu-id="864d2-146">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="864d2-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="864d2-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="864d2-147">OUTPUTS</span></span>

### <span data-ttu-id="864d2-148">Microsoft. Azure. Commands. Factoring. Models. PSRunLogInfo</span><span class="sxs-lookup"><span data-stu-id="864d2-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="864d2-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="864d2-149">NOTES</span></span>
* <span data-ttu-id="864d2-150">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики</span><span class="sxs-lookup"><span data-stu-id="864d2-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="864d2-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="864d2-151">RELATED LINKS</span></span>

[<span data-ttu-id="864d2-152">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="864d2-152">Get-AzureRmDataFactoryRun</span></span>](./Get-AzureRmDataFactoryRun.md)

[<span data-ttu-id="864d2-153">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="864d2-153">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="864d2-154">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="864d2-154">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="864d2-155">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="864d2-155">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="864d2-156">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="864d2-156">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="864d2-157">Приостановить — AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="864d2-157">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)

