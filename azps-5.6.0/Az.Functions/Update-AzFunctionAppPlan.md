---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: 522de6721d92b76938843b28322b94b5cc6ce481
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963043"
---
# Update-AzFunctionAppPlan

## SYNOPSIS
Обновляет план обслуживания приложения для функций.

## СИНТАКСИС

### ByName (по умолчанию)
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## ОПИСАНИЕ
Обновляет план обслуживания приложения для функций.

## ПРИМЕРЫ

### Пример 1. Обновив план обслуживания приложений до 2 SKU для двадцати максимально допустимых сотрудников.
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

Эта команда обновляет план обслуживания приложений до SKU EP2 для двадцати максимально допустимых сотрудников.

## PARAMETERS

### -AsJob
Выполнить команду как задание.

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

### -DefaultProfile


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaximumWorkerCount
Максимальное количество сотрудников для плана обслуживания приложений.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinimumWorkerCount
Минимальное количество сотрудников для плана обслуживания приложений.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Имя плана службы приложений.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Запустите команду асинхронно.

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

### -ResourceGroupName
Имя группы ресурсов, к которой принадлежит ресурс.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKU
SKU плана.
Допустимые входные данные: EP1, EP2, EP3

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

### -SubscriptionId
ИД подписки Azure.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Теги ресурсов.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Запрос на подтверждение перед запуском cmdlet.

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
Показывает, что произойдет при запуске cmdlet.
Этот cmdlet не будет выполниться.

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


<IAppServicePlan>INPUTOBJECT: 
  - `Location <String>`: Расположение ресурса.
  - `[Kind <String>]`: Тип ресурса.
  - `[Tag <IResourceTags>]`: теги ресурсов.
    - `[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.
  - `[Capacity <Int32?>]`: Текущее количество экземпляров, которые назначены ресурсу.
  - `[FreeOfferExpirationTime <DateTime?>]`. Время истечения срока действия бесплатного предложения фермы серверов.
  - `[HostingEnvironmentProfileId <String>]`: ИД ресурса среды служб приложений.
  - `[HyperV <Boolean?>]`. Если Hyper-V план обслуживания контейнера <code>true</code> приложения, <code>false</code> в противном случае.
  - `[IsSpot <Boolean?>]`. Если этот план служб приложения принадлежит spot <code>true</code> экземплярам.
  - `[IsXenon <Boolean?>]`: Устарело: если Hyper-V план обслуживания контейнера <code>true</code> приложения, <code>false</code> в противном случае.
  - `[MaximumElasticWorkerCount <Int32?>]`: Максимальное количество сотрудников, разрешенных для этого плана обслуживания приложения ВадимScaleEnabled
  - `[PerSiteScaling <Boolean?>]`. Если приложения, которые назначены этому плану обслуживания приложений, <code>true</code> можно масштабировать независимо друг от друга.         Если приложения, которые назначены этому плану обслуживания приложений, будут масштабироваться во всех <code>false</code> его экземплярах.
  - `[Reserved <Boolean?>]`. Если вы планируете службу приложения <code>true</code> Linux, <code>false</code> в противном случае.
  - `[SkuCapability <ICapability[]>]`. Возможности SKU, например, включен ли диспетчер трафика?
    - `[Name <String>]`: Имя возможности SKU.
    - `[Reason <String>]`: Причина возможности SKU.
    - `[Value <String>]`: значение возможности SKU.
  - `[SkuCapacityDefault <Int32?>]`: Число сотрудников по умолчанию для этого плана обслуживания приложений.
  - `[SkuCapacityMaximum <Int32?>]`: Максимальное количество сотрудников для этого плана обслуживания приложений.
  - `[SkuCapacityMinimum <Int32?>]`: Минимальное количество сотрудников для этого плана обслуживания приложений.
  - `[SkuCapacityScaleType <String>]`: Доступны масштаб конфигурации для плана службы приложений.
  - `[SkuFamily <String>]`: Семейный код SKU ресурса.
  - `[SkuLocation <String[]>]`: Местоположения SKU.
  - `[SkuName <String>]`: Имя SKU ресурса.
  - `[SkuSize <String>]`: Заданный размер SKU ресурса.
  - `[SkuTier <String>]`: уровень обслуживания SKU ресурса.
  - `[SpotExpirationTime <DateTime?>]`Время истечения срока действия фермы серверов. Допустимо только в том случае, если это ферма точественных серверов.
  - `[TargetWorkerCount <Int32?>]`: количество масштабируемых сотрудников.
  - `[TargetWorkerSizeId <Int32?>]`: ИД размера масштабируемой работники.
  - `[WorkerTierName <String>]`: уровень целевого сотрудника, который назначен плану службы приложений.

## СВЯЗАННЫЕ ССЫЛКИ

