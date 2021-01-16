---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
ms.openlocfilehash: 0645b3f5286526ba72db35fd8b9e048c895f4108
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509362"
---
# <span data-ttu-id="04fcf-101">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="04fcf-101">Remove-AzCdnCustomDomain</span></span>

## <span data-ttu-id="04fcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04fcf-102">SYNOPSIS</span></span>
<span data-ttu-id="04fcf-103">Удаляет пользовательский домен.</span><span class="sxs-lookup"><span data-stu-id="04fcf-103">Removes a custom domain.</span></span>

## <span data-ttu-id="04fcf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="04fcf-104">SYNTAX</span></span>

### <span data-ttu-id="04fcf-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="04fcf-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04fcf-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04fcf-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04fcf-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04fcf-107">DESCRIPTION</span></span>
<span data-ttu-id="04fcf-108">Для удаления пользовательского домена из конечной точки СЕТИ доставки содержимого (CDN) Azure удаляется **cmdn AzCdnCustomDomain.**</span><span class="sxs-lookup"><span data-stu-id="04fcf-108">The **Remove-AzCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="04fcf-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="04fcf-109">EXAMPLES</span></span>

## <span data-ttu-id="04fcf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04fcf-110">PARAMETERS</span></span>

### <span data-ttu-id="04fcf-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="04fcf-111">-CdnCustomDomain</span></span>
<span data-ttu-id="04fcf-112">Определяет настраиваемый домен, который этот cmdlet удаляет.</span><span class="sxs-lookup"><span data-stu-id="04fcf-112">Specifies the custom domain that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04fcf-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="04fcf-113">-CustomDomainName</span></span>
<span data-ttu-id="04fcf-114">Указывает имя ресурса для настраиваемого домена, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04fcf-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04fcf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04fcf-115">-DefaultProfile</span></span>
<span data-ttu-id="04fcf-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="04fcf-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04fcf-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="04fcf-117">-EndpointName</span></span>
<span data-ttu-id="04fcf-118">Указывает имя конечной точки, из которой этот cmdlet удаляет настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="04fcf-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04fcf-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04fcf-119">-PassThru</span></span>
<span data-ttu-id="04fcf-120">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="04fcf-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="04fcf-121">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="04fcf-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="04fcf-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="04fcf-122">-ProfileName</span></span>
<span data-ttu-id="04fcf-123">Указывает имя профиля, из которого этот cmdlet удаляет настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="04fcf-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04fcf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04fcf-124">-ResourceGroupName</span></span>
<span data-ttu-id="04fcf-125">Указывает имя группы ресурсов, из которой этот cmdlet удаляет настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="04fcf-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04fcf-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04fcf-126">-Confirm</span></span>
<span data-ttu-id="04fcf-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04fcf-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04fcf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04fcf-128">-WhatIf</span></span>
<span data-ttu-id="04fcf-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04fcf-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04fcf-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="04fcf-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04fcf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04fcf-131">CommonParameters</span></span>
<span data-ttu-id="04fcf-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04fcf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04fcf-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04fcf-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04fcf-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04fcf-134">INPUTS</span></span>

### <span data-ttu-id="04fcf-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="04fcf-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="04fcf-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="04fcf-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="04fcf-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="04fcf-137">OUTPUTS</span></span>

### <span data-ttu-id="04fcf-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="04fcf-138">System.Boolean</span></span>

## <span data-ttu-id="04fcf-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="04fcf-139">NOTES</span></span>

## <span data-ttu-id="04fcf-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04fcf-140">RELATED LINKS</span></span>

[<span data-ttu-id="04fcf-141">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="04fcf-141">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="04fcf-142">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="04fcf-142">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="04fcf-143">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="04fcf-143">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)

