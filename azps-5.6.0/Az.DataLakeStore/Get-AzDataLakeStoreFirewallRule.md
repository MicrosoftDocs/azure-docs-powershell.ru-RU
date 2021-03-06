---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 580b5518e1fc0894a51920e781464258bef9e9cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966664"
---
# Get-AzDataLakeStoreFirewallRule

## SYNOPSIS
Получает указанные правила брандмауэра в указанном магазине data Lake Store.
Если правило брандмауэра не задано, будут перечислены все правила брандмауэра для учетной записи.

## СИНТАКСИС

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Этот Get-AzDataLakeStoreFirewallRule получает указанные правила брандмауэра в указанном магазине.
Если правило брандмауэра не задано, будут перечислены все правила брандмауэра для учетной записи.

## ПРИМЕРЫ

### Пример 1. Извлечение определенного правила брандмауэра
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

Возвращает правило брандмауэра MyFirewallRule из учетной записи ContosoADL.

### Пример 2. Список всех правил брандмауэра в учетной записи
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

Возвращает все правила брандмауэра в учетной записи ContosoADL.

## PARAMETERS

### -Account
Учетная запись Магазина данных для получения правила брандмауэра.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Имя правила брандмауэра, которое нужно восстановить

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов, для которой нужно получить указанное правило брандмауэра указанной учетной записи.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
