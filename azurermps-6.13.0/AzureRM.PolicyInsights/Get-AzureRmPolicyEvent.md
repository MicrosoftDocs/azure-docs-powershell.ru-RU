---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyEvent.md
ms.openlocfilehash: 0c4e4f531dac3f75f0eff69ba1dcfc644473ea06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565806"
---
# <span data-ttu-id="6ae30-101">Get-AzureRmPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="6ae30-101">Get-AzureRmPolicyEvent</span></span>

## <span data-ttu-id="6ae30-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6ae30-102">SYNOPSIS</span></span>
<span data-ttu-id="6ae30-103">Получение событий оценки политики, возникающих при создании или обновлении ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ae30-103">Gets policy evaluation events generated as resources are created or updated.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ae30-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6ae30-104">SYNTAX</span></span>

### <span data-ttu-id="6ae30-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6ae30-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ae30-106">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="6ae30-106">ManagementGroupScope</span></span>
```
Get-AzureRmPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ae30-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="6ae30-107">ResourceGroupScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ae30-108">PolicySetDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="6ae30-108">PolicySetDefinitionScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ae30-109">PolicyDefinitionScope</span><span class="sxs-lookup"><span data-stu-id="6ae30-109">PolicyDefinitionScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ae30-110">SubscriptionLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="6ae30-110">SubscriptionLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ae30-111">ResourceGroupLevelPolicyAssignmentScope</span><span class="sxs-lookup"><span data-stu-id="6ae30-111">ResourceGroupLevelPolicyAssignmentScope</span></span>
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ae30-112">ResourceScope</span><span class="sxs-lookup"><span data-stu-id="6ae30-112">ResourceScope</span></span>
```
Get-AzureRmPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ae30-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ae30-113">DESCRIPTION</span></span>
<span data-ttu-id="6ae30-114">Получение событий оценки политики, возникающих при создании или обновлении ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ae30-114">Gets policy evaluation events generated as resources are created or updated.</span></span> <span data-ttu-id="6ae30-115">Записи событий политики можно запрашивать в различных областях на основе указанного интервала времени (по умолчанию для последнего дня).</span><span class="sxs-lookup"><span data-stu-id="6ae30-115">Policy event records can be queried at various scopes based on the time interval specified (defaults to last day).</span></span> <span data-ttu-id="6ae30-116">Результаты могут быть вычислены с фильтрацией, группировкой и группировкой.</span><span class="sxs-lookup"><span data-stu-id="6ae30-116">Results can be filtered, grouped, and group aggregations can be computed.</span></span>

## <span data-ttu-id="6ae30-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6ae30-117">EXAMPLES</span></span>

### <span data-ttu-id="6ae30-118">Пример 1: получение событий политики в текущей области подписки</span><span class="sxs-lookup"><span data-stu-id="6ae30-118">Example 1: Get policy events in current subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent
```

<span data-ttu-id="6ae30-119">Возвращает записи событий политики, созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="6ae30-119">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="6ae30-120">Пример 2: получение событий политики в указанной области подписки</span><span class="sxs-lookup"><span data-stu-id="6ae30-120">Example 2: Get policy events in the specified subscription scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

<span data-ttu-id="6ae30-121">Возвращает записи событий политики, созданные за последний день для всех ресурсов в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="6ae30-121">Gets policy event records generated in the last day for all resources within the specified subscription.</span></span>

### <span data-ttu-id="6ae30-122">Пример 3: получение событий политики в области группы управления</span><span class="sxs-lookup"><span data-stu-id="6ae30-122">Example 3: Get policy events in management group scope</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -ManagementGroupName "myManagementGroup"
```

<span data-ttu-id="6ae30-123">Возвращает записи событий политики, созданные за последний день для всех ресурсов в указанной группе управления.</span><span class="sxs-lookup"><span data-stu-id="6ae30-123">Gets policy event records generated in the last day for all resources within the specified management group.</span></span>

### <span data-ttu-id="6ae30-124">Пример 4: получение событий политики в области группы ресурсов в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="6ae30-124">Example 4: Get policy events in resource group scope in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="6ae30-125">Возвращает записи событий политики, созданные за последний день для всех ресурсов в указанной группе ресурсов (в контексте текущего сеанса).</span><span class="sxs-lookup"><span data-stu-id="6ae30-125">Gets policy event records generated in the last day for all resources within the specified resource group (in the subscription in current session context).</span></span>

