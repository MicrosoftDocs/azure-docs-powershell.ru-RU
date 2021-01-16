---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 53f251b001b4e2f6319840079e9db3111c00b006
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397172"
---
# <span data-ttu-id="57269-101">Remove-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="57269-101">Remove-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="57269-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57269-102">SYNOPSIS</span></span>
<span data-ttu-id="57269-103">Удаляет экземпляр поставщика для указанной подписки, группы ресурсов, имени SapMonitor и имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="57269-103">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="57269-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="57269-104">SYNTAX</span></span>

### <span data-ttu-id="57269-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57269-105">Delete (Default)</span></span>
```
Remove-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="57269-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="57269-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="57269-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57269-107">DESCRIPTION</span></span>
<span data-ttu-id="57269-108">Удаляет экземпляр поставщика для указанной подписки, группы ресурсов, имени sapMonitor и имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="57269-108">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="57269-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="57269-109">EXAMPLES</span></span>

### <span data-ttu-id="57269-110">Пример 1. Удаление экземпляра монитора SAP по имени</span><span class="sxs-lookup"><span data-stu-id="57269-110">Example 1: Remove instance of SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

```

<span data-ttu-id="57269-111">Эта команда удаляет экземпляр монитора SAP по имени.</span><span class="sxs-lookup"><span data-stu-id="57269-111">This command removes instance of SAP monitor by name.</span></span>

### <span data-ttu-id="57269-112">Пример 2. Удаление экземпляра монитора SAP для объекта</span><span class="sxs-lookup"><span data-stu-id="57269-112">Example 2: Remove instance of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t01
PS C:\> Remove-AzSapMonitorProviderInstance -InputObject $sapIns

```

<span data-ttu-id="57269-113">Эта команда удаляет экземпляр монитора SAP для объекта.</span><span class="sxs-lookup"><span data-stu-id="57269-113">This command removes instance of SAP monitor by object.</span></span>

## <span data-ttu-id="57269-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57269-114">PARAMETERS</span></span>

### <span data-ttu-id="57269-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57269-115">-AsJob</span></span>
<span data-ttu-id="57269-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="57269-116">Run the command as a job</span></span>

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

### <span data-ttu-id="57269-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57269-117">-DefaultProfile</span></span>
<span data-ttu-id="57269-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57269-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57269-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57269-119">-InputObject</span></span>
<span data-ttu-id="57269-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="57269-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57269-121">-Name</span><span class="sxs-lookup"><span data-stu-id="57269-121">-Name</span></span>
<span data-ttu-id="57269-122">Имя экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="57269-122">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57269-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="57269-123">-NoWait</span></span>
<span data-ttu-id="57269-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="57269-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="57269-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57269-125">-PassThru</span></span>
<span data-ttu-id="57269-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="57269-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="57269-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57269-127">-ResourceGroupName</span></span>
<span data-ttu-id="57269-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="57269-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="57269-129">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="57269-129">-SapMonitorName</span></span>
<span data-ttu-id="57269-130">Имя ресурса sap monitor.</span><span class="sxs-lookup"><span data-stu-id="57269-130">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="57269-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57269-131">-SubscriptionId</span></span>
<span data-ttu-id="57269-132">Идентификация подписки, однозначно определяемая подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="57269-132">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="57269-133">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="57269-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="57269-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57269-134">-Confirm</span></span>
<span data-ttu-id="57269-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57269-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57269-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57269-136">-WhatIf</span></span>
<span data-ttu-id="57269-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57269-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57269-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="57269-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57269-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57269-139">CommonParameters</span></span>
<span data-ttu-id="57269-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57269-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57269-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57269-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57269-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57269-142">INPUTS</span></span>

### <span data-ttu-id="57269-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="57269-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="57269-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="57269-144">OUTPUTS</span></span>

### <span data-ttu-id="57269-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="57269-145">System.Boolean</span></span>

## <span data-ttu-id="57269-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="57269-146">NOTES</span></span>

<span data-ttu-id="57269-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="57269-147">ALIASES</span></span>

<span data-ttu-id="57269-148">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="57269-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="57269-149">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="57269-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="57269-150">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="57269-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="57269-151">INPUTOBJECT <IHanaOnAzureIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="57269-151">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="57269-152">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="57269-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="57269-153">`[Location <String>]`: расположение удаленного сейфа.</span><span class="sxs-lookup"><span data-stu-id="57269-153">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="57269-154">`[OperationKind <AccessPolicyUpdateKind?>]`: название операции</span><span class="sxs-lookup"><span data-stu-id="57269-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="57269-155">`[ProviderInstanceName <String>]`: имя экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="57269-155">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="57269-156">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="57269-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="57269-157">`[ResourceName <String>]`: Имя ресурса удостоверения.</span><span class="sxs-lookup"><span data-stu-id="57269-157">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="57269-158">`[SapMonitorName <String>]`. Имя ресурса sap monitor.</span><span class="sxs-lookup"><span data-stu-id="57269-158">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="57269-159">`[Scope <String>]`Область поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="57269-159">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="57269-160">Родительский ресурс, который расширяется с помощью управляемых удостоверений.</span><span class="sxs-lookup"><span data-stu-id="57269-160">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="57269-161">`[SubscriptionId <String>]`: ИД подписки, однозначно определяемой подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="57269-161">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="57269-162">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="57269-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="57269-163">`[VaultName <String>]`: имя сейфа</span><span class="sxs-lookup"><span data-stu-id="57269-163">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="57269-164">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57269-164">RELATED LINKS</span></span>
