---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 71c093573f4384884702c72e586c36bbdb9b4066
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566696"
---
# <span data-ttu-id="f9585-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9585-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="f9585-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f9585-102">SYNOPSIS</span></span>
<span data-ttu-id="f9585-103">Получает конфигурацию правила NAT для входящего трафика для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f9585-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9585-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f9585-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9585-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9585-105">DESCRIPTION</span></span>
<span data-ttu-id="f9585-106">Командлет **Get-AzureRmLoadBalancerInboundNatRuleConfig** получает одно или несколько правил трансляции сетевых адресов (NAT) для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="f9585-106">The **Get-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="f9585-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f9585-107">EXAMPLES</span></span>

### <span data-ttu-id="f9585-108">Пример 1: получение конфигурации правила входящего NAT</span><span class="sxs-lookup"><span data-stu-id="f9585-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="f9585-109">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в $slb переменной.</span><span class="sxs-lookup"><span data-stu-id="f9585-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>

<span data-ttu-id="f9585-110">Вторая команда получает соответствующее правило NAT с именем MyInboundNatRule1 из подсистемы балансировки нагрузки в $slb.</span><span class="sxs-lookup"><span data-stu-id="f9585-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="f9585-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f9585-111">PARAMETERS</span></span>

### <span data-ttu-id="f9585-112">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="f9585-112">-LoadBalancer</span></span>
<span data-ttu-id="f9585-113">Указывает подсистему балансировки нагрузки, связанную с конфигурацией правила входящего NAT для получения.</span><span class="sxs-lookup"><span data-stu-id="f9585-113">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9585-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f9585-114">-Name</span></span>
<span data-ttu-id="f9585-115">Указывает имя конфигурации правила входящего NAT, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="f9585-115">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="f9585-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9585-116">-DefaultProfile</span></span>
<span data-ttu-id="f9585-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f9585-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9585-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9585-118">CommonParameters</span></span>
<span data-ttu-id="f9585-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f9585-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9585-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9585-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9585-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f9585-121">INPUTS</span></span>

### <span data-ttu-id="f9585-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f9585-122">PSLoadBalancer</span></span>
<span data-ttu-id="f9585-123">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f9585-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="f9585-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9585-124">OUTPUTS</span></span>

### <span data-ttu-id="f9585-125">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="f9585-125">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="f9585-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="f9585-126">NOTES</span></span>

## <span data-ttu-id="f9585-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f9585-127">RELATED LINKS</span></span>

[<span data-ttu-id="f9585-128">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f9585-128">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="f9585-129">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9585-129">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f9585-130">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9585-130">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="f9585-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f9585-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)

