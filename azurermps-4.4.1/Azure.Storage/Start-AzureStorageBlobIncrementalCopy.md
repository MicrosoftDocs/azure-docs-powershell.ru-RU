---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageBlobIncrementalCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageBlobIncrementalCopy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/e87bc1c9e534808427b7dc77aa06eacc46663253
ms.openlocfilehash: b327db4c7054e3c841dca3310887b1d1f1201d23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566357"
---
# <span data-ttu-id="5c88d-101">Start-AzureStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="5c88d-101">Start-AzureStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="5c88d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5c88d-102">SYNOPSIS</span></span>
<span data-ttu-id="5c88d-103">Начните операцию добавочного копирования из моментального снимка большого двоичного объекта страницы до указанного блоба страниц назначения.</span><span class="sxs-lookup"><span data-stu-id="5c88d-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c88d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5c88d-104">SYNTAX</span></span>

### <span data-ttu-id="5c88d-105">ContainerInstance (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5c88d-105">ContainerInstance (Default)</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c88d-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="5c88d-106">BlobInstance</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c88d-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="5c88d-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c88d-108">ContainerName</span><span class="sxs-lookup"><span data-stu-id="5c88d-108">ContainerName</span></span>
```
Start-AzureStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c88d-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="5c88d-109">UriPipeline</span></span>
```
Start-AzureStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c88d-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c88d-110">DESCRIPTION</span></span>
<span data-ttu-id="5c88d-111">Начните операцию добавочного копирования из моментального снимка большого двоичного объекта страницы до указанного блоба страниц назначения.</span><span class="sxs-lookup"><span data-stu-id="5c88d-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="5c88d-112">Ознакомьтесь с дополнительными сведениями об этой функции https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="5c88d-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="5c88d-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5c88d-113">EXAMPLES</span></span>

### <span data-ttu-id="5c88d-114">Пример 1: запуск добавочной операции копирования по имени BLOB-объектов и времени создания моментального снимка</span><span class="sxs-lookup"><span data-stu-id="5c88d-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzureStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="5c88d-115">Эта команда запускает добавочную операцию копирования по имени BLOB-объектов и времени snapshot.</span><span class="sxs-lookup"><span data-stu-id="5c88d-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="5c88d-116">Пример 2: запуск операции добавочного копирования с помощью URI источника</span><span class="sxs-lookup"><span data-stu-id="5c88d-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzureStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="5c88d-117">Эта команда запускает операцию добавочного копирования с использованием исходного кода ресурса</span><span class="sxs-lookup"><span data-stu-id="5c88d-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="5c88d-118">Пример 3: запуск операции добавочного копирования с помощью конвейера контейнера из GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="5c88d-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzureStorageContainer -Container container1 | Start-AzureStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="5c88d-119">Эта команда запускает операцию добавочного копирования с помощью конвейера контейнера из GetAzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="5c88d-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="5c88d-120">Пример 4: запуск операции добавочного копирования из объекта CloudPageBlob в конечный BLOB-объект с именем BLOB-объекта</span><span class="sxs-lookup"><span data-stu-id="5c88d-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzureStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzureStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="5c88d-121">Эта команда запускает операцию добавочного копирования из объекта CloudPageBlob в конечный большой двоичный объект с именем BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="5c88d-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="5c88d-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5c88d-122">PARAMETERS</span></span>

### <span data-ttu-id="5c88d-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="5c88d-123">-AbsoluteUri</span></span>
<span data-ttu-id="5c88d-124">Абсолютный URI в источник.</span><span class="sxs-lookup"><span data-stu-id="5c88d-124">Absolute Uri to the source.</span></span> <span data-ttu-id="5c88d-125">Следует отметить, что учетные данные должны быть указаны в универсальном коде ресурса (URI), если их источник требуется.</span><span class="sxs-lookup"><span data-stu-id="5c88d-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

