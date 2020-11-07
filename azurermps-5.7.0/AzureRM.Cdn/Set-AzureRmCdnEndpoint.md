---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
ms.openlocfilehash: 13b5b219ec789ac54332caa366cfb0277f0bfacb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563732"
---
# <span data-ttu-id="4d984-101">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d984-101">Set-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="4d984-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4d984-102">SYNOPSIS</span></span>
<span data-ttu-id="4d984-103">Обновляет конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="4d984-103">Updates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d984-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4d984-104">SYNTAX</span></span>

```
Set-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d984-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d984-105">DESCRIPTION</span></span>
<span data-ttu-id="4d984-106">Командлет **Set-AzureRmCdnEndpoint** обновляет конечную точку сети доставки содержимого (CDN) для Azure.</span><span class="sxs-lookup"><span data-stu-id="4d984-106">The **Set-AzureRmCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="4d984-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4d984-107">EXAMPLES</span></span>

## <span data-ttu-id="4d984-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4d984-108">PARAMETERS</span></span>

### <span data-ttu-id="4d984-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d984-109">-CdnEndpoint</span></span>
<span data-ttu-id="4d984-110">Указывает конечную точку, которую обновляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4d984-110">Specifies the endpoint that this cmdlet updates.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d984-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d984-111">-DefaultProfile</span></span>
<span data-ttu-id="4d984-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4d984-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d984-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d984-113">-Confirm</span></span>
<span data-ttu-id="4d984-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4d984-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d984-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d984-115">-WhatIf</span></span>
<span data-ttu-id="4d984-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4d984-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d984-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4d984-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d984-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d984-118">CommonParameters</span></span>
<span data-ttu-id="4d984-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4d984-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d984-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d984-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d984-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4d984-121">INPUTS</span></span>

### <span data-ttu-id="4d984-122">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d984-122">PSEndpoint</span></span>
<span data-ttu-id="4d984-123">Параметр "CdnEndpoint" принимает значение типа "PSEndpoint" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4d984-123">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="4d984-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d984-124">OUTPUTS</span></span>

### <span data-ttu-id="4d984-125">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d984-125">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="4d984-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="4d984-126">NOTES</span></span>

## <span data-ttu-id="4d984-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d984-127">RELATED LINKS</span></span>

[<span data-ttu-id="4d984-128">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d984-128">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="4d984-129">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d984-129">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="4d984-130">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d984-130">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="4d984-131">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d984-131">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="4d984-132">Остановить-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d984-132">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)

