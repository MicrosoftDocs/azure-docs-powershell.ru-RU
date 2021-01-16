---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 91694efaeaf1a24018269706f3ee388feb7218ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409964"
---
# <span data-ttu-id="43dc3-101">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="43dc3-101">Get-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="43dc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43dc3-102">SYNOPSIS</span></span>
<span data-ttu-id="43dc3-103">Здесь перечислены все обогащения сообщений или определенное обогащение сообщений для вашего концентратора IoT.</span><span class="sxs-lookup"><span data-stu-id="43dc3-103">Lists all message enrichments or a particular message enrichment for your IoT Hub.</span></span>

## <span data-ttu-id="43dc3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="43dc3-104">SYNTAX</span></span>

### <span data-ttu-id="43dc3-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="43dc3-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43dc3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="43dc3-106">InputObjectSet</span></span>
```
Get-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43dc3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="43dc3-107">ResourceIdSet</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43dc3-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43dc3-108">DESCRIPTION</span></span>
<span data-ttu-id="43dc3-109">Подробное описание обогащения сообщений в Azure IoT Hub см. в https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="43dc3-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="43dc3-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="43dc3-110">EXAMPLES</span></span>

### <span data-ttu-id="43dc3-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="43dc3-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub"

Key  Value   Endpoint(s)
---  -----   -----------
key1 value1  {endpoint1, endpoint2}
key2 value2  {endpoint3, endpoint4}
```

<span data-ttu-id="43dc3-112">Список всех обогащений сообщений в MyIotHub</span><span class="sxs-lookup"><span data-stu-id="43dc3-112">List all message enrichments in MyIotHub</span></span>

### <span data-ttu-id="43dc3-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="43dc3-113">Example 2</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey"

Key         : key1
Value       : value1
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="43dc3-114">Показать сведения о обогащении сообщений newKey.</span><span class="sxs-lookup"><span data-stu-id="43dc3-114">Show details about "newKey" message enrichment.</span></span>

## <span data-ttu-id="43dc3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43dc3-115">PARAMETERS</span></span>

### <span data-ttu-id="43dc3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43dc3-116">-DefaultProfile</span></span>
<span data-ttu-id="43dc3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43dc3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43dc3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43dc3-118">-InputObject</span></span>
<span data-ttu-id="43dc3-119">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="43dc3-119">IotHub object</span></span>

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

### <span data-ttu-id="43dc3-120">-Key</span><span class="sxs-lookup"><span data-stu-id="43dc3-120">-Key</span></span>
<span data-ttu-id="43dc3-121">Ключ обогащения.</span><span class="sxs-lookup"><span data-stu-id="43dc3-121">The enrichment's key.</span></span>

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

### <span data-ttu-id="43dc3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="43dc3-122">-Name</span></span>
<span data-ttu-id="43dc3-123">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="43dc3-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="43dc3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43dc3-124">-ResourceGroupName</span></span>
<span data-ttu-id="43dc3-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="43dc3-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="43dc3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43dc3-126">-ResourceId</span></span>
<span data-ttu-id="43dc3-127">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="43dc3-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="43dc3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43dc3-128">CommonParameters</span></span>
<span data-ttu-id="43dc3-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43dc3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43dc3-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43dc3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43dc3-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43dc3-131">INPUTS</span></span>

### <span data-ttu-id="43dc3-132">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="43dc3-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="43dc3-133">System.String</span><span class="sxs-lookup"><span data-stu-id="43dc3-133">System.String</span></span>

## <span data-ttu-id="43dc3-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="43dc3-134">OUTPUTS</span></span>

### <span data-ttu-id="43dc3-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span><span class="sxs-lookup"><span data-stu-id="43dc3-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

### <span data-ttu-id="43dc3-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span><span class="sxs-lookup"><span data-stu-id="43dc3-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span></span>

## <span data-ttu-id="43dc3-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="43dc3-137">NOTES</span></span>

## <span data-ttu-id="43dc3-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43dc3-138">RELATED LINKS</span></span>