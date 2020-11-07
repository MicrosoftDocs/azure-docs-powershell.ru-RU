---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: 6908bc4d474d0dbe9df045332f3820b5f7536dac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567015"
---
# <span data-ttu-id="29b6f-101">Set-AzureRmDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="29b6f-101">Set-AzureRmDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="29b6f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="29b6f-102">SYNOPSIS</span></span>
<span data-ttu-id="29b6f-103">Задает или удаляет время окончания срока действия файла в учетной записи Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="29b6f-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29b6f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="29b6f-104">SYNTAX</span></span>

### <span data-ttu-id="29b6f-105">SetAbsoluteNeverExpireExpiry (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="29b6f-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29b6f-106">SetRelativeExpiry</span><span class="sxs-lookup"><span data-stu-id="29b6f-106">SetRelativeExpiry</span></span>
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-RelativeFileExpiryOption] <PathRelativeExpiryOptions>] [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29b6f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29b6f-107">DESCRIPTION</span></span>
<span data-ttu-id="29b6f-108">Командлет **Set-AzureRmDataLakeStoreItemExpiry** задает или удаляет время окончания для файла в учетной записи Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="29b6f-108">The **Set-AzureRmDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="29b6f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="29b6f-109">EXAMPLES</span></span>

### <span data-ttu-id="29b6f-110">Пример 1: Установка срока действия для файла</span><span class="sxs-lookup"><span data-stu-id="29b6f-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="29b6f-111">Задает срок действия файла в myfile.txt учетной записи в ContosoADL в два часа.</span><span class="sxs-lookup"><span data-stu-id="29b6f-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="29b6f-112">Это приведет к истечении срока действия файла (помечается для удаления) в два часа.</span><span class="sxs-lookup"><span data-stu-id="29b6f-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="29b6f-113">Пример 2: удаление срока действия для файла</span><span class="sxs-lookup"><span data-stu-id="29b6f-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="29b6f-114">Удаление срока действия, установленного ранее, для файла "myfile.txt" в учетной записи "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="29b6f-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="29b6f-115">Это означает, что срок действия файла не истечет автоматически (помечать для удаления), и его необходимо будет удалить вручную или установить срок действия.</span><span class="sxs-lookup"><span data-stu-id="29b6f-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>


### <span data-ttu-id="29b6f-116">Пример 3: Настройка срока действия файла относительно текущего времени</span><span class="sxs-lookup"><span data-stu-id="29b6f-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="29b6f-117">Первая команда задает время истечения срока действия файла/myfile.txt 240 секунды относительно текущего времени на сервере.</span><span class="sxs-lookup"><span data-stu-id="29b6f-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>

<span data-ttu-id="29b6f-118">Вторая команда задает время истечения срока действия файла/myfile.txt 240 секунд относительно времени создания на сервере.</span><span class="sxs-lookup"><span data-stu-id="29b6f-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="29b6f-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="29b6f-119">PARAMETERS</span></span>

### <span data-ttu-id="29b6f-120">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="29b6f-120">-Account</span></span>
<span data-ttu-id="29b6f-121">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="29b6f-121">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29b6f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29b6f-122">-DefaultProfile</span></span>
<span data-ttu-id="29b6f-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="29b6f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29b6f-124">-Срок действия</span><span class="sxs-lookup"><span data-stu-id="29b6f-124">-Expiration</span></span>
<span data-ttu-id="29b6f-125">Абсолютное время окончания срока действия указанного файла.</span><span class="sxs-lookup"><span data-stu-id="29b6f-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="29b6f-126">Если значение не указано или равно MaxValue, срок действия файла не ограничен.</span><span class="sxs-lookup"><span data-stu-id="29b6f-126">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: Set expiry as Absolute or NeverExpire
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29b6f-127">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="29b6f-127">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="29b6f-128">Относительные параметры срока действия.</span><span class="sxs-lookup"><span data-stu-id="29b6f-128">Relative expiry options.</span></span> <span data-ttu-id="29b6f-129">RelativeToNow или RelativeToCreationDate являются текущими параметрами</span><span class="sxs-lookup"><span data-stu-id="29b6f-129">RelativeToNow or RelativeToCreationDate are current options</span></span>
```yaml
Type: PathRelativeExpiryOptions
Parameter Sets: Set expiry as relative to creation or now
Aliases: 
Accepted values: RelativeToNow, RelativeToCreationDate

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29b6f-130">-Path</span><span class="sxs-lookup"><span data-stu-id="29b6f-130">-Path</span></span>
<span data-ttu-id="29b6f-131">Задает путь к файлу Data Lake Store для элемента, для которого нужно задать или удалить срок действия.</span><span class="sxs-lookup"><span data-stu-id="29b6f-131">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29b6f-132">-RelativeTime</span><span class="sxs-lookup"><span data-stu-id="29b6f-132">-RelativeTime</span></span>
<span data-ttu-id="29b6f-133">Относительное время (в миллисекундах), по отношению к моменту и времени создания</span><span class="sxs-lookup"><span data-stu-id="29b6f-133">The relative time in milliseconds with respect to now or creation time</span></span>
```yaml
Type: Int64
Parameter Sets: Set expiry as relative to creation or now
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29b6f-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29b6f-134">-Confirm</span></span>
<span data-ttu-id="29b6f-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="29b6f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29b6f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29b6f-136">-WhatIf</span></span>
<span data-ttu-id="29b6f-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="29b6f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29b6f-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="29b6f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29b6f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29b6f-139">CommonParameters</span></span>
<span data-ttu-id="29b6f-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="29b6f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29b6f-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29b6f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29b6f-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="29b6f-142">INPUTS</span></span>

### <span data-ttu-id="29b6f-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="29b6f-143">None</span></span>
<span data-ttu-id="29b6f-144">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="29b6f-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="29b6f-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="29b6f-145">OUTPUTS</span></span>

### <span data-ttu-id="29b6f-146">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="29b6f-146">DataLakeStoreItem</span></span>
<span data-ttu-id="29b6f-147">Обновленный файл с новым временем истечения срока действия.</span><span class="sxs-lookup"><span data-stu-id="29b6f-147">The updated file with a new expiration time.</span></span>

## <span data-ttu-id="29b6f-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="29b6f-148">NOTES</span></span>
<span data-ttu-id="29b6f-149">Alias (псевдоним): Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="29b6f-149">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="29b6f-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29b6f-150">RELATED LINKS</span></span>

[<span data-ttu-id="29b6f-151">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="29b6f-151">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)
