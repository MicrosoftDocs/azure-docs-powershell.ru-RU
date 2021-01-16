---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
ms.openlocfilehash: 1e13cad885d18d8c15a033ae85b340041107cdc0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519933"
---
# <span data-ttu-id="9060f-101">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9060f-101">Remove-AzVpnGateway</span></span>

## <span data-ttu-id="9060f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9060f-102">SYNOPSIS</span></span>
<span data-ttu-id="9060f-103">С Remove-AzVpnGateway удаляется VPN-шлюз Azure.</span><span class="sxs-lookup"><span data-stu-id="9060f-103">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="9060f-104">Это шлюз, специфичность подключения к программному обеспечению, определяемом программным обеспечением виртуальной WAN Azure.</span><span class="sxs-lookup"><span data-stu-id="9060f-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="9060f-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9060f-105">SYNTAX</span></span>

### <span data-ttu-id="9060f-106">ByVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9060f-106">ByVpnGatewayName (Default)</span></span>
```
Remove-AzVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9060f-107">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="9060f-107">ByVpnGatewayObject</span></span>
```
Remove-AzVpnGateway -InputObject <PSVpnGateway> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9060f-108">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="9060f-108">ByVpnGatewayResourceId</span></span>
```
Remove-AzVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9060f-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9060f-109">DESCRIPTION</span></span>
<span data-ttu-id="9060f-110">С Remove-AzVpnGateway удаляется VPN-шлюз Azure.</span><span class="sxs-lookup"><span data-stu-id="9060f-110">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="9060f-111">Это шлюз, специфичность подключения к программному обеспечению, определяемом программным обеспечением виртуальной WAN Azure.</span><span class="sxs-lookup"><span data-stu-id="9060f-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="9060f-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9060f-112">EXAMPLES</span></span>

### <span data-ttu-id="9060f-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9060f-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Remove-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -Passthru
```

<span data-ttu-id="9060f-114">В этом примере создаются группы ресурсов, виртуальные WAN, виртуальные концентраторы, масштабируемые VPN-шлюзы в центральной части США, а затем сразу удаляются.</span><span class="sxs-lookup"><span data-stu-id="9060f-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="9060f-115">Чтобы скрыть запрос при удалении виртуального шлюза, используйте флаг -Force.</span><span class="sxs-lookup"><span data-stu-id="9060f-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="9060f-116">При этом будут удалены VpnGateway и все подключенные к нему VPNConnections.</span><span class="sxs-lookup"><span data-stu-id="9060f-116">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

### <span data-ttu-id="9060f-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9060f-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" | Remove-AzVpnGateway-Passthru
```

<span data-ttu-id="9060f-118">В этом примере создаются группы ресурсов, виртуальные WAN, виртуальные концентраторы, масштабируемые VPN-шлюзы в центральной части США, а затем сразу удаляются.</span><span class="sxs-lookup"><span data-stu-id="9060f-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="9060f-119">Это удаление происходит с помощью piping powershell, в котором используется объект VpnGateway, Get-AzVpnGateway команды.</span><span class="sxs-lookup"><span data-stu-id="9060f-119">This deletion happens using powershell piping, which uses the VpnGateway object returned by the Get-AzVpnGateway command.</span></span>
<span data-ttu-id="9060f-120">Чтобы скрыть запрос при удалении виртуального шлюза, используйте флаг -Force.</span><span class="sxs-lookup"><span data-stu-id="9060f-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="9060f-121">При этом будут удалены VpnGateway и все подключенные к нему VPNConnections.</span><span class="sxs-lookup"><span data-stu-id="9060f-121">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

## <span data-ttu-id="9060f-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9060f-122">PARAMETERS</span></span>

### <span data-ttu-id="9060f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9060f-123">-DefaultProfile</span></span>
<span data-ttu-id="9060f-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9060f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9060f-125">-Force</span><span class="sxs-lookup"><span data-stu-id="9060f-125">-Force</span></span>
<span data-ttu-id="9060f-126">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="9060f-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9060f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9060f-127">-InputObject</span></span>
<span data-ttu-id="9060f-128">Объект VPNGateway, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="9060f-128">The vpnGateway object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9060f-129">-Name</span><span class="sxs-lookup"><span data-stu-id="9060f-129">-Name</span></span>
<span data-ttu-id="9060f-130">Имя VPNGateway.</span><span class="sxs-lookup"><span data-stu-id="9060f-130">The vpnGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9060f-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9060f-131">-PassThru</span></span>
<span data-ttu-id="9060f-132">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="9060f-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9060f-133">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9060f-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9060f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9060f-134">-ResourceGroupName</span></span>
<span data-ttu-id="9060f-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9060f-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9060f-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9060f-136">-ResourceId</span></span>
<span data-ttu-id="9060f-137">ИД ресурса Azure для VPNGateway, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="9060f-137">The Azure resource ID for the vpnGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: vpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9060f-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9060f-138">-Confirm</span></span>
<span data-ttu-id="9060f-139">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9060f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9060f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9060f-140">-WhatIf</span></span>
<span data-ttu-id="9060f-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9060f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9060f-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9060f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9060f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9060f-143">CommonParameters</span></span>
<span data-ttu-id="9060f-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9060f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9060f-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9060f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9060f-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9060f-146">INPUTS</span></span>

### <span data-ttu-id="9060f-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9060f-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="9060f-148">System.String</span><span class="sxs-lookup"><span data-stu-id="9060f-148">System.String</span></span>

## <span data-ttu-id="9060f-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9060f-149">OUTPUTS</span></span>

### <span data-ttu-id="9060f-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9060f-150">System.Boolean</span></span>

## <span data-ttu-id="9060f-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9060f-151">NOTES</span></span>

## <span data-ttu-id="9060f-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9060f-152">RELATED LINKS</span></span>

[<span data-ttu-id="9060f-153">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9060f-153">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="9060f-154">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9060f-154">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="9060f-155">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9060f-155">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)