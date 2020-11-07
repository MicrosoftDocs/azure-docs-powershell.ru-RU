---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: db1f78f3adec999cdf8839eb972a71595f6c15b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555848"
---
# <span data-ttu-id="70739-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="70739-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="70739-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="70739-102">SYNOPSIS</span></span>
<span data-ttu-id="70739-103">Отправляет элемент коллекции поставщика в хранилище.</span><span class="sxs-lookup"><span data-stu-id="70739-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="70739-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="70739-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70739-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="70739-105">DESCRIPTION</span></span>
<span data-ttu-id="70739-106">Отправляет элемент коллекции поставщика в хранилище.</span><span class="sxs-lookup"><span data-stu-id="70739-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="70739-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="70739-107">EXAMPLES</span></span>

### <span data-ttu-id="70739-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="70739-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="70739-109">Создание нового элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="70739-109">Create a new gallery item.</span></span>

## <span data-ttu-id="70739-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="70739-110">PARAMETERS</span></span>

### <span data-ttu-id="70739-111">-Force</span><span class="sxs-lookup"><span data-stu-id="70739-111">-Force</span></span>
<span data-ttu-id="70739-112">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="70739-112">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70739-113">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="70739-113">-GalleryItemUri</span></span>
<span data-ttu-id="70739-114">Универсальный код ресурса (URI) для файла JSON элемента коллекции.</span><span class="sxs-lookup"><span data-stu-id="70739-114">The URI to the gallery item JSON file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70739-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70739-115">-Confirm</span></span>
<span data-ttu-id="70739-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="70739-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70739-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70739-117">-WhatIf</span></span>
<span data-ttu-id="70739-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="70739-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70739-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="70739-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70739-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70739-120">CommonParameters</span></span>
<span data-ttu-id="70739-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="70739-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70739-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70739-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70739-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="70739-123">INPUTS</span></span>

## <span data-ttu-id="70739-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="70739-124">OUTPUTS</span></span>

### <span data-ttu-id="70739-125">Microsoft. AzureStack. Management. Gallery. admin. Model. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="70739-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="70739-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="70739-126">NOTES</span></span>

## <span data-ttu-id="70739-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="70739-127">RELATED LINKS</span></span>
