---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: cd8bc24a0cedac91ef18e19a80e1662fdcbac297
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506694"
---
# <span data-ttu-id="b1df6-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="b1df6-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="b1df6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1df6-102">SYNOPSIS</span></span>
<span data-ttu-id="b1df6-103">Изменяет определение набора политик.</span><span class="sxs-lookup"><span data-stu-id="b1df6-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="b1df6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b1df6-104">SYNTAX</span></span>

### <span data-ttu-id="b1df6-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b1df6-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1df6-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1df6-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1df6-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1df6-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1df6-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1df6-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1df6-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1df6-109">InputObjectParameterSet</span></span>
```
Set-AzPolicySetDefinition [-DisplayName <String>] [-Description <String>] [-PolicyDefinition <String>]
 [-Metadata <String>] [-Parameter <String>] -InputObject <PsPolicySetDefinition> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1df6-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1df6-110">DESCRIPTION</span></span>
<span data-ttu-id="b1df6-111">**Cmdlet Set-AzPolicySetDefinition** изменяет определение политики.</span><span class="sxs-lookup"><span data-stu-id="b1df6-111">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="b1df6-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b1df6-112">EXAMPLES</span></span>

### <span data-ttu-id="b1df6-113">Пример 1. Обновление описания определения набора политик</span><span class="sxs-lookup"><span data-stu-id="b1df6-113">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="b1df6-114">Первая команда получает определение набора политики с помощью Get-AzPolicySetDefinition командлета.</span><span class="sxs-lookup"><span data-stu-id="b1df6-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="b1df6-115">Эта команда сохраняет этот объект в $PolicySetDefinition переменной.</span><span class="sxs-lookup"><span data-stu-id="b1df6-115">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="b1df6-116">Вторая команда обновляет описание определения набора политики, заданного **свойством ResourceId** $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="b1df6-116">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="b1df6-117">Пример 2. Обновление метаданных определения набора политики</span><span class="sxs-lookup"><span data-stu-id="b1df6-117">Example 2: Update the metadata of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}'


Name                  : VMPolicySetDefinition
ResourceId            : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
ResourceName          : VMPolicySetDefinition
ResourceType          : Microsoft.Authorization/policySetDefinitions
SubscriptionId        : 11111111-1111-1111-1111-111111111111
Properties            : @{displayName=VMPolicySetDefinition; policyType=Custom; metadata=; parameters=; policyDefinitions=System.Object[]}
PolicySetDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
```

<span data-ttu-id="b1df6-118">Эта команда обновляет метаданные определения набора политики VMPolicySetDefinition, чтобы указать для категории виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="b1df6-118">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

