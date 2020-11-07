---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 4e5f2578d0e9dbb2139b330ec0a7c2fe81b3124e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560007"
---
# <span data-ttu-id="36d82-101">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="36d82-101">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="36d82-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36d82-102">SYNOPSIS</span></span>
<span data-ttu-id="36d82-103">Задает свойства правила маскирования данных для базы данных.</span><span class="sxs-lookup"><span data-stu-id="36d82-103">Sets the properties of a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36d82-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36d82-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36d82-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36d82-105">DESCRIPTION</span></span>
<span data-ttu-id="36d82-106">Командлет **Set-AzureRmSqlDatabaseDataMaskingRule** задает правило маскирования данных для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="36d82-106">The **Set-AzureRmSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="36d82-107">Чтобы использовать командлет, укажите параметры *ResourceGroupName* , *ServerName* , *DatabaseName* и *RuleId* , чтобы определить правило.</span><span class="sxs-lookup"><span data-stu-id="36d82-107">To use the cmdlet, provide the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="36d82-108">Вы можете предоставить любой из параметров *SchemaName* , *TableName* и *ColumnName* , чтобы перенацелить правило.</span><span class="sxs-lookup"><span data-stu-id="36d82-108">You can provide any of the parameters of *SchemaName* , *TableName* , and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="36d82-109">Укажите параметр *MaskingFunction* , чтобы изменить способ маскирования данных.</span><span class="sxs-lookup"><span data-stu-id="36d82-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="36d82-110">Если вы задаете значение числа или текста для *MaskingFunction* , вы можете указать параметры *NumberFrom* и *NumberTo* для масок номеров, а также параметры *PrefixSize* , *ReplacementString* и *SuffixSize* для маскирования текста.</span><span class="sxs-lookup"><span data-stu-id="36d82-110">If you specify a value of Number or Text for *MaskingFunction* , you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize* , *ReplacementString* , and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="36d82-111">Если команда выполнена успешно, а параметр *PassThru* указан, командлет возвращает объект, описывающий свойства правила масок данных и идентификаторы правил.</span><span class="sxs-lookup"><span data-stu-id="36d82-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="36d82-112">Идентификаторы правила включают, но не ограничиваются, **ResourceGroupName** , **ServerName** , **DatabaseName** и **RuleId**.</span><span class="sxs-lookup"><span data-stu-id="36d82-112">Rule identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , **DatabaseName** , and **RuleId**.</span></span>
<span data-ttu-id="36d82-113">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="36d82-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="36d82-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36d82-114">EXAMPLES</span></span>

### <span data-ttu-id="36d82-115">Пример 1: изменение диапазона правила маскировки данных в базе данных</span><span class="sxs-lookup"><span data-stu-id="36d82-115">Example 1: Change the range of a data masking rule in a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="36d82-116">Эта команда изменяет правило маскировки данных с ИДЕНТИФИКАТОРом Rule17.</span><span class="sxs-lookup"><span data-stu-id="36d82-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="36d82-117">Это правило работает в базе данных с именем Database01 на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="36d82-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="36d82-118">Эта команда изменяет границы интервала, в течение которого случайное число генерируется как маскированное значение.</span><span class="sxs-lookup"><span data-stu-id="36d82-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="36d82-119">Новый диапазон находится в диапазоне от 23 до 42.</span><span class="sxs-lookup"><span data-stu-id="36d82-119">The new range is between 23 and 42.</span></span>

## <span data-ttu-id="36d82-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36d82-120">PARAMETERS</span></span>

