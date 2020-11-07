---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
ms.openlocfilehash: a9f86b9b316c14e40505932e0bf3b30fc66c55c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567213"
---
# <span data-ttu-id="ce5ed-101">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="ce5ed-101">Get-AzureRmSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="ce5ed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ce5ed-102">SYNOPSIS</span></span>
<span data-ttu-id="ce5ed-103">Возвращает эластичные базы данных в пуле эластичных БД и их значения свойств.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-103">Gets elastic databases in an elastic pool and their property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce5ed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ce5ed-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce5ed-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce5ed-105">DESCRIPTION</span></span>
<span data-ttu-id="ce5ed-106">Командлет **Get-AzureRmSqlElasticPoolDatabase** получает эластичные базы данных в пуле эластичных БД и значения их свойств.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-106">The **Get-AzureRmSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="ce5ed-107">В базе данных SQL Azure можно указать имя эластичной базы данных, чтобы просмотреть значения свойств только для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="ce5ed-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ce5ed-108">EXAMPLES</span></span>

### <span data-ttu-id="ce5ed-109">Пример 1: получение всех баз данных в пуле эластичных БД</span><span class="sxs-lookup"><span data-stu-id="ce5ed-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="ce5ed-110">Эта команда получает все базы данных в пуле эластичных БД с именем ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="ce5ed-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ce5ed-111">PARAMETERS</span></span>

### <span data-ttu-id="ce5ed-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ce5ed-112">-DatabaseName</span></span>
<span data-ttu-id="ce5ed-113">Указывает имя базы данных SQL, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-113">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ce5ed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce5ed-114">-DefaultProfile</span></span>
<span data-ttu-id="ce5ed-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ce5ed-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce5ed-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ce5ed-116">-ElasticPoolName</span></span>
<span data-ttu-id="ce5ed-117">Указывает имя эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-117">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="ce5ed-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce5ed-118">-ResourceGroupName</span></span>
<span data-ttu-id="ce5ed-119">Указывает имя группы ресурсов, которой назначен эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="ce5ed-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="ce5ed-120">-ServerName</span></span>
<span data-ttu-id="ce5ed-121">Указывает имя сервера, который содержит эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="ce5ed-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce5ed-122">-Confirm</span></span>
<span data-ttu-id="ce5ed-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce5ed-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce5ed-124">-WhatIf</span></span>
<span data-ttu-id="ce5ed-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce5ed-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce5ed-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce5ed-127">CommonParameters</span></span>
<span data-ttu-id="ce5ed-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ce5ed-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce5ed-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce5ed-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce5ed-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ce5ed-130">INPUTS</span></span>

### <span data-ttu-id="ce5ed-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ce5ed-131">System.String</span></span>

## <span data-ttu-id="ce5ed-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce5ed-132">OUTPUTS</span></span>

### <span data-ttu-id="ce5ed-133">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ce5ed-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ce5ed-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="ce5ed-134">NOTES</span></span>

## <span data-ttu-id="ce5ed-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce5ed-135">RELATED LINKS</span></span>

[<span data-ttu-id="ce5ed-136">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ce5ed-136">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="ce5ed-137">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="ce5ed-137">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="ce5ed-138">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ce5ed-138">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="ce5ed-139">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ce5ed-139">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="ce5ed-140">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="ce5ed-140">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)
