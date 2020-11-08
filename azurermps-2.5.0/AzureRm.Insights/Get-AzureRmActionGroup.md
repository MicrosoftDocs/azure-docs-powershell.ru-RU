---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: 7a881b6479561ac7a616158c8054bff592209289
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915313"
---
# Get-AzureRmActionGroup

## КРАТКИй обзор
Получает группу действий.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### BySubscriptionOrResourceGroup (по умолчанию)
```
Get-AzureRmActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByName
```
Get-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmActionGroup** получает одну или несколько групп действий.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение группы действий по коду подписки
```
PS C:\>Get-AzureRmActionGroup
```

Эта команда выводит список всех групп действий для текущей подписки.

### Пример 2: получение групп действий для указанной группы ресурсов
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts"
```

Эта команда перечисляет группы действий для указанной группы ресурсов.

### Пример 3: получение группы действий.
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

Эта команда перечисляет один (список с одной группой действий).

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### -Name (имя)
Имя группы действий.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)