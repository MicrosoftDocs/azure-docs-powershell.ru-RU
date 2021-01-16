---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/stop-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: e865098b0c85227baf1f537fb22c40ee351902fd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420524"
---
# <span data-ttu-id="111d5-101">Stop-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="111d5-101">Stop-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="111d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="111d5-102">SYNOPSIS</span></span>
<span data-ttu-id="111d5-103">Прекращает текущую синхронизацию для подписки на совместное использования.</span><span class="sxs-lookup"><span data-stu-id="111d5-103">Stops ongoing synchronization for a share subscription.</span></span> <span data-ttu-id="111d5-104">Подписку на один ресурс можно укаментить с помощью ее ИД ресурса или имени.</span><span class="sxs-lookup"><span data-stu-id="111d5-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="111d5-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="111d5-105">SYNTAX</span></span>

### <span data-ttu-id="111d5-106">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="111d5-106">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="111d5-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="111d5-107">ByResourceIdParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -SynchronizationId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="111d5-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="111d5-108">ByObjectParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="111d5-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="111d5-109">DESCRIPTION</span></span>
<span data-ttu-id="111d5-110">**Cmdlet Stop-AzDataShareSubscriptionSynchronization** останавливает текущую синхронизацию для подписки на доступ</span><span class="sxs-lookup"><span data-stu-id="111d5-110">The **Stop-AzDataShareSubscriptionSynchronization** cmdlet stops ongoing synchronization for a share subscription</span></span>

## <span data-ttu-id="111d5-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="111d5-111">EXAMPLES</span></span>

### <span data-ttu-id="111d5-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="111d5-112">Example 1</span></span>
```
PS C:\> Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationId 20a4416b-b33b-4539-a908-71dc8ef698fb

Confirm
AdsShareSubscription
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

durationMs        : 231869
endTime           : 
message           :
startTime         : 7/9/2019 11:40:53 PM
status            : Canceled
synchronizationId : 20a4416b-b33b-4539-a908-71dc8ef698fb
```

<span data-ttu-id="111d5-113">Остановка текущей синхронизации, выявленной по id - 20a4416b-b33b-4539-a908-71dc8ef698fb</span><span class="sxs-lookup"><span data-stu-id="111d5-113">Stops ongoing synchronization identified by id - 20a4416b-b33b-4539-a908-71dc8ef698fb</span></span>

## <span data-ttu-id="111d5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="111d5-114">PARAMETERS</span></span>

### <span data-ttu-id="111d5-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="111d5-115">-AccountName</span></span>
<span data-ttu-id="111d5-116">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="111d5-116">Azure data share account name</span></span>

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

### <span data-ttu-id="111d5-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="111d5-117">-AsJob</span></span>
<span data-ttu-id="111d5-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="111d5-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="111d5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="111d5-119">-DefaultProfile</span></span>
<span data-ttu-id="111d5-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="111d5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="111d5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="111d5-121">-InputObject</span></span>
<span data-ttu-id="111d5-122">Объект подписки на службу обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="111d5-122">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="111d5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="111d5-123">-ResourceGroupName</span></span>
<span data-ttu-id="111d5-124">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="111d5-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="111d5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="111d5-125">-ResourceId</span></span>
<span data-ttu-id="111d5-126">ИД ресурса подписки на azure share</span><span class="sxs-lookup"><span data-stu-id="111d5-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="111d5-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="111d5-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="111d5-128">Имя подписки на службу обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="111d5-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="111d5-129">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="111d5-129">-SynchronizationId</span></span>
<span data-ttu-id="111d5-130">ID синхронизации, который нужно остановить</span><span class="sxs-lookup"><span data-stu-id="111d5-130">Synchronization id that needs to be stopped</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="111d5-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="111d5-131">-Confirm</span></span>
<span data-ttu-id="111d5-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="111d5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="111d5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="111d5-133">-WhatIf</span></span>
<span data-ttu-id="111d5-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="111d5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="111d5-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="111d5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="111d5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="111d5-136">CommonParameters</span></span>
<span data-ttu-id="111d5-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="111d5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="111d5-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="111d5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="111d5-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="111d5-139">INPUTS</span></span>

### <span data-ttu-id="111d5-140">System.String</span><span class="sxs-lookup"><span data-stu-id="111d5-140">System.String</span></span>

### <span data-ttu-id="111d5-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="111d5-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="111d5-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="111d5-142">OUTPUTS</span></span>

### <span data-ttu-id="111d5-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="111d5-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="111d5-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="111d5-144">NOTES</span></span>

## <span data-ttu-id="111d5-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="111d5-145">RELATED LINKS</span></span>