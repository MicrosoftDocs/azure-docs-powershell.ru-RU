---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 658a242b724c57092bd155be69743f2080c07732
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507750"
---
# <span data-ttu-id="eeb40-101">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="eeb40-101">Set-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="eeb40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eeb40-102">SYNOPSIS</span></span>
<span data-ttu-id="eeb40-103">Задает параметры vpn ipsec для существующего виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="eeb40-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

## <span data-ttu-id="eeb40-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eeb40-104">SYNTAX</span></span>

### <span data-ttu-id="eeb40-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eeb40-105">ByFactoryName (Default)</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeb40-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="eeb40-106">ByFactoryObject</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeb40-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="eeb40-107">ByResourceId</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eeb40-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eeb40-108">DESCRIPTION</span></span>
<span data-ttu-id="eeb40-109">Cmdlet **Set-AzVpnClientIpsecParameter** задает параметры vpn ipsec для существующего виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="eeb40-109">The **Set-AzVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="eeb40-110">Когда создается виртуальный сетевой шлюз, он устанавливает для шлюза набор стандартных политик VPN IPSEC.</span><span class="sxs-lookup"><span data-stu-id="eeb40-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="eeb40-111">Если пользователь на сайте хочет использовать настраиваемую политику ipsec для подключения к VPN-шлюзу, сначала необходимо настроить эту политику ipsec на VPN Gateway.</span><span class="sxs-lookup"><span data-stu-id="eeb40-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="eeb40-112">**Set-AzVpnClientIpsecParameter** позволяет это сделать.</span><span class="sxs-lookup"><span data-stu-id="eeb40-112">**Set-AzVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="eeb40-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eeb40-113">EXAMPLES</span></span>

### <span data-ttu-id="eeb40-114">Пример 1. Настраиваемая политика ipsec VPN для существующего виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="eeb40-114">Example 1: Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="eeb40-115">В этом примере настраиваемая политика ipsec VPN настраивается для существующего виртуального сетевого шлюза ContosoVirtualGateway из группы ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="eeb40-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="eeb40-116">New-AzVpnClientIpsecParameter используется для создания объекта параметров VPN ipsec, в котором используются значения, которые пользователь может установить для существующего виртуального сетевого шлюза в resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="eeb40-116">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="eeb40-117">Созданный объект VpnClientIPsecParameters передается команде Set-AzVpnClientIpsecParameter для настройки настраиваемой политики Vpn ipsec на виртуальном сетевом шлюзе, как показано в примере выше.</span><span class="sxs-lookup"><span data-stu-id="eeb40-117">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="eeb40-118">Эта команда возвращает объект VpnClientIPsecParameters, отображая параметры набора.</span><span class="sxs-lookup"><span data-stu-id="eeb40-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="eeb40-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eeb40-119">PARAMETERS</span></span>

### <span data-ttu-id="eeb40-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeb40-120">-DefaultProfile</span></span>
<span data-ttu-id="eeb40-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eeb40-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eeb40-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eeb40-122">-InputObject</span></span>
<span data-ttu-id="eeb40-123">Объект виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="eeb40-123">The virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb40-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeb40-124">-ResourceGroupName</span></span>
<span data-ttu-id="eeb40-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eeb40-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb40-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eeb40-126">-ResourceId</span></span>
<span data-ttu-id="eeb40-127">ИД ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="eeb40-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb40-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="eeb40-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="eeb40-129">Имя виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="eeb40-129">The virtual network gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb40-130">-VpnClientIPsecParameter</span><span class="sxs-lookup"><span data-stu-id="eeb40-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="eeb40-131">Параметры ipsec клиента Vpn.</span><span class="sxs-lookup"><span data-stu-id="eeb40-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="eeb40-132">Это значение параметра можно построить с помощью команды PS let:New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="eeb40-132">This parameter value can be constructed using PS command let:New-AzVpnClientIpsecParameter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb40-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eeb40-133">-Confirm</span></span>
<span data-ttu-id="eeb40-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeb40-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeb40-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeb40-135">-WhatIf</span></span>
<span data-ttu-id="eeb40-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeb40-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eeb40-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="eeb40-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeb40-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeb40-138">CommonParameters</span></span>
<span data-ttu-id="eeb40-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeb40-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeb40-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeb40-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeb40-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eeb40-141">INPUTS</span></span>

### <span data-ttu-id="eeb40-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="eeb40-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

### <span data-ttu-id="eeb40-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="eeb40-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="eeb40-144">System.String</span><span class="sxs-lookup"><span data-stu-id="eeb40-144">System.String</span></span>

## <span data-ttu-id="eeb40-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eeb40-145">OUTPUTS</span></span>

### <span data-ttu-id="eeb40-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="eeb40-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="eeb40-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eeb40-147">NOTES</span></span>

## <span data-ttu-id="eeb40-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eeb40-148">RELATED LINKS</span></span>

[<span data-ttu-id="eeb40-149">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="eeb40-149">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="eeb40-150">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="eeb40-150">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="eeb40-151">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="eeb40-151">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)