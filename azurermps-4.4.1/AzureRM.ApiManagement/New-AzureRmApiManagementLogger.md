---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
ms.openlocfilehash: c7827f0df8b1baf4bb2fead9df091619751c969c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565726"
---
# New-AzureRmApiManagementLogger

## КРАТКИй обзор
Создает средство ведения журнала управления API.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmApiManagementLogger** создает **средство ведения журнала** управления API Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание средства ведения журнала
```
PS C:\>New-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

Эта команда создает средство ведения журнала с именем ContosoSdkEventHub, используя указанную строку подключения.

## ПАРАМЕТРЫ

### -ConnectionString
Указывает строку подключения к концентраторам событий Azure, которая начинается со следующего: 

`Endpoint=endpoint and key from Azure classic portal`

Ключ с правами отправки в строке соединения должен быть настроен.

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

### -Context
Указывает объект **PsApiManagementContext** .

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Описание
Задает описание.

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

### -Буферизация
Указывает, буферизуются ли записи в средстве ведения журнала перед публикацией.
Значение по умолчанию — $True.
Когда записи записываются в буфер, они отправляются в концентраторы событий каждые 15 секунд или каждый раз, когда буфер получает 256 КБ сообщений.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoggerId
Указывает идентификатор для средства ведения журнала.
Если идентификатор не указан, этот командлет создаст его.

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

### -Name (имя)
Указывает имя сущности концентратора событий на классическом портале Azure.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmApiManagementLogger](./Get-AzureRmApiManagementLogger.md)

[Remove-AzureRmApiManagementLogger](./Remove-AzureRmApiManagementLogger.md)

[Set-AzureRmApiManagementLogger](./Set-AzureRmApiManagementLogger.md)


