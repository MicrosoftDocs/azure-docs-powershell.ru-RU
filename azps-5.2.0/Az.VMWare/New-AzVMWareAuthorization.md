---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
ms.openlocfilehash: b1e8ca1e5140470524ec83656ef0042bafa494b7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391623"
---
# <span data-ttu-id="ccca6-101">New-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="ccca6-101">New-AzVMWareAuthorization</span></span>

## <span data-ttu-id="ccca6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccca6-102">SYNOPSIS</span></span>
<span data-ttu-id="ccca6-103">Создание или обновление авторизации каналов ExpressRoute в закрытом облаке</span><span class="sxs-lookup"><span data-stu-id="ccca6-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="ccca6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ccca6-104">SYNTAX</span></span>

```
New-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ccca6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ccca6-105">DESCRIPTION</span></span>
<span data-ttu-id="ccca6-106">Создание или обновление авторизации каналов ExpressRoute в закрытом облаке</span><span class="sxs-lookup"><span data-stu-id="ccca6-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="ccca6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ccca6-107">EXAMPLES</span></span>

### <span data-ttu-id="ccca6-108">Пример 1. Создание автозаверх</span><span class="sxs-lookup"><span data-stu-id="ccca6-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="ccca6-109">Этот cmdlet создает авторизацию в `azps-test-auth` закрытом облаке `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="ccca6-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="ccca6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ccca6-110">PARAMETERS</span></span>

### <span data-ttu-id="ccca6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccca6-111">-AsJob</span></span>
<span data-ttu-id="ccca6-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="ccca6-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ccca6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccca6-113">-DefaultProfile</span></span>
<span data-ttu-id="ccca6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ccca6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccca6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ccca6-115">-Name</span></span>
<span data-ttu-id="ccca6-116">Имя авторизации каналов ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="ccca6-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccca6-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ccca6-117">-NoWait</span></span>
<span data-ttu-id="ccca6-118">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="ccca6-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ccca6-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="ccca6-119">-PrivateCloudName</span></span>
<span data-ttu-id="ccca6-120">Имя закрытого облака.</span><span class="sxs-lookup"><span data-stu-id="ccca6-120">The name of the private cloud.</span></span>

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

### <span data-ttu-id="ccca6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccca6-121">-ResourceGroupName</span></span>
<span data-ttu-id="ccca6-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ccca6-122">The name of the resource group.</span></span>
<span data-ttu-id="ccca6-123">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="ccca6-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ccca6-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ccca6-124">-SubscriptionId</span></span>
<span data-ttu-id="ccca6-125">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="ccca6-125">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccca6-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ccca6-126">-Confirm</span></span>
<span data-ttu-id="ccca6-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ccca6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccca6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccca6-128">-WhatIf</span></span>
<span data-ttu-id="ccca6-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccca6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccca6-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ccca6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccca6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccca6-131">CommonParameters</span></span>
<span data-ttu-id="ccca6-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccca6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccca6-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ccca6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccca6-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ccca6-134">INPUTS</span></span>

## <span data-ttu-id="ccca6-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ccca6-135">OUTPUTS</span></span>

### <span data-ttu-id="ccca6-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="ccca6-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="ccca6-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ccca6-137">NOTES</span></span>

<span data-ttu-id="ccca6-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ccca6-138">ALIASES</span></span>

## <span data-ttu-id="ccca6-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ccca6-139">RELATED LINKS</span></span>
