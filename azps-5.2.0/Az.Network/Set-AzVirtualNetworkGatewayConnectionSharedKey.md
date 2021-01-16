---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: a35d659de6019d9d9451289716a7acac7e33a8b7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392287"
---
# <span data-ttu-id="49181-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="49181-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="49181-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49181-102">SYNOPSIS</span></span>
<span data-ttu-id="49181-103">Настраивает общий ключ подключения виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="49181-103">Configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="49181-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="49181-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49181-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49181-105">DESCRIPTION</span></span>
<span data-ttu-id="49181-106">Командлет **Set-AzVirtualNetworkGatewayConnectionSharedKey** настраивает общий ключ подключения виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="49181-106">The **Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="49181-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="49181-107">EXAMPLES</span></span>

### <span data-ttu-id="49181-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="49181-108">Example 1</span></span>
```powershell
PS C:\Users\alzam> Set-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName VPNGatewayV3 -Name VNet1toVNet2 -Value abcd1234

Confirm
Are you sure you want to overwrite resource 'VNet1toVNet2'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
abcd1234
```

## <span data-ttu-id="49181-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49181-109">PARAMETERS</span></span>

### <span data-ttu-id="49181-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49181-110">-DefaultProfile</span></span>
<span data-ttu-id="49181-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49181-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49181-112">-Force</span><span class="sxs-lookup"><span data-stu-id="49181-112">-Force</span></span>
<span data-ttu-id="49181-113">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="49181-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="49181-114">-Name</span><span class="sxs-lookup"><span data-stu-id="49181-114">-Name</span></span>
<span data-ttu-id="49181-115">Указывает имя общего ключа виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="49181-115">Specifies the name of the virtual network gateway shared key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49181-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49181-116">-ResourceGroupName</span></span>
<span data-ttu-id="49181-117">Имя группы ресурсов, к которой принадлежит виртуальный сетевой шлюз.</span><span class="sxs-lookup"><span data-stu-id="49181-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="49181-118">-Value</span><span class="sxs-lookup"><span data-stu-id="49181-118">-Value</span></span>
<span data-ttu-id="49181-119">Указывает значение общего ключа.</span><span class="sxs-lookup"><span data-stu-id="49181-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="49181-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49181-120">-Confirm</span></span>
<span data-ttu-id="49181-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49181-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49181-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49181-122">-WhatIf</span></span>
<span data-ttu-id="49181-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49181-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49181-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="49181-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49181-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49181-125">CommonParameters</span></span>
<span data-ttu-id="49181-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49181-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49181-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49181-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49181-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49181-128">INPUTS</span></span>

### <span data-ttu-id="49181-129">System.String</span><span class="sxs-lookup"><span data-stu-id="49181-129">System.String</span></span>

## <span data-ttu-id="49181-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="49181-130">OUTPUTS</span></span>

### <span data-ttu-id="49181-131">System.String</span><span class="sxs-lookup"><span data-stu-id="49181-131">System.String</span></span>

## <span data-ttu-id="49181-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="49181-132">NOTES</span></span>

## <span data-ttu-id="49181-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49181-133">RELATED LINKS</span></span>

[<span data-ttu-id="49181-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="49181-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="49181-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="49181-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)