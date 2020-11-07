---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: b53b32b30e1b69da94ac8319ed3a5f4eee7ffc0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557052"
---
# <span data-ttu-id="2df18-101">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2df18-101">New-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="2df18-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2df18-102">SYNOPSIS</span></span>
<span data-ttu-id="2df18-103">Создание правила маскирования данных для базы данных.</span><span class="sxs-lookup"><span data-stu-id="2df18-103">Creates a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2df18-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2df18-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2df18-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2df18-105">DESCRIPTION</span></span>
<span data-ttu-id="2df18-106">Командлет **New-AzureRmSqlDatabaseDataMaskingRule** создает правило маскирования данных для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2df18-106">The **New-AzureRmSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="2df18-107">Чтобы использовать командлет, используйте параметры *ResourceGroupName* , *ServerName* , *DatabaseName* и *RuleId* , чтобы определить правило.</span><span class="sxs-lookup"><span data-stu-id="2df18-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="2df18-108">Укажите *TableName* и *ColumnName* для указания целевого объекта правила и параметра *MaskingFunction* , определяющего способ маскирования данных.</span><span class="sxs-lookup"><span data-stu-id="2df18-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>

<span data-ttu-id="2df18-109">Если *MaskingFunction* имеет значение число или текст, вы можете указать параметры *NumberFrom* и *NumberTo* , для масок номеров, а также *PrefixSize* , *ReplacementString* и *SuffixSize* для маскирования текста.</span><span class="sxs-lookup"><span data-stu-id="2df18-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize* , *ReplacementString* , and *SuffixSize* for text masking.</span></span>

<span data-ttu-id="2df18-110">Если команда пройдет успешно и используется параметр *PassThru* , командлет возвращает объект, описывающий свойства правила масок данных в дополнение к идентификаторам правил.</span><span class="sxs-lookup"><span data-stu-id="2df18-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="2df18-111">Идентификаторы правила включают, но не ограничиваются, *ResourceGroupName* , *ServerName* , *DatabaseName* и *RuleID*.</span><span class="sxs-lookup"><span data-stu-id="2df18-111">Rule identifiers include, but are not limited to, *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleID*.</span></span>

<span data-ttu-id="2df18-112">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="2df18-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="2df18-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2df18-113">EXAMPLES</span></span>

### <span data-ttu-id="2df18-114">Пример 1: Создание правила маскирования данных для числового столбца в базе данных</span><span class="sxs-lookup"><span data-stu-id="2df18-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RuleId "Rule01" -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="2df18-115">Эта команда создает правило маскировки данных для столбца с именем Column01 в таблице с именем Table01 в схеме с именем Schema01.</span><span class="sxs-lookup"><span data-stu-id="2df18-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="2df18-116">База данных с именем Database01 включает все эти элементы.</span><span class="sxs-lookup"><span data-stu-id="2df18-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="2df18-117">Правило — это правило маскирования чисел, использующее случайное число в интервале от 5 до 14 в качестве значения маски.</span><span class="sxs-lookup"><span data-stu-id="2df18-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>
<span data-ttu-id="2df18-118">Правило называется Rule01.</span><span class="sxs-lookup"><span data-stu-id="2df18-118">The rule is named Rule01.</span></span>

## <span data-ttu-id="2df18-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2df18-119">PARAMETERS</span></span>

### <span data-ttu-id="2df18-120">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="2df18-120">-ColumnName</span></span>
<span data-ttu-id="2df18-121">Задает имя столбца, на которое указывает правило маскирования.</span><span class="sxs-lookup"><span data-stu-id="2df18-121">Specifies the name of the column targeted by the masking rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df18-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2df18-122">-DatabaseName</span></span>
<span data-ttu-id="2df18-123">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="2df18-123">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="2df18-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2df18-124">-DefaultProfile</span></span>
<span data-ttu-id="2df18-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2df18-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2df18-126">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="2df18-126">-MaskingFunction</span></span>
<span data-ttu-id="2df18-127">Указывает функцию маскирования, используемую правилом.</span><span class="sxs-lookup"><span data-stu-id="2df18-127">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="2df18-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2df18-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2df18-129">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="2df18-129">Default</span></span>
- <span data-ttu-id="2df18-130">Маскировка</span><span class="sxs-lookup"><span data-stu-id="2df18-130">NoMasking</span></span>
- <span data-ttu-id="2df18-131">Текстовые</span><span class="sxs-lookup"><span data-stu-id="2df18-131">Text</span></span>
- <span data-ttu-id="2df18-132">Счетчик</span><span class="sxs-lookup"><span data-stu-id="2df18-132">Number</span></span>
- <span data-ttu-id="2df18-133">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="2df18-133">SocialSecurityNumber</span></span>
- <span data-ttu-id="2df18-134">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="2df18-134">CreditCardNumber</span></span>
- <span data-ttu-id="2df18-135">Отправить по электронной почте</span><span class="sxs-lookup"><span data-stu-id="2df18-135">Email</span></span>

