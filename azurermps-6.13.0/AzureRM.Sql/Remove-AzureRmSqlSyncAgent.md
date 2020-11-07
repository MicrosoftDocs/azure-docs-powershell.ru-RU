---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlSyncAgent.md
ms.openlocfilehash: 9886d2d32dd3bce8841dcf2652cf89054335b112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568125"
---
# <span data-ttu-id="02a9c-101">Remove-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="02a9c-101">Remove-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="02a9c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="02a9c-102">SYNOPSIS</span></span>
<span data-ttu-id="02a9c-103">Удаляет агент Azure SQL Sync.</span><span class="sxs-lookup"><span data-stu-id="02a9c-103">Removes an Azure SQL Sync Agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02a9c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="02a9c-104">SYNTAX</span></span>

```
Remove-AzureRmSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02a9c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02a9c-105">DESCRIPTION</span></span>
<span data-ttu-id="02a9c-106">Командлет **Remove-AzureRmSqlSyncAgent** удаляет агент Azure SQL Sync Agent.</span><span class="sxs-lookup"><span data-stu-id="02a9c-106">The **Remove-AzureRmSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="02a9c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="02a9c-107">EXAMPLES</span></span>

### <span data-ttu-id="02a9c-108">Пример 1: Удаление агента синхронизации</span><span class="sxs-lookup"><span data-stu-id="02a9c-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="02a9c-109">Эта команда удаляет агент Azure SQL Sync Agent с именем syncAgent01.</span><span class="sxs-lookup"><span data-stu-id="02a9c-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="02a9c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="02a9c-110">PARAMETERS</span></span>

### <span data-ttu-id="02a9c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a9c-111">-DefaultProfile</span></span>
<span data-ttu-id="02a9c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="02a9c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02a9c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="02a9c-113">-Force</span></span>
<span data-ttu-id="02a9c-114">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="02a9c-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="02a9c-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="02a9c-115">-Name</span></span>
<span data-ttu-id="02a9c-116">Имя агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="02a9c-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02a9c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02a9c-117">-PassThru</span></span>
<span data-ttu-id="02a9c-118">Определяет, возвращать ли удаленный агент синхронизации</span><span class="sxs-lookup"><span data-stu-id="02a9c-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="02a9c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02a9c-119">-ResourceGroupName</span></span>
<span data-ttu-id="02a9c-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="02a9c-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="02a9c-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="02a9c-121">-ServerName</span></span>
<span data-ttu-id="02a9c-122">Имя сервера Azure SQL Server, в котором находится агент синхронизации.</span><span class="sxs-lookup"><span data-stu-id="02a9c-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="02a9c-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02a9c-123">-Confirm</span></span>
<span data-ttu-id="02a9c-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="02a9c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02a9c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02a9c-125">-WhatIf</span></span>
<span data-ttu-id="02a9c-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="02a9c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02a9c-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="02a9c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02a9c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a9c-128">CommonParameters</span></span>
<span data-ttu-id="02a9c-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="02a9c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a9c-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02a9c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a9c-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="02a9c-131">INPUTS</span></span>

### <span data-ttu-id="02a9c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="02a9c-132">System.String</span></span>

## <span data-ttu-id="02a9c-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="02a9c-133">OUTPUTS</span></span>

### <span data-ttu-id="02a9c-134">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="02a9c-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="02a9c-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="02a9c-135">NOTES</span></span>

## <span data-ttu-id="02a9c-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02a9c-136">RELATED LINKS</span></span>

[<span data-ttu-id="02a9c-137">New-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="02a9c-137">New-AzureRmSqlSyncAgent</span></span>](./New-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="02a9c-138">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="02a9c-138">Get-AzureRmSqlSyncAgent</span></span>](./Get-AzureRmSqlSyncAgent.md)
