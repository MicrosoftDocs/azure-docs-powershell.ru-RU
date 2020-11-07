---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: 37cd1f7b00cbfae6421b5dab06ce87c0f462434c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721033"
---
# <span data-ttu-id="a23df-101">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a23df-101">Get-AzDnsRecordSet</span></span>

## <span data-ttu-id="a23df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a23df-102">SYNOPSIS</span></span>
<span data-ttu-id="a23df-103">Получает набор записей DNS.</span><span class="sxs-lookup"><span data-stu-id="a23df-103">Gets a DNS record set.</span></span>

## <span data-ttu-id="a23df-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a23df-104">SYNTAX</span></span>

### <span data-ttu-id="a23df-105">»</span><span class="sxs-lookup"><span data-stu-id="a23df-105">Fields</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a23df-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="a23df-106">Object</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a23df-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a23df-107">DESCRIPTION</span></span>
<span data-ttu-id="a23df-108">Командлет **Get-AzDnsRecordSet** получает набор записей DNS (Domain Name System) с указанными именем и типом в указанной зоне.</span><span class="sxs-lookup"><span data-stu-id="a23df-108">The **Get-AzDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>
<span data-ttu-id="a23df-109">Если не указать параметры *Name* или *RecordType* , этот командлет возвращает все наборы записей указанного типа в зоне.</span><span class="sxs-lookup"><span data-stu-id="a23df-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="a23df-110">Если указать параметр *RecordType* , но не параметр *Name* , этот командлет возвращает все наборы записей с указанным типом записи.</span><span class="sxs-lookup"><span data-stu-id="a23df-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>
<span data-ttu-id="a23df-111">Вы можете использовать оператор конвейера для передачи объекта **dnsZone** в этот командлет или передавать объект **dnsZone** в качестве параметра *зоны* или можно указать зону и группу ресурсов по имени.</span><span class="sxs-lookup"><span data-stu-id="a23df-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="a23df-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a23df-112">EXAMPLES</span></span>

### <span data-ttu-id="a23df-113">Пример 1: получение наборов записей с указанным именем и типом</span><span class="sxs-lookup"><span data-stu-id="a23df-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="a23df-114">Эта команда получает набор записей с именем www в заданной группе ресурсов и зоне, а затем сохраняет его в переменной $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="a23df-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="a23df-115">Так как указаны параметры *Name* и *RecordType* , возвращается только один объект **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="a23df-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="a23df-116">Пример 2: получение наборов записей указанного типа</span><span class="sxs-lookup"><span data-stu-id="a23df-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="a23df-117">Эта команда получает массив всех наборов записей типа A в зоне с именем myzone.com в группе ресурсов с именем MyResourceGroup и сохраняет их в переменной $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="a23df-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="a23df-118">Пример 3: получение всех наборов записей в зоне</span><span class="sxs-lookup"><span data-stu-id="a23df-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="a23df-119">Эта команда получает массив всех наборов записей в зоне с именем myzone.com в группе ресурсов с именем MyResourceGroup, а затем сохраняет их в переменной $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="a23df-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="a23df-120">Пример 4: получение всех наборов записей в зоне с помощью объекта DnsZone</span><span class="sxs-lookup"><span data-stu-id="a23df-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

<span data-ttu-id="a23df-121">Этот пример эквивалентен примеру 3 выше.</span><span class="sxs-lookup"><span data-stu-id="a23df-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="a23df-122">На этот раз зона задается с помощью объекта Zone.</span><span class="sxs-lookup"><span data-stu-id="a23df-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="a23df-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a23df-123">PARAMETERS</span></span>

