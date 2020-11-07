---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordSet.md
ms.openlocfilehash: e009eea8276bbfe9653c506864604ca955a6367f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559823"
---
# <span data-ttu-id="4e494-101">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4e494-101">Remove-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="4e494-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e494-102">SYNOPSIS</span></span>
<span data-ttu-id="4e494-103">Удаляет набор записей.</span><span class="sxs-lookup"><span data-stu-id="4e494-103">Deletes a record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e494-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e494-104">SYNTAX</span></span>

### <span data-ttu-id="4e494-105">»</span><span class="sxs-lookup"><span data-stu-id="4e494-105">Fields</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String>
 -ResourceGroupName <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e494-106">Смешивания</span><span class="sxs-lookup"><span data-stu-id="4e494-106">Mixed</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e494-107">DataObject</span><span class="sxs-lookup"><span data-stu-id="4e494-107">Object</span></span>
```
Remove-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e494-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e494-108">DESCRIPTION</span></span>
<span data-ttu-id="4e494-109">Командлет **Remove-AzureRmDnsRecordSet** удаляет набор записей из указанной зоны.</span><span class="sxs-lookup"><span data-stu-id="4e494-109">The **Remove-AzureRmDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="4e494-110">Вы не можете удалить записи SOA или сервера имен (NS), которые будут автоматически созданы на зоне Апекс.</span><span class="sxs-lookup"><span data-stu-id="4e494-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>

<span data-ttu-id="4e494-111">Вы можете передать в этот командлет объект **набора записей** с помощью оператора конвейера или в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="4e494-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="4e494-112">Чтобы определить набор записей по имени и типу, не используя объект **Recordset** , необходимо передать зону как объект **dnsZone** с помощью оператора конвейера или в качестве параметра либо можно указать параметры *zonename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="4e494-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="4e494-113">Вы можете использовать параметр Confirm и $ConfirmPreference переменной Windows PowerShell, чтобы указать, нужно ли командлету запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4e494-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="4e494-114">При указании набора записей с помощью объекта **Recordset** набор записей не удаляется, если он был изменен в Azure DNS, так как был получен объект локального **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="4e494-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="4e494-115">Это обеспечивает защиту для параллельных изменений.</span><span class="sxs-lookup"><span data-stu-id="4e494-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="4e494-116">Вы можете отключить этот параметр с помощью параметра *overwrite* , который удаляет набор записей независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="4e494-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="4e494-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e494-117">EXAMPLES</span></span>

### <span data-ttu-id="4e494-118">Пример 1: удаление набор записей</span><span class="sxs-lookup"><span data-stu-id="4e494-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="4e494-119">Первая команда получает указанный наборы записей и сохраняет ее в переменной $RecordSet. Вторая команда удаляет запись, указанную в $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="4e494-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="4e494-120">Пример 2: удаление набор записей и отключение всех подтверждений</span><span class="sxs-lookup"><span data-stu-id="4e494-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="4e494-121">Первая команда получает указанный наборы записей.</span><span class="sxs-lookup"><span data-stu-id="4e494-121">The first command gets the specified record set.</span></span>

<span data-ttu-id="4e494-122">Вторая команда удаляет наборы записей, даже если она была изменена.</span><span class="sxs-lookup"><span data-stu-id="4e494-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="4e494-123">Запросы на подтверждение подавляются.</span><span class="sxs-lookup"><span data-stu-id="4e494-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="4e494-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e494-124">PARAMETERS</span></span>

### <span data-ttu-id="4e494-125">-Force</span><span class="sxs-lookup"><span data-stu-id="4e494-125">-Force</span></span>
<span data-ttu-id="4e494-126">Этот параметр устарел для этого командлета.</span><span class="sxs-lookup"><span data-stu-id="4e494-126">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="4e494-127">Оно будет удалено в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="4e494-127">It will be removed in a future release.</span></span>

<span data-ttu-id="4e494-128">Чтобы указать, будет ли этот командлет запрашивать подтверждение, используйте параметр *Confirm* .</span><span class="sxs-lookup"><span data-stu-id="4e494-128">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="4e494-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e494-129">-Name</span></span>
<span data-ttu-id="4e494-130">Указывает имя **набора записей** , который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="4e494-130">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="4e494-131">Когда вы указываете набор записей по имени, зона DNS должна быть указана с помощью параметра *Zone* или параметров *zonename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="4e494-131">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="4e494-132">Кроме того, набор записей можно указать с помощью объекта **Recordset** , передаваемого с помощью параметра *Recordset* .</span><span class="sxs-lookup"><span data-stu-id="4e494-132">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e494-133">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="4e494-133">-Overwrite</span></span>
<span data-ttu-id="4e494-134">При указании набора записей с помощью объекта **Recordset** набор записей не удаляется, если он был изменен в Azure DNS, так как был получен объект локального **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="4e494-134">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="4e494-135">Это обеспечивает защиту для параллельных изменений.</span><span class="sxs-lookup"><span data-stu-id="4e494-135">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="4e494-136">Это может быть подавлено с помощью параметра *overwrite* , который удаляет набор записей независимо от текущих изменений.</span><span class="sxs-lookup"><span data-stu-id="4e494-136">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e494-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e494-137">-PassThru</span></span>
<span data-ttu-id="4e494-138">PassThru</span><span class="sxs-lookup"><span data-stu-id="4e494-138">passthru</span></span>

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

### <span data-ttu-id="4e494-139">-Набор записей</span><span class="sxs-lookup"><span data-stu-id="4e494-139">-RecordSet</span></span>
<span data-ttu-id="4e494-140">Указывает объект **набора записей** , который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="4e494-140">Specifies the **RecordSet** object to remove.</span></span>

<span data-ttu-id="4e494-141">Кроме того, можно задать набор записей с помощью параметров *имени* и *зоны* либо с помощью параметров *Name* , *имя_зоны* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="4e494-141">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e494-142">-RecordType</span><span class="sxs-lookup"><span data-stu-id="4e494-142">-RecordType</span></span>
<span data-ttu-id="4e494-143">Указывает тип DNS-записи.</span><span class="sxs-lookup"><span data-stu-id="4e494-143">Specifies the type of DNS record.</span></span>

<span data-ttu-id="4e494-144">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="4e494-144">Valid values are:</span></span>

- <span data-ttu-id="4e494-145">Помощью</span><span class="sxs-lookup"><span data-stu-id="4e494-145">A</span></span>
- <span data-ttu-id="4e494-146">AAAA</span><span class="sxs-lookup"><span data-stu-id="4e494-146">AAAA</span></span>
- <span data-ttu-id="4e494-147">CNAME</span><span class="sxs-lookup"><span data-stu-id="4e494-147">CNAME</span></span>
- <span data-ttu-id="4e494-148">МХ</span><span class="sxs-lookup"><span data-stu-id="4e494-148">MX</span></span>
- <span data-ttu-id="4e494-149">СЛУЖБУ</span><span class="sxs-lookup"><span data-stu-id="4e494-149">NS</span></span>
- <span data-ttu-id="4e494-150">УКАЗАТЕЛЯ</span><span class="sxs-lookup"><span data-stu-id="4e494-150">PTR</span></span>
- <span data-ttu-id="4e494-151">МОГЛА</span><span class="sxs-lookup"><span data-stu-id="4e494-151">SRV</span></span>
- <span data-ttu-id="4e494-152">ТХТ</span><span class="sxs-lookup"><span data-stu-id="4e494-152">TXT</span></span>

<span data-ttu-id="4e494-153">Записи SOA удаляются автоматически при удалении зоны.</span><span class="sxs-lookup"><span data-stu-id="4e494-153">SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="4e494-154">Записи SOA нельзя удалять вручную.</span><span class="sxs-lookup"><span data-stu-id="4e494-154">You cannot manually delete SOA records.</span></span>

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e494-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e494-155">-ResourceGroupName</span></span>
<span data-ttu-id="4e494-156">Указывает группу ресурсов, которая содержит DNS-зону, которая содержит **набор записей** для удаления.</span><span class="sxs-lookup"><span data-stu-id="4e494-156">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="4e494-157">Этот параметр применяется только в том случае, если набор записей и зона DNS указаны с использованием параметров *Name* и *zonename* .</span><span class="sxs-lookup"><span data-stu-id="4e494-157">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>

<span data-ttu-id="4e494-158">Кроме того, вы можете задать набор записей с помощью параметра " *набор записей* " или параметров " *имя* " и " *зона* ".</span><span class="sxs-lookup"><span data-stu-id="4e494-158">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="4e494-159">-Zone</span><span class="sxs-lookup"><span data-stu-id="4e494-159">-Zone</span></span>
<span data-ttu-id="4e494-160">Указывает DNS-зону, которая содержит **набор записей** для удаления.</span><span class="sxs-lookup"><span data-stu-id="4e494-160">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="4e494-161">Этот параметр применяется только при указании заданной записи с помощью параметра *Name* .</span><span class="sxs-lookup"><span data-stu-id="4e494-161">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>

<span data-ttu-id="4e494-162">Кроме того, вы можете задать набор записей с помощью параметра " *набор записей* " или параметров *Name* , *имя_зоны* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="4e494-162">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e494-163">-ИмяЗоны</span><span class="sxs-lookup"><span data-stu-id="4e494-163">-ZoneName</span></span>
<span data-ttu-id="4e494-164">Указывает имя зоны, содержащей **набор записей** для удаления.</span><span class="sxs-lookup"><span data-stu-id="4e494-164">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="4e494-165">Кроме того, необходимо указать параметры *Name* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="4e494-165">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="4e494-166">Кроме того, можно задать набор записей с помощью параметра " *набор записей* ", а также параметров *имени* и *зоны* .</span><span class="sxs-lookup"><span data-stu-id="4e494-166">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="4e494-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e494-167">-Confirm</span></span>
<span data-ttu-id="4e494-168">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4e494-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e494-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e494-169">-WhatIf</span></span>
<span data-ttu-id="4e494-170">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4e494-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e494-171">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4e494-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e494-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e494-172">-DefaultProfile</span></span>
<span data-ttu-id="4e494-173">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e494-173">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e494-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e494-174">CommonParameters</span></span>
<span data-ttu-id="4e494-175">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e494-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e494-176">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e494-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e494-177">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e494-177">INPUTS</span></span>

### <span data-ttu-id="4e494-178">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4e494-178">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="4e494-179">Вы можете передать в этот командлет объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="4e494-179">You can pipe a **RecordSet** object to this cmdlet.</span></span>

## <span data-ttu-id="4e494-180">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e494-180">OUTPUTS</span></span>

### <span data-ttu-id="4e494-181">Ничего</span><span class="sxs-lookup"><span data-stu-id="4e494-181">None</span></span>
<span data-ttu-id="4e494-182">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="4e494-182">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="4e494-183">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e494-183">NOTES</span></span>
<span data-ttu-id="4e494-184">Вы можете использовать параметр *Confirm* , чтобы указать, будет ли этот командлет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4e494-184">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="4e494-185">По умолчанию командлет запрашивает подтверждение, если значение переменной $ConfirmPreference Windows PowerShell — средний или ниже.</span><span class="sxs-lookup"><span data-stu-id="4e494-185">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="4e494-186">Если вы задаете параметр *Confirm* или *Confirm: $true* , этот командлет запрашивает подтверждение перед запуском.</span><span class="sxs-lookup"><span data-stu-id="4e494-186">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="4e494-187">Если вы задаете значение *Confirm: $false* , командлет не будет запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="4e494-187">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="4e494-188">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e494-188">RELATED LINKS</span></span>

[<span data-ttu-id="4e494-189">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4e494-189">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="4e494-190">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4e494-190">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="4e494-191">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="4e494-191">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)