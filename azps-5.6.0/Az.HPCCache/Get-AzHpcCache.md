---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/get-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
ms.openlocfilehash: c88e7d2b930eb7d04760f963a5ab8ea60ab8d455
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012099"
---
# Get-AzHpcCache

## SYNOPSIS
Кэш.

## СИНТАКСИС

```
Get-AzHpcCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Для **кэша** в определенной группе ресурсов или списка кэшов с подпиской можно получить один кэш, кэш или кэш для подписки.

## ПРИМЕРЫ

### Пример 1
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest -CacheName cachetest
```

### Пример 2
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest
```

### Пример 3
```powershell
PS C:\> Get-AzHPCCache
```

## PARAMETERS

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

### -Name
Имя определенного кэша.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов, в которую вы хотите вычесть кэш.

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

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ
