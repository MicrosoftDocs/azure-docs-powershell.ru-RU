---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservice
schema: 2.0.0
content_git_url: ''
ms.openlocfilehash: 655cfeeae35d1b48bbfe2149fd4262dffe72ae09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556324"
---
# <span data-ttu-id="75d2b-101">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="75d2b-101">Get-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="75d2b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="75d2b-102">SYNOPSIS</span></span>
<span data-ttu-id="75d2b-103">Возвращает службу в топологии службы.</span><span class="sxs-lookup"><span data-stu-id="75d2b-103">Gets a service in a service topology.</span></span>

## <span data-ttu-id="75d2b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="75d2b-104">SYNTAX</span></span>

### <span data-ttu-id="75d2b-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="75d2b-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75d2b-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="75d2b-106">ByServiceTopologyObject</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75d2b-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="75d2b-107">ByServiceTopologyResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75d2b-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="75d2b-108">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="75d2b-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="75d2b-109">InputObject</span></span>
```
Get-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75d2b-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75d2b-110">DESCRIPTION</span></span>
<span data-ttu-id="75d2b-111">Командлет **Get-AzureRmDeploymentManagerService** Получает службу в рамках топологии службы и возвращает объект, представляющий эту службу.</span><span class="sxs-lookup"><span data-stu-id="75d2b-111">The **Get-AzureRmDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="75d2b-112">Укажите службу, указав ее имя, топологию службы и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75d2b-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="75d2b-113">Кроме того, можно предоставить объект обслуживания или ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="75d2b-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="75d2b-114">Вы можете локально изменить этот объект, а затем применить изменения к службе с помощью командлета Set-AzureRmDeploymentManagerService.</span><span class="sxs-lookup"><span data-stu-id="75d2b-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="75d2b-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="75d2b-115">EXAMPLES</span></span>

### <span data-ttu-id="75d2b-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="75d2b-116">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="75d2b-117">Эта команда получает службу с именем ContosoService1 в топологии службы с именем ContosoServiceTopology в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="75d2b-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="75d2b-118">Пример 2: получение службы с помощью идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="75d2b-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="75d2b-119">Эта команда получает службу с именем ContosoService1 в топологии службы с именем ContosoServiceTopology в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="75d2b-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="75d2b-120">Пример 3: получение службы с помощью объекта обслуживания.</span><span class="sxs-lookup"><span data-stu-id="75d2b-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="75d2b-121">Эта команда возвращает службу, имя и название топологии обслуживания и ResourceGroup которой соответствуют свойствам Name, ServiceTopologyName и ResourceGroupName для $serviceObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="75d2b-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="75d2b-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="75d2b-122">PARAMETERS</span></span>

### <span data-ttu-id="75d2b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d2b-123">-DefaultProfile</span></span>
<span data-ttu-id="75d2b-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75d2b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75d2b-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="75d2b-125">-Name</span></span>
<span data-ttu-id="75d2b-126">Имя службы.</span><span class="sxs-lookup"><span data-stu-id="75d2b-126">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75d2b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75d2b-127">-ResourceGroupName</span></span>
<span data-ttu-id="75d2b-128">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75d2b-128">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75d2b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75d2b-129">-ResourceId</span></span>
<span data-ttu-id="75d2b-130">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="75d2b-130">The resource identifier.</span></span>

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

### <span data-ttu-id="75d2b-131">-Служба</span><span class="sxs-lookup"><span data-stu-id="75d2b-131">-Service</span></span>
<span data-ttu-id="75d2b-132">Объект обслуживания.</span><span class="sxs-lookup"><span data-stu-id="75d2b-132">Service object.</span></span>

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

### <span data-ttu-id="75d2b-133">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="75d2b-133">-ServiceTopology</span></span>
<span data-ttu-id="75d2b-134">Объект Topology (топология службы), в котором должна быть создана служба.</span><span class="sxs-lookup"><span data-stu-id="75d2b-134">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="75d2b-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="75d2b-135">-ServiceTopologyName</span></span>
<span data-ttu-id="75d2b-136">Имя топологии службы.</span><span class="sxs-lookup"><span data-stu-id="75d2b-136">The name of the service topology.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75d2b-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="75d2b-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="75d2b-138">Идентификатор ресурса топологии обслуживания, в котором должна быть создана служба.</span><span class="sxs-lookup"><span data-stu-id="75d2b-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="75d2b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d2b-139">CommonParameters</span></span>
<span data-ttu-id="75d2b-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="75d2b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d2b-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75d2b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d2b-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="75d2b-142">INPUTS</span></span>

### <span data-ttu-id="75d2b-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="75d2b-143">None</span></span>

## <span data-ttu-id="75d2b-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="75d2b-144">OUTPUTS</span></span>

### <span data-ttu-id="75d2b-145">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="75d2b-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="75d2b-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="75d2b-146">NOTES</span></span>

## <span data-ttu-id="75d2b-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75d2b-147">RELATED LINKS</span></span>

[<span data-ttu-id="75d2b-148">New-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="75d2b-148">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="75d2b-149">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="75d2b-149">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="75d2b-150">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="75d2b-150">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)