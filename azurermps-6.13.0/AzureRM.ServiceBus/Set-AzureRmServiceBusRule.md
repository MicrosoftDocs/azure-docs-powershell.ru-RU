---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
ms.openlocfilehash: cb6200156b68524119df86e24d812b97bcd250e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563995"
---
# <span data-ttu-id="ef64f-101">Set-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="ef64f-101">Set-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="ef64f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef64f-102">SYNOPSIS</span></span>
<span data-ttu-id="ef64f-103">Обновляет указанное описание правила для данной подписки.</span><span class="sxs-lookup"><span data-stu-id="ef64f-103">Updates the specified rule description for the given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef64f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef64f-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef64f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef64f-105">DESCRIPTION</span></span>
<span data-ttu-id="ef64f-106">Командлет **Set-AzureRmServiceBusRule** обновляет описание указанного правила данной подписки.</span><span class="sxs-lookup"><span data-stu-id="ef64f-106">The **Set-AzureRmServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="ef64f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef64f-107">EXAMPLES</span></span>

### <span data-ttu-id="ef64f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ef64f-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="ef64f-109">обновляет sqlexpression **mysqlexpression = "Condition"** правила `SBEule` подписки `SBSubscription` в разделе `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="ef64f-109">updates the sqlexpression **mysqlexpression='condition'** of the rule `SBEule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="ef64f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef64f-110">PARAMETERS</span></span>

### <span data-ttu-id="ef64f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef64f-111">-DefaultProfile</span></span>
<span data-ttu-id="ef64f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef64f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef64f-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef64f-113">-InputObject</span></span>
<span data-ttu-id="ef64f-114">Определение правил ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="ef64f-114">ServiceBus Rules definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef64f-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ef64f-115">-Name</span></span>
<span data-ttu-id="ef64f-116">Имя правила.</span><span class="sxs-lookup"><span data-stu-id="ef64f-116">Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef64f-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ef64f-117">-Namespace</span></span>
<span data-ttu-id="ef64f-118">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="ef64f-118">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef64f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef64f-119">-ResourceGroupName</span></span>
<span data-ttu-id="ef64f-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ef64f-120">The name of the resource group</span></span>

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

### <span data-ttu-id="ef64f-121">-Подписка</span><span class="sxs-lookup"><span data-stu-id="ef64f-121">-Subscription</span></span>
<span data-ttu-id="ef64f-122">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="ef64f-122">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef64f-123">-Темы</span><span class="sxs-lookup"><span data-stu-id="ef64f-123">-Topic</span></span>
<span data-ttu-id="ef64f-124">Название раздела.</span><span class="sxs-lookup"><span data-stu-id="ef64f-124">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef64f-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef64f-125">-Confirm</span></span>
<span data-ttu-id="ef64f-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ef64f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef64f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef64f-127">-WhatIf</span></span>
<span data-ttu-id="ef64f-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ef64f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef64f-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ef64f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef64f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef64f-130">CommonParameters</span></span>
<span data-ttu-id="ef64f-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef64f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef64f-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef64f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef64f-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef64f-133">INPUTS</span></span>

### <span data-ttu-id="ef64f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ef64f-134">System.String</span></span>

### <span data-ttu-id="ef64f-135">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="ef64f-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="ef64f-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef64f-136">OUTPUTS</span></span>

### <span data-ttu-id="ef64f-137">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="ef64f-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="ef64f-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef64f-138">NOTES</span></span>

## <span data-ttu-id="ef64f-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef64f-139">RELATED LINKS</span></span>