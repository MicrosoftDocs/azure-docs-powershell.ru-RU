---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: 459c217904ba44662d18c81c4c493a3b7f2033e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565003"
---
# <span data-ttu-id="4e8ed-101">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="4e8ed-101">Get-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="4e8ed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e8ed-102">SYNOPSIS</span></span>
<span data-ttu-id="4e8ed-103">Возвращает Runbook Automation и связанные расписания.</span><span class="sxs-lookup"><span data-stu-id="4e8ed-103">Gets Automation runbooks and associated schedules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e8ed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e8ed-104">SYNTAX</span></span>

### <span data-ttu-id="4e8ed-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e8ed-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e8ed-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="4e8ed-106">ByJobScheduleId</span></span>
```
Get-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e8ed-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="4e8ed-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e8ed-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="4e8ed-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e8ed-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="4e8ed-109">ByScheduleName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e8ed-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e8ed-110">DESCRIPTION</span></span>
<span data-ttu-id="4e8ed-111">Командлет **Get-AzureRmAutomationScheduledRunbook** получает один или несколько Runbook автоматизации Azure и связанных с ними расписаний.</span><span class="sxs-lookup"><span data-stu-id="4e8ed-111">The **Get-AzureRmAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="4e8ed-112">По умолчанию этот командлет получает все запланированные Runbook.</span><span class="sxs-lookup"><span data-stu-id="4e8ed-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="4e8ed-113">Укажите имя Runbook или расписание или оба варианта для просмотра конкретных расписаний Runbook.</span><span class="sxs-lookup"><span data-stu-id="4e8ed-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="4e8ed-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e8ed-114">EXAMPLES</span></span>

### <span data-ttu-id="4e8ed-115">Пример 1: получение всех запланированных Runbook</span><span class="sxs-lookup"><span data-stu-id="4e8ed-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4e8ed-116">Эта команда получает все запланированные Runbook в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4e8ed-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="4e8ed-117">Пример 2: получение всех расписаний, связанных с модулем Runbook</span><span class="sxs-lookup"><span data-stu-id="4e8ed-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="4e8ed-118">Эта команда получает все запланированные Runbook для модуля Runbook Runbk01 в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4e8ed-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="4e8ed-119">Пример 3: получение всех модулей Runbook, связанных с расписанием</span><span class="sxs-lookup"><span data-stu-id="4e8ed-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="4e8ed-120">Эта команда получает все запланированные Runbook для Schedule01 расписания в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4e8ed-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="4e8ed-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e8ed-121">PARAMETERS</span></span>

### <span data-ttu-id="4e8ed-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4e8ed-122">-AutomationAccountName</span></span>
<span data-ttu-id="4e8ed-123">Указывает учетную запись автоматизации для модуля Runbook, на котором работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4e8ed-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="4e8ed-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e8ed-124">-DefaultProfile</span></span>
<span data-ttu-id="4e8ed-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4e8ed-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e8ed-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="4e8ed-126">-JobScheduleId</span></span>
<span data-ttu-id="4e8ed-127">Указывает идентификатор запланированного задания, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4e8ed-127">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e8ed-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e8ed-128">-ResourceGroupName</span></span>
<span data-ttu-id="4e8ed-129">Указывает имя группы ресурсов для запланированных Runbook, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4e8ed-129">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4e8ed-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="4e8ed-130">-RunbookName</span></span>
<span data-ttu-id="4e8ed-131">Указывает имя Runbook, для которого этот командлет получает запланированные Runbook.</span><span class="sxs-lookup"><span data-stu-id="4e8ed-131">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e8ed-132">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="4e8ed-132">-ScheduleName</span></span>
<span data-ttu-id="4e8ed-133">Указывает имя расписания, для которого этот командлет получает запланированные Runbook.</span><span class="sxs-lookup"><span data-stu-id="4e8ed-133">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e8ed-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e8ed-134">CommonParameters</span></span>
<span data-ttu-id="4e8ed-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e8ed-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e8ed-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e8ed-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e8ed-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e8ed-137">INPUTS</span></span>

### <span data-ttu-id="4e8ed-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="4e8ed-138">None</span></span>
<span data-ttu-id="4e8ed-139">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="4e8ed-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4e8ed-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e8ed-140">OUTPUTS</span></span>

### <span data-ttu-id="4e8ed-141">Microsoft. Azure. Commands. Automation. Model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="4e8ed-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="4e8ed-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e8ed-142">NOTES</span></span>

## <span data-ttu-id="4e8ed-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e8ed-143">RELATED LINKS</span></span>

[<span data-ttu-id="4e8ed-144">Регистрация — AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="4e8ed-144">Register-AzureRmAutomationScheduledRunbook</span></span>](./Register-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="4e8ed-145">Отмена регистрации — AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="4e8ed-145">Unregister-AzureRmAutomationScheduledRunbook</span></span>](./Unregister-AzureRMAutomationScheduledRunbook.md)

