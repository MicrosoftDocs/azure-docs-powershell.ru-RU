---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFile.md
ms.openlocfilehash: a66b84586693052a2e6279c0cd56d8b091ae4230
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565093"
---
# <span data-ttu-id="6c34c-101">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="6c34c-101">Get-AzureStorageFile</span></span>

## <span data-ttu-id="6c34c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6c34c-102">SYNOPSIS</span></span>
<span data-ttu-id="6c34c-103">Перечисление каталогов и файлов для пути.</span><span class="sxs-lookup"><span data-stu-id="6c34c-103">Lists directories and files for a path.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c34c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6c34c-104">SYNTAX</span></span>

### <span data-ttu-id="6c34c-105">Имя_общего_ресурса (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6c34c-105">ShareName (Default)</span></span>
```
Get-AzureStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c34c-106">Предоставить общий доступ</span><span class="sxs-lookup"><span data-stu-id="6c34c-106">Share</span></span>
```
Get-AzureStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6c34c-107">Папка</span><span class="sxs-lookup"><span data-stu-id="6c34c-107">Directory</span></span>
```
Get-AzureStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="6c34c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c34c-108">DESCRIPTION</span></span>
<span data-ttu-id="6c34c-109">Командлет **Get-AzureStorageFile** выводит список папок и файлов для указанного вами общего доступа или каталога.</span><span class="sxs-lookup"><span data-stu-id="6c34c-109">The **Get-AzureStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="6c34c-110">Укажите параметр *path* , чтобы получить экземпляр каталога или файла по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="6c34c-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>

<span data-ttu-id="6c34c-111">Этот командлет возвращает объекты **AzureStorageFile** и **AzureStorageDirectory** .</span><span class="sxs-lookup"><span data-stu-id="6c34c-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="6c34c-112">Вы можете использовать свойство " **подкаталог** " для различения папок и файлов.</span><span class="sxs-lookup"><span data-stu-id="6c34c-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="6c34c-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6c34c-113">EXAMPLES</span></span>

### <span data-ttu-id="6c34c-114">Пример 1: список папок в общем доступе</span><span class="sxs-lookup"><span data-stu-id="6c34c-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

<span data-ttu-id="6c34c-115">Эта команда выводит список только для каталогов в ContosoShare06 общего доступа.</span><span class="sxs-lookup"><span data-stu-id="6c34c-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="6c34c-116">Сначала она извлекает оба файла и каталоги, передает их оператору **WHERE** с помощью оператора конвейера, а затем удаляет все объекты, тип которых не "CloudFileDirectory".</span><span class="sxs-lookup"><span data-stu-id="6c34c-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "CloudFileDirectory".</span></span>

### <span data-ttu-id="6c34c-117">Пример 2: список папок с файлами</span><span class="sxs-lookup"><span data-stu-id="6c34c-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzureStorageFile
```

<span data-ttu-id="6c34c-118">Эта команда выводит список файлов и папок в каталоге ContosoWorkingFolder в разделе Общий доступ ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="6c34c-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="6c34c-119">Сначала он получает экземпляр службы каталогов, а затем конвейер в командлет **Get-AzureStorageFile для получения** списка каталогов.</span><span class="sxs-lookup"><span data-stu-id="6c34c-119">It first gets the directory instance, and then pipelines it to the **Get-AzureStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="6c34c-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6c34c-120">PARAMETERS</span></span>

### <span data-ttu-id="6c34c-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6c34c-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6c34c-122">Указывает интервал времени ожидания для одного запроса службы (в секундах).</span><span class="sxs-lookup"><span data-stu-id="6c34c-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6c34c-123">Если предыдущий вызов завершается сбоем в течение указанного интервала, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="6c34c-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6c34c-124">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="6c34c-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6c34c-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6c34c-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6c34c-126">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="6c34c-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6c34c-127">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="6c34c-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6c34c-128">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="6c34c-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6c34c-129">Этот параметр помогает уменьшить число проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="6c34c-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6c34c-130">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="6c34c-130">The default value is 10.</span></span>

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

