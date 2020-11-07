---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: e30a03f82d0bcf719ffc4dc5640e3fbf9b3bb99f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567568"
---
# <span data-ttu-id="3d576-101">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3d576-101">New-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="3d576-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d576-102">SYNOPSIS</span></span>
<span data-ttu-id="3d576-103">Создание конфигурации правила сетевой безопасности.</span><span class="sxs-lookup"><span data-stu-id="3d576-103">Creates a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d576-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d576-104">SYNTAX</span></span>

### <span data-ttu-id="3d576-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3d576-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d576-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3d576-106">SetByResourceId</span></span>
```
New-AzureRmNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d576-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d576-107">DESCRIPTION</span></span>
<span data-ttu-id="3d576-108">Командлет **New-AzureRmNetworkSecurityRuleConfig** создает конфигурацию правила сетевой безопасности Azure для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="3d576-108">The **New-AzureRmNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="3d576-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d576-109">EXAMPLES</span></span>

### <span data-ttu-id="3d576-110">1: Создание правила сетевой безопасности, разрешающее RDP</span><span class="sxs-lookup"><span data-stu-id="3d576-110">1: Create a network security rule to allow RDP</span></span>
```
$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="3d576-111">Эта команда создает правило безопасности, позволяющее доступ из Интернета к порту 3389</span><span class="sxs-lookup"><span data-stu-id="3d576-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="3d576-112">2. Создание правила сетевой безопасности, разрешающего HTTP</span><span class="sxs-lookup"><span data-stu-id="3d576-112">2: Create a network security rule that allows HTTP</span></span>
```
$rule2 = New-AzureRmNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="3d576-113">Эта команда создает правило безопасности, позволяющее доступ из Интернета к порту 80</span><span class="sxs-lookup"><span data-stu-id="3d576-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="3d576-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d576-114">PARAMETERS</span></span>

### <span data-ttu-id="3d576-115">-Доступ</span><span class="sxs-lookup"><span data-stu-id="3d576-115">-Access</span></span>
<span data-ttu-id="3d576-116">Указывает, разрешен ли сетевой трафик или нет.</span><span class="sxs-lookup"><span data-stu-id="3d576-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="3d576-117">Допустимые значения этого параметра: allow и Deny.</span><span class="sxs-lookup"><span data-stu-id="3d576-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="3d576-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d576-118">-DefaultProfile</span></span>
<span data-ttu-id="3d576-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3d576-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d576-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="3d576-120">-Description</span></span>
<span data-ttu-id="3d576-121">Задает описание конфигурации правила сетевой безопасности для создания.</span><span class="sxs-lookup"><span data-stu-id="3d576-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="3d576-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3d576-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="3d576-123">Указывает префикс адреса назначения.</span><span class="sxs-lookup"><span data-stu-id="3d576-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="3d576-124">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3d576-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3d576-125">Неклассовый адрес междоменной маршрутизации (CIDR)</span><span class="sxs-lookup"><span data-stu-id="3d576-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="3d576-126">Диапазон IP-адресов назначения</span><span class="sxs-lookup"><span data-stu-id="3d576-126">A destination IP address range</span></span> 
- <span data-ttu-id="3d576-127">Подстановочный знак (\*) для поиска соответствия любому IP-адресу</span><span class="sxs-lookup"><span data-stu-id="3d576-127">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="3d576-128">Вы можете использовать теги, например VirtualNetwork, AzureLoadBalancer и Интернет.</span><span class="sxs-lookup"><span data-stu-id="3d576-128">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d576-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3d576-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="3d576-130">Группа безопасности приложения, установленная в качестве назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="3d576-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="3d576-131">Его нельзя использовать с параметром "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="3d576-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d576-132">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="3d576-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="3d576-133">Группа безопасности приложения, установленная в качестве назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="3d576-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="3d576-134">Его нельзя использовать с параметром "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="3d576-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d576-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="3d576-135">-DestinationPortRange</span></span>
<span data-ttu-id="3d576-136">Указывает конечный порт или диапазон.</span><span class="sxs-lookup"><span data-stu-id="3d576-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="3d576-137">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3d576-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3d576-138">Целое число</span><span class="sxs-lookup"><span data-stu-id="3d576-138">An integer</span></span>
- <span data-ttu-id="3d576-139">Диапазон целочисленных значений от 0 до 65535</span><span class="sxs-lookup"><span data-stu-id="3d576-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="3d576-140">Подстановочный знак (\*) для соответствия любому порту</span><span class="sxs-lookup"><span data-stu-id="3d576-140">A wildcard character (\*) to match any port</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d576-141">-Направление</span><span class="sxs-lookup"><span data-stu-id="3d576-141">-Direction</span></span>
<span data-ttu-id="3d576-142">Указывает, оценивается ли правило для входящего и исходящего трафика.</span><span class="sxs-lookup"><span data-stu-id="3d576-142">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="3d576-143">Допустимые значения этого параметра: входящие и исходящие.</span><span class="sxs-lookup"><span data-stu-id="3d576-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="3d576-144">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3d576-144">-Name</span></span>
<span data-ttu-id="3d576-145">Указывает имя конфигурации правила сетевой безопасности, создаваемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="3d576-145">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="3d576-146">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="3d576-146">-Priority</span></span>
<span data-ttu-id="3d576-147">Задает приоритет конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="3d576-147">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="3d576-148">Допустимые значения этого параметра: целое число между 100 и 4096.</span><span class="sxs-lookup"><span data-stu-id="3d576-148">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>

<span data-ttu-id="3d576-149">Номер приоритета должен быть уникальным для каждого правила в коллекции.</span><span class="sxs-lookup"><span data-stu-id="3d576-149">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="3d576-150">Чем меньше номер приоритета, тем выше приоритет правила.</span><span class="sxs-lookup"><span data-stu-id="3d576-150">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="3d576-151">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="3d576-151">-Protocol</span></span>
<span data-ttu-id="3d576-152">Указывает сетевой протокол, к которому применяется новая конфигурация правила.</span><span class="sxs-lookup"><span data-stu-id="3d576-152">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="3d576-153">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3d576-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3d576-154">Номера</span><span class="sxs-lookup"><span data-stu-id="3d576-154">Tcp</span></span>
- <span data-ttu-id="3d576-155">Трафика</span><span class="sxs-lookup"><span data-stu-id="3d576-155">Udp</span></span>
- <span data-ttu-id="3d576-156">подстановочный знак (\*) для поиска соответствия обоим.</span><span class="sxs-lookup"><span data-stu-id="3d576-156">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="3d576-157">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="3d576-157">-SourceAddressPrefix</span></span>
<span data-ttu-id="3d576-158">Указывает префикс исходного адреса.</span><span class="sxs-lookup"><span data-stu-id="3d576-158">Specifies a source address prefix.</span></span>
<span data-ttu-id="3d576-159">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3d576-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3d576-160">CIDR</span><span class="sxs-lookup"><span data-stu-id="3d576-160">A CIDR</span></span>
- <span data-ttu-id="3d576-161">Диапазон IP-адресов источника</span><span class="sxs-lookup"><span data-stu-id="3d576-161">A source IP range</span></span>
- <span data-ttu-id="3d576-162">Подстановочный знак (\*) для соответствия любому IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="3d576-162">A wildcard character (\*) to match any IP address.</span></span>

<span data-ttu-id="3d576-163">Вы также можете использовать теги, например VirtualNetwork, AzureLoadBalancer и Интернет.</span><span class="sxs-lookup"><span data-stu-id="3d576-163">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d576-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3d576-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="3d576-165">Группа безопасности приложения, установленная как источник для правила.</span><span class="sxs-lookup"><span data-stu-id="3d576-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="3d576-166">Его нельзя использовать с параметром "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="3d576-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d576-167">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="3d576-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="3d576-168">Группа безопасности приложения, установленная как источник для правила.</span><span class="sxs-lookup"><span data-stu-id="3d576-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="3d576-169">Его нельзя использовать с параметром "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="3d576-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d576-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="3d576-170">-SourcePortRange</span></span>
<span data-ttu-id="3d576-171">Указывает исходный порт или диапазон.</span><span class="sxs-lookup"><span data-stu-id="3d576-171">Specifies the source port or range.</span></span>
<span data-ttu-id="3d576-172">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3d576-172">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3d576-173">Целое число</span><span class="sxs-lookup"><span data-stu-id="3d576-173">An integer</span></span>
- <span data-ttu-id="3d576-174">Диапазон целочисленных значений от 0 до 65535</span><span class="sxs-lookup"><span data-stu-id="3d576-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="3d576-175">Подстановочный знак (\*) для соответствия любому порту</span><span class="sxs-lookup"><span data-stu-id="3d576-175">A wildcard character (\*) to match any port</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d576-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d576-176">CommonParameters</span></span>
<span data-ttu-id="3d576-177">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d576-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d576-178">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d576-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d576-179">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d576-179">INPUTS</span></span>

## <span data-ttu-id="3d576-180">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d576-180">OUTPUTS</span></span>

### <span data-ttu-id="3d576-181">Microsoft. Azure. Commands. Network. Models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="3d576-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="3d576-182">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d576-182">NOTES</span></span>

## <span data-ttu-id="3d576-183">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d576-183">RELATED LINKS</span></span>

[<span data-ttu-id="3d576-184">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3d576-184">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3d576-185">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3d576-185">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3d576-186">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3d576-186">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3d576-187">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3d576-187">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

