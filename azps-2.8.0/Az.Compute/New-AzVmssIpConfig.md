---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: 271d4c9d9fd4a7eb34d4ced4b32dc3929a32b31b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721814"
---
# <span data-ttu-id="3bedd-101">New-AzVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="3bedd-101">New-AzVmssIpConfig</span></span>

## <span data-ttu-id="3bedd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3bedd-102">SYNOPSIS</span></span>
<span data-ttu-id="3bedd-103">Создание IP-конфигурации для сетевого интерфейса VMSS.</span><span class="sxs-lookup"><span data-stu-id="3bedd-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

## <span data-ttu-id="3bedd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3bedd-104">SYNTAX</span></span>

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bedd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3bedd-105">DESCRIPTION</span></span>
<span data-ttu-id="3bedd-106">Командлет **New-AzVmssIpConfig** создает объект конфигурации IP для сетевого интерфейса набора масштабирования виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="3bedd-106">The **New-AzVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="3bedd-107">Укажите конфигурацию из этого командлета в качестве параметра *IP* для командлета Add-AzVmssNetworkInterfaceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3bedd-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="3bedd-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3bedd-108">EXAMPLES</span></span>

### <span data-ttu-id="3bedd-109">Пример 1: создание объекта конфигурации IP для интерфейса VMSS</span><span class="sxs-lookup"><span data-stu-id="3bedd-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="3bedd-110">Эта команда создает объект конфигурации IP с именем ContosoVmssInterface02.</span><span class="sxs-lookup"><span data-stu-id="3bedd-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="3bedd-111">В команде используется ранее определенный идентификатор подсети, хранящийся в $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="3bedd-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="3bedd-112">Команда сохраняет параметры конфигурации в переменной $IPConfiguration для последующего использования с помощью **Add-AzVmssNetworkInterfaceConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="3bedd-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="3bedd-113">Пример 2: создание объекта конфигурации IP, включающего параметры пула NAT</span><span class="sxs-lookup"><span data-stu-id="3bedd-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="3bedd-114">Эта команда создает объект конфигурации IP с именем ContosoVmssInterface03 и сохраняет его в переменной $IPConfiguration для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="3bedd-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="3bedd-115">В команде используется ранее определенный идентификатор подсети, хранящийся в $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="3bedd-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="3bedd-116">Команда сохраняет параметры конфигурации в переменной $IPConfiguration для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="3bedd-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="3bedd-117">Команда задает значения для параметров *LoadBalancerInboundNatPoolsId* и *LoadBalancerBackendAddressPoolsId* .</span><span class="sxs-lookup"><span data-stu-id="3bedd-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="3bedd-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3bedd-118">PARAMETERS</span></span>

### <span data-ttu-id="3bedd-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="3bedd-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="3bedd-120">Указывает массив ссылок на серверные пулы адресных пулов подсистем балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="3bedd-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="3bedd-121">Набор масштабов может ссылаться на пулы серверных адресов одного открытого и одного внутреннего подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="3bedd-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="3bedd-122">Несколько наборов масштабов не могут использовать одну и ту же подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="3bedd-122">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bedd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bedd-123">-DefaultProfile</span></span>
<span data-ttu-id="3bedd-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3bedd-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bedd-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="3bedd-125">-DnsSetting</span></span>
<span data-ttu-id="3bedd-126">Параметры DNS, применяемые к адресам publicIP.</span><span class="sxs-lookup"><span data-stu-id="3bedd-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="3bedd-127">Метка доменного имени параметров DNS, которые будут применяться к publicIP адресам.</span><span class="sxs-lookup"><span data-stu-id="3bedd-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="3bedd-128">Объединение метки доменного имени и индекса ВМ — это метки доменных имен ресурсов общедоступного IP-адреса, которые будут созданы.</span><span class="sxs-lookup"><span data-stu-id="3bedd-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bedd-129">-ID</span><span class="sxs-lookup"><span data-stu-id="3bedd-129">-Id</span></span>
<span data-ttu-id="3bedd-130">Указывает идентификатор.</span><span class="sxs-lookup"><span data-stu-id="3bedd-130">Specifies an ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bedd-131">-IpTag</span><span class="sxs-lookup"><span data-stu-id="3bedd-131">-IpTag</span></span>
<span data-ttu-id="3bedd-132">Указывает массив объектов IP-тегов.</span><span class="sxs-lookup"><span data-stu-id="3bedd-132">Specifies an array of Ip Tag objects.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bedd-133">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="3bedd-133">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="3bedd-134">Задает массив ссылок на пулы NAT для подсистем балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="3bedd-134">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="3bedd-135">Набор масштабов может ссылаться на входящие пулы NAT для одной открытой и одной внутренней подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="3bedd-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="3bedd-136">Несколько наборов масштабов не могут использовать одну и ту же подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="3bedd-136">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bedd-137">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="3bedd-137">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="3bedd-138">Указывает массив ссылок на входящие пулы NAT для подсистем балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="3bedd-138">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="3bedd-139">Набор масштабов может ссылаться на входящие пулы NAT для одной открытой и одной внутренней подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="3bedd-139">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="3bedd-140">Несколько наборов масштабов не могут использовать одну и ту же подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="3bedd-140">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bedd-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3bedd-141">-Name</span></span>
<span data-ttu-id="3bedd-142">Указывает имя конфигурации IP.</span><span class="sxs-lookup"><span data-stu-id="3bedd-142">Specifies the name of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bedd-143">-Primary</span><span class="sxs-lookup"><span data-stu-id="3bedd-143">-Primary</span></span>
<span data-ttu-id="3bedd-144">Определяет основную конфигурацию IP-адреса в случае, если сетевой интерфейс имеет несколько конфигураций IP.</span><span class="sxs-lookup"><span data-stu-id="3bedd-144">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

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

