---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 8AAD9309-5763-4903-AF6A-1E50310146C0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: edded91551b87e180b17ff8f97d84d16bef0b0ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568588"
---
# <span data-ttu-id="bb423-101">Set-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="bb423-101">Set-AzureRmDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="bb423-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb423-102">SYNOPSIS</span></span>
<span data-ttu-id="bb423-103">Задает политику автоматического выключения лабораторных семинаров DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="bb423-103">Sets the auto shutdown policy of a lab DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb423-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb423-104">SYNTAX</span></span>

### <span data-ttu-id="bb423-105">Включить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bb423-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb423-106">Ключив</span><span class="sxs-lookup"><span data-stu-id="bb423-106">Disable</span></span>
```
Set-AzureRmDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb423-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb423-107">DESCRIPTION</span></span>
<span data-ttu-id="bb423-108">Командлет **Set-AzureRmDtlAutoShutdownPolicy** задает политику автоматического отключения лаборатории, которая автоматически завершает работу всех виртуальных машин в лаборатории в заданное время суток.</span><span class="sxs-lookup"><span data-stu-id="bb423-108">The **Set-AzureRmDtlAutoShutdownPolicy** cmdlet sets the auto shutdown policy of a lab, which automatically shuts down all the virtual machines in the lab at a specified time of the day.</span></span>
<span data-ttu-id="bb423-109">Для настройки политики командлет использует указанную группу ресурсов и имя лаборатории.</span><span class="sxs-lookup"><span data-stu-id="bb423-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="bb423-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb423-110">EXAMPLES</span></span>

## <span data-ttu-id="bb423-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb423-111">PARAMETERS</span></span>

### <span data-ttu-id="bb423-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb423-112">-DefaultProfile</span></span>
<span data-ttu-id="bb423-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bb423-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb423-114">-Отключение</span><span class="sxs-lookup"><span data-stu-id="bb423-114">-Disable</span></span>
<span data-ttu-id="bb423-115">Указывает на то, что командлет отключает политику в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="bb423-115">Indicates that the cmdlet disables the policy in the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disable
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb423-116">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="bb423-116">-Enable</span></span>
<span data-ttu-id="bb423-117">Указывает на то, что командлет включает политику в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="bb423-117">Indicates that the cmdlet enables the policy in the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Enable
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb423-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="bb423-118">-LabName</span></span>
<span data-ttu-id="bb423-119">Указывает имя лаборатории, для которой этот командлет задает политику автоматического отключения.</span><span class="sxs-lookup"><span data-stu-id="bb423-119">Specifies the name of the lab for which this cmdlet sets the auto shutdown policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb423-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb423-120">-ResourceGroupName</span></span>
<span data-ttu-id="bb423-121">Указывает имя группы ресурсов, которой принадлежит лаборатория.</span><span class="sxs-lookup"><span data-stu-id="bb423-121">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb423-122">-Time (время)</span><span class="sxs-lookup"><span data-stu-id="bb423-122">-Time</span></span>
<span data-ttu-id="bb423-123">Задает время в виде объекта **DateTime** , по истечении которого виртуальные машины в лаборатории должны завершить работу.</span><span class="sxs-lookup"><span data-stu-id="bb423-123">Specifies the time, as a **DateTime** object, for when the virtual machines in the lab must shut down.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb423-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb423-124">-Confirm</span></span>
<span data-ttu-id="bb423-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bb423-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb423-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb423-126">-WhatIf</span></span>
<span data-ttu-id="bb423-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bb423-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb423-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bb423-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb423-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb423-129">CommonParameters</span></span>
<span data-ttu-id="bb423-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb423-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb423-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb423-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb423-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb423-132">INPUTS</span></span>

### <span data-ttu-id="bb423-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="bb423-133">None</span></span>
<span data-ttu-id="bb423-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="bb423-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bb423-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb423-135">OUTPUTS</span></span>

### <span data-ttu-id="bb423-136">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="bb423-136">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="bb423-137">Этот командлет возвращает расписание, которое определяет, когда должны быть закрыты виртуальные машины в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="bb423-137">This cmdlet returns the schedule which specifies when the virtual machines in the lab must shut down.</span></span>

## <span data-ttu-id="bb423-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb423-138">NOTES</span></span>

## <span data-ttu-id="bb423-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb423-139">RELATED LINKS</span></span>

[<span data-ttu-id="bb423-140">Get-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="bb423-140">Get-AzureRmDtlAutoShutdownPolicy</span></span>](./Get-AzureRmDtlAutoShutdownPolicy.md)

