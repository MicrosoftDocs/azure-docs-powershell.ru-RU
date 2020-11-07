---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobCopyState.md
ms.openlocfilehash: fba71dbac836fb6cc6551982945135e8e9410744
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559396"
---
# <span data-ttu-id="fd1aa-101">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="fd1aa-101">Get-AzureStorageBlobCopyState</span></span>

## <span data-ttu-id="fd1aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fd1aa-102">SYNOPSIS</span></span>
<span data-ttu-id="fd1aa-103">Получает состояние копии большого двоичного объекта хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-103">Gets the copy status of an Azure Storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd1aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fd1aa-104">SYNTAX</span></span>

### <span data-ttu-id="fd1aa-105">NamePipeline (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fd1aa-105">NamePipeline (Default)</span></span>
```
Get-AzureStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="fd1aa-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="fd1aa-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="fd1aa-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="fd1aa-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="fd1aa-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd1aa-108">DESCRIPTION</span></span>
<span data-ttu-id="fd1aa-109">Командлет **Get-AzureStorageBlobCopyState** получает состояние копии большого двоичного объекта хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-109">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="fd1aa-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fd1aa-110">EXAMPLES</span></span>

### <span data-ttu-id="fd1aa-111">Пример 1: получение состояния копии большого двоичного объекта</span><span class="sxs-lookup"><span data-stu-id="fd1aa-111">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="fd1aa-112">Эта команда возвращает состояние копирования большого двоичного объекта с именем ContosoPlanning2015 в контейнере ContosoUploads.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-112">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="fd1aa-113">Пример 2: получение состояния копии для большого двоичного объекта с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="fd1aa-113">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzureStorageBlobCopyState
```

<span data-ttu-id="fd1aa-114">Эта команда получает двоичный объект с именем ContosoPlanning2015 в контейнере с именем ContosoUploads с помощью командлета **Get-AzureStorageBlob** , а затем передает результат в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-114">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fd1aa-115">Командлет **Get-AzureStorageBlobCopyState** получает состояние копирования для этого большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-115">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="fd1aa-116">Пример 3: получение состояния копии для большого двоичного объекта в контейнере с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="fd1aa-116">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="fd1aa-117">Эта команда получает контейнер с именем с помощью командлета **Get-AzureStorageBlob** , а затем передает результат в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-117">This command gets the container named by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="fd1aa-118">Командлет **Get-AzureStorageContainer** получает состояние копирования для большого двоичного объекта с именем ContosoPlanning2015 в этом контейнере.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-118">The **Get-AzureStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

## <span data-ttu-id="fd1aa-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fd1aa-119">PARAMETERS</span></span>

### <span data-ttu-id="fd1aa-120">-BLOB</span><span class="sxs-lookup"><span data-stu-id="fd1aa-120">-Blob</span></span>
<span data-ttu-id="fd1aa-121">Указывает имя большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-121">Specifies the name of a blob.</span></span>
<span data-ttu-id="fd1aa-122">Этот командлет получает состояние операции копирования BLOB-объектов хранилища Azure, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-122">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd1aa-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fd1aa-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fd1aa-124">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fd1aa-125">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fd1aa-126">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fd1aa-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="fd1aa-127">-CloudBlob</span></span>
<span data-ttu-id="fd1aa-128">Указывает объект **CloudBlob** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-128">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="fd1aa-129">Чтобы получить объект **CloudBlob** , используйте командлет Get-AzureStorageBlob.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="fd1aa-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="fd1aa-130">-CloudBlobContainer</span></span>
<span data-ttu-id="fd1aa-131">Указывает объект **CloudBlobContainer** из библиотеки клиента хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-131">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="fd1aa-132">Этот командлет получает состояние копирования большого двоичного объекта в контейнере, указанном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-132">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="fd1aa-133">Чтобы получить объект **CloudBlobContainer** , используйте командлет Get-AzureStorageContainer.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-133">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="fd1aa-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fd1aa-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fd1aa-135">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fd1aa-136">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fd1aa-137">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fd1aa-138">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fd1aa-139">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-139">The default value is 10.</span></span>

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

### <span data-ttu-id="fd1aa-140">-Container</span><span class="sxs-lookup"><span data-stu-id="fd1aa-140">-Container</span></span>
<span data-ttu-id="fd1aa-141">Указывает имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-141">Specifies the name of a container.</span></span>
<span data-ttu-id="fd1aa-142">Этот командлет получает состояние копирования для большого двоичного объекта в контейнере, указанном в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-142">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd1aa-143">-Context</span><span class="sxs-lookup"><span data-stu-id="fd1aa-143">-Context</span></span>
<span data-ttu-id="fd1aa-144">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-144">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fd1aa-145">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-145">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fd1aa-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fd1aa-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fd1aa-147">Указывает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="fd1aa-148">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="fd1aa-149">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="fd1aa-149">-WaitForComplete</span></span>
<span data-ttu-id="fd1aa-150">Указывает на то, что этот командлет ожидает завершения копирования.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-150">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="fd1aa-151">Если этот параметр не указан, этот командлет возвращает результат немедленно.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-151">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="fd1aa-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd1aa-152">CommonParameters</span></span>
<span data-ttu-id="fd1aa-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd1aa-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd1aa-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd1aa-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fd1aa-155">INPUTS</span></span>

### <span data-ttu-id="fd1aa-156">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fd1aa-156">IStorageContext</span></span>

<span data-ttu-id="fd1aa-157">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="fd1aa-157">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="fd1aa-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd1aa-158">OUTPUTS</span></span>

### <span data-ttu-id="fd1aa-159">CopyState</span><span class="sxs-lookup"><span data-stu-id="fd1aa-159">CopyState</span></span>

## <span data-ttu-id="fd1aa-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="fd1aa-160">NOTES</span></span>

## <span data-ttu-id="fd1aa-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd1aa-161">RELATED LINKS</span></span>

[<span data-ttu-id="fd1aa-162">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="fd1aa-162">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="fd1aa-163">Остановить-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="fd1aa-163">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)

