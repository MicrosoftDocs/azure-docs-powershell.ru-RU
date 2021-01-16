---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipconfigurationbgppeeringaddressobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
ms.openlocfilehash: 2a31aa9db3264dd24c6d77bdad7b10d6ecad10b1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421700"
---
# <span data-ttu-id="5c59a-101">New-AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="5c59a-101">New-AzIpConfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="5c59a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c59a-102">SYNOPSIS</span></span>
<span data-ttu-id="5c59a-103">создание нового ipconfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="5c59a-103">creates a new IpconfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="5c59a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5c59a-104">SYNTAX</span></span>

### <span data-ttu-id="5c59a-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5c59a-105">Default (Default)</span></span>
```
New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId <String>
 -CustomAddress <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```
## <span data-ttu-id="5c59a-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c59a-106">DESCRIPTION</span></span>
<span data-ttu-id="5c59a-107">С помощью **свойства New-AzIpConfigurationBgpPeeringAddressObject** создается объект IpConfigurationBgpPeeringAddressObject, который представляет свойство BgpPeeringAddresses в Bgpsettings виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="5c59a-107">The **New-AzIpConfigurationBgpPeeringAddressObject** creates a IpConfigurationBgpPeeringAddressObject object which represents BgpPeeringAddresses property in your virtual network gateway bgpsettings.</span></span>

## <span data-ttu-id="5c59a-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5c59a-108">EXAMPLES</span></span>

### <span data-ttu-id="5c59a-109">1. Создание azIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="5c59a-109">1: Create a AzIpConfigurationBgpPeeringAddressObject</span></span>
```
$ipconfigurationId1 = '/subscriptions/c886bc58-0000-4e01-993f-e01ba3702aaf/resourceGroups/testRg/providers/Microsoft.Network/virtualNetworkGateways/gw1/ipConfigurations/default'
$addresslist1 = @('169.254.21.5')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddresses -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
```

<span data-ttu-id="5c59a-110">Выше будет создаваться ipConfigurationBgpPeeringAddressObject.This new object will be to gw1ipconfBgp1.</span><span class="sxs-lookup"><span data-stu-id="5c59a-110">The above will create a IpConfigurationBgpPeeringAddressObject.This new object will be to gw1ipconfBgp1.</span></span>

## <span data-ttu-id="5c59a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c59a-111">PARAMETERS</span></span>

### <span data-ttu-id="5c59a-112">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c59a-112">-Confirm</span></span>
<span data-ttu-id="5c59a-113">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5c59a-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c59a-114">-CustomAddress</span><span class="sxs-lookup"><span data-stu-id="5c59a-114">-CustomAddress</span></span>
<span data-ttu-id="5c59a-115">Список customAddress виртуального сетевого шлюза для BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="5c59a-115">The virtual network gateway CustomAddress List for BgpPeeringAddresses.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c59a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c59a-116">-DefaultProfile</span></span>
<span data-ttu-id="5c59a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5c59a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c59a-118">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5c59a-118">-IpConfigurationId</span></span>
<span data-ttu-id="5c59a-119">Виртуальный сетевой шлюз IpConfigurationId для BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="5c59a-119">The virtual network gateway IpConfigurationId for BgpPeeringAddresses.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c59a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c59a-120">-WhatIf</span></span>
<span data-ttu-id="5c59a-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c59a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c59a-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5c59a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c59a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c59a-123">CommonParameters</span></span>
<span data-ttu-id="5c59a-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c59a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c59a-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c59a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c59a-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c59a-126">INPUTS</span></span>

### <span data-ttu-id="5c59a-127">Нет</span><span class="sxs-lookup"><span data-stu-id="5c59a-127">None</span></span>

## <span data-ttu-id="5c59a-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5c59a-128">OUTPUTS</span></span>

### <span data-ttu-id="5c59a-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="5c59a-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span></span>

## <span data-ttu-id="5c59a-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5c59a-130">NOTES</span></span>

## <span data-ttu-id="5c59a-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c59a-131">RELATED LINKS</span></span>