---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/stop-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 9f1ec54ded16f68c3af2a9449f9c97afb40a520a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564595"
---
# <span data-ttu-id="566ec-101">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="566ec-101">Stop-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="566ec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="566ec-102">SYNOPSIS</span></span>
<span data-ttu-id="566ec-103">Остановка триггера в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="566ec-103">Stops a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="566ec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="566ec-104">SYNTAX</span></span>

### <span data-ttu-id="566ec-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="566ec-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="566ec-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="566ec-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="566ec-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="566ec-107">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="566ec-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="566ec-108">DESCRIPTION</span></span>
<span data-ttu-id="566ec-109">Командлет **Stop-AzureRmDataFactoryV2Trigger** останавливает триггер в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="566ec-109">The **Stop-AzureRmDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="566ec-110">Если триггер находится в состоянии "начато", этот командлет останавливает срабатывание триггера и больше не вызывает конвейеры.</span><span class="sxs-lookup"><span data-stu-id="566ec-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="566ec-111">Если триггер уже находится в состоянии "остановлено", этот командлет не действует.</span><span class="sxs-lookup"><span data-stu-id="566ec-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="566ec-112">Если указан параметр Force, командлет не выводит запрос перед остановкой триггера.</span><span class="sxs-lookup"><span data-stu-id="566ec-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="566ec-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="566ec-113">EXAMPLES</span></span>

### <span data-ttu-id="566ec-114">Пример 1: остановка триггера</span><span class="sxs-lookup"><span data-stu-id="566ec-114">Example 1: Stop a trigger</span></span>
```
Stop-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="566ec-115">Останавливает триггер с именем "ScheduledTrigger" в фабрике данных "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="566ec-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="566ec-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="566ec-116">PARAMETERS</span></span>

### <span data-ttu-id="566ec-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="566ec-117">-DataFactoryName</span></span>
<span data-ttu-id="566ec-118">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="566ec-118">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="566ec-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="566ec-119">-DefaultProfile</span></span>
<span data-ttu-id="566ec-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="566ec-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="566ec-121">-Force</span><span class="sxs-lookup"><span data-stu-id="566ec-121">-Force</span></span>
<span data-ttu-id="566ec-122">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="566ec-122">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="566ec-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="566ec-123">-InputObject</span></span>
<span data-ttu-id="566ec-124">Запускаемый объект.</span><span class="sxs-lookup"><span data-stu-id="566ec-124">Trigger object to start.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="566ec-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="566ec-125">-Name</span></span>
<span data-ttu-id="566ec-126">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="566ec-126">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="566ec-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="566ec-127">-ResourceGroupName</span></span>
<span data-ttu-id="566ec-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="566ec-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="566ec-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="566ec-129">-ResourceId</span></span>
<span data-ttu-id="566ec-130">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="566ec-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="566ec-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="566ec-131">-Confirm</span></span>
<span data-ttu-id="566ec-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="566ec-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="566ec-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="566ec-133">-WhatIf</span></span>
<span data-ttu-id="566ec-134">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="566ec-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="566ec-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="566ec-135">CommonParameters</span></span>
<span data-ttu-id="566ec-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="566ec-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="566ec-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="566ec-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="566ec-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="566ec-138">INPUTS</span></span>

### <span data-ttu-id="566ec-139">System. String</span><span class="sxs-lookup"><span data-stu-id="566ec-139">System.String</span></span>

### <span data-ttu-id="566ec-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="566ec-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>
<span data-ttu-id="566ec-141">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="566ec-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="566ec-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="566ec-142">OUTPUTS</span></span>

### <span data-ttu-id="566ec-143">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="566ec-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="566ec-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="566ec-144">NOTES</span></span>

## <span data-ttu-id="566ec-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="566ec-145">RELATED LINKS</span></span>

[<span data-ttu-id="566ec-146">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="566ec-146">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="566ec-147">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="566ec-147">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="566ec-148">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="566ec-148">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="566ec-149">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="566ec-149">Remove-AzureRmDataFactoryV2Trigger</span></span>]()