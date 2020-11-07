---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseIndexRecommendations.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseIndexRecommendations.md
ms.openlocfilehash: b3b09e9027a578809fe68a90630331ad6ee35943
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569163"
---
# <span data-ttu-id="1a3c3-101">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="1a3c3-101">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>

## <span data-ttu-id="1a3c3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1a3c3-102">SYNOPSIS</span></span>
<span data-ttu-id="1a3c3-103">Получает рекомендованные операции с индексами для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="1a3c3-103">Gets the recommended index operations for a server or database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a3c3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1a3c3-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseIndexRecommendations -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a3c3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a3c3-105">DESCRIPTION</span></span>
<span data-ttu-id="1a3c3-106">Командлет **Get-AzureRmSqlDatabaseIndexRecommendations** получает рекомендованные операции с индексами для сервера базы данных SQL Azure или базы данных.</span><span class="sxs-lookup"><span data-stu-id="1a3c3-106">The **Get-AzureRmSqlDatabaseIndexRecommendations** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="1a3c3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1a3c3-107">EXAMPLES</span></span>

### <span data-ttu-id="1a3c3-108">Пример 1: получение рекомендаций по индексам для всех баз данных на сервере</span><span class="sxs-lookup"><span data-stu-id="1a3c3-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="1a3c3-109">Эта команда возвращает рекомендации по индексам для всех баз данных на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="1a3c3-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="1a3c3-110">Пример 2: получение рекомендаций по индексу для определенной базы данных</span><span class="sxs-lookup"><span data-stu-id="1a3c3-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="1a3c3-111">Эта команда возвращает рекомендации по индексированию для определенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="1a3c3-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="1a3c3-112">Пример 3: получение одной рекомендации по индексу по имени</span><span class="sxs-lookup"><span data-stu-id="1a3c3-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="1a3c3-113">Эта команда возвращает один совет по индексу по имени.</span><span class="sxs-lookup"><span data-stu-id="1a3c3-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="1a3c3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1a3c3-114">PARAMETERS</span></span>

### <span data-ttu-id="1a3c3-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1a3c3-115">-DatabaseName</span></span>
<span data-ttu-id="1a3c3-116">Указывает имя базы данных, для которой этот командлет получает рекомендации по индексу.</span><span class="sxs-lookup"><span data-stu-id="1a3c3-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c3-117">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="1a3c3-117">-IndexRecommendationName</span></span>
<span data-ttu-id="1a3c3-118">Указывает имя рекомендации по индексированию, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1a3c3-118">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a3c3-119">-ResourceGroupName</span></span>
<span data-ttu-id="1a3c3-120">Указывает имя группы ресурсов, для которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="1a3c3-120">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="1a3c3-121">Этот командлет получает рекомендации по индексу для базы данных, размещенной на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="1a3c3-121">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="1a3c3-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="1a3c3-122">-ServerName</span></span>
<span data-ttu-id="1a3c3-123">Указывает сервер, на котором размещена база данных, для которой этот командлет получает рекомендации по индексу.</span><span class="sxs-lookup"><span data-stu-id="1a3c3-123">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c3-124">-TableName</span><span class="sxs-lookup"><span data-stu-id="1a3c3-124">-TableName</span></span>
<span data-ttu-id="1a3c3-125">Указывает имя таблицы Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1a3c3-125">Specifies the name of an Azure SQL table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a3c3-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a3c3-126">-Confirm</span></span>
<span data-ttu-id="1a3c3-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1a3c3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a3c3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a3c3-128">-WhatIf</span></span>
<span data-ttu-id="1a3c3-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1a3c3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a3c3-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1a3c3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a3c3-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a3c3-131">-DefaultProfile</span></span>
<span data-ttu-id="1a3c3-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a3c3-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a3c3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a3c3-133">CommonParameters</span></span>
<span data-ttu-id="1a3c3-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1a3c3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a3c3-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a3c3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a3c3-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1a3c3-136">INPUTS</span></span>

## <span data-ttu-id="1a3c3-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a3c3-137">OUTPUTS</span></span>

## <span data-ttu-id="1a3c3-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="1a3c3-138">NOTES</span></span>

## <span data-ttu-id="1a3c3-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a3c3-139">RELATED LINKS</span></span>

[<span data-ttu-id="1a3c3-140">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="1a3c3-140">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="1a3c3-141">Остановить-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="1a3c3-141">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)