---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F1522074-7EEA-4DCF-AC16-26FE8E654720
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancer.md
ms.openlocfilehash: 558f7bb9937d52117f37cc4964d4dc925b0dca47
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421679"
---
# <span data-ttu-id="46981-101">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="46981-101">New-AzLoadBalancer</span></span>

## <span data-ttu-id="46981-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46981-102">SYNOPSIS</span></span>
<span data-ttu-id="46981-103">Создает балансировку нагрузки.</span><span class="sxs-lookup"><span data-stu-id="46981-103">Creates a load balancer.</span></span>

## <span data-ttu-id="46981-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="46981-104">SYNTAX</span></span>

```
New-AzLoadBalancer -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Sku <String>] [-Tier <String>] [-FrontendIpConfiguration <PSFrontendIPConfiguration[]>]
 [-BackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancingRule <PSLoadBalancingRule[]>]
 [-Probe <PSProbe[]>] [-InboundNatRule <PSInboundNatRule[]>] [-InboundNatPool <PSInboundNatPool[]>]
 [-OutboundRule <PSOutboundRule[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46981-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46981-105">DESCRIPTION</span></span>
<span data-ttu-id="46981-106">Для создания балансиров нагрузки Azure создается новый клиент **AzLoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="46981-106">The **New-AzLoadBalancer** cmdlet creates an Azure load balancer.</span></span>

## <span data-ttu-id="46981-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="46981-107">EXAMPLES</span></span>

### <span data-ttu-id="46981-108">Пример 1. Создание балансиров нагрузки</span><span class="sxs-lookup"><span data-stu-id="46981-108">Example 1: Create a load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIp" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig02"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx"
PS C:\> $inboundNatRule1 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule1" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389 -IdleTimeoutInMinutes 15 -EnableFloatingIP
PS C:\> $inboundNatRule2 = New-AzLoadBalancerInboundNatRuleConfig -Name "MyinboundNatRule2" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3391 -BackendPort 3392
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol "Tcp" -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP
PS C:\> $lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -InboundNatRule $inboundNatRule1,$inboundNatRule2 -LoadBalancingRule $lbrule
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="46981-109">Для развертывания балансировки нагрузки необходимо сначала создать несколько объектов, а первые семь команд покажут, как их создать.</span><span class="sxs-lookup"><span data-stu-id="46981-109">Deploying a load balancer requires that you first create several objects, and the first seven commands show how to create those objects.</span></span>
<span data-ttu-id="46981-110">С ее названием в группе ресурсов MyResourceGroup создается балансировка нагрузки MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="46981-110">The eighth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="46981-111">Последняя и последняя команда получает новый баланс нагрузки для успешного создания.</span><span class="sxs-lookup"><span data-stu-id="46981-111">The ninth and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="46981-112">Обратите внимание, что в этом примере показано только создание балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="46981-112">Note that this example only shows how to create a load balancer.</span></span> <span data-ttu-id="46981-113">Его также необходимо настроить с помощью Add-AzNetworkInterfaceIpConfig, чтобы назначить ники на различных виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="46981-113">You must also configure it using the Add-AzNetworkInterfaceIpConfig cmdlet to assign the NICs to different virtual machines.</span></span>

### <span data-ttu-id="46981-114">Пример 2. Создание глобального балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="46981-114">Example 2: Create a global load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -name "MyPublicIp" -Location "West US" -AllocationMethod Static -DomainNameLabel $domainNameLabel -Sku Standard -Tier Global
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
PS C:\> $backendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name "MyBackendAddPoolConfig01"
PS C:\> $probe = New-AzLoadBalancerProbeConfig -Name "MyProbe" -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
PS C:\> $lbrule = New-AzLoadBalancerRuleConfig -Name "MyLBruleName" -FrontendIPConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP -DisableOutboundSNAT
PS C:\> lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" -Location "West US" -FrontendIpConfiguration $frontend -BackendAddressPool $backendAddressPool -Probe $probe -LoadBalancingRule $lbrule -Sku Standard -Tier Global        
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="46981-115">Чтобы развернуть глобальный баланс нагрузки, необходимо сначала создать несколько объектов, а первые пять команд покажут, как их создать.</span><span class="sxs-lookup"><span data-stu-id="46981-115">Deploying a global load balancer requires that you first create several objects, and the first five commands show how to create those objects.</span></span>
<span data-ttu-id="46981-116">Шестая команда создает балансировку нагрузки MyLoadBalancer в группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="46981-116">The sixth command creates a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>
<span data-ttu-id="46981-117">Седьмой и последний команды получают новый баланс нагрузки для успешного создания.</span><span class="sxs-lookup"><span data-stu-id="46981-117">The seventh and last command gets the new load balancer to ensure it was successfully created.</span></span>
<span data-ttu-id="46981-118">Обратите внимание, что в этом примере показано только создание глобального балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="46981-118">Note that this example only shows how to create a global load balancer.</span></span> <span data-ttu-id="46981-119">Его также необходимо настроить с помощью New-AzLoadBalancerBackendAddressConfig для назначения ipconfig ids регионального балансирового баланса нагрузки своему пулу адресов</span><span class="sxs-lookup"><span data-stu-id="46981-119">You must also configure it using the New-AzLoadBalancerBackendAddressConfig cmdlet to assign regional load balancer frontend ipconfig ids to its backend address pool</span></span>

## <span data-ttu-id="46981-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46981-120">PARAMETERS</span></span>

### <span data-ttu-id="46981-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46981-121">-AsJob</span></span>
<span data-ttu-id="46981-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="46981-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46981-123">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="46981-123">-BackendAddressPool</span></span>
<span data-ttu-id="46981-124">Определяет пул адресов для загрузки, который нужно связать с балансировой нагрузкой.</span><span class="sxs-lookup"><span data-stu-id="46981-124">Specifies a backend address pool to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46981-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46981-125">-DefaultProfile</span></span>
<span data-ttu-id="46981-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="46981-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46981-127">-Force</span><span class="sxs-lookup"><span data-stu-id="46981-127">-Force</span></span>
<span data-ttu-id="46981-128">Указывает на то, что с помощью этого cmdlet создается баланс балансиров нагрузки, даже если балансировая нагрузка с таким именем уже существует.</span><span class="sxs-lookup"><span data-stu-id="46981-128">Indicates that this cmdlet creates a load balancer even if a load balancer with the same name already exists.</span></span>

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

### <span data-ttu-id="46981-129">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="46981-129">-FrontendIpConfiguration</span></span>
<span data-ttu-id="46981-130">Список IP-адресов, которые нужно связать с балансировой нагрузкой.</span><span class="sxs-lookup"><span data-stu-id="46981-130">Specifies a list of front-end IP addresses to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46981-131">-InboundNatPool</span><span class="sxs-lookup"><span data-stu-id="46981-131">-InboundNatPool</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46981-132">-InboundNatRule</span><span class="sxs-lookup"><span data-stu-id="46981-132">-InboundNatRule</span></span>
<span data-ttu-id="46981-133">Определяет список правил перевода сетевых адресов (NAT), которые нужно связать с балансировой нагрузкой.</span><span class="sxs-lookup"><span data-stu-id="46981-133">Specifies a list of inbound network address translation (NAT) rules to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46981-134">-LoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="46981-134">-LoadBalancingRule</span></span>
<span data-ttu-id="46981-135">Список правил балансировки нагрузки, которые нужно связать с балансировчиком нагрузки.</span><span class="sxs-lookup"><span data-stu-id="46981-135">Specifies a list of load balancing rules to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46981-136">-Location</span><span class="sxs-lookup"><span data-stu-id="46981-136">-Location</span></span>
<span data-ttu-id="46981-137">Определяет регион, в котором нужно создать баланс нагрузки.</span><span class="sxs-lookup"><span data-stu-id="46981-137">Specifies the region in which to create a load balancer.</span></span>

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

### <span data-ttu-id="46981-138">-Name</span><span class="sxs-lookup"><span data-stu-id="46981-138">-Name</span></span>
<span data-ttu-id="46981-139">Указывает имя создаемого балансира нагрузки.</span><span class="sxs-lookup"><span data-stu-id="46981-139">Specifies the name of the load balancer that this creates.</span></span>

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

### <span data-ttu-id="46981-140">-OutboundRule</span><span class="sxs-lookup"><span data-stu-id="46981-140">-OutboundRule</span></span>
<span data-ttu-id="46981-141">Правила исходящие.</span><span class="sxs-lookup"><span data-stu-id="46981-141">The outbound rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46981-142">-Разротные</span><span class="sxs-lookup"><span data-stu-id="46981-142">-Probe</span></span>
<span data-ttu-id="46981-143">Определяет список сравниний, которые нужно связать с балансировой нагрузки.</span><span class="sxs-lookup"><span data-stu-id="46981-143">Specifies a list of probes to associate with a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46981-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46981-144">-ResourceGroupName</span></span>
<span data-ttu-id="46981-145">Имя группы ресурсов, в которой нужно создать баланс нагрузки.</span><span class="sxs-lookup"><span data-stu-id="46981-145">Specifies the name of the resource group in which to create a load balancer.</span></span>

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

### <span data-ttu-id="46981-146">-SKU</span><span class="sxs-lookup"><span data-stu-id="46981-146">-Sku</span></span>
<span data-ttu-id="46981-147">Имя SKU балансира нагрузки.</span><span class="sxs-lookup"><span data-stu-id="46981-147">The load balancer Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46981-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="46981-148">-Tag</span></span>
<span data-ttu-id="46981-149">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="46981-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="46981-150">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="46981-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="46981-151">-Tier</span><span class="sxs-lookup"><span data-stu-id="46981-151">-Tier</span></span>
<span data-ttu-id="46981-152">Уровень балансиров нагрузки SKU.</span><span class="sxs-lookup"><span data-stu-id="46981-152">The load balancer Sku Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46981-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46981-153">-Confirm</span></span>
<span data-ttu-id="46981-154">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46981-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46981-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46981-155">-WhatIf</span></span>
<span data-ttu-id="46981-156">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46981-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46981-157">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="46981-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46981-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46981-158">CommonParameters</span></span>
<span data-ttu-id="46981-159">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46981-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46981-160">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46981-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46981-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46981-161">INPUTS</span></span>

### <span data-ttu-id="46981-162">System.String</span><span class="sxs-lookup"><span data-stu-id="46981-162">System.String</span></span>

### <span data-ttu-id="46981-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="46981-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="46981-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="46981-164">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="46981-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span><span class="sxs-lookup"><span data-stu-id="46981-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="46981-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]</span><span class="sxs-lookup"><span data-stu-id="46981-166">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule[]</span></span>

### <span data-ttu-id="46981-167">Microsoft.Azure.Commands.Network.Models.PSProbe[]</span><span class="sxs-lookup"><span data-stu-id="46981-167">Microsoft.Azure.Commands.Network.Models.PSProbe[]</span></span>

### <span data-ttu-id="46981-168">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span><span class="sxs-lookup"><span data-stu-id="46981-168">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="46981-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]</span><span class="sxs-lookup"><span data-stu-id="46981-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool[]</span></span>

### <span data-ttu-id="46981-170">Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]</span><span class="sxs-lookup"><span data-stu-id="46981-170">Microsoft.Azure.Commands.Network.Models.PSOutboundRule[]</span></span>

## <span data-ttu-id="46981-171">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="46981-171">OUTPUTS</span></span>

### <span data-ttu-id="46981-172">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="46981-172">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="46981-173">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="46981-173">NOTES</span></span>

## <span data-ttu-id="46981-174">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46981-174">RELATED LINKS</span></span>

[<span data-ttu-id="46981-175">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="46981-175">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="46981-176">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="46981-176">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="46981-177">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="46981-177">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="46981-178">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="46981-178">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)