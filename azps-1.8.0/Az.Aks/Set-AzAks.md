---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAks.md
ms.openlocfilehash: 9b63ede0bbd24adb98159ca6cfee08238b26aabc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720215"
---
# <span data-ttu-id="74832-101">Set-AzAks</span><span class="sxs-lookup"><span data-stu-id="74832-101">Set-AzAks</span></span>

## <span data-ttu-id="74832-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74832-102">SYNOPSIS</span></span>
<span data-ttu-id="74832-103">Обновите или создайте управляемый кластер Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="74832-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="74832-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74832-104">SYNTAX</span></span>

### <span data-ttu-id="74832-105">defaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="74832-105">defaultParameterSet (Default)</span></span>
```
Set-AzAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74832-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74832-106">InputObjectParameterSet</span></span>
```
Set-AzAks -InputObject <PSKubernetesCluster> [-Location <String>] [-AdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74832-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="74832-107">IdParameterSet</span></span>
```
Set-AzAks [-Id] <String> [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74832-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74832-108">DESCRIPTION</span></span>
<span data-ttu-id="74832-109">Обновите или создайте управляемый кластер Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="74832-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="74832-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74832-110">EXAMPLES</span></span>

### <span data-ttu-id="74832-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="74832-111">Example 1</span></span>
```
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="74832-112">Установите количество узлов в кластере Kubernetes равным 5.</span><span class="sxs-lookup"><span data-stu-id="74832-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="74832-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74832-113">PARAMETERS</span></span>

### <span data-ttu-id="74832-114">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="74832-114">-AdminUserName</span></span>
<span data-ttu-id="74832-115">Имя пользователя для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="74832-115">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="74832-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74832-116">-AsJob</span></span>
<span data-ttu-id="74832-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="74832-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74832-118">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="74832-118">-ClientIdAndSecret</span></span>
<span data-ttu-id="74832-119">Идентификатор клиента и секрет клиента, связанные с приложением или участником-службой AAD.</span><span class="sxs-lookup"><span data-stu-id="74832-119">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: defaultParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74832-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74832-120">-DefaultProfile</span></span>
<span data-ttu-id="74832-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74832-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74832-122">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="74832-122">-DnsNamePrefix</span></span>
<span data-ttu-id="74832-123">Префикс DNS-имени для кластера.</span><span class="sxs-lookup"><span data-stu-id="74832-123">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="74832-124">-ID</span><span class="sxs-lookup"><span data-stu-id="74832-124">-Id</span></span>
<span data-ttu-id="74832-125">Идентификатор управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="74832-125">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74832-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74832-126">-InputObject</span></span>
<span data-ttu-id="74832-127">Объект PSKubernetesCluster, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="74832-127">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74832-128">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="74832-128">-KubernetesVersion</span></span>
<span data-ttu-id="74832-129">Версия Kubernetes, используемая для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="74832-129">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="74832-130">-Location</span><span class="sxs-lookup"><span data-stu-id="74832-130">-Location</span></span>
<span data-ttu-id="74832-131">Расположение Azure для кластера.</span><span class="sxs-lookup"><span data-stu-id="74832-131">Azure location for the cluster.</span></span>
<span data-ttu-id="74832-132">По умолчанию — расположение группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="74832-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="74832-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="74832-133">-Name</span></span>
<span data-ttu-id="74832-134">Имя управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="74832-134">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74832-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="74832-135">-NodeCount</span></span>
<span data-ttu-id="74832-136">Количество узлов, используемое по умолчанию для пулов узлов.</span><span class="sxs-lookup"><span data-stu-id="74832-136">The default number of nodes for the node pools.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74832-137">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="74832-137">-NodeOsDiskSize</span></span>
<span data-ttu-id="74832-138">Количество узлов, используемое по умолчанию для пулов узлов.</span><span class="sxs-lookup"><span data-stu-id="74832-138">The default number of nodes for the node pools.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74832-139">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="74832-139">-NodeVmSize</span></span>
<span data-ttu-id="74832-140">Размер виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="74832-140">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="74832-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74832-141">-ResourceGroupName</span></span>
<span data-ttu-id="74832-142">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="74832-142">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74832-143">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="74832-143">-SshKeyValue</span></span>
<span data-ttu-id="74832-144">Значение файла ключа SSH или путь к файлу ключа.</span><span class="sxs-lookup"><span data-stu-id="74832-144">SSH key file value or key file path.</span></span>
<span data-ttu-id="74832-145">По умолчанию: {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="74832-145">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74832-146">-Тег</span><span class="sxs-lookup"><span data-stu-id="74832-146">-Tag</span></span>
<span data-ttu-id="74832-147">Теги, применяемые к ресурсу</span><span class="sxs-lookup"><span data-stu-id="74832-147">Tags to be applied to the resource</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74832-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74832-148">-Confirm</span></span>
<span data-ttu-id="74832-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="74832-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74832-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74832-150">-WhatIf</span></span>
<span data-ttu-id="74832-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="74832-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74832-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="74832-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74832-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74832-153">CommonParameters</span></span>
<span data-ttu-id="74832-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74832-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74832-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74832-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74832-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74832-156">INPUTS</span></span>

### <span data-ttu-id="74832-157">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="74832-157">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="74832-158">System. String</span><span class="sxs-lookup"><span data-stu-id="74832-158">System.String</span></span>

## <span data-ttu-id="74832-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74832-159">OUTPUTS</span></span>

### <span data-ttu-id="74832-160">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="74832-160">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="74832-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="74832-161">NOTES</span></span>

## <span data-ttu-id="74832-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74832-162">RELATED LINKS</span></span>