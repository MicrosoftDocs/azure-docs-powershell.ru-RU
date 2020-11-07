---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoute.md
ms.openlocfilehash: 8c3aaad928545574c7da0adeae140a250056cd83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720760"
---
# <span data-ttu-id="dcb8c-101">Add-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="dcb8c-101">Add-AzIotHubRoute</span></span>

## <span data-ttu-id="dcb8c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dcb8c-102">SYNOPSIS</span></span>
<span data-ttu-id="dcb8c-103">Создание маршрута в центре Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="dcb8c-103">Create a route in IoT Hub</span></span>

## <span data-ttu-id="dcb8c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dcb8c-104">SYNTAX</span></span>

### <span data-ttu-id="dcb8c-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dcb8c-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 -Source <PSRoutingSource> -EndpointName <String> [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcb8c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dcb8c-106">InputObjectSet</span></span>
```
Add-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> -Source <PSRoutingSource>
 -EndpointName <String> [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcb8c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dcb8c-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> -Source <PSRoutingSource> -EndpointName <String>
 [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dcb8c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcb8c-108">DESCRIPTION</span></span>
<span data-ttu-id="dcb8c-109">Создание маршрута для отправки определенного источника данных и условия на нужную конечную точку.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-109">Create a route to send specific data source and condition to a desired endpoint.</span></span>

## <span data-ttu-id="dcb8c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dcb8c-110">EXAMPLES</span></span>

### <span data-ttu-id="dcb8c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dcb8c-111">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source DeviceMessages -EndpointName E1

RouteName     : R1
DataSource    : DeviceMessages
EndpointNames : E1
Condition     : 
IsEnabled     : False
```

<span data-ttu-id="dcb8c-112">Создать новый маршрут R1.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-112">Create a new route "R1".</span></span>

## <span data-ttu-id="dcb8c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dcb8c-113">PARAMETERS</span></span>

### <span data-ttu-id="dcb8c-114">-Условие</span><span class="sxs-lookup"><span data-stu-id="dcb8c-114">-Condition</span></span>
<span data-ttu-id="dcb8c-115">Условие, которое оценивается для применения правила маршрутизации</span><span class="sxs-lookup"><span data-stu-id="dcb8c-115">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="dcb8c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcb8c-116">-DefaultProfile</span></span>
<span data-ttu-id="dcb8c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcb8c-118">-Включено</span><span class="sxs-lookup"><span data-stu-id="dcb8c-118">-Enabled</span></span>
<span data-ttu-id="dcb8c-119">Включить маршрут</span><span class="sxs-lookup"><span data-stu-id="dcb8c-119">Enable route</span></span>

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

### <span data-ttu-id="dcb8c-120">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="dcb8c-120">-EndpointName</span></span>
<span data-ttu-id="dcb8c-121">Имя конечной точки маршрутизации</span><span class="sxs-lookup"><span data-stu-id="dcb8c-121">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="dcb8c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dcb8c-122">-InputObject</span></span>
<span data-ttu-id="dcb8c-123">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="dcb8c-123">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb8c-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dcb8c-124">-Name</span></span>
<span data-ttu-id="dcb8c-125">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="dcb8c-125">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcb8c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcb8c-126">-ResourceGroupName</span></span>
<span data-ttu-id="dcb8c-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="dcb8c-127">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcb8c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcb8c-128">-ResourceId</span></span>
<span data-ttu-id="dcb8c-129">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="dcb8c-129">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcb8c-130">-RouteName</span><span class="sxs-lookup"><span data-stu-id="dcb8c-130">-RouteName</span></span>
<span data-ttu-id="dcb8c-131">Имя маршрута</span><span class="sxs-lookup"><span data-stu-id="dcb8c-131">Name of the Route</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcb8c-132">-Source (источник)</span><span class="sxs-lookup"><span data-stu-id="dcb8c-132">-Source</span></span>
<span data-ttu-id="dcb8c-133">Источник маршрута</span><span class="sxs-lookup"><span data-stu-id="dcb8c-133">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcb8c-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dcb8c-134">-Confirm</span></span>
<span data-ttu-id="dcb8c-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcb8c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcb8c-136">-WhatIf</span></span>
<span data-ttu-id="dcb8c-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcb8c-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcb8c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcb8c-139">CommonParameters</span></span>
<span data-ttu-id="dcb8c-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcb8c-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcb8c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcb8c-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dcb8c-142">INPUTS</span></span>

### <span data-ttu-id="dcb8c-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="dcb8c-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="dcb8c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="dcb8c-144">System.String</span></span>

## <span data-ttu-id="dcb8c-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcb8c-145">OUTPUTS</span></span>

### <span data-ttu-id="dcb8c-146">Microsoft. Azure. Commands. Management. IotHub. Models. PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="dcb8c-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="dcb8c-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="dcb8c-147">NOTES</span></span>

## <span data-ttu-id="dcb8c-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dcb8c-148">RELATED LINKS</span></span>