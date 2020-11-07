---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 346a09a635b72612c270889afd904a1535994624
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721067"
---
# <span data-ttu-id="35d08-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="35d08-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="35d08-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35d08-102">SYNOPSIS</span></span>
<span data-ttu-id="35d08-103">Центр Интернета Интернет-провайдеров, связанный с службой подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="35d08-103">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="35d08-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35d08-104">SYNTAX</span></span>

### <span data-ttu-id="35d08-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="35d08-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35d08-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="35d08-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35d08-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="35d08-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-IotHubConnectionString] <String>
 [-IotHubLocation] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35d08-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35d08-108">DESCRIPTION</span></span>
<span data-ttu-id="35d08-109">Введение в службу подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="35d08-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="35d08-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35d08-110">EXAMPLES</span></span>

### <span data-ttu-id="35d08-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="35d08-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 
ApplyAllocationPolicy : 
Location              : eastus
```

<span data-ttu-id="35d08-112">Центр Интернета Интернет-провайдеров, связанный с службой подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="35d08-112">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="35d08-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="35d08-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus" -AllocationWeight 10 -ApplyAllocationPolicy $false

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2                   true
myiothub2.azure-devices.net     westus2     10                  false
```

<span data-ttu-id="35d08-114">Связанный центр Интернета Интернет вещей с службой подготовки устройств центра для Azure IoT с AllocationWeight и ApplyAllocationPolicy.</span><span class="sxs-lookup"><span data-stu-id="35d08-114">Linked IoT hub to an Azure IoT Hub device provisioning service with AllocationWeight and ApplyAllocationPolicy.</span></span>

## <span data-ttu-id="35d08-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35d08-115">PARAMETERS</span></span>

### <span data-ttu-id="35d08-116">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="35d08-116">-AllocationWeight</span></span>
<span data-ttu-id="35d08-117">Плотность выделения для центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="35d08-117">Allocation weight of the IoT Hub</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35d08-118">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="35d08-118">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="35d08-119">Логическое значение, указывающее, следует ли применять политику выделения к концентратору Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="35d08-119">A boolean indicating whether to apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="35d08-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35d08-120">-DefaultProfile</span></span>
<span data-ttu-id="35d08-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35d08-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35d08-122">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="35d08-122">-DpsObject</span></span>
<span data-ttu-id="35d08-123">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="35d08-123">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35d08-124">-IotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="35d08-124">-IotHubConnectionString</span></span>
<span data-ttu-id="35d08-125">Строка подключения ресурса центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="35d08-125">Connection String of the Iot Hub resource.</span></span>

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

### <span data-ttu-id="35d08-126">-IotHubLocation</span><span class="sxs-lookup"><span data-stu-id="35d08-126">-IotHubLocation</span></span>
<span data-ttu-id="35d08-127">Расположение центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="35d08-127">Location of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35d08-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="35d08-128">-Name</span></span>
<span data-ttu-id="35d08-129">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="35d08-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="35d08-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35d08-130">-ResourceGroupName</span></span>
<span data-ttu-id="35d08-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="35d08-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="35d08-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35d08-132">-ResourceId</span></span>
<span data-ttu-id="35d08-133">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="35d08-133">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="35d08-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35d08-134">-Confirm</span></span>
<span data-ttu-id="35d08-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="35d08-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35d08-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35d08-136">-WhatIf</span></span>
<span data-ttu-id="35d08-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="35d08-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35d08-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="35d08-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35d08-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35d08-139">CommonParameters</span></span>
<span data-ttu-id="35d08-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35d08-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35d08-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35d08-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35d08-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35d08-142">INPUTS</span></span>

### <span data-ttu-id="35d08-143">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="35d08-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="35d08-144">System. String</span><span class="sxs-lookup"><span data-stu-id="35d08-144">System.String</span></span>

## <span data-ttu-id="35d08-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35d08-145">OUTPUTS</span></span>

### <span data-ttu-id="35d08-146">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="35d08-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="35d08-147">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="35d08-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="35d08-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="35d08-148">NOTES</span></span>

## <span data-ttu-id="35d08-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35d08-149">RELATED LINKS</span></span>