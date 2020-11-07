---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 066026331fa43af06fc2e3314ccb97d06a0f9b50
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721119"
---
# <span data-ttu-id="52526-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="52526-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="52526-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="52526-102">SYNOPSIS</span></span>
<span data-ttu-id="52526-103">Удаляет выпуск.</span><span class="sxs-lookup"><span data-stu-id="52526-103">Deletes the rollout.</span></span>

## <span data-ttu-id="52526-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="52526-104">SYNTAX</span></span>

### <span data-ttu-id="52526-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="52526-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52526-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="52526-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52526-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="52526-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52526-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52526-108">DESCRIPTION</span></span>
<span data-ttu-id="52526-109">Командлет **Remove-AzDeploymentManagerRollout** удаляет выпуск в состоянии терминала.</span><span class="sxs-lookup"><span data-stu-id="52526-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="52526-110">Укажите имя и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="52526-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="52526-111">Кроме того, можно предоставить объект выпуска или ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="52526-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="52526-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="52526-112">EXAMPLES</span></span>

### <span data-ttu-id="52526-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="52526-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="52526-114">Эта команда удаляет выгрузку с именем ContosoRollout в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="52526-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="52526-115">Пример 2: удаление выпуска с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="52526-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="52526-116">Эта команда удаляет выгрузку с именем ContosoRollout в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="52526-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="52526-117">Пример 3: удаление выпуска с помощью объекта выпуска.</span><span class="sxs-lookup"><span data-stu-id="52526-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="52526-118">Эта команда удаляет выпуску, имя и значение ResourceGroup которого совпадают со свойствами Name и ResourceGroupName в $rolloutObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="52526-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="52526-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="52526-119">PARAMETERS</span></span>

### <span data-ttu-id="52526-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52526-120">-DefaultProfile</span></span>
<span data-ttu-id="52526-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52526-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52526-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52526-122">-InputObject</span></span>
<span data-ttu-id="52526-123">Ресурс, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="52526-123">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52526-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="52526-124">-Name</span></span>
<span data-ttu-id="52526-125">Имя выпуска.</span><span class="sxs-lookup"><span data-stu-id="52526-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="52526-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52526-126">-PassThru</span></span>
<span data-ttu-id="52526-127">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="52526-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="52526-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52526-128">-ResourceGroupName</span></span>
<span data-ttu-id="52526-129">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="52526-129">The resource group.</span></span>

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

### <span data-ttu-id="52526-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52526-130">-ResourceId</span></span>
<span data-ttu-id="52526-131">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="52526-131">The resource identifier.</span></span>

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

### <span data-ttu-id="52526-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52526-132">-Confirm</span></span>
<span data-ttu-id="52526-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="52526-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52526-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52526-134">-WhatIf</span></span>
<span data-ttu-id="52526-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="52526-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52526-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="52526-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52526-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52526-137">CommonParameters</span></span>
<span data-ttu-id="52526-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="52526-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52526-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52526-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52526-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="52526-140">INPUTS</span></span>

### <span data-ttu-id="52526-141">System. String</span><span class="sxs-lookup"><span data-stu-id="52526-141">System.String</span></span>

### <span data-ttu-id="52526-142">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="52526-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="52526-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="52526-143">OUTPUTS</span></span>

### <span data-ttu-id="52526-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52526-144">System.Boolean</span></span>

## <span data-ttu-id="52526-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="52526-145">NOTES</span></span>

## <span data-ttu-id="52526-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52526-146">RELATED LINKS</span></span>