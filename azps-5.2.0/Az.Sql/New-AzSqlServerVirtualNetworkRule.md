---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 64fc7b3acdc497759b707f024a0fb14c7017c44c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393391"
---
# <span data-ttu-id="1d8cc-101">New-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1d8cc-101">New-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="1d8cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d8cc-102">SYNOPSIS</span></span>
<span data-ttu-id="1d8cc-103">Создает правило виртуальной SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="1d8cc-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

## <span data-ttu-id="1d8cc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1d8cc-104">SYNTAX</span></span>

```
New-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d8cc-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d8cc-105">DESCRIPTION</span></span>
<span data-ttu-id="1d8cc-106">Создает правило виртуальной SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="1d8cc-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="1d8cc-107">Виртуальные правила сети используются для подключения Azure SQL Server к определенной виртуальной сети, чтобы ограничить доступ к Azure SQL Server только в пределах виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1d8cc-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="1d8cc-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1d8cc-108">EXAMPLES</span></span>

### <span data-ttu-id="1d8cc-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1d8cc-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="1d8cc-110">Создание правила виртуальной SQL Server Azure</span><span class="sxs-lookup"><span data-stu-id="1d8cc-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="1d8cc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d8cc-111">PARAMETERS</span></span>

### <span data-ttu-id="1d8cc-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d8cc-112">-AsJob</span></span>
<span data-ttu-id="1d8cc-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1d8cc-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d8cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d8cc-114">-DefaultProfile</span></span>
<span data-ttu-id="1d8cc-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1d8cc-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d8cc-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="1d8cc-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="1d8cc-117">Создайте правило брандмауэра до того, как в виртуальной сети будет включена конечная точка службы VNET.</span><span class="sxs-lookup"><span data-stu-id="1d8cc-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="1d8cc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d8cc-118">-ResourceGroupName</span></span>
<span data-ttu-id="1d8cc-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1d8cc-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d8cc-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1d8cc-120">-ServerName</span></span>
<span data-ttu-id="1d8cc-121">Имя Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="1d8cc-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="1d8cc-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="1d8cc-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="1d8cc-123">Имя виртуального правила сети Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="1d8cc-123">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="1d8cc-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="1d8cc-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="1d8cc-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span><span class="sxs-lookup"><span data-stu-id="1d8cc-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="1d8cc-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d8cc-126">-Confirm</span></span>
<span data-ttu-id="1d8cc-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d8cc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d8cc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d8cc-128">-WhatIf</span></span>
<span data-ttu-id="1d8cc-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d8cc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d8cc-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1d8cc-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d8cc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d8cc-131">CommonParameters</span></span>
<span data-ttu-id="1d8cc-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d8cc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d8cc-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d8cc-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d8cc-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d8cc-134">INPUTS</span></span>

### <span data-ttu-id="1d8cc-135">System.String</span><span class="sxs-lookup"><span data-stu-id="1d8cc-135">System.String</span></span>

## <span data-ttu-id="1d8cc-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1d8cc-136">OUTPUTS</span></span>

### <span data-ttu-id="1d8cc-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="1d8cc-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="1d8cc-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1d8cc-138">NOTES</span></span>

## <span data-ttu-id="1d8cc-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d8cc-139">RELATED LINKS</span></span>