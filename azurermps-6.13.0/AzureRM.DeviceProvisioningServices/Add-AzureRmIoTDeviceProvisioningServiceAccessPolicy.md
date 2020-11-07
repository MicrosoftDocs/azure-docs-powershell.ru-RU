---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 23d9e40fe6d25fbd2a6bb3e23959d1a4bf087af2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567760"
---
# <span data-ttu-id="d6ee7-101">Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d6ee7-101">Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="d6ee7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6ee7-102">SYNOPSIS</span></span>
<span data-ttu-id="d6ee7-103">Добавьте новую политику общего доступа в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="d6ee7-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6ee7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6ee7-104">SYNTAX</span></span>

### <span data-ttu-id="d6ee7-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d6ee7-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6ee7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d6ee7-106">InputObjectSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6ee7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d6ee7-107">ResourceIdSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6ee7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6ee7-108">DESCRIPTION</span></span>
<span data-ttu-id="d6ee7-109">Введение в службу подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="d6ee7-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="d6ee7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6ee7-110">EXAMPLES</span></span>

### <span data-ttu-id="d6ee7-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d6ee7-111">Example 1</span></span>
```
PS C:\> Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="d6ee7-112">Добавьте новую политику общего доступа в службе подготовки устройств центра для Azure IoT с EnrollmentWrite и ServiceConfig правами.</span><span class="sxs-lookup"><span data-stu-id="d6ee7-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="d6ee7-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d6ee7-113">Example 2</span></span>
```
PS C:\> Add-AzureRmIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="d6ee7-114">Добавьте новую политику общего доступа в службе подготовки устройств центра для Azure IoT с EnrollmentRead right.</span><span class="sxs-lookup"><span data-stu-id="d6ee7-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="d6ee7-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6ee7-115">PARAMETERS</span></span>

### <span data-ttu-id="d6ee7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6ee7-116">-DefaultProfile</span></span>
<span data-ttu-id="d6ee7-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d6ee7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6ee7-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="d6ee7-118">-DpsObject</span></span>
<span data-ttu-id="d6ee7-119">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="d6ee7-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="d6ee7-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d6ee7-120">-KeyName</span></span>
<span data-ttu-id="d6ee7-121">Имя ключа политики доступа к службе для подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="d6ee7-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="d6ee7-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d6ee7-122">-Name</span></span>
<span data-ttu-id="d6ee7-123">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="d6ee7-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d6ee7-124">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="d6ee7-124">-Permissions</span></span>
<span data-ttu-id="d6ee7-125">Разрешения для политики доступа к службам для устройства IoT</span><span class="sxs-lookup"><span data-stu-id="d6ee7-125">IoT Device Provisioning Service access policy permissions</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ServiceConfig, EnrollmentRead, EnrollmentWrite, DeviceConnect, RegistrationStatusRead, RegistrationStatusWrite

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6ee7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6ee7-126">-ResourceGroupName</span></span>
<span data-ttu-id="d6ee7-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d6ee7-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d6ee7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6ee7-128">-ResourceId</span></span>
<span data-ttu-id="d6ee7-129">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="d6ee7-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="d6ee7-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6ee7-130">-Confirm</span></span>
<span data-ttu-id="d6ee7-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d6ee7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6ee7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6ee7-132">-WhatIf</span></span>
<span data-ttu-id="d6ee7-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d6ee7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6ee7-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d6ee7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6ee7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6ee7-135">CommonParameters</span></span>
<span data-ttu-id="d6ee7-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6ee7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6ee7-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6ee7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6ee7-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6ee7-138">INPUTS</span></span>

### <span data-ttu-id="d6ee7-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="d6ee7-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="d6ee7-140">Параметры: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d6ee7-140">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="d6ee7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d6ee7-141">System.String</span></span>

## <span data-ttu-id="d6ee7-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6ee7-142">OUTPUTS</span></span>

### <span data-ttu-id="d6ee7-143">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="d6ee7-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="d6ee7-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6ee7-144">NOTES</span></span>

## <span data-ttu-id="d6ee7-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6ee7-145">RELATED LINKS</span></span>