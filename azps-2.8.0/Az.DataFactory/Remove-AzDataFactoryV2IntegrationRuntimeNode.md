---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: dbf5b4eba8c6fe2dc55e55a58df79ed9b7d08afb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721464"
---
# <span data-ttu-id="8ff1d-101">Remove-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="8ff1d-101">Remove-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="8ff1d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ff1d-102">SYNOPSIS</span></span>
<span data-ttu-id="8ff1d-103">Удаление узла с заданным именем в среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="8ff1d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ff1d-104">SYNTAX</span></span>

### <span data-ttu-id="8ff1d-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8ff1d-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ff1d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8ff1d-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ff1d-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="8ff1d-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ff1d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ff1d-108">DESCRIPTION</span></span>
<span data-ttu-id="8ff1d-109">Командлет Remove-AzDataFactoryV2IntegrationRuntimeNode удаляет узел в среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-109">The Remove-AzDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="8ff1d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ff1d-110">EXAMPLES</span></span>

### <span data-ttu-id="8ff1d-111">Пример 1: Удаление узла из среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="8ff1d-111">Example 1: Remove a node from an integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="8ff1d-112">Эта команда удаляет узел с именем "Node_1" в среде выполнения интеграции с именем "Test-SelfHost-IR" в подписке для группы ресурсов с именем "Test-DF-Eu2".</span><span class="sxs-lookup"><span data-stu-id="8ff1d-112">This command removes an node named 'Node_1' in the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="8ff1d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ff1d-113">PARAMETERS</span></span>

### <span data-ttu-id="8ff1d-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8ff1d-114">-DataFactoryName</span></span>
<span data-ttu-id="8ff1d-115">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ff1d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ff1d-116">-DefaultProfile</span></span>
<span data-ttu-id="8ff1d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ff1d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8ff1d-118">-Force</span></span>
<span data-ttu-id="8ff1d-119">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="8ff1d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ff1d-120">-InputObject</span></span>
<span data-ttu-id="8ff1d-121">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-121">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ff1d-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="8ff1d-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="8ff1d-123">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ff1d-124">-NodeName</span><span class="sxs-lookup"><span data-stu-id="8ff1d-124">-NodeName</span></span>
<span data-ttu-id="8ff1d-125">Имя узла среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-125">The integration runtime node name.</span></span>

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

### <span data-ttu-id="8ff1d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ff1d-126">-ResourceGroupName</span></span>
<span data-ttu-id="8ff1d-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ff1d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ff1d-128">-ResourceId</span></span>
<span data-ttu-id="8ff1d-129">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-129">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ff1d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ff1d-130">-Confirm</span></span>
<span data-ttu-id="8ff1d-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ff1d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ff1d-132">-WhatIf</span></span>
<span data-ttu-id="8ff1d-133">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="8ff1d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ff1d-134">CommonParameters</span></span>
<span data-ttu-id="8ff1d-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ff1d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ff1d-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ff1d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ff1d-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ff1d-137">INPUTS</span></span>

### <span data-ttu-id="8ff1d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8ff1d-138">System.String</span></span>

### <span data-ttu-id="8ff1d-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8ff1d-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="8ff1d-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ff1d-140">OUTPUTS</span></span>

### <span data-ttu-id="8ff1d-141">System. void</span><span class="sxs-lookup"><span data-stu-id="8ff1d-141">System.Void</span></span>

## <span data-ttu-id="8ff1d-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ff1d-142">NOTES</span></span>

## <span data-ttu-id="8ff1d-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ff1d-143">RELATED LINKS</span></span>