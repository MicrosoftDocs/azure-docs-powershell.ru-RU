---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightswindowsperformancecounterdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: b827c9d133ff6fc0bb9df0e1e3e25c3eea23916f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560220"
---
# <span data-ttu-id="89343-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="89343-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="89343-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89343-102">SYNOPSIS</span></span>
<span data-ttu-id="89343-103">Добавляет источник данных счетчика производительности Windows для подключенных компьютеров, работающих под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="89343-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89343-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89343-104">SYNTAX</span></span>

### <span data-ttu-id="89343-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="89343-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89343-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="89343-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89343-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89343-107">DESCRIPTION</span></span>
<span data-ttu-id="89343-108">Командлет **New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** добавляет источник данных счетчика производительности Windows для подключенных компьютеров, работающих под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="89343-108">The **New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="89343-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89343-109">EXAMPLES</span></span>

## <span data-ttu-id="89343-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89343-110">PARAMETERS</span></span>

### <span data-ttu-id="89343-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="89343-111">-CounterName</span></span>
<span data-ttu-id="89343-112">Указывает имя счетчика.</span><span class="sxs-lookup"><span data-stu-id="89343-112">Specifies the name of a counter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89343-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89343-113">-DefaultProfile</span></span>
<span data-ttu-id="89343-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="89343-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89343-115">-Force</span><span class="sxs-lookup"><span data-stu-id="89343-115">-Force</span></span>
<span data-ttu-id="89343-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="89343-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89343-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="89343-117">-InstanceName</span></span>
<span data-ttu-id="89343-118">Указывает имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="89343-118">Specifies an instance name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89343-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="89343-119">-IntervalSeconds</span></span>
<span data-ttu-id="89343-120">Указывает интервал сбора.</span><span class="sxs-lookup"><span data-stu-id="89343-120">Specifies the interval of collection.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89343-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="89343-121">-Name</span></span>
<span data-ttu-id="89343-122">Задает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="89343-122">Specifies a name for the data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89343-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="89343-123">-ObjectName</span></span>
<span data-ttu-id="89343-124">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="89343-124">Specifies the name of an object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89343-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89343-125">-ResourceGroupName</span></span>
<span data-ttu-id="89343-126">Указывает имя группы ресурсов, содержащей компьютеры.</span><span class="sxs-lookup"><span data-stu-id="89343-126">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89343-127">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="89343-127">-UseLegacyCollector</span></span>
<span data-ttu-id="89343-128">Использование устаревшего сборщика или сборщика по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="89343-128">Use legacy collector or the default collector.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89343-129">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="89343-129">-Workspace</span></span>
<span data-ttu-id="89343-130">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="89343-130">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89343-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="89343-131">-WorkspaceName</span></span>
<span data-ttu-id="89343-132">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="89343-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89343-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89343-133">-Confirm</span></span>
<span data-ttu-id="89343-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="89343-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89343-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89343-135">-WhatIf</span></span>
<span data-ttu-id="89343-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="89343-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89343-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="89343-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89343-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89343-138">CommonParameters</span></span>
<span data-ttu-id="89343-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89343-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89343-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89343-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89343-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89343-141">INPUTS</span></span>

### <span data-ttu-id="89343-142">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="89343-142">PSWorkspace</span></span>
<span data-ttu-id="89343-143">Параметр "Рабочая область" принимает значение типа "PSWorkspace" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="89343-143">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="89343-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89343-144">OUTPUTS</span></span>

### <span data-ttu-id="89343-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="89343-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="89343-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="89343-146">NOTES</span></span>

## <span data-ttu-id="89343-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89343-147">RELATED LINKS</span></span>
