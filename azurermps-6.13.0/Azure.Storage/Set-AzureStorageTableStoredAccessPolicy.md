---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 80fe36072840d112c4c8849e72deedd0a7f49d25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565995"
---
# <span data-ttu-id="250bb-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="250bb-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="250bb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="250bb-102">SYNOPSIS</span></span>
<span data-ttu-id="250bb-103">Задает политику сохранения для доступа к таблице хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="250bb-103">Sets the stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="250bb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="250bb-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="250bb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="250bb-105">DESCRIPTION</span></span>
<span data-ttu-id="250bb-106">Командлет **Set-AzureStorageTableStoredAccessPolicy** задает политику сохраненных прав доступа для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="250bb-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="250bb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="250bb-107">EXAMPLES</span></span>

### <span data-ttu-id="250bb-108">Пример 1: Настройка политики доступа в таблице с полным разрешением</span><span class="sxs-lookup"><span data-stu-id="250bb-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="250bb-109">Эта команда задает политику доступа с именем Policy08 для таблицы хранения с именем MyTable.</span><span class="sxs-lookup"><span data-stu-id="250bb-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="250bb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="250bb-110">PARAMETERS</span></span>

### <span data-ttu-id="250bb-111">-Context</span><span class="sxs-lookup"><span data-stu-id="250bb-111">-Context</span></span>
<span data-ttu-id="250bb-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="250bb-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="250bb-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="250bb-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="250bb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="250bb-114">-DefaultProfile</span></span>
<span data-ttu-id="250bb-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="250bb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="250bb-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="250bb-116">-ExpiryTime</span></span>
<span data-ttu-id="250bb-117">Указывает время истечения срока действия политики для сохраненной доступа.</span><span class="sxs-lookup"><span data-stu-id="250bb-117">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="250bb-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="250bb-118">-NoExpiryTime</span></span>
<span data-ttu-id="250bb-119">Указывает на то, что политика доступа не содержит дату окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="250bb-119">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="250bb-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="250bb-120">-NoStartTime</span></span>
<span data-ttu-id="250bb-121">Указывает на то, что для времени начала задано значение $Null.</span><span class="sxs-lookup"><span data-stu-id="250bb-121">Indicates that the start time is set to $Null.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="250bb-122">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="250bb-122">-Permission</span></span>
<span data-ttu-id="250bb-123">Определяет разрешения в политике сохранения доступа для доступа к таблице хранения.</span><span class="sxs-lookup"><span data-stu-id="250bb-123">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="250bb-124">Важно отметить, что это строка, например `rwd` (для чтения, записи и удаления).</span><span class="sxs-lookup"><span data-stu-id="250bb-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="250bb-125">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="250bb-125">-Policy</span></span>
<span data-ttu-id="250bb-126">Задает имя для политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="250bb-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="250bb-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="250bb-127">-StartTime</span></span>
<span data-ttu-id="250bb-128">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="250bb-128">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="250bb-129">-Таблица</span><span class="sxs-lookup"><span data-stu-id="250bb-129">-Table</span></span>
<span data-ttu-id="250bb-130">Указывает имя таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="250bb-130">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="250bb-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="250bb-131">-Confirm</span></span>
<span data-ttu-id="250bb-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="250bb-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="250bb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="250bb-133">-WhatIf</span></span>
<span data-ttu-id="250bb-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="250bb-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="250bb-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="250bb-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="250bb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="250bb-136">CommonParameters</span></span>
<span data-ttu-id="250bb-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="250bb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="250bb-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="250bb-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="250bb-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="250bb-139">INPUTS</span></span>

### <span data-ttu-id="250bb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="250bb-140">System.String</span></span>

### <span data-ttu-id="250bb-141">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="250bb-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="250bb-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="250bb-142">OUTPUTS</span></span>

### <span data-ttu-id="250bb-143">System. String</span><span class="sxs-lookup"><span data-stu-id="250bb-143">System.String</span></span>

## <span data-ttu-id="250bb-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="250bb-144">NOTES</span></span>

## <span data-ttu-id="250bb-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="250bb-145">RELATED LINKS</span></span>

[<span data-ttu-id="250bb-146">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="250bb-146">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="250bb-147">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="250bb-147">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="250bb-148">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="250bb-148">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="250bb-149">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="250bb-149">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)