---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/add-azmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
ms.openlocfilehash: 877ef93dbecf3510887a24cb0b5dfe65948658f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720462"
---
# <span data-ttu-id="f6ff9-101">Add-AzMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="f6ff9-101">Add-AzMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="f6ff9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6ff9-102">SYNOPSIS</span></span>
<span data-ttu-id="f6ff9-103">Создание свойств региональных веб-служб.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-103">Creates regional web service properties.</span></span>

## <span data-ttu-id="f6ff9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6ff9-104">SYNTAX</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6ff9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6ff9-105">DESCRIPTION</span></span>
<span data-ttu-id="f6ff9-106">Создание региональных свойств для службы машинного обучения Azure для существующей веб-службы.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="f6ff9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6ff9-107">EXAMPLES</span></span>

### <span data-ttu-id="f6ff9-108">Пример 1: Добавление новых региональных свойств для "Западная Центральная США"</span><span class="sxs-lookup"><span data-stu-id="f6ff9-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="f6ff9-109">Этот пример команды создает региональное свойство для веб-службы в регионе "Западная Центральная часть США".</span><span class="sxs-lookup"><span data-stu-id="f6ff9-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="f6ff9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6ff9-110">PARAMETERS</span></span>

### <span data-ttu-id="f6ff9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6ff9-111">-DefaultProfile</span></span>
<span data-ttu-id="f6ff9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f6ff9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6ff9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f6ff9-113">-Force</span></span>
<span data-ttu-id="f6ff9-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f6ff9-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f6ff9-115">-Name</span></span>
<span data-ttu-id="f6ff9-116">Имя веб-службы.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-116">The name for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6ff9-117">-Region (регион)</span><span class="sxs-lookup"><span data-stu-id="f6ff9-117">-Region</span></span>
<span data-ttu-id="f6ff9-118">Область, в которой нужно создать свойства веб-службы.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-118">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="f6ff9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6ff9-119">-ResourceGroupName</span></span>
<span data-ttu-id="f6ff9-120">Группа ресурсов, к которой принадлежит веб-служба.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-120">The resource group in which the web service belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6ff9-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6ff9-121">-Confirm</span></span>
<span data-ttu-id="f6ff9-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6ff9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6ff9-123">-WhatIf</span></span>
<span data-ttu-id="f6ff9-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6ff9-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6ff9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6ff9-126">CommonParameters</span></span>
<span data-ttu-id="f6ff9-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6ff9-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6ff9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6ff9-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6ff9-129">INPUTS</span></span>

### <span data-ttu-id="f6ff9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f6ff9-130">System.String</span></span>

## <span data-ttu-id="f6ff9-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6ff9-131">OUTPUTS</span></span>

### <span data-ttu-id="f6ff9-132">Microsoft. Azure. Management. MachineLearning. WebService. Models.</span><span class="sxs-lookup"><span data-stu-id="f6ff9-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="f6ff9-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6ff9-133">NOTES</span></span>
<span data-ttu-id="f6ff9-134">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="f6ff9-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f6ff9-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6ff9-135">RELATED LINKS</span></span>