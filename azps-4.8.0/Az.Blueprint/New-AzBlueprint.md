---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
ms.openlocfilehash: 790a74ef5a296dbc90e9c1db16678b8c1bacf071
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078478"
---
# New-AzBlueprint

## КРАТКИй обзор
Создание нового определения чертежа и сохранение его в указанной подписке или группе управления.

## Максимальное

### CreateBlueprintBySubscription (по умолчанию)
```
New-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateBlueprintByManagementGroup
```
New-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Создание нового определения чертежа. 

## ИЛЛЮСТРИРУЮТ

### Пример 1
```powershell
PS C:\> New-AzBlueprint -Name MyNewBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -BlueprintFile C:\Blueprint.json

Name              : SimpleBlueprint
Id                : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint
ManagementGroupId : myManagementGroupId
Versions          : 
Description       : test
TimeCreated       : 2019-05-12
TargetScope       : Subscription
Parameters        : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue}
ResourceGroups    : {AppNetworkRG}
```

Создание нового определения чертежа в рамках указанной подписки.

## ПАРАМЕТРЫ

### -BlueprintFile
Путь к JSON-файлу, который планируется на диске.

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

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

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

### -ManagementGroupId
Идентификатор группы управления, в которой должно быть сохранено определение.

```yaml
Type: System.String
Parameter Sets: CreateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
Имя определения чертежа.

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

### -SubscriptionId
Идентификатор подписки, в которой должно быть сохранено определение.

```yaml
Type: System.String
Parameter Sets: CreateBlueprintBySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

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

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. чертеж. Models. PSBlueprint

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
