---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
ms.openlocfilehash: ae9b9f37a20f63a502da2904fd6d94f8a6aa281f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720477"
---
# <span data-ttu-id="9690c-101">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="9690c-101">Set-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="9690c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9690c-102">SYNOPSIS</span></span>
<span data-ttu-id="9690c-103">Изменение партнера учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="9690c-103">Modifies an integration account partner.</span></span>

## <span data-ttu-id="9690c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9690c-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9690c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9690c-105">DESCRIPTION</span></span>
<span data-ttu-id="9690c-106">Командлет **Set-AzIntegrationAccountPartner** изменяет партнера учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="9690c-106">The **Set-AzIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="9690c-107">Этот командлет возвращает объект, представляющий партнера по учетным записям интеграции.</span><span class="sxs-lookup"><span data-stu-id="9690c-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="9690c-108">Укажите имя учетной записи интеграции, имя группы ресурсов и имя партнера.</span><span class="sxs-lookup"><span data-stu-id="9690c-108">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="9690c-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="9690c-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9690c-110">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="9690c-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9690c-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="9690c-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9690c-112">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="9690c-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="9690c-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9690c-113">EXAMPLES</span></span>

### <span data-ttu-id="9690c-114">Пример 1: изменение партнера учетной записи для интеграции</span><span class="sxs-lookup"><span data-stu-id="9690c-114">Example 1: Modify an integration account partner</span></span>
```
PS C:\>Set-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata
```

<span data-ttu-id="9690c-115">Эта команда изменяет партнера учетной записи интеграции с именем IntegrationAccountPartner22 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9690c-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="9690c-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9690c-116">PARAMETERS</span></span>

### <span data-ttu-id="9690c-117">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="9690c-117">-BusinessIdentities</span></span>
<span data-ttu-id="9690c-118">Указывает бизнес-идентификаторы для партнера по учетным записям интеграции.</span><span class="sxs-lookup"><span data-stu-id="9690c-118">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="9690c-119">Укажите хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="9690c-119">Specify a hash table.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9690c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9690c-120">-DefaultProfile</span></span>
<span data-ttu-id="9690c-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9690c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9690c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="9690c-122">-Force</span></span>
<span data-ttu-id="9690c-123">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="9690c-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9690c-124">-Metadata</span><span class="sxs-lookup"><span data-stu-id="9690c-124">-Metadata</span></span>
<span data-ttu-id="9690c-125">Указывает объект метаданных для партнера.</span><span class="sxs-lookup"><span data-stu-id="9690c-125">Specifies a metadata object for the partner.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9690c-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9690c-126">-Name</span></span>
<span data-ttu-id="9690c-127">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="9690c-127">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9690c-128">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="9690c-128">-PartnerName</span></span>
<span data-ttu-id="9690c-129">Указывает имя партнера учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="9690c-129">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="9690c-130">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="9690c-130">-PartnerType</span></span>
<span data-ttu-id="9690c-131">Указывает тип учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="9690c-131">Specifies the type of the integration account.</span></span>
<span data-ttu-id="9690c-132">Этот параметр поддерживает тип B2B.</span><span class="sxs-lookup"><span data-stu-id="9690c-132">This parameter supports the type B2B.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: B2B

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9690c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9690c-133">-ResourceGroupName</span></span>
<span data-ttu-id="9690c-134">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9690c-134">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9690c-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9690c-135">-Confirm</span></span>
<span data-ttu-id="9690c-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9690c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9690c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9690c-137">-WhatIf</span></span>
<span data-ttu-id="9690c-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9690c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9690c-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9690c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9690c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9690c-140">CommonParameters</span></span>
<span data-ttu-id="9690c-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9690c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9690c-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9690c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9690c-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9690c-143">INPUTS</span></span>

### <span data-ttu-id="9690c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9690c-144">System.String</span></span>

## <span data-ttu-id="9690c-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9690c-145">OUTPUTS</span></span>

### <span data-ttu-id="9690c-146">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="9690c-146">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="9690c-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="9690c-147">NOTES</span></span>

## <span data-ttu-id="9690c-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9690c-148">RELATED LINKS</span></span>

[<span data-ttu-id="9690c-149">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="9690c-149">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="9690c-150">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="9690c-150">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="9690c-151">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="9690c-151">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

