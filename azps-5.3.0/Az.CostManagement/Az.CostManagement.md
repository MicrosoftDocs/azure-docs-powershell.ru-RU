---
Module Name: Az.CostManagement
Module Guid: 4cd9af10-559e-4fb9-8dcd-d3e8eb9e03b7
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Az.CostManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Az.CostManagement.md
ms.openlocfilehash: 0bfac4d12c15bef8b16e9ba239423b1443a9f5b7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508697"
---
# <span data-ttu-id="878ad-101">Az.CostManagement Module</span><span class="sxs-lookup"><span data-stu-id="878ad-101">Az.CostManagement Module</span></span>
## <span data-ttu-id="878ad-102">Описание</span><span class="sxs-lookup"><span data-stu-id="878ad-102">Description</span></span>
<span data-ttu-id="878ad-103">Microsoft Azure PowerShell: затраты</span><span class="sxs-lookup"><span data-stu-id="878ad-103">Microsoft Azure PowerShell: Cost cmdlets</span></span>

## <span data-ttu-id="878ad-104">Az.CostManagement Cmdlets</span><span class="sxs-lookup"><span data-stu-id="878ad-104">Az.CostManagement Cmdlets</span></span>
### [<span data-ttu-id="878ad-105">Get-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="878ad-105">Get-AzCostManagementExport</span></span>](Get-AzCostManagementExport.md)
<span data-ttu-id="878ad-106">Операция получения экспорта для определенной области по имени экспорта.</span><span class="sxs-lookup"><span data-stu-id="878ad-106">The operation to get the export for the defined scope by export name.</span></span>

### [<span data-ttu-id="878ad-107">Get-AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="878ad-107">Get-AzCostManagementExportExecutionHistory</span></span>](Get-AzCostManagementExportExecutionHistory.md)
<span data-ttu-id="878ad-108">Операция получения истории выполнения экспорта для определенной области и имени экспорта.</span><span class="sxs-lookup"><span data-stu-id="878ad-108">The operation to get the execution history of an export for the defined scope and export name.</span></span>

### [<span data-ttu-id="878ad-109">Invoke-AzCostManagementExecuteExport</span><span class="sxs-lookup"><span data-stu-id="878ad-109">Invoke-AzCostManagementExecuteExport</span></span>](Invoke-AzCostManagementExecuteExport.md)
<span data-ttu-id="878ad-110">Операция экспорта.</span><span class="sxs-lookup"><span data-stu-id="878ad-110">The operation to execute an export.</span></span>

### [<span data-ttu-id="878ad-111">Invoke-AzCostManagementQuery</span><span class="sxs-lookup"><span data-stu-id="878ad-111">Invoke-AzCostManagementQuery</span></span>](Invoke-AzCostManagementQuery.md)
<span data-ttu-id="878ad-112">Запрос данных об использовании для определенной области.</span><span class="sxs-lookup"><span data-stu-id="878ad-112">Query the usage data for scope defined.</span></span>

### [<span data-ttu-id="878ad-113">New-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="878ad-113">New-AzCostManagementExport</span></span>](New-AzCostManagementExport.md)
<span data-ttu-id="878ad-114">Операция создания или обновления экспорта.</span><span class="sxs-lookup"><span data-stu-id="878ad-114">The operation to create or update a export.</span></span>
<span data-ttu-id="878ad-115">Для обновления требуется установить в запросе последнюю версию eTag.</span><span class="sxs-lookup"><span data-stu-id="878ad-115">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="878ad-116">Вы можете получить последнюю версию eTag, выполив получение.</span><span class="sxs-lookup"><span data-stu-id="878ad-116">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="878ad-117">Для создания операции не требуется eTag.</span><span class="sxs-lookup"><span data-stu-id="878ad-117">Create operation does not require eTag.</span></span>

### [<span data-ttu-id="878ad-118">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="878ad-118">New-AzCostManagementQueryComparisonExpressionObject</span></span>](New-AzCostManagementQueryComparisonExpressionObject.md)
<span data-ttu-id="878ad-119">Создание объекта в памяти для запросаComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="878ad-119">Create a in-memory object for QueryComparisonExpression</span></span>

### [<span data-ttu-id="878ad-120">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="878ad-120">New-AzCostManagementQueryFilterObject</span></span>](New-AzCostManagementQueryFilterObject.md)
<span data-ttu-id="878ad-121">Создание объекта в памяти для queryFilter</span><span class="sxs-lookup"><span data-stu-id="878ad-121">Create a in-memory object for QueryFilter</span></span>

### [<span data-ttu-id="878ad-122">Remove-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="878ad-122">Remove-AzCostManagementExport</span></span>](Remove-AzCostManagementExport.md)
<span data-ttu-id="878ad-123">Операция удаления экспорта.</span><span class="sxs-lookup"><span data-stu-id="878ad-123">The operation to delete a export.</span></span>

### [<span data-ttu-id="878ad-124">Update-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="878ad-124">Update-AzCostManagementExport</span></span>](Update-AzCostManagementExport.md)
<span data-ttu-id="878ad-125">Операция создания или обновления экспорта.</span><span class="sxs-lookup"><span data-stu-id="878ad-125">The operation to create or update a export.</span></span>
<span data-ttu-id="878ad-126">Для обновления требуется установить в запросе последнюю версию eTag.</span><span class="sxs-lookup"><span data-stu-id="878ad-126">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="878ad-127">Вы можете получить последнюю версию eTag, выполив получение.</span><span class="sxs-lookup"><span data-stu-id="878ad-127">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="878ad-128">Для создания операции не требуется eTag.</span><span class="sxs-lookup"><span data-stu-id="878ad-128">Create operation does not require eTag.</span></span>
