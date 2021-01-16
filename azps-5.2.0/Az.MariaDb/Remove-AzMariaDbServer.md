---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbServer.md
ms.openlocfilehash: c495cb1372735c856224d45010728f264f73c252
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406476"
---
# <span data-ttu-id="39e70-101">Remove-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="39e70-101">Remove-AzMariaDbServer</span></span>

## <span data-ttu-id="39e70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39e70-102">SYNOPSIS</span></span>
<span data-ttu-id="39e70-103">Удаляет сервер.</span><span class="sxs-lookup"><span data-stu-id="39e70-103">Deletes a server.</span></span>

## <span data-ttu-id="39e70-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="39e70-104">SYNTAX</span></span>

### <span data-ttu-id="39e70-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="39e70-105">Delete (Default)</span></span>
```
Remove-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="39e70-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="39e70-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="39e70-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39e70-107">DESCRIPTION</span></span>
<span data-ttu-id="39e70-108">Удаляет сервер.</span><span class="sxs-lookup"><span data-stu-id="39e70-108">Deletes a server.</span></span>

## <span data-ttu-id="39e70-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="39e70-109">EXAMPLES</span></span>

### <span data-ttu-id="39e70-110">Пример 1. Удаление Приложения MariaDB</span><span class="sxs-lookup"><span data-stu-id="39e70-110">Example 1: Remove a MariaDB</span></span>
```powershell
PS C:\> Remove-AzMariaDbServer -Name mariadb-asd-01 -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="39e70-111">Эта команда удаляет MariaDB.</span><span class="sxs-lookup"><span data-stu-id="39e70-111">This command removes a MariaDB.</span></span>

### <span data-ttu-id="39e70-112">Пример 2. Удаление Мария ДВ</span><span class="sxs-lookup"><span data-stu-id="39e70-112">Example 2: Remove a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-bc-t01 -ResourceGroupName mariadb-test-qu5ov0 | Remove-AzMariaDbServer

```

<span data-ttu-id="39e70-113">Эта команда удаляет MariaDB.</span><span class="sxs-lookup"><span data-stu-id="39e70-113">This command removes a MariaDB.</span></span>

## <span data-ttu-id="39e70-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39e70-114">PARAMETERS</span></span>

### <span data-ttu-id="39e70-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39e70-115">-AsJob</span></span>
<span data-ttu-id="39e70-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="39e70-116">Run the command as a job</span></span>

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

### <span data-ttu-id="39e70-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39e70-117">-DefaultProfile</span></span>
<span data-ttu-id="39e70-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39e70-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e70-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39e70-119">-InputObject</span></span>
<span data-ttu-id="39e70-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="39e70-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39e70-121">-Name</span><span class="sxs-lookup"><span data-stu-id="39e70-121">-Name</span></span>
<span data-ttu-id="39e70-122">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="39e70-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e70-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="39e70-123">-NoWait</span></span>
<span data-ttu-id="39e70-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="39e70-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="39e70-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39e70-125">-PassThru</span></span>
<span data-ttu-id="39e70-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="39e70-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="39e70-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39e70-127">-ResourceGroupName</span></span>
<span data-ttu-id="39e70-128">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="39e70-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="39e70-129">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="39e70-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e70-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39e70-130">-SubscriptionId</span></span>
<span data-ttu-id="39e70-131">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="39e70-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e70-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39e70-132">-Confirm</span></span>
<span data-ttu-id="39e70-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="39e70-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39e70-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39e70-134">-WhatIf</span></span>
<span data-ttu-id="39e70-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39e70-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39e70-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="39e70-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39e70-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39e70-137">CommonParameters</span></span>
<span data-ttu-id="39e70-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39e70-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39e70-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39e70-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39e70-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39e70-140">INPUTS</span></span>

### <span data-ttu-id="39e70-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="39e70-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="39e70-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="39e70-142">OUTPUTS</span></span>

### <span data-ttu-id="39e70-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="39e70-143">System.Boolean</span></span>

## <span data-ttu-id="39e70-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="39e70-144">NOTES</span></span>

<span data-ttu-id="39e70-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="39e70-145">ALIASES</span></span>

<span data-ttu-id="39e70-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="39e70-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="39e70-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="39e70-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="39e70-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="39e70-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="39e70-149">INPUTOBJECT <IMariaDbIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="39e70-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="39e70-150">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="39e70-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="39e70-151">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="39e70-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="39e70-152">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="39e70-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="39e70-153">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="39e70-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="39e70-154">`[LocationName <String>]`: Название расположения.</span><span class="sxs-lookup"><span data-stu-id="39e70-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="39e70-155">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="39e70-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="39e70-156">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="39e70-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="39e70-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="39e70-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="39e70-158">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="39e70-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="39e70-159">`[SubscriptionId <String>]`. Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="39e70-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="39e70-160">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="39e70-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="39e70-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39e70-161">RELATED LINKS</span></span>
