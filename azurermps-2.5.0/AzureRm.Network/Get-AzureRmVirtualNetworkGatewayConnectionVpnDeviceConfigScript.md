---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
ms.openlocfilehash: 0565956d7f40a633bc1aa2c2049ef9a7d764d77e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914430"
---
# Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript

## КРАТКИй обзор
Этот unifiedgroup берет на себя ресурс подключения, марку VPN-устройства, модель, версию микропрограммы и возвращает соответствующий сценарий конфигурации, который пользователи могут применять непосредственно на локальных виртуальных устройствах VPN. Сценарий будет следовать синтаксису выбранного устройства и заполнить необходимые параметры, такие как общедоступные IP-адреса шлюза Azure, префиксы виртуальных сетевых адресов, предварительный ключ VPN-туннеля и т. д., чтобы пользователи могли просто копировать и вставлять их в конфигурации VPN-устройств.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Этот unifiedgroup берет на себя ресурс подключения, марку VPN-устройства, модель, версию микропрограммы и возвращает соответствующий сценарий конфигурации, который пользователи могут применять непосредственно на локальных виртуальных устройствах VPN. Сценарий будет следовать синтаксису выбранного устройства и заполнить необходимые параметры, такие как общедоступные IP-адреса шлюза Azure, префиксы виртуальных сетевых адресов, предварительный ключ VPN-туннеля и т. д., чтобы пользователи могли просто копировать и вставлять их в конфигурации VPN-устройств.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

В приведенном выше примере Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice используется для получения поддерживаемых торговых марок, моделей и версий микропрограмм для устройств VPN.
Затем использует одну из данных возвращенных моделей для создания сценария конфигурации устройства VPN для VirtualNetworkGatewayConnection "TestConnection". Устройство, используемое в этом примере, имеет DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" и FirmwareVersion 20.

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceFamily
Имя модели или семейства VPN-устройств.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DeviceVendor
Имя поставщика VPN-устройства.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FirmwareVersion
Версия встроенного по устройства VPN.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
Название ресурса соединения, для которого необходимо создать конфигурацию.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### System. String

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

