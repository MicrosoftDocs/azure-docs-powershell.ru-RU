---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Restore-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: c12241457b78d9020e447b6f464d5623e90d52b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568701"
---
# Restore-AzureRmRecoveryServicesBackupItem

## КРАТКИй обзор
Восстанавливает данные и конфигурацию элемента резервного копирования в точку восстановления.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Restore-AzureRmRecoveryServicesBackupItem [-RecoveryPoint] <RecoveryPointBase> [-StorageAccountName] <String>
 [-StorageAccountResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **RESTORE-AzureRmRecoveryServicesBackupItem** восстанавливает данные и конфигурацию элемента резервного копирования Azure для указанной точки восстановления.
Этот командлет запускает восстановление из хранилища служб восстановления на учетную запись хранения клиента.

Операция восстановления не восстанавливает полную виртуальную машину.
Она восстанавливает данные о дисках и сведения о конфигурации.
После завершения операции восстановления необходимо создать виртуальную машину и запустить ее.

Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Восстановление элемента в точке восстановления
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() 
PS C:\> $RestoreJob = Restore-AzureRmRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG"
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

Первая команда получает контейнер резервного копирования типа AzureVM и сохраняет его в переменной $Container.

Вторая команда получает элемент резервного копирования с именем V2VM from $Container и сохраняет его в переменной $BackupItem.

Третья команда получает дату из семи дней раньше и сохраняет ее в переменной $StartDate.

Четвертая команда получает текущую дату, а затем сохраняет ее в переменной $EndDate.

Пятая команда возвращает список точек восстановления для определенного элемента резервного копирования, отфильтрованного по $StartDate и $EndDate.
Указанный диапазон дат — последние 7 дней.

Последняя команда восстанавливает диски на целевую учетную запись хранения DestAccount в группе ресурсов DestRG.

## ПАРАМЕТРЫ

### -RecoveryPoint
Указывает точку восстановления, в которую нужно восстановить виртуальную машину.
Чтобы получить объект **AzureRmRecoveryServicesBackupRecoveryPoint** , используйте командлет Get-AzureRmRecoveryServicesBackupRecoveryPoint.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StorageAccountName
Указывает имя целевой учетной записи хранения в подписке.
В ходе процесса восстановления этот командлет сохраняет диски и сведения о конфигурации в этой учетной записи хранения.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountResourceGroupName
Указывает имя группы ресурсов, которая содержит целевую учетную запись хранилища в вашей подписке.
В ходе процесса восстановления этот командлет сохраняет диски и сведения о конфигурации в этой учетной записи хранения.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
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

### RecoveryPointBase
Параметр "RecoveryPoint" принимает значение типа "RecoveryPointBase" из конвейера.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Backup-AzureRmRecoveryServicesBackupItem](./Backup-AzureRmRecoveryServicesBackupItem.md)

[Get-AzureRmRecoveryServicesBackupItem](./Get-AzureRmRecoveryServicesBackupItem.md)

[Get-AzureRmRecoveryServicesBackupRecoveryPoint](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)


