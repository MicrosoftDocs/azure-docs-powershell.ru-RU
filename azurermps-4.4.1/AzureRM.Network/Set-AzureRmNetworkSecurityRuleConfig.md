---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: fa1416d7bd65236d3a4e1198d6f70efb1a860985
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562407"
---
# <span data-ttu-id="0d33d-101">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0d33d-101">Set-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="0d33d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d33d-102">SYNOPSIS</span></span>
<span data-ttu-id="0d33d-103">Задает состояние цели для конфигурации правила сетевой безопасности.</span><span class="sxs-lookup"><span data-stu-id="0d33d-103">Sets the goal state for a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d33d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d33d-104">SYNTAX</span></span>

### <span data-ttu-id="0d33d-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0d33d-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d33d-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0d33d-106">SetByResourceId</span></span>
```
Set-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d33d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d33d-107">DESCRIPTION</span></span>
<span data-ttu-id="0d33d-108">Командлет **Set-AzureRmNetworkSecurityRuleConfig** задает состояние цели для конфигурации правила сетевой безопасности Azure.</span><span class="sxs-lookup"><span data-stu-id="0d33d-108">The **Set-AzureRmNetworkSecurityRuleConfig** cmdlet sets the goal state for an Azure network security rule configuration.</span></span>

## <span data-ttu-id="0d33d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d33d-109">EXAMPLES</span></span>

### <span data-ttu-id="0d33d-110">Пример 1: изменение конфигурации доступа в правиле сетевой безопасности</span><span class="sxs-lookup"><span data-stu-id="0d33d-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="0d33d-111">Первая команда получает сетевую группу безопасности с именем NSG-интерфейс и сохраняет ее в переменной $nsg.</span><span class="sxs-lookup"><span data-stu-id="0d33d-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>

<span data-ttu-id="0d33d-112">Вторая команда использует оператор Pipeline для передачи группы безопасности в $nsg на Get-AzureRmNetworkSecurityRuleConfig, который получает конфигурацию правила безопасности с именем RDP-Rule.</span><span class="sxs-lookup"><span data-stu-id="0d33d-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzureRmNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>

<span data-ttu-id="0d33d-113">Третья команда изменяет конфигурацию доступа RDP-правила на "запретить".</span><span class="sxs-lookup"><span data-stu-id="0d33d-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="0d33d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d33d-114">PARAMETERS</span></span>

### <span data-ttu-id="0d33d-115">-Доступ</span><span class="sxs-lookup"><span data-stu-id="0d33d-115">-Access</span></span>
<span data-ttu-id="0d33d-116">Указывает, разрешен ли сетевой трафик или нет.</span><span class="sxs-lookup"><span data-stu-id="0d33d-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="0d33d-117">Допустимые значения этого параметра: allow и Deny.</span><span class="sxs-lookup"><span data-stu-id="0d33d-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="0d33d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d33d-118">-DefaultProfile</span></span>
<span data-ttu-id="0d33d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d33d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d33d-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="0d33d-120">-Description</span></span>
<span data-ttu-id="0d33d-121">Задает описание конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="0d33d-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="0d33d-122">Максимальный размер — 140 символов.</span><span class="sxs-lookup"><span data-stu-id="0d33d-122">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="0d33d-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0d33d-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="0d33d-124">Указывает префикс адреса назначения.</span><span class="sxs-lookup"><span data-stu-id="0d33d-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="0d33d-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0d33d-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0d33d-126">Неклассовый адрес междоменной маршрутизации (CIDR)</span><span class="sxs-lookup"><span data-stu-id="0d33d-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="0d33d-127">Диапазон IP-адресов назначения</span><span class="sxs-lookup"><span data-stu-id="0d33d-127">A destination IP address range</span></span> 
- <span data-ttu-id="0d33d-128">Подстановочный знак (\*) для поиска соответствия любому IP-адресу</span><span class="sxs-lookup"><span data-stu-id="0d33d-128">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="0d33d-129">Вы можете использовать теги, например VirtualNetwork, AzureLoadBalancer и Интернет.</span><span class="sxs-lookup"><span data-stu-id="0d33d-129">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="0d33d-130">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0d33d-130">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="0d33d-131">Группа безопасности приложения, установленная в качестве назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="0d33d-131">The application security group set as destination for the rule.</span></span> <span data-ttu-id="0d33d-132">Его нельзя использовать с параметром "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="0d33d-132">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="0d33d-133">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="0d33d-133">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="0d33d-134">Группа безопасности приложения, установленная в качестве назначения для правила.</span><span class="sxs-lookup"><span data-stu-id="0d33d-134">The application security group set as destination for the rule.</span></span> <span data-ttu-id="0d33d-135">Его нельзя использовать с параметром "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="0d33d-135">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="0d33d-136">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="0d33d-136">-DestinationPortRange</span></span>
<span data-ttu-id="0d33d-137">Указывает конечный порт или диапазон.</span><span class="sxs-lookup"><span data-stu-id="0d33d-137">Specifies a destination port or range.</span></span>
<span data-ttu-id="0d33d-138">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0d33d-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0d33d-139">Целое число</span><span class="sxs-lookup"><span data-stu-id="0d33d-139">An integer</span></span> 
- <span data-ttu-id="0d33d-140">Диапазон целочисленных значений от 0 до 65535</span><span class="sxs-lookup"><span data-stu-id="0d33d-140">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="0d33d-141">Подстановочный знак (\*) для соответствия любому порту</span><span class="sxs-lookup"><span data-stu-id="0d33d-141">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="0d33d-142">-Направление</span><span class="sxs-lookup"><span data-stu-id="0d33d-142">-Direction</span></span>
<span data-ttu-id="0d33d-143">Указывает, оценивается ли правило для входящего и исходящего трафика.</span><span class="sxs-lookup"><span data-stu-id="0d33d-143">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="0d33d-144">Допустимые значения этого параметра: входящие и исходящие.</span><span class="sxs-lookup"><span data-stu-id="0d33d-144">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="0d33d-145">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0d33d-145">-Name</span></span>
<span data-ttu-id="0d33d-146">Указывает имя конфигурации правила сетевой безопасности, которую задает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0d33d-146">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="0d33d-147">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0d33d-147">-NetworkSecurityGroup</span></span>
<span data-ttu-id="0d33d-148">Указывает объект **NetworkSecurityGroup** , содержащий конфигурацию правила сетевой безопасности, которую нужно задать.</span><span class="sxs-lookup"><span data-stu-id="0d33d-148">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d33d-149">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="0d33d-149">-Priority</span></span>
<span data-ttu-id="0d33d-150">Задает приоритет конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="0d33d-150">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="0d33d-151">Допустимые значения этого параметра: целое число между 100 и 4096.</span><span class="sxs-lookup"><span data-stu-id="0d33d-151">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>

<span data-ttu-id="0d33d-152">Номер приоритета должен быть уникальным для каждого правила в коллекции.</span><span class="sxs-lookup"><span data-stu-id="0d33d-152">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="0d33d-153">Чем меньше номер приоритета, тем выше приоритет правила.</span><span class="sxs-lookup"><span data-stu-id="0d33d-153">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="0d33d-154">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="0d33d-154">-Protocol</span></span>
<span data-ttu-id="0d33d-155">Указывает сетевой протокол, к которому применяется конфигурация правила.</span><span class="sxs-lookup"><span data-stu-id="0d33d-155">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="0d33d-156">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0d33d-156">The acceptable values for this parameter are:</span></span>

 <span data-ttu-id="0d33d-157">--TCP</span><span class="sxs-lookup"><span data-stu-id="0d33d-157">--Tcp</span></span>
- <span data-ttu-id="0d33d-158">Трафика</span><span class="sxs-lookup"><span data-stu-id="0d33d-158">Udp</span></span>
- <span data-ttu-id="0d33d-159">Подстановочный знак (\*) для поиска соответствия обоим</span><span class="sxs-lookup"><span data-stu-id="0d33d-159">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="0d33d-160">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0d33d-160">-SourceAddressPrefix</span></span>
<span data-ttu-id="0d33d-161">Указывает префикс исходного адреса.</span><span class="sxs-lookup"><span data-stu-id="0d33d-161">Specifies a source address prefix.</span></span>
<span data-ttu-id="0d33d-162">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0d33d-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0d33d-163">CIDR</span><span class="sxs-lookup"><span data-stu-id="0d33d-163">A CIDR</span></span>
- <span data-ttu-id="0d33d-164">Диапазон IP-адресов источника</span><span class="sxs-lookup"><span data-stu-id="0d33d-164">A source IP range</span></span>
- <span data-ttu-id="0d33d-165">Подстановочный знак (\*) для поиска соответствия любому IP-адресу</span><span class="sxs-lookup"><span data-stu-id="0d33d-165">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="0d33d-166">Вы также можете использовать теги, например VirtualNetwork, AzureLoadBalancer и Интернет.</span><span class="sxs-lookup"><span data-stu-id="0d33d-166">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="0d33d-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0d33d-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="0d33d-168">Группа безопасности приложения, установленная как источник для правила.</span><span class="sxs-lookup"><span data-stu-id="0d33d-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="0d33d-169">Его нельзя использовать с параметром "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="0d33d-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="0d33d-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="0d33d-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="0d33d-171">Группа безопасности приложения, установленная как источник для правила.</span><span class="sxs-lookup"><span data-stu-id="0d33d-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="0d33d-172">Его нельзя использовать с параметром "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="0d33d-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="0d33d-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="0d33d-173">-SourcePortRange</span></span>
<span data-ttu-id="0d33d-174">Указывает исходный порт или диапазон.</span><span class="sxs-lookup"><span data-stu-id="0d33d-174">Specifies the source port or range.</span></span>
<span data-ttu-id="0d33d-175">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0d33d-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0d33d-176">Целое число</span><span class="sxs-lookup"><span data-stu-id="0d33d-176">An integer</span></span>
- <span data-ttu-id="0d33d-177">Диапазон целочисленных значений от 0 до 65535</span><span class="sxs-lookup"><span data-stu-id="0d33d-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="0d33d-178">Подстановочный знак (\*) для соответствия любому порту</span><span class="sxs-lookup"><span data-stu-id="0d33d-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="0d33d-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d33d-179">CommonParameters</span></span>
<span data-ttu-id="0d33d-180">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d33d-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d33d-181">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d33d-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d33d-182">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d33d-182">INPUTS</span></span>

### <span data-ttu-id="0d33d-183">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0d33d-183">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="0d33d-184">Параметр "NetworkSecurityGroup" принимает значение типа "PSNetworkSecurityGroup" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="0d33d-184">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="0d33d-185">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d33d-185">OUTPUTS</span></span>

### <span data-ttu-id="0d33d-186">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0d33d-186">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="0d33d-187">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d33d-187">NOTES</span></span>

## <span data-ttu-id="0d33d-188">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d33d-188">RELATED LINKS</span></span>

[<span data-ttu-id="0d33d-189">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0d33d-189">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0d33d-190">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0d33d-190">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0d33d-191">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0d33d-191">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="0d33d-192">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0d33d-192">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

