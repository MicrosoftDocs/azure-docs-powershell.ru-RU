---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
ms.openlocfilehash: 9141f695a965fac5e3e71ee516aacf08cfd58a40
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720527"
---
# <span data-ttu-id="cbd03-101">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="cbd03-101">New-AzIntegrationAccount</span></span>

## <span data-ttu-id="cbd03-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cbd03-102">SYNOPSIS</span></span>
<span data-ttu-id="cbd03-103">Создание учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="cbd03-103">Creates an integration account.</span></span>

## <span data-ttu-id="cbd03-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cbd03-104">SYNTAX</span></span>

```
New-AzIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbd03-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbd03-105">DESCRIPTION</span></span>
<span data-ttu-id="cbd03-106">Командлет **New-AzIntegrationAccount** создает учетную запись интеграции.</span><span class="sxs-lookup"><span data-stu-id="cbd03-106">The **New-AzIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="cbd03-107">Этот командлет возвращает объект, представляющий учетную запись интеграции. Укажите имя, расположение, имя группы ресурсов и название SKU.</span><span class="sxs-lookup"><span data-stu-id="cbd03-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>
<span data-ttu-id="cbd03-108">Значения файла параметров шаблона, заданные в командной строке, имеют приоритет над значениями параметров шаблона в объекте параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="cbd03-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="cbd03-109">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="cbd03-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="cbd03-110">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="cbd03-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="cbd03-111">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="cbd03-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cbd03-112">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="cbd03-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cbd03-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cbd03-113">EXAMPLES</span></span>

### <span data-ttu-id="cbd03-114">Пример 1: создание учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="cbd03-114">Example 1: Create an integration account</span></span>
```
PS C:\>New-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Location "brazilsouth" -Sku "Standard"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="cbd03-115">Эта команда создает учетную запись интеграции с именем IntegrationAccount31 в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cbd03-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="cbd03-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cbd03-116">PARAMETERS</span></span>

### <span data-ttu-id="cbd03-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbd03-117">-DefaultProfile</span></span>
<span data-ttu-id="cbd03-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cbd03-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cbd03-119">-Location</span><span class="sxs-lookup"><span data-stu-id="cbd03-119">-Location</span></span>
<span data-ttu-id="cbd03-120">Указывает расположение для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="cbd03-120">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="cbd03-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cbd03-121">-Name</span></span>
<span data-ttu-id="cbd03-122">Указывает имя для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="cbd03-122">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="cbd03-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbd03-123">-ResourceGroupName</span></span>
<span data-ttu-id="cbd03-124">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cbd03-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cbd03-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="cbd03-125">-Sku</span></span>
<span data-ttu-id="cbd03-126">Указывает имя SKU для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="cbd03-126">Specifies a SKU name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbd03-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cbd03-127">-Confirm</span></span>
<span data-ttu-id="cbd03-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cbd03-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbd03-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbd03-129">-WhatIf</span></span>
<span data-ttu-id="cbd03-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cbd03-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbd03-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cbd03-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbd03-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbd03-132">CommonParameters</span></span>
<span data-ttu-id="cbd03-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cbd03-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbd03-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbd03-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbd03-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cbd03-135">INPUTS</span></span>

### <span data-ttu-id="cbd03-136">System. String</span><span class="sxs-lookup"><span data-stu-id="cbd03-136">System.String</span></span>

## <span data-ttu-id="cbd03-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbd03-137">OUTPUTS</span></span>

### <span data-ttu-id="cbd03-138">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="cbd03-138">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="cbd03-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="cbd03-139">NOTES</span></span>

## <span data-ttu-id="cbd03-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cbd03-140">RELATED LINKS</span></span>

[<span data-ttu-id="cbd03-141">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="cbd03-141">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="cbd03-142">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="cbd03-142">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="cbd03-143">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="cbd03-143">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)

