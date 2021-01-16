---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: b09671fcb075ff029eaa0a28185d8f88d650caf1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398759"
---
# <span data-ttu-id="05010-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="05010-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="05010-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05010-102">SYNOPSIS</span></span>
<span data-ttu-id="05010-103">Получите параметры распределенной трассии для устройства.</span><span class="sxs-lookup"><span data-stu-id="05010-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="05010-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="05010-104">SYNTAX</span></span>

### <span data-ttu-id="05010-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="05010-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05010-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="05010-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05010-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="05010-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05010-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05010-108">DESCRIPTION</span></span>
<span data-ttu-id="05010-109">Получите параметры распределенной трассии для устройства.</span><span class="sxs-lookup"><span data-stu-id="05010-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="05010-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="05010-110">EXAMPLES</span></span>

### <span data-ttu-id="05010-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="05010-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="05010-112">Получите параметры распределенной трассии для устройства.</span><span class="sxs-lookup"><span data-stu-id="05010-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="05010-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05010-113">PARAMETERS</span></span>

### <span data-ttu-id="05010-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05010-114">-DefaultProfile</span></span>
<span data-ttu-id="05010-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="05010-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05010-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="05010-116">-DeviceId</span></span>
<span data-ttu-id="05010-117">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="05010-117">Target Device Id.</span></span>

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

### <span data-ttu-id="05010-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05010-118">-InputObject</span></span>
<span data-ttu-id="05010-119">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="05010-119">IotHub object</span></span>

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

### <span data-ttu-id="05010-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="05010-120">-IotHubName</span></span>
<span data-ttu-id="05010-121">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="05010-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="05010-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05010-122">-ResourceGroupName</span></span>
<span data-ttu-id="05010-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="05010-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="05010-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05010-124">-ResourceId</span></span>
<span data-ttu-id="05010-125">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="05010-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="05010-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05010-126">CommonParameters</span></span>
<span data-ttu-id="05010-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05010-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05010-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05010-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05010-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05010-129">INPUTS</span></span>

### <span data-ttu-id="05010-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="05010-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="05010-131">System.String</span><span class="sxs-lookup"><span data-stu-id="05010-131">System.String</span></span>

## <span data-ttu-id="05010-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="05010-132">OUTPUTS</span></span>

### <span data-ttu-id="05010-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="05010-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="05010-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="05010-134">NOTES</span></span>

## <span data-ttu-id="05010-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05010-135">RELATED LINKS</span></span>