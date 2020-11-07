---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 01744DBD-1991-45EF-AA92-FD471F7E7551
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasetransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 0b2a9174f90ece49f417dd413e23da786b983a37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558791"
---
# <span data-ttu-id="1334e-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="1334e-101">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="1334e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1334e-102">SYNOPSIS</span></span>
<span data-ttu-id="1334e-103">Изменяет свойство TDE для базы данных.</span><span class="sxs-lookup"><span data-stu-id="1334e-103">Modifies TDE property for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1334e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1334e-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseTransparentDataEncryption [-State] <TransparentDataEncryptionStateType>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1334e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1334e-105">DESCRIPTION</span></span>
<span data-ttu-id="1334e-106">Командлет **Set-AzureRmSqlDatabaseTransparentDataEncryption** изменяет свойство шифрования прозрачных данных (TDE) для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1334e-106">The **Set-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet modifies the Transparent Data Encryption (TDE) property of an Azure SQL database.</span></span>
<span data-ttu-id="1334e-107">Дополнительные сведения можно найти в разделе прозрачное шифрование данных с базой данных Azure SQL https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) в сетевой библиотеке разработчиков Microsoft).</span><span class="sxs-lookup"><span data-stu-id="1334e-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>

<span data-ttu-id="1334e-108">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="1334e-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="1334e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1334e-109">EXAMPLES</span></span>

### <span data-ttu-id="1334e-110">Пример 1: Включение TDE для базы данных</span><span class="sxs-lookup"><span data-stu-id="1334e-110">Example 1: Enable TDE for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseTransparentDataEncryption -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -State Enabled
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
ResourceGroup01               Server01                      Database01                                            Enabled
```

<span data-ttu-id="1334e-111">Эта команда включает TDE для базы данных с именем Database01 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="1334e-111">This command enables TDE for the database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="1334e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1334e-112">PARAMETERS</span></span>

### <span data-ttu-id="1334e-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1334e-113">-DatabaseName</span></span>
<span data-ttu-id="1334e-114">Указывает имя базы данных, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1334e-114">Specifies the name of the database that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1334e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1334e-115">-DefaultProfile</span></span>
<span data-ttu-id="1334e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1334e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1334e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1334e-117">-ResourceGroupName</span></span>
<span data-ttu-id="1334e-118">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="1334e-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="1334e-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="1334e-119">-ServerName</span></span>
<span data-ttu-id="1334e-120">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="1334e-120">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="1334e-121">-State</span><span class="sxs-lookup"><span data-stu-id="1334e-121">-State</span></span>
<span data-ttu-id="1334e-122">Задает значение свойства TDE.</span><span class="sxs-lookup"><span data-stu-id="1334e-122">Specifies the value of the TDE property.</span></span>
<span data-ttu-id="1334e-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1334e-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1334e-124">Включаем</span><span class="sxs-lookup"><span data-stu-id="1334e-124">Enabled</span></span> 
- <span data-ttu-id="1334e-125">Отключает</span><span class="sxs-lookup"><span data-stu-id="1334e-125">Disabled</span></span>

```yaml
Type: TransparentDataEncryptionStateType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1334e-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1334e-126">-Confirm</span></span>
<span data-ttu-id="1334e-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1334e-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1334e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1334e-128">-WhatIf</span></span>
<span data-ttu-id="1334e-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1334e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1334e-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1334e-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1334e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1334e-131">CommonParameters</span></span>
<span data-ttu-id="1334e-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1334e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1334e-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1334e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1334e-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1334e-134">INPUTS</span></span>

### <span data-ttu-id="1334e-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="1334e-135">None</span></span>
<span data-ttu-id="1334e-136">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="1334e-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1334e-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1334e-137">OUTPUTS</span></span>

### <span data-ttu-id="1334e-138">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="1334e-138">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="1334e-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="1334e-139">NOTES</span></span>

## <span data-ttu-id="1334e-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1334e-140">RELATED LINKS</span></span>

[<span data-ttu-id="1334e-141">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="1334e-141">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="1334e-142">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="1334e-142">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="1334e-143">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="1334e-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

