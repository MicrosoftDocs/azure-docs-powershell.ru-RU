---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: d2508b233bc67cb49d0a1c525f7e43ccf07242b2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421684"
---
# <span data-ttu-id="1c025-101">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1c025-101">New-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="1c025-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c025-102">SYNOPSIS</span></span>
<span data-ttu-id="1c025-103">Создает конфигурацию правила NAT для балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="1c025-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="1c025-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1c025-104">SYNTAX</span></span>

### <span data-ttu-id="1c025-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1c025-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c025-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1c025-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1c025-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c025-107">DESCRIPTION</span></span>
<span data-ttu-id="1c025-108">Для балансиров нагрузки Azure с его использованием создается конфигурация правила перевода сетевых адресов (NAT) **new-AzLoadBalancerInboundNatRuleConfig.**</span><span class="sxs-lookup"><span data-stu-id="1c025-108">The **New-AzLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="1c025-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1c025-109">EXAMPLES</span></span>

### <span data-ttu-id="1c025-110">Пример 1. Создание конфигурации входящие правила NAT для балансиров нагрузки</span><span class="sxs-lookup"><span data-stu-id="1c025-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="1c025-111">Первая команда создает общедоступный IP-адрес MyPublicIP в группе ресурсов MyResourceGroup, а затем сохраняет его в переменной $publicip.</span><span class="sxs-lookup"><span data-stu-id="1c025-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="1c025-112">Вторая команда создает конфигурацию переднего IP-адреса с именем FrontendIpConfig01, используя общедоступный IP-адрес в $publicip, а затем сохраняет ее в переменной $frontend.</span><span class="sxs-lookup"><span data-stu-id="1c025-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="1c025-113">Третья команда создает конфигурацию входящие правила NAT с именем MyInboundNatRule с использованием переднего объекта в $frontend.</span><span class="sxs-lookup"><span data-stu-id="1c025-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="1c025-114">Задан протокол TCP, а на переднем — 3389.</span><span class="sxs-lookup"><span data-stu-id="1c025-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="1c025-115">Параметры *FrontendIpConfiguration,* *Protocol,* *FrontendPort* и *BackendPort* необходимы для создания конфигурации правила NAT входящие.</span><span class="sxs-lookup"><span data-stu-id="1c025-115">The *FrontendIpConfiguration*, *Protocol*, *FrontendPort*, and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="1c025-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c025-116">PARAMETERS</span></span>

### <span data-ttu-id="1c025-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="1c025-117">-BackendPort</span></span>
<span data-ttu-id="1c025-118">Определяет порт для трафика, на который совме задана конфигурация правила.</span><span class="sxs-lookup"><span data-stu-id="1c025-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c025-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c025-119">-DefaultProfile</span></span>
<span data-ttu-id="1c025-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1c025-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c025-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="1c025-121">-EnableFloatingIP</span></span>
<span data-ttu-id="1c025-122">Указывает на то, что этот cmdlet включает плавающий IP-адрес для настройки правил.</span><span class="sxs-lookup"><span data-stu-id="1c025-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="1c025-123">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="1c025-123">-EnableTcpReset</span></span>
<span data-ttu-id="1c025-124">Получение перенаправленного TCP-сброса при неавторяемом времени ожидания потока TCP или о непредвиде приостановке подключения.</span><span class="sxs-lookup"><span data-stu-id="1c025-124">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="1c025-125">Этот элемент используется только в том случае, если протокол имеет протокол TCP.</span><span class="sxs-lookup"><span data-stu-id="1c025-125">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="1c025-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c025-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="1c025-127">Список IP-адресов, которые нужно связать с конфигурацией правил балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="1c025-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c025-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="1c025-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="1c025-129">Определяет ID конфигурации переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="1c025-129">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c025-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="1c025-130">-FrontendPort</span></span>
<span data-ttu-id="1c025-131">Указывает порт переднего адреса, который соответствует конфигурации правил балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="1c025-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c025-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="1c025-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="1c025-133">Определяет продолжительность бесед (в минутах), в течение которых состояние бесед сохраняется на балансе нагрузки.</span><span class="sxs-lookup"><span data-stu-id="1c025-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c025-134">-Name</span><span class="sxs-lookup"><span data-stu-id="1c025-134">-Name</span></span>
<span data-ttu-id="1c025-135">Указывает имя конфигурации правила, которую создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c025-135">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="1c025-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="1c025-136">-Protocol</span></span>
<span data-ttu-id="1c025-137">Протокол.</span><span class="sxs-lookup"><span data-stu-id="1c025-137">Specifies a protocol.</span></span>
<span data-ttu-id="1c025-138">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="1c025-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1c025-139">Tcp</span><span class="sxs-lookup"><span data-stu-id="1c025-139">Tcp</span></span>
- <span data-ttu-id="1c025-140">Udp</span><span class="sxs-lookup"><span data-stu-id="1c025-140">Udp</span></span>

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

### <span data-ttu-id="1c025-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c025-141">-Confirm</span></span>
<span data-ttu-id="1c025-142">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c025-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c025-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c025-143">-WhatIf</span></span>
<span data-ttu-id="1c025-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c025-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c025-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1c025-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c025-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c025-146">CommonParameters</span></span>
<span data-ttu-id="1c025-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c025-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c025-148">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c025-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c025-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c025-149">INPUTS</span></span>

### <span data-ttu-id="1c025-150">System.String</span><span class="sxs-lookup"><span data-stu-id="1c025-150">System.String</span></span>

### <span data-ttu-id="1c025-151">System.Int32</span><span class="sxs-lookup"><span data-stu-id="1c025-151">System.Int32</span></span>

### <span data-ttu-id="1c025-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c025-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="1c025-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1c025-153">OUTPUTS</span></span>

### <span data-ttu-id="1c025-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="1c025-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="1c025-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1c025-155">NOTES</span></span>

## <span data-ttu-id="1c025-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c025-156">RELATED LINKS</span></span>

[<span data-ttu-id="1c025-157">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1c025-157">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="1c025-158">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1c025-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="1c025-159">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1c025-159">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="1c025-160">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1c025-160">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="1c025-161">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1c025-161">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="1c025-162">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1c025-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)

