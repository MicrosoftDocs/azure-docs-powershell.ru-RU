---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: 0d4e1977e0985dbe82731376bd78547ce21251e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567436"
---
# <span data-ttu-id="63635-101">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="63635-101">Set-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="63635-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63635-102">SYNOPSIS</span></span>
<span data-ttu-id="63635-103">Изменение номера SKU для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="63635-103">Modifies the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63635-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63635-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 -Capacity <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63635-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63635-105">DESCRIPTION</span></span>
<span data-ttu-id="63635-106">Командлет **Set-AzureRmApplicationGatewaySku** изменяет единицу складского учета (SKU) для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="63635-106">The **Set-AzureRmApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="63635-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63635-107">EXAMPLES</span></span>

### <span data-ttu-id="63635-108">Пример 1: обновление SKU шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="63635-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="63635-109">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="63635-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="63635-110">Вторая команда обновляет SKU шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="63635-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="63635-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63635-111">PARAMETERS</span></span>

### <span data-ttu-id="63635-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63635-112">-ApplicationGateway</span></span>
<span data-ttu-id="63635-113">Указывает объект шлюза приложения, с которым этот командлет связывает SKU.</span><span class="sxs-lookup"><span data-stu-id="63635-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63635-114">-Capacity</span><span class="sxs-lookup"><span data-stu-id="63635-114">-Capacity</span></span>
<span data-ttu-id="63635-115">Указывает количество экземпляров шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="63635-115">Specifies the instance count of the application gateway.</span></span>

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

### <span data-ttu-id="63635-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63635-116">-DefaultProfile</span></span>
<span data-ttu-id="63635-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63635-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63635-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="63635-118">-Name</span></span>
<span data-ttu-id="63635-119">Указывает имя шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="63635-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="63635-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="63635-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="63635-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="63635-121">Standard_Small</span></span>
- <span data-ttu-id="63635-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="63635-122">Standard_Medium</span></span>
- <span data-ttu-id="63635-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="63635-123">Standard_Large</span></span>
- <span data-ttu-id="63635-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="63635-124">WAF_Medium</span></span>
- <span data-ttu-id="63635-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="63635-125">WAF_Large</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63635-126">Уровень</span><span class="sxs-lookup"><span data-stu-id="63635-126">-Tier</span></span>
<span data-ttu-id="63635-127">Указывает уровень шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="63635-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="63635-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="63635-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="63635-129">Стандартная</span><span class="sxs-lookup"><span data-stu-id="63635-129">Standard</span></span>
- <span data-ttu-id="63635-130">WAF</span><span class="sxs-lookup"><span data-stu-id="63635-130">WAF</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63635-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63635-131">CommonParameters</span></span>
<span data-ttu-id="63635-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63635-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63635-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63635-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63635-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63635-134">INPUTS</span></span>

### <span data-ttu-id="63635-135">System. String</span><span class="sxs-lookup"><span data-stu-id="63635-135">System.String</span></span>

## <span data-ttu-id="63635-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63635-136">OUTPUTS</span></span>

### <span data-ttu-id="63635-137">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="63635-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="63635-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="63635-138">NOTES</span></span>

## <span data-ttu-id="63635-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63635-139">RELATED LINKS</span></span>

[<span data-ttu-id="63635-140">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="63635-140">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="63635-141">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="63635-141">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