### <span data-ttu-id="6ae30-126">Пример 5: получение событий политики в области группы ресурсов в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="6ae30-126">Example 5: Get policy events in resource group scope in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="6ae30-127">Возвращает записи событий политики, созданные за последний день для всех ресурсов в указанной группе ресурсов (в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="6ae30-127">Gets policy event records generated in the last day for all resources within the specified resource group (in the specified subscription).</span></span>

### <span data-ttu-id="6ae30-128">Пример 6: получение событий политики для ресурса</span><span class="sxs-lookup"><span data-stu-id="6ae30-128">Example 6: Get policy events for a resource</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

<span data-ttu-id="6ae30-129">Возвращает записи событий политики, созданные за последний день для указанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="6ae30-129">Gets policy event records generated in the last day for the specified resource.</span></span>

### <span data-ttu-id="6ae30-130">Пример 7: получение событий политики для определения политики в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="6ae30-130">Example 7: Get policy events for a policy set definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="6ae30-131">Возвращает записи событий политики, созданные за последний день для всех ресурсов (в рамках текущего контекста сеанса), которые были применены указанным определением политики (которое существует в текущем контексте сеанса).</span><span class="sxs-lookup"><span data-stu-id="6ae30-131">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="6ae30-132">Пример 8: получение событий политики для определения политики в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="6ae30-132">Example 8: Get policy events for a policy set definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="6ae30-133">Возвращает записи событий политики, созданные за последний день для всех ресурсов (в рамках текущего контекста сеанса), которые были применены указанным определением политики (которое существует в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="6ae30-133">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy set definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="6ae30-134">Пример 9: получение событий политики для определения политики в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="6ae30-134">Example 9: Get policy events for a policy definition in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="6ae30-135">Возвращает записи событий политики, созданные в последнем дне для всех ресурсов (в рамках текущего контекста сеанса), которые были применены указанным определением политики (которое существует в текущем контексте сеанса).</span><span class="sxs-lookup"><span data-stu-id="6ae30-135">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="6ae30-136">Пример 10: получение событий политики для определения политики в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="6ae30-136">Example 10: Get policy events for a policy definition in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

