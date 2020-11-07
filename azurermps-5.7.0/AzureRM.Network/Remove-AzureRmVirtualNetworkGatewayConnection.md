---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 73bb12aebbe4f67c1aba4526f6ed656e5b6feb09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568238"
---
# <span data-ttu-id="8de83-101">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8de83-101">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="8de83-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8de83-102">SYNOPSIS</span></span>
<span data-ttu-id="8de83-103">Удаление подключения к шлюзу виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="8de83-103">Deletes a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8de83-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8de83-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8de83-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8de83-105">DESCRIPTION</span></span>
<span data-ttu-id="8de83-106">Подключение к шлюзу виртуальной сети является объектом, представляющим туннель IPsec ("сайт-сайт" или "Виртуальная сеть-сеть"), подключенного к шлюзу виртуальной сети в Azure.</span><span class="sxs-lookup"><span data-stu-id="8de83-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="8de83-107">Командлет **Remove-AzureRmVirtualNetworkGatewayConnection** удаляет объект подключения на основе имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8de83-107">The **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="8de83-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8de83-108">EXAMPLES</span></span>

### <span data-ttu-id="8de83-109">1: Удаление подключения к шлюзу виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="8de83-109">1: Delete a Virtual Network Gateway Connection</span></span>
```
Remove-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="8de83-110">Удаляет объект подключения к шлюзу виртуальной сети с именем "myTunnel" в группе ресурсов "myRG"</span><span class="sxs-lookup"><span data-stu-id="8de83-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="8de83-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8de83-111">PARAMETERS</span></span>

### <span data-ttu-id="8de83-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8de83-112">-DefaultProfile</span></span>
<span data-ttu-id="8de83-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8de83-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8de83-114">-Force</span><span class="sxs-lookup"><span data-stu-id="8de83-114">-Force</span></span>
<span data-ttu-id="8de83-115">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8de83-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8de83-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8de83-116">-Name</span></span>
<span data-ttu-id="8de83-117">Указывает имя подключения к шлюзу виртуальной сети, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="8de83-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8de83-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8de83-118">-PassThru</span></span>
<span data-ttu-id="8de83-119">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="8de83-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8de83-120">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8de83-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8de83-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8de83-121">-ResourceGroupName</span></span>
<span data-ttu-id="8de83-122">Указывает имя группы ресурсов, которая содержит подключение к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8de83-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8de83-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8de83-123">-Confirm</span></span>
<span data-ttu-id="8de83-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8de83-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8de83-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8de83-125">-WhatIf</span></span>
<span data-ttu-id="8de83-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8de83-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8de83-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8de83-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8de83-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8de83-128">CommonParameters</span></span>
<span data-ttu-id="8de83-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8de83-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8de83-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8de83-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8de83-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8de83-131">INPUTS</span></span>

### <span data-ttu-id="8de83-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="8de83-132">None</span></span>
<span data-ttu-id="8de83-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="8de83-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8de83-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8de83-134">OUTPUTS</span></span>

## <span data-ttu-id="8de83-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="8de83-135">NOTES</span></span>

## <span data-ttu-id="8de83-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8de83-136">RELATED LINKS</span></span>

[<span data-ttu-id="8de83-137">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8de83-137">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="8de83-138">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8de83-138">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="8de83-139">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8de83-139">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)