### <span data-ttu-id="6c34c-131">-Context</span><span class="sxs-lookup"><span data-stu-id="6c34c-131">-Context</span></span>
<span data-ttu-id="6c34c-132">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="6c34c-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="6c34c-133">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="6c34c-133">To obtain a Storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6c34c-134">-Каталог</span><span class="sxs-lookup"><span data-stu-id="6c34c-134">-Directory</span></span>
<span data-ttu-id="6c34c-135">Определяет папку как объект **CloudFileDirectory** .</span><span class="sxs-lookup"><span data-stu-id="6c34c-135">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="6c34c-136">Этот командлет получает папку, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="6c34c-136">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="6c34c-137">Чтобы получить каталог, используйте командлет New-AzureStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="6c34c-137">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="6c34c-138">Вы также можете использовать командлет **Get-AzureStorageFile** , чтобы получить доступ к каталогу.</span><span class="sxs-lookup"><span data-stu-id="6c34c-138">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c34c-139">-Path</span><span class="sxs-lookup"><span data-stu-id="6c34c-139">-Path</span></span>
<span data-ttu-id="6c34c-140">Указывает путь к папке.</span><span class="sxs-lookup"><span data-stu-id="6c34c-140">Specifies the path of a folder.</span></span>

<span data-ttu-id="6c34c-141">Если параметр *путь* не указан, **Get-AzureStorageFile** приводит к перечислению каталогов и файлов в указанной общей папке или в каталоге.</span><span class="sxs-lookup"><span data-stu-id="6c34c-141">If you omit the *Path* parameter, **Get-AzureStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="6c34c-142">Если вы включаете параметр *path* , функция **Get-AzureStorageFile** возвращает экземпляр каталога или файла в указанном пути.</span><span class="sxs-lookup"><span data-stu-id="6c34c-142">If you include the *Path* parameter, **Get-AzureStorageFile** returns an instance of a directory or file in the specified path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c34c-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6c34c-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6c34c-144">Задает интервал времени ожидания службы (в секундах) для запроса.</span><span class="sxs-lookup"><span data-stu-id="6c34c-144">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="6c34c-145">Если заданный интервал проходит до обработки запроса службой, служба хранилища возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="6c34c-145">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="6c34c-146">-Общий доступ</span><span class="sxs-lookup"><span data-stu-id="6c34c-146">-Share</span></span>
<span data-ttu-id="6c34c-147">Указывает объект **CloudFileShare** .</span><span class="sxs-lookup"><span data-stu-id="6c34c-147">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="6c34c-148">Этот командлет получает файл или каталог из общей папки, которую указываете этот параметр.</span><span class="sxs-lookup"><span data-stu-id="6c34c-148">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="6c34c-149">Чтобы получить объект **CloudFileShare** , используйте командлет Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="6c34c-149">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="6c34c-150">Этот объект имеет контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="6c34c-150">This object contains the Storage context.</span></span>
<span data-ttu-id="6c34c-151">Если вы задаете этот параметр, не указывайте параметр *контекста* .</span><span class="sxs-lookup"><span data-stu-id="6c34c-151">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c34c-152">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="6c34c-152">-ShareName</span></span>
<span data-ttu-id="6c34c-153">Указывает имя общего файлового файла.</span><span class="sxs-lookup"><span data-stu-id="6c34c-153">Specifies the name of the file share.</span></span>
<span data-ttu-id="6c34c-154">Этот командлет получает файл или каталог из общей папки, которую указываете этот параметр.</span><span class="sxs-lookup"><span data-stu-id="6c34c-154">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="6c34c-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c34c-155">CommonParameters</span></span>
<span data-ttu-id="6c34c-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6c34c-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c34c-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c34c-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c34c-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6c34c-158">INPUTS</span></span>

### <span data-ttu-id="6c34c-159">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6c34c-159">IStorageContext</span></span>

<span data-ttu-id="6c34c-160">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="6c34c-160">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="6c34c-161">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="6c34c-161">CloudFileDirectory</span></span>

<span data-ttu-id="6c34c-162">Параметр "Directory" принимает значение типа "CloudFileDirectory" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="6c34c-162">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="6c34c-163">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="6c34c-163">CloudFileShare</span></span>

<span data-ttu-id="6c34c-164">Параметр "общий доступ" принимает значение типа "CloudFileShare" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="6c34c-164">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="6c34c-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c34c-165">OUTPUTS</span></span>

## <span data-ttu-id="6c34c-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="6c34c-166">NOTES</span></span>

## <span data-ttu-id="6c34c-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c34c-167">RELATED LINKS</span></span>

[<span data-ttu-id="6c34c-168">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6c34c-168">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="6c34c-169">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="6c34c-169">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="6c34c-170">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="6c34c-170">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="6c34c-171">Remove-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="6c34c-171">Remove-AzureStorageFile</span></span>](./Remove-AzureStorageFile.md)

[<span data-ttu-id="6c34c-172">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6c34c-172">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)

