---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
ms.openlocfilehash: a4c8e2687fd525b32ef3a9da3684a3da9f3c5717
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720420"
---
# <span data-ttu-id="c6e13-101">Update-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="c6e13-101">Update-AzMlWebService</span></span>

## <span data-ttu-id="c6e13-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c6e13-102">SYNOPSIS</span></span>
<span data-ttu-id="c6e13-103">Обновляет свойства существующего ресурса веб-службы.</span><span class="sxs-lookup"><span data-stu-id="c6e13-103">Updates properties of an existing web service resource.</span></span>

## <span data-ttu-id="c6e13-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c6e13-104">SYNTAX</span></span>

### <span data-ttu-id="c6e13-105">UpdateFromParameters</span><span class="sxs-lookup"><span data-stu-id="c6e13-105">UpdateFromParameters</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6e13-106">UpdateFromObject</span><span class="sxs-lookup"><span data-stu-id="c6e13-106">UpdateFromObject</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6e13-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6e13-107">DESCRIPTION</span></span>
<span data-ttu-id="c6e13-108">Командлет Update-AzMlWebService позволяет обновлять нестатические свойства веб-службы.</span><span class="sxs-lookup"><span data-stu-id="c6e13-108">The Update-AzMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="c6e13-109">Командлет работает как операция исправления.</span><span class="sxs-lookup"><span data-stu-id="c6e13-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="c6e13-110">Передача только тех свойств, которые вы хотите изменить.</span><span class="sxs-lookup"><span data-stu-id="c6e13-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="c6e13-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c6e13-111">EXAMPLES</span></span>

