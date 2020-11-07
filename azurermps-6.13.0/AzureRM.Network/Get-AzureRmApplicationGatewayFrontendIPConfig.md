---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: f460b2668309e942b383adeab581d9772c9bfca2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568481"
---
# <span data-ttu-id="250ab-101">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="250ab-101">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="250ab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="250ab-102">SYNOPSIS</span></span>
<span data-ttu-id="250ab-103">Получает интерфейсную конфигурацию IP-конфигурации для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="250ab-103">Gets the front-end IP configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="250ab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="250ab-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="250ab-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="250ab-105">DESCRIPTION</span></span>
<span data-ttu-id="250ab-106">Командлет **Get-AzureRmApplicationGatewayFrontendIPConfig** получает интерфейсную конфигурацию IP-конфигурации для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="250ab-106">The **Get-AzureRmApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="250ab-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="250ab-107">EXAMPLES</span></span>

### <span data-ttu-id="250ab-108">Пример 1: получение указанной переднего плана IP-конфигурации</span><span class="sxs-lookup"><span data-stu-id="250ab-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="250ab-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 из группы ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw. Вторая команда получает клиентскую IP-конфигурацию с именем FrontEndIP01 from $AppGw и сохраняет ее в переменной $FrontEndIP.</span><span class="sxs-lookup"><span data-stu-id="250ab-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="250ab-110">Пример 2: получение списка конфигураций IP-адресов интерфейсов</span><span class="sxs-lookup"><span data-stu-id="250ab-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzureRmApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="250ab-111">Первая команда получает шлюз приложения с именем ApplicationGateway01 из группы ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw. Вторая команда получает список IP-конфигураций переднего плана из $AppGw и сохраняет их в переменной $FrontEndIPs.</span><span class="sxs-lookup"><span data-stu-id="250ab-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="250ab-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="250ab-112">PARAMETERS</span></span>

### <span data-ttu-id="250ab-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="250ab-113">-ApplicationGateway</span></span>
<span data-ttu-id="250ab-114">Указывает объект шлюза приложения, который содержит интерфейсную конфигурацию IP.</span><span class="sxs-lookup"><span data-stu-id="250ab-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="250ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="250ab-115">-DefaultProfile</span></span>
<span data-ttu-id="250ab-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="250ab-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="250ab-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="250ab-117">-Name</span></span>
<span data-ttu-id="250ab-118">Задает имя интерфейса IP-конфигурации, который получает интерфейсный командлет.</span><span class="sxs-lookup"><span data-stu-id="250ab-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="250ab-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="250ab-119">CommonParameters</span></span>
<span data-ttu-id="250ab-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="250ab-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="250ab-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="250ab-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="250ab-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="250ab-122">INPUTS</span></span>

### <span data-ttu-id="250ab-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="250ab-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="250ab-124">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="250ab-124">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="250ab-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="250ab-125">OUTPUTS</span></span>

### <span data-ttu-id="250ab-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="250ab-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="250ab-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="250ab-127">NOTES</span></span>

## <span data-ttu-id="250ab-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="250ab-128">RELATED LINKS</span></span>

[<span data-ttu-id="250ab-129">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="250ab-129">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="250ab-130">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="250ab-130">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="250ab-131">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="250ab-131">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="250ab-132">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="250ab-132">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)

