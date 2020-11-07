---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/update-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncMember.md
ms.openlocfilehash: afaa0446b46fca343b4d53ae491c67ef1ceb923a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567372"
---
# <span data-ttu-id="ba7a9-101">Update-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ba7a9-101">Update-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="ba7a9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba7a9-102">SYNOPSIS</span></span>
<span data-ttu-id="ba7a9-103">Обновляет элемент синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-103">Updates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba7a9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba7a9-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba7a9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba7a9-105">DESCRIPTION</span></span>
<span data-ttu-id="ba7a9-106">Командлет **Update-AzureRmSqlSyncGroup** изменяет свойства члена синхронизации базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="ba7a9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba7a9-107">EXAMPLES</span></span>

### <span data-ttu-id="ba7a9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ba7a9-108">Example 1</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01"
-MemberDatabaseCredential $credential | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount-new
MemberDatabasePassword      : 
SyncState                   : Good
```

<span data-ttu-id="ba7a9-109">Эта команда сбрасывает пароль администратора для базы данных пользователей.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="ba7a9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba7a9-110">PARAMETERS</span></span>

### <span data-ttu-id="ba7a9-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ba7a9-111">-DatabaseName</span></span>
<span data-ttu-id="ba7a9-112">Имя базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-112">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba7a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba7a9-113">-DefaultProfile</span></span>
<span data-ttu-id="ba7a9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ba7a9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba7a9-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="ba7a9-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="ba7a9-116">Учетные данные (имя пользователя и пароль) для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba7a9-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ba7a9-117">-Name</span></span>
<span data-ttu-id="ba7a9-118">Имя элемента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-118">The sync member name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba7a9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba7a9-119">-ResourceGroupName</span></span>
<span data-ttu-id="ba7a9-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-120">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba7a9-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="ba7a9-121">-ServerName</span></span>
<span data-ttu-id="ba7a9-122">Имя сервера Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-122">The name of the Azure SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba7a9-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="ba7a9-123">-SyncGroupName</span></span>
<span data-ttu-id="ba7a9-124">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-124">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba7a9-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba7a9-125">-Confirm</span></span>
<span data-ttu-id="ba7a9-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba7a9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba7a9-127">-WhatIf</span></span>
<span data-ttu-id="ba7a9-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba7a9-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba7a9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba7a9-130">CommonParameters</span></span>
<span data-ttu-id="ba7a9-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba7a9-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba7a9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba7a9-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba7a9-133">INPUTS</span></span>

### <span data-ttu-id="ba7a9-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="ba7a9-134">None</span></span>
<span data-ttu-id="ba7a9-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="ba7a9-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ba7a9-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba7a9-136">OUTPUTS</span></span>

### <span data-ttu-id="ba7a9-137">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="ba7a9-137">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="ba7a9-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba7a9-138">NOTES</span></span>

## <span data-ttu-id="ba7a9-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba7a9-139">RELATED LINKS</span></span>

[<span data-ttu-id="ba7a9-140">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ba7a9-140">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="ba7a9-141">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ba7a9-141">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="ba7a9-142">Remove-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="ba7a9-142">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)
