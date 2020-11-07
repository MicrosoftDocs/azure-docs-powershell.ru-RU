---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2528d9b4f9443d8857006b6fc1e94100b0b477ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555375"
---
# <span data-ttu-id="ef884-101">Get-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="ef884-101">Get-AzsIpPool</span></span>

## <span data-ttu-id="ef884-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef884-102">SYNOPSIS</span></span>
<span data-ttu-id="ef884-103">Возвращает список всех IP-пулов в определенном расположении.</span><span class="sxs-lookup"><span data-stu-id="ef884-103">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="ef884-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef884-104">SYNTAX</span></span>

### <span data-ttu-id="ef884-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ef884-105">List (Default)</span></span>
```
Get-AzsIpPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="ef884-106">Получить</span><span class="sxs-lookup"><span data-stu-id="ef884-106">Get</span></span>
```
Get-AzsIpPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="ef884-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef884-107">ResourceId</span></span>
```
Get-AzsIpPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ef884-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef884-108">DESCRIPTION</span></span>
<span data-ttu-id="ef884-109">Возвращает список всех IP-пулов в определенном расположении.</span><span class="sxs-lookup"><span data-stu-id="ef884-109">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="ef884-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef884-110">EXAMPLES</span></span>

### <span data-ttu-id="ef884-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ef884-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsIpPool
```

<span data-ttu-id="ef884-112">Получение всех пулов IP-адресов инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="ef884-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="ef884-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="ef884-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"
```

<span data-ttu-id="ef884-114">Получение пула IP-адресов инфраструктуры на основе имени.</span><span class="sxs-lookup"><span data-stu-id="ef884-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="ef884-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef884-115">PARAMETERS</span></span>

### <span data-ttu-id="ef884-116">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="ef884-116">-Filter</span></span>
<span data-ttu-id="ef884-117">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="ef884-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="ef884-118">-Location</span><span class="sxs-lookup"><span data-stu-id="ef884-118">-Location</span></span>
<span data-ttu-id="ef884-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="ef884-119">Location of the resource.</span></span>

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

### <span data-ttu-id="ef884-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ef884-120">-Name</span></span>
<span data-ttu-id="ef884-121">Имя пула IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="ef884-121">IP pool name.</span></span>

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

### <span data-ttu-id="ef884-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef884-122">-ResourceGroupName</span></span>
<span data-ttu-id="ef884-123">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ef884-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="ef884-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef884-124">-ResourceId</span></span>
<span data-ttu-id="ef884-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="ef884-125">The resource id.</span></span>

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

### <span data-ttu-id="ef884-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="ef884-126">-Skip</span></span>
<span data-ttu-id="ef884-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="ef884-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ef884-128">-Top</span><span class="sxs-lookup"><span data-stu-id="ef884-128">-Top</span></span>
<span data-ttu-id="ef884-129">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="ef884-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ef884-130">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="ef884-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ef884-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef884-131">CommonParameters</span></span>
<span data-ttu-id="ef884-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef884-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef884-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef884-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef884-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef884-134">INPUTS</span></span>

## <span data-ttu-id="ef884-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef884-135">OUTPUTS</span></span>

### <span data-ttu-id="ef884-136">Microsoft. AzureStack. Management. Fabric. admin. Models. IpPool</span><span class="sxs-lookup"><span data-stu-id="ef884-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.IpPool</span></span>

## <span data-ttu-id="ef884-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef884-137">NOTES</span></span>

## <span data-ttu-id="ef884-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef884-138">RELATED LINKS</span></span>
