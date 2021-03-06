---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
ms.openlocfilehash: e00b31783554b8ea70760809c36f23a6a62575ca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911231"
---
# Remove-AzDnsRecordConfig

## КРАТКИй обзор
Удаление записи DNS из локального объекта Set Record.

## Максимальное

### Помощью
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### AAAA
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### СЛУЖБУ
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### МХ
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### УКАЗАТЕЛЯ
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### ТХТ
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### МОГЛА
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### CNAME
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Remove-AzDnsRecordConfig** УДАЛЯЕТ запись DNS (Domain Name System) из множества записей.
Объект **Recordset** является автономным объектом, и изменения в нем не изменяют ответы DNS, пока не будет запущен командлет Set-AzDnsRecordSet, чтобы сохранить изменения в службе Microsoft Azure DNS.

Для удаления записи все поля для этого типа записей должны точно совпадать.
Вы не можете добавлять и удалять записи SOA.
Записи SOA автоматически создаются при создании зоны DNS и автоматически удаляются при удалении зоны DNS.

Вы можете передать объект **набора записей** в этот командлет как параметр или с помощью оператора конвейера.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Удаление записи A из множества записей
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

В этом примере удаляется запись A из существующего набор записей.
Если это единственная запись в наборе записей, результатом будет пустой набор записей.
Чтобы полностью удалить набор записей, ознакомьтесь со сведениями в разделе Remove-AzDnsRecordSet.

### Пример 2: Удаление записи AAAA из набор записей
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

В этом примере удаляется запись AAAA из существующего множества записей.
Если это единственная запись в наборе записей, результатом будет пустой набор записей.
Чтобы полностью удалить набор записей, ознакомьтесь со сведениями в разделе Remove-AzDnsRecordSet.

### Пример 3: Удаление записи CNAME из набор записей
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

В этом примере запись CNAME удаляется из существующего набор записей.
Так как набор записей CNAME может содержать не более одной записи, результатом будет пустой набор записей.

### Пример 4: Удаление записи MX из набор записей
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

В этом примере удаляется запись MX из существующего множества записей.
Имя записи "@" обозначает набор записей на Апексе зоны.
Если это единственная запись в наборе записей, результатом будет пустой набор записей.
Чтобы полностью удалить набор записей, ознакомьтесь со сведениями в разделе Remove-AzDnsRecordSet.

### Пример 5: Удаление записи NS из множества записей
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzDnsRecordSet
```

В этом примере удаляется запись NS из существующего множества записей.
Если это единственная запись в наборе записей, результатом будет пустой набор записей.
Чтобы полностью удалить набор записей, ознакомьтесь со сведениями в разделе Remove-AzDnsRecordSet.

### Пример 6: Удаление записи PTR из набор записей
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

В этом примере удаляется запись PTR из существующего множества записей.
Если это единственная запись в наборе записей, результатом будет пустой набор записей.
Чтобы полностью удалить набор записей, ознакомьтесь со сведениями в разделе Remove-AzDnsRecordSet.

### Пример 7: Удаление записи SRV из набор записей
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

В этом примере удаляется запись SRV из существующего множества записей.
Если это единственная запись в наборе записей, результатом будет пустой набор записей.
Чтобы полностью удалить набор записей, ознакомьтесь со сведениями в разделе Remove-AzDnsRecordSet.

### Пример 8: Удаление записи TXT из множества записей
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Value "This is a TXT Record"  | Set-AzDnsRecordSet
```

В этом примере запись TXT удаляется из существующего набор записей.
Если это единственная запись в наборе записей, результатом будет пустой набор записей.
Чтобы полностью удалить набор записей, ознакомьтесь со сведениями в разделе Remove-AzDnsRecordSet.

## ПАРАМЕТРЫ

### -CNAME
Задает доменное имя для записи канонического имени (CNAME).

```yaml
Type: String
Parameter Sets: CNAME
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Exchange
Указывает имя почтового сервера для записи почтового обменника (MX).

```yaml
Type: String
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ipv4Address
Задает IPv4-адрес для записи A.

```yaml
Type: String
Parameter Sets: A
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ipv6Address
Задает IPv6-адрес для записи AAAA.

```yaml
Type: String
Parameter Sets: AAAA
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nsdname
Указывает сервер доменных имен для записи сервера доменных имен (NS).

```yaml
Type: String
Parameter Sets: NS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Port (порт)
Указывает порт для записи службы (SRV).

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Предпочтения
Задает приоритет MX-записи.

```yaml
Type: UInt16
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Priority (приоритет)
Указывает приоритет записи SRV.

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ptrdname
Указывает целевое доменное имя записи указателя (PTR).

```yaml
Type: String
Parameter Sets: PTR
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Набор записей
Указывает объект **набора записей** , содержащий удаляемую запись.

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Target
Указывает целевой объект для записи SRV.

```yaml
Type: String
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Value (значение)
Задает значение для записи TXT.

```yaml
Type: String
Parameter Sets: TXT
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Weight
Определяет вес записи SRV.

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Вы можете передать на этот командлет объект **DnsRecordSet** .
Это автономное представление набора записей и его обновления не изменяют ответы DNS, пока не будет запущен параметр SET-AzDnsRecordSet.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Этот командлет возвращает измененный объект **набора записей** .

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzDnsRecordConfig](./Add-AzDnsRecordConfig.md)

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)
