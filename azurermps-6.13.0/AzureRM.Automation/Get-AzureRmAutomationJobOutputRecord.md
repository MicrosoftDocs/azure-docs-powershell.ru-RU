---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationJobOutputRecord.md
ms.openlocfilehash: 63227ad14eb16c5a43e37095f7cfa80ccd8b9cce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556876"
---
# <span data-ttu-id="af465-101">Get-AzureRmAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="af465-101">Get-AzureRmAutomationJobOutputRecord</span></span>

## <span data-ttu-id="af465-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af465-102">SYNOPSIS</span></span>
<span data-ttu-id="af465-103">Получает полный вывод записи выходных данных задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="af465-103">Gets the full output of an Automation job output record.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af465-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af465-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af465-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af465-105">DESCRIPTION</span></span>
<span data-ttu-id="af465-106">Командлет **Get-AzureRmAutomationJobOutputRecord** получает полный вывод записи выходных данных задания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="af465-106">The **Get-AzureRmAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="af465-107">Несмотря на то, что командлет **Get-AzureRmAutomationJobOutput** содержит одну или несколько выходных записей задания, она возвращает только сводку из строки значения любой выходной записи.</span><span class="sxs-lookup"><span data-stu-id="af465-107">Although the **Get-AzureRmAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="af465-108">Оно не возвращает полную величину введенного значения из выходной записи в исходном типе.</span><span class="sxs-lookup"><span data-stu-id="af465-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="af465-109">Кроме того, сводка имеет максимальную длину, которая может превысить полное значение, которое выводит этот командлет.</span><span class="sxs-lookup"><span data-stu-id="af465-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>
<span data-ttu-id="af465-110">В отличие от **Get-AzureRmAutomationJobOutput** , этот командлет возвращает полное значение из первоначально выданного типа для значения, выводимого из записи.</span><span class="sxs-lookup"><span data-stu-id="af465-110">Unlike **Get-AzureRmAutomationJobOutput** , this cmdlet returns the full value in its originally outputted type, for any output record's outputted value.</span></span>

## <span data-ttu-id="af465-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af465-111">EXAMPLES</span></span>

### <span data-ttu-id="af465-112">Пример 1: получение полного результата задания автоматизации</span><span class="sxs-lookup"><span data-stu-id="af465-112">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzureRmAutomationJobOutputRecord
```

<span data-ttu-id="af465-113">Эта команда получает полный вывод задания с указанным ИДЕНТИФИКАТОРом задания.</span><span class="sxs-lookup"><span data-stu-id="af465-113">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="af465-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af465-114">PARAMETERS</span></span>

### <span data-ttu-id="af465-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="af465-115">-AutomationAccountName</span></span>
<span data-ttu-id="af465-116">Указывает имя учетной записи автоматизации, для которой этот командлет получает выходную запись о задании.</span><span class="sxs-lookup"><span data-stu-id="af465-116">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="af465-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af465-117">-DefaultProfile</span></span>
<span data-ttu-id="af465-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="af465-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af465-119">-ID</span><span class="sxs-lookup"><span data-stu-id="af465-119">-Id</span></span>
<span data-ttu-id="af465-120">Указывает идентификатор записи выходных данных задания для этого командлета, который требуется извлечь.</span><span class="sxs-lookup"><span data-stu-id="af465-120">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StreamRecordId

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af465-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="af465-121">-JobId</span></span>
<span data-ttu-id="af465-122">Указывает идентификатор задания, для которого этот командлет получает выходную запись.</span><span class="sxs-lookup"><span data-stu-id="af465-122">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af465-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af465-123">-ResourceGroupName</span></span>
<span data-ttu-id="af465-124">Указывает имя группы ресурсов, для которой этот командлет получает выходную запись задания.</span><span class="sxs-lookup"><span data-stu-id="af465-124">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="af465-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af465-125">CommonParameters</span></span>
<span data-ttu-id="af465-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af465-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af465-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af465-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af465-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af465-128">INPUTS</span></span>

### <span data-ttu-id="af465-129">System. GUID</span><span class="sxs-lookup"><span data-stu-id="af465-129">System.Guid</span></span>

### <span data-ttu-id="af465-130">System. String</span><span class="sxs-lookup"><span data-stu-id="af465-130">System.String</span></span>

## <span data-ttu-id="af465-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af465-131">OUTPUTS</span></span>

### <span data-ttu-id="af465-132">Microsoft. Azure. Commands. Automation. Model. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="af465-132">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="af465-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="af465-133">NOTES</span></span>

## <span data-ttu-id="af465-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af465-134">RELATED LINKS</span></span>

[<span data-ttu-id="af465-135">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="af465-135">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

