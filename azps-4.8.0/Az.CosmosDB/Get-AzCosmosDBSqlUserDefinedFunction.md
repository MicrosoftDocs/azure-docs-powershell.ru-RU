---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: b2f6e203b1ef8f14623df2910b853ea6f3841f72
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242873"
---
# Get-AzCosmosDBSqlUserDefinedFunction

## КРАТКИй обзор
Возвращает пользовательскую функцию SQL CosmosDB, определяемую пользователем.

## Максимальное

### ByNameParameterSet
```
Get-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByParentObjectParameterSet
```
Get-AzCosmosDBSqlUserDefinedFunction [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzCosmosDBSqlUserDefinedFunction** получает список всех существующих CosmosDB SQL UserDefinedFunctions для указанных ResourceGroupName, имя_учетной_записи, DatabaseName и ContainerName и возвращает один CosmosDB SQL UserDefinedFunction для данного ResourceGroupName, имя_учетной_записи, DatabaseName, ContainerName и UserDefinedFunctionName.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```powershell
PS C:\> Get-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {userDefinedFunctionName} -ContainerName {containerName} 

Name                               : {userDefinedFunctionName}
Id                                 : {userDefinedFunctionId}
Resource                           : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetPropertiesResource
```

## ПАРАМЕТРЫ

### -Имя_учетной_записи
Имя учетной записи базы данных Cosmos DB.

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContainerName
Имя контейнера.

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
Имя базы данных.

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
Имя пользовательской функции.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentObject
Объект контейнера SQL.

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUserDefinedFunctionGetResults

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
