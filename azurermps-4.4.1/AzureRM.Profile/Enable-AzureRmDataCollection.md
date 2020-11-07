---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmDataCollection.md
ms.openlocfilehash: 4a29a1d57d903edb0e19689750de2bad45b2c2f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565189"
---
# <span data-ttu-id="8d9d8-101">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="8d9d8-101">Enable-AzureRmDataCollection</span></span>

## <span data-ttu-id="8d9d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8d9d8-102">SYNOPSIS</span></span>
<span data-ttu-id="8d9d8-103">Позволяет Azure PowerShell собирать данные, чтобы улучшить взаимодействие с пользователем с помощью командлетов AzurePowerShell.</span><span class="sxs-lookup"><span data-stu-id="8d9d8-103">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="8d9d8-104">Выполнение этого командлета наследуется в сборе данных для текущего пользователя на текущем компьютере.</span><span class="sxs-lookup"><span data-stu-id="8d9d8-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="8d9d8-105">Никакие данные не собираются, пока не будет явно задействовано.</span><span class="sxs-lookup"><span data-stu-id="8d9d8-105">No data is collected unless you explicitly opt in.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d9d8-106">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8d9d8-106">SYNTAX</span></span>

```
Enable-AzureRmDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d9d8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d9d8-107">DESCRIPTION</span></span>
<span data-ttu-id="8d9d8-108">Вы можете улучшить взаимодействие с использованием Microsoft Cloud и Azure PowerShell, перейдя в коллекцию данных.</span><span class="sxs-lookup"><span data-stu-id="8d9d8-108">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="8d9d8-109">Azure PowerShell не собирает данные без согласия пользователя, поэтому вы должны явно присоединиться, выполнив Enable-AzureRmDataCollection или ответив на "Да", когда Azure PowerShell попросит вас собрать данные при первом запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8d9d8-109">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="8d9d8-110">Корпорация Майкрософт собирает собранные данные для выявления закономерностей использования, для выявления распространенных проблем и для повышения эффективности использования Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8d9d8-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="8d9d8-111">Microsoft Azure PowerShell не может собирать конфиденциальные данные и любые сведения, которые можно идентифицировать.</span><span class="sxs-lookup"><span data-stu-id="8d9d8-111">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="8d9d8-112">Запустите командлет Enable-AzureRMDataCollection, чтобы включить сбор данных для текущего пользователя на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="8d9d8-112">Run the Enable-AzureRMDataCollection cmdlet to enable data collection for the current user on the current machine.</span></span>
<span data-ttu-id="8d9d8-113">Это предотвратит вывод запроса о сборе данных текущим пользователем при первом выполнении командлетов.</span><span class="sxs-lookup"><span data-stu-id="8d9d8-113">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="8d9d8-114">Чтобы отключить сбор данных для текущего пользователя, выполните командлет Disable-AzureRmDataCollection.</span><span class="sxs-lookup"><span data-stu-id="8d9d8-114">To disable data collection for the current user, run the Disable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="8d9d8-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8d9d8-115">EXAMPLES</span></span>

### <span data-ttu-id="8d9d8-116">Пример 1: Включение сбора данных для текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="8d9d8-116">Example 1: Enabling data collection for the current user</span></span>
```
PS C:\> Enable-AzureRmDataCollection
```

<span data-ttu-id="8d9d8-117">В этом примере показано, как включить сбор данных для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="8d9d8-117">This example shows how to enable data collection for the current user.</span></span>

## <span data-ttu-id="8d9d8-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8d9d8-118">PARAMETERS</span></span>

### <span data-ttu-id="8d9d8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d9d8-119">-DefaultProfile</span></span>
<span data-ttu-id="8d9d8-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d9d8-120">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d9d8-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d9d8-121">-Confirm</span></span>
<span data-ttu-id="8d9d8-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8d9d8-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d9d8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d9d8-123">-WhatIf</span></span>
<span data-ttu-id="8d9d8-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8d9d8-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d9d8-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8d9d8-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d9d8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d9d8-126">CommonParameters</span></span>
<span data-ttu-id="8d9d8-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8d9d8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d9d8-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d9d8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d9d8-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8d9d8-129">INPUTS</span></span>

## <span data-ttu-id="8d9d8-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d9d8-130">OUTPUTS</span></span>

### <span data-ttu-id="8d9d8-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="8d9d8-131">None</span></span>

## <span data-ttu-id="8d9d8-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="8d9d8-132">NOTES</span></span>

## <span data-ttu-id="8d9d8-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d9d8-133">RELATED LINKS</span></span>

[<span data-ttu-id="8d9d8-134">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="8d9d8-134">Disable-AzureRmDataCollection</span></span>](./Disable-AzureRmDataCollection.md)
