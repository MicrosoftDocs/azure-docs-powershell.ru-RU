---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/resize-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 0a8a5c4084813bac74ea907575d2bd26c3d8c5f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568444"
---
# Resize-AzureRmVirtualNetworkGateway

## КРАТКИй обзор
Изменение размера существующего шлюза виртуальной сети.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **resize-AzureRmVirtualNetworkGateway** позволяет изменить единицу хранения (SKU) для шлюза виртуальной сети.
SKU определяет возможности шлюза, включая такие аспекты, как пропускная способность и максимальное количество разрешенных IP-туннелей.
Azure поддерживает базовые, стандартные, высокопроизводительные, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ и ErGw2AZ, ErGw3AZ SKU (иногда называются небольшим, средним и крупными SKU).
Подробные сведения о возможностях каждого типа SKU можно найти в разделе https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .
Имейте в виду, что номера SKU отличаются в ценах и возможностях.
Дополнительные сведения можно найти в разделе https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .

## ИЛЛЮСТРИРУЮТ

### Пример 1: изменение размера шлюза виртуальной сети
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

В этом примере изменяется размер шлюза виртуальной сети с именем ContosoVirtualGateway.
Первая команда создает ссылку на объект в ContosoVirtualGateway; Эта ссылка на объект хранится в переменной с именем $Gateway.
Вторая команда использует командлет **resize-AzureRmVirtualNetworkGateway** , чтобы присвоить свойству *GatewaySku* значение Basic.

## ПАРАМЕТРЫ

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

### -GatewaySku
Указывает новый тип SKU шлюза.
Для этого параметра допустимы следующие значения:
- Базового
- Стандартная
- Высокая производительность
- VpnGw1
- VpnGw2
- VpnGw3
- VpnGw1AZ 
- VpnGw2AZ 
- VpnGw3AZ 
- ErGw1AZ 
- ErGw2AZ 
- ErGw3AZ 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Указывает ссылку на объект для изменения шлюза виртуальной сети.
Вы можете создать ссылку на объект, используя Get-AzureRmVirtualNetworkGateway и указав имя шлюза.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway
Параметры: VirtualNetworkGateway (ByValue)

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway

## Пуск
В новой конфигурации VpnGw1/VpnGw2/VpnGw3 SKU нельзя изменить размер из базовой/стандартной/HighPerformance SKU. Дальнейшее изменение размера не разрешено для VpnGw1AZ/VpnGw2AZ/VpnGw3AZ или ErGw1AZ/ErGw2AZ/ErGw3AZ. Изменение размера разрешено только в пределах номера SKU, например, VpnGw1AZ можно изменить до и из VpnGw2AZ/VpnGw3AZ и ErGw1AZ можно изменить до/с ErGw2AZ или ErGw3AZ. Для получения инструкций ознакомьтесь с https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways инструкциями.

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmVpnClientPackage](./Get-AzureRmVpnClientPackage.md)

[Get-AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[Set-AzureRmVirtualNetworkGatewayVpnClientConfig](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


