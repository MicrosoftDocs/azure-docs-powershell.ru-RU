---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86b9e7574344e1b4724648ce55fa2e36aed6591b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555347"
---
# <span data-ttu-id="83981-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="83981-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="83981-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="83981-102">SYNOPSIS</span></span>
<span data-ttu-id="83981-103">Возвращает список всех файловых ресурсов структуры в определенном расположении.</span><span class="sxs-lookup"><span data-stu-id="83981-103">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="83981-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="83981-104">SYNTAX</span></span>

### <span data-ttu-id="83981-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="83981-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="83981-106">Получить</span><span class="sxs-lookup"><span data-stu-id="83981-106">Get</span></span>
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="83981-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="83981-107">ResourceId</span></span>
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="83981-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="83981-108">DESCRIPTION</span></span>
<span data-ttu-id="83981-109">Возвращает список всех файловых ресурсов структуры в определенном расположении.</span><span class="sxs-lookup"><span data-stu-id="83981-109">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="83981-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="83981-110">EXAMPLES</span></span>

### <span data-ttu-id="83981-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="83981-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureShare
```

<span data-ttu-id="83981-112">Возвращает список всех общих файловых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83981-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="83981-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="83981-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

<span data-ttu-id="83981-114">Возвращает общую файловую систему на основе имени.</span><span class="sxs-lookup"><span data-stu-id="83981-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="83981-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="83981-115">PARAMETERS</span></span>

### <span data-ttu-id="83981-116">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="83981-116">-Filter</span></span>
<span data-ttu-id="83981-117">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="83981-117">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83981-118">-Location</span><span class="sxs-lookup"><span data-stu-id="83981-118">-Location</span></span>
<span data-ttu-id="83981-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="83981-119">Location of the resource.</span></span>

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

### <span data-ttu-id="83981-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="83981-120">-Name</span></span>
<span data-ttu-id="83981-121">Имя общего файлового файла структуры.</span><span class="sxs-lookup"><span data-stu-id="83981-121">Fabric file share name.</span></span>

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

### <span data-ttu-id="83981-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83981-122">-ResourceGroupName</span></span>
<span data-ttu-id="83981-123">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83981-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="83981-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83981-124">-ResourceId</span></span>
<span data-ttu-id="83981-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="83981-125">The resource id.</span></span>

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

### <span data-ttu-id="83981-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83981-126">CommonParameters</span></span>
<span data-ttu-id="83981-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="83981-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83981-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83981-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83981-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="83981-129">INPUTS</span></span>

## <span data-ttu-id="83981-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="83981-130">OUTPUTS</span></span>

### <span data-ttu-id="83981-131">Microsoft. AzureStack. Management. Fabric. admin. Models. \ мои</span><span class="sxs-lookup"><span data-stu-id="83981-131">Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare</span></span>

## <span data-ttu-id="83981-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="83981-132">NOTES</span></span>

## <span data-ttu-id="83981-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="83981-133">RELATED LINKS</span></span>
