---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/update-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
ms.openlocfilehash: 95334b4f67685183e499518b068f1003f5bb6547
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325601"
---
# <span data-ttu-id="978b2-101">Update-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="978b2-101">Update-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="978b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="978b2-102">SYNOPSIS</span></span>
<span data-ttu-id="978b2-103">Операция создания или обновления расширения.</span><span class="sxs-lookup"><span data-stu-id="978b2-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="978b2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="978b2-104">SYNTAX</span></span>

### <span data-ttu-id="978b2-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="978b2-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>] [-Type <String>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="978b2-106">Обновление</span><span class="sxs-lookup"><span data-stu-id="978b2-106">Update</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtensionUpdate> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="978b2-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="978b2-107">UpdateViaIdentity</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtensionUpdate> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="978b2-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="978b2-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-AutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>]
 [-Type <String>] [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="978b2-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="978b2-109">DESCRIPTION</span></span>
<span data-ttu-id="978b2-110">Операция создания или обновления расширения.</span><span class="sxs-lookup"><span data-stu-id="978b2-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="978b2-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="978b2-111">EXAMPLES</span></span>

### <span data-ttu-id="978b2-112">Пример 1. Обновление расширения</span><span class="sxs-lookup"><span data-stu-id="978b2-112">Example 1: Update an extension</span></span>
```powershell
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
            Settings = @{
                commandToExecute = "ls -l"
            }
        }
PS C:\> Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="978b2-113">Обновляет расширение на определенном компьютере.</span><span class="sxs-lookup"><span data-stu-id="978b2-113">Updates an extension on a specific machine.</span></span>

### <span data-ttu-id="978b2-114">Пример 2. Обновление расширения с заданным расположением в конвейере</span><span class="sxs-lookup"><span data-stu-id="978b2-114">Example 2: Update an extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -Settings @{
                commandToExecute = "ls -l"
            }

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="978b2-115">Обновляет определенное расширение, переданное через конвейер.</span><span class="sxs-lookup"><span data-stu-id="978b2-115">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="978b2-116">Мы используем расширение, которое передается через конвейер, чтобы мы могли определить, какое расширение нужно использовать, и указывать, что нужно изменить с помощью обычных параметров `-Settings` (например),</span><span class="sxs-lookup"><span data-stu-id="978b2-116">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on and are specifying what we want to change via the normal parameters (like `-Settings`)</span></span>

### <span data-ttu-id="978b2-117">Пример 3. Обновление расширения с параметрами расширения, указанными через конвейер</span><span class="sxs-lookup"><span data-stu-id="978b2-117">Example 3: Update an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
        }
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="978b2-118">Обновляет определенное расширение, переданное через конвейер.</span><span class="sxs-lookup"><span data-stu-id="978b2-118">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="978b2-119">Здесь мы используем расширение, переданный через конвейер, чтобы предоставлять изменения, которые мы хотим внести в расширение.</span><span class="sxs-lookup"><span data-stu-id="978b2-119">Here we are using the extension passed in via the pipeline to provide the changes we want to make on the extension.</span></span>
<span data-ttu-id="978b2-120">Расположение расширения определяется не по конвейеру, а через параметры, заданные обычным образом (с помощью параметра splat).</span><span class="sxs-lookup"><span data-stu-id="978b2-120">The location of the extension is not retrieved via the pipeline but rather via the parameters specified normally (by the splat parameter).</span></span>

### <span data-ttu-id="978b2-121">Пример 4. Использование объекта расширения как расположения и параметров для обновления</span><span class="sxs-lookup"><span data-stu-id="978b2-121">Example 4: Using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -ExtensionParameter $extToUpdate

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="978b2-122">Обновляет определенное расширение, переданное через конвейер.</span><span class="sxs-lookup"><span data-stu-id="978b2-122">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="978b2-123">В этом мы используем расширение, переданный по конвейеру, чтобы мы могли определить, какое расширение нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="978b2-123">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on.</span></span>
<span data-ttu-id="978b2-124">Кроме того, мы используем параметры объекта расширения, чтобы указать, что нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="978b2-124">In addition to that, we are using the parameters of the extension object to specify what to update.</span></span>

## <span data-ttu-id="978b2-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="978b2-125">PARAMETERS</span></span>

### <span data-ttu-id="978b2-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="978b2-126">-AsJob</span></span>
<span data-ttu-id="978b2-127">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="978b2-127">Run the command as a job</span></span>

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

### <span data-ttu-id="978b2-128">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="978b2-128">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="978b2-129">Указывает, следует ли использовать в расширении более новую версию, если она доступна во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="978b2-129">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="978b2-130">Однако после развертывания расширение не будет обновлять дополнительные версии, если не развернуть их снова, даже если для этого свойства установлено true.</span><span class="sxs-lookup"><span data-stu-id="978b2-130">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978b2-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="978b2-131">-DefaultProfile</span></span>
<span data-ttu-id="978b2-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="978b2-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="978b2-133">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="978b2-133">-ExtensionParameter</span></span>
<span data-ttu-id="978b2-134">В статье описано обновление расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="978b2-134">Describes a Machine Extension Update.</span></span>
<span data-ttu-id="978b2-135">Чтобы создать таблицу, см. раздел "ЗАМЕТКИ" для свойств EXTENSIONPARAMETER и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="978b2-135">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate
Parameter Sets: Update, UpdateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="978b2-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="978b2-136">-ForceRerun</span></span>
<span data-ttu-id="978b2-137">Как обработник расширений должен быть принудительно обновляться, даже если конфигурация расширения не изменилась.</span><span class="sxs-lookup"><span data-stu-id="978b2-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978b2-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="978b2-138">-InputObject</span></span>
<span data-ttu-id="978b2-139">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="978b2-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: UpdateViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="978b2-140">-MachineName</span><span class="sxs-lookup"><span data-stu-id="978b2-140">-MachineName</span></span>
<span data-ttu-id="978b2-141">Имя компьютера, на котором нужно создать или обновить расширение.</span><span class="sxs-lookup"><span data-stu-id="978b2-141">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978b2-142">-Name</span><span class="sxs-lookup"><span data-stu-id="978b2-142">-Name</span></span>
<span data-ttu-id="978b2-143">Имя расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="978b2-143">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978b2-144">-NoWait</span><span class="sxs-lookup"><span data-stu-id="978b2-144">-NoWait</span></span>
<span data-ttu-id="978b2-145">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="978b2-145">Run the command asynchronously</span></span>

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

### <span data-ttu-id="978b2-146">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="978b2-146">-ProtectedSetting</span></span>
<span data-ttu-id="978b2-147">Расширение может содержать защищенные параметрыSettings или protectedSettingsFromKeyVault или не защищенные параметры.</span><span class="sxs-lookup"><span data-stu-id="978b2-147">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesProtectedSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978b2-148">-Publisher</span><span class="sxs-lookup"><span data-stu-id="978b2-148">-Publisher</span></span>
<span data-ttu-id="978b2-149">Имя издателя обработера расширений.</span><span class="sxs-lookup"><span data-stu-id="978b2-149">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978b2-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="978b2-150">-ResourceGroupName</span></span>
<span data-ttu-id="978b2-151">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="978b2-151">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978b2-152">-Setting</span><span class="sxs-lookup"><span data-stu-id="978b2-152">-Setting</span></span>
<span data-ttu-id="978b2-153">Общедоступные параметры расширения, отформатированные Json.</span><span class="sxs-lookup"><span data-stu-id="978b2-153">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978b2-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="978b2-154">-SubscriptionId</span></span>
<span data-ttu-id="978b2-155">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="978b2-155">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="978b2-156">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="978b2-156">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978b2-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="978b2-157">-Tag</span></span>
<span data-ttu-id="978b2-158">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="978b2-158">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978b2-159">-Type</span><span class="sxs-lookup"><span data-stu-id="978b2-159">-Type</span></span>
<span data-ttu-id="978b2-160">Тип расширения. например: CustomScriptExtension.</span><span class="sxs-lookup"><span data-stu-id="978b2-160">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978b2-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="978b2-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="978b2-162">Определяет версию обработера сценариев.</span><span class="sxs-lookup"><span data-stu-id="978b2-162">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="978b2-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="978b2-163">-Confirm</span></span>
<span data-ttu-id="978b2-164">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="978b2-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="978b2-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="978b2-165">-WhatIf</span></span>
<span data-ttu-id="978b2-166">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="978b2-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="978b2-167">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="978b2-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="978b2-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="978b2-168">CommonParameters</span></span>
<span data-ttu-id="978b2-169">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="978b2-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="978b2-170">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="978b2-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="978b2-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="978b2-171">INPUTS</span></span>

### <span data-ttu-id="978b2-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMa modelse.Models.Api20200802.IMa modelseExtensionUpdate</span><span class="sxs-lookup"><span data-stu-id="978b2-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span></span>

### <span data-ttu-id="978b2-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMa modelse.Models.IConnectedMa modelseIdentity</span><span class="sxs-lookup"><span data-stu-id="978b2-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="978b2-174">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="978b2-174">OUTPUTS</span></span>

### <span data-ttu-id="978b2-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMa modelse.Models.Api20200802.IMa modelseExtension</span><span class="sxs-lookup"><span data-stu-id="978b2-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="978b2-176">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="978b2-176">NOTES</span></span>

<span data-ttu-id="978b2-177">ALIASES</span><span class="sxs-lookup"><span data-stu-id="978b2-177">ALIASES</span></span>

<span data-ttu-id="978b2-178">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="978b2-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="978b2-179">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="978b2-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="978b2-180">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="978b2-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="978b2-181">EXTENSIONPARAMETER: <IMachineExtensionUpdate> описание обновления расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="978b2-181">EXTENSIONPARAMETER <IMachineExtensionUpdate>: Describes a Machine Extension Update.</span></span>
  - <span data-ttu-id="978b2-182">`[Tag <IUpdateResourceTags>]`: теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="978b2-182">`[Tag <IUpdateResourceTags>]`: Resource tags</span></span>
    - <span data-ttu-id="978b2-183">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="978b2-183">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="978b2-184">`[AutoUpgradeMinorVersion <Boolean?>]`: указывает, следует ли использовать в расширении более новую версию, если она доступна во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="978b2-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="978b2-185">Однако после развертывания расширение не будет обновлять дополнительные версии, если не развернуть их снова, даже если для этого свойства установлено true.</span><span class="sxs-lookup"><span data-stu-id="978b2-185">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="978b2-186">`[ForceUpdateTag <String>]`. Как обработник расширений должен быть принудительно обновляться, даже если конфигурация расширения не изменилась.</span><span class="sxs-lookup"><span data-stu-id="978b2-186">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="978b2-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: Расширение может содержать защищенные параметрыSettings или protectedSettingsFromKeyVault или не защищенные параметры.</span><span class="sxs-lookup"><span data-stu-id="978b2-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="978b2-188">`[Publisher <String>]`: имя издателя обработера расширений.</span><span class="sxs-lookup"><span data-stu-id="978b2-188">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="978b2-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Общедоступные параметры расширения отформатированы Json.</span><span class="sxs-lookup"><span data-stu-id="978b2-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="978b2-190">`[Type <String>]`: тип расширения; например: CustomScriptExtension.</span><span class="sxs-lookup"><span data-stu-id="978b2-190">`[Type <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="978b2-191">`[TypeHandlerVersion <String>]`: определяет версию обработера сценариев.</span><span class="sxs-lookup"><span data-stu-id="978b2-191">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="978b2-192">INPUTOBJECT <IConnectedMachineIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="978b2-192">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="978b2-193">`[ExtensionName <String>]`: имя расширения компьютера.</span><span class="sxs-lookup"><span data-stu-id="978b2-193">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="978b2-194">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="978b2-194">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="978b2-195">`[Name <String>]`: имя гибридной машины.</span><span class="sxs-lookup"><span data-stu-id="978b2-195">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="978b2-196">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="978b2-196">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="978b2-197">`[SubscriptionId <String>]`: учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="978b2-197">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="978b2-198">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="978b2-198">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="978b2-199">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="978b2-199">RELATED LINKS</span></span>
