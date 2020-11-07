---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 6dadd92955c325120b67d8faae99c7f8ae90dc5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566023"
---
# <span data-ttu-id="2cfdf-101">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2cfdf-101">New-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="2cfdf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2cfdf-102">SYNOPSIS</span></span>
<span data-ttu-id="2cfdf-103">Создание политики сохраненного доступа для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2cfdf-103">Creates a stored access policy for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cfdf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2cfdf-104">SYNTAX</span></span>

```
New-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="2cfdf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cfdf-105">DESCRIPTION</span></span>
<span data-ttu-id="2cfdf-106">Командлет **New-AzureStorageContainerStoredAccessPolicy** создает политику сохраненного доступа для контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2cfdf-106">The **New-AzureStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="2cfdf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2cfdf-107">EXAMPLES</span></span>

### <span data-ttu-id="2cfdf-108">Пример 1: Создание политики для сохраненного доступа в контейнере хранилища</span><span class="sxs-lookup"><span data-stu-id="2cfdf-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="2cfdf-109">Эта команда создает политику доступа с именем Policy01 в контейнере хранения с именем MyContainer.</span><span class="sxs-lookup"><span data-stu-id="2cfdf-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="2cfdf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2cfdf-110">PARAMETERS</span></span>

### <span data-ttu-id="2cfdf-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2cfdf-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2cfdf-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="2cfdf-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2cfdf-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="2cfdf-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2cfdf-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="2cfdf-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2cfdf-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2cfdf-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2cfdf-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="2cfdf-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2cfdf-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="2cfdf-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2cfdf-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="2cfdf-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2cfdf-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="2cfdf-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2cfdf-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="2cfdf-120">The default value is 10.</span></span>

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

### <span data-ttu-id="2cfdf-121">-Container</span><span class="sxs-lookup"><span data-stu-id="2cfdf-121">-Container</span></span>
<span data-ttu-id="2cfdf-122">Указывает имя контейнера хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2cfdf-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cfdf-123">-Context</span><span class="sxs-lookup"><span data-stu-id="2cfdf-123">-Context</span></span>
<span data-ttu-id="2cfdf-124">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="2cfdf-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2cfdf-125">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="2cfdf-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2cfdf-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cfdf-126">-DefaultProfile</span></span>
<span data-ttu-id="2cfdf-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2cfdf-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cfdf-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2cfdf-128">-ExpiryTime</span></span>
<span data-ttu-id="2cfdf-129">Указывает время, в течение которого политика хранения сохраненных прав становится недействительной.</span><span class="sxs-lookup"><span data-stu-id="2cfdf-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfdf-130">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="2cfdf-130">-Permission</span></span>
<span data-ttu-id="2cfdf-131">Определяет разрешения в политике сохранения доступа для доступа к контейнеру.</span><span class="sxs-lookup"><span data-stu-id="2cfdf-131">Specifies permissions in the stored access policy to access the container.</span></span>
<span data-ttu-id="2cfdf-132">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="2cfdf-132">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfdf-133">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="2cfdf-133">-Policy</span></span>
<span data-ttu-id="2cfdf-134">Указывает политику сохраненного доступа, которая включает разрешения для этого маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="2cfdf-134">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfdf-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2cfdf-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2cfdf-136">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="2cfdf-136">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2cfdf-137">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="2cfdf-137">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2cfdf-138">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="2cfdf-138">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2cfdf-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2cfdf-139">-StartTime</span></span>
<span data-ttu-id="2cfdf-140">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="2cfdf-140">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfdf-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cfdf-141">CommonParameters</span></span>
<span data-ttu-id="2cfdf-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2cfdf-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cfdf-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cfdf-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cfdf-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2cfdf-144">INPUTS</span></span>

### <span data-ttu-id="2cfdf-145">System. String</span><span class="sxs-lookup"><span data-stu-id="2cfdf-145">System.String</span></span>

### <span data-ttu-id="2cfdf-146">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2cfdf-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2cfdf-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cfdf-147">OUTPUTS</span></span>

### <span data-ttu-id="2cfdf-148">System. String</span><span class="sxs-lookup"><span data-stu-id="2cfdf-148">System.String</span></span>

## <span data-ttu-id="2cfdf-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="2cfdf-149">NOTES</span></span>

## <span data-ttu-id="2cfdf-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2cfdf-150">RELATED LINKS</span></span>

[<span data-ttu-id="2cfdf-151">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2cfdf-151">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="2cfdf-152">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="2cfdf-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="2cfdf-153">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2cfdf-153">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="2cfdf-154">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2cfdf-154">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)

