---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4F487FCA-930D-4D56-8D28-7693312E1A01
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteTable.md
ms.openlocfilehash: 711d9848188cbdbaaeac9313680fd9fd70cb1f34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560295"
---
# <span data-ttu-id="c26b4-101">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="c26b4-101">Get-AzureRmRouteTable</span></span>

## <span data-ttu-id="c26b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c26b4-102">SYNOPSIS</span></span>
<span data-ttu-id="c26b4-103">Возвращает таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="c26b4-103">Gets route tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c26b4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c26b4-104">SYNTAX</span></span>

### <span data-ttu-id="c26b4-105">Кройте</span><span class="sxs-lookup"><span data-stu-id="c26b4-105">Expand</span></span>
```
Get-AzureRmRouteTable -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c26b4-106">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="c26b4-106">NoExpand</span></span>
```
Get-AzureRmRouteTable [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c26b4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c26b4-107">DESCRIPTION</span></span>
<span data-ttu-id="c26b4-108">Командлет **Get-AzureRmRouteTable** получает таблицы маршрутов Azure.</span><span class="sxs-lookup"><span data-stu-id="c26b4-108">The **Get-AzureRmRouteTable** cmdlet gets Azure route tables.</span></span>
<span data-ttu-id="c26b4-109">Вы можете получить одну таблицу маршрутов или получить все таблицы маршрутов в группе ресурсов или в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="c26b4-109">You can get a single route table, or get all the route tables in a resource group or in your subscription.</span></span>

## <span data-ttu-id="c26b4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c26b4-110">EXAMPLES</span></span>

### <span data-ttu-id="c26b4-111">Пример 1: получение таблицы маршрутов</span><span class="sxs-lookup"><span data-stu-id="c26b4-111">Example 1: Get a route table</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"db5f4e12-3f34-465b-92dd-0ab3bf6fc274"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"db5f4e12-3f34-465b-92dd-0ab3bf6fc274\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="c26b4-112">Эта команда получает таблицу маршрутов с именем RouteTable01 в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c26b4-112">This command gets the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="c26b4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c26b4-113">PARAMETERS</span></span>

### <span data-ttu-id="c26b4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c26b4-114">-DefaultProfile</span></span>
<span data-ttu-id="c26b4-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c26b4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c26b4-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="c26b4-116">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c26b4-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c26b4-117">-Name</span></span>
<span data-ttu-id="c26b4-118">Указывает имя таблицы маршрутов, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c26b4-118">Specifies the name of the route table that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c26b4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c26b4-119">-ResourceGroupName</span></span>
<span data-ttu-id="c26b4-120">Указывает имя группы ресурсов, содержащей таблицы маршрутов, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c26b4-120">Specifies the name of the resource group that contains the route tables that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c26b4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c26b4-121">CommonParameters</span></span>
<span data-ttu-id="c26b4-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c26b4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c26b4-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c26b4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c26b4-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c26b4-124">INPUTS</span></span>

### <span data-ttu-id="c26b4-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="c26b4-125">None</span></span>
<span data-ttu-id="c26b4-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c26b4-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c26b4-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c26b4-127">OUTPUTS</span></span>

### <span data-ttu-id="c26b4-128">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="c26b4-128">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="c26b4-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="c26b4-129">NOTES</span></span>

## <span data-ttu-id="c26b4-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c26b4-130">RELATED LINKS</span></span>

[<span data-ttu-id="c26b4-131">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="c26b4-131">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="c26b4-132">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="c26b4-132">Remove-AzureRmRouteTable</span></span>](./Remove-AzureRmRouteTable.md)

[<span data-ttu-id="c26b4-133">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="c26b4-133">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)

