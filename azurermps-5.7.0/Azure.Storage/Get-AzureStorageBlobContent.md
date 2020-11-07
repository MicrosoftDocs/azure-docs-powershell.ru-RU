---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobContent.md
ms.openlocfilehash: 5023643ae57ab73ea625254f7b2362c947209f8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559399"
---
# <span data-ttu-id="84121-101">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="84121-101">Get-AzureStorageBlobContent</span></span>

## <span data-ttu-id="84121-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="84121-102">SYNOPSIS</span></span>
<span data-ttu-id="84121-103">Загружает большой двоичный объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="84121-103">Downloads a storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84121-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="84121-104">SYNTAX</span></span>

### <span data-ttu-id="84121-105">ReceiveManual (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="84121-105">ReceiveManual (Default)</span></span>
```
Get-AzureStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84121-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="84121-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlob <CloudBlob> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84121-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="84121-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84121-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84121-108">DESCRIPTION</span></span>
<span data-ttu-id="84121-109">Командлет **Get-AzureStorageBlobContent** загружает указанный большой двоичный объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="84121-109">The **Get-AzureStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="84121-110">Если имя большого двоичного объекта не является допустимым для локального компьютера, этот командлет автоматически разрешает его, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="84121-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="84121-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="84121-111">EXAMPLES</span></span>

### <span data-ttu-id="84121-112">Пример 1: Загрузка содержимого BLOB-объектов по имени</span><span class="sxs-lookup"><span data-stu-id="84121-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzureStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="84121-113">Эта команда загружает большой двоичный объект по имени.</span><span class="sxs-lookup"><span data-stu-id="84121-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="84121-114">Пример 2: Загрузка содержимого BLOB-объектов с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="84121-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzureStorageBlob -Container containername -Blob blobname | Get-AzureStorageBlobContent
```

<span data-ttu-id="84121-115">Эта команда использует конвейер для поиска и загрузки содержимого BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="84121-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="84121-116">Пример 3: скачивание содержимого BLOB-объектов с помощью конвейера и подстановочного знака</span><span class="sxs-lookup"><span data-stu-id="84121-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Get-AzureStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="84121-117">В этом примере используется подстановочный знак "звездочка" и канал продаж для поиска и загрузки содержимого BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="84121-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

## <span data-ttu-id="84121-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="84121-118">PARAMETERS</span></span>

### <span data-ttu-id="84121-119">-BLOB</span><span class="sxs-lookup"><span data-stu-id="84121-119">-Blob</span></span>
<span data-ttu-id="84121-120">Указывает имя большого двоичного объекта, который нужно скачать.</span><span class="sxs-lookup"><span data-stu-id="84121-120">Specifies the name of the blob to be downloaded.</span></span>

```yaml
Type: String
Parameter Sets: ReceiveManual, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84121-121">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="84121-121">-CheckMd5</span></span>
<span data-ttu-id="84121-122">Указывает, следует ли проверять сумму Md5 для скачанного файла.</span><span class="sxs-lookup"><span data-stu-id="84121-122">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="84121-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="84121-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="84121-124">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="84121-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="84121-125">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="84121-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="84121-126">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="84121-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="84121-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="84121-127">-CloudBlob</span></span>
<span data-ttu-id="84121-128">Задает большой двоичный объект облака.</span><span class="sxs-lookup"><span data-stu-id="84121-128">Specifies a cloud blob.</span></span>
<span data-ttu-id="84121-129">Чтобы получить объект **CloudBlob** , используйте командлет Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="84121-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84121-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="84121-130">-CloudBlobContainer</span></span>
<span data-ttu-id="84121-131">Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="84121-131">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="84121-132">Вы можете создать его или воспользоваться командлетом Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="84121-132">You can create it or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84121-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="84121-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="84121-134">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="84121-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="84121-135">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="84121-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="84121-136">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="84121-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="84121-137">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="84121-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="84121-138">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="84121-138">The default value is 10.</span></span>

<span data-ttu-id="84121-139">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="84121-139">The default value is 10.</span></span>

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

### <span data-ttu-id="84121-140">-Container</span><span class="sxs-lookup"><span data-stu-id="84121-140">-Container</span></span>
<span data-ttu-id="84121-141">Указывает имя контейнера, в котором есть большой двоичный объект, который вы хотите скачать.</span><span class="sxs-lookup"><span data-stu-id="84121-141">Specifies the name of container that has the blob you want to download.</span></span>

```yaml
Type: String
Parameter Sets: ReceiveManual
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84121-142">-Context</span><span class="sxs-lookup"><span data-stu-id="84121-142">-Context</span></span>
<span data-ttu-id="84121-143">Указывает учетную запись хранения Azure, из которой вы хотите скачать содержимое BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="84121-143">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="84121-144">Вы можете использовать командлет New-AzureStorageContext для создания контекста хранилища.</span><span class="sxs-lookup"><span data-stu-id="84121-144">You can use the New-AzureStorageContext cmdlet to create a storage context.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84121-145">-Destination</span><span class="sxs-lookup"><span data-stu-id="84121-145">-Destination</span></span>
<span data-ttu-id="84121-146">Указывает место для хранения скачанного файла.</span><span class="sxs-lookup"><span data-stu-id="84121-146">Specifies the location to store the downloaded file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84121-147">-Force</span><span class="sxs-lookup"><span data-stu-id="84121-147">-Force</span></span>
<span data-ttu-id="84121-148">Перезаписывает существующий файл без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="84121-148">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="84121-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="84121-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="84121-150">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="84121-150">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="84121-151">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="84121-151">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="84121-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84121-152">-Confirm</span></span>
<span data-ttu-id="84121-153">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="84121-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84121-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84121-154">-WhatIf</span></span>
<span data-ttu-id="84121-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="84121-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84121-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="84121-156">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84121-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84121-157">CommonParameters</span></span>
<span data-ttu-id="84121-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="84121-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84121-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84121-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84121-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="84121-160">INPUTS</span></span>

### <span data-ttu-id="84121-161">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="84121-161">IStorageContext</span></span>

<span data-ttu-id="84121-162">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="84121-162">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="84121-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="84121-163">OUTPUTS</span></span>

### <span data-ttu-id="84121-164">AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="84121-164">AzureStorageContainer</span></span>

## <span data-ttu-id="84121-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="84121-165">NOTES</span></span>
* <span data-ttu-id="84121-166">Если имя большого двоичного объекта не является допустимым для локального компьютера, этот командлет по возможности разрешает его.</span><span class="sxs-lookup"><span data-stu-id="84121-166">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="84121-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84121-167">RELATED LINKS</span></span>

[<span data-ttu-id="84121-168">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="84121-168">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)

[<span data-ttu-id="84121-169">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="84121-169">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="84121-170">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="84121-170">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)