---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Enable-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Enable-AzureRmActivityLogAlert.md
ms.openlocfilehash: 92607537fb80132627e1f26f240a10b8f7150fb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569408"
---
# <span data-ttu-id="dcaf1-101">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="dcaf1-101">Enable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="dcaf1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dcaf1-102">SYNOPSIS</span></span>
<span data-ttu-id="dcaf1-103">Включает предупреждение журнала активности и задает его Теги.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-103">Enables an activity log alert and sets its Tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcaf1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dcaf1-104">SYNTAX</span></span>

### <span data-ttu-id="dcaf1-105">Параметры по умолчанию для включения оповещения журнала активности</span><span class="sxs-lookup"><span data-stu-id="dcaf1-105">Default parameters for enable an activity log alert</span></span>
```
Enable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcaf1-106">Параметры для включения уведомлений журнала действий, принимающего значение из канала</span><span class="sxs-lookup"><span data-stu-id="dcaf1-106">Parameters to enable an activity log alerts taking value from the pipe</span></span>
```
Enable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcaf1-107">Параметры для включения уведомлений журнала активности, принимающего значение ResourceId из канала</span><span class="sxs-lookup"><span data-stu-id="dcaf1-107">Parameters to enable an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Enable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcaf1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcaf1-108">DESCRIPTION</span></span>
<span data-ttu-id="dcaf1-109">Командлет **Enable-AzureRmActivityLogAlert** позволяет включить оповещение журнала активности и задать его Теги.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-109">The **Enable-AzureRmActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="dcaf1-110">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно обновить ресурс.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="dcaf1-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dcaf1-111">EXAMPLES</span></span>

### <span data-ttu-id="dcaf1-112">Пример 1: Отключение оповещения журнала активности</span><span class="sxs-lookup"><span data-stu-id="dcaf1-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Enable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="dcaf1-113">Эта команда включает предупреждение журнала активности с именем alert1 в группе ресурсов по умолчанию — ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="dcaf1-114">Пример 2: Включение оповещения журнала активности с помощью объекта PSActivityLogAlertResource в качестве входных данных</span><span class="sxs-lookup"><span data-stu-id="dcaf1-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="dcaf1-115">Эта команда включает предупреждение журнала активности с именем alert1.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="dcaf1-116">Для этого он использует объект PSActivityLogAlertResource в качестве аргумента ввода.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="dcaf1-117">Пример 3: включение ActivityLogAlert с помощью параметра ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcaf1-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Enable-AzureRmActivityLogAlert
```

<span data-ttu-id="dcaf1-118">Эта команда активирует ActivityLogAlert с помощью параметра ResourceId в канале.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="dcaf1-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dcaf1-119">PARAMETERS</span></span>

### <span data-ttu-id="dcaf1-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dcaf1-120">-Name</span></span>
<span data-ttu-id="dcaf1-121">Имя оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-121">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for enable an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcaf1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcaf1-122">-ResourceGroupName</span></span>
<span data-ttu-id="dcaf1-123">Имя группы ресурсов, в которой будет находиться ресурс оповещения.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-123">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for enable an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcaf1-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dcaf1-124">-InputObject</span></span>
<span data-ttu-id="dcaf1-125">Задает свойство Tags (Теги InputObject) для вызова, чтобы извлечь требуемое имя, имя группы ресурсов и необязательные свойства Tags.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-125">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to enable an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcaf1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcaf1-126">-ResourceId</span></span>
<span data-ttu-id="dcaf1-127">Задает свойство Tags (Теги) для вызова, чтобы извлечь требуемое имя, свойства имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-127">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to enable an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcaf1-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dcaf1-128">-Confirm</span></span>
<span data-ttu-id="dcaf1-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcaf1-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcaf1-130">-DefaultProfile</span></span>
<span data-ttu-id="dcaf1-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcaf1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcaf1-132">-WhatIf</span></span>
<span data-ttu-id="dcaf1-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dcaf1-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcaf1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcaf1-135">CommonParameters</span></span>
<span data-ttu-id="dcaf1-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dcaf1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcaf1-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcaf1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcaf1-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dcaf1-138">INPUTS</span></span>

## <span data-ttu-id="dcaf1-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcaf1-139">OUTPUTS</span></span>

### <span data-ttu-id="dcaf1-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="dcaf1-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="dcaf1-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="dcaf1-141">NOTES</span></span>

## <span data-ttu-id="dcaf1-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dcaf1-142">RELATED LINKS</span></span>

[<span data-ttu-id="dcaf1-143">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="dcaf1-143">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="dcaf1-144">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="dcaf1-144">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="dcaf1-145">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="dcaf1-145">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="dcaf1-146">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="dcaf1-146">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="dcaf1-147">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="dcaf1-147">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="dcaf1-148">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="dcaf1-148">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)