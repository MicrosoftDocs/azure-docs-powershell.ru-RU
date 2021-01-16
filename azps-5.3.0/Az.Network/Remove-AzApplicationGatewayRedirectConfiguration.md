---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: fdd461ea2908e59ba824b09a49bed3b6b8f4d38f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507790"
---
# <span data-ttu-id="618bc-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="618bc-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="618bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="618bc-102">SYNOPSIS</span></span>
<span data-ttu-id="618bc-103">Удаляет конфигурацию перенаправления из существующего шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="618bc-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="618bc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="618bc-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="618bc-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="618bc-105">DESCRIPTION</span></span>
<span data-ttu-id="618bc-106">Cmdlet **Remove-AzApplicationGatewayRedirectConfiguration** удаляет конфигурацию перенаправления из существующего шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="618bc-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="618bc-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="618bc-107">EXAMPLES</span></span>

### <span data-ttu-id="618bc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="618bc-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="618bc-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="618bc-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="618bc-110">Вторая команда удаляет конфигурацию перенаправления Redirect01 из шлюза приложения, $AppGw.</span><span class="sxs-lookup"><span data-stu-id="618bc-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="618bc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="618bc-111">PARAMETERS</span></span>

### <span data-ttu-id="618bc-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="618bc-112">-ApplicationGateway</span></span>
<span data-ttu-id="618bc-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="618bc-113">The applicationGateway</span></span>

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

### <span data-ttu-id="618bc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="618bc-114">-DefaultProfile</span></span>
<span data-ttu-id="618bc-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="618bc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="618bc-116">-Name</span><span class="sxs-lookup"><span data-stu-id="618bc-116">-Name</span></span>
<span data-ttu-id="618bc-117">Имя конфигурации перенаправления</span><span class="sxs-lookup"><span data-stu-id="618bc-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="618bc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="618bc-118">CommonParameters</span></span>
<span data-ttu-id="618bc-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="618bc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="618bc-120">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="618bc-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="618bc-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="618bc-121">INPUTS</span></span>

### <span data-ttu-id="618bc-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="618bc-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="618bc-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="618bc-123">OUTPUTS</span></span>

### <span data-ttu-id="618bc-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="618bc-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="618bc-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="618bc-125">NOTES</span></span>

## <span data-ttu-id="618bc-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="618bc-126">RELATED LINKS</span></span>

[<span data-ttu-id="618bc-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="618bc-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="618bc-128">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="618bc-128">Get-AzApplicationGatewayRedirectConfiguration</span></span>](./Get-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="618bc-129">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="618bc-129">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="618bc-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="618bc-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)