<span data-ttu-id="6ae30-137">Возвращает записи событий политики, созданные в прошлом дне для всех ресурсов (в рамках текущего контекста сеанса), которые были применены указанным определением политики (которое существует в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="6ae30-137">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy definition (that exists in the specified subscription).</span></span>

### <span data-ttu-id="6ae30-138">Пример 11: получение событий политики для назначения политики в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="6ae30-138">Example 11: Get policy events for a policy assignment in current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="6ae30-139">Получает записи событий политики, созданные за последний день для всех ресурсов (в рамках текущего контекста сеанса), которые влияют на указанное назначение политики (оно существует в контексте текущего сеанса).</span><span class="sxs-lookup"><span data-stu-id="6ae30-139">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the subscription in current session context).</span></span>

### <span data-ttu-id="6ae30-140">Пример 12: получение событий политики для назначения политики в указанной подписке</span><span class="sxs-lookup"><span data-stu-id="6ae30-140">Example 12: Get policy events for a policy assignment in the specified subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="6ae30-141">Получает записи событий политики, созданные за последний день для всех ресурсов (в рамках текущего контекста сеанса), на которые влияет указанное назначение политики (которое существует в указанной подписке).</span><span class="sxs-lookup"><span data-stu-id="6ae30-141">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the specified subscription).</span></span>

### <span data-ttu-id="6ae30-142">Пример 13: получение событий политики для назначения политики в указанной группе ресурсов в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="6ae30-142">Example 13: Get policy events for a policy assignment in the specified resource group in the current subscription</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

<span data-ttu-id="6ae30-143">Возвращает записи событий политики, созданные за последний день для всех ресурсов (в рамках текущего контекста сеанса), которые влияют на указанное назначение политики (которое существует в группе ресурсов в контексте текущего сеанса).</span><span class="sxs-lookup"><span data-stu-id="6ae30-143">Gets policy event records generated in the last day for all resources (within the tenant in current session context) effected by the specified policy assignment (that exists in the resource group in the subscription in current session context).</span></span>

### <span data-ttu-id="6ae30-144">Пример 14: получение событий политики в текущей области подписки с параметрами OrderBy, Top и SELECT запроса</span><span class="sxs-lookup"><span data-stu-id="6ae30-144">Example 14: Get policy events in current subscription scope, with OrderBy, Top and Select query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

<span data-ttu-id="6ae30-145">Возвращает записи событий политики, созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="6ae30-145">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="6ae30-146">Команда упорядочивает результаты по свойствам timestamp и Name назначения политики и занимает только первые 5 из указанных в этом порядке.</span><span class="sxs-lookup"><span data-stu-id="6ae30-146">The command orders the results by timestamp and policy assignment name properties, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="6ae30-147">Он также выберет для списка только подмножество столбцов для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="6ae30-147">It also selects to list only a subset of the columns for each record.</span></span>

### <span data-ttu-id="6ae30-148">Пример 15: получение событий политики в текущей области подписки с параметрами "из" и "по запросу"</span><span class="sxs-lookup"><span data-stu-id="6ae30-148">Example 15: Get policy events in current subscription scope, with From and To query options</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

<span data-ttu-id="6ae30-149">Получение записей событий политики, сформированных в диапазоне дат, указанном для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="6ae30-149">Gets policy event records generated within the date range specified for all resources within the subscription in current session context.</span></span>

### <span data-ttu-id="6ae30-150">Пример 16: получение событий политики в текущей области подписки с помощью параметра запроса фильтра</span><span class="sxs-lookup"><span data-stu-id="6ae30-150">Example 16: Get policy events in current subscription scope, with Filter query option</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

<span data-ttu-id="6ae30-151">Возвращает записи событий политики, созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="6ae30-151">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="6ae30-152">Команда ограничивает результаты, возвращаемые фильтром, на основе действия с определением политики (в том числе действия запрета или аудита) и расположения ресурсов (исключает расположение eastus).</span><span class="sxs-lookup"><span data-stu-id="6ae30-152">The command limits the results returned by filtering based on policy definition action (includes deny or audit actions) and resource location (excludes eastus location).</span></span>

### <span data-ttu-id="6ae30-153">Пример 17: получение событий политики в текущей области подписки с указанием агрегата количества строк</span><span class="sxs-lookup"><span data-stu-id="6ae30-153">Example 17: Get policy events in current subscription scope, with Apply specifying row count aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

<span data-ttu-id="6ae30-154">Возвращает количество записей событий политики, созданных за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="6ae30-154">Gets the number of policy event records generated in the last day for all resources within the subscription in current session context.</span></span>
<span data-ttu-id="6ae30-155">Команда возвращает количество записей событий политики, которые возвращаются только в свойстве AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="6ae30-155">The command returns the count of the policy event records only, which is returned inside AdditionalProperties property.</span></span>

### <span data-ttu-id="6ae30-156">Пример 18: получение событий политики в текущей области подписок с применением задания группирования с агрегированием</span><span class="sxs-lookup"><span data-stu-id="6ae30-156">Example 18: Get policy events in current subscription scope, with Apply specifying grouping with aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

<span data-ttu-id="6ae30-157">Возвращает записи событий политики, созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="6ae30-157">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="6ae30-158">Команда ограничивает результаты, возвращаемые фильтром, на основе действия с определением политики (включает только аудит и запрет событий).</span><span class="sxs-lookup"><span data-stu-id="6ae30-158">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="6ae30-159">Результаты группируются на основе назначения политики, определения политики, действия определения политики и идентификатора ресурса, а также вычисляется количество записей в каждой группе, которое возвращается в рамках свойства AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="6ae30-159">It groups the results based on policy assignment, policy definition, policy definition action, and resource id, and computes the number of records in each group, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="6ae30-160">Результаты статистического выражения упорядочиваются по убыванию и выполняются только первые 5 из указанных в этом порядке.</span><span class="sxs-lookup"><span data-stu-id="6ae30-160">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>

### <span data-ttu-id="6ae30-161">Пример 19: получение событий политики в текущей области подписки с применением задания группирования без агрегата</span><span class="sxs-lookup"><span data-stu-id="6ae30-161">Example 19: Get policy events in current subscription scope, with Apply specifying grouping without aggregation</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

<span data-ttu-id="6ae30-162">Возвращает записи событий политики, созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="6ae30-162">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="6ae30-163">Команда ограничивает результаты, возвращаемые фильтром, на основе действия с определением политики (включает только аудит и запрет событий).</span><span class="sxs-lookup"><span data-stu-id="6ae30-163">The command limits the results returned by filtering based on policy definition action (includes only audit and deny events).</span></span>
<span data-ttu-id="6ae30-164">Результаты группируются на основе идентификатора ресурса. Это приведет к формированию списка всех ресурсов в подписке, которые создали событие политики по крайней мере для одной политики аудита или запрета.</span><span class="sxs-lookup"><span data-stu-id="6ae30-164">It groups the results based on resource id. This generates the list of all resources within the subscription that generated a policy event for at least one audit or deny policy.</span></span>

### <span data-ttu-id="6ae30-165">Пример 20: получение событий политики в текущей области подписки с применением задания нескольких групп</span><span class="sxs-lookup"><span data-stu-id="6ae30-165">Example 20: Get policy events in current subscription scope, with Apply specifying multiple groupings</span></span>
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

<span data-ttu-id="6ae30-166">Возвращает записи событий политики, созданные за последний день для всех ресурсов в рамках подписки в текущем контексте сеанса.</span><span class="sxs-lookup"><span data-stu-id="6ae30-166">Gets policy event records generated in the last day for all resources within the subscription in current session context.</span></span> <span data-ttu-id="6ae30-167">Команда ограничивает результаты, возвращаемые фильтром, на основе действия с определением политики (включает только отклонения событий).</span><span class="sxs-lookup"><span data-stu-id="6ae30-167">The command limits the results returned by filtering based on policy definition action (includes only deny events).</span></span>
<span data-ttu-id="6ae30-168">Результаты сначала группируются в соответствии с назначением политики, определением политики и идентификатором ресурса. Затем он дополнительно группирует результаты этого группирования с теми же свойствами, но за исключением идентификатора ресурса, и вычисляет количество записей в каждой из этих групп, которое возвращается в рамках свойства AdditionalProperties.</span><span class="sxs-lookup"><span data-stu-id="6ae30-168">It groups the results first based on policy assignment, policy definition, and resource id. Then, it further groups the results of this grouping with the same properties except for resource id, and computes the number of records in each of these groups, which is returned inside AdditionalProperties property.</span></span>
<span data-ttu-id="6ae30-169">Результаты статистического выражения упорядочиваются по убыванию и выполняются только первые 5 из указанных в этом порядке.</span><span class="sxs-lookup"><span data-stu-id="6ae30-169">It orders the results by the count aggregation in descending order, and takes only top 5 of those listed in that order.</span></span>
<span data-ttu-id="6ae30-170">Это приведет к формированию 5 основных политик запретов с наибольшим количеством запрещенных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ae30-170">This generates the top 5 deny policies with the most number of denied resources.</span></span>

## <span data-ttu-id="6ae30-171">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6ae30-171">PARAMETERS</span></span>

### <span data-ttu-id="6ae30-172">-Apply (Применить)</span><span class="sxs-lookup"><span data-stu-id="6ae30-172">-Apply</span></span>
<span data-ttu-id="6ae30-173">Применение выражения для агрегатов с использованием нотации OData.</span><span class="sxs-lookup"><span data-stu-id="6ae30-173">Apply expression for aggregations using OData notation.</span></span>

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

### <span data-ttu-id="6ae30-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ae30-174">-DefaultProfile</span></span>
<span data-ttu-id="6ae30-175">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ae30-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ae30-176">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="6ae30-176">-Filter</span></span>
<span data-ttu-id="6ae30-177">Выражение фильтра с использованием нотации OData.</span><span class="sxs-lookup"><span data-stu-id="6ae30-177">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="6ae30-178">-From</span><span class="sxs-lookup"><span data-stu-id="6ae30-178">-From</span></span>
<span data-ttu-id="6ae30-179">Отформатированная отметка времени ISO 8601 с указанием времени начала интервала для запроса.</span><span class="sxs-lookup"><span data-stu-id="6ae30-179">ISO 8601 formatted timestamp specifying the start time of the interval to query.</span></span>
<span data-ttu-id="6ae30-180">Если не указано, по умолчанию используется значение параметра "до" за вычетом 1 дня.</span><span class="sxs-lookup"><span data-stu-id="6ae30-180">When not specified, defaults to 'To' parameter value minus 1 day.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ae30-181">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="6ae30-181">-ManagementGroupName</span></span>
<span data-ttu-id="6ae30-182">Имя группы управления.</span><span class="sxs-lookup"><span data-stu-id="6ae30-182">Management group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ae30-183">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="6ae30-183">-OrderBy</span></span>
<span data-ttu-id="6ae30-184">Выражение упорядочивания с использованием нотации OData.</span><span class="sxs-lookup"><span data-stu-id="6ae30-184">Ordering expression using OData notation.</span></span>
<span data-ttu-id="6ae30-185">Одно или несколько имен столбцов с разделителями-запятыми с дополнительным аргументом "DESC" (значение по умолчанию) или "ASC".</span><span class="sxs-lookup"><span data-stu-id="6ae30-185">One or more comma-separated column names with an optional 'desc' (the default) or 'asc'.</span></span>

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

### <span data-ttu-id="6ae30-186">-PolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="6ae30-186">-PolicyAssignmentName</span></span>
<span data-ttu-id="6ae30-187">Имя назначения политики.</span><span class="sxs-lookup"><span data-stu-id="6ae30-187">Policy assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ae30-188">-PolicyDefinitionName</span><span class="sxs-lookup"><span data-stu-id="6ae30-188">-PolicyDefinitionName</span></span>
<span data-ttu-id="6ae30-189">Имя определения политики.</span><span class="sxs-lookup"><span data-stu-id="6ae30-189">Policy definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ae30-190">-PolicySetDefinitionName</span><span class="sxs-lookup"><span data-stu-id="6ae30-190">-PolicySetDefinitionName</span></span>
<span data-ttu-id="6ae30-191">Имя определения политики.</span><span class="sxs-lookup"><span data-stu-id="6ae30-191">Policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicySetDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ae30-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ae30-192">-ResourceGroupName</span></span>
<span data-ttu-id="6ae30-193">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ae30-193">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ae30-194">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ae30-194">-ResourceId</span></span>
<span data-ttu-id="6ae30-195">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="6ae30-195">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ae30-196">-SELECT</span><span class="sxs-lookup"><span data-stu-id="6ae30-196">-Select</span></span>
<span data-ttu-id="6ae30-197">Выберите выражение с помощью нотации OData.</span><span class="sxs-lookup"><span data-stu-id="6ae30-197">Select expression using OData notation.</span></span>
<span data-ttu-id="6ae30-198">Одно или несколько имен столбцов с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="6ae30-198">One or more comma-separated column names.</span></span>
<span data-ttu-id="6ae30-199">Ограничивает столбцы каждой записи только запрошенными.</span><span class="sxs-lookup"><span data-stu-id="6ae30-199">Limits the columns on each record to just those requested.</span></span>

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

### <span data-ttu-id="6ae30-200">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6ae30-200">-SubscriptionId</span></span>
<span data-ttu-id="6ae30-201">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="6ae30-201">Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, ResourceGroupScope, PolicySetDefinitionScope, PolicyDefinitionScope, SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ae30-202">-To</span><span class="sxs-lookup"><span data-stu-id="6ae30-202">-To</span></span>
<span data-ttu-id="6ae30-203">Отформатированная отметка времени ISO 8601, указывающая время окончания интервала для запроса.</span><span class="sxs-lookup"><span data-stu-id="6ae30-203">ISO 8601 formatted timestamp specifying the end time of the interval to query.</span></span>
<span data-ttu-id="6ae30-204">Если не указано, по умолчанию используется время запроса.</span><span class="sxs-lookup"><span data-stu-id="6ae30-204">When not specified, defaults to time of request.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ae30-205">-Top</span><span class="sxs-lookup"><span data-stu-id="6ae30-205">-Top</span></span>
<span data-ttu-id="6ae30-206">Максимальное количество возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="6ae30-206">Maximum number of records to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ae30-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ae30-207">CommonParameters</span></span>
<span data-ttu-id="6ae30-208">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6ae30-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ae30-209">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ae30-209">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ae30-210">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6ae30-210">INPUTS</span></span>

### <span data-ttu-id="6ae30-211">System. String</span><span class="sxs-lookup"><span data-stu-id="6ae30-211">System.String</span></span>

## <span data-ttu-id="6ae30-212">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ae30-212">OUTPUTS</span></span>

### <span data-ttu-id="6ae30-213">Microsoft. Azure. Commands. PolicyInsights. Models. PolicyEvent</span><span class="sxs-lookup"><span data-stu-id="6ae30-213">Microsoft.Azure.Commands.PolicyInsights.Models.PolicyEvent</span></span>

## <span data-ttu-id="6ae30-214">Пуск</span><span class="sxs-lookup"><span data-stu-id="6ae30-214">NOTES</span></span>

## <span data-ttu-id="6ae30-215">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ae30-215">RELATED LINKS</span></span>