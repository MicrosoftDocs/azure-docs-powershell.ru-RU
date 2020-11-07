---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f5a52ebfe2d59a200add1c8f763f7a3cafa59c18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555864"
---
# <span data-ttu-id="9a71d-101">Start-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="9a71d-101">Start-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="9a71d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9a71d-102">SYNOPSIS</span></span>
<span data-ttu-id="9a71d-103">Постепенный экземпляр роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="9a71d-103">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="9a71d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9a71d-104">SYNTAX</span></span>

### <span data-ttu-id="9a71d-105">PowerOn (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9a71d-105">PowerOn (Default)</span></span>
```
Start-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a71d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a71d-106">ResourceId</span></span>
```
Start-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a71d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a71d-107">DESCRIPTION</span></span>
<span data-ttu-id="9a71d-108">Постепенный экземпляр роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="9a71d-108">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="9a71d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9a71d-109">EXAMPLES</span></span>

### <span data-ttu-id="9a71d-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9a71d-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="9a71d-111">Постепенный экземпляр роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="9a71d-111">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="9a71d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9a71d-112">PARAMETERS</span></span>

### <span data-ttu-id="9a71d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a71d-113">-AsJob</span></span>
<span data-ttu-id="9a71d-114">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="9a71d-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="9a71d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9a71d-115">-Force</span></span>
<span data-ttu-id="9a71d-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="9a71d-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="9a71d-117">-Location</span><span class="sxs-lookup"><span data-stu-id="9a71d-117">-Location</span></span>
<span data-ttu-id="9a71d-118">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="9a71d-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a71d-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9a71d-119">-Name</span></span>
<span data-ttu-id="9a71d-120">Имя экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="9a71d-120">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a71d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a71d-121">-ResourceGroupName</span></span>
<span data-ttu-id="9a71d-122">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9a71d-122">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a71d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a71d-123">-ResourceId</span></span>
<span data-ttu-id="9a71d-124">Идентификатор ресурса для экземпляра роли инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="9a71d-124">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="9a71d-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a71d-125">-Confirm</span></span>
<span data-ttu-id="9a71d-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9a71d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a71d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a71d-127">-WhatIf</span></span>
<span data-ttu-id="9a71d-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9a71d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a71d-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9a71d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a71d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a71d-130">CommonParameters</span></span>
<span data-ttu-id="9a71d-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9a71d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a71d-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a71d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a71d-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9a71d-133">INPUTS</span></span>

## <span data-ttu-id="9a71d-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a71d-134">OUTPUTS</span></span>

## <span data-ttu-id="9a71d-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="9a71d-135">NOTES</span></span>

## <span data-ttu-id="9a71d-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a71d-136">RELATED LINKS</span></span>
