---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
ms.openlocfilehash: 30addde4594c7b67fd5ba9c1358d64ac206a4531
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390967"
---
# <span data-ttu-id="05504-101">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="05504-101">Get-AzExpressRouteCrossConnectionArpTable</span></span>

## <span data-ttu-id="05504-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05504-102">SYNOPSIS</span></span>
<span data-ttu-id="05504-103">Получает таблицу ARP из перекрестного подключения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="05504-103">Gets the ARP table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="05504-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="05504-104">SYNTAX</span></span>

### <span data-ttu-id="05504-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="05504-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05504-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="05504-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05504-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05504-107">DESCRIPTION</span></span>
<span data-ttu-id="05504-108">С помощью cmdlet **Get-AzExpressRouteCrossConnectionARPTable** можно извлечь таблицу ARP из обоих интерфейсов перекрестного подключения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="05504-108">The **Get-AzExpressRouteCrossConnectionARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute cross connection.</span></span> <span data-ttu-id="05504-109">Таблица "ARP" содержит сопоставление IPv4-адреса с MAC-адресом для определенного пиринга.</span><span class="sxs-lookup"><span data-stu-id="05504-109">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="05504-110">Таблицу ARP можно использовать для проверки конфигурации и подключения уровня 2.</span><span class="sxs-lookup"><span data-stu-id="05504-110">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="05504-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="05504-111">EXAMPLES</span></span>

### <span data-ttu-id="05504-112">Пример 1. Отображение таблицы ARP для одноранговой сети ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="05504-112">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCrossConnectionARPTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="05504-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05504-113">PARAMETERS</span></span>

### <span data-ttu-id="05504-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="05504-114">-CrossConnectionName</span></span>
<span data-ttu-id="05504-115">Имя перекрестного подключения Express Route</span><span class="sxs-lookup"><span data-stu-id="05504-115">The Name of Express Route Cross Connection</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05504-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05504-116">-DefaultProfile</span></span>
<span data-ttu-id="05504-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="05504-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05504-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="05504-118">-DevicePath</span></span>
<span data-ttu-id="05504-119">Допустимыми значениями для этого параметра являются: `Primary` или `Secondary`</span><span class="sxs-lookup"><span data-stu-id="05504-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.DevicePathEnum
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05504-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="05504-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="05504-121">Перекрестное подключение Express Route</span><span class="sxs-lookup"><span data-stu-id="05504-121">The Express Route Cross Connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: SpecifyByReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05504-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="05504-122">-PeeringType</span></span>
<span data-ttu-id="05504-123">Допустимыми значениями для этого параметра являются: `AzurePrivatePeering` `AzurePublicPeering` , и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="05504-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05504-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05504-124">-ResourceGroupName</span></span>
<span data-ttu-id="05504-125">Имя группы ресурсов, содержащей перекрестное подключение ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="05504-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05504-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05504-126">CommonParameters</span></span>
<span data-ttu-id="05504-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05504-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05504-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05504-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05504-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05504-129">INPUTS</span></span>

### <span data-ttu-id="05504-130">Нет</span><span class="sxs-lookup"><span data-stu-id="05504-130">None</span></span>
<span data-ttu-id="05504-131">Этот cmdlet не принимает входные данные.</span><span class="sxs-lookup"><span data-stu-id="05504-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="05504-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="05504-132">OUTPUTS</span></span>

### <span data-ttu-id="05504-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="05504-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="05504-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="05504-134">NOTES</span></span>

## <span data-ttu-id="05504-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05504-135">RELATED LINKS</span></span>

[<span data-ttu-id="05504-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="05504-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)

[<span data-ttu-id="05504-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="05504-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)