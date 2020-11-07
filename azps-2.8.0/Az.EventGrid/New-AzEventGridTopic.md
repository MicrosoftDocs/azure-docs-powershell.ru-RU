---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: 25882d3fe897c77df864d429cfc3cd9d31197916
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720991"
---
# <span data-ttu-id="a12ef-101">New-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="a12ef-101">New-AzEventGridTopic</span></span>

## <span data-ttu-id="a12ef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a12ef-102">SYNOPSIS</span></span>
<span data-ttu-id="a12ef-103">Создание нового раздела сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="a12ef-103">Creates a new Azure Event Grid Topic.</span></span>

## <span data-ttu-id="a12ef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a12ef-104">SYNTAX</span></span>

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a12ef-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a12ef-105">DESCRIPTION</span></span>
<span data-ttu-id="a12ef-106">Создание нового раздела сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="a12ef-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="a12ef-107">После создания темы приложение может публиковать события в конечной точке раздела.</span><span class="sxs-lookup"><span data-stu-id="a12ef-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="a12ef-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a12ef-108">EXAMPLES</span></span>

### <span data-ttu-id="a12ef-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a12ef-109">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="a12ef-110">Создание сетки событий в разделе \` элемент1 \` в указанном географическом расположении \` westus2 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a12ef-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a12ef-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a12ef-111">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="a12ef-112">Создает сетку событий \` в разделе элемент1 \` в указанном географическом расположении \` westus2 \` , в группе ресурсов \` MyResourceGroupName \` с заданными тегами "Отдел" и "среда".</span><span class="sxs-lookup"><span data-stu-id="a12ef-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="a12ef-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a12ef-113">PARAMETERS</span></span>

### <span data-ttu-id="a12ef-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a12ef-114">-DefaultProfile</span></span>
<span data-ttu-id="a12ef-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a12ef-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a12ef-116">-Location</span><span class="sxs-lookup"><span data-stu-id="a12ef-116">-Location</span></span>
<span data-ttu-id="a12ef-117">Расположение темы</span><span class="sxs-lookup"><span data-stu-id="a12ef-117">The location of the topic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a12ef-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a12ef-118">-Name</span></span>
<span data-ttu-id="a12ef-119">Название темы.</span><span class="sxs-lookup"><span data-stu-id="a12ef-119">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a12ef-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a12ef-120">-ResourceGroupName</span></span>
<span data-ttu-id="a12ef-121">Группа ресурсов, в которой должен быть создан раздел.</span><span class="sxs-lookup"><span data-stu-id="a12ef-121">The resource group in which the topic should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a12ef-122">-Тег</span><span class="sxs-lookup"><span data-stu-id="a12ef-122">-Tag</span></span>
<span data-ttu-id="a12ef-123">Хэш-таблицы, представляющие Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a12ef-123">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a12ef-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a12ef-124">-Confirm</span></span>
<span data-ttu-id="a12ef-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a12ef-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a12ef-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a12ef-126">-WhatIf</span></span>
<span data-ttu-id="a12ef-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a12ef-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a12ef-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a12ef-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a12ef-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a12ef-129">CommonParameters</span></span>
<span data-ttu-id="a12ef-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a12ef-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a12ef-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a12ef-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a12ef-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a12ef-132">INPUTS</span></span>

### <span data-ttu-id="a12ef-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a12ef-133">System.String</span></span>

### <span data-ttu-id="a12ef-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a12ef-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a12ef-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a12ef-135">OUTPUTS</span></span>

### <span data-ttu-id="a12ef-136">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="a12ef-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="a12ef-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="a12ef-137">NOTES</span></span>

## <span data-ttu-id="a12ef-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a12ef-138">RELATED LINKS</span></span>