---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 149579bb6bbcd4ee5fe5fa192ad040e6e4c68b28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570039"
---
# <span data-ttu-id="e4510-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="e4510-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="e4510-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e4510-102">SYNOPSIS</span></span>
<span data-ttu-id="e4510-103">Изменяет состояние автоматического выполнения помощника по базам данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e4510-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4510-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e4510-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -DatabaseName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e4510-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4510-105">DESCRIPTION</span></span>
<span data-ttu-id="e4510-106">Командлет **Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** изменяет свойство автоматического выполнения для помощника по базам данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e4510-106">The **Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="e4510-107">В настоящее время этот командлет поддерживает значения Enabled, Disabled и Default.</span><span class="sxs-lookup"><span data-stu-id="e4510-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="e4510-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e4510-108">EXAMPLES</span></span>

### <span data-ttu-id="e4510-109">Пример 1: Включение автоматического выполнения для помощника</span><span class="sxs-lookup"><span data-stu-id="e4510-109">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -ResourceGroupName "ContosoRunnersProd" -ServerName "runner-australia-east" -DatabaseName "ContosoRunner" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
DatabaseName                   : ContosoRunner
ResourceGroupName              : ContosoRunnersProd
ServerName                     : runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="e4510-110">Эта команда изменяет состояние автоматического выполнения для помощника с именем CreateIndex на Enabled.</span><span class="sxs-lookup"><span data-stu-id="e4510-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="e4510-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e4510-111">PARAMETERS</span></span>

### <span data-ttu-id="e4510-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="e4510-112">-AdvisorName</span></span>
<span data-ttu-id="e4510-113">Указывает имя помощника, для которого этот командлет изменяет состояние.</span><span class="sxs-lookup"><span data-stu-id="e4510-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

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

### <span data-ttu-id="e4510-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="e4510-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="e4510-115">Задает значение состояния.</span><span class="sxs-lookup"><span data-stu-id="e4510-115">Specifies the value for the status.</span></span>
<span data-ttu-id="e4510-116">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e4510-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e4510-117">Включаем</span><span class="sxs-lookup"><span data-stu-id="e4510-117">Enabled</span></span> 
- <span data-ttu-id="e4510-118">Отключает</span><span class="sxs-lookup"><span data-stu-id="e4510-118">Disabled</span></span> 
- <span data-ttu-id="e4510-119">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="e4510-119">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4510-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e4510-120">-DatabaseName</span></span>
<span data-ttu-id="e4510-121">Указывает имя базы данных, для которой этот командлет изменяет состояние.</span><span class="sxs-lookup"><span data-stu-id="e4510-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

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

### <span data-ttu-id="e4510-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4510-122">-ResourceGroupName</span></span>
<span data-ttu-id="e4510-123">Указывает имя группы ресурсов для сервера, который содержит эту базу данных.</span><span class="sxs-lookup"><span data-stu-id="e4510-123">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="e4510-124">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="e4510-124">-ServerName</span></span>
<span data-ttu-id="e4510-125">Указывает имя сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="e4510-125">Specifies the name of the server for the database.</span></span>

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

### <span data-ttu-id="e4510-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4510-126">-Confirm</span></span>
<span data-ttu-id="e4510-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e4510-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4510-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4510-128">-WhatIf</span></span>
<span data-ttu-id="e4510-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e4510-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4510-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e4510-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4510-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4510-131">-DefaultProfile</span></span>
<span data-ttu-id="e4510-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e4510-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4510-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4510-133">CommonParameters</span></span>
<span data-ttu-id="e4510-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e4510-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4510-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4510-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4510-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e4510-136">INPUTS</span></span>

## <span data-ttu-id="e4510-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4510-137">OUTPUTS</span></span>

### <span data-ttu-id="e4510-138">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="e4510-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>
<span data-ttu-id="e4510-139">Этот командлет возвращает объект **AzureSqlDatabaseAdvisorModel** .</span><span class="sxs-lookup"><span data-stu-id="e4510-139">This cmdlet returns an **AzureSqlDatabaseAdvisorModel** object.</span></span>

## <span data-ttu-id="e4510-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="e4510-140">NOTES</span></span>

## <span data-ttu-id="e4510-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4510-141">RELATED LINKS</span></span>

[<span data-ttu-id="e4510-142">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="e4510-142">Get-AzureRmSqlDatabaseAdvisor</span></span>](./Get-AzureRmSqlDatabaseAdvisor.md)

[<span data-ttu-id="e4510-143">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="e4510-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
