---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 5988aed4ca0560daedc1470198e0b02975f18196
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392356"
---
# <span data-ttu-id="0bfad-101">New-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="0bfad-101">New-AzMlWebService</span></span>

## <span data-ttu-id="0bfad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bfad-102">SYNOPSIS</span></span>
<span data-ttu-id="0bfad-103">Создает веб-службу.</span><span class="sxs-lookup"><span data-stu-id="0bfad-103">Creates a new web service.</span></span>

## <span data-ttu-id="0bfad-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0bfad-104">SYNTAX</span></span>

### <span data-ttu-id="0bfad-105">CreateFromFile</span><span class="sxs-lookup"><span data-stu-id="0bfad-105">CreateFromFile</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bfad-106">CreateFromInstance</span><span class="sxs-lookup"><span data-stu-id="0bfad-106">CreateFromInstance</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0bfad-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0bfad-107">DESCRIPTION</span></span>
<span data-ttu-id="0bfad-108">Создает веб-службу машинного обучения Azure в существующей группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0bfad-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="0bfad-109">Если в группе ресурсов есть веб-служба с таким же именем, звонок будет обновяться, а существующая веб-служба будет перезаписана.</span><span class="sxs-lookup"><span data-stu-id="0bfad-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="0bfad-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0bfad-110">EXAMPLES</span></span>

### <span data-ttu-id="0bfad-111">Пример 1. Создание службы на основе определения Json</span><span class="sxs-lookup"><span data-stu-id="0bfad-111">Example 1: Create a new service from a Json file based definition</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="0bfad-112">Создает веб-службу машинного обучения Azure "mywebservicename" в группе myresourcegroup и регионЕ Южный Центр США на основе определения, представленного в файле json, на который имеется ссылка.</span><span class="sxs-lookup"><span data-stu-id="0bfad-112">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="0bfad-113">Пример 2. Создание службы из экземпляра объекта</span><span class="sxs-lookup"><span data-stu-id="0bfad-113">Example 2: Create a new service from an object instance</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="0bfad-114">Вы можете получить экземпляр объекта веб-службы, который нужно настроить перед публикацией в качестве ресурса, с помощью Import-AzMlWebService-управления.</span><span class="sxs-lookup"><span data-stu-id="0bfad-114">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="0bfad-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0bfad-115">PARAMETERS</span></span>

### <span data-ttu-id="0bfad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bfad-116">-DefaultProfile</span></span>
<span data-ttu-id="0bfad-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0bfad-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0bfad-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="0bfad-118">-DefinitionFile</span></span>
<span data-ttu-id="0bfad-119">Путь к файлу, содержащего определение формата JSON веб-службы.</span><span class="sxs-lookup"><span data-stu-id="0bfad-119">Specifies the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="0bfad-120">Последнюю спецификацию определения веб-службы можно найти в swagger spec в https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning области .</span><span class="sxs-lookup"><span data-stu-id="0bfad-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bfad-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0bfad-121">-Force</span></span>
<span data-ttu-id="0bfad-122">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="0bfad-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0bfad-123">-Location</span><span class="sxs-lookup"><span data-stu-id="0bfad-123">-Location</span></span>
<span data-ttu-id="0bfad-124">Регион веб-службы.</span><span class="sxs-lookup"><span data-stu-id="0bfad-124">The region of the web service.</span></span>
<span data-ttu-id="0bfad-125">Введите регион центра обработки данных Azure, например "Запад США" или "Юго-Восточная Азия".</span><span class="sxs-lookup"><span data-stu-id="0bfad-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="0bfad-126">Вы можете разместить веб-службу в любом регионе, который поддерживает ресурсы такого типа.</span><span class="sxs-lookup"><span data-stu-id="0bfad-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="0bfad-127">Веб-служба не должна быть в том же регионе, что и в подписке Azure, или в том же регионе, что и группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0bfad-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="0bfad-128">Группы ресурсов могут содержать веб-службы из разных регионов.</span><span class="sxs-lookup"><span data-stu-id="0bfad-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="0bfad-129">Чтобы определить, в каких регионах поддерживается каждый тип ресурсов, используйте Get-AzResourceProvider с помощью Get-AzResourceProvider параметра ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="0bfad-129">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bfad-130">-Name</span><span class="sxs-lookup"><span data-stu-id="0bfad-130">-Name</span></span>
<span data-ttu-id="0bfad-131">Имя веб-службы.</span><span class="sxs-lookup"><span data-stu-id="0bfad-131">The name for the web service.</span></span>
<span data-ttu-id="0bfad-132">Имя должно быть уникальным в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0bfad-132">The name must be unique in the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bfad-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="0bfad-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="0bfad-134">Определение для новой веб-службы, содержащее все свойства, которые ее составляют.</span><span class="sxs-lookup"><span data-stu-id="0bfad-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="0bfad-135">Этот параметр является required и представляет экземпляр класса Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span><span class="sxs-lookup"><span data-stu-id="0bfad-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="0bfad-136">Последнюю спецификацию определения веб-службы можно найти в swagger spec в https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json области .</span><span class="sxs-lookup"><span data-stu-id="0bfad-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: CreateFromInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0bfad-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bfad-137">-ResourceGroupName</span></span>
<span data-ttu-id="0bfad-138">Группа ресурсов, в которую нужно разместить веб-службу.</span><span class="sxs-lookup"><span data-stu-id="0bfad-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="0bfad-139">Введите регион центра обработки данных Azure, например "Запад США" или "Юго-Восточная Азия".</span><span class="sxs-lookup"><span data-stu-id="0bfad-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="0bfad-140">Вы можете разместить веб-службу в любом регионе, который поддерживает ресурсы такого типа.</span><span class="sxs-lookup"><span data-stu-id="0bfad-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="0bfad-141">Веб-служба не должна быть в том же регионе, что и в подписке Azure, или в том же регионе, что и группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0bfad-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="0bfad-142">Группы ресурсов могут содержать веб-службы из разных регионов.</span><span class="sxs-lookup"><span data-stu-id="0bfad-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="0bfad-143">Чтобы определить, в каких регионах поддерживается каждый тип ресурсов, используйте Get-AzResourceProvider с помощью Get-AzResourceProvider параметра ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="0bfad-143">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bfad-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0bfad-144">-Confirm</span></span>
<span data-ttu-id="0bfad-145">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0bfad-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bfad-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bfad-146">-WhatIf</span></span>
<span data-ttu-id="0bfad-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bfad-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bfad-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0bfad-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bfad-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bfad-149">CommonParameters</span></span>
<span data-ttu-id="0bfad-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bfad-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bfad-151">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bfad-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bfad-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0bfad-152">INPUTS</span></span>

### <span data-ttu-id="0bfad-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="0bfad-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="0bfad-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0bfad-154">OUTPUTS</span></span>

### <span data-ttu-id="0bfad-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="0bfad-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="0bfad-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0bfad-156">NOTES</span></span>
<span data-ttu-id="0bfad-157">Ключевые слова: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="0bfad-157">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="0bfad-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0bfad-158">RELATED LINKS</span></span>