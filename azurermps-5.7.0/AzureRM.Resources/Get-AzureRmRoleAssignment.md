---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 488229AF-FD6D-4E1B-B3DA-E57CA781D91E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleAssignment.md
ms.openlocfilehash: c6dd17917624d8b2b914ac94c8310358fac03b68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567408"
---
# <span data-ttu-id="2cd67-101">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="2cd67-101">Get-AzureRmRoleAssignment</span></span>

## <span data-ttu-id="2cd67-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2cd67-102">SYNOPSIS</span></span>
<span data-ttu-id="2cd67-103">Выводит список назначений ролей Azure RBAC в указанной области.</span><span class="sxs-lookup"><span data-stu-id="2cd67-103">Lists Azure RBAC role assignments at the specified scope.</span></span>
<span data-ttu-id="2cd67-104">По умолчанию в списке перечислены все назначения ролей в выбранной подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="2cd67-104">By default it lists all role assignments in the selected Azure subscription.</span></span>
<span data-ttu-id="2cd67-105">Применяйте соответствующие параметры для списка назначений определенного пользователя или перечислите назначения в определенной группе ресурсов или ресурсе.</span><span class="sxs-lookup"><span data-stu-id="2cd67-105">Use respective parameters to list assignments to a specific user, or to list assignments on a specific resource group or resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cd67-106">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2cd67-106">SYNTAX</span></span>

### <span data-ttu-id="2cd67-107">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2cd67-107">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmRoleAssignment [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cd67-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cd67-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cd67-109">ResourceGroupWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cd67-109">ResourceGroupWithObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cd67-110">ResourceWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cd67-110">ResourceWithObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cd67-111">ScopeWithObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cd67-111">ScopeWithObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ObjectId <Guid> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cd67-112">RoleIdWithScopeAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cd67-112">RoleIdWithScopeAndObjectIdParameterSet</span></span>
```
Get-AzureRmRoleAssignment [-ObjectId <Guid>] -RoleDefinitionId <Guid> [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cd67-113">ResourceGroupWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cd67-113">ResourceGroupWithSignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cd67-114">ResourceWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cd67-114">ResourceWithSignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cd67-115">ScopeWithSignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cd67-115">ScopeWithSignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cd67-116">SignInNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cd67-116">SignInNameParameterSet</span></span>
```
Get-AzureRmRoleAssignment -SignInName <String> [-RoleDefinitionName <String>] [-ExpandPrincipalGroups]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cd67-117">ResourceGroupWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cd67-117">ResourceGroupWithSPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String>
 [-RoleDefinitionName <String>] [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2cd67-118">ResourceWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cd67-118">ResourceWithSPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cd67-119">ScopeWithSPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cd67-119">ScopeWithSPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>] -Scope <String>
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cd67-120">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cd67-120">SPNParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ServicePrincipalName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cd67-121">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cd67-121">ResourceGroupParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ResourceGroupName <String> [-RoleDefinitionName <String>]
 [-IncludeClassicAdministrators] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cd67-122">ResourceParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cd67-122">ResourceParameterSet</span></span>
