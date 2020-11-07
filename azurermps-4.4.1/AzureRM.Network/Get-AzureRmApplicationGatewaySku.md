---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: 09639badc9ac96525456b7a9556c8e2afa7ebf2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563911"
---
# <span data-ttu-id="f00b0-101">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f00b0-101">Get-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="f00b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f00b0-102">SYNOPSIS</span></span>
<span data-ttu-id="f00b0-103">Возвращает SKU шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="f00b0-103">Gets the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f00b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f00b0-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f00b0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f00b0-105">DESCRIPTION</span></span>
<span data-ttu-id="f00b0-106">Командлет **Get-AzureRmApplicationGatewaySku** получает единицу хранения (SKU) шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="f00b0-106">The **Get-AzureRmApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="f00b0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f00b0-107">EXAMPLES</span></span>

### <span data-ttu-id="f00b0-108">Пример 1: получение SKU шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="f00b0-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzureRmApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="f00b0-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет результат в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="f00b0-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="f00b0-110">Вторая команда возвращает SKU шлюза приложения с именем ApplicationGateway01 и сохраняет результат в переменной с именем $SKU.</span><span class="sxs-lookup"><span data-stu-id="f00b0-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="f00b0-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f00b0-111">PARAMETERS</span></span>

### <span data-ttu-id="f00b0-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f00b0-112">-ApplicationGateway</span></span>
<span data-ttu-id="f00b0-113">Указывает объект шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="f00b0-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="f00b0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f00b0-114">-DefaultProfile</span></span>
<span data-ttu-id="f00b0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f00b0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f00b0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f00b0-116">CommonParameters</span></span>
<span data-ttu-id="f00b0-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f00b0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f00b0-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f00b0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f00b0-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f00b0-119">INPUTS</span></span>

### <span data-ttu-id="f00b0-120">System. String</span><span class="sxs-lookup"><span data-stu-id="f00b0-120">System.String</span></span>

## <span data-ttu-id="f00b0-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f00b0-121">OUTPUTS</span></span>

### <span data-ttu-id="f00b0-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f00b0-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="f00b0-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="f00b0-123">NOTES</span></span>

## <span data-ttu-id="f00b0-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f00b0-124">RELATED LINKS</span></span>

[<span data-ttu-id="f00b0-125">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f00b0-125">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="f00b0-126">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f00b0-126">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)

