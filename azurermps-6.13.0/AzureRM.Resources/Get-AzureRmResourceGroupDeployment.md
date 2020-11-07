---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: a125635ec9cce66cb74c9a9d7c5f56323fb9b53f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562703"
---
# <span data-ttu-id="521f1-101">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="521f1-101">Get-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="521f1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="521f1-102">SYNOPSIS</span></span>
<span data-ttu-id="521f1-103">Возвращает развертывания в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="521f1-103">Gets the deployments in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="521f1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="521f1-104">SYNTAX</span></span>

### <span data-ttu-id="521f1-105">GetByResourceGroupDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="521f1-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="521f1-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="521f1-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="521f1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="521f1-107">DESCRIPTION</span></span>
<span data-ttu-id="521f1-108">Командлет **Get-AzureRmResourceGroupDeployment** получает развертывание в группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="521f1-108">The **Get-AzureRmResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="521f1-109">Укажите параметр *Name* ( *идентификатор* ), чтобы отфильтровать результаты.</span><span class="sxs-lookup"><span data-stu-id="521f1-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="521f1-110">По умолчанию **Get-AzureRmResourceGroupDeployment** получает все развертывания для указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="521f1-110">By default, **Get-AzureRmResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="521f1-111">Ресурс Azure — это управляемая пользователем сущность Azure, например сервер базы данных, база данных или веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="521f1-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="521f1-112">Группа ресурсов Azure — это коллекция ресурсов Azure, развернутых как единое целое.</span><span class="sxs-lookup"><span data-stu-id="521f1-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="521f1-113">Развертывание — это операция, которая делает ресурсы в группе ресурсов доступной для использования.</span><span class="sxs-lookup"><span data-stu-id="521f1-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="521f1-114">Дополнительные сведения о ресурсах Azure и группах ресурсов Azure можно найти в командлете New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="521f1-114">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="521f1-115">Вы можете использовать этот командлет для отслеживания.</span><span class="sxs-lookup"><span data-stu-id="521f1-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="521f1-116">Для отладки используйте этот командлет с командлетом Get-AzureRmLog.</span><span class="sxs-lookup"><span data-stu-id="521f1-116">For debugging, use this cmdlet with the Get-AzureRmLog cmdlet.</span></span>

## <span data-ttu-id="521f1-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="521f1-117">EXAMPLES</span></span>

### <span data-ttu-id="521f1-118">Пример 1: получение всех развертываний для группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="521f1-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="521f1-119">Эта команда получает все развертывания для группы ресурсов ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="521f1-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="521f1-120">На выходе показано развертывание для блога WordPress, в котором был использован шаблон коллекции.</span><span class="sxs-lookup"><span data-stu-id="521f1-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="521f1-121">Пример 2: получение развертывания по имени</span><span class="sxs-lookup"><span data-stu-id="521f1-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="521f1-122">Эта команда получает развертывание DeployWebsite01 группы ресурсов ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="521f1-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="521f1-123">Вы можете присвоить имя развертыванию при создании с помощью командлетов **New-AzureRmResourceGroup** или **New-AzureRmResourceGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="521f1-123">You can assign a name to a deployment when you create it by using the **New-AzureRmResourceGroup** or **New-AzureRmResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="521f1-124">Если вы не назначаете имя, командлеты предоставляют имя по умолчанию на основе шаблона, который используется для создания развертывания.</span><span class="sxs-lookup"><span data-stu-id="521f1-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="521f1-125">Пример 3: получение развертываний всех групп ресурсов</span><span class="sxs-lookup"><span data-stu-id="521f1-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="521f1-126">Эта команда получает все группы ресурсов в подписке с помощью командлета Get-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="521f1-126">This command gets all resource groups in your subscription by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="521f1-127">Команда передает группы ресурсов в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="521f1-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="521f1-128">Текущий командлет получает все развертывания всех групп ресурсов в подписке и передает результаты в командлет Format-Table, чтобы отобразить значения свойств **ResourceGroupName** , **DeploymentName** и **ProvisioningState** .</span><span class="sxs-lookup"><span data-stu-id="521f1-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="521f1-129">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="521f1-129">PARAMETERS</span></span>

### <span data-ttu-id="521f1-130">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="521f1-130">-ApiVersion</span></span>
<span data-ttu-id="521f1-131">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="521f1-131">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="521f1-132">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="521f1-132">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="521f1-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="521f1-133">-DefaultProfile</span></span>
<span data-ttu-id="521f1-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="521f1-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="521f1-135">-ID</span><span class="sxs-lookup"><span data-stu-id="521f1-135">-Id</span></span>
<span data-ttu-id="521f1-136">Указывает идентификатор развертывания группы ресурсов, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="521f1-136">Specifies the ID of the resource group deployment to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="521f1-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="521f1-137">-Name</span></span>
<span data-ttu-id="521f1-138">Указывает имя развертывания, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="521f1-138">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="521f1-139">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="521f1-139">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="521f1-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="521f1-140">-Pre</span></span>
<span data-ttu-id="521f1-141">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="521f1-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="521f1-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="521f1-142">-ResourceGroupName</span></span>
<span data-ttu-id="521f1-143">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="521f1-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="521f1-144">Командлет получает развертывание для группы ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="521f1-144">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="521f1-145">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="521f1-145">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="521f1-146">Этот параметр является обязательным, и вы можете указать только одну группу ресурсов в каждой команде.</span><span class="sxs-lookup"><span data-stu-id="521f1-146">This parameter is required and you can specify only one resource group in each command.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="521f1-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="521f1-147">CommonParameters</span></span>
<span data-ttu-id="521f1-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="521f1-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="521f1-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="521f1-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="521f1-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="521f1-150">INPUTS</span></span>

### <span data-ttu-id="521f1-151">Ничего</span><span class="sxs-lookup"><span data-stu-id="521f1-151">None</span></span>

## <span data-ttu-id="521f1-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="521f1-152">OUTPUTS</span></span>

### <span data-ttu-id="521f1-153">Microsoft. Azure. Commands. ResourceManagement. Models.</span><span class="sxs-lookup"><span data-stu-id="521f1-153">Microsoft.Azure.Commands.ResourceManagement.Models.</span></span> <span data-ttu-id="521f1-154">PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="521f1-154">PSResourceGroupDeployment</span></span>

## <span data-ttu-id="521f1-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="521f1-155">NOTES</span></span>

## <span data-ttu-id="521f1-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="521f1-156">RELATED LINKS</span></span>

[<span data-ttu-id="521f1-157">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="521f1-157">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="521f1-158">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="521f1-158">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="521f1-159">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="521f1-159">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="521f1-160">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="521f1-160">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="521f1-161">Остановить-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="521f1-161">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="521f1-162">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="521f1-162">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)

