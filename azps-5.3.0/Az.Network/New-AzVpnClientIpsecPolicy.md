---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: 028c33db36df5debb6f951f11e27f0586e7a21dc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421607"
---
# <span data-ttu-id="019e0-101">New-AzVpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="019e0-101">New-AzVpnClientIpsecPolicy</span></span>

## <span data-ttu-id="019e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="019e0-102">SYNOPSIS</span></span>
<span data-ttu-id="019e0-103">Эта команда позволяет пользователям создать объект политики Vpn ipsec, определяющий одно или все значения, такие как IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup, чтобы установить на VPN-шлюзе.</span><span class="sxs-lookup"><span data-stu-id="019e0-103">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="019e0-104">Эта команда, позволяющая вывести объект, используется для того, чтобы настроить политику ipsec VPN для нового и существующего шлюза.</span><span class="sxs-lookup"><span data-stu-id="019e0-104">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="019e0-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="019e0-105">SYNTAX</span></span>

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="019e0-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="019e0-106">DESCRIPTION</span></span>
<span data-ttu-id="019e0-107">Эта команда позволяет пользователям создать объект политики Vpn ipsec, определяющий одно или все значения, такие как IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup, чтобы установить на VPN-шлюзе.</span><span class="sxs-lookup"><span data-stu-id="019e0-107">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="019e0-108">Эта команда, позволяющая вывести объект, используется для того, чтобы настроить политику ipsec VPN для нового и существующего шлюза.</span><span class="sxs-lookup"><span data-stu-id="019e0-108">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="019e0-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="019e0-109">EXAMPLES</span></span>

### <span data-ttu-id="019e0-110">Пример 1. Определение объекта политики VPN ipsec:</span><span class="sxs-lookup"><span data-stu-id="019e0-110">Example 1: Define vpn ipsec policy object:</span></span>
```powershell
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

<span data-ttu-id="019e0-111">Этот командлет используется для создания объекта политики VPN IPSec с использованием одного или всех значений, которые пользователь может передавать в параметры:VpnClientIpsecPolicy ps command let: New-AzVirtualNetworkGateway (создание нового VPN-шлюза) / Set-AzVirtualNetworkGateway (существующее обновление шлюза VPN) в ResourceGroup:</span><span class="sxs-lookup"><span data-stu-id="019e0-111">This cmdlet is used to create the vpn ipsec policy object using the passed one or all parameters' values which user can pass to param:VpnClientIpsecPolicy of PS command let: New-AzVirtualNetworkGateway (New VPN Gateway creation) / Set-AzVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :</span></span>

### <span data-ttu-id="019e0-112">Пример 2. Создание виртуального сетевого шлюза с настройкой настраиваемой политики ipsec vpn:</span><span class="sxs-lookup"><span data-stu-id="019e0-112">Example 2: Create new virtual network gateway with setting vpn custom ipsec policy:</span></span>
```powershell
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="019e0-113">Этот cmdlet возвращает объект виртуального сетевого шлюза после создания.</span><span class="sxs-lookup"><span data-stu-id="019e0-113">This cmdlet returns virtual network gateway object after creation.</span></span> 

### <span data-ttu-id="019e0-114">Пример 3. Настройка настраиваемой политики ipsec vpn для существующего виртуального сетевого шлюза:</span><span class="sxs-lookup"><span data-stu-id="019e0-114">Example 3: Set vpn custom ipsec policy on existing virtual network gateway:</span></span>
```powershell
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="019e0-115">Этот cmdlet возвращает объект виртуального сетевого шлюза после настройки настраиваемой политики IPSEC vpn.</span><span class="sxs-lookup"><span data-stu-id="019e0-115">This cmdlet returns virtual network gateway object after setting vpn custom ipsec policy.</span></span>

### <span data-ttu-id="019e0-116">Пример 4. Установите виртуальный сетевой шлюз, чтобы узнать, правильно ли настроена настраиваемая политика VPN:</span><span class="sxs-lookup"><span data-stu-id="019e0-116">Example 4: Get virtual network gateway to see if vpn custom policy is set correctly:</span></span>
```powershell
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

<span data-ttu-id="019e0-117">Этот cmdlet возвращает объект виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="019e0-117">This cmdlet returns virtual network gateway object.</span></span>

## <span data-ttu-id="019e0-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="019e0-118">PARAMETERS</span></span>

### <span data-ttu-id="019e0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="019e0-119">-DefaultProfile</span></span>
<span data-ttu-id="019e0-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="019e0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="019e0-121">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="019e0-121">-DhGroup</span></span>
<span data-ttu-id="019e0-122">Группы DH VpnClient, используемые в IKE, этапе 1 для первоначального SA</span><span class="sxs-lookup"><span data-stu-id="019e0-122">The VpnClient DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="019e0-123">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="019e0-123">-IkeEncryption</span></span>
<span data-ttu-id="019e0-124">Алгоритм шифрования VPNClient IKE (этап 2)</span><span class="sxs-lookup"><span data-stu-id="019e0-124">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="019e0-125">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="019e0-125">-IkeIntegrity</span></span>
<span data-ttu-id="019e0-126">Алгоритм целостности IKE с vpnClient (этап 2)</span><span class="sxs-lookup"><span data-stu-id="019e0-126">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="019e0-127">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="019e0-127">-IpsecEncryption</span></span>
<span data-ttu-id="019e0-128">Алгоритм шифрования VPNClient IPSec (этап 1 IKE)</span><span class="sxs-lookup"><span data-stu-id="019e0-128">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="019e0-129">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="019e0-129">-IpsecIntegrity</span></span>
<span data-ttu-id="019e0-130">Алгоритм целостности IPSec VpnClient (этап 1 IKE)</span><span class="sxs-lookup"><span data-stu-id="019e0-130">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="019e0-131">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="019e0-131">-PfsGroup</span></span>
<span data-ttu-id="019e0-132">Группы VPNClient PFS, используемые на этапе 2 IKE для нового sa</span><span class="sxs-lookup"><span data-stu-id="019e0-132">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="019e0-133">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="019e0-133">-SADataSize</span></span>
<span data-ttu-id="019e0-134">Размер загрузки VPNClient IPSec (быстрый режим или этап 2 SA) в КБ</span><span class="sxs-lookup"><span data-stu-id="019e0-134">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="019e0-135">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="019e0-135">-SALifeTime</span></span>
<span data-ttu-id="019e0-136">Срок службы Безопасности VpnClient IPSec (экспресс-режим или этап 2 SA) — считанные секунды</span><span class="sxs-lookup"><span data-stu-id="019e0-136">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="019e0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="019e0-137">CommonParameters</span></span>
<span data-ttu-id="019e0-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="019e0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="019e0-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="019e0-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="019e0-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="019e0-140">INPUTS</span></span>

### <span data-ttu-id="019e0-141">Нет</span><span class="sxs-lookup"><span data-stu-id="019e0-141">None</span></span>

## <span data-ttu-id="019e0-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="019e0-142">OUTPUTS</span></span>

### <span data-ttu-id="019e0-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="019e0-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="019e0-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="019e0-144">NOTES</span></span>

## <span data-ttu-id="019e0-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="019e0-145">RELATED LINKS</span></span>