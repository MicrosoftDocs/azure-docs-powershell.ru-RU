---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: 49d465b1d993542790c20833ff5b1f75e03d5f26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569876"
---
# <span data-ttu-id="adaf6-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="adaf6-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="adaf6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="adaf6-102">SYNOPSIS</span></span>
<span data-ttu-id="adaf6-103">Добавляет источник данных на компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="adaf6-103">Adds a data source to Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adaf6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="adaf6-104">SYNTAX</span></span>

### <span data-ttu-id="adaf6-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="adaf6-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adaf6-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="adaf6-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning]
 [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adaf6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="adaf6-107">DESCRIPTION</span></span>
<span data-ttu-id="adaf6-108">Командлет **New-AzureRmOperationalInsightsLinuxSyslogDataSource** добавляет источник данных syslog на подключенные компьютеры Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="adaf6-108">The **New-AzureRmOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="adaf6-109">Azure Operational Insights может собирать данные syslog.</span><span class="sxs-lookup"><span data-stu-id="adaf6-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="adaf6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="adaf6-110">EXAMPLES</span></span>

## <span data-ttu-id="adaf6-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="adaf6-111">PARAMETERS</span></span>

### <span data-ttu-id="adaf6-112">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="adaf6-112">-CollectAlert</span></span>
<span data-ttu-id="adaf6-113">Указывает, что оперативная аналитика собирает сообщения оповещений.</span><span class="sxs-lookup"><span data-stu-id="adaf6-113">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="adaf6-114">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="adaf6-114">-CollectCritical</span></span>
<span data-ttu-id="adaf6-115">Указывает, что оперативная аналитика собирает важные сообщения.</span><span class="sxs-lookup"><span data-stu-id="adaf6-115">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="adaf6-116">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="adaf6-116">-CollectDebug</span></span>
<span data-ttu-id="adaf6-117">Указывает, что оперативная аналитика собирает сообщения об отладке.</span><span class="sxs-lookup"><span data-stu-id="adaf6-117">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="adaf6-118">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="adaf6-118">-CollectEmergency</span></span>
<span data-ttu-id="adaf6-119">Указывает на то, что оперативная аналитика собирает сообщения для экстренного реагирования.</span><span class="sxs-lookup"><span data-stu-id="adaf6-119">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="adaf6-120">-CollectError</span><span class="sxs-lookup"><span data-stu-id="adaf6-120">-CollectError</span></span>
<span data-ttu-id="adaf6-121">Указывает на то, что оперативная аналитика собирает сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="adaf6-121">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="adaf6-122">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="adaf6-122">-CollectInformational</span></span>
<span data-ttu-id="adaf6-123">Указывает, что при работе с аналитической аналитикой собираются информационные сообщения.</span><span class="sxs-lookup"><span data-stu-id="adaf6-123">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="adaf6-124">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="adaf6-124">-CollectNotice</span></span>
<span data-ttu-id="adaf6-125">Указывает, что оперативная аналитика собирает сообщения с уведомлениями.</span><span class="sxs-lookup"><span data-stu-id="adaf6-125">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="adaf6-126">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="adaf6-126">-CollectWarning</span></span>
<span data-ttu-id="adaf6-127">Указывает на то, что в syslog есть предупреждающие сообщения.</span><span class="sxs-lookup"><span data-stu-id="adaf6-127">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="adaf6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adaf6-128">-DefaultProfile</span></span>
<span data-ttu-id="adaf6-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="adaf6-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="adaf6-130">-Ссуда</span><span class="sxs-lookup"><span data-stu-id="adaf6-130">-Facility</span></span>
<span data-ttu-id="adaf6-131">Указывает код оборудования.</span><span class="sxs-lookup"><span data-stu-id="adaf6-131">Specifies a facility code.</span></span>

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

### <span data-ttu-id="adaf6-132">-Force</span><span class="sxs-lookup"><span data-stu-id="adaf6-132">-Force</span></span>
<span data-ttu-id="adaf6-133">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="adaf6-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="adaf6-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="adaf6-134">-Name</span></span>
<span data-ttu-id="adaf6-135">Задает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="adaf6-135">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="adaf6-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adaf6-136">-ResourceGroupName</span></span>
<span data-ttu-id="adaf6-137">Указывает имя группы ресурсов, которая содержит компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="adaf6-137">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="adaf6-138">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="adaf6-138">-Workspace</span></span>
<span data-ttu-id="adaf6-139">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="adaf6-139">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="adaf6-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="adaf6-140">-WorkspaceName</span></span>
<span data-ttu-id="adaf6-141">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="adaf6-141">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="adaf6-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="adaf6-142">-Confirm</span></span>
<span data-ttu-id="adaf6-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="adaf6-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adaf6-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adaf6-144">-WhatIf</span></span>
<span data-ttu-id="adaf6-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="adaf6-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adaf6-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="adaf6-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adaf6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adaf6-147">CommonParameters</span></span>
<span data-ttu-id="adaf6-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="adaf6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adaf6-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adaf6-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adaf6-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="adaf6-150">INPUTS</span></span>

### <span data-ttu-id="adaf6-151">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="adaf6-151">PSWorkspace</span></span>
<span data-ttu-id="adaf6-152">Параметр "Рабочая область" принимает значение типа "PSWorkspace" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="adaf6-152">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="adaf6-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="adaf6-153">OUTPUTS</span></span>

### <span data-ttu-id="adaf6-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="adaf6-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="adaf6-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="adaf6-155">NOTES</span></span>

## <span data-ttu-id="adaf6-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="adaf6-156">RELATED LINKS</span></span>

[<span data-ttu-id="adaf6-157">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="adaf6-157">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="adaf6-158">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="adaf6-158">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md)

