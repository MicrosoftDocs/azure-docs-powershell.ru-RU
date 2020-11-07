---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: f4dfc77be9006229e2919dd1a4e0cdb1dd8c548e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566363"
---
# <span data-ttu-id="27190-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="27190-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="27190-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27190-102">SYNOPSIS</span></span>
<span data-ttu-id="27190-103">Задает политику сохранения для доступа к таблице хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="27190-103">Sets the stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27190-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27190-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27190-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27190-105">DESCRIPTION</span></span>
<span data-ttu-id="27190-106">Командлет **Set-AzureStorageTableStoredAccessPolicy** задает политику сохраненных прав доступа для таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="27190-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="27190-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27190-107">EXAMPLES</span></span>

### <span data-ttu-id="27190-108">Пример 1: Настройка политики доступа в таблице с полным разрешением</span><span class="sxs-lookup"><span data-stu-id="27190-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="27190-109">Эта команда задает политику доступа с именем Policy08 для таблицы хранения с именем MyTable.</span><span class="sxs-lookup"><span data-stu-id="27190-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="27190-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27190-110">PARAMETERS</span></span>

### <span data-ttu-id="27190-111">-Context</span><span class="sxs-lookup"><span data-stu-id="27190-111">-Context</span></span>
<span data-ttu-id="27190-112">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="27190-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="27190-113">Чтобы получить контекст хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="27190-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="27190-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="27190-114">-ExpiryTime</span></span>
<span data-ttu-id="27190-115">Указывает время истечения срока действия политики для сохраненной доступа.</span><span class="sxs-lookup"><span data-stu-id="27190-115">Specifies the time at which the stored access policy expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27190-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="27190-116">-NoExpiryTime</span></span>
<span data-ttu-id="27190-117">Указывает на то, что политика доступа не содержит дату окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="27190-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="27190-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="27190-118">-NoStartTime</span></span>
<span data-ttu-id="27190-119">Указывает на то, что для времени начала задано значение $Null.</span><span class="sxs-lookup"><span data-stu-id="27190-119">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="27190-120">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="27190-120">-Permission</span></span>
<span data-ttu-id="27190-121">Определяет разрешения в политике сохранения доступа для доступа к таблице хранения.</span><span class="sxs-lookup"><span data-stu-id="27190-121">Specifies permissions in the stored access policy to access the storage table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27190-122">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="27190-122">-Policy</span></span>
<span data-ttu-id="27190-123">Задает имя для политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="27190-123">Specifies the name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27190-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="27190-124">-StartTime</span></span>
<span data-ttu-id="27190-125">Указывает время вступления в силу политики сохраненных прав доступа.</span><span class="sxs-lookup"><span data-stu-id="27190-125">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27190-126">-Таблица</span><span class="sxs-lookup"><span data-stu-id="27190-126">-Table</span></span>
<span data-ttu-id="27190-127">Указывает имя таблицы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="27190-127">Specifies the Azure storage table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27190-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27190-128">-Confirm</span></span>
<span data-ttu-id="27190-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="27190-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27190-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27190-130">-WhatIf</span></span>
<span data-ttu-id="27190-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="27190-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27190-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="27190-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27190-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27190-133">CommonParameters</span></span>
<span data-ttu-id="27190-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27190-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27190-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27190-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27190-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27190-136">INPUTS</span></span>

### <span data-ttu-id="27190-137">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="27190-137">IStorageContext</span></span>

<span data-ttu-id="27190-138">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="27190-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="27190-139">Подстрок</span><span class="sxs-lookup"><span data-stu-id="27190-139">String</span></span>

<span data-ttu-id="27190-140">Параметр "Таблица" принимает значение типа String из конвейера</span><span class="sxs-lookup"><span data-stu-id="27190-140">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="27190-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27190-141">OUTPUTS</span></span>

### <span data-ttu-id="27190-142">System. String</span><span class="sxs-lookup"><span data-stu-id="27190-142">System.String</span></span>

## <span data-ttu-id="27190-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="27190-143">NOTES</span></span>

## <span data-ttu-id="27190-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27190-144">RELATED LINKS</span></span>

[<span data-ttu-id="27190-145">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="27190-145">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="27190-146">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="27190-146">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="27190-147">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="27190-147">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="27190-148">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="27190-148">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)