### <span data-ttu-id="a23df-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a23df-124">-DefaultProfile</span></span>
<span data-ttu-id="a23df-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a23df-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a23df-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a23df-126">-Name</span></span>
<span data-ttu-id="a23df-127">Указывает имя **набора записей** для получения.</span><span class="sxs-lookup"><span data-stu-id="a23df-127">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="a23df-128">Если параметр *Name* не указан, возвращаются все наборы записей указанного типа.</span><span class="sxs-lookup"><span data-stu-id="a23df-128">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a23df-129">-RecordType</span><span class="sxs-lookup"><span data-stu-id="a23df-129">-RecordType</span></span>
<span data-ttu-id="a23df-130">Указывает тип DNS-записи, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a23df-130">Specifies the type of DNS record that this cmdlet gets.</span></span>
<span data-ttu-id="a23df-131">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="a23df-131">Valid values are:</span></span> 
- <span data-ttu-id="a23df-132">Помощью</span><span class="sxs-lookup"><span data-stu-id="a23df-132">A</span></span>
- <span data-ttu-id="a23df-133">AAAA</span><span class="sxs-lookup"><span data-stu-id="a23df-133">AAAA</span></span>
- <span data-ttu-id="a23df-134">CNAME</span><span class="sxs-lookup"><span data-stu-id="a23df-134">CNAME</span></span>
- <span data-ttu-id="a23df-135">МХ</span><span class="sxs-lookup"><span data-stu-id="a23df-135">MX</span></span>
- <span data-ttu-id="a23df-136">СЛУЖБУ</span><span class="sxs-lookup"><span data-stu-id="a23df-136">NS</span></span>
- <span data-ttu-id="a23df-137">УКАЗАТЕЛЯ</span><span class="sxs-lookup"><span data-stu-id="a23df-137">PTR</span></span>
- <span data-ttu-id="a23df-138">ЗОНЫ</span><span class="sxs-lookup"><span data-stu-id="a23df-138">SOA</span></span>
- <span data-ttu-id="a23df-139">МОГЛА</span><span class="sxs-lookup"><span data-stu-id="a23df-139">SRV</span></span>
- <span data-ttu-id="a23df-140">TXT если параметр *RecordType* не указан, необходимо также опустить параметр *Name* .</span><span class="sxs-lookup"><span data-stu-id="a23df-140">TXT If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="a23df-141">Затем этот командлет возвращает все наборы записей в зоне (для всех имен и типов).</span><span class="sxs-lookup"><span data-stu-id="a23df-141">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.RecordType]
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a23df-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a23df-142">-ResourceGroupName</span></span>
<span data-ttu-id="a23df-143">Указывает группу ресурсов, которая содержит зону DNS.</span><span class="sxs-lookup"><span data-stu-id="a23df-143">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="a23df-144">Имя зоны также должно быть указано с помощью параметра *zonename* .</span><span class="sxs-lookup"><span data-stu-id="a23df-144">The zone name must also be specified, using the *ZoneName* parameter.</span></span>
<span data-ttu-id="a23df-145">Кроме того, вы можете указать зону и группу ресурсов, передав объект **dnsZone** с помощью параметра *Zone* .</span><span class="sxs-lookup"><span data-stu-id="a23df-145">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a23df-146">-Zone</span><span class="sxs-lookup"><span data-stu-id="a23df-146">-Zone</span></span>
<span data-ttu-id="a23df-147">Указывает зону DNS, которая содержит набор записей, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a23df-147">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="a23df-148">Кроме того, вы можете указать зону с помощью параметров *zonename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="a23df-148">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a23df-149">-ИмяЗоны</span><span class="sxs-lookup"><span data-stu-id="a23df-149">-ZoneName</span></span>
<span data-ttu-id="a23df-150">Указывает имя зоны DNS, которая содержит набор записей, для которого требуется получить доступ.</span><span class="sxs-lookup"><span data-stu-id="a23df-150">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="a23df-151">Группа ресурсов, содержащая зону, также должна быть указана с помощью параметра *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="a23df-151">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="a23df-152">Кроме того, вы можете указать зону и группу ресурсов, передав объект зоны DNS с помощью параметра *Zone* .</span><span class="sxs-lookup"><span data-stu-id="a23df-152">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a23df-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a23df-153">CommonParameters</span></span>
<span data-ttu-id="a23df-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a23df-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a23df-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a23df-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a23df-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a23df-156">INPUTS</span></span>

### <span data-ttu-id="a23df-157">System. String</span><span class="sxs-lookup"><span data-stu-id="a23df-157">System.String</span></span>

### <span data-ttu-id="a23df-158">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="a23df-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="a23df-159">System. Nullable "1 [[Microsoft. Azure. Management. DNS. Models. RecordType, Microsoft. Azure. Management. DNS, Version = 3.0.0.0, культура = нейтральная, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a23df-159">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="a23df-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a23df-160">OUTPUTS</span></span>

### <span data-ttu-id="a23df-161">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a23df-161">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="a23df-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="a23df-162">NOTES</span></span>

## <span data-ttu-id="a23df-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a23df-163">RELATED LINKS</span></span>

[<span data-ttu-id="a23df-164">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a23df-164">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="a23df-165">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a23df-165">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="a23df-166">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a23df-166">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)

