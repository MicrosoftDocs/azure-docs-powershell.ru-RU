---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
ms.openlocfilehash: 7342601bba3c963131728f02773cb3b84e917bb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720501"
---
# <span data-ttu-id="86563-101">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="86563-101">Remove-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="86563-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="86563-102">SYNOPSIS</span></span>
<span data-ttu-id="86563-103">Удаляет карту учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="86563-103">Removes an integration account map.</span></span>

## <span data-ttu-id="86563-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="86563-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86563-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86563-105">DESCRIPTION</span></span>
<span data-ttu-id="86563-106">Командлет **Remove-AzIntegrationAccountMap** удаляет карту учетной записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="86563-106">The **Remove-AzIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="86563-107">Укажите имя учетной записи интеграции, имя группы ресурсов и имя карты.</span><span class="sxs-lookup"><span data-stu-id="86563-107">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="86563-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="86563-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="86563-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="86563-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="86563-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="86563-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="86563-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="86563-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="86563-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="86563-112">EXAMPLES</span></span>

### <span data-ttu-id="86563-113">Пример 1: удаление карты учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="86563-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="86563-114">Эта команда удаляет карту учетной записи интеграции с именем IntegrationAccountMap47.</span><span class="sxs-lookup"><span data-stu-id="86563-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="86563-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="86563-115">PARAMETERS</span></span>

### <span data-ttu-id="86563-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86563-116">-DefaultProfile</span></span>
<span data-ttu-id="86563-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="86563-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86563-118">-Force</span><span class="sxs-lookup"><span data-stu-id="86563-118">-Force</span></span>
<span data-ttu-id="86563-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="86563-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="86563-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="86563-120">-MapName</span></span>
<span data-ttu-id="86563-121">Указывает имя карты учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="86563-121">Specifies the name of the integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86563-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="86563-122">-Name</span></span>
<span data-ttu-id="86563-123">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="86563-123">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86563-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86563-124">-ResourceGroupName</span></span>
<span data-ttu-id="86563-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="86563-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86563-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86563-126">-Confirm</span></span>
<span data-ttu-id="86563-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="86563-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86563-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86563-128">-WhatIf</span></span>
<span data-ttu-id="86563-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="86563-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86563-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="86563-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86563-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86563-131">CommonParameters</span></span>
<span data-ttu-id="86563-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="86563-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86563-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86563-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86563-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="86563-134">INPUTS</span></span>

### <span data-ttu-id="86563-135">System. String</span><span class="sxs-lookup"><span data-stu-id="86563-135">System.String</span></span>

## <span data-ttu-id="86563-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="86563-136">OUTPUTS</span></span>

### <span data-ttu-id="86563-137">System. void</span><span class="sxs-lookup"><span data-stu-id="86563-137">System.Void</span></span>

## <span data-ttu-id="86563-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="86563-138">NOTES</span></span>

## <span data-ttu-id="86563-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86563-139">RELATED LINKS</span></span>

[<span data-ttu-id="86563-140">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="86563-140">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="86563-141">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="86563-141">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="86563-142">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="86563-142">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)

