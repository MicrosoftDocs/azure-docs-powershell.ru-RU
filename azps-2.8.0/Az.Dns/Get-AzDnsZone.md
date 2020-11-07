---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: 9be5ca678b690400e044b9627fd455ea2cbc29c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721030"
---
# <span data-ttu-id="7178b-101">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="7178b-101">Get-AzDnsZone</span></span>

## <span data-ttu-id="7178b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7178b-102">SYNOPSIS</span></span>
<span data-ttu-id="7178b-103">Возвращает зону DNS.</span><span class="sxs-lookup"><span data-stu-id="7178b-103">Gets a DNS zone.</span></span>

## <span data-ttu-id="7178b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7178b-104">SYNTAX</span></span>

### <span data-ttu-id="7178b-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7178b-105">Default (Default)</span></span>
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7178b-106">Группа</span><span class="sxs-lookup"><span data-stu-id="7178b-106">ResourceGroup</span></span>
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7178b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7178b-107">DESCRIPTION</span></span>
<span data-ttu-id="7178b-108">Командлет **Get-AzDnsZone** получает DNS-зону из заданной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7178b-108">The **Get-AzDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="7178b-109">Если указан параметр *Name* , возвращается один объект **dnsZone** .</span><span class="sxs-lookup"><span data-stu-id="7178b-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="7178b-110">Если параметр *Name* не указан, возвращается массив, содержащий все зоны в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7178b-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="7178b-111">Вы можете использовать объект **dnsZone** , чтобы обновить зону, например добавить в нее объекты **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="7178b-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="7178b-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7178b-112">EXAMPLES</span></span>

### <span data-ttu-id="7178b-113">Пример 1: получение зоны</span><span class="sxs-lookup"><span data-stu-id="7178b-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="7178b-114">В этом примере возвращается зона DNS с именем myzone.com из указанной группы ресурсов, а затем она сохраняется в переменной $Zone.</span><span class="sxs-lookup"><span data-stu-id="7178b-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="7178b-115">Пример 2: получение всех зон в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="7178b-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="7178b-116">В этом примере выполняется получение всех зон DNS в указанной группе ресурсов и их сохранение в переменной $Zones.</span><span class="sxs-lookup"><span data-stu-id="7178b-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="7178b-117">Пример 3: получение всех зон в подписке</span><span class="sxs-lookup"><span data-stu-id="7178b-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzDnsZone
```

<span data-ttu-id="7178b-118">В этом примере выполняется получение всех зон DNS в текущей подписке Azure и их сохранение в переменной $Zones.</span><span class="sxs-lookup"><span data-stu-id="7178b-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="7178b-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7178b-119">PARAMETERS</span></span>

### <span data-ttu-id="7178b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7178b-120">-DefaultProfile</span></span>
<span data-ttu-id="7178b-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7178b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7178b-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7178b-122">-Name</span></span>
<span data-ttu-id="7178b-123">Указывает имя зоны DNS, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="7178b-123">Specifies the name of the DNS zone to get.</span></span>
<span data-ttu-id="7178b-124">Если вы не укажете значение параметра *Name* , этот командлет получает все зоны DNS в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7178b-124">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="7178b-125">Если параметр *ResourceGroupName* также опущен, этот командлет получает все зоны DNS в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="7178b-125">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7178b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7178b-126">-ResourceGroupName</span></span>
<span data-ttu-id="7178b-127">Указывает имя группы ресурсов, содержащей зону DNS, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="7178b-127">Specifies the name of the resource group that contains the DNS zone to get.</span></span>
<span data-ttu-id="7178b-128">Если *ResourceGroupName* не указан, необходимо также опустить параметр *Name* .</span><span class="sxs-lookup"><span data-stu-id="7178b-128">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="7178b-129">В этом случае этот командлет получает все зоны DNS в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="7178b-129">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7178b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7178b-130">CommonParameters</span></span>
<span data-ttu-id="7178b-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7178b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7178b-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7178b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7178b-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7178b-133">INPUTS</span></span>

### <span data-ttu-id="7178b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7178b-134">System.String</span></span>

## <span data-ttu-id="7178b-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7178b-135">OUTPUTS</span></span>

### <span data-ttu-id="7178b-136">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="7178b-136">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="7178b-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="7178b-137">NOTES</span></span>

## <span data-ttu-id="7178b-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7178b-138">RELATED LINKS</span></span>

[<span data-ttu-id="7178b-139">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="7178b-139">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="7178b-140">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="7178b-140">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

[<span data-ttu-id="7178b-141">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="7178b-141">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)