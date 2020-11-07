---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c7ec31ce2af23a4376f8b5f94deca302345e81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556120"
---
# <span data-ttu-id="5fda3-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="5fda3-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="5fda3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5fda3-102">SYNOPSIS</span></span>
<span data-ttu-id="5fda3-103">Начните сбор мусора для удаленных объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="5fda3-103">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="5fda3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5fda3-104">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [[-ResourceGroupName] <String>] [-FarmName] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fda3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fda3-105">DESCRIPTION</span></span>
<span data-ttu-id="5fda3-106">Начните сбор мусора для удаленных объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="5fda3-106">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="5fda3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5fda3-107">EXAMPLES</span></span>

### <span data-ttu-id="5fda3-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5fda3-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsReclaimStorageCapacity -FarmName "44263c10-13b2-4912-9b17-85c1e43b2a30"
```

<span data-ttu-id="5fda3-109">Начните сбор мусора.</span><span class="sxs-lookup"><span data-stu-id="5fda3-109">Start garbage collection.</span></span>

## <span data-ttu-id="5fda3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5fda3-110">PARAMETERS</span></span>

### <span data-ttu-id="5fda3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5fda3-111">-AsJob</span></span>
<span data-ttu-id="5fda3-112">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="5fda3-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="5fda3-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="5fda3-113">-FarmName</span></span>
<span data-ttu-id="5fda3-114">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="5fda3-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fda3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5fda3-115">-Force</span></span>
<span data-ttu-id="5fda3-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="5fda3-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5fda3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fda3-117">-ResourceGroupName</span></span>
<span data-ttu-id="5fda3-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5fda3-118">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fda3-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5fda3-119">-Confirm</span></span>
<span data-ttu-id="5fda3-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5fda3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fda3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fda3-121">-WhatIf</span></span>
<span data-ttu-id="5fda3-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5fda3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fda3-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5fda3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fda3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fda3-124">CommonParameters</span></span>
<span data-ttu-id="5fda3-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5fda3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fda3-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fda3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fda3-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5fda3-127">INPUTS</span></span>

## <span data-ttu-id="5fda3-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fda3-128">OUTPUTS</span></span>

## <span data-ttu-id="5fda3-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="5fda3-129">NOTES</span></span>

## <span data-ttu-id="5fda3-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5fda3-130">RELATED LINKS</span></span>
