---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 94cb9e07bc5d4b8d59e543c39ddada5386ebcb27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560071"
---
# <span data-ttu-id="f086f-101">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f086f-101">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="f086f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f086f-102">SYNOPSIS</span></span>
<span data-ttu-id="f086f-103">Удаляет интерфейсную конфигурацию IP из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="f086f-103">Removes a front-end IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f086f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f086f-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f086f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f086f-105">DESCRIPTION</span></span>
<span data-ttu-id="f086f-106">Командлет **Remove-AzureRmApplicationGatewayFrontendIPConfig** удаляет IP-интерфейс из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="f086f-106">The **Remove-AzureRmApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="f086f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f086f-107">EXAMPLES</span></span>

### <span data-ttu-id="f086f-108">Пример 1: удаление интерфейсной конфигурации IP</span><span class="sxs-lookup"><span data-stu-id="f086f-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="f086f-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f086f-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f086f-110">Вторая команда удаляет IP-конфигурацию переднего плана с именем FrontEndIP02 из шлюза приложений, хранящегося в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f086f-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="f086f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f086f-111">PARAMETERS</span></span>

### <span data-ttu-id="f086f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f086f-112">-ApplicationGateway</span></span>
<span data-ttu-id="f086f-113">Указывает шлюз приложений, из которого нужно удалить IP-конфигурацию интерфейсной части.</span><span class="sxs-lookup"><span data-stu-id="f086f-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f086f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f086f-114">-DefaultProfile</span></span>
<span data-ttu-id="f086f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f086f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f086f-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f086f-116">-Name</span></span>
<span data-ttu-id="f086f-117">Указывает имя удаляемой интерфейсной IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f086f-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="f086f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f086f-118">CommonParameters</span></span>
<span data-ttu-id="f086f-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f086f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f086f-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f086f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f086f-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f086f-121">INPUTS</span></span>

### <span data-ttu-id="f086f-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f086f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="f086f-123">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f086f-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="f086f-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f086f-124">OUTPUTS</span></span>

### <span data-ttu-id="f086f-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f086f-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f086f-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="f086f-126">NOTES</span></span>

## <span data-ttu-id="f086f-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f086f-127">RELATED LINKS</span></span>

[<span data-ttu-id="f086f-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f086f-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f086f-129">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f086f-129">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f086f-130">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f086f-130">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f086f-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f086f-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)