### <span data-ttu-id="36d82-121">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="36d82-121">-ColumnName</span></span>
<span data-ttu-id="36d82-122">Задает имя столбца, на которое указывает правило маскирования.</span><span class="sxs-lookup"><span data-stu-id="36d82-122">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="36d82-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="36d82-123">-DatabaseName</span></span>
<span data-ttu-id="36d82-124">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="36d82-124">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="36d82-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36d82-125">-DefaultProfile</span></span>
<span data-ttu-id="36d82-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="36d82-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36d82-127">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="36d82-127">-MaskingFunction</span></span>
<span data-ttu-id="36d82-128">Указывает функцию маскирования, используемую правилом.</span><span class="sxs-lookup"><span data-stu-id="36d82-128">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="36d82-129">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="36d82-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="36d82-130">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="36d82-130">Default</span></span>
- <span data-ttu-id="36d82-131">Маскировка</span><span class="sxs-lookup"><span data-stu-id="36d82-131">NoMasking</span></span>
- <span data-ttu-id="36d82-132">Текстовые</span><span class="sxs-lookup"><span data-stu-id="36d82-132">Text</span></span>
- <span data-ttu-id="36d82-133">Счетчик</span><span class="sxs-lookup"><span data-stu-id="36d82-133">Number</span></span>
- <span data-ttu-id="36d82-134">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="36d82-134">SocialSecurityNumber</span></span>
- <span data-ttu-id="36d82-135">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="36d82-135">CreditCardNumber</span></span>
- <span data-ttu-id="36d82-136">Адрес электронной почты по умолчанию используется значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="36d82-136">Email The default value is Default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36d82-137">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="36d82-137">-NumberFrom</span></span>
<span data-ttu-id="36d82-138">Задает меньшую границу интервала, из которого выделено случайное значение.</span><span class="sxs-lookup"><span data-stu-id="36d82-138">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="36d82-139">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Number.</span><span class="sxs-lookup"><span data-stu-id="36d82-139">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="36d82-140">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="36d82-140">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36d82-141">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="36d82-141">-NumberTo</span></span>
<span data-ttu-id="36d82-142">Задает верхнюю границу интервала, из которого выделено случайное значение.</span><span class="sxs-lookup"><span data-stu-id="36d82-142">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="36d82-143">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Number.</span><span class="sxs-lookup"><span data-stu-id="36d82-143">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="36d82-144">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="36d82-144">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36d82-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36d82-145">-PassThru</span></span>
<span data-ttu-id="36d82-146">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="36d82-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="36d82-147">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="36d82-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="36d82-148">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="36d82-148">-PrefixSize</span></span>
<span data-ttu-id="36d82-149">Указывает число знаков в начале текста, для которого не задана маска.</span><span class="sxs-lookup"><span data-stu-id="36d82-149">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="36d82-150">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.</span><span class="sxs-lookup"><span data-stu-id="36d82-150">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="36d82-151">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="36d82-151">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36d82-152">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="36d82-152">-ReplacementString</span></span>
<span data-ttu-id="36d82-153">Задает количество символов в конце текста, которые не были скрыты.</span><span class="sxs-lookup"><span data-stu-id="36d82-153">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="36d82-154">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.</span><span class="sxs-lookup"><span data-stu-id="36d82-154">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="36d82-155">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="36d82-155">The default value is 0.</span></span>

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

### <span data-ttu-id="36d82-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36d82-156">-ResourceGroupName</span></span>
<span data-ttu-id="36d82-157">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="36d82-157">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="36d82-158">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="36d82-158">-SchemaName</span></span>
<span data-ttu-id="36d82-159">Указывает имя схемы.</span><span class="sxs-lookup"><span data-stu-id="36d82-159">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="36d82-160">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="36d82-160">-ServerName</span></span>
<span data-ttu-id="36d82-161">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="36d82-161">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="36d82-162">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="36d82-162">-SuffixSize</span></span>
<span data-ttu-id="36d82-163">Задает количество символов в конце текста, которые не были скрыты.</span><span class="sxs-lookup"><span data-stu-id="36d82-163">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="36d82-164">Указывайте этот параметр только в том случае, если для параметра *MaskingFunction* задано значение Text.</span><span class="sxs-lookup"><span data-stu-id="36d82-164">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="36d82-165">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="36d82-165">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36d82-166">-TableName</span><span class="sxs-lookup"><span data-stu-id="36d82-166">-TableName</span></span>
<span data-ttu-id="36d82-167">Указывает имя таблицы базы данных, которая содержит столбец с маскированием.</span><span class="sxs-lookup"><span data-stu-id="36d82-167">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="36d82-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36d82-168">-Confirm</span></span>
<span data-ttu-id="36d82-169">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="36d82-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36d82-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36d82-170">-WhatIf</span></span>
<span data-ttu-id="36d82-171">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="36d82-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36d82-172">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="36d82-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36d82-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d82-173">CommonParameters</span></span>
<span data-ttu-id="36d82-174">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36d82-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d82-175">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36d82-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d82-176">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36d82-176">INPUTS</span></span>

### <span data-ttu-id="36d82-177">System. String</span><span class="sxs-lookup"><span data-stu-id="36d82-177">System.String</span></span>

### <span data-ttu-id="36d82-178">System. Nullable "1 [[System. UInt32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="36d82-178">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="36d82-179">System. Nullable "1 [[System. Double, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="36d82-179">System.Nullable\`1[[System.Double, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="36d82-180">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36d82-180">OUTPUTS</span></span>

### <span data-ttu-id="36d82-181">Microsoft. Azure. Commands. SQL. маскирует. Model. DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="36d82-181">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="36d82-182">Пуск</span><span class="sxs-lookup"><span data-stu-id="36d82-182">NOTES</span></span>

## <span data-ttu-id="36d82-183">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36d82-183">RELATED LINKS</span></span>

[<span data-ttu-id="36d82-184">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="36d82-184">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="36d82-185">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="36d82-185">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="36d82-186">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="36d82-186">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="36d82-187">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="36d82-187">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

