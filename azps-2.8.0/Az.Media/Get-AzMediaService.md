---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: a6d1ff6d169fab90fa866e94577ce9b3f9580a4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720379"
---
# Get-AzMediaService

## КРАТКИй обзор
Получение сведений о службе мультимедиа.

## Максимальное

### ResourceGroupParameterSet
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### AccountNameParameterSet
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzMediaService** получает сведения о службе мультимедиа.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение всех служб мультимедиа в группе ресурсов
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

Эта команда получает свойства для всех служб мультимедиа в группе ресурсов с именем ResourceGroup001.

### Пример 2: получение свойств службы мультимедиа
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

Эта команда получает свойства службы мультимедиа с именем MediaService1, которая относится к группе ресурсов с именем ResourceGroup002.

## ПАРАМЕТРЫ

### -Имя_учетной_записи
Указывает имя службы мультимедиа, которую получает этот командлет.

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
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

### -ResourceGroupName
Указывает имя группы ресурсов, в которой находится служба мультимедиа.

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

### Microsoft. Azure. Commands. Media. Models. PSMediaService

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzMediaService](./New-AzMediaService.md)

[Remove-AzMediaService](./Remove-AzMediaService.md)

[Set-AzMediaService](./Set-AzMediaService.md)


