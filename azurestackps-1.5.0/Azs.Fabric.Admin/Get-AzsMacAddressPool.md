---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5c686faa457d83ab0ddffb932b20ab5fcd168ff0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556204"
---
# <span data-ttu-id="ccd40-101">Get-AzsMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="ccd40-101">Get-AzsMacAddressPool</span></span>

## <span data-ttu-id="ccd40-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ccd40-102">SYNOPSIS</span></span>
<span data-ttu-id="ccd40-103">Возвращает список всех пулов MAC-адресов в местоположении.</span><span class="sxs-lookup"><span data-stu-id="ccd40-103">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="ccd40-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ccd40-104">SYNTAX</span></span>

### <span data-ttu-id="ccd40-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ccd40-105">List (Default)</span></span>
```
Get-AzsMacAddressPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="ccd40-106">Получить</span><span class="sxs-lookup"><span data-stu-id="ccd40-106">Get</span></span>
```
Get-AzsMacAddressPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="ccd40-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccd40-107">ResourceId</span></span>
```
Get-AzsMacAddressPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ccd40-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ccd40-108">DESCRIPTION</span></span>
<span data-ttu-id="ccd40-109">Возвращает список всех пулов MAC-адресов в местоположении.</span><span class="sxs-lookup"><span data-stu-id="ccd40-109">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="ccd40-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ccd40-110">EXAMPLES</span></span>

### <span data-ttu-id="ccd40-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ccd40-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsMacAddressPool
```

<span data-ttu-id="ccd40-112">Получение всех пулов MAC-адресов в местоположении.</span><span class="sxs-lookup"><span data-stu-id="ccd40-112">Get all MAC address pools at a location.</span></span>

### <span data-ttu-id="ccd40-113">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="ccd40-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsMacAddressPool -Name "8197fd09-8a69-417e-a55c-10c2c61f5ee7"
```

<span data-ttu-id="ccd40-114">Получение определенного пула MAC-адресов в местоположении на основе имени.</span><span class="sxs-lookup"><span data-stu-id="ccd40-114">Get a specific MAC address pool at a location based on name.</span></span>

## <span data-ttu-id="ccd40-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ccd40-115">PARAMETERS</span></span>

### <span data-ttu-id="ccd40-116">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="ccd40-116">-Filter</span></span>
<span data-ttu-id="ccd40-117">Параметр фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="ccd40-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="ccd40-118">-Location</span><span class="sxs-lookup"><span data-stu-id="ccd40-118">-Location</span></span>
<span data-ttu-id="ccd40-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="ccd40-119">Location of the resource.</span></span>

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

### <span data-ttu-id="ccd40-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ccd40-120">-Name</span></span>
<span data-ttu-id="ccd40-121">Имя пула MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="ccd40-121">Name of the MAC address pool.</span></span>

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

### <span data-ttu-id="ccd40-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccd40-122">-ResourceGroupName</span></span>
<span data-ttu-id="ccd40-123">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ccd40-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="ccd40-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccd40-124">-ResourceId</span></span>
<span data-ttu-id="ccd40-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="ccd40-125">The resource id.</span></span>

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

### <span data-ttu-id="ccd40-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="ccd40-126">-Skip</span></span>
<span data-ttu-id="ccd40-127">Пропуск первых N элементов, указанных в значении параметра.</span><span class="sxs-lookup"><span data-stu-id="ccd40-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ccd40-128">-Top</span><span class="sxs-lookup"><span data-stu-id="ccd40-128">-Top</span></span>
<span data-ttu-id="ccd40-129">Возвращает первые N элементов, заданные значением параметра.</span><span class="sxs-lookup"><span data-stu-id="ccd40-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ccd40-130">Действует после параметра-Skip.</span><span class="sxs-lookup"><span data-stu-id="ccd40-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ccd40-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccd40-131">CommonParameters</span></span>
<span data-ttu-id="ccd40-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ccd40-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccd40-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccd40-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccd40-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ccd40-134">INPUTS</span></span>

## <span data-ttu-id="ccd40-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ccd40-135">OUTPUTS</span></span>

### <span data-ttu-id="ccd40-136">Microsoft. AzureStack. Management. Fabric. admin. Models. MacAddressPool</span><span class="sxs-lookup"><span data-stu-id="ccd40-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.MacAddressPool</span></span>

## <span data-ttu-id="ccd40-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="ccd40-137">NOTES</span></span>

## <span data-ttu-id="ccd40-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ccd40-138">RELATED LINKS</span></span>
