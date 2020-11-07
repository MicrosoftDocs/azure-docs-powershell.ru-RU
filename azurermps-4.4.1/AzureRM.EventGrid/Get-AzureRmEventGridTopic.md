---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
ms.openlocfilehash: 8ea4fc7674af247ffded2c6c4317f07a831adf2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567638"
---
# <span data-ttu-id="5aa67-101">Get-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="5aa67-101">Get-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="5aa67-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5aa67-102">SYNOPSIS</span></span>
<span data-ttu-id="5aa67-103">Получает сведения о сетке событий или получает список всех разделов сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="5aa67-103">Gets the details of an Event Grid topic, or gets a list of all Event Grid topics in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5aa67-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5aa67-104">SYNTAX</span></span>

### <span data-ttu-id="5aa67-105">ResourceGroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5aa67-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5aa67-106">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5aa67-106">TopicNameParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5aa67-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="5aa67-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5aa67-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5aa67-108">DESCRIPTION</span></span>
<span data-ttu-id="5aa67-109">Командлет Get-AzureRmEventGridTopic получает либо сведения о заданной теме сетки событий, либо список всех разделов сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="5aa67-109">The Get-AzureRmEventGridTopic cmdlet gets either the details of a specified Event Grid Topic, or a list of all Event Grid topics in the current Azure subscription.</span></span>
<span data-ttu-id="5aa67-110">Если указано название раздела, возвращается информация об одной статье.</span><span class="sxs-lookup"><span data-stu-id="5aa67-110">If the topic name is provided, the details of a single Event Grid Topic is returned.</span></span>
<span data-ttu-id="5aa67-111">Если название темы не указано, возвращается список тем.</span><span class="sxs-lookup"><span data-stu-id="5aa67-111">If the topic name is not provided, a list of topics is returned.</span></span>

## <span data-ttu-id="5aa67-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5aa67-112">EXAMPLES</span></span>

### <span data-ttu-id="5aa67-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5aa67-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="5aa67-114">Получает сведения о сетке событий \` в разделе элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="5aa67-114">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5aa67-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5aa67-115">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

<span data-ttu-id="5aa67-116">Получает сведения о сетке событий \` в разделе элемент1 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="5aa67-116">Gets the details of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5aa67-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5aa67-117">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName
```

<span data-ttu-id="5aa67-118">Перечислите все разделы сетки событий в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="5aa67-118">List all the Event Grid topics in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5aa67-119">Пример 4</span><span class="sxs-lookup"><span data-stu-id="5aa67-119">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridTopic
```

<span data-ttu-id="5aa67-120">Список всех подразделов сетки событий в подписке.</span><span class="sxs-lookup"><span data-stu-id="5aa67-120">List all the Event Grid topics in the subscription.</span></span>

## <span data-ttu-id="5aa67-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5aa67-121">PARAMETERS</span></span>

### <span data-ttu-id="5aa67-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5aa67-122">-Name</span></span>
<span data-ttu-id="5aa67-123">Название раздела EventGrid.</span><span class="sxs-lookup"><span data-stu-id="5aa67-123">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5aa67-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5aa67-124">-ResourceGroupName</span></span>
<span data-ttu-id="5aa67-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5aa67-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5aa67-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5aa67-126">-ResourceId</span></span>
<span data-ttu-id="5aa67-127">Идентификатор ресурса, представляющий раздел сетки событий.</span><span class="sxs-lookup"><span data-stu-id="5aa67-127">Resource Identifier representing the Event Grid Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5aa67-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aa67-128">-DefaultProfile</span></span>
<span data-ttu-id="5aa67-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5aa67-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5aa67-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aa67-130">CommonParameters</span></span>
<span data-ttu-id="5aa67-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5aa67-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aa67-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5aa67-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aa67-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5aa67-133">INPUTS</span></span>

### <span data-ttu-id="5aa67-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5aa67-134">System.String</span></span>
<span data-ttu-id="5aa67-135">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="5aa67-135">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="5aa67-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5aa67-136">OUTPUTS</span></span>

### <span data-ttu-id="5aa67-137">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="5aa67-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="5aa67-138">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventGrid. Models. PSTopicListInstance, Microsoft. Azure. Commands = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="5aa67-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5aa67-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="5aa67-139">NOTES</span></span>

## <span data-ttu-id="5aa67-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5aa67-140">RELATED LINKS</span></span>
