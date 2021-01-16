---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 265600b201a6333b8dcd7c14f0cefe429f92619e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400236"
---
# <span data-ttu-id="d1020-101">Remove-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d1020-101">Remove-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="d1020-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1020-102">SYNOPSIS</span></span>
<span data-ttu-id="d1020-103">Удаляет правило виртуальной SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="d1020-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="d1020-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d1020-104">SYNTAX</span></span>

```
Remove-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> [-AsJob] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1020-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1020-105">DESCRIPTION</span></span>
<span data-ttu-id="d1020-106">Эта команда удаляет правило виртуальной SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="d1020-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="d1020-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d1020-107">EXAMPLES</span></span>

### <span data-ttu-id="d1020-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d1020-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="d1020-109">Удаление существующего правила виртуальной SQL Server Azure</span><span class="sxs-lookup"><span data-stu-id="d1020-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="d1020-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1020-110">PARAMETERS</span></span>

### <span data-ttu-id="d1020-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1020-111">-AsJob</span></span>
<span data-ttu-id="d1020-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d1020-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d1020-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1020-113">-DefaultProfile</span></span>
<span data-ttu-id="d1020-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d1020-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1020-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1020-115">-ResourceGroupName</span></span>
<span data-ttu-id="d1020-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d1020-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="d1020-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d1020-117">-ServerName</span></span>
<span data-ttu-id="d1020-118">Имя Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="d1020-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="d1020-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="d1020-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="d1020-120">Имя виртуального правила сети Azure Sql Server</span><span class="sxs-lookup"><span data-stu-id="d1020-120">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="d1020-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1020-121">-Confirm</span></span>
<span data-ttu-id="d1020-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d1020-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1020-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1020-123">-WhatIf</span></span>
<span data-ttu-id="d1020-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1020-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1020-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d1020-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1020-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1020-126">CommonParameters</span></span>
<span data-ttu-id="d1020-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1020-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1020-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1020-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1020-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d1020-129">INPUTS</span></span>

### <span data-ttu-id="d1020-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d1020-130">System.String</span></span>

## <span data-ttu-id="d1020-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d1020-131">OUTPUTS</span></span>

### <span data-ttu-id="d1020-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="d1020-132">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="d1020-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d1020-133">NOTES</span></span>

## <span data-ttu-id="d1020-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1020-134">RELATED LINKS</span></span>