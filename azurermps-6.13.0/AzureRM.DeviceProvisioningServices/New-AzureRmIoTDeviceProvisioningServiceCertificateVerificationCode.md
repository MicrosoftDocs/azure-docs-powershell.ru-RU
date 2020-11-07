---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode.md
ms.openlocfilehash: 59445c2e162a7cbfce5cff26bac91d133c8928a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560184"
---
# <span data-ttu-id="d4b5a-101">New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="d4b5a-101">New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode</span></span>

## <span data-ttu-id="d4b5a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d4b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="d4b5a-103">Создайте проверочный код для сертификата службы подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-103">Generate a verification code for an Azure IoT Hub Device Provisioning Service certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4b5a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d4b5a-104">SYNTAX</span></span>

### <span data-ttu-id="d4b5a-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4b5a-105">ResourceSet (Default)</span></span>
```
New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceGroupName] <String>
 [-Name] <String> [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4b5a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d4b5a-106">InputObjectSet</span></span>
```
New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode [-InputObject] <PSCertificateResponse>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4b5a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d4b5a-107">ResourceIdSet</span></span>
```
New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4b5a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4b5a-108">DESCRIPTION</span></span>
<span data-ttu-id="d4b5a-109">Этот проверочный код используется для завершения этапа проверки подлинности для сертификата.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="d4b5a-110">Используйте этот проверочный код в качестве CN нового сертификата, подписанного закрытым ключом корневых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="d4b5a-111">Подробное описание сертификатов ЦС в службе подготовки устройств центра Azure IoT можно найти в разделе https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="d4b5a-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="d4b5a-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d4b5a-112">EXAMPLES</span></span>

### <span data-ttu-id="d4b5a-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d4b5a-113">Example 1</span></span>
```
PS C:\> New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
VerificationCode    : A901A843EFF75419AC1F0EB460E85DF153092A0547AA30F5
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="d4b5a-114">Создайте проверочный код для "mycertificate".</span><span class="sxs-lookup"><span data-stu-id="d4b5a-114">Generate a verification code for "mycertificate".</span></span>

### <span data-ttu-id="d4b5a-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d4b5a-115">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | New-AzureRmIoTDpsCVC

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
VerificationCode    : A901A843EFF75419AC1F0EB460E85DF153092A0547AA30F5
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="d4b5a-116">Создайте проверочный код для "mycertificate" с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-116">Generate a verification code for "mycertificate" using pipeline.</span></span>

## <span data-ttu-id="d4b5a-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d4b5a-117">PARAMETERS</span></span>

### <span data-ttu-id="d4b5a-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="d4b5a-118">-CertificateName</span></span>
<span data-ttu-id="d4b5a-119">Имя сертификата службы подготовки устройства IOT</span><span class="sxs-lookup"><span data-stu-id="d4b5a-119">Name of the Iot device provisioning service certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4b5a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4b5a-120">-DefaultProfile</span></span>
<span data-ttu-id="d4b5a-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4b5a-122">-ETag</span><span class="sxs-lookup"><span data-stu-id="d4b5a-122">-Etag</span></span>
<span data-ttu-id="d4b5a-123">ETag сертификата</span><span class="sxs-lookup"><span data-stu-id="d4b5a-123">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4b5a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4b5a-124">-InputObject</span></span>
<span data-ttu-id="d4b5a-125">Объект сертификата службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="d4b5a-125">IoT Device Provisioning Service Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4b5a-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d4b5a-126">-Name</span></span>
<span data-ttu-id="d4b5a-127">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="d4b5a-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d4b5a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4b5a-128">-ResourceGroupName</span></span>
<span data-ttu-id="d4b5a-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d4b5a-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d4b5a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4b5a-130">-ResourceId</span></span>
<span data-ttu-id="d4b5a-131">Идентификатор ресурса сертификата службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="d4b5a-131">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="d4b5a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4b5a-132">-Confirm</span></span>
<span data-ttu-id="d4b5a-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4b5a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4b5a-134">-WhatIf</span></span>
<span data-ttu-id="d4b5a-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4b5a-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4b5a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4b5a-137">CommonParameters</span></span>
<span data-ttu-id="d4b5a-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d4b5a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4b5a-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4b5a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4b5a-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d4b5a-140">INPUTS</span></span>

### <span data-ttu-id="d4b5a-141">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="d4b5a-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>
<span data-ttu-id="d4b5a-142">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d4b5a-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="d4b5a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d4b5a-143">System.String</span></span>

## <span data-ttu-id="d4b5a-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4b5a-144">OUTPUTS</span></span>

### <span data-ttu-id="d4b5a-145">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSVerificationCodeResponse</span><span class="sxs-lookup"><span data-stu-id="d4b5a-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span></span>

## <span data-ttu-id="d4b5a-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="d4b5a-146">NOTES</span></span>

## <span data-ttu-id="d4b5a-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4b5a-147">RELATED LINKS</span></span>