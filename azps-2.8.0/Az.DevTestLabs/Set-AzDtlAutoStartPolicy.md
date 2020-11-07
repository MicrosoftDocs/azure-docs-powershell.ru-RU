---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 3FADEC2E-4A2B-46EB-8A94-CF48D717C7FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoStartPolicy.md
ms.openlocfilehash: c751335f05f0e6ac9df5acb585dc5eb651d957a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721074"
---
# <span data-ttu-id="d829f-101">Set-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="d829f-101">Set-AzDtlAutoStartPolicy</span></span>

## <span data-ttu-id="d829f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d829f-102">SYNOPSIS</span></span>
<span data-ttu-id="d829f-103">Задает политику автоматического запуска лаборатории в DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="d829f-103">Sets the auto start policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="d829f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d829f-104">SYNTAX</span></span>

### <span data-ttu-id="d829f-105">Включить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d829f-105">Enable (Default)</span></span>
```
Set-AzDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d829f-106">Ключив</span><span class="sxs-lookup"><span data-stu-id="d829f-106">Disable</span></span>
```
Set-AzDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d829f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d829f-107">DESCRIPTION</span></span>
<span data-ttu-id="d829f-108">Командлет **Set-AzDtlAutoStartPolicy** задает политику автоматического запуска лаборатории, позволяющую планировать автоматическое начало для виртуальных машин лаборатории.</span><span class="sxs-lookup"><span data-stu-id="d829f-108">The **Set-AzDtlAutoStartPolicy** cmdlet sets the auto start policy of a lab, which allows lab virtual machines to be scheduled for automatic start.</span></span>
<span data-ttu-id="d829f-109">Для настройки политики командлет использует указанную группу ресурсов и имя лаборатории.</span><span class="sxs-lookup"><span data-stu-id="d829f-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="d829f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d829f-110">EXAMPLES</span></span>

## <span data-ttu-id="d829f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d829f-111">PARAMETERS</span></span>

### <span data-ttu-id="d829f-112">-Days</span><span class="sxs-lookup"><span data-stu-id="d829f-112">-Days</span></span>
<span data-ttu-id="d829f-113">Указывает в виде массива дни недели, когда должны быть запущены виртуальные машины лаборатории.</span><span class="sxs-lookup"><span data-stu-id="d829f-113">Specifies, as an array, the days of the week for when the virtual machines of the lab must be started.</span></span>

```yaml
Type: System.DayOfWeek[]
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d829f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d829f-114">-DefaultProfile</span></span>
<span data-ttu-id="d829f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d829f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d829f-116">-Отключение</span><span class="sxs-lookup"><span data-stu-id="d829f-116">-Disable</span></span>
<span data-ttu-id="d829f-117">Указывает, что этот командлет отключает политику для виртуальных машин в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="d829f-117">Indicates that this cmdlet disables the policy for the virtual machines in the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d829f-118">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="d829f-118">-Enable</span></span>
<span data-ttu-id="d829f-119">Указывает на то, что этот командлет включает политику для виртуальных машин в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="d829f-119">Indicates that this cmdlet enables the policy for the virtual machines in the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d829f-120">-LabName</span><span class="sxs-lookup"><span data-stu-id="d829f-120">-LabName</span></span>
<span data-ttu-id="d829f-121">Указывает имя лаборатории, для которой этот командлет задает политику автоматического запуска.</span><span class="sxs-lookup"><span data-stu-id="d829f-121">Specifies the name of the lab for which this cmdlet sets the automatic start policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d829f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d829f-122">-ResourceGroupName</span></span>
<span data-ttu-id="d829f-123">Указывает имя группы ресурсов, которой принадлежит лаборатория.</span><span class="sxs-lookup"><span data-stu-id="d829f-123">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d829f-124">-Time (время)</span><span class="sxs-lookup"><span data-stu-id="d829f-124">-Time</span></span>
<span data-ttu-id="d829f-125">Указывает время, когда должны быть запущены виртуальные машины лаборатории.</span><span class="sxs-lookup"><span data-stu-id="d829f-125">Specifies the time when the virtual machines of the lab must be started.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d829f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d829f-126">-Confirm</span></span>
<span data-ttu-id="d829f-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d829f-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d829f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d829f-128">-WhatIf</span></span>
<span data-ttu-id="d829f-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d829f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d829f-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d829f-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d829f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d829f-131">CommonParameters</span></span>
<span data-ttu-id="d829f-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d829f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d829f-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d829f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d829f-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d829f-134">INPUTS</span></span>

### <span data-ttu-id="d829f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d829f-135">System.String</span></span>

## <span data-ttu-id="d829f-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d829f-136">OUTPUTS</span></span>

### <span data-ttu-id="d829f-137">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="d829f-137">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="d829f-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="d829f-138">NOTES</span></span>

## <span data-ttu-id="d829f-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d829f-139">RELATED LINKS</span></span>

[<span data-ttu-id="d829f-140">Get-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="d829f-140">Get-AzDtlAutoStartPolicy</span></span>](./Get-AzDtlAutoStartPolicy.md)

