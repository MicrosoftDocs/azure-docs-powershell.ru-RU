---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
ms.openlocfilehash: b6323cd751d25038ff6705cee45594796d782326
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98418780"
---
# <span data-ttu-id="58e24-101">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="58e24-101">Get-AzStorageShare</span></span>

## <span data-ttu-id="58e24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58e24-102">SYNOPSIS</span></span>
<span data-ttu-id="58e24-103">Возвращает список файловой папки.</span><span class="sxs-lookup"><span data-stu-id="58e24-103">Gets a list of file shares.</span></span>

## <span data-ttu-id="58e24-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="58e24-104">SYNTAX</span></span>

### <span data-ttu-id="58e24-105">MatchingPrefix (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="58e24-105">MatchingPrefix (Default)</span></span>
```
Get-AzStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="58e24-106">Конкретные</span><span class="sxs-lookup"><span data-stu-id="58e24-106">Specific</span></span>
```
Get-AzStorageShare [-Name] <String> [[-SnapshotTime] <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="58e24-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58e24-107">DESCRIPTION</span></span>
<span data-ttu-id="58e24-108">Для учетной записи хранения с его учетной записью возвращается список файловой папки **Get-AzStorageShare.**</span><span class="sxs-lookup"><span data-stu-id="58e24-108">The **Get-AzStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="58e24-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="58e24-109">EXAMPLES</span></span>

### <span data-ttu-id="58e24-110">Пример 1. Получить файловую папку</span><span class="sxs-lookup"><span data-stu-id="58e24-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="58e24-111">Эта команда получает файл с именем ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="58e24-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="58e24-112">Пример 2. Получить все файловые папки, которые начинаются со строки</span><span class="sxs-lookup"><span data-stu-id="58e24-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "Contoso"
```

<span data-ttu-id="58e24-113">Эта команда возвращает все папки с именами, имена которых начинаются с Contoso.</span><span class="sxs-lookup"><span data-stu-id="58e24-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="58e24-114">Пример 3. Получить все файловые папки в заданный контекст</span><span class="sxs-lookup"><span data-stu-id="58e24-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzStorageContext -Local
PS C:\> Get-AzStorageShare -Context $Context
```

<span data-ttu-id="58e24-115">Первая команда использует командлет **New-AzStorageContext** для создания контекста с использованием параметра *Local,* а затем сохраняет этот объект контекста в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="58e24-115">The first command uses the **New-AzStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>
<span data-ttu-id="58e24-116">Вторая команда получает папки с файлами для контекстного объекта, $Context.</span><span class="sxs-lookup"><span data-stu-id="58e24-116">The second command gets the file shares for the context object stored in $Context.</span></span>

### <span data-ttu-id="58e24-117">Пример 4. Снимок файла с именем определенного файла и моментальный снимок</span><span class="sxs-lookup"><span data-stu-id="58e24-117">Example 4: Get a file share snapshot with specific share name and SnapshotTime</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

<span data-ttu-id="58e24-118">Эта команда получает моментальный снимок файловой папки с конкретным именем и временем моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="58e24-118">This command gets a file share snapshot with specific share name and SnapshotTime.</span></span>

## <span data-ttu-id="58e24-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58e24-119">PARAMETERS</span></span>

### <span data-ttu-id="58e24-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="58e24-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="58e24-121">Указывает интервал времени и времени, в секундах, для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="58e24-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="58e24-122">Если предыдущий вызов не сошел с заданного интервала, этот cmdlet получает запрос повторно.</span><span class="sxs-lookup"><span data-stu-id="58e24-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="58e24-123">Если этот cmdlet не получает успешного отклика до интервала, он возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="58e24-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e24-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="58e24-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="58e24-125">Указывает максимальное число сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="58e24-125">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="58e24-126">С помощью этого параметра можно ограничить одновременное использование локального ЦП и пропускной способности, указав максимальное количество сетевых звонков одновременно.</span><span class="sxs-lookup"><span data-stu-id="58e24-126">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="58e24-127">Указанное значение является абсолютным и не умножается на основное.</span><span class="sxs-lookup"><span data-stu-id="58e24-127">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="58e24-128">Этот параметр помогает уменьшить количество проблем с сетевым подключением при низкой пропускной способности, например 100 КБ в секунду.</span><span class="sxs-lookup"><span data-stu-id="58e24-128">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="58e24-129">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="58e24-129">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e24-130">-Контекст</span><span class="sxs-lookup"><span data-stu-id="58e24-130">-Context</span></span>
<span data-ttu-id="58e24-131">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="58e24-131">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="58e24-132">Для получения контекста используйте [cmdlet New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="58e24-132">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58e24-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58e24-133">-DefaultProfile</span></span>
<span data-ttu-id="58e24-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="58e24-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e24-135">-Name</span><span class="sxs-lookup"><span data-stu-id="58e24-135">-Name</span></span>
<span data-ttu-id="58e24-136">Имя файловой папки.</span><span class="sxs-lookup"><span data-stu-id="58e24-136">Specifies the name of the file share.</span></span>
<span data-ttu-id="58e24-137">Этот cmdlet возвращает файловую папку, заданную этим параметром, или ничего, если указать имя файла, который не существует.</span><span class="sxs-lookup"><span data-stu-id="58e24-137">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e24-138">-Префикс</span><span class="sxs-lookup"><span data-stu-id="58e24-138">-Prefix</span></span>
<span data-ttu-id="58e24-139">Указывает префикс для файловых акций.</span><span class="sxs-lookup"><span data-stu-id="58e24-139">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="58e24-140">Этот командлет получает файлы в папках, которые соответствуют префиксу, указанному этим параметром, или не должны совпадать с указанным префиксом.</span><span class="sxs-lookup"><span data-stu-id="58e24-140">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: MatchingPrefix
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e24-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="58e24-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="58e24-142">Определяет продолжительность периода времени ожидания для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="58e24-142">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e24-143">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="58e24-143">-SnapshotTime</span></span>
<span data-ttu-id="58e24-144">Моментальный снимок моментального снимка, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="58e24-144">SnapshotTime of the file share snapshot to be received.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: Specific
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58e24-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58e24-145">CommonParameters</span></span>
<span data-ttu-id="58e24-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58e24-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58e24-147">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58e24-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58e24-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58e24-148">INPUTS</span></span>

### <span data-ttu-id="58e24-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="58e24-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="58e24-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="58e24-150">OUTPUTS</span></span>

### <span data-ttu-id="58e24-151">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="58e24-151">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="58e24-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="58e24-152">NOTES</span></span>

## <span data-ttu-id="58e24-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58e24-153">RELATED LINKS</span></span>

[<span data-ttu-id="58e24-154">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="58e24-154">New-AzStorageShare</span></span>](./New-AzStorageShare.md)

[<span data-ttu-id="58e24-155">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="58e24-155">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)