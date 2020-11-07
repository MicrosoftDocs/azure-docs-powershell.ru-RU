---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: aa70b94614f8a0826a5d1563439afa8cb9ef6d95
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567866"
---
# <span data-ttu-id="e8772-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e8772-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="e8772-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8772-102">SYNOPSIS</span></span>
<span data-ttu-id="e8772-103">Задает политику обнаружения угроз для базы данных.</span><span class="sxs-lookup"><span data-stu-id="e8772-103">Sets a threat detection policy on a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8772-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8772-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8772-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8772-105">DESCRIPTION</span></span>
<span data-ttu-id="e8772-106">Командлет **Set-AzureRmSqlDatabaseThreatDetectionPolicy** устанавливает политику обнаружения угроз в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e8772-106">The **Set-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL database.</span></span>
<span data-ttu-id="e8772-107">Чтобы включить обнаружение угроз для базы данных, необходимо включить в этой базе данных политику аудита.</span><span class="sxs-lookup"><span data-stu-id="e8772-107">In order to enable threat detection on a database an auditing policy must be enabled on that database.</span></span>

<span data-ttu-id="e8772-108">Чтобы использовать этот командлет, укажите параметры *ResourceGroupName* , *ServerName* и *DatabaseName* , чтобы идентифицировать базу данных.</span><span class="sxs-lookup"><span data-stu-id="e8772-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>

<span data-ttu-id="e8772-109">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="e8772-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="e8772-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8772-110">EXAMPLES</span></span>

### <span data-ttu-id="e8772-111">Пример 1: Настройка политики обнаружения угроз для базы данных</span><span class="sxs-lookup"><span data-stu-id="e8772-111">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="e8772-112">Эта команда задает политику обнаружения угроз для базы данных с именем Database01 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="e8772-112">This command sets the threat detection policy for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="e8772-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8772-113">PARAMETERS</span></span>

### <span data-ttu-id="e8772-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e8772-114">-DatabaseName</span></span>
<span data-ttu-id="e8772-115">Указывает имя базы данных, в которой задана политика.</span><span class="sxs-lookup"><span data-stu-id="e8772-115">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="e8772-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8772-116">-DefaultProfile</span></span>
<span data-ttu-id="e8772-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e8772-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8772-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="e8772-118">-EmailAdmins</span></span>
<span data-ttu-id="e8772-119">Определяет, является ли политика обнаружения угроз контактными администраторами с помощью электронной почты.</span><span class="sxs-lookup"><span data-stu-id="e8772-119">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8772-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="e8772-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="e8772-121">Указывает массив типов обнаружения, исключаемых из политики.</span><span class="sxs-lookup"><span data-stu-id="e8772-121">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="e8772-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e8772-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e8772-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="e8772-123">Sql_Injection</span></span> 
- <span data-ttu-id="e8772-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="e8772-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="e8772-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="e8772-125">Access_Anomaly</span></span> 
- <span data-ttu-id="e8772-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="e8772-126">None</span></span>

```yaml
Type: DetectionType[]
Parameter Sets: (All)
Aliases:
Accepted values: Sql_Injection, Sql_Injection_Vulnerability, Access_Anomaly, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8772-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="e8772-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="e8772-128">Указывает список адресов электронной почты, разделенных точкой с запятой, по которым политика отправляет оповещения.</span><span class="sxs-lookup"><span data-stu-id="e8772-128">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="e8772-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8772-129">-PassThru</span></span>
<span data-ttu-id="e8772-130">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="e8772-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e8772-131">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e8772-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e8772-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8772-132">-ResourceGroupName</span></span>
<span data-ttu-id="e8772-133">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="e8772-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e8772-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e8772-134">-RetentionInDays</span></span>
<span data-ttu-id="e8772-135">Количество дней хранения для журналов аудита</span><span class="sxs-lookup"><span data-stu-id="e8772-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="e8772-136">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="e8772-136">-ServerName</span></span>
<span data-ttu-id="e8772-137">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="e8772-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="e8772-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e8772-138">-StorageAccountName</span></span>
<span data-ttu-id="e8772-139">Указывает имя учетной записи хранения, которую нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="e8772-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="e8772-140">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="e8772-140">Wildcards are not permitted.</span></span> <span data-ttu-id="e8772-141">Этот параметр не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e8772-141">This parameter is not required.</span></span> <span data-ttu-id="e8772-142">Если этот параметр не указан, командлет будет использовать учетную запись хранения, которая была ранее определена как часть политики обнаружения угроз для базы данных.</span><span class="sxs-lookup"><span data-stu-id="e8772-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="e8772-143">Если определена политика обнаружения угроз базы данных в первый раз и этот параметр не указан, командлет завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="e8772-143">If this is the first time a database threat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="e8772-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8772-144">-Confirm</span></span>
<span data-ttu-id="e8772-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e8772-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8772-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8772-146">-WhatIf</span></span>
<span data-ttu-id="e8772-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e8772-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8772-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e8772-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8772-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8772-149">CommonParameters</span></span>
<span data-ttu-id="e8772-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8772-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8772-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8772-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8772-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8772-152">INPUTS</span></span>

###  
<span data-ttu-id="e8772-153">Вы не можете передавать входные данные в этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e8772-153">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="e8772-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8772-154">OUTPUTS</span></span>

### <span data-ttu-id="e8772-155">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="e8772-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="e8772-156">Этот командлет возвращает объект **model. DatabaseThreatDetectionPolicyModel** .</span><span class="sxs-lookup"><span data-stu-id="e8772-156">This cmdlet returns a **Model.DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="e8772-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8772-157">NOTES</span></span>

## <span data-ttu-id="e8772-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8772-158">RELATED LINKS</span></span>

[<span data-ttu-id="e8772-159">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e8772-159">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="e8772-160">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e8772-160">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="e8772-161">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="e8772-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

