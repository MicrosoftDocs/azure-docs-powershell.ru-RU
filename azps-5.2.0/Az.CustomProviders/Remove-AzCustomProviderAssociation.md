---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
ms.openlocfilehash: 708bac976e32c2af114576d971c05843fd58ef93
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391620"
---
# <span data-ttu-id="93398-101">Remove-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="93398-101">Remove-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="93398-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93398-102">SYNOPSIS</span></span>
<span data-ttu-id="93398-103">Удаление связи.</span><span class="sxs-lookup"><span data-stu-id="93398-103">Delete an association.</span></span>

## <span data-ttu-id="93398-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="93398-104">SYNTAX</span></span>

### <span data-ttu-id="93398-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="93398-105">Delete (Default)</span></span>
```
Remove-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="93398-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="93398-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="93398-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93398-107">DESCRIPTION</span></span>
<span data-ttu-id="93398-108">Удаление связи.</span><span class="sxs-lookup"><span data-stu-id="93398-108">Delete an association.</span></span>

## <span data-ttu-id="93398-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="93398-109">EXAMPLES</span></span>

### <span data-ttu-id="93398-110">Пример 1. Удаление пользовательской связи поставщика.</span><span class="sxs-lookup"><span data-stu-id="93398-110">Example 1: Remove a custom provider association.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProviderAssociation -Scope $id -Name Namespace.Type
```

<span data-ttu-id="93398-111">Удаление пользовательской связи поставщика.</span><span class="sxs-lookup"><span data-stu-id="93398-111">Remove a custom provider association.</span></span>

### <span data-ttu-id="93398-112">Пример 2. Удаление пользовательской связи поставщика с Piping</span><span class="sxs-lookup"><span data-stu-id="93398-112">Example 2: Remove a custom provider association with Piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProviderAssociation | Remove-AzCustomProviderAssociation -PassThru

True
```

<span data-ttu-id="93398-113">Удаление пользовательской связи поставщика с помощью операторов piping и функции "Переу", чтобы указать успешность или сбой.</span><span class="sxs-lookup"><span data-stu-id="93398-113">Remove a custom provider association, using piping and the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="93398-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93398-114">PARAMETERS</span></span>

### <span data-ttu-id="93398-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93398-115">-AsJob</span></span>
<span data-ttu-id="93398-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="93398-116">Run the command as a job</span></span>

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

### <span data-ttu-id="93398-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93398-117">-DefaultProfile</span></span>
<span data-ttu-id="93398-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93398-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93398-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93398-119">-InputObject</span></span>
<span data-ttu-id="93398-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="93398-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93398-121">-Name</span><span class="sxs-lookup"><span data-stu-id="93398-121">-Name</span></span>
<span data-ttu-id="93398-122">Имя связи.</span><span class="sxs-lookup"><span data-stu-id="93398-122">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93398-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="93398-123">-NoWait</span></span>
<span data-ttu-id="93398-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="93398-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="93398-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93398-125">-PassThru</span></span>
<span data-ttu-id="93398-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="93398-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="93398-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="93398-127">-Scope</span></span>
<span data-ttu-id="93398-128">Область действия связи.</span><span class="sxs-lookup"><span data-stu-id="93398-128">The scope of the association.</span></span>

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

### <span data-ttu-id="93398-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93398-129">-Confirm</span></span>
<span data-ttu-id="93398-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93398-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93398-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93398-131">-WhatIf</span></span>
<span data-ttu-id="93398-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93398-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93398-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="93398-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93398-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93398-134">CommonParameters</span></span>
<span data-ttu-id="93398-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93398-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93398-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93398-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93398-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93398-137">INPUTS</span></span>

### <span data-ttu-id="93398-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="93398-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="93398-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="93398-139">OUTPUTS</span></span>

### <span data-ttu-id="93398-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="93398-140">System.Boolean</span></span>

## <span data-ttu-id="93398-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="93398-141">NOTES</span></span>

<span data-ttu-id="93398-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="93398-142">ALIASES</span></span>

<span data-ttu-id="93398-143">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="93398-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="93398-144">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="93398-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="93398-145">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="93398-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="93398-146">INPUTOBJECT <ICustomProvidersIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="93398-146">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="93398-147">`[AssociationName <String>]`: Название связи.</span><span class="sxs-lookup"><span data-stu-id="93398-147">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="93398-148">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="93398-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="93398-149">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="93398-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="93398-150">`[ResourceProviderName <String>]`: имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="93398-150">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="93398-151">`[Scope <String>]`: область действия связи.</span><span class="sxs-lookup"><span data-stu-id="93398-151">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="93398-152">`[SubscriptionId <String>]`: ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="93398-152">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="93398-153">Строка в формате GUID (например, 00000000-0000-0000-0000-0000-00000000000000)</span><span class="sxs-lookup"><span data-stu-id="93398-153">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="93398-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93398-154">RELATED LINKS</span></span>
