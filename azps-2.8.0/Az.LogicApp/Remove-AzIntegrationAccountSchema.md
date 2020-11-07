---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
ms.openlocfilehash: 1137ba802bc1ccd920b45c895b70aee2f8a8e7ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720495"
---
# <span data-ttu-id="f39fd-101">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="f39fd-101">Remove-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="f39fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f39fd-102">SYNOPSIS</span></span>
<span data-ttu-id="f39fd-103">Удаляет схему учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f39fd-103">Removes an integration account schema.</span></span>

## <span data-ttu-id="f39fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f39fd-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f39fd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f39fd-105">DESCRIPTION</span></span>
<span data-ttu-id="f39fd-106">Командлет **Remove-AzIntegrationAccountSchema** удаляет схему учетной записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f39fd-106">The **Remove-AzIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="f39fd-107">Указание имени учетной записи интеграции, имени группы ресурсов и имени схемы.</span><span class="sxs-lookup"><span data-stu-id="f39fd-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="f39fd-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="f39fd-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f39fd-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="f39fd-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f39fd-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="f39fd-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f39fd-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="f39fd-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f39fd-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f39fd-112">EXAMPLES</span></span>

### <span data-ttu-id="f39fd-113">Пример 1: удаление схемы учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="f39fd-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="f39fd-114">Эта команда удаляет схему учетной записи интеграции с именем IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="f39fd-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="f39fd-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f39fd-115">PARAMETERS</span></span>

### <span data-ttu-id="f39fd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f39fd-116">-DefaultProfile</span></span>
<span data-ttu-id="f39fd-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f39fd-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f39fd-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f39fd-118">-Force</span></span>
<span data-ttu-id="f39fd-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f39fd-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f39fd-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f39fd-120">-Name</span></span>
<span data-ttu-id="f39fd-121">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f39fd-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="f39fd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f39fd-122">-ResourceGroupName</span></span>
<span data-ttu-id="f39fd-123">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f39fd-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f39fd-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="f39fd-124">-SchemaName</span></span>
<span data-ttu-id="f39fd-125">Указывает имя схемы учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f39fd-125">Specifies the name of an integration account schema.</span></span>

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

### <span data-ttu-id="f39fd-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f39fd-126">-Confirm</span></span>
<span data-ttu-id="f39fd-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f39fd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f39fd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f39fd-128">-WhatIf</span></span>
<span data-ttu-id="f39fd-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f39fd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f39fd-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f39fd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f39fd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f39fd-131">CommonParameters</span></span>
<span data-ttu-id="f39fd-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f39fd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f39fd-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f39fd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f39fd-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f39fd-134">INPUTS</span></span>

### <span data-ttu-id="f39fd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f39fd-135">System.String</span></span>

## <span data-ttu-id="f39fd-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f39fd-136">OUTPUTS</span></span>

### <span data-ttu-id="f39fd-137">System. void</span><span class="sxs-lookup"><span data-stu-id="f39fd-137">System.Void</span></span>

## <span data-ttu-id="f39fd-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="f39fd-138">NOTES</span></span>

## <span data-ttu-id="f39fd-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f39fd-139">RELATED LINKS</span></span>

[<span data-ttu-id="f39fd-140">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="f39fd-140">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="f39fd-141">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="f39fd-141">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="f39fd-142">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="f39fd-142">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)