```
Get-AzureRmRoleAssignment -ResourceGroupName <String> -ResourceName <String> -ResourceType <String>
 [-ParentResource <String>] [-RoleDefinitionName <String>] [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cd67-123">ScopeParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cd67-123">ScopeParameterSet</span></span>
```
Get-AzureRmRoleAssignment [-RoleDefinitionName <String>] -Scope <String> [-IncludeClassicAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cd67-124">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cd67-124">DESCRIPTION</span></span>
<span data-ttu-id="2cd67-125">С помощью команды Get-AzureRMRoleAssignment вы можете получить список всех назначений ролей, действующих в области.</span><span class="sxs-lookup"><span data-stu-id="2cd67-125">Use the Get-AzureRMRoleAssignment command to list all role assignments that are effective on a scope.</span></span>

<span data-ttu-id="2cd67-126">При отсутствии каких бы то ни было параметров эта команда возвращает все назначения ролей, выполненные в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="2cd67-126">Without any parameters, this command returns all the role assignments made under the subscription.</span></span>
<span data-ttu-id="2cd67-127">Этот список можно фильтровать с помощью параметров фильтрации для участника, роли и области.</span><span class="sxs-lookup"><span data-stu-id="2cd67-127">This list can  be filtered using filtering parameters for principal, role and scope.</span></span>

<span data-ttu-id="2cd67-128">Необходимо указать тему назначения.</span><span class="sxs-lookup"><span data-stu-id="2cd67-128">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="2cd67-129">Чтобы указать пользователя, используйте параметры SignInName или Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="2cd67-129">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="2cd67-130">Чтобы указать группу безопасности, используйте параметр Azure AD ObjectId.</span><span class="sxs-lookup"><span data-stu-id="2cd67-130">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="2cd67-131">Чтобы указать приложение Azure AD, используйте параметры "ИД" или "ObjectId".</span><span class="sxs-lookup"><span data-stu-id="2cd67-131">And to specify an Azure AD application, use ServicePrincipalName or ObjectId parameters.</span></span>

<span data-ttu-id="2cd67-132">Назначаемая роль должна быть указана с помощью параметра RoleDefinitionName.</span><span class="sxs-lookup"><span data-stu-id="2cd67-132">The role that is being assigned must be specified using the RoleDefinitionName parameter.</span></span>

<span data-ttu-id="2cd67-133">Может быть указана область, для которой предоставляется доступ.</span><span class="sxs-lookup"><span data-stu-id="2cd67-133">The scope at which access is being granted may be specified.</span></span>
<span data-ttu-id="2cd67-134">По умолчанию используется выбранная подписка.</span><span class="sxs-lookup"><span data-stu-id="2cd67-134">It defaults to the selected subscription.</span></span> <span data-ttu-id="2cd67-135">Область назначения может быть указана с помощью одного из следующих сочетаний параметров a.</span><span class="sxs-lookup"><span data-stu-id="2cd67-135">The scope of the assignment can be specified using one of the following parameter combinations a.</span></span>
<span data-ttu-id="2cd67-136">Scope — это полностью определенная область, начиная с/Subscriptions/ \<subscriptionId\> .</span><span class="sxs-lookup"><span data-stu-id="2cd67-136">Scope - This is the fully qualified scope starting with /subscriptions/\<subscriptionId\>.</span></span>
<span data-ttu-id="2cd67-137">Таким образом будут фильтроваться назначения, действующие в этой конкретной области, т.е. все задания в этой области и более поздних.</span><span class="sxs-lookup"><span data-stu-id="2cd67-137">This will filter assignments that are effective at that particular scope i.e. all assignments at that scope and above.</span></span>
<span data-ttu-id="2cd67-138">байт.</span><span class="sxs-lookup"><span data-stu-id="2cd67-138">b.</span></span>
<span data-ttu-id="2cd67-139">ResourceGroupName — имя любой группы ресурсов в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="2cd67-139">ResourceGroupName - Name of any resource group under the subscription.</span></span>
<span data-ttu-id="2cd67-140">Это позволяет отфильтровать назначения, действующие в указанной группе ресурсов c.</span><span class="sxs-lookup"><span data-stu-id="2cd67-140">This will filter assignments effective at the specified resource group c.</span></span>
<span data-ttu-id="2cd67-141">ResourceName, ResourceType, ResourceGroupName и (необязательно) ParentResource — определяет конкретный ресурс в подписке, а также отфильтровать назначения, действующие в этой области ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2cd67-141">ResourceName, ResourceType, ResourceGroupName and (optionally) ParentResource - Identifies a particular resource under the subscription and will filter assignments effective at that resource scope.</span></span>

<span data-ttu-id="2cd67-142">Чтобы определить, какой пользователь имеет доступ к подписке для определенного пользователя, используйте параметр ExpandPrincipalGroups.</span><span class="sxs-lookup"><span data-stu-id="2cd67-142">To determine what access a particular user has in the subscription, use the ExpandPrincipalGroups switch.</span></span>
<span data-ttu-id="2cd67-143">Будут перечислены все роли, назначенные пользователю, и группы, в которых он входит.</span><span class="sxs-lookup"><span data-stu-id="2cd67-143">This will list all roles assigned to the user, and to the groups that the user is member of.</span></span>

<span data-ttu-id="2cd67-144">С помощью переключателя IncludeClassicAdministrators также можно отобразить администраторов подписок и соадминистраторов.</span><span class="sxs-lookup"><span data-stu-id="2cd67-144">Use the IncludeClassicAdministrators switch to also display the subscription admins and co-admins.</span></span>

## <span data-ttu-id="2cd67-145">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2cd67-145">EXAMPLES</span></span>

### <span data-ttu-id="2cd67-146">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2cd67-146">Example 1</span></span>
```
PS C:\> Get-AzureRmRoleAssignment
```

<span data-ttu-id="2cd67-147">Список всех назначений ролей в подписке</span><span class="sxs-lookup"><span data-stu-id="2cd67-147">List all role assignments in the subscription</span></span>

### <span data-ttu-id="2cd67-148">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2cd67-148">Example 2</span></span>
```
PS C:\> Get-AzureRmRoleAssignment -ResourceGroupName testRG -SignInName john.doe@contoso.com
```

<span data-ttu-id="2cd67-149">Получает все назначения ролей для пользователя john.doe@contoso.com и группы, членом которых является пользователь, в области testRG или более поздней.</span><span class="sxs-lookup"><span data-stu-id="2cd67-149">Gets all role assignments made to user john.doe@contoso.com, and the groups of which he is member, at the testRG scope or above.</span></span>

### <span data-ttu-id="2cd67-150">Пример 3</span><span class="sxs-lookup"><span data-stu-id="2cd67-150">Example 3</span></span>
```
PS C:\> Get-AzureRmRoleAssignment -ServicePrincipalName "http://testapp1.com"
```

<span data-ttu-id="2cd67-151">Возвращает все назначения ролей для указанного субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="2cd67-151">Gets all role assignments of the specified service principal</span></span>

### <span data-ttu-id="2cd67-152">Пример 4</span><span class="sxs-lookup"><span data-stu-id="2cd67-152">Example 4</span></span>
```
PS C:\> Get-AzureRmRoleAssignment -Scope "/subscriptions/96231a05-34ce-4eb4-aa6a-70759cbb5e83/resourcegroups/rg1/providers/Microsoft.Web/sites/site1"
```

<span data-ttu-id="2cd67-153">Получает назначения ролей в области веб-сайта "site1".</span><span class="sxs-lookup"><span data-stu-id="2cd67-153">Gets role assignments at the 'site1' website scope.</span></span>

## <span data-ttu-id="2cd67-154">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2cd67-154">PARAMETERS</span></span>

### <span data-ttu-id="2cd67-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cd67-155">-DefaultProfile</span></span>
<span data-ttu-id="2cd67-156">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2cd67-156">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2cd67-157">-ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="2cd67-157">-ExpandPrincipalGroups</span></span>
<span data-ttu-id="2cd67-158">Если задано, возвращает роли, непосредственно назначенные пользователю, и группам, участником которых является пользователь (транзитивно).</span><span class="sxs-lookup"><span data-stu-id="2cd67-158">If specified, returns roles directly assigned to the user and to the groups of which the user is a member (transitively).</span></span>
<span data-ttu-id="2cd67-159">Поддерживается только для участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="2cd67-159">Supported only for a user principal.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ObjectIdParameterSet, SignInNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cd67-160">-IncludeClassicAdministrators</span><span class="sxs-lookup"><span data-stu-id="2cd67-160">-IncludeClassicAdministrators</span></span>
<span data-ttu-id="2cd67-161">Если указано, также выводится список администраторов классической подписки (соадминистраторов, администраторов служб и т. д.).</span><span class="sxs-lookup"><span data-stu-id="2cd67-161">If specified, also lists subscription classic administrators (co-admins, service admins, etc.) role assignments.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cd67-162">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2cd67-162">-ObjectId</span></span>
<span data-ttu-id="2cd67-163">ИД служб Azure AD ObjectId для пользователя, группы или участника-службы.</span><span class="sxs-lookup"><span data-stu-id="2cd67-163">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>
<span data-ttu-id="2cd67-164">Фильтрует все назначения, выполненные указанному участнику.</span><span class="sxs-lookup"><span data-stu-id="2cd67-164">Filters all assignments that are made to the specified principal.</span></span>

```yaml
Type: Guid
Parameter Sets: ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd67-165">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="2cd67-165">-ParentResource</span></span>
<span data-ttu-id="2cd67-166">Родительский ресурс в иерархии ресурса, указанный с помощью параметра ResourceName.</span><span class="sxs-lookup"><span data-stu-id="2cd67-166">The parent resource in the hierarchy of the resource specified using ResourceName parameter.</span></span>
<span data-ttu-id="2cd67-167">Необходимо использовать в сочетании с параметрами ResourceGroupName, ResourceType и ResourceName.</span><span class="sxs-lookup"><span data-stu-id="2cd67-167">Must be used in conjunction with ResourceGroupName, ResourceType, and ResourceName parameters.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd67-168">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cd67-168">-ResourceGroupName</span></span>
<span data-ttu-id="2cd67-169">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2cd67-169">The resource group name.</span></span>
<span data-ttu-id="2cd67-170">Список назначений ролей, действующих в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2cd67-170">Lists role assignments that are effective at the specified resource group.</span></span>
<span data-ttu-id="2cd67-171">При использовании в сочетании с параметрами ResourceName, ResourceType и ParentResource команда перечисляет назначения, действующие на ресурсах в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2cd67-171">When used in conjunction with ResourceName, ResourceType, and ParentResource parameters, the command lists assignments effective at resources within the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd67-172">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2cd67-172">-ResourceName</span></span>
<span data-ttu-id="2cd67-173">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="2cd67-173">The resource name.</span></span>
<span data-ttu-id="2cd67-174">Например, storageaccountprod.</span><span class="sxs-lookup"><span data-stu-id="2cd67-174">For e.g. storageaccountprod.</span></span>
<span data-ttu-id="2cd67-175">Необходимо использовать в сочетании с ResourceGroupName, ResourceType и (необязательно) параметрами ParentResource.</span><span class="sxs-lookup"><span data-stu-id="2cd67-175">Must be used in conjunction with ResourceGroupName, ResourceType, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd67-176">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="2cd67-176">-ResourceType</span></span>
<span data-ttu-id="2cd67-177">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="2cd67-177">The resource type.</span></span>
<span data-ttu-id="2cd67-178">Для таких, например, Microsoft. Network/virtualNetworks.</span><span class="sxs-lookup"><span data-stu-id="2cd67-178">For e.g. Microsoft.Network/virtualNetworks.</span></span>
<span data-ttu-id="2cd67-179">Необходимо использовать в сочетании с ResourceGroupName, ResourceName и (необязательно) параметрами ParentResource.</span><span class="sxs-lookup"><span data-stu-id="2cd67-179">Must be used in conjunction with ResourceGroupName, ResourceName, and (optionally)ParentResource parameters.</span></span>

```yaml
Type: String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd67-180">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="2cd67-180">-RoleDefinitionId</span></span>
<span data-ttu-id="2cd67-181">Идентификатор роли, назначенной участнику.</span><span class="sxs-lookup"><span data-stu-id="2cd67-181">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd67-182">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="2cd67-182">-RoleDefinitionName</span></span>
<span data-ttu-id="2cd67-183">Роль, назначенная участнику, например читатель, участник, Администратор виртуальной сети и т. д.</span><span class="sxs-lookup"><span data-stu-id="2cd67-183">Role that is assigned to the principal i.e. Reader, Contributor, Virtual Network Administrator, etc.</span></span>

```yaml
Type: String
Parameter Sets: EmptyParameterSet, ObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet, ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet, ResourceGroupParameterSet, ResourceParameterSet, ScopeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd67-184">-Scope</span><span class="sxs-lookup"><span data-stu-id="2cd67-184">-Scope</span></span>
<span data-ttu-id="2cd67-185">Область назначения роли.</span><span class="sxs-lookup"><span data-stu-id="2cd67-185">The Scope of the role assignment.</span></span>
<span data-ttu-id="2cd67-186">В формате относительных URI.</span><span class="sxs-lookup"><span data-stu-id="2cd67-186">In the format of relative URI.</span></span>
<span data-ttu-id="2cd67-187">Например,/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span><span class="sxs-lookup"><span data-stu-id="2cd67-187">For e.g. /subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG.</span></span>
<span data-ttu-id="2cd67-188">Оно должно начинаться с "/Subscriptions/{ID}".</span><span class="sxs-lookup"><span data-stu-id="2cd67-188">It must start with "/subscriptions/{id}".</span></span>
<span data-ttu-id="2cd67-189">Команда фильтрует все задания, действующие в этой области.</span><span class="sxs-lookup"><span data-stu-id="2cd67-189">The command filters all assignments that are effective at that scope.</span></span>

```yaml
Type: String
Parameter Sets: ScopeWithObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet, ScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd67-190">-Намерено</span><span class="sxs-lookup"><span data-stu-id="2cd67-190">-ServicePrincipalName</span></span>
<span data-ttu-id="2cd67-191">Значение параметра безопасности участника-службы.</span><span class="sxs-lookup"><span data-stu-id="2cd67-191">The ServicePrincipalName of the service principal.</span></span>
<span data-ttu-id="2cd67-192">Фильтрует все назначения, выполненные в указанном приложении Azure AD.</span><span class="sxs-lookup"><span data-stu-id="2cd67-192">Filters all assignments that are made to the specified Azure AD application.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupWithSPNParameterSet, ResourceWithSPNParameterSet, ScopeWithSPNParameterSet, SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd67-193">-SignInName</span><span class="sxs-lookup"><span data-stu-id="2cd67-193">-SignInName</span></span>
<span data-ttu-id="2cd67-194">Адрес электронной почты или имя участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="2cd67-194">The email address or the user principal name of the user.</span></span>
<span data-ttu-id="2cd67-195">Фильтрует все назначения, выполненные указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="2cd67-195">Filters all assignments that are made to the specified user.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupWithSignInNameParameterSet, ResourceWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, SignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd67-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cd67-196">CommonParameters</span></span>
<span data-ttu-id="2cd67-197">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2cd67-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cd67-198">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cd67-198">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cd67-199">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2cd67-199">INPUTS</span></span>

### <span data-ttu-id="2cd67-200">Ничего</span><span class="sxs-lookup"><span data-stu-id="2cd67-200">None</span></span>
<span data-ttu-id="2cd67-201">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="2cd67-201">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2cd67-202">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cd67-202">OUTPUTS</span></span>

### <span data-ttu-id="2cd67-203">System. Collections. Generic. List ' 1 [Microsoft. Azure. System. Resources. Authorization. PSRoleAssignment]</span><span class="sxs-lookup"><span data-stu-id="2cd67-203">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment]</span></span>

## <span data-ttu-id="2cd67-204">Пуск</span><span class="sxs-lookup"><span data-stu-id="2cd67-204">NOTES</span></span>
<span data-ttu-id="2cd67-205">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="2cd67-205">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="2cd67-206">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2cd67-206">RELATED LINKS</span></span>

[<span data-ttu-id="2cd67-207">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="2cd67-207">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="2cd67-208">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="2cd67-208">Remove-AzureRmRoleAssignment</span></span>](./Remove-AzureRmRoleAssignment.md)

[<span data-ttu-id="2cd67-209">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="2cd67-209">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)
