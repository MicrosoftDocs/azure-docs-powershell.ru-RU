---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 283a7963d7dcf278f203385bd790bd19cadc9d7c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406444"
---
# <span data-ttu-id="34e9a-101">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="34e9a-101">Remove-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="34e9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34e9a-102">SYNOPSIS</span></span>
<span data-ttu-id="34e9a-103">Удаляет группу отбойных SQL баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="34e9a-103">Removes an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="34e9a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="34e9a-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34e9a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34e9a-105">DESCRIPTION</span></span>
<span data-ttu-id="34e9a-106">Эта команда удаляет группу отбойных команд с указанным именем, оставляя все базы данных и связи репликации без изменений.</span><span class="sxs-lookup"><span data-stu-id="34e9a-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="34e9a-107">Конечная точка будет отрегистрирована из DNS.</span><span class="sxs-lookup"><span data-stu-id="34e9a-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="34e9a-108">Для выполнения команды следует использовать основной сервер группы отбойных команд.</span><span class="sxs-lookup"><span data-stu-id="34e9a-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="34e9a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="34e9a-109">EXAMPLES</span></span>

### <span data-ttu-id="34e9a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="34e9a-110">Example 1</span></span>
```
PS C:\> Remove-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="34e9a-111">Удалите группу отбойных передач.</span><span class="sxs-lookup"><span data-stu-id="34e9a-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="34e9a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34e9a-112">PARAMETERS</span></span>

### <span data-ttu-id="34e9a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34e9a-113">-DefaultProfile</span></span>
<span data-ttu-id="34e9a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="34e9a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34e9a-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="34e9a-115">-FailoverGroupName</span></span>
<span data-ttu-id="34e9a-116">Имя группы отбойных SQL базы данных Azure, удаляемой.</span><span class="sxs-lookup"><span data-stu-id="34e9a-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e9a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="34e9a-117">-Force</span></span>
<span data-ttu-id="34e9a-118">Пропустите сообщение с подтверждением выполнения действия.</span><span class="sxs-lookup"><span data-stu-id="34e9a-118">Skip confirmation message for performing the action.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e9a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34e9a-119">-ResourceGroupName</span></span>
<span data-ttu-id="34e9a-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="34e9a-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="34e9a-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="34e9a-121">-ServerName</span></span>
<span data-ttu-id="34e9a-122">Имя основного сервера баз данных Azure SQL группы failover.</span><span class="sxs-lookup"><span data-stu-id="34e9a-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e9a-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34e9a-123">-Confirm</span></span>
<span data-ttu-id="34e9a-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="34e9a-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e9a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34e9a-125">-WhatIf</span></span>
<span data-ttu-id="34e9a-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34e9a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34e9a-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="34e9a-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e9a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34e9a-128">CommonParameters</span></span>
<span data-ttu-id="34e9a-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34e9a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34e9a-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34e9a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34e9a-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="34e9a-131">INPUTS</span></span>

### <span data-ttu-id="34e9a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="34e9a-132">System.String</span></span>

## <span data-ttu-id="34e9a-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="34e9a-133">OUTPUTS</span></span>

### <span data-ttu-id="34e9a-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="34e9a-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="34e9a-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="34e9a-135">NOTES</span></span>

## <span data-ttu-id="34e9a-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34e9a-136">RELATED LINKS</span></span>

[<span data-ttu-id="34e9a-137">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="34e9a-137">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="34e9a-138">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="34e9a-138">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="34e9a-139">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="34e9a-139">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="34e9a-140">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="34e9a-140">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="34e9a-141">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="34e9a-141">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="34e9a-142">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="34e9a-142">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="34e9a-143">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="34e9a-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)