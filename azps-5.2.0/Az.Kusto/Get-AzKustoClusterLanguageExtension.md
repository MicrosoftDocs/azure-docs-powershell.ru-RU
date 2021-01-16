---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: f33d644e9726d09f9f2314e74a6b5fb80b788952
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399135"
---
# <span data-ttu-id="d918c-101">Get-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="d918c-101">Get-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="d918c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d918c-102">SYNOPSIS</span></span>
<span data-ttu-id="d918c-103">Возвращает список языковых расширений, которые можно использовать в запросах KQL.</span><span class="sxs-lookup"><span data-stu-id="d918c-103">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="d918c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d918c-104">SYNTAX</span></span>

```
Get-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d918c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d918c-105">DESCRIPTION</span></span>
<span data-ttu-id="d918c-106">Возвращает список языковых расширений, которые можно использовать в запросах KQL.</span><span class="sxs-lookup"><span data-stu-id="d918c-106">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="d918c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d918c-107">EXAMPLES</span></span>

### <span data-ttu-id="d918c-108">Пример 1. Список всех языковых расширений, установленных для кластера</span><span class="sxs-lookup"><span data-stu-id="d918c-108">Example 1: List all language extensions set for a cluster</span></span>
```powershell
PS C:\> Get-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster

Name
----
R
PYTHON
```

<span data-ttu-id="d918c-109">Эта команда возвращает список языковых расширений, которые можно использовать в запросах KQL.</span><span class="sxs-lookup"><span data-stu-id="d918c-109">The above command returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="d918c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d918c-110">PARAMETERS</span></span>

### <span data-ttu-id="d918c-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d918c-111">-ClusterName</span></span>
<span data-ttu-id="d918c-112">Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="d918c-112">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d918c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d918c-113">-DefaultProfile</span></span>
<span data-ttu-id="d918c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d918c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d918c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d918c-115">-ResourceGroupName</span></span>
<span data-ttu-id="d918c-116">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="d918c-116">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d918c-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d918c-117">-SubscriptionId</span></span>
<span data-ttu-id="d918c-118">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d918c-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d918c-119">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="d918c-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d918c-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d918c-120">-Confirm</span></span>
<span data-ttu-id="d918c-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d918c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d918c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d918c-122">-WhatIf</span></span>
<span data-ttu-id="d918c-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d918c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d918c-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d918c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d918c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d918c-125">CommonParameters</span></span>
<span data-ttu-id="d918c-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d918c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d918c-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d918c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d918c-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d918c-128">INPUTS</span></span>

## <span data-ttu-id="d918c-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d918c-129">OUTPUTS</span></span>

### <span data-ttu-id="d918c-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension</span><span class="sxs-lookup"><span data-stu-id="d918c-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension</span></span>

## <span data-ttu-id="d918c-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d918c-131">NOTES</span></span>

<span data-ttu-id="d918c-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d918c-132">ALIASES</span></span>

## <span data-ttu-id="d918c-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d918c-133">RELATED LINKS</span></span>
