---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8BAA6D8C-1530-4CC4-8AE5-A2CE6B1192CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobSchedule.md
ms.openlocfilehash: a90f437bc593e1abcb6dc2d92292e04dd9c9f74b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94077304"
---
# Get-AzBatchJobSchedule

## КРАТКИй обзор
Получает расписания пакетных заданий.

## Максимальное

### ODataFilter (по умолчанию)
```
Get-AzBatchJobSchedule [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Номер
```
Get-AzBatchJobSchedule [[-Id] <String>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzBatchJobSchedule** получает расписания пакетных заданий Azure для учетной записи пакетной службы, указанной параметром *BatchContext* .
Укажите идентификатор для получения одного расписания задания.
Укажите параметр *фильтра* для получения расписаний заданий, соответствующих фильтру протокола OData (Open Data Protocol).

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение расписания задания с указанием идентификатора
```
PS C:\>Get-AzBatchJobSchedule -Id "JobSchedule23" -BatchContext $Context
CreationTime                : 7/25/2015 9:15:43 PM
DisplayName                 : 
ETag                        : 0x8D2953633427FCA
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule23
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/25/2015 9:15:43 PM
Metadata                    : 
PreviousState               : Invalid
PreviousStateTransitionTime : 
Schedule                    : 
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:43 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule23
```

Эта команда получает расписание задания с ИДЕНТИФИКАТОРом JobSchedule23.
Используйте командлет Get-AzBatchAccountKey для присвоения контекста переменной $Context.

### Пример 2: получение расписаний заданий с помощью фильтра
```
PS C:\>Get-AzBatchJobSchedule -Filter "startswith(id,'Job')" -BatchContext $Context
CreationTime                : 7/25/2015 9:15:43 PM
DisplayName                 : 
ETag                        : 0x8D2953633427FCA
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule23
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/25/2015 9:15:43 PM
Metadata                    : 
PreviousState               : Invalid
PreviousStateTransitionTime : 
Schedule                    : 
State                       : Active
StateTransitionTime         : 7/25/2015 9:15:43 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule23

CreationTime                : 7/26/2015 5:39:33 PM
DisplayName                 : 
ETag                        : 0x8D295E12B1084B4
ExecutionInformation        : Microsoft.Azure.Commands.Batch.Models.PSJobScheduleExecutionInformation
Id                          : JobSchedule26
JobSpecification            : Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
LastModified                : 7/26/2015 5:39:33 PM
Metadata                    : 
PreviousState               : Invalid
PreviousStateTransitionTime : 
Schedule                    : 
State                       : Active
StateTransitionTime         : 7/26/2015 5:39:33 PM
Statistics                  : 
Url                         : https://pfuller.westus.batch.azure.com/jobschedules/JobSchedule26
```

Эта команда получает все расписания заданий с идентификаторами, которые начинаются с задания, указав параметр *фильтра* .

## ПАРАМЕТРЫ

### -BatchContext
Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.
Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой. Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа. При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа. Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -Expand
Указывает предложение развертывания протокола Open Data Protocol (OData).
Укажите значение этого параметра, чтобы получить связанные сущности от основной сущности, которые вы получаете.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Фильтр
Задает предложение фильтра OData.
Этот командлет возвращает расписания заданий, соответствующие фильтру, указанному в этом параметре.
Если фильтр не указан, этот командлет возвращает все расписания заданий для контекста пакета.

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Указывает идентификатор расписания задания, который получает этот командлет.
Подстановочные знаки указывать нельзя.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -MaxCount
Задает максимальное количество возвращаемых расписаний задач.
Если вы задаете нулевое значение (0) или меньше, в командлете не используется верхний предел.
Значение по умолчанию — 1000.

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SELECT
Задает предложение SELECT OData.
Укажите значение этого параметра, чтобы получить конкретные свойства, а не все свойства объекта.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

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

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## НАПРЯЖЕНИЕ

### Microsoft.Azure.Commands.BatCH. Models. PSCloudJobSchedule

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Disable-AzBatchJobSchedule](./Disable-AzBatchJobSchedule.md)

[Enable-AzBatchJobSchedule](./Enable-AzBatchJobSchedule.md)

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[New-AzBatchJobSchedule](./New-AzBatchJobSchedule.md)

[Remove-AzBatchJobSchedule](./Remove-AzBatchJobSchedule.md)

[Остановить-AzBatchJobSchedule](./Stop-AzBatchJobSchedule.md)

[Командлеты пакетной службы Azure](/powershell/module/az.batch)


