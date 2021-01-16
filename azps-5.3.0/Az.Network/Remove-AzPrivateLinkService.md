---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
ms.openlocfilehash: 4b95610996aad93144ccaa749c41319cf513ff7f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519961"
---
# <span data-ttu-id="585d6-101">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="585d6-101">Remove-AzPrivateLinkService</span></span>

## <span data-ttu-id="585d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="585d6-102">SYNOPSIS</span></span>
<span data-ttu-id="585d6-103">Удаление службы частных ссылок</span><span class="sxs-lookup"><span data-stu-id="585d6-103">Removes a private link service</span></span>

## <span data-ttu-id="585d6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="585d6-104">SYNTAX</span></span>

```
Remove-AzPrivateLinkService -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="585d6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="585d6-105">DESCRIPTION</span></span>
<span data-ttu-id="585d6-106">Для **удаления частной службы ссылок удаляется cmdlet Remove-AzPrivateLinkService.**</span><span class="sxs-lookup"><span data-stu-id="585d6-106">The **Remove-AzPrivateLinkService** cmdlet removes a private link service</span></span>

## <span data-ttu-id="585d6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="585d6-107">EXAMPLES</span></span>

### <span data-ttu-id="585d6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="585d6-108">Example 1</span></span>
```
Remove-AzPrivateLinkService -ResourceGroupName TestResourceGroup -Name TestPrivateLinkService
```

<span data-ttu-id="585d6-109">В этом примере удаляется частная служба с именем TestPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="585d6-109">This example removes a private link service named TestPrivateLinkService.</span></span>

## <span data-ttu-id="585d6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="585d6-110">PARAMETERS</span></span>

### <span data-ttu-id="585d6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="585d6-111">-AsJob</span></span>
<span data-ttu-id="585d6-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="585d6-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="585d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="585d6-113">-DefaultProfile</span></span>
<span data-ttu-id="585d6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="585d6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="585d6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="585d6-115">-Force</span></span>
<span data-ttu-id="585d6-116">Не спрашивайте подтверждения, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="585d6-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="585d6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="585d6-117">-Name</span></span>
<span data-ttu-id="585d6-118">Имя службы.</span><span class="sxs-lookup"><span data-stu-id="585d6-118">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="585d6-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="585d6-119">-PassThru</span></span>
<span data-ttu-id="585d6-120">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="585d6-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="585d6-121">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="585d6-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="585d6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="585d6-122">-ResourceGroupName</span></span>
<span data-ttu-id="585d6-123">Имя группы ресурсов для закрытой службы ссылок.</span><span class="sxs-lookup"><span data-stu-id="585d6-123">The resource group name of the private link service.</span></span>

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

### <span data-ttu-id="585d6-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="585d6-124">-Confirm</span></span>
<span data-ttu-id="585d6-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="585d6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="585d6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="585d6-126">-WhatIf</span></span>
<span data-ttu-id="585d6-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="585d6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="585d6-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="585d6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="585d6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="585d6-129">CommonParameters</span></span>
<span data-ttu-id="585d6-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="585d6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="585d6-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="585d6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="585d6-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="585d6-132">INPUTS</span></span>

### <span data-ttu-id="585d6-133">System.String</span><span class="sxs-lookup"><span data-stu-id="585d6-133">System.String</span></span>

## <span data-ttu-id="585d6-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="585d6-134">OUTPUTS</span></span>

### <span data-ttu-id="585d6-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="585d6-135">System.Boolean</span></span>

## <span data-ttu-id="585d6-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="585d6-136">NOTES</span></span>

## <span data-ttu-id="585d6-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="585d6-137">RELATED LINKS</span></span>

[<span data-ttu-id="585d6-138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="585d6-138">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="585d6-139">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="585d6-139">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)