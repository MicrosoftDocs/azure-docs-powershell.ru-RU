---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 3fe3d07a40f81c22fba39aee0db2eb0a2da6e788
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568559"
---
# <span data-ttu-id="2bb69-101">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2bb69-101">Set-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="2bb69-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2bb69-102">SYNOPSIS</span></span>
<span data-ttu-id="2bb69-103">Изменяет конфигурацию сток подключений для серверного объекта параметров HTTP.</span><span class="sxs-lookup"><span data-stu-id="2bb69-103">Modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bb69-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2bb69-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 -Enabled <Boolean> -DrainTimeoutInSec <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bb69-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2bb69-105">DESCRIPTION</span></span>
<span data-ttu-id="2bb69-106">Командлет **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** изменяет конфигурацию сток подключений для серверного объекта параметров HTTP.</span><span class="sxs-lookup"><span data-stu-id="2bb69-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="2bb69-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2bb69-107">EXAMPLES</span></span>

### <span data-ttu-id="2bb69-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2bb69-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Set-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $poolSetting02 -Enabled $False -DrainTimeoutInSec 3600
```

<span data-ttu-id="2bb69-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2bb69-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2bb69-110">Вторая команда получает серверные параметры HTTP с именем Settings01 для $AppGw и сохраняет параметры в переменной $Settings.</span><span class="sxs-lookup"><span data-stu-id="2bb69-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="2bb69-111">Последняя команда изменяет конфигурацию сток подключений для серверного объекта параметров HTTP, сохраненного в $Settings, установив для параметра Enabled значение false и DrainTimeoutInSec на 3600.</span><span class="sxs-lookup"><span data-stu-id="2bb69-111">The last command modifies the connection draining configuration of the back-end HTTP settings object stored in $Settings by setting Enabled to False and DrainTimeoutInSec to 3600.</span></span>

## <span data-ttu-id="2bb69-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2bb69-112">PARAMETERS</span></span>

### <span data-ttu-id="2bb69-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2bb69-113">-BackendHttpSettings</span></span>
<span data-ttu-id="2bb69-114">Параметры внутренних HTTP-данных</span><span class="sxs-lookup"><span data-stu-id="2bb69-114">The backend http settings</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bb69-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bb69-115">-DefaultProfile</span></span>
<span data-ttu-id="2bb69-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2bb69-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bb69-117">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="2bb69-117">-DrainTimeoutInSec</span></span>
<span data-ttu-id="2bb69-118">Число секунд, в течение которого сток подключений является активным.</span><span class="sxs-lookup"><span data-stu-id="2bb69-118">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="2bb69-119">Допустимые значения: от 1 секунды до 3600 секунд.</span><span class="sxs-lookup"><span data-stu-id="2bb69-119">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bb69-120">-Включено</span><span class="sxs-lookup"><span data-stu-id="2bb69-120">-Enabled</span></span>
<span data-ttu-id="2bb69-121">Включена ли сток подключений.</span><span class="sxs-lookup"><span data-stu-id="2bb69-121">Whether connection draining is enabled or not.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bb69-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bb69-122">CommonParameters</span></span>
<span data-ttu-id="2bb69-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2bb69-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bb69-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bb69-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bb69-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2bb69-125">INPUTS</span></span>

### <span data-ttu-id="2bb69-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2bb69-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="2bb69-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2bb69-127">OUTPUTS</span></span>

### <span data-ttu-id="2bb69-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2bb69-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="2bb69-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="2bb69-129">NOTES</span></span>

## <span data-ttu-id="2bb69-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2bb69-130">RELATED LINKS</span></span>

[<span data-ttu-id="2bb69-131">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2bb69-131">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="2bb69-132">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2bb69-132">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="2bb69-133">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2bb69-133">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="2bb69-134">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2bb69-134">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="2bb69-135">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2bb69-135">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)
