---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
ms.openlocfilehash: 1091a8433cd226982d3f2addf7e02b2414020fe4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568223"
---
# <span data-ttu-id="1b9ec-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1b9ec-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="1b9ec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1b9ec-102">SYNOPSIS</span></span>
<span data-ttu-id="1b9ec-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="1b9ec-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b9ec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1b9ec-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b9ec-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b9ec-105">DESCRIPTION</span></span>
<span data-ttu-id="1b9ec-106">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="1b9ec-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="1b9ec-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1b9ec-107">EXAMPLES</span></span>

### <span data-ttu-id="1b9ec-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1b9ec-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="1b9ec-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="1b9ec-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="1b9ec-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1b9ec-110">PARAMETERS</span></span>

### <span data-ttu-id="1b9ec-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b9ec-111">-AsJob</span></span>
<span data-ttu-id="1b9ec-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1b9ec-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b9ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b9ec-113">-DefaultProfile</span></span>
<span data-ttu-id="1b9ec-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b9ec-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1b9ec-115">-Force</span></span>
<span data-ttu-id="1b9ec-116">Не запрашивать подтверждение, если вы хотите переделать ресурс</span><span class="sxs-lookup"><span data-stu-id="1b9ec-116">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b9ec-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1b9ec-117">-RouteFilter</span></span>
<span data-ttu-id="1b9ec-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1b9ec-118">The RouteFilter</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b9ec-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b9ec-119">-Confirm</span></span>
<span data-ttu-id="1b9ec-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b9ec-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b9ec-121">-WhatIf</span></span>
<span data-ttu-id="1b9ec-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b9ec-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b9ec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b9ec-124">CommonParameters</span></span>
<span data-ttu-id="1b9ec-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b9ec-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b9ec-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b9ec-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1b9ec-127">INPUTS</span></span>

### <span data-ttu-id="1b9ec-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1b9ec-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1b9ec-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b9ec-129">OUTPUTS</span></span>

### <span data-ttu-id="1b9ec-130">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1b9ec-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1b9ec-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="1b9ec-131">NOTES</span></span>

## <span data-ttu-id="1b9ec-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b9ec-132">RELATED LINKS</span></span>
