---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 70ee408b65839e46e408256780a6d705c9881bde
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555188"
---
# <span data-ttu-id="40990-101">Disable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="40990-101">Disable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="40990-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40990-102">SYNOPSIS</span></span>
<span data-ttu-id="40990-103">Запуск режима обслуживания для узла масштабируемой единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="40990-103">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="40990-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40990-104">SYNTAX</span></span>

### <span data-ttu-id="40990-105">Отключить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="40990-105">Disable (Default)</span></span>
```
Disable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40990-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="40990-106">ResourceId</span></span>
```
Disable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40990-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40990-107">DESCRIPTION</span></span>
<span data-ttu-id="40990-108">Запуск режима обслуживания для узла масштабируемой единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="40990-108">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="40990-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40990-109">EXAMPLES</span></span>

### <span data-ttu-id="40990-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="40990-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Disable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="40990-111">Включение режима обслуживания для узла масштабируемой единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="40990-111">Enable maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="40990-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40990-112">PARAMETERS</span></span>

### <span data-ttu-id="40990-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40990-113">-AsJob</span></span>
<span data-ttu-id="40990-114">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="40990-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="40990-115">-Force</span><span class="sxs-lookup"><span data-stu-id="40990-115">-Force</span></span>
<span data-ttu-id="40990-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="40990-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="40990-117">-Location</span><span class="sxs-lookup"><span data-stu-id="40990-117">-Location</span></span>
<span data-ttu-id="40990-118">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="40990-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40990-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="40990-119">-Name</span></span>
<span data-ttu-id="40990-120">Имя узла единиц масштабирования.</span><span class="sxs-lookup"><span data-stu-id="40990-120">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40990-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40990-121">-ResourceGroupName</span></span>
<span data-ttu-id="40990-122">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="40990-122">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40990-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40990-123">-ResourceId</span></span>
<span data-ttu-id="40990-124">Идентификатор ресурса узла единицы масштабирования.</span><span class="sxs-lookup"><span data-stu-id="40990-124">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="40990-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40990-125">-Confirm</span></span>
<span data-ttu-id="40990-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="40990-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40990-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40990-127">-WhatIf</span></span>
<span data-ttu-id="40990-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="40990-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40990-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="40990-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40990-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40990-130">CommonParameters</span></span>
<span data-ttu-id="40990-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40990-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40990-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40990-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40990-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40990-133">INPUTS</span></span>

## <span data-ttu-id="40990-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40990-134">OUTPUTS</span></span>

## <span data-ttu-id="40990-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="40990-135">NOTES</span></span>

## <span data-ttu-id="40990-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40990-136">RELATED LINKS</span></span>
