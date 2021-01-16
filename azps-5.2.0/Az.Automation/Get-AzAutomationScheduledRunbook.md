---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 8080361b0dabd7d4114580777e6508fa4503fbbc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418628"
---
# <span data-ttu-id="9ec0d-101">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="9ec0d-101">Get-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="9ec0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ec0d-102">SYNOPSIS</span></span>
<span data-ttu-id="9ec0d-103">Получает книги автоматизации и связанные расписания.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-103">Gets Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="9ec0d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9ec0d-104">SYNTAX</span></span>

### <span data-ttu-id="9ec0d-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9ec0d-105">ByAll (Default)</span></span>
```
Get-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ec0d-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="9ec0d-106">ByJobScheduleId</span></span>
```
Get-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ec0d-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="9ec0d-107">ByRunbookName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ec0d-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="9ec0d-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ec0d-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="9ec0d-109">ByScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ec0d-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ec0d-110">DESCRIPTION</span></span>
<span data-ttu-id="9ec0d-111">С **его использованием** можно получить одну или несколько книг автоматизации Azure и связанных расписания.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-111">The **Get-AzAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="9ec0d-112">По умолчанию этот cmdlet получает все запланированные книги.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="9ec0d-113">Укажите имя книги или расписание, чтобы увидеть ее расписание.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="9ec0d-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9ec0d-114">EXAMPLES</span></span>

### <span data-ttu-id="9ec0d-115">Пример 1. Получить все запланированные книги</span><span class="sxs-lookup"><span data-stu-id="9ec0d-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9ec0d-116">Эта команда получает все запланированные книги в учетной записи автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="9ec0d-117">Пример 2. Получить все расписания, связанные с книгой</span><span class="sxs-lookup"><span data-stu-id="9ec0d-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="9ec0d-118">Эта команда получает все запланированные книги runbk01 в учетной записи автоматизации Azure Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="9ec0d-119">Пример 3. Все книги, связанные с расписанием</span><span class="sxs-lookup"><span data-stu-id="9ec0d-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="9ec0d-120">Эта команда получает все запланированные книги для расписания Schedule01 в учетной записи автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="9ec0d-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ec0d-121">PARAMETERS</span></span>

### <span data-ttu-id="9ec0d-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9ec0d-122">-AutomationAccountName</span></span>
<span data-ttu-id="9ec0d-123">Указывает учетную запись автоматизации для книги, с которой работает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9ec0d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ec0d-124">-DefaultProfile</span></span>
<span data-ttu-id="9ec0d-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9ec0d-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ec0d-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="9ec0d-126">-JobScheduleId</span></span>
<span data-ttu-id="9ec0d-127">Определяет код запланированного задания, которое получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-127">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ec0d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ec0d-128">-ResourceGroupName</span></span>
<span data-ttu-id="9ec0d-129">Имя группы ресурсов для запланированных запусков, которые получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-129">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9ec0d-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="9ec0d-130">-RunbookName</span></span>
<span data-ttu-id="9ec0d-131">Определяет имя книги, для которой этот cmdlet получает запланированные runbooks.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-131">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ec0d-132">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="9ec0d-132">-ScheduleName</span></span>
<span data-ttu-id="9ec0d-133">Определяет имя расписания, для которого этот cmdlet получает запланированные книги.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-133">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ec0d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ec0d-134">CommonParameters</span></span>
<span data-ttu-id="9ec0d-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ec0d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ec0d-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ec0d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ec0d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9ec0d-137">INPUTS</span></span>

### <span data-ttu-id="9ec0d-138">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9ec0d-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9ec0d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9ec0d-139">System.String</span></span>

## <span data-ttu-id="9ec0d-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9ec0d-140">OUTPUTS</span></span>

### <span data-ttu-id="9ec0d-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span><span class="sxs-lookup"><span data-stu-id="9ec0d-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="9ec0d-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9ec0d-142">NOTES</span></span>

## <span data-ttu-id="9ec0d-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ec0d-143">RELATED LINKS</span></span>

[<span data-ttu-id="9ec0d-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="9ec0d-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="9ec0d-145">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="9ec0d-145">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)

