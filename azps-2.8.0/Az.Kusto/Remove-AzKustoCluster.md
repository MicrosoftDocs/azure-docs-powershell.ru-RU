---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoCluster.md
ms.openlocfilehash: 3556ff99dafe804ab78899f8b0eefc64db4ca82b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720578"
---
# <span data-ttu-id="b345e-101">Remove-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="b345e-101">Remove-AzKustoCluster</span></span>

## <span data-ttu-id="b345e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b345e-102">SYNOPSIS</span></span>
<span data-ttu-id="b345e-103">Удаляет существующий кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="b345e-103">Deletes an existing Kusto cluster.</span></span>

## <span data-ttu-id="b345e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b345e-104">SYNTAX</span></span>

### <span data-ttu-id="b345e-105">ByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b345e-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b345e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b345e-106">ByResourceId</span></span>
```
Remove-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b345e-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b345e-107">ByInputObject</span></span>
```
Remove-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b345e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b345e-108">DESCRIPTION</span></span>
<span data-ttu-id="b345e-109">Удаляет существующий кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="b345e-109">Deletes an existing Kusto cluster.</span></span>

## <span data-ttu-id="b345e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b345e-110">EXAMPLES</span></span>

### <span data-ttu-id="b345e-111">Пример 1. Удалите существующий кластер Kusto по имени</span><span class="sxs-lookup"><span data-stu-id="b345e-111">Example 1 - Delete an existing Kusto cluster by name</span></span>

```
PS C:\> Remove-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="b345e-112">Приведенная выше команда удаляет кластер Kusto с именем "mykustocluster" в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="b345e-112">The above command deletes the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="b345e-113">Пример 2. Удаление существующего кластера Kusto с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="b345e-113">Example 2 - Delete an existing Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Remove-AzKustoCluster
```

<span data-ttu-id="b345e-114">В приведенной выше команде получается кластер Kusto с именем "mykustocluster" в группе ресурсов "testrg" с помощью `Get-AzKustoCluster` командлета, а затем `Remove-AzKustoCluster` продается результат, чтобы удалить его.</span><span class="sxs-lookup"><span data-stu-id="b345e-114">The above command gets the Kusto cluster named "mykustocluster" in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Remove-AzKustoCluster` to delete it.</span></span>

## <span data-ttu-id="b345e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b345e-115">PARAMETERS</span></span>

### <span data-ttu-id="b345e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b345e-116">-DefaultProfile</span></span>
<span data-ttu-id="b345e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b345e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b345e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b345e-118">-InputObject</span></span>
<span data-ttu-id="b345e-119">Объект Cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="b345e-119">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b345e-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b345e-120">-Name</span></span>
<span data-ttu-id="b345e-121">Имя кластера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="b345e-121">Name of cluster to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b345e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b345e-122">-PassThru</span></span>
<span data-ttu-id="b345e-123">Возвращают данные о том, был ли этот кластер успешно удален или нет.</span><span class="sxs-lookup"><span data-stu-id="b345e-123">Return whether the specified cluster was successfully deleted or not.</span></span>

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

### <span data-ttu-id="b345e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b345e-124">-ResourceGroupName</span></span>
<span data-ttu-id="b345e-125">Имя группы ресурсов, в которой находится кластер.</span><span class="sxs-lookup"><span data-stu-id="b345e-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b345e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b345e-126">-ResourceId</span></span>
<span data-ttu-id="b345e-127">Kusto Cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="b345e-127">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b345e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b345e-128">-Confirm</span></span>
<span data-ttu-id="b345e-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b345e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b345e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b345e-130">-WhatIf</span></span>
<span data-ttu-id="b345e-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b345e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b345e-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b345e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b345e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b345e-133">CommonParameters</span></span>
<span data-ttu-id="b345e-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b345e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b345e-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b345e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b345e-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b345e-136">INPUTS</span></span>

### <span data-ttu-id="b345e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b345e-137">System.String</span></span>

### <span data-ttu-id="b345e-138">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="b345e-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="b345e-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b345e-139">OUTPUTS</span></span>

### <span data-ttu-id="b345e-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b345e-140">System.Boolean</span></span>

## <span data-ttu-id="b345e-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="b345e-141">NOTES</span></span>

## <span data-ttu-id="b345e-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b345e-142">RELATED LINKS</span></span>