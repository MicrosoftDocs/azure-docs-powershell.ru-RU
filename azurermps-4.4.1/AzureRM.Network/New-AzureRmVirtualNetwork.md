---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 81D55C43-C9A3-4DA7-A469-A3A7550FE9A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetwork.md
ms.openlocfilehash: 7fccc6b16d44e9bd050d40a21a748dbd1d251a06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570352"
---
# <span data-ttu-id="8af38-101">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8af38-101">New-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="8af38-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8af38-102">SYNOPSIS</span></span>
<span data-ttu-id="8af38-103">Создание виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8af38-103">Creates a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8af38-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8af38-104">SYNTAX</span></span>

```
New-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -Location <String>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-Subnet <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]>]
 [-Tag <Hashtable>] [-EnableDDoSProtection] [-EnableVmProtection] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8af38-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8af38-105">DESCRIPTION</span></span>
<span data-ttu-id="8af38-106">Командлет **New-AzureRmVirtualNetwork** создает виртуальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="8af38-106">The **New-AzureRmVirtualNetwork** cmdlet creates an Azure virtual network.</span></span>

## <span data-ttu-id="8af38-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8af38-107">EXAMPLES</span></span>

### <span data-ttu-id="8af38-108">1: создание виртуальной сети с двумя подсетями</span><span class="sxs-lookup"><span data-stu-id="8af38-108">1:  Create a virtual network with two subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="8af38-109">В этом примере создается виртуальная сеть с двумя подсетями.</span><span class="sxs-lookup"><span data-stu-id="8af38-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="8af38-110">Сначала создается новая группа ресурсов в области centralus.</span><span class="sxs-lookup"><span data-stu-id="8af38-110">First, a new resource group is created in the centralus region.</span></span> <span data-ttu-id="8af38-111">Затем в примере создаются представления двух подсетей в памяти.</span><span class="sxs-lookup"><span data-stu-id="8af38-111">Then, the example creates in-memory representations of two subnets.</span></span> <span data-ttu-id="8af38-112">Командлет New-AzureRmVirtualNetworkSubnetConfig не создаст подсеть на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="8af38-112">The New-AzureRmVirtualNetworkSubnetConfig cmdlet will not create any subnet on the server side.</span></span> <span data-ttu-id="8af38-113">Одна подсеть называется frontendSubnet и одной подсетью под названием backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="8af38-113">There is one subnet called frontendSubnet and one subnet called backendSubnet.</span></span> <span data-ttu-id="8af38-114">Затем командлет New-AzureRmVirtualNetwork создает виртуальную сеть, используя CIDR 10.0.0.0/16 в качестве префикса адреса и двух подсетей.</span><span class="sxs-lookup"><span data-stu-id="8af38-114">The New-AzureRmVirtualNetwork cmdlet then creates a virtual network using the CIDR 10.0.0.0/16 as the address prefix and two subnets.</span></span>

### <span data-ttu-id="8af38-115">2. Создание виртуальной сети с помощью параметров DNS</span><span class="sxs-lookup"><span data-stu-id="8af38-115">2:  Create a virtual network with DNS settings</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet -DnsServer 10.0.1.5,10.0.1.6
```

<span data-ttu-id="8af38-116">В этом примере создается виртуальная сеть с двумя подсетями и двумя DNS-серверами.</span><span class="sxs-lookup"><span data-stu-id="8af38-116">This example create a virtual network with two subnets and two DNS servers.</span></span> <span data-ttu-id="8af38-117">Результат задания DNS-серверов в виртуальной сети заключается в том, что сетевые адаптеры и виртуальные машины, развернутые в этой виртуальной сети, наследуют эти DNS-серверы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8af38-117">The effect of specifying the DNS servers on the virtual network is that the NICs/VMs that are deployed into this virtual network inherit these DNS servers as defaults.</span></span> <span data-ttu-id="8af38-118">Эти значения по умолчанию могут быть заменены на NIC с помощью параметра уровня NIC.</span><span class="sxs-lookup"><span data-stu-id="8af38-118">These defaults can be overwritten per NIC through a NIC-level setting.</span></span> <span data-ttu-id="8af38-119">Если в виртуальной сети не указаны DNS-серверы и DNS-серверы на сетевых адаптерах, то для разрешения DNS используются DNS-серверы Azure по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8af38-119">If no DNS servers are specified on a VNET and no DNS servers on the NICs, then the default Azure DNS servers are used for DNS resolution.</span></span>

