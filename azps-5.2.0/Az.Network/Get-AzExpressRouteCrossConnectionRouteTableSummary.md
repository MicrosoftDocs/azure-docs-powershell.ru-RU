---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
ms.openlocfilehash: 7479d18660ede3f70ac5e62f614b8a815b86433c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390948"
---
# <span data-ttu-id="f187a-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="f187a-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

## <span data-ttu-id="f187a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f187a-102">SYNOPSIS</span></span>
<span data-ttu-id="f187a-103">Получает сводку таблицы маршрутов для перекрестного подключения ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f187a-103">Gets a route table summary of an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="f187a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f187a-104">SYNTAX</span></span>

### <span data-ttu-id="f187a-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="f187a-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f187a-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="f187a-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f187a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f187a-107">DESCRIPTION</span></span>
<span data-ttu-id="f187a-108">С  его учетом можно получить сводку данных о соседних BGP-данных для конкретного контекста маршрутки.</span><span class="sxs-lookup"><span data-stu-id="f187a-108">The **Get-AzExpressRouteCrossConnectionRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="f187a-109">Эти сведения полезны для определения времени установления контекста маршрутки и количества префиксов маршрутов, объявленных маршрутизатором пиринга.</span><span class="sxs-lookup"><span data-stu-id="f187a-109">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="f187a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f187a-110">EXAMPLES</span></span>

### <span data-ttu-id="f187a-111">Пример 1. Отображение сводки маршрута для основного пути</span><span class="sxs-lookup"><span data-stu-id="f187a-111">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -DevicePath 'Primary'
```

## <span data-ttu-id="f187a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f187a-112">PARAMETERS</span></span>

### <span data-ttu-id="f187a-113">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="f187a-113">-CrossConnectionName</span></span>
<span data-ttu-id="f187a-114">Имя перекрестного подключения Express Route</span><span class="sxs-lookup"><span data-stu-id="f187a-114">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="f187a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f187a-115">-DefaultProfile</span></span>
<span data-ttu-id="f187a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f187a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f187a-117">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="f187a-117">-DevicePath</span></span>
<span data-ttu-id="f187a-118">Допустимыми значениями для этого параметра являются: `Primary` или `Secondary`</span><span class="sxs-lookup"><span data-stu-id="f187a-118">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="f187a-119">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f187a-119">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="f187a-120">Перекрестное подключение Express Route</span><span class="sxs-lookup"><span data-stu-id="f187a-120">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="f187a-121">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="f187a-121">-PeeringType</span></span>
<span data-ttu-id="f187a-122">Допустимыми значениями для этого параметра являются: `AzurePrivatePeering` `AzurePublicPeering` , и `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="f187a-122">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="f187a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f187a-123">-ResourceGroupName</span></span>
<span data-ttu-id="f187a-124">Имя группы ресурсов, содержащей перекрестное подключение ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="f187a-124">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="f187a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f187a-125">CommonParameters</span></span>
<span data-ttu-id="f187a-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f187a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f187a-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f187a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f187a-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f187a-128">INPUTS</span></span>

### <span data-ttu-id="f187a-129">Нет</span><span class="sxs-lookup"><span data-stu-id="f187a-129">None</span></span>
<span data-ttu-id="f187a-130">Этот cmdlet не принимает входные данные.</span><span class="sxs-lookup"><span data-stu-id="f187a-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f187a-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f187a-131">OUTPUTS</span></span>

### <span data-ttu-id="f187a-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesSummary</span><span class="sxs-lookup"><span data-stu-id="f187a-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span></span>

## <span data-ttu-id="f187a-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f187a-133">NOTES</span></span>

## <span data-ttu-id="f187a-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f187a-134">RELATED LINKS</span></span>

[<span data-ttu-id="f187a-135">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="f187a-135">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="f187a-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="f187a-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)