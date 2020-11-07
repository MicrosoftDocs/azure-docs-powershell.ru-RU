---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShareStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: b88a03f38ff3e88b6fbbe7b966498e547f8cc026
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560603"
---
# <span data-ttu-id="d3afd-101">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d3afd-101">Remove-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="d3afd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3afd-102">SYNOPSIS</span></span>
<span data-ttu-id="d3afd-103">Удаление политики сохраненного доступа из общей папке хранилища.</span><span class="sxs-lookup"><span data-stu-id="d3afd-103">Removes a stored access policy from a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3afd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3afd-104">SYNTAX</span></span>

```
Remove-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3afd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3afd-105">DESCRIPTION</span></span>
<span data-ttu-id="d3afd-106">Командлет **Remove-AzureStorageShareStoredAccessPolicy** удаляет политику доступа из хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d3afd-106">The **Remove-AzureStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="d3afd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3afd-107">EXAMPLES</span></span>

### <span data-ttu-id="d3afd-108">Пример 1: Удаление политики сохраненного доступа из общего доступа к хранилищу Azure</span><span class="sxs-lookup"><span data-stu-id="d3afd-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="d3afd-109">Эта команда удаляет политику сохраненного доступа с именем GeneralPolicy из ContosoShare.</span><span class="sxs-lookup"><span data-stu-id="d3afd-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="d3afd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3afd-110">PARAMETERS</span></span>

### <span data-ttu-id="d3afd-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d3afd-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d3afd-112">Указывает интервал времени ожидания клиента (в секундах) для одного запроса на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="d3afd-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d3afd-113">Если предыдущий вызов завершается с ошибкой в указанном интервале, этот командлет повторно пытается выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="d3afd-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d3afd-114">Если этот командлет не получает успешный ответ до истечения интервала, этот командлет возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d3afd-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d3afd-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d3afd-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d3afd-116">Задает максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="d3afd-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d3afd-117">Вы можете использовать этот параметр, чтобы ограничить параллелизм для регулирования локального ЦП и использования пропускной способности, указав максимальное количество одновременных сетевых вызовов.</span><span class="sxs-lookup"><span data-stu-id="d3afd-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d3afd-118">Указанное значение является абсолютным числом и не умножается на количество ядер.</span><span class="sxs-lookup"><span data-stu-id="d3afd-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d3afd-119">Этот параметр помогает уменьшить количество проблем с подключением к сети в средах с низкой пропускной способностью, например 100 килобит в секунду.</span><span class="sxs-lookup"><span data-stu-id="d3afd-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d3afd-120">Значение по умолчанию — 10.</span><span class="sxs-lookup"><span data-stu-id="d3afd-120">The default value is 10.</span></span>

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

### <span data-ttu-id="d3afd-121">-Context</span><span class="sxs-lookup"><span data-stu-id="d3afd-121">-Context</span></span>
<span data-ttu-id="d3afd-122">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d3afd-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d3afd-123">Чтобы получить контекст хранения, используйте командлет [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="d3afd-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="d3afd-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3afd-124">-PassThru</span></span>
<span data-ttu-id="d3afd-125">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="d3afd-125">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="d3afd-126">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d3afd-126">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="d3afd-127">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="d3afd-127">-Policy</span></span>
<span data-ttu-id="d3afd-128">Указывает имя политики хранения, которая удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="d3afd-128">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d3afd-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d3afd-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d3afd-130">Указывает длину тайм-аута для серверной части запроса.</span><span class="sxs-lookup"><span data-stu-id="d3afd-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="d3afd-131">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="d3afd-131">-ShareName</span></span>
<span data-ttu-id="d3afd-132">Указывает имя общего хранилища, для которого этот командлет удаляет политику.</span><span class="sxs-lookup"><span data-stu-id="d3afd-132">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3afd-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3afd-133">-Confirm</span></span>
<span data-ttu-id="d3afd-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d3afd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3afd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3afd-135">-WhatIf</span></span>
<span data-ttu-id="d3afd-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d3afd-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3afd-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d3afd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3afd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3afd-138">CommonParameters</span></span>
<span data-ttu-id="d3afd-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3afd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3afd-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3afd-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3afd-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3afd-141">INPUTS</span></span>

### <span data-ttu-id="d3afd-142">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d3afd-142">IStorageContext</span></span>

<span data-ttu-id="d3afd-143">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d3afd-143">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="d3afd-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3afd-144">OUTPUTS</span></span>

### <span data-ttu-id="d3afd-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d3afd-145">System.Boolean</span></span>

## <span data-ttu-id="d3afd-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3afd-146">NOTES</span></span>

## <span data-ttu-id="d3afd-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3afd-147">RELATED LINKS</span></span>

[<span data-ttu-id="d3afd-148">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d3afd-148">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="d3afd-149">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d3afd-149">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="d3afd-150">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d3afd-150">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="d3afd-151">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d3afd-151">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)