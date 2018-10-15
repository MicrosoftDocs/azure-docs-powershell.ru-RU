---
title: Выходные данные запроса командлетов Azure PowerShell
description: Как обратиться к ресурсам в Azure и форматировать результаты запроса.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: da8c8f37d8c60e9555b4627a7b5c3d1d6e7888fa
ms.sourcegitcommit: a749eb729f583c9d0dd86141bbd04984d77ae9ab
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/11/2018
ms.locfileid: "48889263"
---
# <a name="query-output-of-azure-powershell-cmdlets"></a><span data-ttu-id="31df2-103">Выходные данные запроса командлетов Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="31df2-103">Query output of Azure PowerShell cmdlets</span></span>

<span data-ttu-id="31df2-104">Вы можете обращаться к ресурсам с помощью встроенных командлетов PowerShell.</span><span class="sxs-lookup"><span data-stu-id="31df2-104">Querying in PowerShell can be completed by using built-in cmdlets.</span></span> <span data-ttu-id="31df2-105">В PowerShell имена командлетов представлены в формате **_глагол-существительное_**.</span><span class="sxs-lookup"><span data-stu-id="31df2-105">In PowerShell, cmdlet names take the form of **_Verb-Noun_**.</span></span> <span data-ttu-id="31df2-106">Командлеты, в которых используется глагол **_Get_** (Получить) — это командлеты запроса.</span><span class="sxs-lookup"><span data-stu-id="31df2-106">The cmdlets using the verb **_Get_** are the query cmdlets.</span></span> <span data-ttu-id="31df2-107">Существительные командлета — это типы ресурсов Azure, к которым будет применено действие командлета.</span><span class="sxs-lookup"><span data-stu-id="31df2-107">The cmdlet nouns are the types of Azure resources that are acted upon by the cmdlet verbs.</span></span>

## <a name="select-simple-properties"></a><span data-ttu-id="31df2-108">Выбор простых свойств</span><span class="sxs-lookup"><span data-stu-id="31df2-108">Select simple properties</span></span>

<span data-ttu-id="31df2-109">Для каждого командлета Azure PowerShell определено форматирование по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="31df2-109">Azure PowerShell has default formatting defined for each cmdlet.</span></span> <span data-ttu-id="31df2-110">Самые распространенные свойства каждого типа ресурсов автоматически отображаются в формате таблицы или списка.</span><span class="sxs-lookup"><span data-stu-id="31df2-110">The most common properties for each resource type are displayed in a table or list format automatically.</span></span> <span data-ttu-id="31df2-111">Дополнительные сведения о форматировании выходных данных см. в статье о [форматировании результатов запроса](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="31df2-111">For more information about formatting output, see [Formatting query results](formatting-output.md).</span></span>

<span data-ttu-id="31df2-112">Используйте командлет `Get-AzureRmVM`, чтобы получить список виртуальных машин своей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="31df2-112">Use the `Get-AzureRmVM` cmdlet to query for a list of VMs in your account.</span></span>

```azurepowershell-interactive
Get-AzureRmVM
```

<span data-ttu-id="31df2-113">Результаты по умолчанию автоматически форматируются в виде таблицы.</span><span class="sxs-lookup"><span data-stu-id="31df2-113">The default output is automatically formatted as a table.</span></span>

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="31df2-114">Командлет `Select-Object` можно использовать для выбора определенных свойств, которые вас интересуют.</span><span class="sxs-lookup"><span data-stu-id="31df2-114">The `Select-Object` cmdlet can be used to select the specific properties that are interesting to you.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="select-complex-nested-properties"></a><span data-ttu-id="31df2-115">Выбор сложных вложенных свойств</span><span class="sxs-lookup"><span data-stu-id="31df2-115">Select complex nested properties</span></span>

<span data-ttu-id="31df2-116">Если требуется выбрать свойство, вложенное в выходные данные JSON, укажите полный путь к такому свойству.</span><span class="sxs-lookup"><span data-stu-id="31df2-116">If the property you want is nested in the JSON output, you need to supply the full path to the property.</span></span> <span data-ttu-id="31df2-117">Следующий пример показывает, как выбрать имя виртуальной машины и тип ОС с помощью командлета `Get-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="31df2-117">The following example shows how to select the VM Name and the OS type from the `Get-AzureRmVM` cmdlet.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-results-with-the-where-object-cmdlet"></a><span data-ttu-id="31df2-118">Фильтрация результатов с помощью командлета Where-Object</span><span class="sxs-lookup"><span data-stu-id="31df2-118">Filter results with the Where-Object cmdlet</span></span>

<span data-ttu-id="31df2-119">Командлет `Where-Object` позволяет фильтровать результаты на основе любого значения свойства.</span><span class="sxs-lookup"><span data-stu-id="31df2-119">The `Where-Object` cmdlet allows you to filter the result based on any property value.</span></span> <span data-ttu-id="31df2-120">В следующем примере фильтр выбирает только виртуальные машины, имя которых содержит текст RGD.</span><span class="sxs-lookup"><span data-stu-id="31df2-120">In the following example, the filter selects only VMs that have the text "RGD" in their name.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

<span data-ttu-id="31df2-121">В следующем примере результаты вернут виртуальные машины размера Standard_DS1_V2.</span><span class="sxs-lookup"><span data-stu-id="31df2-121">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1_V2'.</span></span>

```azurepowershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```