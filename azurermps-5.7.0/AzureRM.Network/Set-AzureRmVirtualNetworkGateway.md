---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 013da22d02f091d49e9780585bb8648c9c895ad7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561692"
---
# <span data-ttu-id="c3edc-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c3edc-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="c3edc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c3edc-102">SYNOPSIS</span></span>
<span data-ttu-id="c3edc-103">Обновление шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="c3edc-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3edc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c3edc-104">SYNTAX</span></span>

### <span data-ttu-id="c3edc-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c3edc-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3edc-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3edc-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3edc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3edc-107">DESCRIPTION</span></span>
<span data-ttu-id="c3edc-108">Командлет **Set-AzureRmVirtualNetworkGateway** обновляет шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="c3edc-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="c3edc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c3edc-109">EXAMPLES</span></span>

### <span data-ttu-id="c3edc-110">Пример 1: Установка состояния цели для шлюза виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="c3edc-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="c3edc-111">Первая команда получает шлюз виртуальной сети с именем Gateway01, принадлежащий группе ресурсов ResourceGroup001 и сохраняет его в переменной с именем $Gateway</span><span class="sxs-lookup"><span data-stu-id="c3edc-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway</span></span>

<span data-ttu-id="c3edc-112">Вторая команда задает состояние цели для шлюза виртуальной сети, сохраненного в переменной $Gateway.</span><span class="sxs-lookup"><span data-stu-id="c3edc-112">The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="c3edc-113">Команда также задает для ASN значение 1337.</span><span class="sxs-lookup"><span data-stu-id="c3edc-113">The command also sets the ASN to 1337.</span></span>

## <span data-ttu-id="c3edc-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c3edc-114">PARAMETERS</span></span>

