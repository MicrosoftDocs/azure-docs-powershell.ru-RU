---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 155d2ab8a1e43264a3598a0ea44011ebb66e9e58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563451"
---
# <span data-ttu-id="733cf-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="733cf-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="733cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="733cf-102">SYNOPSIS</span></span>
<span data-ttu-id="733cf-103">Удаляет интерфейсную конфигурацию IP из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="733cf-103">Removes a front-end IP configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="733cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="733cf-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="733cf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="733cf-105">DESCRIPTION</span></span>
<span data-ttu-id="733cf-106">Командлет **Remove-AzureRmLoadBalancerFrontendIpConfig** удаляет IP-конфигурацию интерфейсов из подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="733cf-106">The **Remove-AzureRmLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="733cf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="733cf-107">EXAMPLES</span></span>

### <span data-ttu-id="733cf-108">Пример 1: удаление интерфейсной конфигурации IP из подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="733cf-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="733cf-109">Первая команда получает подсистему балансировки нагрузки, связанную с интерфейсной IP-конфигурацией, которую вы хотите удалить, и сохраняет ее в переменной $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="733cf-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="733cf-110">Вторая команда удаляет связанную конфигурацию IP-интерфейсов из подсистемы балансировки нагрузки в $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="733cf-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="733cf-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="733cf-111">PARAMETERS</span></span>

### <span data-ttu-id="733cf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="733cf-112">-DefaultProfile</span></span>
<span data-ttu-id="733cf-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="733cf-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="733cf-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="733cf-114">-LoadBalancer</span></span>
<span data-ttu-id="733cf-115">Указывает подсистему балансировки нагрузки, которая содержит интерфейсную конфигурацию IP-интерфейса, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="733cf-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="733cf-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="733cf-116">-Name</span></span>
<span data-ttu-id="733cf-117">Указывает имя удаляемой конфигурации переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="733cf-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="733cf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="733cf-118">CommonParameters</span></span>
<span data-ttu-id="733cf-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="733cf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="733cf-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="733cf-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="733cf-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="733cf-121">INPUTS</span></span>

### <span data-ttu-id="733cf-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="733cf-122">PSLoadBalancer</span></span>
<span data-ttu-id="733cf-123">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="733cf-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="733cf-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="733cf-124">OUTPUTS</span></span>

### <span data-ttu-id="733cf-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="733cf-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="733cf-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="733cf-126">NOTES</span></span>

## <span data-ttu-id="733cf-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="733cf-127">RELATED LINKS</span></span>

[<span data-ttu-id="733cf-128">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="733cf-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="733cf-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="733cf-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="733cf-130">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="733cf-130">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="733cf-131">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="733cf-131">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="733cf-132">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="733cf-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)