### <span data-ttu-id="3bedd-145">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="3bedd-145">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="3bedd-146">Укажите IP-конфигурацию: либо IPv4, либо IPv6.</span><span class="sxs-lookup"><span data-stu-id="3bedd-146">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="3bedd-147">По умолчанию используется протокол IPv4.</span><span class="sxs-lookup"><span data-stu-id="3bedd-147">Default is taken as IPv4.</span></span>  <span data-ttu-id="3bedd-148">Возможные значения: "IPv4" и "IPv6".</span><span class="sxs-lookup"><span data-stu-id="3bedd-148">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="3bedd-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="3bedd-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="3bedd-150">Таймаут простоя общего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="3bedd-150">The idle timeout of the public IP address.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bedd-151">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3bedd-151">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="3bedd-152">Имя конфигурации адреса publicIP.</span><span class="sxs-lookup"><span data-stu-id="3bedd-152">The publicIP address configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bedd-153">-PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="3bedd-153">-PublicIPPrefix</span></span>
<span data-ttu-id="3bedd-154">Идентификатор префикса общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="3bedd-154">The ID of Public IP Prefix</span></span>

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

### <span data-ttu-id="3bedd-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="3bedd-155">-SubnetId</span></span>
<span data-ttu-id="3bedd-156">Указывает идентификатор подсети, в котором конфигурация создает сетевой интерфейс VMSS.</span><span class="sxs-lookup"><span data-stu-id="3bedd-156">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bedd-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3bedd-157">-Confirm</span></span>
<span data-ttu-id="3bedd-158">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3bedd-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bedd-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bedd-159">-WhatIf</span></span>
<span data-ttu-id="3bedd-160">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3bedd-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3bedd-161">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3bedd-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bedd-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bedd-162">CommonParameters</span></span>
<span data-ttu-id="3bedd-163">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3bedd-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bedd-164">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3bedd-164">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bedd-165">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3bedd-165">INPUTS</span></span>

### <span data-ttu-id="3bedd-166">System. String</span><span class="sxs-lookup"><span data-stu-id="3bedd-166">System.String</span></span>

### <span data-ttu-id="3bedd-167">System. String []</span><span class="sxs-lookup"><span data-stu-id="3bedd-167">System.String[]</span></span>

### <span data-ttu-id="3bedd-168">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3bedd-168">System.Int32</span></span>

### <span data-ttu-id="3bedd-169">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetIpTag []</span><span class="sxs-lookup"><span data-stu-id="3bedd-169">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span></span>

## <span data-ttu-id="3bedd-170">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3bedd-170">OUTPUTS</span></span>

### <span data-ttu-id="3bedd-171">Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3bedd-171">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="3bedd-172">Пуск</span><span class="sxs-lookup"><span data-stu-id="3bedd-172">NOTES</span></span>

## <span data-ttu-id="3bedd-173">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3bedd-173">RELATED LINKS</span></span>

[<span data-ttu-id="3bedd-174">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="3bedd-174">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