### <span data-ttu-id="c3edc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3edc-115">-AsJob</span></span>
<span data-ttu-id="c3edc-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c3edc-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3edc-117">-ASN</span><span class="sxs-lookup"><span data-stu-id="c3edc-117">-Asn</span></span>
<span data-ttu-id="c3edc-118">Задает номер автономной системы шлюза виртуальной сети (ASN), который используется для настройки сеансов BGP в туннелях IPsec.</span><span class="sxs-lookup"><span data-stu-id="c3edc-118">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3edc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3edc-119">-DefaultProfile</span></span>
<span data-ttu-id="c3edc-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c3edc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="c3edc-121">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="c3edc-121">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="c3edc-122">Отключение активного активного компонента.</span><span class="sxs-lookup"><span data-stu-id="c3edc-122">Disables the active-active feature.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3edc-123">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="c3edc-123">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="c3edc-124">Включает функцию активный активный компонент.</span><span class="sxs-lookup"><span data-stu-id="c3edc-124">Enables the active-active feature.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3edc-125">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="c3edc-125">-GatewayDefaultSite</span></span>
<span data-ttu-id="c3edc-126">Указывает сайт по умолчанию, который будет использоваться для принудительного туннелирования.</span><span class="sxs-lookup"><span data-stu-id="c3edc-126">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="c3edc-127">Если указан сайт по умолчанию, весь Интернет-трафик от виртуальной частной сети (VPN) шлюза пересылается на этот сайт.</span><span class="sxs-lookup"><span data-stu-id="c3edc-127">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3edc-128">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="c3edc-128">-GatewaySku</span></span>
<span data-ttu-id="c3edc-129">Задает единицу хранения (SKU) шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="c3edc-129">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="c3edc-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c3edc-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c3edc-131">Базового</span><span class="sxs-lookup"><span data-stu-id="c3edc-131">Basic</span></span>
- <span data-ttu-id="c3edc-132">Стандартная</span><span class="sxs-lookup"><span data-stu-id="c3edc-132">Standard</span></span>
- <span data-ttu-id="c3edc-133">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="c3edc-133">HighPerformance</span></span>
- <span data-ttu-id="c3edc-134">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="c3edc-134">VpnGw1</span></span>
- <span data-ttu-id="c3edc-135">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="c3edc-135">VpnGw2</span></span>
- <span data-ttu-id="c3edc-136">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="c3edc-136">VpnGw3</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3edc-137">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="c3edc-137">-PeerWeight</span></span>
<span data-ttu-id="c3edc-138">Указывает вес, добавленный в маршруты, полученные по протоколу BGP из этого шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="c3edc-138">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3edc-139">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="c3edc-139">-RadiusServerAddress</span></span>
<span data-ttu-id="c3edc-140">Адрес внешнего RADIUS-сервера P2S.</span><span class="sxs-lookup"><span data-stu-id="c3edc-140">P2S External Radius server address.</span></span>
```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3edc-141">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="c3edc-141">-RadiusServerSecret</span></span>
<span data-ttu-id="c3edc-142">Секретный P2S внешнего RADIUS-сервера.</span><span class="sxs-lookup"><span data-stu-id="c3edc-142">P2S External Radius server secret.</span></span>
```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3edc-143">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c3edc-143">-VirtualNetworkGateway</span></span>
<span data-ttu-id="c3edc-144">Указывает объект шлюза виртуальной сети, для которого изменяются базовые изменения.</span><span class="sxs-lookup"><span data-stu-id="c3edc-144">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="c3edc-145">Вы можете использовать командлет Get-AzureRmVirtualNetworkGateway, чтобы получить объект шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="c3edc-145">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3edc-146">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="c3edc-146">-VpnClientAddressPool</span></span>
<span data-ttu-id="c3edc-147">Указывает адресное пространство, используемое этим командлетом для выделения IP-адресов VPN-клиентов.</span><span class="sxs-lookup"><span data-stu-id="c3edc-147">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="c3edc-148">Это не должно перекрываться с помощью виртуальной сети или локальных диапазонов.</span><span class="sxs-lookup"><span data-stu-id="c3edc-148">This should not overlap with virtual network or on-premise ranges.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3edc-149">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="c3edc-149">-VpnClientProtocol</span></span>
<span data-ttu-id="c3edc-150">Список туннельных протоколов клиента VPN P2S</span><span class="sxs-lookup"><span data-stu-id="c3edc-150">A list of P2S VPN client tunneling protocols</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 
Accepted values: SSTP, IkeV2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3edc-151">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="c3edc-151">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="c3edc-152">Указывает список отозванных сертификатов VPN-клиентов.</span><span class="sxs-lookup"><span data-stu-id="c3edc-152">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="c3edc-153">VPN-клиент, выступающий сертификат, совпадающий с одним из них, удаляется.</span><span class="sxs-lookup"><span data-stu-id="c3edc-153">A VPN client presenting a certificate that matches one of these is removed.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3edc-154">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="c3edc-154">-VpnClientRootCertificates</span></span>
<span data-ttu-id="c3edc-155">Указывает список корневых сертификатов VPN-клиентов, используемых для проверки подлинности клиента VPN.</span><span class="sxs-lookup"><span data-stu-id="c3edc-155">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="c3edc-156">Подключение VPN-клиентов должно представлять сертификаты, созданные на основе одного из этих корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="c3edc-156">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3edc-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3edc-157">-Confirm</span></span>
<span data-ttu-id="c3edc-158">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c3edc-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3edc-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3edc-159">-WhatIf</span></span>
<span data-ttu-id="c3edc-160">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c3edc-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3edc-161">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c3edc-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3edc-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3edc-162">CommonParameters</span></span>
<span data-ttu-id="c3edc-163">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c3edc-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3edc-164">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3edc-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3edc-165">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c3edc-165">INPUTS</span></span>

### <span data-ttu-id="c3edc-166">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c3edc-166">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="c3edc-167">Параметр "VirtualNetworkGateway" принимает значение типа "PSVirtualNetworkGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c3edc-167">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="c3edc-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3edc-168">OUTPUTS</span></span>

### <span data-ttu-id="c3edc-169">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c3edc-169">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="c3edc-170">Пуск</span><span class="sxs-lookup"><span data-stu-id="c3edc-170">NOTES</span></span>
* <span data-ttu-id="c3edc-171">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="c3edc-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c3edc-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c3edc-172">RELATED LINKS</span></span>

[<span data-ttu-id="c3edc-173">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c3edc-173">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="c3edc-174">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c3edc-174">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="c3edc-175">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c3edc-175">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="c3edc-176">Сброс — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c3edc-176">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="c3edc-177">Изменить размер — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c3edc-177">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

