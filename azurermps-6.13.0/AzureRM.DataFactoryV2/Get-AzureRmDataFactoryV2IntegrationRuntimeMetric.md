---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 07c5b03b3d5717115238e3cd66b9f80925b51537
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566519"
---
# <span data-ttu-id="3f262-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="3f262-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="3f262-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f262-102">SYNOPSIS</span></span>
<span data-ttu-id="3f262-103">Возвращает данные метрик для среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="3f262-103">Gets metric data for an integration runtime.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f262-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f262-104">SYNTAX</span></span>

### <span data-ttu-id="3f262-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3f262-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f262-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3f262-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f262-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="3f262-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f262-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f262-108">DESCRIPTION</span></span>
<span data-ttu-id="3f262-109">Командлет Get-AzureRmDataFactoryV2IntegrationRuntimeMetric получает данные метрик о среде выполнения интеграции в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="3f262-109">The Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="3f262-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f262-110">EXAMPLES</span></span>

### <span data-ttu-id="3f262-111">Пример 1: получение метрики среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="3f262-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="3f262-112">Эта команда отображает данные метрик о среде выполнения интеграции с именем Test-SelfHost-IR в подписке для группы ресурсов с именем "Test-DF-Eu2".</span><span class="sxs-lookup"><span data-stu-id="3f262-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="3f262-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f262-113">PARAMETERS</span></span>

### <span data-ttu-id="3f262-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3f262-114">-DataFactoryName</span></span>
<span data-ttu-id="3f262-115">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="3f262-115">The data factory name.</span></span>

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

### <span data-ttu-id="3f262-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f262-116">-DefaultProfile</span></span>
<span data-ttu-id="3f262-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f262-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f262-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f262-118">-InputObject</span></span>
<span data-ttu-id="3f262-119">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="3f262-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="3f262-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3f262-120">-Name</span></span>
<span data-ttu-id="3f262-121">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="3f262-121">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f262-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f262-122">-ResourceGroupName</span></span>
<span data-ttu-id="3f262-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3f262-123">The resource group name.</span></span>

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

### <span data-ttu-id="3f262-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f262-124">-ResourceId</span></span>
<span data-ttu-id="3f262-125">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="3f262-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3f262-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f262-126">CommonParameters</span></span>
<span data-ttu-id="3f262-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f262-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f262-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f262-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f262-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f262-129">INPUTS</span></span>

### <span data-ttu-id="3f262-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3f262-130">System.String</span></span>

### <span data-ttu-id="3f262-131">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3f262-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="3f262-132">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3f262-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="3f262-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f262-133">OUTPUTS</span></span>

### <span data-ttu-id="3f262-134">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeMetrics</span><span class="sxs-lookup"><span data-stu-id="3f262-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="3f262-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f262-135">NOTES</span></span>

## <span data-ttu-id="3f262-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f262-136">RELATED LINKS</span></span>

[<span data-ttu-id="3f262-137">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3f262-137">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
