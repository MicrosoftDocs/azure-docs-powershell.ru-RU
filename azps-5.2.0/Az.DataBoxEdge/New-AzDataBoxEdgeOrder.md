---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 4b8bd90cd96654fa137301379dceaabccad8a2ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397175"
---
# <span data-ttu-id="56bb5-101">New-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="56bb5-101">New-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="56bb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56bb5-102">SYNOPSIS</span></span>
<span data-ttu-id="56bb5-103">Создает новый заказ для устройства.</span><span class="sxs-lookup"><span data-stu-id="56bb5-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="56bb5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="56bb5-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56bb5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56bb5-105">DESCRIPTION</span></span>
<span data-ttu-id="56bb5-106">Для **устройства Edge data Box создается** новый порядок.</span><span class="sxs-lookup"><span data-stu-id="56bb5-106">The **New-AzDataBoxEdgeOrder** cmdlet creates a new order for a Data Box Edge device.</span></span> <span data-ttu-id="56bb5-107">Перед созданием заказа необходимо создать ресурс устройства с полем данных Edge.</span><span class="sxs-lookup"><span data-stu-id="56bb5-107">A Data Box Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="56bb5-108">В качестве параметров для создания заказа можно указать такие сведения, как контактное лицо, название компании, адрес электронной почты и т. д.</span><span class="sxs-lookup"><span data-stu-id="56bb5-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="56bb5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="56bb5-109">EXAMPLES</span></span>

### <span data-ttu-id="56bb5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="56bb5-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="56bb5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56bb5-111">PARAMETERS</span></span>

### <span data-ttu-id="56bb5-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="56bb5-112">-AddressLine1</span></span>
<span data-ttu-id="56bb5-113">Первая строка адреса</span><span class="sxs-lookup"><span data-stu-id="56bb5-113">Address first line</span></span>

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

### <span data-ttu-id="56bb5-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="56bb5-114">-AddressLine2</span></span>
<span data-ttu-id="56bb5-115">Вторая строка адреса</span><span class="sxs-lookup"><span data-stu-id="56bb5-115">Address second line</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56bb5-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="56bb5-116">-AddressLine3</span></span>
<span data-ttu-id="56bb5-117">Адрес, третий строка</span><span class="sxs-lookup"><span data-stu-id="56bb5-117">Address third line</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56bb5-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56bb5-118">-AsJob</span></span>
<span data-ttu-id="56bb5-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="56bb5-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56bb5-120">-Город</span><span class="sxs-lookup"><span data-stu-id="56bb5-120">-City</span></span>
<span data-ttu-id="56bb5-121">Название города</span><span class="sxs-lookup"><span data-stu-id="56bb5-121">Name of the City</span></span>

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

### <span data-ttu-id="56bb5-122">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="56bb5-122">-CompanyName</span></span>
<span data-ttu-id="56bb5-123">Название компании</span><span class="sxs-lookup"><span data-stu-id="56bb5-123">Name of the company</span></span>

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

### <span data-ttu-id="56bb5-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="56bb5-124">-ContactPerson</span></span>
<span data-ttu-id="56bb5-125">Имя контактного лица</span><span class="sxs-lookup"><span data-stu-id="56bb5-125">Name of the contact person</span></span>

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

### <span data-ttu-id="56bb5-126">-Country</span><span class="sxs-lookup"><span data-stu-id="56bb5-126">-Country</span></span>
<span data-ttu-id="56bb5-127">Название страны</span><span class="sxs-lookup"><span data-stu-id="56bb5-127">Name of the Country</span></span>

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

### <span data-ttu-id="56bb5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56bb5-128">-DefaultProfile</span></span>
<span data-ttu-id="56bb5-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56bb5-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56bb5-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="56bb5-130">-DeviceName</span></span>
<span data-ttu-id="56bb5-131">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="56bb5-131">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56bb5-132">-Электронная почта</span><span class="sxs-lookup"><span data-stu-id="56bb5-132">-Email</span></span>
<span data-ttu-id="56bb5-133">Список сообщений электронной почты для получения обновлений, принимает не более 10 сообщений</span><span class="sxs-lookup"><span data-stu-id="56bb5-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56bb5-134">-Phone</span><span class="sxs-lookup"><span data-stu-id="56bb5-134">-Phone</span></span>
<span data-ttu-id="56bb5-135">Номер телефона контактного лица</span><span class="sxs-lookup"><span data-stu-id="56bb5-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="56bb5-136">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="56bb5-136">-PostalCode</span></span>
<span data-ttu-id="56bb5-137">Почтовый индекс адреса</span><span class="sxs-lookup"><span data-stu-id="56bb5-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="56bb5-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56bb5-138">-ResourceGroupName</span></span>
<span data-ttu-id="56bb5-139">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="56bb5-139">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56bb5-140">-State</span><span class="sxs-lookup"><span data-stu-id="56bb5-140">-State</span></span>
<span data-ttu-id="56bb5-141">Название штата</span><span class="sxs-lookup"><span data-stu-id="56bb5-141">Name of the State</span></span>

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

### <span data-ttu-id="56bb5-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56bb5-142">-Confirm</span></span>
<span data-ttu-id="56bb5-143">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="56bb5-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56bb5-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56bb5-144">-WhatIf</span></span>
<span data-ttu-id="56bb5-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56bb5-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56bb5-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="56bb5-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56bb5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56bb5-147">CommonParameters</span></span>
<span data-ttu-id="56bb5-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56bb5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56bb5-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56bb5-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56bb5-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56bb5-150">INPUTS</span></span>

### <span data-ttu-id="56bb5-151">System.String</span><span class="sxs-lookup"><span data-stu-id="56bb5-151">System.String</span></span>

## <span data-ttu-id="56bb5-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="56bb5-152">OUTPUTS</span></span>

### <span data-ttu-id="56bb5-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="56bb5-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="56bb5-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="56bb5-154">NOTES</span></span>

## <span data-ttu-id="56bb5-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56bb5-155">RELATED LINKS</span></span>