<span data-ttu-id="2df18-136">По умолчанию используется значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2df18-136">The default value is Default.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df18-137">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="2df18-137">-NumberFrom</span></span>
<span data-ttu-id="2df18-138">Задает меньшую границу интервала, из которого выделено случайное значение.</span><span class="sxs-lookup"><span data-stu-id="2df18-138">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="2df18-139">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Number.</span><span class="sxs-lookup"><span data-stu-id="2df18-139">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="2df18-140">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="2df18-140">The default value is 0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df18-141">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="2df18-141">-NumberTo</span></span>
<span data-ttu-id="2df18-142">Задает верхнюю границу интервала, из которого выделено случайное значение.</span><span class="sxs-lookup"><span data-stu-id="2df18-142">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="2df18-143">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Number.</span><span class="sxs-lookup"><span data-stu-id="2df18-143">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="2df18-144">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="2df18-144">The default value is 0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df18-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2df18-145">-PassThru</span></span>
<span data-ttu-id="2df18-146">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="2df18-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2df18-147">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2df18-147">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2df18-148">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="2df18-148">-PrefixSize</span></span>
<span data-ttu-id="2df18-149">Указывает число знаков в начале текста, для которого не задана маска.</span><span class="sxs-lookup"><span data-stu-id="2df18-149">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="2df18-150">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.</span><span class="sxs-lookup"><span data-stu-id="2df18-150">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="2df18-151">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="2df18-151">The default value is 0.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df18-152">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="2df18-152">-ReplacementString</span></span>
<span data-ttu-id="2df18-153">Указывает число знаков в конце текста, которые не были скрыты.</span><span class="sxs-lookup"><span data-stu-id="2df18-153">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="2df18-154">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.</span><span class="sxs-lookup"><span data-stu-id="2df18-154">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="2df18-155">Значением по умолчанию является пустая строка.</span><span class="sxs-lookup"><span data-stu-id="2df18-155">The default value is an empty string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df18-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2df18-156">-ResourceGroupName</span></span>
<span data-ttu-id="2df18-157">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="2df18-157">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="2df18-158">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="2df18-158">-SchemaName</span></span>
<span data-ttu-id="2df18-159">Указывает имя схемы.</span><span class="sxs-lookup"><span data-stu-id="2df18-159">Specifies the name of a schema.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df18-160">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="2df18-160">-ServerName</span></span>
<span data-ttu-id="2df18-161">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="2df18-161">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="2df18-162">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="2df18-162">-SuffixSize</span></span>
<span data-ttu-id="2df18-163">Задает количество символов в конце текста, которые не были скрыты.</span><span class="sxs-lookup"><span data-stu-id="2df18-163">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="2df18-164">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.</span><span class="sxs-lookup"><span data-stu-id="2df18-164">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="2df18-165">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="2df18-165">The default value is 0.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df18-166">-TableName</span><span class="sxs-lookup"><span data-stu-id="2df18-166">-TableName</span></span>
<span data-ttu-id="2df18-167">Указывает имя таблицы базы данных, которая содержит столбец с маскированием.</span><span class="sxs-lookup"><span data-stu-id="2df18-167">Specifies the name of the database table that contains the masked column.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df18-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2df18-168">-Confirm</span></span>
<span data-ttu-id="2df18-169">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2df18-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2df18-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2df18-170">-WhatIf</span></span>
<span data-ttu-id="2df18-171">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2df18-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2df18-172">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2df18-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2df18-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2df18-173">CommonParameters</span></span>
<span data-ttu-id="2df18-174">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2df18-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2df18-175">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2df18-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2df18-176">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2df18-176">INPUTS</span></span>

###  
<span data-ttu-id="2df18-177">Ничего.</span><span class="sxs-lookup"><span data-stu-id="2df18-177">None.</span></span>

## <span data-ttu-id="2df18-178">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2df18-178">OUTPUTS</span></span>

### <span data-ttu-id="2df18-179">Microsoft. Azure. Commands. SQL. Security. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="2df18-179">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="2df18-180">Пуск</span><span class="sxs-lookup"><span data-stu-id="2df18-180">NOTES</span></span>

## <span data-ttu-id="2df18-181">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2df18-181">RELATED LINKS</span></span>

[<span data-ttu-id="2df18-182">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2df18-182">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="2df18-183">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2df18-183">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="2df18-184">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="2df18-184">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="2df18-185">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="2df18-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

