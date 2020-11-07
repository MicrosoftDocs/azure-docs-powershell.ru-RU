---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
ms.openlocfilehash: a2fc63409f36215d40fcf1e2e17c48b4dbe89e11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720255"
---
# <span data-ttu-id="6b796-101">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="6b796-101">Remove-AzContext</span></span>

## <span data-ttu-id="6b796-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b796-102">SYNOPSIS</span></span>
<span data-ttu-id="6b796-103">Удаление контекста из набора доступных контекстов</span><span class="sxs-lookup"><span data-stu-id="6b796-103">Remove a context from the set of available contexts</span></span>

## <span data-ttu-id="6b796-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b796-104">SYNTAX</span></span>

### <span data-ttu-id="6b796-105">RemoveByInputObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6b796-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b796-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="6b796-106">RemoveByName</span></span>
```
Remove-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="6b796-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b796-107">DESCRIPTION</span></span>
<span data-ttu-id="6b796-108">Удаление контекста Azure из набора контекстов</span><span class="sxs-lookup"><span data-stu-id="6b796-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="6b796-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b796-109">EXAMPLES</span></span>

### <span data-ttu-id="6b796-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6b796-110">Example 1</span></span>
```
PS C:\> Remove-AzContext -Name Default
```

<span data-ttu-id="6b796-111">Удалить контекст с именем по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6b796-111">Remove the context named default</span></span>

## <span data-ttu-id="6b796-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b796-112">PARAMETERS</span></span>

### <span data-ttu-id="6b796-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b796-113">-DefaultProfile</span></span>
<span data-ttu-id="6b796-114">Учетные данные, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6b796-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b796-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6b796-115">-Force</span></span>
<span data-ttu-id="6b796-116">Удалить контекст даже в том случае, если это defualt</span><span class="sxs-lookup"><span data-stu-id="6b796-116">Remove context even if it is the defualt</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b796-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b796-117">-InputObject</span></span>
<span data-ttu-id="6b796-118">Контекстный объект, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="6b796-118">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b796-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6b796-119">-Name</span></span>
<span data-ttu-id="6b796-120">Имя контекста.</span><span class="sxs-lookup"><span data-stu-id="6b796-120">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b796-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b796-121">-PassThru</span></span>
<span data-ttu-id="6b796-122">Вернуть удаленный контекст</span><span class="sxs-lookup"><span data-stu-id="6b796-122">Return the removed context</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b796-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="6b796-123">-Scope</span></span>
<span data-ttu-id="6b796-124">Определяет область изменений контекста, например, применимы ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="6b796-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b796-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b796-125">-Confirm</span></span>
<span data-ttu-id="6b796-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6b796-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b796-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b796-127">-WhatIf</span></span>
<span data-ttu-id="6b796-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6b796-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b796-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6b796-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b796-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b796-130">CommonParameters</span></span>
<span data-ttu-id="6b796-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b796-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b796-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b796-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b796-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b796-133">INPUTS</span></span>

### <span data-ttu-id="6b796-134">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="6b796-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="6b796-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b796-135">OUTPUTS</span></span>

### <span data-ttu-id="6b796-136">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="6b796-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="6b796-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b796-137">NOTES</span></span>

## <span data-ttu-id="6b796-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b796-138">RELATED LINKS</span></span>