---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: adef9e3a2ba0d1e67ee8cb2ec9bdd14d9833f5d7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421676"
---
# <span data-ttu-id="9dd61-101">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9dd61-101">New-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="9dd61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dd61-102">SYNOPSIS</span></span>
<span data-ttu-id="9dd61-103">Создает конфигурацию правила безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="9dd61-103">Creates a network security rule configuration.</span></span>

## <span data-ttu-id="9dd61-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9dd61-104">SYNTAX</span></span>

### <span data-ttu-id="9dd61-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9dd61-105">SetByResource (Default)</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dd61-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9dd61-106">SetByResourceId</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroupId <String[]>]
 [-DestinationApplicationSecurityGroupId <String[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dd61-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9dd61-107">DESCRIPTION</span></span>
<span data-ttu-id="9dd61-108">Командлет **New-AzNetworkSecurityRuleConfig** создает конфигурацию правила безопасности сети Azure для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="9dd61-108">The **New-AzNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="9dd61-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9dd61-109">EXAMPLES</span></span>

### <span data-ttu-id="9dd61-110">Пример 1. Создание правила безопасности сети для разрешение RDP</span><span class="sxs-lookup"><span data-stu-id="9dd61-110">Example 1: Create a network security rule to allow RDP</span></span>
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="9dd61-111">Эта команда создает правило безопасности, разрешающие доступ из Интернета к порту 3389</span><span class="sxs-lookup"><span data-stu-id="9dd61-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="9dd61-112">Пример 2. Создание правила безопасности сети, которое позволяет http</span><span class="sxs-lookup"><span data-stu-id="9dd61-112">Example 2: Create a network security rule that allows HTTP</span></span>
```powershell
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="9dd61-113">Эта команда создает правило безопасности, разрешающие доступ из Интернета к порту 80</span><span class="sxs-lookup"><span data-stu-id="9dd61-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="9dd61-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9dd61-114">PARAMETERS</span></span>

### <span data-ttu-id="9dd61-115">-Access</span><span class="sxs-lookup"><span data-stu-id="9dd61-115">-Access</span></span>
<span data-ttu-id="9dd61-116">Указывает, разрешен или запрещен сетевой трафик.</span><span class="sxs-lookup"><span data-stu-id="9dd61-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="9dd61-117">Для этого параметра можно использовать допустимые значения: Allow (Разрешить) и Deny (Запретить).</span><span class="sxs-lookup"><span data-stu-id="9dd61-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd61-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dd61-118">-DefaultProfile</span></span>
<span data-ttu-id="9dd61-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9dd61-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9dd61-120">-Description</span><span class="sxs-lookup"><span data-stu-id="9dd61-120">-Description</span></span>
<span data-ttu-id="9dd61-121">Описание создаемой конфигурации правила безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="9dd61-121">Specifies a description of the network security rule configuration to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd61-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9dd61-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="9dd61-123">Указывает префикс адреса назначения.</span><span class="sxs-lookup"><span data-stu-id="9dd61-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="9dd61-124">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="9dd61-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9dd61-125">Адрес CIDR CIDR</span><span class="sxs-lookup"><span data-stu-id="9dd61-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="9dd61-126">Диапазон IP-адресов назначения</span><span class="sxs-lookup"><span data-stu-id="9dd61-126">A destination IP address range</span></span> 
- <span data-ttu-id="9dd61-127">Подстановка (\*) для совпадения с ЛЮБЫМ IP-адресом, который можно использовать с такими тегами, как VirtualNetwork, AzureLoadBalancer и Internet.</span><span class="sxs-lookup"><span data-stu-id="9dd61-127">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd61-128">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9dd61-128">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="9dd61-129">Группа безопасности приложений, заемная в качестве назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="9dd61-129">The application security group set as destination for the rule.</span></span> <span data-ttu-id="9dd61-130">Его нельзя использовать с параметром DestinationAddressPrefix.</span><span class="sxs-lookup"><span data-stu-id="9dd61-130">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd61-131">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="9dd61-131">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="9dd61-132">Группа безопасности приложений, заемная в качестве назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="9dd61-132">The application security group set as destination for the rule.</span></span> <span data-ttu-id="9dd61-133">Его нельзя использовать с параметром DestinationAddressPrefix.</span><span class="sxs-lookup"><span data-stu-id="9dd61-133">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd61-134">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="9dd61-134">-DestinationPortRange</span></span>
<span data-ttu-id="9dd61-135">Определяет порт назначения или диапазон.</span><span class="sxs-lookup"><span data-stu-id="9dd61-135">Specifies a destination port or range.</span></span>
<span data-ttu-id="9dd61-136">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="9dd61-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9dd61-137">Integer (Integer)</span><span class="sxs-lookup"><span data-stu-id="9dd61-137">An integer</span></span>
- <span data-ttu-id="9dd61-138">Диапазон от 0 до 65 535</span><span class="sxs-lookup"><span data-stu-id="9dd61-138">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="9dd61-139">Поддиавный знак (\*), который соответствует любому порту</span><span class="sxs-lookup"><span data-stu-id="9dd61-139">A wildcard character (\*) to match any port</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd61-140">-Direction</span><span class="sxs-lookup"><span data-stu-id="9dd61-140">-Direction</span></span>
<span data-ttu-id="9dd61-141">Указывает, следует ли оценивать правило для входящих и исходяющих трафика.</span><span class="sxs-lookup"><span data-stu-id="9dd61-141">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="9dd61-142">Допустимыми значениями для этого параметра являются входящие и исходящие.</span><span class="sxs-lookup"><span data-stu-id="9dd61-142">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd61-143">-Name</span><span class="sxs-lookup"><span data-stu-id="9dd61-143">-Name</span></span>
<span data-ttu-id="9dd61-144">Указывает имя конфигурации правила безопасности сети, которую создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dd61-144">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9dd61-145">-Priority</span><span class="sxs-lookup"><span data-stu-id="9dd61-145">-Priority</span></span>
<span data-ttu-id="9dd61-146">Определяет приоритет конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="9dd61-146">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="9dd61-147">Допустимыми значениями для этого параметра являются: integer between 100–4096.</span><span class="sxs-lookup"><span data-stu-id="9dd61-147">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="9dd61-148">Номер приоритета должен быть уникальным для каждого правила в коллекции.</span><span class="sxs-lookup"><span data-stu-id="9dd61-148">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="9dd61-149">Чем ниже номер приоритета, тем выше приоритет правила.</span><span class="sxs-lookup"><span data-stu-id="9dd61-149">The lower the priority number, the higher the priority of the rule.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd61-150">-Protocol</span><span class="sxs-lookup"><span data-stu-id="9dd61-150">-Protocol</span></span>
<span data-ttu-id="9dd61-151">Определяет сетевой протокол, к который применяется новая конфигурация правила.</span><span class="sxs-lookup"><span data-stu-id="9dd61-151">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="9dd61-152">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="9dd61-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9dd61-153">Tcp</span><span class="sxs-lookup"><span data-stu-id="9dd61-153">Tcp</span></span>
- <span data-ttu-id="9dd61-154">Udp</span><span class="sxs-lookup"><span data-stu-id="9dd61-154">Udp</span></span>
- <span data-ttu-id="9dd61-155">поддиавный знак (\*), который соответствует обоим.</span><span class="sxs-lookup"><span data-stu-id="9dd61-155">wildcard character (\*) to match both.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd61-156">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9dd61-156">-SourceAddressPrefix</span></span>
<span data-ttu-id="9dd61-157">Указывает префикс для исходных адресов.</span><span class="sxs-lookup"><span data-stu-id="9dd61-157">Specifies a source address prefix.</span></span>
<span data-ttu-id="9dd61-158">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="9dd61-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9dd61-159">A CIDR</span><span class="sxs-lookup"><span data-stu-id="9dd61-159">A CIDR</span></span>
- <span data-ttu-id="9dd61-160">Диапазон IP-адресов источника</span><span class="sxs-lookup"><span data-stu-id="9dd61-160">A source IP range</span></span>
- <span data-ttu-id="9dd61-161">Поддиавный знак (\*), который соответствует любому IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="9dd61-161">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="9dd61-162">Вы также можете использовать такие теги, как VirtualNetwork, AzureLoadBalancer и Internet.</span><span class="sxs-lookup"><span data-stu-id="9dd61-162">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd61-163">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9dd61-163">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="9dd61-164">Группа безопасности приложений, заемная в качестве источника для правила.</span><span class="sxs-lookup"><span data-stu-id="9dd61-164">The application security group set as source for the rule.</span></span> <span data-ttu-id="9dd61-165">Его нельзя использовать с параметром SourceAddressPrefix.</span><span class="sxs-lookup"><span data-stu-id="9dd61-165">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd61-166">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="9dd61-166">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="9dd61-167">Группа безопасности приложений, заемная в качестве источника для правила.</span><span class="sxs-lookup"><span data-stu-id="9dd61-167">The application security group set as source for the rule.</span></span> <span data-ttu-id="9dd61-168">Его нельзя использовать с параметром SourceAddressPrefix.</span><span class="sxs-lookup"><span data-stu-id="9dd61-168">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd61-169">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="9dd61-169">-SourcePortRange</span></span>
<span data-ttu-id="9dd61-170">Определяет исходный порт или диапазон.</span><span class="sxs-lookup"><span data-stu-id="9dd61-170">Specifies the source port or range.</span></span>
<span data-ttu-id="9dd61-171">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="9dd61-171">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9dd61-172">Integer (Integer)</span><span class="sxs-lookup"><span data-stu-id="9dd61-172">An integer</span></span>
- <span data-ttu-id="9dd61-173">Диапазон от 0 до 65 535</span><span class="sxs-lookup"><span data-stu-id="9dd61-173">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="9dd61-174">Поддиавный знак (\*), который соответствует любому порту</span><span class="sxs-lookup"><span data-stu-id="9dd61-174">A wildcard character (\*) to match any port</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dd61-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dd61-175">CommonParameters</span></span>
<span data-ttu-id="9dd61-176">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dd61-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dd61-177">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dd61-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dd61-178">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9dd61-178">INPUTS</span></span>

### <span data-ttu-id="9dd61-179">Нет</span><span class="sxs-lookup"><span data-stu-id="9dd61-179">None</span></span>

## <span data-ttu-id="9dd61-180">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9dd61-180">OUTPUTS</span></span>

### <span data-ttu-id="9dd61-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="9dd61-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="9dd61-182">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9dd61-182">NOTES</span></span>

## <span data-ttu-id="9dd61-183">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9dd61-183">RELATED LINKS</span></span>

[<span data-ttu-id="9dd61-184">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9dd61-184">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9dd61-185">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9dd61-185">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9dd61-186">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9dd61-186">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9dd61-187">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9dd61-187">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

