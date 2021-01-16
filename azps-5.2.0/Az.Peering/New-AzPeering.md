---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeering.md
ms.openlocfilehash: 41880f4d3e6a0f7cea67e60853d8309c9377d494
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407332"
---
# <span data-ttu-id="3ec20-101">New-AzPeering</span><span class="sxs-lookup"><span data-stu-id="3ec20-101">New-AzPeering</span></span>

## <span data-ttu-id="3ec20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ec20-102">SYNOPSIS</span></span>
<span data-ttu-id="3ec20-103">Создание нового ресурса для ARM пиринга</span><span class="sxs-lookup"><span data-stu-id="3ec20-103">Creates a new Peering ARM Resource</span></span>

## <span data-ttu-id="3ec20-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3ec20-104">SYNTAX</span></span>

### <span data-ttu-id="3ec20-105">Exchange (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3ec20-105">Exchange (Default)</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeerAsnResourceId] <String> -ExchangeConnection <PSExchangeConnection[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ec20-106">ConvertLegacyPeering</span><span class="sxs-lookup"><span data-stu-id="3ec20-106">ConvertLegacyPeering</span></span>
```
New-AzPeering -InputObject <PSPeering> [-ResourceGroupName] <String> [-Name] <String>
 [-PeerAsnResourceId] <String> [-ExchangeConnection <PSExchangeConnection[]>]
 [-DirectConnection <PSDirectConnection[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ec20-107">Direct</span><span class="sxs-lookup"><span data-stu-id="3ec20-107">Direct</span></span>
```
New-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 -MicrosoftNetwork <String> [-PeerAsnResourceId] <String> -DirectConnection <PSDirectConnection[]>
 -Sku <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ec20-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ec20-108">DESCRIPTION</span></span>
<span data-ttu-id="3ec20-109">Создается ARM пиринг для подписки.</span><span class="sxs-lookup"><span data-stu-id="3ec20-109">Creates an ARM Peering for the subscription.</span></span> <span data-ttu-id="3ec20-110">Дополнительные сведения о создании объектов подключения см. в проекте [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) или [New-AzPeeringExchangeConnectionObject.](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject)</span><span class="sxs-lookup"><span data-stu-id="3ec20-110">See [New-AzPeeringDirectConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject) or [New-AzPeeringExchangeConnectionObject](https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject) for more information on creating a connection object.</span></span>

## <span data-ttu-id="3ec20-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3ec20-111">EXAMPLES</span></span>

### <span data-ttu-id="3ec20-112">Создание нового прямого пиринга</span><span class="sxs-lookup"><span data-stu-id="3ec20-112">Create New Direct Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the Direct Peering Location
PS C:> $location = Get-AzPeeringLocation Direct -PeeringLocation Seattle
#Creates the ARM Resource
PS C:> New-AzPeering -Name ContosoSeattlePeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id -DirectConnection $connection

Name                 : ContosoSeattlePeering
Sku.Name             : Basic_Direct_Free
Kind                 : Direct
Connections          : {99999}
PeerAsn.Id           : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
UseForPeeringService : False
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : centralus
Id                   : /subscriptions//resourceGroups/testCarrier/providers/Microsoft.Peering/peerings/ContosoSeattlePeering
Type                 : Microsoft.Peering/peerings
Tags                 : {}
```

<span data-ttu-id="3ec20-113">Создание нового прямого пиринга с одним подключением на территории Сиэтла с помощью PeerAsn 65000</span><span class="sxs-lookup"><span data-stu-id="3ec20-113">Create a new Direct Peering with a single connection at the Seattle facility using PeerAsn 65000</span></span>

### <span data-ttu-id="3ec20-114">Создание нового пиринга Exchange</span><span class="sxs-lookup"><span data-stu-id="3ec20-114">Create New Exchange Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the Exchange Peering Location
PS C:> $location = Get-AzPeeringLocation Exchange -PeeringLocation Seattle
#Creates the ARM Resource
PS C:> New-AzPeering -Name ContosoSeattlePeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id -ExchangeConnection $connection

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions//resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="3ec20-115">Создание нового пиринга exchange</span><span class="sxs-lookup"><span data-stu-id="3ec20-115">Create a new exchange peering</span></span>

### <span data-ttu-id="3ec20-116">Преобразование устаревшего пиринга в ARM пирингу</span><span class="sxs-lookup"><span data-stu-id="3ec20-116">Convert Legacy Peering to ARM Peering</span></span>
```powershell
#Gets the ASN
PS C:> $asn = Get-AzPeerAsn -PeerName Contoso
#Gets the legacy Peering
PS C:> $legacy = Get-AzLegacyPeering -PeeringLocation Amsterdam -Kind Direct | New-AzPeering -Name ContosoAmsterdamPeering -ResourceGroupName testCarrier -PeeringLocation $location.PeeringLocation -PeerAsnResourceId $asn.Id

