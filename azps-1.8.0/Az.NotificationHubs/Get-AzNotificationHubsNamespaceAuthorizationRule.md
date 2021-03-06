---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 284e283eb05608524e0a746a2b5eeb1769e368a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729906"
---
# Get-AzNotificationHubsNamespaceAuthorizationRule

## КРАТКИй обзор
Получает сведения о правилах авторизации, связанных с пространством имен концентратора уведомлений.

## Максимальное

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzNotificationHubsNamespaceAuthorizationRule** возвращает сведения о правилах авторизации для общих подписей доступа (SAS), связанных с пространством имен концентратора уведомлений.
Вы можете вернуть сведения обо всех правилах, связанных с пространством имен.
Кроме того, с помощью параметра *AuthorizationRule* можно вернуть сведения о конкретном правиле.
Правила авторизации управляют доступом к пространствам имен.
Это делается с помощью создания ссылок в виде URI, основанных на различных уровнях разрешений.
Уровни платформы могут быть одним из следующих: 
- Прослушивающих
- Отправить
- Управление клиентами направляется на один из этих URI на основе соответствующего уровня разрешений.
Например, клиент, которому предоставлено разрешение прослушивания, будет направлен на универсальный код ресурса (URI) для этого разрешения.
Этот командлет получает только те правила авторизации, которые связаны с пространством имен.
Чтобы получить сведения о пространстве имен, используйте Get-AzNotificationHubsNamespace.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение сведений обо всех правилах авторизации, назначенных пространствам имен
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

Эта команда получает сведения обо всех правилах авторизации, назначенных для группы ресурсов Namespace ContosoNamespace и ContosoNotificationsGroup.

### Пример 2: получение сведений о правиле авторизации
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

Эта команда получает сведения о одном правиле авторизации пространства имен с именем ListenRule.
При получении сведений о конкретном правиле авторизации необходимо включать пространство имен и группу ресурсов.

## ПАРАМЕТРЫ

### -AuthorizationRule
Указывает имя правила проверки подлинности SAS.
Эти правила определяют тип доступа пользователей к пространству имен.

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

### -Namespace
Задает пространство имен, которым назначены правила авторизации.
Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.

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

### -ResourceGroup
Указывает группу ресурсов, которой назначены правила авторизации.
Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


