---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: 1012bd4da163b992aec049643feb1e3fd8b4bf76
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519969"
---
# <span data-ttu-id="61bee-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="61bee-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="61bee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61bee-102">SYNOPSIS</span></span>
<span data-ttu-id="61bee-103">Удаляет группу зон DNS.</span><span class="sxs-lookup"><span data-stu-id="61bee-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="61bee-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="61bee-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61bee-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61bee-105">DESCRIPTION</span></span>
<span data-ttu-id="61bee-106">Для удаления группы зон DNS удаляется **cmdlet Remove-AzPrivateDnsZoneGroup.**</span><span class="sxs-lookup"><span data-stu-id="61bee-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="61bee-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="61bee-107">EXAMPLES</span></span>

### <span data-ttu-id="61bee-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="61bee-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="61bee-109">В примере выше из конечной точки test-pr-endpoint удаляется группа DNS zone grup named dnsgroup1.</span><span class="sxs-lookup"><span data-stu-id="61bee-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="61bee-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61bee-110">PARAMETERS</span></span>

### <span data-ttu-id="61bee-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61bee-111">-AsJob</span></span>
<span data-ttu-id="61bee-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="61bee-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61bee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61bee-113">-DefaultProfile</span></span>
<span data-ttu-id="61bee-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61bee-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61bee-115">-Force</span><span class="sxs-lookup"><span data-stu-id="61bee-115">-Force</span></span>
<span data-ttu-id="61bee-116">Не спрашивайте подтверждения, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="61bee-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="61bee-117">-Name</span><span class="sxs-lookup"><span data-stu-id="61bee-117">-Name</span></span>
<span data-ttu-id="61bee-118">Имя закрытой группы зон DNS.</span><span class="sxs-lookup"><span data-stu-id="61bee-118">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61bee-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61bee-119">-PassThru</span></span>
<span data-ttu-id="61bee-120">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="61bee-120">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="61bee-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="61bee-121">-PrivateEndpointName</span></span>
<span data-ttu-id="61bee-122">Имя закрытой конечной точки.</span><span class="sxs-lookup"><span data-stu-id="61bee-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="61bee-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61bee-123">-ResourceGroupName</span></span>
<span data-ttu-id="61bee-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="61bee-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="61bee-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61bee-125">-Confirm</span></span>
<span data-ttu-id="61bee-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61bee-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61bee-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61bee-127">-WhatIf</span></span>
<span data-ttu-id="61bee-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61bee-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61bee-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="61bee-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61bee-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61bee-130">CommonParameters</span></span>
<span data-ttu-id="61bee-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61bee-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61bee-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61bee-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61bee-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61bee-133">INPUTS</span></span>

### <span data-ttu-id="61bee-134">System.String</span><span class="sxs-lookup"><span data-stu-id="61bee-134">System.String</span></span>

## <span data-ttu-id="61bee-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="61bee-135">OUTPUTS</span></span>

### <span data-ttu-id="61bee-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="61bee-136">System.Boolean</span></span>

## <span data-ttu-id="61bee-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="61bee-137">NOTES</span></span>

## <span data-ttu-id="61bee-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61bee-138">RELATED LINKS</span></span>