---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/update-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
ms.openlocfilehash: cafb705ec5f2882eb239931b22ccfba610721100
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399740"
---
# <span data-ttu-id="08788-101">Update-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="08788-101">Update-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="08788-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08788-102">SYNOPSIS</span></span>
<span data-ttu-id="08788-103">Обновление политики WAF</span><span class="sxs-lookup"><span data-stu-id="08788-103">Update WAF policy</span></span>

## <span data-ttu-id="08788-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="08788-104">SYNTAX</span></span>

### <span data-ttu-id="08788-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="08788-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08788-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08788-106">ByObjectParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08788-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08788-107">ByResourceIdParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08788-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="08788-108">DESCRIPTION</span></span>
<span data-ttu-id="08788-109">Для обновления политики WAF будет обновлена существующая политика **AzFrontDoorWafPolicy.**</span><span class="sxs-lookup"><span data-stu-id="08788-109">The **Update-AzFrontDoorWafPolicy** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="08788-110">Если входные параметры не предоставлены, будут использоваться старые параметры из существующей политики WAF.</span><span class="sxs-lookup"><span data-stu-id="08788-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="08788-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="08788-111">EXAMPLES</span></span>

### <span data-ttu-id="08788-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="08788-112">Example 1</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -CustomBlockResponseStatusCode 403

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="08788-113">Обновление существующего пользовательского кода состояния политики WAF.</span><span class="sxs-lookup"><span data-stu-id="08788-113">Update an existing WAF policy custom status code.</span></span>

### <span data-ttu-id="08788-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="08788-114">Example 2</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Detection            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="08788-115">Обновление существующего режима политики WAF.</span><span class="sxs-lookup"><span data-stu-id="08788-115">Update an existing WAF policy mode.</span></span>

### <span data-ttu-id="08788-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="08788-116">Example 3</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection -EnabledState Disabled

Name          PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----          ---------- ------------------ ----------------------------- -----------
{policyName}  Detection           Disabled                           403 https://www.bing.com/
```

<span data-ttu-id="08788-117">Обновление состояния и режима, включаемого политикой WAF.</span><span class="sxs-lookup"><span data-stu-id="08788-117">Update an existing WAF policy enabled state and mode.</span></span>

### <span data-ttu-id="08788-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="08788-118">Example 4</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Update-AzFrontDoorWafPolicy -Mode Detection -EnabledState Disabled
```

<span data-ttu-id="08788-119">Обновление всех политик WAF в $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08788-119">Update all WAF policies in $resourceGroupName</span></span>

## <span data-ttu-id="08788-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08788-120">PARAMETERS</span></span>

### <span data-ttu-id="08788-121">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="08788-121">-CustomBlockResponseBody</span></span>
<span data-ttu-id="08788-122">Настраиваемый тело ответа</span><span class="sxs-lookup"><span data-stu-id="08788-122">Custom Response Body</span></span>

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

### <span data-ttu-id="08788-123">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="08788-123">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="08788-124">Пользовательский код состояния ответа</span><span class="sxs-lookup"><span data-stu-id="08788-124">Custom Response Status Code</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08788-125">-Customrule</span><span class="sxs-lookup"><span data-stu-id="08788-125">-Customrule</span></span>
<span data-ttu-id="08788-126">Настраиваемые правила в политике</span><span class="sxs-lookup"><span data-stu-id="08788-126">Custom rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08788-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08788-127">-DefaultProfile</span></span>
<span data-ttu-id="08788-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="08788-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08788-129">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="08788-129">-EnabledState</span></span>
<span data-ttu-id="08788-130">Состояние политики (включена или отключена).</span><span class="sxs-lookup"><span data-stu-id="08788-130">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="08788-131">Возможные значения: "Отключено", "Включено"</span><span class="sxs-lookup"><span data-stu-id="08788-131">Possible values include: 'Disabled', 'Enabled'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08788-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08788-132">-InputObject</span></span>
<span data-ttu-id="08788-133">Объект FireWallPolicy, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="08788-133">The FireWallPolicy object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08788-134">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="08788-134">-ManagedRule</span></span>
<span data-ttu-id="08788-135">Управляемые правила в политике</span><span class="sxs-lookup"><span data-stu-id="08788-135">Managed rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08788-136">-Mode</span><span class="sxs-lookup"><span data-stu-id="08788-136">-Mode</span></span>
<span data-ttu-id="08788-137">В нем описывается, находится ли он в режиме обнаружения или режиме предотвращения на уровне политики.</span><span class="sxs-lookup"><span data-stu-id="08788-137">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="08788-138">Возможные значения: 'Prevention', 'Detection'</span><span class="sxs-lookup"><span data-stu-id="08788-138">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="08788-139">-Name</span><span class="sxs-lookup"><span data-stu-id="08788-139">-Name</span></span>
<span data-ttu-id="08788-140">Имя поля FireWallPolicy, которое нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="08788-140">The name of the FireWallPolicy to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08788-141">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="08788-141">-RedirectUrl</span></span>
<span data-ttu-id="08788-142">Url-адрес перенаправления</span><span class="sxs-lookup"><span data-stu-id="08788-142">Redirect URL</span></span>

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

### <span data-ttu-id="08788-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08788-143">-ResourceGroupName</span></span>
<span data-ttu-id="08788-144">Группа ресурсов, к которой принадлежит FireWallPolicy.</span><span class="sxs-lookup"><span data-stu-id="08788-144">The resource group to which the FireWallPolicy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08788-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08788-145">-ResourceId</span></span>
<span data-ttu-id="08788-146">ИД ресурса для обновления FireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="08788-146">Resource Id of the FireWallPolicy to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08788-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08788-147">-Confirm</span></span>
<span data-ttu-id="08788-148">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08788-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08788-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08788-149">-WhatIf</span></span>
<span data-ttu-id="08788-150">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08788-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08788-151">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="08788-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08788-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08788-152">CommonParameters</span></span>
<span data-ttu-id="08788-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08788-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08788-154">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08788-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08788-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="08788-155">INPUTS</span></span>

### <span data-ttu-id="08788-156">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="08788-156">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="08788-157">System.String</span><span class="sxs-lookup"><span data-stu-id="08788-157">System.String</span></span>

## <span data-ttu-id="08788-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="08788-158">OUTPUTS</span></span>

### <span data-ttu-id="08788-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="08788-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="08788-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="08788-160">NOTES</span></span>

## <span data-ttu-id="08788-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="08788-161">RELATED LINKS</span></span>

<span data-ttu-id="08788-162">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="08788-162">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>