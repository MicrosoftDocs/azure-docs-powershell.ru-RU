---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
ms.openlocfilehash: dc3cde19bde2da95fd2ffc731223783c1963d1f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327015"
---
# <span data-ttu-id="a595c-101">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="a595c-101">Set-AzExpressRouteConnection</span></span>

## <span data-ttu-id="a595c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a595c-102">SYNOPSIS</span></span>
<span data-ttu-id="a595c-103">Обновляет подключение express route, созданное между шлюзом express route и локальной пирингом express route.</span><span class="sxs-lookup"><span data-stu-id="a595c-103">Updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="a595c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a595c-104">SYNTAX</span></span>

### <span data-ttu-id="a595c-105">ByExpressRouteConnectionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a595c-105">ByExpressRouteConnectionName (Default)</span></span>
```
Set-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a595c-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="a595c-106">ByExpressRouteConnectionResourceId</span></span>
```
Set-AzExpressRouteConnection -ResourceId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a595c-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="a595c-107">ByExpressRouteConnectionObject</span></span>
```
Set-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-AuthorizationKey <String>]
 [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a595c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a595c-108">DESCRIPTION</span></span>
<span data-ttu-id="a595c-109">Командалет **Set-AzExpressRouteConnection** обновляет подключение express route, созданное между шлюзом express route и локальной пирингом express route.</span><span class="sxs-lookup"><span data-stu-id="a595c-109">The **Set-AzExpressRouteConnection** cmdlet updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="a595c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a595c-110">EXAMPLES</span></span>

### <span data-ttu-id="a595c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a595c-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> $ExpressRouteGateway = Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"
PS C:\> $ExpressRouteCircuit = New-AzExpressRouteCircuit -ResourceGroupName "testRG" -Name "testExpressRouteCircuit" -Location "West Central US" -SkuTier Premium -SkuFamily MeteredData -ServiceProviderName "Equinix" -PeeringLocation "Silicon Valley" -BandwidthInMbps 200
PS C:\> Add-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ExpressRouteCircuit -PeeringType AzurePrivatePeering -PeerASN 100 -PrimaryPeerAddressPrefix "123.0.0.0/30" -SecondaryPeerAddressPrefix "123.0.0.4/30" -VlanId 300
PS C:\> $ExpressRouteCircuit = Set-AzExpressRouteCircuit -ExpressRouteCircuit $ExpressRouteCircuit
PS C:\> $ExpressRouteCircuitPeeringId = $ExpressRouteCircuit.Peerings[0].Id
PS C:\> New-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" -ExpressRouteCircuitPeeringId $ExpressRouteCircuitPeeringId -RoutingWeight 20
PS C:\> Set-AzExpressRouteConnection -InputObject $ExpressRouteConnection -RoutingWeight 30

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 30
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
RoutingConfiguration               : {
                                       "AssociatedRouteTable": {
                                         "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                       },
                                       "PropagatedRouteTables": {
                                         "Labels": [],
                                         "Ids": [
                                           {
                                             "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                           }
                                         ]
                                       },
                                       "VnetRoutes": {
                                         "StaticRoutes": []
                                       }
                                     }
```

<span data-ttu-id="a595c-112">Выше будет создаваться группа ресурсов, виртуальная сеть, виртуальная сеть, виртуальный концентратор и узел ExpressRouteSite в западной части США в группе ресурсов testRG в Azure.</span><span class="sxs-lookup"><span data-stu-id="a595c-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="a595c-113">После этого в виртуальном центре будет создан шлюз ExpressRoute с 2-масштабными единицами.</span><span class="sxs-lookup"><span data-stu-id="a595c-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="a595c-114">После создания шлюз подключается к локальному каналу ExpressRoute с помощью команды New-AzExpressRouteConnection подключения.</span><span class="sxs-lookup"><span data-stu-id="a595c-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit peering using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="a595c-115">Соединение будет обновлено с использованием команды Set-AzExpressRouteConnection RoutingWeight.</span><span class="sxs-lookup"><span data-stu-id="a595c-115">The connection is then updated to have a different RoutingWeight by using the Set-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="a595c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a595c-116">PARAMETERS</span></span>

### <span data-ttu-id="a595c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a595c-117">-AsJob</span></span>
<span data-ttu-id="a595c-118">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a595c-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a595c-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="a595c-119">-AuthorizationKey</span></span>
<span data-ttu-id="a595c-120">Ключ авторизации, используемый для создания подключения шлюза ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="a595c-120">The authorization key to be used to create the ExpressRoute gateway connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a595c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a595c-121">-DefaultProfile</span></span>
<span data-ttu-id="a595c-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a595c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a595c-123">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="a595c-123">-EnableInternetSecurity</span></span>
<span data-ttu-id="a595c-124">Включить безопасность Интернета для этого подключения шлюза ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="a595c-124">Enable internet security for this ExpressRoute Gateway connection</span></span>

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

### <span data-ttu-id="a595c-125">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="a595c-125">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="a595c-126">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="a595c-126">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a595c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a595c-127">-InputObject</span></span>
<span data-ttu-id="a595c-128">Объект ExpressRouteConnection, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="a595c-128">The ExpressRouteConnection object to update.</span></span>

```yaml
Type: PSExpressRouteConnection
Parameter Sets: ByExpressRouteConnectionObject
Aliases: ExpressRouteConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a595c-129">-Name</span><span class="sxs-lookup"><span data-stu-id="a595c-129">-Name</span></span>
<span data-ttu-id="a595c-130">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="a595c-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionName
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a595c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a595c-131">-ResourceGroupName</span></span>
<span data-ttu-id="a595c-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a595c-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a595c-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a595c-133">-ResourceId</span></span>
<span data-ttu-id="a595c-134">ИД ресурса объекта ExpressRouteConnection, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a595c-134">The resource id of the ExpressRouteConnection object to delete.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionResourceId
Aliases: ExpressRouteConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a595c-135">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="a595c-135">-RoutingConfiguration</span></span>
<span data-ttu-id="a595c-136">Настройка маршрутиации для этого подключения</span><span class="sxs-lookup"><span data-stu-id="a595c-136">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a595c-137">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="a595c-137">-RoutingWeight</span></span>
<span data-ttu-id="a595c-138">Вес, который должен быть назначен этому подключению для маршрутики пакетов.</span><span class="sxs-lookup"><span data-stu-id="a595c-138">The weight that needs to be assigned to this connection for packet routing.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a595c-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a595c-139">-Confirm</span></span>
<span data-ttu-id="a595c-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a595c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a595c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a595c-141">-WhatIf</span></span>
<span data-ttu-id="a595c-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a595c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a595c-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a595c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a595c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a595c-144">CommonParameters</span></span>
<span data-ttu-id="a595c-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a595c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a595c-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a595c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a595c-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a595c-147">INPUTS</span></span>

### <span data-ttu-id="a595c-148">System.String</span><span class="sxs-lookup"><span data-stu-id="a595c-148">System.String</span></span>

### <span data-ttu-id="a595c-149">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="a595c-149">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="a595c-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a595c-150">OUTPUTS</span></span>

### <span data-ttu-id="a595c-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="a595c-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="a595c-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a595c-152">NOTES</span></span>

## <span data-ttu-id="a595c-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a595c-153">RELATED LINKS</span></span>

[<span data-ttu-id="a595c-154">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="a595c-154">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)