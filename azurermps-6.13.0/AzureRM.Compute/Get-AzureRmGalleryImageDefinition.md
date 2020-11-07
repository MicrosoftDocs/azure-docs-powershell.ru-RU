---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: 75d30165c5dc5d69eabd08e89ad2577df82f7ebd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561071"
---
# <span data-ttu-id="46914-101">Get-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="46914-101">Get-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="46914-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="46914-102">SYNOPSIS</span></span>
<span data-ttu-id="46914-103">Получение и перечисление определений изображений в галерее.</span><span class="sxs-lookup"><span data-stu-id="46914-103">Get or list gallery image definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46914-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="46914-104">SYNTAX</span></span>

### <span data-ttu-id="46914-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="46914-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46914-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="46914-106">ResourceIdParameter</span></span>
```
Get-AzureRmGalleryImageDefinition [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46914-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46914-107">DESCRIPTION</span></span>
<span data-ttu-id="46914-108">Получение и перечисление определений изображений в галерее.</span><span class="sxs-lookup"><span data-stu-id="46914-108">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="46914-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="46914-109">EXAMPLES</span></span>

### <span data-ttu-id="46914-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="46914-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $image
```

<span data-ttu-id="46914-111">Получение определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="46914-111">Get the gallery image definition.</span></span>

## <span data-ttu-id="46914-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="46914-112">PARAMETERS</span></span>

### <span data-ttu-id="46914-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46914-113">-DefaultProfile</span></span>
<span data-ttu-id="46914-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="46914-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46914-115">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="46914-115">-GalleryName</span></span>
<span data-ttu-id="46914-116">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="46914-116">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46914-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="46914-117">-Name</span></span>
<span data-ttu-id="46914-118">Имя определения изображения коллекции.</span><span class="sxs-lookup"><span data-stu-id="46914-118">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46914-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46914-119">-ResourceGroupName</span></span>
<span data-ttu-id="46914-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="46914-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46914-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46914-121">-ResourceId</span></span>
<span data-ttu-id="46914-122">Идентификатор ресурса для определения изображения коллекции</span><span class="sxs-lookup"><span data-stu-id="46914-122">The resource ID for the gallery image definition</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46914-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46914-123">CommonParameters</span></span>
<span data-ttu-id="46914-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="46914-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46914-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46914-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46914-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="46914-126">INPUTS</span></span>

### <span data-ttu-id="46914-127">System. String</span><span class="sxs-lookup"><span data-stu-id="46914-127">System.String</span></span>

## <span data-ttu-id="46914-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="46914-128">OUTPUTS</span></span>

### <span data-ttu-id="46914-129">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="46914-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="46914-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="46914-130">NOTES</span></span>

## <span data-ttu-id="46914-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46914-131">RELATED LINKS</span></span>