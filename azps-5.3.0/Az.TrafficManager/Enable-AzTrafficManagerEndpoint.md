---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 5d7ef8e2fd778b5bcaaea1413bddd85eceb0582c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507897"
---
# <span data-ttu-id="426f9-101">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="426f9-101">Enable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="426f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="426f9-102">SYNOPSIS</span></span>
<span data-ttu-id="426f9-103">Включает конечную точку в профиле Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="426f9-103">Enables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="426f9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="426f9-104">SYNTAX</span></span>

### <span data-ttu-id="426f9-105">Поля</span><span class="sxs-lookup"><span data-stu-id="426f9-105">Fields</span></span>
```
Enable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="426f9-106">Объект</span><span class="sxs-lookup"><span data-stu-id="426f9-106">Object</span></span>
```
Enable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="426f9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="426f9-107">DESCRIPTION</span></span>
<span data-ttu-id="426f9-108">С **помощью cmdlet Enable-AzTrafficManagerEndpoint** можно включить конечную точку в профиле Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="426f9-108">The **Enable-AzTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="426f9-109">С помощью оператора конвейера можно передать объект **TrafficManagerEndpoint** этому cmdlet или указать объект **TrafficManagerEndpoint** с помощью параметра *TrafficManagerEndpoint.*</span><span class="sxs-lookup"><span data-stu-id="426f9-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="426f9-110">Кроме того, можно указать имя и тип конечной точки с помощью параметров *"Имя"* и "Тип" вместе с параметрами *ProfileName* и  *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="426f9-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="426f9-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="426f9-111">EXAMPLES</span></span>

### <span data-ttu-id="426f9-112">Пример 1. Включить конечную точку из профиля</span><span class="sxs-lookup"><span data-stu-id="426f9-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="426f9-113">Эта команда включает внешнюю конечную точку contoso в профиле ContosoProfile группы ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="426f9-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>

### <span data-ttu-id="426f9-114">Пример 2. Включить конечную точку с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="426f9-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerEndpoint
```

<span data-ttu-id="426f9-115">Эта команда получает внешнюю конечную точку Contoso из профиля ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="426f9-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="426f9-116">Затем эта команда передает эту конечную точку **командлету Enable-AzTrafficManagerEndpoint** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="426f9-116">The command then passes that endpoint to the **Enable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="426f9-117">Этот cmdlet включает эту конечную точку.</span><span class="sxs-lookup"><span data-stu-id="426f9-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="426f9-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="426f9-118">PARAMETERS</span></span>

### <span data-ttu-id="426f9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="426f9-119">-DefaultProfile</span></span>
<span data-ttu-id="426f9-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="426f9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="426f9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="426f9-121">-Name</span></span>
<span data-ttu-id="426f9-122">Указывает имя конечной точки Диспетчера трафика, которую включает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="426f9-122">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426f9-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="426f9-123">-ProfileName</span></span>
<span data-ttu-id="426f9-124">Указывает имя профиля Диспетчера трафика, в котором этот cmdlet включает конечную точку.</span><span class="sxs-lookup"><span data-stu-id="426f9-124">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="426f9-125">Чтобы получить профиль, воспользуйтесь Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="426f9-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426f9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="426f9-126">-ResourceGroupName</span></span>
<span data-ttu-id="426f9-127">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="426f9-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="426f9-128">Этот cmdlet включает конечную точку Диспетчера трафика в группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="426f9-128">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426f9-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="426f9-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="426f9-130">Указывает конечную точку диспетчера трафика, которую включает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="426f9-130">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="426f9-131">Чтобы получить объект **TrafficManagerEndpoint,** воспользуйтесь Get-AzTrafficManagerEndpoint управления.</span><span class="sxs-lookup"><span data-stu-id="426f9-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="426f9-132">-Type</span><span class="sxs-lookup"><span data-stu-id="426f9-132">-Type</span></span>
<span data-ttu-id="426f9-133">Определяет тип конечной точки, которую этот cmdlet отключает в профиле Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="426f9-133">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="426f9-134">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="426f9-134">Valid values are:</span></span> 

- <span data-ttu-id="426f9-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="426f9-135">AzureEndpoints</span></span>
- <span data-ttu-id="426f9-136">Внешниеendpoints</span><span class="sxs-lookup"><span data-stu-id="426f9-136">ExternalEndpoints</span></span>
- <span data-ttu-id="426f9-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="426f9-137">NestedEndpoints</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="426f9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="426f9-138">CommonParameters</span></span>
<span data-ttu-id="426f9-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="426f9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="426f9-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="426f9-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="426f9-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="426f9-141">INPUTS</span></span>

### <span data-ttu-id="426f9-142">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="426f9-142">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="426f9-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="426f9-143">OUTPUTS</span></span>

### <span data-ttu-id="426f9-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="426f9-144">System.Boolean</span></span>

## <span data-ttu-id="426f9-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="426f9-145">NOTES</span></span>

## <span data-ttu-id="426f9-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="426f9-146">RELATED LINKS</span></span>

[<span data-ttu-id="426f9-147">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="426f9-147">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="426f9-148">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="426f9-148">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="426f9-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="426f9-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="426f9-150">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="426f9-150">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="426f9-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="426f9-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="426f9-152">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="426f9-152">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="426f9-153">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="426f9-153">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

