---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
ms.openlocfilehash: 45e2c822bc21acfe69296f8d784a3a707dc1797f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328947"
---
# <span data-ttu-id="cd7fb-101">Remove-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="cd7fb-101">Remove-AzWvdMsixPackage</span></span>

## <span data-ttu-id="cd7fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd7fb-102">SYNOPSIS</span></span>
<span data-ttu-id="cd7fb-103">Удаление пакета MSIX.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-103">Remove an MSIX Package.</span></span>

## <span data-ttu-id="cd7fb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cd7fb-104">SYNTAX</span></span>

### <span data-ttu-id="cd7fb-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cd7fb-105">Delete (Default)</span></span>
```
Remove-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cd7fb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cd7fb-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd7fb-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd7fb-107">DESCRIPTION</span></span>
<span data-ttu-id="cd7fb-108">Удаление пакета MSIX.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-108">Remove an MSIX Package.</span></span>

## <span data-ttu-id="cd7fb-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cd7fb-109">EXAMPLES</span></span>

### <span data-ttu-id="cd7fb-110">Пример 1. Удаление пакета MSIX по полному имени пакета</span><span class="sxs-lookup"><span data-stu-id="cd7fb-110">Example 1: Delete MSIX Package by Package Full Name</span></span>
```powershell
PS C:\> Remove-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName
```

<span data-ttu-id="cd7fb-111">Эта команда удаляет пакет MSIX в hostPool</span><span class="sxs-lookup"><span data-stu-id="cd7fb-111">This command deletes a MSIX Package in a HostPool</span></span>

## <span data-ttu-id="cd7fb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd7fb-112">PARAMETERS</span></span>

### <span data-ttu-id="cd7fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd7fb-113">-DefaultProfile</span></span>
<span data-ttu-id="cd7fb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd7fb-115">-FullName</span><span class="sxs-lookup"><span data-stu-id="cd7fb-115">-FullName</span></span>
<span data-ttu-id="cd7fb-116">Полное имя пакета MSIX для версии в указанном хостпаке</span><span class="sxs-lookup"><span data-stu-id="cd7fb-116">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd7fb-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="cd7fb-117">-HostPoolName</span></span>
<span data-ttu-id="cd7fb-118">Имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="cd7fb-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="cd7fb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd7fb-119">-InputObject</span></span>
<span data-ttu-id="cd7fb-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd7fb-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd7fb-121">-PassThru</span></span>
<span data-ttu-id="cd7fb-122">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cd7fb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd7fb-123">-ResourceGroupName</span></span>
<span data-ttu-id="cd7fb-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-124">The name of the resource group.</span></span>
<span data-ttu-id="cd7fb-125">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="cd7fb-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd7fb-126">-SubscriptionId</span></span>
<span data-ttu-id="cd7fb-127">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="cd7fb-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd7fb-128">-Confirm</span></span>
<span data-ttu-id="cd7fb-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd7fb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd7fb-130">-WhatIf</span></span>
<span data-ttu-id="cd7fb-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd7fb-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd7fb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd7fb-133">CommonParameters</span></span>
<span data-ttu-id="cd7fb-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd7fb-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd7fb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd7fb-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd7fb-136">INPUTS</span></span>

### <span data-ttu-id="cd7fb-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="cd7fb-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="cd7fb-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cd7fb-138">OUTPUTS</span></span>

### <span data-ttu-id="cd7fb-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cd7fb-139">System.Boolean</span></span>

## <span data-ttu-id="cd7fb-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cd7fb-140">NOTES</span></span>

<span data-ttu-id="cd7fb-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="cd7fb-141">ALIASES</span></span>

<span data-ttu-id="cd7fb-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="cd7fb-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cd7fb-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cd7fb-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cd7fb-145">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="cd7fb-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cd7fb-146">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="cd7fb-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="cd7fb-147">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="cd7fb-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="cd7fb-148">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="cd7fb-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="cd7fb-149">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="cd7fb-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="cd7fb-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="cd7fb-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cd7fb-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="cd7fb-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="cd7fb-152">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cd7fb-153">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="cd7fb-154">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="cd7fb-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="cd7fb-155">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="cd7fb-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="cd7fb-156">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="cd7fb-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="cd7fb-157">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="cd7fb-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="cd7fb-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd7fb-158">RELATED LINKS</span></span>
