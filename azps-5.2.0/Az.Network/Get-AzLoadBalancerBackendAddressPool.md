---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 5d1c561af678086671927d3782a1fafbd9de503b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413948"
---
# <span data-ttu-id="50557-101">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="50557-101">Get-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="50557-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50557-102">SYNOPSIS</span></span>
<span data-ttu-id="50557-103">Get-AzLoadBalancerBackendAddressPool извлекает один или несколько пулов дополнительных адресов, связанных с балансировой нагрузки.</span><span class="sxs-lookup"><span data-stu-id="50557-103">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span> 

## <span data-ttu-id="50557-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="50557-104">SYNTAX</span></span>

### <span data-ttu-id="50557-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="50557-105">GetByNameParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50557-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="50557-106">GetByParentObjectParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50557-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="50557-107">GetByResourceIdParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="50557-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50557-108">DESCRIPTION</span></span>
<span data-ttu-id="50557-109">Get-AzLoadBalancerBackendAddressPool извлекает один или несколько пулов дополнительных адресов, связанных с балансировой нагрузки.</span><span class="sxs-lookup"><span data-stu-id="50557-109">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span>

## <span data-ttu-id="50557-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="50557-110">EXAMPLES</span></span>

### <span data-ttu-id="50557-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="50557-111">Example 1</span></span>
```powershell
## Get single backend under loadbalancer
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
```

```powershell
## Get all backends under loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool
```
### <span data-ttu-id="50557-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="50557-112">Example 2</span></span>
```powershell
#Get specific backend from loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="50557-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="50557-113">Example 3</span></span>
```powershell
#Get a backend by resource Id
PS C:\> Get-AzLoadBalancerBackendAddressPool -ResourceId $backendPool1.Id
```

## <span data-ttu-id="50557-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50557-114">PARAMETERS</span></span>

### <span data-ttu-id="50557-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50557-115">-DefaultProfile</span></span>
<span data-ttu-id="50557-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50557-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50557-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="50557-117">-LoadBalancer</span></span>
<span data-ttu-id="50557-118">{{ Fill LoadBalancer Description }}</span><span class="sxs-lookup"><span data-stu-id="50557-118">{{ Fill LoadBalancer Description }}</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50557-119">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="50557-119">-LoadBalancerName</span></span>
<span data-ttu-id="50557-120">Имя балансира нагрузки.</span><span class="sxs-lookup"><span data-stu-id="50557-120">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50557-121">-Name</span><span class="sxs-lookup"><span data-stu-id="50557-121">-Name</span></span>
<span data-ttu-id="50557-122">Имя пула адресов для backend.</span><span class="sxs-lookup"><span data-stu-id="50557-122">The name of the backend address pool.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50557-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50557-123">-ResourceGroupName</span></span>
<span data-ttu-id="50557-124">Имя группы ресурсов балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="50557-124">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50557-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50557-125">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50557-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50557-126">CommonParameters</span></span>
<span data-ttu-id="50557-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50557-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50557-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50557-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50557-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50557-129">INPUTS</span></span>

### <span data-ttu-id="50557-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="50557-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="50557-131">System.String</span><span class="sxs-lookup"><span data-stu-id="50557-131">System.String</span></span>

## <span data-ttu-id="50557-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="50557-132">OUTPUTS</span></span>

### <span data-ttu-id="50557-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="50557-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="50557-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="50557-134">NOTES</span></span>

## <span data-ttu-id="50557-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50557-135">RELATED LINKS</span></span>