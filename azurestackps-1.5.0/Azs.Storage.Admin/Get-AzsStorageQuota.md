---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e4277ee88af840674d6fc8e4e2d5f614e745ace
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555532"
---
# <span data-ttu-id="142e3-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="142e3-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="142e3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="142e3-102">SYNOPSIS</span></span>
<span data-ttu-id="142e3-103">Возвращает список квот хранилища в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="142e3-103">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="142e3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="142e3-104">SYNTAX</span></span>

### <span data-ttu-id="142e3-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="142e3-105">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="142e3-106">Получить</span><span class="sxs-lookup"><span data-stu-id="142e3-106">Get</span></span>
```
Get-AzsStorageQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="142e3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="142e3-107">ResourceId</span></span>
```
Get-AzsStorageQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="142e3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="142e3-108">DESCRIPTION</span></span>
<span data-ttu-id="142e3-109">Возвращает список квот хранилища в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="142e3-109">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="142e3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="142e3-110">EXAMPLES</span></span>

### <span data-ttu-id="142e3-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="142e3-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageQuota
```

<span data-ttu-id="142e3-112">Получите список квот хранилища.</span><span class="sxs-lookup"><span data-stu-id="142e3-112">Get the list of storage quotas.</span></span>

### <span data-ttu-id="142e3-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="142e3-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageQuota -Name "storagequota1"
```

<span data-ttu-id="142e3-114">Получение сведений об указанной квоте хранилища по имени.</span><span class="sxs-lookup"><span data-stu-id="142e3-114">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="142e3-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="142e3-115">PARAMETERS</span></span>

### <span data-ttu-id="142e3-116">-Location</span><span class="sxs-lookup"><span data-stu-id="142e3-116">-Location</span></span>
<span data-ttu-id="142e3-117">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="142e3-117">Resource location.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="142e3-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="142e3-118">-Name</span></span>
<span data-ttu-id="142e3-119">Имя квоты хранилища.</span><span class="sxs-lookup"><span data-stu-id="142e3-119">The name of the storage quota.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="142e3-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="142e3-120">-ResourceId</span></span>
<span data-ttu-id="142e3-121">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="142e3-121">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="142e3-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="142e3-122">-Skip</span></span>
<span data-ttu-id="142e3-123">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="142e3-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="142e3-124">-Top</span><span class="sxs-lookup"><span data-stu-id="142e3-124">-Top</span></span>
<span data-ttu-id="142e3-125">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="142e3-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="142e3-126">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="142e3-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="142e3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="142e3-127">CommonParameters</span></span>
<span data-ttu-id="142e3-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="142e3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="142e3-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="142e3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="142e3-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="142e3-130">INPUTS</span></span>

## <span data-ttu-id="142e3-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="142e3-131">OUTPUTS</span></span>

### <span data-ttu-id="142e3-132">Microsoft. AzureStack. Management. Storage. admin. Models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="142e3-132">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="142e3-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="142e3-133">NOTES</span></span>

## <span data-ttu-id="142e3-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="142e3-134">RELATED LINKS</span></span>
