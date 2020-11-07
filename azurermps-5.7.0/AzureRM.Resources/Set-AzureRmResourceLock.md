---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
ms.openlocfilehash: 12d1a696bd37cd6844a54f32f60bf70eaba6a0b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567931"
---
# <span data-ttu-id="87032-101">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="87032-101">Set-AzureRmResourceLock</span></span>

## <span data-ttu-id="87032-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87032-102">SYNOPSIS</span></span>
<span data-ttu-id="87032-103">Изменяет блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="87032-103">Modifies a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87032-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87032-104">SYNTAX</span></span>

### <span data-ttu-id="87032-105">BySpecifiedScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="87032-105">BySpecifiedScope (Default)</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87032-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="87032-106">ByResourceGroup</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87032-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="87032-107">ByResourceGroupLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87032-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="87032-108">BySubscription</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87032-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="87032-109">BySubscriptionLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87032-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="87032-110">ByTenantLevel</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87032-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="87032-111">ByLockId</span></span>
```
Set-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87032-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87032-112">DESCRIPTION</span></span>
<span data-ttu-id="87032-113">Командлет **Set-AzureRmResourceLock** изменяет блокировку ресурса.</span><span class="sxs-lookup"><span data-stu-id="87032-113">The **Set-AzureRmResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="87032-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87032-114">EXAMPLES</span></span>

### <span data-ttu-id="87032-115">Пример 1: обновление заметок для блокировки</span><span class="sxs-lookup"><span data-stu-id="87032-115">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="87032-116">Эта команда обновляет Примечание для блокировки с именем ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="87032-116">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="87032-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87032-117">PARAMETERS</span></span>

### <span data-ttu-id="87032-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="87032-118">-ApiVersion</span></span>
<span data-ttu-id="87032-119">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="87032-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="87032-120">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="87032-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="87032-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87032-121">-DefaultProfile</span></span>
<span data-ttu-id="87032-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="87032-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87032-123">-Force</span><span class="sxs-lookup"><span data-stu-id="87032-123">-Force</span></span>
<span data-ttu-id="87032-124">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="87032-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="87032-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="87032-125">-InformationAction</span></span>
<span data-ttu-id="87032-126">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="87032-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="87032-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="87032-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="87032-128">Продолжал</span><span class="sxs-lookup"><span data-stu-id="87032-128">Continue</span></span>
- <span data-ttu-id="87032-129">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="87032-129">Ignore</span></span>
- <span data-ttu-id="87032-130">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="87032-130">Inquire</span></span>
- <span data-ttu-id="87032-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="87032-131">SilentlyContinue</span></span>
- <span data-ttu-id="87032-132">Остановить</span><span class="sxs-lookup"><span data-stu-id="87032-132">Stop</span></span>
- <span data-ttu-id="87032-133">Рвать</span><span class="sxs-lookup"><span data-stu-id="87032-133">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87032-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="87032-134">-InformationVariable</span></span>
<span data-ttu-id="87032-135">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="87032-135">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87032-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="87032-136">-LockId</span></span>
<span data-ttu-id="87032-137">Указывает идентификатор блокировки, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="87032-137">Specifies the ID of the lock that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87032-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="87032-138">-LockLevel</span></span>
<span data-ttu-id="87032-139">Задает уровень блокировки.</span><span class="sxs-lookup"><span data-stu-id="87032-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="87032-140">В настоящее время единственным допустимым значением является CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="87032-140">Currently, the only valid value is CanNotDelete.</span></span>

```yaml
Type: LockLevel
Parameter Sets: (All)
Aliases: Level

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87032-141">-LockName</span><span class="sxs-lookup"><span data-stu-id="87032-141">-LockName</span></span>
<span data-ttu-id="87032-142">Указывает имя блокировки, измененной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="87032-142">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87032-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="87032-143">-LockNotes</span></span>
<span data-ttu-id="87032-144">Задает заметки для блокировки.</span><span class="sxs-lookup"><span data-stu-id="87032-144">Specifies the notes for the lock.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Notes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87032-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="87032-145">-Pre</span></span>
<span data-ttu-id="87032-146">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="87032-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="87032-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87032-147">-ResourceGroupName</span></span>
<span data-ttu-id="87032-148">Указывает имя группы ресурсов, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="87032-148">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87032-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="87032-149">-ResourceName</span></span>
<span data-ttu-id="87032-150">Указывает имя ресурса, к которому применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="87032-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="87032-151">Например, чтобы указать базу данных, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="87032-151">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="87032-152">`/`База данных сервера</span><span class="sxs-lookup"><span data-stu-id="87032-152">Server`/`Database</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87032-153">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="87032-153">-ResourceType</span></span>
<span data-ttu-id="87032-154">Указывает тип ресурса, к которому применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="87032-154">Specifies the resource type for which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87032-155">-Scope</span><span class="sxs-lookup"><span data-stu-id="87032-155">-Scope</span></span>
<span data-ttu-id="87032-156">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="87032-156">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="87032-157">Например, чтобы указать базу данных, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="87032-157">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="87032-158">`/subscriptions/`Идентификатор подписки имя `/resourceGroups/` группы ресурсов имя `/providers/Microsoft.Sql/servers/` сервера `/databases/` базы данных</span><span class="sxs-lookup"><span data-stu-id="87032-158">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="87032-159">Чтобы указать группу ресурсов, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="87032-159">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="87032-160">`/subscriptions/``/resourceGroups/`имя группы ресурсов для идентификатора подписки</span><span class="sxs-lookup"><span data-stu-id="87032-160">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87032-161">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="87032-161">-TenantLevel</span></span>
<span data-ttu-id="87032-162">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="87032-162">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87032-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87032-163">-Confirm</span></span>
<span data-ttu-id="87032-164">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="87032-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87032-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87032-165">-WhatIf</span></span>
<span data-ttu-id="87032-166">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="87032-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87032-167">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="87032-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87032-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87032-168">CommonParameters</span></span>
<span data-ttu-id="87032-169">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87032-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87032-170">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87032-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87032-171">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87032-171">INPUTS</span></span>

### <span data-ttu-id="87032-172">Ничего</span><span class="sxs-lookup"><span data-stu-id="87032-172">None</span></span>
<span data-ttu-id="87032-173">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="87032-173">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="87032-174">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87032-174">OUTPUTS</span></span>

### <span data-ttu-id="87032-175">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="87032-175">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="87032-176">Пуск</span><span class="sxs-lookup"><span data-stu-id="87032-176">NOTES</span></span>

## <span data-ttu-id="87032-177">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87032-177">RELATED LINKS</span></span>

[<span data-ttu-id="87032-178">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="87032-178">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="87032-179">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="87032-179">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="87032-180">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="87032-180">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