### <span data-ttu-id="8af38-120">3. Создание виртуальной сети с подсетью, ссылающейся на сетевую группу безопасности</span><span class="sxs-lookup"><span data-stu-id="8af38-120">3: Create a virtual network with a subnet referencing a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
$rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule
$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup
$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup
New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="8af38-121">В этом примере создается виртуальная сеть с подсетями, которые ссылаются на сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="8af38-121">This example creates a virtual network with subnets that reference a network security group.</span></span> <span data-ttu-id="8af38-122">Сначала в примере создается группа ресурсов в качестве контейнера для ресурсов, которые будут созданы.</span><span class="sxs-lookup"><span data-stu-id="8af38-122">First, the example creates a resource group as a container for the resources that will be created.</span></span> <span data-ttu-id="8af38-123">Затем создается группа безопасности сети, разрешающая входящий доступ к удаленному рабочему столу, но в противном случае принудительно применяет правила групповой безопасности по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8af38-123">Then, a network security group is created that allows inbound RDP access, but otherwise enforces the default network security group rules.</span></span> <span data-ttu-id="8af38-124">Затем командлет New-AzureRmVirtualNetworkSubnetConfig создает в памяти одновременные представления двух подсетей, которые ссылаются на созданную сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="8af38-124">The New-AzureRmVirtualNetworkSubnetConfig cmdlet then creates in-memory representations of two subnets that both reference the network security group that was created.</span></span> <span data-ttu-id="8af38-125">Затем команда New-AzureRmVirtualNetwork создает виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="8af38-125">The New-AzureRmVirtualNetwork command then creates the virtual network.</span></span>

## <span data-ttu-id="8af38-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8af38-126">PARAMETERS</span></span>

### <span data-ttu-id="8af38-127">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8af38-127">-AddressPrefix</span></span>
<span data-ttu-id="8af38-128">Указывает диапазон IP-адресов для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8af38-128">Specifies a range of IP addresses for a virtual network.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8af38-129">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="8af38-129">-DnsServer</span></span>
<span data-ttu-id="8af38-130">Указывает DNS-сервер для подсети.</span><span class="sxs-lookup"><span data-stu-id="8af38-130">Specifies the DNS server for a subnet.</span></span>

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

### <span data-ttu-id="8af38-131">-EnableVmProtection</span><span class="sxs-lookup"><span data-stu-id="8af38-131">-EnableVmProtection</span></span>
<span data-ttu-id="8af38-132">Параметр переключателя, который обозначает, включена ли защита виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8af38-132">A switch parameter which represents if Vm protection is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8af38-133">-Force</span><span class="sxs-lookup"><span data-stu-id="8af38-133">-Force</span></span>
<span data-ttu-id="8af38-134">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8af38-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8af38-135">-Location</span><span class="sxs-lookup"><span data-stu-id="8af38-135">-Location</span></span>
<span data-ttu-id="8af38-136">Указывает регион для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8af38-136">Specifies the region for the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8af38-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8af38-137">-Name</span></span>
<span data-ttu-id="8af38-138">Указывает имя виртуальной сети, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="8af38-138">Specifies the name of the virtual network that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8af38-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8af38-139">-ResourceGroupName</span></span>
<span data-ttu-id="8af38-140">Указывает имя группы ресурсов, которая будет содержать виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="8af38-140">Specifies the name of a resource group to contain the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8af38-141">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="8af38-141">-Subnet</span></span>
<span data-ttu-id="8af38-142">Указывает список подсетей, которые нужно связать с виртуальной сетью.</span><span class="sxs-lookup"><span data-stu-id="8af38-142">Specifies a list of subnets to associate with the virtual network.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSubnet]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8af38-143">-Тег</span><span class="sxs-lookup"><span data-stu-id="8af38-143">-Tag</span></span>
<span data-ttu-id="8af38-144">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="8af38-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8af38-145">Например:</span><span class="sxs-lookup"><span data-stu-id="8af38-145">For example:</span></span>

<span data-ttu-id="8af38-146">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="8af38-146">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8af38-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8af38-147">-Confirm</span></span>
<span data-ttu-id="8af38-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8af38-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8af38-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8af38-149">-WhatIf</span></span>
<span data-ttu-id="8af38-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8af38-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8af38-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8af38-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8af38-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8af38-152">-DefaultProfile</span></span>
<span data-ttu-id="8af38-153">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8af38-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8af38-154">-EnableDDoSProtection</span><span class="sxs-lookup"><span data-stu-id="8af38-154">-EnableDDoSProtection</span></span>
<span data-ttu-id="8af38-155">Параметр Switch, обозначающий, включена ли защита Distributed или нет.</span><span class="sxs-lookup"><span data-stu-id="8af38-155">A switch parameter which represents if DDoS protection is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8af38-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8af38-156">CommonParameters</span></span>
<span data-ttu-id="8af38-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8af38-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8af38-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8af38-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8af38-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8af38-159">INPUTS</span></span>

## <span data-ttu-id="8af38-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8af38-160">OUTPUTS</span></span>

### <span data-ttu-id="8af38-161">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8af38-161">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="8af38-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="8af38-162">NOTES</span></span>

## <span data-ttu-id="8af38-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8af38-163">RELATED LINKS</span></span>

[<span data-ttu-id="8af38-164">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8af38-164">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="8af38-165">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8af38-165">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="8af38-166">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8af38-166">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)