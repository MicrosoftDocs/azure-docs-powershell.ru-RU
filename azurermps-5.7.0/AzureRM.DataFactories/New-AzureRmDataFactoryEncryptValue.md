---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryEncryptValue.md
ms.openlocfilehash: ffdd124658ecaadfdd1772fb03a3e8c40254f698
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565521"
---
# New-AzureRmDataFactoryEncryptValue

## КРАТКИй обзор
Шифрует конфиденциальные данные.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### ByFactoryName (по умолчанию)
```
New-AzureRmDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>]
 [[-GatewayName] <String>] [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
New-AzureRmDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>]
 [[-GatewayName] <String>] [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmDataFactoryEncryptValue** шифрует конфиденциальные данные, такие как пароль или строку подключения Microsoft SQL Server, и возвращает зашифрованное значение.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Шифрование строки соединения, не относящегося к ODBC
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzureRmDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

Первая команда использует командлет ConvertTo-SecureString для преобразования указанной строки подключения в объект **SecureString** и сохраняет этот объект в переменной $value.
Для получения дополнительных сведений введите `Get-Help ConvertTo-SecureString` .
Допустимые значения: строка подключения SQL Server или Oracle.

Вторая команда создает зашифрованное значение для объекта, хранящегося в $Value для указанной фабрики данных, шлюза, группы ресурсов и типа связанной службы.

### Пример 2: Шифрование строки подключения, не относящейся к ODBC, в которой используется проверка подлинности Windows.
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzureRmDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;Integrated Security=True' -AsPlainText -Force
```

Первая команда использует **ConvertTo-SecureString** для преобразования указанной строки подключения в безопасный строковый объект, а затем сохраняет этот объект в переменной $value.

Вторая команда использует командлет Get-Credential для сбора проверки подлинности Windows (имя пользователя и пароль), а затем сохраняет этот объект **PSCredential** в переменной $Credential.
Для получения дополнительных сведений введите `Get-Help Get-Credential` .

Третья команда создает зашифрованное значение для объекта, хранящегося в $Value и $Credential для указанной фабрики данных, шлюза, группы ресурсов и типа связанной службы.

### Пример 3: шифрование имени сервера и учетных данных для связанной службы файловой системы
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzureRmDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

Первая команда использует **ConvertTo-SecureString** для преобразования указанной строки в безопасную строку, а затем сохраняет этот объект в переменной $value.

Вторая команда использует **Get-credentials** для сбора данных проверки подлинности Windows (имя пользователя и пароль), а затем сохраняет этот объект **PSCredential** в переменной $Credential.

Третья команда создает зашифрованное значение для объекта, хранящегося в $Value и $Credential для указанной фабрики данных, шлюза, группы ресурсов и типа связанной службы.

### Пример 4: Шифрование учетных данных для связанной службы HDFS
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzureRmDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

Команда **ConvertTo-SecureString** преобразует указанную строку в безопасную строку.
Команда **New-Object** создает объект PSCredential с помощью защищенного имени пользователя и строки пароля.
Вместо этого вы можете использовать команду **Get-Credential** для сбора данных проверки подлинности Windows (имя пользователя и пароль), а затем сохранить возвращенный объект **PSCredential** в переменной $credential, как показано в предыдущих примерах.

Команда **New-AzureRmDataFactoryEncryptValue** создает зашифрованное значение для объекта, хранящегося в $Credential для указанной фабрики данных, шлюза, группы ресурсов и типа связанной службы.

### Пример 5: Шифрование учетных данных для связанной службы ODBC
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzureRmDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

Команда **ConvertTo-SecureString** преобразует указанную строку в безопасную строку.

Команда **New-AzureRmDataFactoryEncryptValue** создает зашифрованное значение для объекта, хранящегося в $value для указанной фабрики данных, шлюза, группы ресурсов и типа связанной службы.

## ПАРАМЕТРЫ

### -AuthenticationType
Указывает тип проверки подлинности, который будет использоваться для подключения к источнику данных.
Для этого параметра допустимы следующие значения:

- Windows
- Базового
- Доступом.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Basic, Anonymous

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
Задает используемые учетные данные проверки подлинности Windows (имя пользователя и пароль).
Этот командлет шифрует данные учетных данных, которые вы указали здесь.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -База данных
Указывает имя базы данных связанной службы.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Фактическое.
Указывает объект **PSDataFactory** .
Этот командлет шифрует данные для фабрики данных, которую указывает этот параметр.

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Указывает имя фабрики данных.
Этот командлет шифрует данные для фабрики данных, которую указывает этот параметр.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### -GatewayName
Указывает имя шлюза.
Этот командлет шифрует данные для шлюза, который указывает этот параметр.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NonCredentialValue
Указывает часть, которая не является учетной записью, в строке соединения ODBC (Open Database Connectivity).
Этот параметр применим только для связанной службы ODBC.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов Azure.
Этот командлет шифрует данные для группы, которую указывает этот параметр.

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Сервер
Указывает имя сервера связанной службы.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type (тип)
Указывает тип связанной службы.
Этот командлет шифрует данные для типа связанной службы, который указывает этот параметр.
Для этого параметра допустимы следующие значения:

- OnPremisesSqlLinkedService 
- OnPremisesFileSystemLinkedService 
- OnPremisesOracleLinkedService 
- OnPremisesOdbcLinkedService 
- OnPremisesPostgreSqlLinkedService 
- OnPremisesTeradataLinkedService 
- OnPremisesMySQLLinkedService 
- OnPremisesDB2LinkedService 
- OnPremisesSybaseLinkedService

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OnPremisesSqlLinkedService, OnPremisesFileSystemLinkedService, OnPremisesOracleLinkedService, OnPremisesOdbcLinkedService, OnPremisesPostgreSqlLinkedService, OnPremisesTeradataLinkedService, OnPremisesMySQLLinkedService, OnPremisesDB2LinkedService, OnPremisesSybaseLinkedService, HdfsLinkedService

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value (значение)
Задает значение, которое нужно зашифровать.
Для локальной связанной службы SQL Server и локальной связанной службы Oracle используйте строку подключения.
Для локальной связанной службы ODBC используйте часть учетных данных в строке подключения.
В локальной файловой системе, связанной со службой, если файловая система является локальной для компьютера-шлюза, используйте Local или localhost и, если файловая система находится на сервере, отличном от компьютера шлюза, используйте \\ \\ ServerName.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### System. String

## Пуск
* Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmDataFactoryEncryptValue](./New-AzureRmDataFactoryEncryptValue.md)