```yaml
Type: String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c88d-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5c88d-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5c88d-127">Максимальное время выполнения на стороне клиента для каждого запроса в секундах.</span><span class="sxs-lookup"><span data-stu-id="5c88d-127">The client side maximum execution time for each request in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c88d-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="5c88d-128">-CloudBlob</span></span>
<span data-ttu-id="5c88d-129">Объект CloudBlob из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="5c88d-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="5c88d-130">Вы можете создать его или воспользоваться командлетом Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="5c88d-130">You can create it or use Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c88d-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="5c88d-131">-CloudBlobContainer</span></span>
<span data-ttu-id="5c88d-132">Объект CloudBlobContainer из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="5c88d-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="5c88d-133">Вы можете создать его или воспользоваться командлетом Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="5c88d-133">You can create it or use Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c88d-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5c88d-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5c88d-135">Общее количество параллельных асинхронных задач.</span><span class="sxs-lookup"><span data-stu-id="5c88d-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="5c88d-136">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="5c88d-136">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c88d-137">-Context</span><span class="sxs-lookup"><span data-stu-id="5c88d-137">-Context</span></span>
<span data-ttu-id="5c88d-138">Контекст исходного хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="5c88d-138">Source Azure Storage Context.</span></span> <span data-ttu-id="5c88d-139">Вы можете создать его с помощью New-AzureStorageContext командлета.</span><span class="sxs-lookup"><span data-stu-id="5c88d-139">You can create it by New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerInstance, BlobInstance, BlobInstanceToBlobInstance, ContainerName
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c88d-140">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="5c88d-140">-DestBlob</span></span>
<span data-ttu-id="5c88d-141">Имя целевого BLOB-объекта</span><span class="sxs-lookup"><span data-stu-id="5c88d-141">Destination blob name</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c88d-142">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="5c88d-142">-DestCloudBlob</span></span>
<span data-ttu-id="5c88d-143">Конечный объект CloudBlob</span><span class="sxs-lookup"><span data-stu-id="5c88d-143">Destination CloudBlob object</span></span>

```yaml
Type: CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c88d-144">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="5c88d-144">-DestContainer</span></span>
<span data-ttu-id="5c88d-145">Имя целевого контейнера</span><span class="sxs-lookup"><span data-stu-id="5c88d-145">Destination container name</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c88d-146">-DestContext</span><span class="sxs-lookup"><span data-stu-id="5c88d-146">-DestContext</span></span>
<span data-ttu-id="5c88d-147">Контекст целевого хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="5c88d-147">Destination Azure Storage Context.</span></span> <span data-ttu-id="5c88d-148">Вы можете создать его с помощью New-AzureStorageContext командлета.</span><span class="sxs-lookup"><span data-stu-id="5c88d-148">You can create it by New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c88d-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5c88d-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5c88d-150">Время ожидания сервера для каждого запроса в секундах.</span><span class="sxs-lookup"><span data-stu-id="5c88d-150">The server time out for each request in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c88d-151">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="5c88d-151">-SrcBlob</span></span>
<span data-ttu-id="5c88d-152">Имя большого двоичного объекта исходной страницы.</span><span class="sxs-lookup"><span data-stu-id="5c88d-152">Source page blob name.</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c88d-153">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="5c88d-153">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="5c88d-154">Время моментального снимка BLOB исходной страницы.</span><span class="sxs-lookup"><span data-stu-id="5c88d-154">Source page blob snapshot time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlobSnapshotTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c88d-155">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="5c88d-155">-SrcContainer</span></span>
<span data-ttu-id="5c88d-156">Имя исходного контейнера</span><span class="sxs-lookup"><span data-stu-id="5c88d-156">Source Container name</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c88d-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c88d-157">-Confirm</span></span>
<span data-ttu-id="5c88d-158">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5c88d-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c88d-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c88d-159">-WhatIf</span></span>
<span data-ttu-id="5c88d-160">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5c88d-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c88d-161">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5c88d-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c88d-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c88d-162">CommonParameters</span></span>
<span data-ttu-id="5c88d-163">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5c88d-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c88d-164">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c88d-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c88d-165">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5c88d-165">INPUTS</span></span>

### <span data-ttu-id="5c88d-166">Microsoft. WindowsAzure. Storage. BLOB. CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="5c88d-166">Microsoft.WindowsAzure.Storage.Blob.CloudPageBlob</span></span>
<span data-ttu-id="5c88d-167">Microsoft. WindowsAzure. Storage. BLOB. CloudBlobContainer System. String Microsoft. WindowsAzure. Commands. Common. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="5c88d-167">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer System.String Microsoft.WindowsAzure.Commands.Common.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="5c88d-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c88d-168">OUTPUTS</span></span>

### <span data-ttu-id="5c88d-169">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="5c88d-169">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="5c88d-170">Пуск</span><span class="sxs-lookup"><span data-stu-id="5c88d-170">NOTES</span></span>

## <span data-ttu-id="5c88d-171">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c88d-171">RELATED LINKS</span></span>
