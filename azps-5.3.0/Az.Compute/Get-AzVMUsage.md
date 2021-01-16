---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: d22e36ad3cc4737be9c73d6b7cdc49329f904263
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509146"
---
# <span data-ttu-id="e5f55-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="e5f55-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="e5f55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5f55-102">SYNOPSIS</span></span>
<span data-ttu-id="e5f55-103">Возвращает количество основных ядер виртуальных машин в расположении.</span><span class="sxs-lookup"><span data-stu-id="e5f55-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="e5f55-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e5f55-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5f55-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5f55-105">DESCRIPTION</span></span>
<span data-ttu-id="e5f55-106">Для определения местоположения с его **использованием** возвращается количество ядер виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="e5f55-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="e5f55-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e5f55-107">EXAMPLES</span></span>

### <span data-ttu-id="e5f55-108">Пример 1. Получить основные данные об использовании для расположения</span><span class="sxs-lookup"><span data-stu-id="e5f55-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="e5f55-109">Эта команда возвращает количество ядер виртуальных машин в центральной части США.</span><span class="sxs-lookup"><span data-stu-id="e5f55-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="e5f55-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5f55-110">PARAMETERS</span></span>

### <span data-ttu-id="e5f55-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5f55-111">-DefaultProfile</span></span>
<span data-ttu-id="e5f55-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5f55-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5f55-113">-Location</span><span class="sxs-lookup"><span data-stu-id="e5f55-113">-Location</span></span>
<span data-ttu-id="e5f55-114">Определяет место, для которого этот cmdlet получает использование виртуальных ядер виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="e5f55-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5f55-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5f55-115">CommonParameters</span></span>
<span data-ttu-id="e5f55-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5f55-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5f55-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5f55-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5f55-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5f55-118">INPUTS</span></span>

### <span data-ttu-id="e5f55-119">System.String</span><span class="sxs-lookup"><span data-stu-id="e5f55-119">System.String</span></span>

## <span data-ttu-id="e5f55-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e5f55-120">OUTPUTS</span></span>

### <span data-ttu-id="e5f55-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="e5f55-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="e5f55-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e5f55-122">NOTES</span></span>

## <span data-ttu-id="e5f55-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5f55-123">RELATED LINKS</span></span>

[<span data-ttu-id="e5f55-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e5f55-124">Get-AzVM</span></span>](./Get-AzVM.md)

