---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 7cc09813f03e5424b7d44b7a56810167ca5affba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721290"
---
# <span data-ttu-id="3ee2f-101">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3ee2f-101">Remove-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="3ee2f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ee2f-102">SYNOPSIS</span></span>
<span data-ttu-id="3ee2f-103">Удаляет запись из ACL файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3ee2f-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="3ee2f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ee2f-104">SYNTAX</span></span>

### <span data-ttu-id="3ee2f-105">RemoveByACLObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3ee2f-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ee2f-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="3ee2f-106">RemoveSpecificACE</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ee2f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ee2f-107">DESCRIPTION</span></span>
<span data-ttu-id="3ee2f-108">Командлет **Remove-AzDataLakeStoreItemAclEntry** удаляет запись (ACE) из списка управления доступом (ACL) для файла или папки в Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3ee2f-108">The **Remove-AzDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="3ee2f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ee2f-109">EXAMPLES</span></span>

### <span data-ttu-id="3ee2f-110">Пример 1: Удаление учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="3ee2f-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="3ee2f-111">Эта команда удаляет ACE пользователя для Patti Белова из учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="3ee2f-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

### <span data-ttu-id="3ee2f-112">Пример 2: рекурсивное удаление записи пользователя</span><span class="sxs-lookup"><span data-stu-id="3ee2f-112">Example 2: Remove a user entry recursively</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Recurse -Concurrency 128
```

### <span data-ttu-id="3ee2f-113">Пример 3: рекурсивное удаление разрешений для записи ACE с помощью объекта ACL</span><span class="sxs-lookup"><span data-stu-id="3ee2f-113">Example 3: Remove permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1,default:user:userid1
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="3ee2f-114">Эта команда удаляет ACE пользователя для Patti Белова из корня и рекурсивно из всех ее подкаталогов и файлов для ContosoADL учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3ee2f-114">This command removes the user ACE for Patti Fuller from the root and recursively from all it's subdirectories and files for account ContosoADL.</span></span>

## <span data-ttu-id="3ee2f-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ee2f-115">PARAMETERS</span></span>

### <span data-ttu-id="3ee2f-116">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="3ee2f-116">-Account</span></span>
<span data-ttu-id="3ee2f-117">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3ee2f-117">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee2f-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="3ee2f-118">-AceType</span></span>
<span data-ttu-id="3ee2f-119">Указывает тип удаляемого элемента управления доступом.</span><span class="sxs-lookup"><span data-stu-id="3ee2f-119">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="3ee2f-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3ee2f-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3ee2f-121">Пользователям</span><span class="sxs-lookup"><span data-stu-id="3ee2f-121">User</span></span>
- <span data-ttu-id="3ee2f-122">Сгруппирован</span><span class="sxs-lookup"><span data-stu-id="3ee2f-122">Group</span></span>
- <span data-ttu-id="3ee2f-123">Маски</span><span class="sxs-lookup"><span data-stu-id="3ee2f-123">Mask</span></span>
- <span data-ttu-id="3ee2f-124">Другие</span><span class="sxs-lookup"><span data-stu-id="3ee2f-124">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: RemoveSpecificACE
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee2f-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="3ee2f-125">-Acl</span></span>
<span data-ttu-id="3ee2f-126">Указывает объект ACL, содержащий записи, которые нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="3ee2f-126">Specifies the ACL object that contains the entries to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: RemoveByACLObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee2f-127">-Параллелизм</span><span class="sxs-lookup"><span data-stu-id="3ee2f-127">-Concurrency</span></span>
<span data-ttu-id="3ee2f-128">Количество параллельных файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="3ee2f-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="3ee2f-129">Необязательно: будет выбрано разумное значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3ee2f-129">Optional: a reasonable default will be selected</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee2f-130">-Default</span><span class="sxs-lookup"><span data-stu-id="3ee2f-130">-Default</span></span>
<span data-ttu-id="3ee2f-131">Указывает на то, что эта операция удаляет запись ACE по умолчанию из указанного списка ACL.</span><span class="sxs-lookup"><span data-stu-id="3ee2f-131">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveSpecificACE
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee2f-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ee2f-132">-DefaultProfile</span></span>
<span data-ttu-id="3ee2f-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ee2f-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee2f-134">-ID</span><span class="sxs-lookup"><span data-stu-id="3ee2f-134">-Id</span></span>
<span data-ttu-id="3ee2f-135">Указывает идентификатор объекта пользователя, группы или субъекта-службы AzureActive каталога, для которого нужно удалить элемент управления доступом.</span><span class="sxs-lookup"><span data-stu-id="3ee2f-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: RemoveSpecificACE
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee2f-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ee2f-136">-PassThru</span></span>
<span data-ttu-id="3ee2f-137">Указывает, что должен возвращаться логический ответ, указывающий результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="3ee2f-137">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee2f-138">-Path</span><span class="sxs-lookup"><span data-stu-id="3ee2f-138">-Path</span></span>
<span data-ttu-id="3ee2f-139">Указывает путь к Data Lake Store для элемента, из которого нужно удалить запись ACE, начиная с корневого каталога (/).</span><span class="sxs-lookup"><span data-stu-id="3ee2f-139">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee2f-140">-Рекурсия</span><span class="sxs-lookup"><span data-stu-id="3ee2f-140">-Recurse</span></span>
<span data-ttu-id="3ee2f-141">Указывает, что ACL нужно удалить рекурсивно для дочерних подкаталогов и файлов.</span><span class="sxs-lookup"><span data-stu-id="3ee2f-141">Indicates the ACL to be removed recursively to the child subdirectories and files</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee2f-142">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="3ee2f-142">-ShowProgress</span></span>
<span data-ttu-id="3ee2f-143">После перезагрузки будет выдано состояние "ход выполнения".</span><span class="sxs-lookup"><span data-stu-id="3ee2f-143">If passed then progress status is showed.</span></span> <span data-ttu-id="3ee2f-144">Применимо только в том случае, если выполняется рекурсивное удаление списка ACL.</span><span class="sxs-lookup"><span data-stu-id="3ee2f-144">Only applicable when recursive Acl remove is done.</span></span>

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

### <span data-ttu-id="3ee2f-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ee2f-145">-Confirm</span></span>
<span data-ttu-id="3ee2f-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3ee2f-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee2f-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ee2f-147">-WhatIf</span></span>
<span data-ttu-id="3ee2f-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3ee2f-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ee2f-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3ee2f-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee2f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ee2f-150">CommonParameters</span></span>
<span data-ttu-id="3ee2f-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ee2f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ee2f-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ee2f-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ee2f-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ee2f-153">INPUTS</span></span>

### <span data-ttu-id="3ee2f-154">System. String</span><span class="sxs-lookup"><span data-stu-id="3ee2f-154">System.String</span></span>

### <span data-ttu-id="3ee2f-155">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="3ee2f-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="3ee2f-156">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="3ee2f-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="3ee2f-157">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + AceType</span><span class="sxs-lookup"><span data-stu-id="3ee2f-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="3ee2f-158">System. GUID</span><span class="sxs-lookup"><span data-stu-id="3ee2f-158">System.Guid</span></span>

### <span data-ttu-id="3ee2f-159">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3ee2f-159">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="3ee2f-160">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3ee2f-160">System.Int32</span></span>

## <span data-ttu-id="3ee2f-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ee2f-161">OUTPUTS</span></span>

### <span data-ttu-id="3ee2f-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3ee2f-162">System.Boolean</span></span>

## <span data-ttu-id="3ee2f-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ee2f-163">NOTES</span></span>

## <span data-ttu-id="3ee2f-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ee2f-164">RELATED LINKS</span></span>

[<span data-ttu-id="3ee2f-165">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3ee2f-165">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)

