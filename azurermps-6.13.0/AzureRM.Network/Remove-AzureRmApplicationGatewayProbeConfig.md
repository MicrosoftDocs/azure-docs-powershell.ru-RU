---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 40a7e63150384ac3fa2c330c079d5377c836d52e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562860"
---
# <span data-ttu-id="00d5c-101">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00d5c-101">Remove-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="00d5c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="00d5c-102">SYNOPSIS</span></span>
<span data-ttu-id="00d5c-103">Удаление проверки работоспособности из существующего шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="00d5c-103">Removes a health probe from an existing application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00d5c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="00d5c-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00d5c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00d5c-105">DESCRIPTION</span></span>
<span data-ttu-id="00d5c-106">Командлет Remove-AzureRmApplicationGatewayProbeConfig удаляет проверку работоспособности из существующего шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="00d5c-106">The Remove-AzureRmApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="00d5c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="00d5c-107">EXAMPLES</span></span>

### <span data-ttu-id="00d5c-108">Пример 1: Удаление проверки работоспособности из существующего шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="00d5c-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="00d5c-109">Эта команда удаляет проверку работоспособности с именем Probe04 из шлюза приложений с именем Gateway.</span><span class="sxs-lookup"><span data-stu-id="00d5c-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="00d5c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="00d5c-110">PARAMETERS</span></span>

### <span data-ttu-id="00d5c-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00d5c-111">-ApplicationGateway</span></span>
<span data-ttu-id="00d5c-112">Указывает шлюз приложений, с которым этот командлет удаляет зонд.</span><span class="sxs-lookup"><span data-stu-id="00d5c-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="00d5c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00d5c-113">-DefaultProfile</span></span>
<span data-ttu-id="00d5c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="00d5c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00d5c-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="00d5c-115">-Name</span></span>
<span data-ttu-id="00d5c-116">Указывает имя пробной версии, для которого удаляется этот командлет.</span><span class="sxs-lookup"><span data-stu-id="00d5c-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="00d5c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00d5c-117">CommonParameters</span></span>
<span data-ttu-id="00d5c-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="00d5c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00d5c-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00d5c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00d5c-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="00d5c-120">INPUTS</span></span>

### <span data-ttu-id="00d5c-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00d5c-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="00d5c-122">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="00d5c-122">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="00d5c-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="00d5c-123">OUTPUTS</span></span>

### <span data-ttu-id="00d5c-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00d5c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="00d5c-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="00d5c-125">NOTES</span></span>

## <span data-ttu-id="00d5c-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00d5c-126">RELATED LINKS</span></span>

[<span data-ttu-id="00d5c-127">Удаление пробы из существующего шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="00d5c-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="00d5c-128">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00d5c-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="00d5c-129">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00d5c-129">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="00d5c-130">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00d5c-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="00d5c-131">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="00d5c-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()
