---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
ms.openlocfilehash: 3dda11ec4fddde67a3ae4300f884290831ac28ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721142"
---
# <span data-ttu-id="8fed6-101">Get-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="8fed6-101">Get-AzDeploymentManagerService</span></span>

## <span data-ttu-id="8fed6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8fed6-102">SYNOPSIS</span></span>
<span data-ttu-id="8fed6-103">Возвращает службу.</span><span class="sxs-lookup"><span data-stu-id="8fed6-103">Gets the service.</span></span>

## <span data-ttu-id="8fed6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8fed6-104">SYNTAX</span></span>

### <span data-ttu-id="8fed6-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8fed6-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fed6-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="8fed6-106">ByServiceTopologyObject</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8fed6-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="8fed6-107">ByServiceTopologyResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fed6-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fed6-108">ResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8fed6-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="8fed6-109">InputObject</span></span>
```
Get-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8fed6-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8fed6-110">DESCRIPTION</span></span>
<span data-ttu-id="8fed6-111">Командлет **Get-AzDeploymentManagerService** Получает службу в рамках топологии службы и возвращает объект, представляющий эту службу.</span><span class="sxs-lookup"><span data-stu-id="8fed6-111">The **Get-AzDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="8fed6-112">Укажите службу, указав ее имя, топологию службы и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8fed6-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="8fed6-113">Кроме того, можно предоставить объект обслуживания или ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="8fed6-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="8fed6-114">Вы можете локально изменить этот объект, а затем применить изменения к службе с помощью командлета Set-AzDeploymentManagerService.</span><span class="sxs-lookup"><span data-stu-id="8fed6-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="8fed6-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8fed6-115">EXAMPLES</span></span>

### <span data-ttu-id="8fed6-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8fed6-116">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="8fed6-117">Эта команда получает службу с именем ContosoService1 в топологии службы с именем ContosoServiceTopology в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8fed6-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="8fed6-118">Пример 2: получение службы с помощью идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="8fed6-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="8fed6-119">Эта команда получает службу с именем ContosoService1 в топологии службы с именем ContosoServiceTopology в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8fed6-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="8fed6-120">Пример 3: получение службы с помощью объекта обслуживания.</span><span class="sxs-lookup"><span data-stu-id="8fed6-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="8fed6-121">Эта команда возвращает службу, имя и название топологии обслуживания и ResourceGroup которой соответствуют свойствам Name, ServiceTopologyName и ResourceGroupName для $serviceObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="8fed6-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
 

## <span data-ttu-id="8fed6-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8fed6-122">PARAMETERS</span></span>

### <span data-ttu-id="8fed6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fed6-123">-DefaultProfile</span></span>
<span data-ttu-id="8fed6-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8fed6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fed6-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8fed6-125">-InputObject</span></span>
<span data-ttu-id="8fed6-126">Объект обслуживания.</span><span class="sxs-lookup"><span data-stu-id="8fed6-126">Service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fed6-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8fed6-127">-Name</span></span>
<span data-ttu-id="8fed6-128">Имя службы.</span><span class="sxs-lookup"><span data-stu-id="8fed6-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fed6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fed6-129">-ResourceGroupName</span></span>
<span data-ttu-id="8fed6-130">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8fed6-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fed6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fed6-131">-ResourceId</span></span>
<span data-ttu-id="8fed6-132">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="8fed6-132">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fed6-133">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="8fed6-133">-ServiceTopologyName</span></span>
<span data-ttu-id="8fed6-134">Имя топологии службы.</span><span class="sxs-lookup"><span data-stu-id="8fed6-134">The name of the service topology.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fed6-135">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="8fed6-135">-ServiceTopologyObject</span></span>
<span data-ttu-id="8fed6-136">Объект Topology (топология службы), в котором должна быть создана служба.</span><span class="sxs-lookup"><span data-stu-id="8fed6-136">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fed6-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="8fed6-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="8fed6-138">Идентификатор ресурса топологии обслуживания, в котором должна быть создана служба.</span><span class="sxs-lookup"><span data-stu-id="8fed6-138">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fed6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fed6-139">CommonParameters</span></span>
<span data-ttu-id="8fed6-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8fed6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fed6-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fed6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fed6-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8fed6-142">INPUTS</span></span>

### <span data-ttu-id="8fed6-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8fed6-143">System.String</span></span>

### <span data-ttu-id="8fed6-144">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="8fed6-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="8fed6-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8fed6-145">OUTPUTS</span></span>

### <span data-ttu-id="8fed6-146">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="8fed6-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="8fed6-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="8fed6-147">NOTES</span></span>

## <span data-ttu-id="8fed6-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8fed6-148">RELATED LINKS</span></span>