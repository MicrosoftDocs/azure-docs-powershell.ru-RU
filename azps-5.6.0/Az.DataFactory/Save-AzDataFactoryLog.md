---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: eb2e3c9acd93e8b20c7bdf6f4ee04ef2910a3cbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006968"
---
# Save-AzDataFactoryLog

## SYNOPSIS
Скачивает файлы журнала из обработки Azure HDInsight.

## СИНТАКСИС

### ByFactoryName (По умолчанию)
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
С **помощью cmdlet Save-AzDataFactoryLog** можно скачивать файлы журналов, связанные с обработкой проектов Порося или Свина (Azure HDInsight) или настраиваемых действий на локальный жесткий диск.
Сначала запустите Get-AzDataFactoryRun-файл, чтобы получить код действия, которое будет выполниться для среза данных, а затем используйте его для извлечения файлов журнала из хранилища двоичных больших объектов (BLOB-объектов), связанного с кластером HDInsight.
Если не указать параметр *DownloadLogs,* будет возвращено расположение файлов журнала.
Если задать *параметр DownloadLogs,* не указав выходной каталог *(выходной* параметр), файлы журнала загружаются в папку "Документы" по умолчанию.
Если вы *указали DownloadLogs* вместе с выходной папкой *(Output),* файлы журнала загружаются в указанную папку.

## ПРИМЕРЫ

### Пример 1. Сохранение файлов журнала в определенную папку
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

Эта команда сохраняет файлы журнала для действия, которое будет выполниться с помощью ИД 841b77c9-d56c-48d1-99a3-8c16c3e77d39, действие принадлежит конвейеру в фабрике данных LogProcessingFactory в группе ресурсов ADF.
Файлы журнала сохраняются в папку C:\Test.

### Пример 2. Сохранение файлов журнала в папку "Документы" по умолчанию
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

Эта команда сохраняет файлы журнала в папку "Документы" (по умолчанию).

### Пример 3. Просмотр расположения файлов журнала
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

Эта команда возвращает расположение файлов журнала.
Обратите *внимание, что downloadLogs* не указан.

## PARAMETERS

### -DataFactory
Указывает объект **PSDataFactory.**

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Название фабрики данных.
Этот cmdlet скачивает файлы журнала для фабрики данных, указанной этим параметром.

```yaml
Type: System.String
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DownloadLogs
Указывает на то, что этот cmdlet скачивает файлы журнала на локальный компьютер.
Если *папка* вывода не указана, файлы сохраняются в папке "Документы" во вложенной папке.

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

### -Id
Определяет ИД действия, запускаемого для среза данных.
Чтобы получить Get-AzDataFactoryRun, воспользуйтесь этим Get-AzDataFactoryRun.

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

### -Output
Определяет выходную папку, в которой сохраняются загруженные файлы журнала.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов Azure.
Этот cmdlet создает фабрику данных, которая принадлежит к группе, указанной этим параметром.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo

## ПРИМЕЧАНИЯ
* Ключевые слова: azure, azurerm, arm, resource, management, manager, data, factories

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzDataFactoryRun](./Get-AzDataFactoryRun.md)

[Get-AzDataFactoryPipeline](./Get-AzDataFactoryPipeline.md)

[New-AzDataFactoryPipeline](./New-AzDataFactoryPipeline.md)

[Remove-AzDataFactoryPipeline](./Remove-AzDataFactoryPipeline.md)

[Set-AzDataFactoryPipelineActivePeriod](./Set-AzDataFactoryPipelineActivePeriod.md)

[Suspend-AzDataFactoryPipeline](./Suspend-AzDataFactoryPipeline.md)


