---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
ms.openlocfilehash: f5936bcbbf12308830fd158baa2c2d20f295694b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563012"
---
# <span data-ttu-id="0555b-101">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="0555b-101">New-AzureRmAlertRuleEmail</span></span>

## <span data-ttu-id="0555b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0555b-102">SYNOPSIS</span></span>
<span data-ttu-id="0555b-103">Создание действия электронной почты для правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="0555b-103">Creates an email action for an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0555b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0555b-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0555b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0555b-105">DESCRIPTION</span></span>
<span data-ttu-id="0555b-106">Командлет **New-AzureRmAlertRuleEmail** создает действие электронной почты для правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="0555b-106">The **New-AzureRmAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="0555b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0555b-107">EXAMPLES</span></span>

### <span data-ttu-id="0555b-108">Пример 1: Создание действия по электронной почте правила оповещения для владельцев служб</span><span class="sxs-lookup"><span data-stu-id="0555b-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="0555b-109">Эта команда создает действие по электронной почте правила оповещения, которое отправляется своим владельцам услуг при срабатывании правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="0555b-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="0555b-110">Пример 2: Создание действия по электронной почте для правила оповещения для владельцев, не связанных с обслуживанием</span><span class="sxs-lookup"><span data-stu-id="0555b-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="0555b-111">Эта команда создает действие по электронной почте правила оповещения для указанных адресов электронной почты, но не для владельцев служб.</span><span class="sxs-lookup"><span data-stu-id="0555b-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="0555b-112">Пример 3: Создание действия по электронной почте правила оповещения для владельцев услуг и не владельцев служб</span><span class="sxs-lookup"><span data-stu-id="0555b-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="0555b-113">Эта команда создает действие по электронной почте правила оповещения для указанного адреса и для владельцев служб.</span><span class="sxs-lookup"><span data-stu-id="0555b-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="0555b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0555b-114">PARAMETERS</span></span>

### <span data-ttu-id="0555b-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="0555b-115">-CustomEmail</span></span>
<span data-ttu-id="0555b-116">Задает список адресов электронной почты, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="0555b-116">Specifies a list of comma-separated e-mail addresses.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0555b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0555b-117">-DefaultProfile</span></span>
<span data-ttu-id="0555b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0555b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0555b-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="0555b-119">-SendToServiceOwner</span></span>
<span data-ttu-id="0555b-120">Указывает, что эта операция отправляет владельцам службы сообщение электронной почты при срабатывании правила.</span><span class="sxs-lookup"><span data-stu-id="0555b-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0555b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0555b-121">CommonParameters</span></span>
<span data-ttu-id="0555b-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0555b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0555b-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0555b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0555b-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0555b-124">INPUTS</span></span>

### <span data-ttu-id="0555b-125">System. String []</span><span class="sxs-lookup"><span data-stu-id="0555b-125">System.String[]</span></span>

### <span data-ttu-id="0555b-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0555b-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0555b-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0555b-127">OUTPUTS</span></span>

### <span data-ttu-id="0555b-128">Microsoft. Azure. Management. Monitor. Management. Models. RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="0555b-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="0555b-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="0555b-129">NOTES</span></span>

## <span data-ttu-id="0555b-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0555b-130">RELATED LINKS</span></span>

[<span data-ttu-id="0555b-131">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="0555b-131">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="0555b-132">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="0555b-132">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="0555b-133">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="0555b-133">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="0555b-134">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="0555b-134">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)