### <span data-ttu-id="b1df6-119">Пример 3. Обновление групп определения набора политик</span><span class="sxs-lookup"><span data-stu-id="b1df6-119">Example 3: Update the groups of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition '[{ "name": "group1", "displayName": "Virtual Machine Security" }, { "name": "group2" }]'
```

<span data-ttu-id="b1df6-120">Эта команда обновляет группы определения набора политик VMPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="b1df6-120">This command updates the groups of a policy set definition named VMPolicySetDefinition.</span></span>

### <span data-ttu-id="b1df6-121">Пример 4. Обновление групп определения набора политик с помощью hash table</span><span class="sxs-lookup"><span data-stu-id="b1df6-121">Example 4: Update the groups of a policy set definition using a hash table</span></span>
```
$groupsJson = ConvertTo-Json @{ name = "group1", displayName = "Virtual Machine Security" }, @{ name = "group2" }
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson
```

<span data-ttu-id="b1df6-122">Эта команда обновляет группы определения набора политик VMPolicySetDefinition с помощью hash table для создания групп.</span><span class="sxs-lookup"><span data-stu-id="b1df6-122">This command updates the groups of a policy set definition named VMPolicySetDefinition using a hash table to construct the groups.</span></span>

## <span data-ttu-id="b1df6-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1df6-123">PARAMETERS</span></span>

### <span data-ttu-id="b1df6-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b1df6-124">-ApiVersion</span></span>
<span data-ttu-id="b1df6-125">Указывает версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b1df6-125">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b1df6-126">Если он не задан, версия API будет автоматически определена как наиболее последняя из доступных.</span><span class="sxs-lookup"><span data-stu-id="b1df6-126">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="b1df6-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1df6-127">-DefaultProfile</span></span>
<span data-ttu-id="b1df6-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b1df6-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1df6-129">-Description</span><span class="sxs-lookup"><span data-stu-id="b1df6-129">-Description</span></span>
<span data-ttu-id="b1df6-130">Описание определения набора политик.</span><span class="sxs-lookup"><span data-stu-id="b1df6-130">The description for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1df6-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b1df6-131">-DisplayName</span></span>
<span data-ttu-id="b1df6-132">Отображаемого имени определения набора политик.</span><span class="sxs-lookup"><span data-stu-id="b1df6-132">The display name for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1df6-133">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="b1df6-133">-GroupDefinition</span></span>
<span data-ttu-id="b1df6-134">Группы определений политик обновленного определения набора политики.</span><span class="sxs-lookup"><span data-stu-id="b1df6-134">The policy definition groups of the updated policy set definition.</span></span> <span data-ttu-id="b1df6-135">Это может быть путь к файлу, содержащего группы, или группы в качестве строки JSON.</span><span class="sxs-lookup"><span data-stu-id="b1df6-135">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1df6-136">-Id</span><span class="sxs-lookup"><span data-stu-id="b1df6-136">-Id</span></span>
<span data-ttu-id="b1df6-137">Полное определение политики, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="b1df6-137">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="b1df6-138">Например, /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="b1df6-138">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1df6-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1df6-139">-InputObject</span></span>
<span data-ttu-id="b1df6-140">Объект определения, задав политику, обновляет выходные данные из другого cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1df6-140">The policy set definition object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1df6-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="b1df6-141">-ManagementGroupName</span></span>
<span data-ttu-id="b1df6-142">Имя группы управления обновляемого определения набора политики.</span><span class="sxs-lookup"><span data-stu-id="b1df6-142">The name of the management group of the policy set definition to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1df6-143">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="b1df6-143">-Metadata</span></span>
<span data-ttu-id="b1df6-144">Метаданные обновленного определения набора политики.</span><span class="sxs-lookup"><span data-stu-id="b1df6-144">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="b1df6-145">Это может быть путь к имени файла, содержащего метаданные, или метаданные в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="b1df6-145">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1df6-146">-Name</span><span class="sxs-lookup"><span data-stu-id="b1df6-146">-Name</span></span>
<span data-ttu-id="b1df6-147">Имя определения набора политики.</span><span class="sxs-lookup"><span data-stu-id="b1df6-147">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1df6-148">-Parameter</span><span class="sxs-lookup"><span data-stu-id="b1df6-148">-Parameter</span></span>
<span data-ttu-id="b1df6-149">Объявление параметров в определении обновленного набора политики.</span><span class="sxs-lookup"><span data-stu-id="b1df6-149">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="b1df6-150">Это может быть путь к имени файла или URI, содержащий объявление параметров, или объявление параметров в качестве строки JSON.</span><span class="sxs-lookup"><span data-stu-id="b1df6-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1df6-151">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b1df6-151">-PolicyDefinition</span></span>
<span data-ttu-id="b1df6-152">Определения политик.</span><span class="sxs-lookup"><span data-stu-id="b1df6-152">The policy definitions.</span></span> <span data-ttu-id="b1df6-153">Это может быть путь к имени файла, содержащего определения политики, или определения политики в качестве строки JSON.</span><span class="sxs-lookup"><span data-stu-id="b1df6-153">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1df6-154">-Pre</span><span class="sxs-lookup"><span data-stu-id="b1df6-154">-Pre</span></span>
<span data-ttu-id="b1df6-155">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="b1df6-155">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b1df6-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b1df6-156">-SubscriptionId</span></span>
<span data-ttu-id="b1df6-157">ИД подписки определения набора политик, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="b1df6-157">The subscription ID of the policy set definition to update.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1df6-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1df6-158">-Confirm</span></span>
<span data-ttu-id="b1df6-159">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1df6-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1df6-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1df6-160">-WhatIf</span></span>
<span data-ttu-id="b1df6-161">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1df6-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1df6-162">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b1df6-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1df6-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1df6-163">CommonParameters</span></span>
<span data-ttu-id="b1df6-164">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1df6-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1df6-165">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1df6-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1df6-166">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1df6-166">INPUTS</span></span>

### <span data-ttu-id="b1df6-167">System.String</span><span class="sxs-lookup"><span data-stu-id="b1df6-167">System.String</span></span>

### <span data-ttu-id="b1df6-168">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b1df6-168">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b1df6-169">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b1df6-169">OUTPUTS</span></span>

### <span data-ttu-id="b1df6-170">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="b1df6-170">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b1df6-171">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b1df6-171">NOTES</span></span>

## <span data-ttu-id="b1df6-172">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1df6-172">RELATED LINKS</span></span>