Name              : ContosoAmsterdamPeering
Sku.Name          : Basic_Direct_Free
Kind              : Direct
Connections       : {64}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions//resourceGroups/test/providers/Microsoft.Peering/peerings/ContosoAmsterdamPeering
Type              : Microsoft.Peering/peerings
Tags              : {}
```

## <span data-ttu-id="3ec20-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ec20-117">PARAMETERS</span></span>

### <span data-ttu-id="3ec20-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ec20-118">-AsJob</span></span>
<span data-ttu-id="3ec20-119">Запускать в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="3ec20-119">Run in the background.</span></span>

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

### <span data-ttu-id="3ec20-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ec20-120">-DefaultProfile</span></span>
<span data-ttu-id="3ec20-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ec20-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ec20-122">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="3ec20-122">-DirectConnection</span></span>
<span data-ttu-id="3ec20-123">Создайте новое прямое подключение, используя New-AzExchangePeeringConnection и по конвейеру до этой команды.</span><span class="sxs-lookup"><span data-stu-id="3ec20-123">Create a new Direct connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec20-124">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="3ec20-124">-ExchangeConnection</span></span>
<span data-ttu-id="3ec20-125">Создайте новые подключения Exchange, используя команду New-AzExchangePeeringConnection и по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="3ec20-125">Create a new Exchange connections using the New-AzExchangePeeringConnection and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: Exchange
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec20-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ec20-126">-InputObject</span></span>
<span data-ttu-id="3ec20-127">Используйте Get-AzLegacyPeering для извлечения этого объекта.</span><span class="sxs-lookup"><span data-stu-id="3ec20-127">Use Get-AzLegacyPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: ConvertLegacyPeering
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ec20-128">-MicrosoftNetwork</span><span class="sxs-lookup"><span data-stu-id="3ec20-128">-MicrosoftNetwork</span></span>
<span data-ttu-id="3ec20-129">Выберите сеть Майкрософт, с помощью чего вы хотите иметь одноранговую сеть.</span><span class="sxs-lookup"><span data-stu-id="3ec20-129">Select the Microsoft network you want to peer with.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec20-130">-Name</span><span class="sxs-lookup"><span data-stu-id="3ec20-130">-Name</span></span>
<span data-ttu-id="3ec20-131">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="3ec20-131">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec20-132">-PeerAsnResourceId</span><span class="sxs-lookup"><span data-stu-id="3ec20-132">-PeerAsnResourceId</span></span>
<span data-ttu-id="3ec20-133">ИД ресурса одноранговой asn. Get-AzPeerAsn, чтобы получить его.</span><span class="sxs-lookup"><span data-stu-id="3ec20-133">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec20-134">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="3ec20-134">-PeeringLocation</span></span>
<span data-ttu-id="3ec20-135">Физическое расположение, отличаее от региона Azure.</span><span class="sxs-lookup"><span data-stu-id="3ec20-135">The Physical Location Different from Azure Region.</span></span>
<span data-ttu-id="3ec20-136">Используйте Get-AzPeeringLocation -Kind \<kind\> use City name as key.</span><span class="sxs-lookup"><span data-stu-id="3ec20-136">Use Get-AzPeeringLocation -Kind \<kind\> use City name as key.</span></span>

```yaml
Type: System.String
Parameter Sets: Exchange, Direct
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec20-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ec20-137">-ResourceGroupName</span></span>
<span data-ttu-id="3ec20-138">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3ec20-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec20-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="3ec20-139">-Sku</span></span>
<span data-ttu-id="3ec20-140">Выберите Basic_Direct_Free или Premium_Direct_Free, если вы не выбрали другой параметр явным образом.</span><span class="sxs-lookup"><span data-stu-id="3ec20-140">Select Basic_Direct_Free or Premium_Direct_Free unless explicitly told to select another option.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec20-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="3ec20-141">-Tag</span></span>
<span data-ttu-id="3ec20-142">Теги, которые нужно связать со службой пиринга Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="3ec20-142">The tags to associate with the Microsoft Peering Service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ec20-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ec20-143">-Confirm</span></span>
<span data-ttu-id="3ec20-144">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ec20-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ec20-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ec20-145">-WhatIf</span></span>
<span data-ttu-id="3ec20-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ec20-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ec20-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3ec20-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ec20-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ec20-148">CommonParameters</span></span>
<span data-ttu-id="3ec20-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ec20-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ec20-150">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ec20-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ec20-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ec20-151">INPUTS</span></span>

### <span data-ttu-id="3ec20-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="3ec20-152">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="3ec20-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3ec20-153">OUTPUTS</span></span>

### <span data-ttu-id="3ec20-154">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="3ec20-154">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="3ec20-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3ec20-155">NOTES</span></span>

## <span data-ttu-id="3ec20-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ec20-156">RELATED LINKS</span></span>