### <span data-ttu-id="c6e13-112">Пример 1: аргументы выборочного обновления</span><span class="sxs-lookup"><span data-stu-id="c6e13-112">Example 1: Selective update arguments</span></span>
```
Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="c6e13-113">Здесь мы изменим описание, основной ключ доступа и Активируй сбор диагностических сведений для всех трассировок во время выполнения для веб-службы.</span><span class="sxs-lookup"><span data-stu-id="c6e13-113">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="c6e13-114">Пример 2: обновление на основе экземпляра веб-службы</span><span class="sxs-lookup"><span data-stu-id="c6e13-114">Example 2: Update based on a web service instance</span></span>
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="c6e13-115">В примере сначала создается определение веб-службы, которое включает только поля, которые нужно обновить, а затем вызывает Update-AzMlWebService, чтобы применить их с помощью параметра ServiceUpdates.</span><span class="sxs-lookup"><span data-stu-id="c6e13-115">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="c6e13-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c6e13-116">PARAMETERS</span></span>

### <span data-ttu-id="c6e13-117">-Активы</span><span class="sxs-lookup"><span data-stu-id="c6e13-117">-Assets</span></span>
<span data-ttu-id="c6e13-118">Набор ресурсов (например, модулей, наборов данных), образующих веб-службу.</span><span class="sxs-lookup"><span data-stu-id="c6e13-118">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e13-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6e13-119">-DefaultProfile</span></span>
<span data-ttu-id="c6e13-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c6e13-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6e13-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="c6e13-121">-Description</span></span>
<span data-ttu-id="c6e13-122">Новое значение для описания веб-службы.</span><span class="sxs-lookup"><span data-stu-id="c6e13-122">The new value for the web service's description.</span></span>
<span data-ttu-id="c6e13-123">Это видно в схеме API службы Swagger.</span><span class="sxs-lookup"><span data-stu-id="c6e13-123">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e13-124">-Диагностика</span><span class="sxs-lookup"><span data-stu-id="c6e13-124">-Diagnostics</span></span>
<span data-ttu-id="c6e13-125">Параметры, управляющие сбором трассировок диагностики для веб-службы.</span><span class="sxs-lookup"><span data-stu-id="c6e13-125">The settings that control the diagnostics traces collection for the web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.DiagnosticsConfiguration
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e13-126">-Force</span><span class="sxs-lookup"><span data-stu-id="c6e13-126">-Force</span></span>
<span data-ttu-id="c6e13-127">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="c6e13-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c6e13-128">-Input</span><span class="sxs-lookup"><span data-stu-id="c6e13-128">-Input</span></span>
<span data-ttu-id="c6e13-129">Определение входных данных веб-службы, предоставленных в качестве конструкции схемы Swagger.</span><span class="sxs-lookup"><span data-stu-id="c6e13-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e13-130">-ReadOnly</span><span class="sxs-lookup"><span data-stu-id="c6e13-130">-IsReadOnly</span></span>
<span data-ttu-id="c6e13-131">Указывает на то, что эта веб-служба доступна только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c6e13-131">Specifies that this web service is readonly.</span></span>
<span data-ttu-id="c6e13-132">После того как вы задали этот параметр, веб-службу можно будет обновлять, в том числе изменить значение этого свойства, и удалить ее.</span><span class="sxs-lookup"><span data-stu-id="c6e13-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e13-133">-Keys</span><span class="sxs-lookup"><span data-stu-id="c6e13-133">-Keys</span></span>
<span data-ttu-id="c6e13-134">Обновляет один или оба клавиши доступа, используемые для проверки подлинности вызовов API среды выполнения службы.</span><span class="sxs-lookup"><span data-stu-id="c6e13-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e13-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c6e13-135">-Name</span></span>
<span data-ttu-id="c6e13-136">Имя ресурса веб-службы, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="c6e13-136">The name of the web service resource to be updated.</span></span>

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

### <span data-ttu-id="c6e13-137">-Output</span><span class="sxs-lookup"><span data-stu-id="c6e13-137">-Output</span></span>
<span data-ttu-id="c6e13-138">Определение выходных данных веб-службы, которые представлены в виде конструкции схемы Swagger.</span><span class="sxs-lookup"><span data-stu-id="c6e13-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e13-139">-Package</span><span class="sxs-lookup"><span data-stu-id="c6e13-139">-Package</span></span>
<span data-ttu-id="c6e13-140">Определение пакета графа, определяющего эту веб-службу.</span><span class="sxs-lookup"><span data-stu-id="c6e13-140">The definition of the graph package that defines this web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.GraphPackage
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e13-141">-Parameters</span><span class="sxs-lookup"><span data-stu-id="c6e13-141">-Parameters</span></span>
<span data-ttu-id="c6e13-142">Набор значений глобальных параметров, определенных для веб-службы, заданный в качестве имени глобального параметра — \> коллекция значений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c6e13-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="c6e13-143">Если значение по умолчанию не задано, параметр считается обязательным.</span><span class="sxs-lookup"><span data-stu-id="c6e13-143">If no default value is specified, the parameter is considered to be required.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e13-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6e13-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="c6e13-145">Обновляет конфигурацию конечной точки реального времени службы.</span><span class="sxs-lookup"><span data-stu-id="c6e13-145">Updates for the configuration of the service's realtime endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.RealtimeConfiguration
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e13-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6e13-146">-ResourceGroupName</span></span>
<span data-ttu-id="c6e13-147">Группа ресурсов, содержащая веб-службу, которую нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="c6e13-147">The resource group that contains the web service to be updated.</span></span>

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

### <span data-ttu-id="c6e13-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="c6e13-148">-ServiceUpdates</span></span>
<span data-ttu-id="c6e13-149">Набор обновлений, которые необходимо применить к веб-службе, указанной в качестве экземпляра определения веб-службы.</span><span class="sxs-lookup"><span data-stu-id="c6e13-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="c6e13-150">Изменяются только поля, не являющиеся статическими.</span><span class="sxs-lookup"><span data-stu-id="c6e13-150">Only non-static fields are modified.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: UpdateFromObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6e13-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c6e13-151">-StorageAccountKey</span></span>
<span data-ttu-id="c6e13-152">Поворачивает клавишу доступа для учетной записи хранения, связанной с веб-службой.</span><span class="sxs-lookup"><span data-stu-id="c6e13-152">Rotates the access key for the storage account associated with the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e13-153">-Title</span><span class="sxs-lookup"><span data-stu-id="c6e13-153">-Title</span></span>
<span data-ttu-id="c6e13-154">Новое значение заголовка веб-службы.</span><span class="sxs-lookup"><span data-stu-id="c6e13-154">The new value for the web service's title.</span></span>
<span data-ttu-id="c6e13-155">Это видно в схеме API службы Swagger.</span><span class="sxs-lookup"><span data-stu-id="c6e13-155">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e13-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6e13-156">-Confirm</span></span>
<span data-ttu-id="c6e13-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c6e13-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6e13-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6e13-158">-WhatIf</span></span>
<span data-ttu-id="c6e13-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c6e13-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6e13-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c6e13-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6e13-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6e13-161">CommonParameters</span></span>
<span data-ttu-id="c6e13-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c6e13-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6e13-163">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6e13-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6e13-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c6e13-164">INPUTS</span></span>

### <span data-ttu-id="c6e13-165">Microsoft. Azure. Management. MachineLearning. WebService. Models.</span><span class="sxs-lookup"><span data-stu-id="c6e13-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="c6e13-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6e13-166">OUTPUTS</span></span>

### <span data-ttu-id="c6e13-167">Microsoft. Azure. Management. MachineLearning. WebService. Models.</span><span class="sxs-lookup"><span data-stu-id="c6e13-167">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="c6e13-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="c6e13-168">NOTES</span></span>
<span data-ttu-id="c6e13-169">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="c6e13-169">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="c6e13-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6e13-170">RELATED LINKS</span></span>