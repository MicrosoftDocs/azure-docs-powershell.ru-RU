---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileCopyState.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 85e91ded08fb3d4a8f026f463de58ff0b0cd7e27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567202"
---
# <span data-ttu-id="e403d-101">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="e403d-101">Get-AzureStorageFileCopyState</span></span>

## <span data-ttu-id="e403d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e403d-102">SYNOPSIS</span></span>
<span data-ttu-id="e403d-103">Получает состояние операции копирования.</span><span class="sxs-lookup"><span data-stu-id="e403d-103">Gets the state of a copy operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e403d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e403d-104">SYNTAX</span></span>

### <span data-ttu-id="e403d-105">Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="e403d-105">ShareName</span></span>
```
Get-AzureStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e403d-106">Файл</span><span class="sxs-lookup"><span data-stu-id="e403d-106">File</span></span>
```
Get-AzureStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="e403d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e403d-107">DESCRIPTION</span></span>
<span data-ttu-id="e403d-108">Командлет **Get-AzureStorageFileCopyState** получает состояние операции копирования файлов в хранилище Azure.</span><span class="sxs-lookup"><span data-stu-id="e403d-108">The **Get-AzureStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>

## <span data-ttu-id="e403d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e403d-109">EXAMPLES</span></span>

### <span data-ttu-id="e403d-110">Пример 1: получение состояния копии по имени файла</span><span class="sxs-lookup"><span data-stu-id="e403d-110">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzureStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="e403d-111">Эта команда возвращает состояние операции копирования для файла с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="e403d-111">This command gets the state of the copy operation for a file that has the specified name.</span></span>

## <span data-ttu-id="e403d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e403d-112">PARAMETERS</span></span>

### <span data-ttu-id="e403d-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e403d-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e403d-114">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="e403d-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e403d-115">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="e403d-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e403d-116">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="e403d-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e403d-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e403d-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e403d-118">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="e403d-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e403d-119">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="e403d-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e403d-120">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="e403d-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e403d-121">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="e403d-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e403d-122">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="e403d-122">The default value is 10.</span></span>

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

### <span data-ttu-id="e403d-123">-Context</span><span class="sxs-lookup"><span data-stu-id="e403d-123">-Context</span></span>
<span data-ttu-id="e403d-124">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e403d-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="e403d-125">Чтобы получить контекст, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="e403d-125">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e403d-126">-Файл</span><span class="sxs-lookup"><span data-stu-id="e403d-126">-File</span></span>
<span data-ttu-id="e403d-127">Указывает объект **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="e403d-127">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="e403d-128">Вы можете создать файл в облаке или получить его с помощью командлета Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="e403d-128">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e403d-129">-FilePath</span><span class="sxs-lookup"><span data-stu-id="e403d-129">-FilePath</span></span>
<span data-ttu-id="e403d-130">Задает путь к файлу относительно общего доступа к хранилищу Azure.</span><span class="sxs-lookup"><span data-stu-id="e403d-130">Specifies the path of the file relative to an Azure Storage share.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e403d-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e403d-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e403d-132">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="e403d-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="e403d-133">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="e403d-133">-ShareName</span></span>
<span data-ttu-id="e403d-134">Указывает имя общего доступа.</span><span class="sxs-lookup"><span data-stu-id="e403d-134">Specifies the name of a share.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e403d-135">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="e403d-135">-WaitForComplete</span></span>
<span data-ttu-id="e403d-136">Указывает на то, что этот командлет ожидает завершения копирования.</span><span class="sxs-lookup"><span data-stu-id="e403d-136">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="e403d-137">Если этот параметр не указан, этот командлет возвращает результат немедленно.</span><span class="sxs-lookup"><span data-stu-id="e403d-137">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="e403d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e403d-138">CommonParameters</span></span>
<span data-ttu-id="e403d-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e403d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e403d-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e403d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e403d-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e403d-141">INPUTS</span></span>

### <span data-ttu-id="e403d-142">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e403d-142">IStorageContext</span></span>

<span data-ttu-id="e403d-143">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e403d-143">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="e403d-144">CloudFile</span><span class="sxs-lookup"><span data-stu-id="e403d-144">CloudFile</span></span>

<span data-ttu-id="e403d-145">Параметр "файл" принимает значение типа "CloudFile" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e403d-145">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

## <span data-ttu-id="e403d-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e403d-146">OUTPUTS</span></span>

## <span data-ttu-id="e403d-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="e403d-147">NOTES</span></span>

## <span data-ttu-id="e403d-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e403d-148">RELATED LINKS</span></span>

[<span data-ttu-id="e403d-149">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="e403d-149">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="e403d-150">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e403d-150">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e403d-151">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e403d-151">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)

[<span data-ttu-id="e403d-152">Остановить-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="e403d-152">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)