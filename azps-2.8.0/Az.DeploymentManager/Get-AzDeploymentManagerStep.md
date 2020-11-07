---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
ms.openlocfilehash: eb0c7db4706aacfba4010632422869f0dca54694
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721133"
---
# <span data-ttu-id="9fff3-101">Get-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="9fff3-101">Get-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="9fff3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9fff3-102">SYNOPSIS</span></span>
<span data-ttu-id="9fff3-103">Получает шаг.</span><span class="sxs-lookup"><span data-stu-id="9fff3-103">Gets the step.</span></span>

## <span data-ttu-id="9fff3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9fff3-104">SYNTAX</span></span>

### <span data-ttu-id="9fff3-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9fff3-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fff3-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fff3-106">ResourceId</span></span>
```
Get-AzDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9fff3-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="9fff3-107">InputObject</span></span>
```
Get-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9fff3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fff3-108">DESCRIPTION</span></span>
<span data-ttu-id="9fff3-109">Командлет **Get-AzDeploymentManagerStep** получает шаг и возвращает объект, который представляет этот шаг.</span><span class="sxs-lookup"><span data-stu-id="9fff3-109">The **Get-AzDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="9fff3-110">Укажите шаг, указав имя и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9fff3-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="9fff3-111">Кроме того, вы можете предоставить объект Step или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="9fff3-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="9fff3-112">Вы можете локально изменить этот объект, а затем применить изменения к источнику артефакта с помощью командлета Set-AzDeploymentManagerStep.</span><span class="sxs-lookup"><span data-stu-id="9fff3-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="9fff3-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9fff3-113">EXAMPLES</span></span>

### <span data-ttu-id="9fff3-114">Пример 1: получение шага</span><span class="sxs-lookup"><span data-stu-id="9fff3-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="9fff3-115">Эта команда получает шаг с именем ContosoService1WaitStep в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9fff3-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="9fff3-116">Пример 2: получение шага с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="9fff3-116">Example 2: Get a step using the resource identifier</span></span>
### <span data-ttu-id="9fff3-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9fff3-117">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="9fff3-118">Эта команда получает шаг с именем ContosoService1WaitStep в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9fff3-118">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="9fff3-119">Пример 3: получение шага с помощью объекта, возвращаемого New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="9fff3-119">Example 3: Get a step using an object returned by New-AzDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="9fff3-120">Эта команда получает шаг, имя и значение ResourceGroup которого совпадают со свойствами Name и ResourceGroupName для $stepObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="9fff3-120">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="9fff3-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9fff3-121">PARAMETERS</span></span>

### <span data-ttu-id="9fff3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fff3-122">-DefaultProfile</span></span>
<span data-ttu-id="9fff3-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9fff3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fff3-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fff3-124">-InputObject</span></span>
<span data-ttu-id="9fff3-125">Объект шага "ресурс".</span><span class="sxs-lookup"><span data-stu-id="9fff3-125">The step resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fff3-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9fff3-126">-Name</span></span>
<span data-ttu-id="9fff3-127">Имя шага.</span><span class="sxs-lookup"><span data-stu-id="9fff3-127">The name of the step.</span></span>

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

### <span data-ttu-id="9fff3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fff3-128">-ResourceGroupName</span></span>
<span data-ttu-id="9fff3-129">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9fff3-129">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fff3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fff3-130">-ResourceId</span></span>
<span data-ttu-id="9fff3-131">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="9fff3-131">The resource identifier.</span></span>

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

### <span data-ttu-id="9fff3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fff3-132">CommonParameters</span></span>
<span data-ttu-id="9fff3-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9fff3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fff3-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fff3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fff3-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9fff3-135">INPUTS</span></span>

### <span data-ttu-id="9fff3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9fff3-136">System.String</span></span>

### <span data-ttu-id="9fff3-137">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="9fff3-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="9fff3-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fff3-138">OUTPUTS</span></span>

### <span data-ttu-id="9fff3-139">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="9fff3-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="9fff3-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="9fff3-140">NOTES</span></span>

## <span data-ttu-id="9fff3-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9fff3-141">RELATED LINKS</span></span>