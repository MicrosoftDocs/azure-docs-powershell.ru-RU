---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-Azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 41fcea2b0afc7c18da2f3e4e71764bff1ab2920c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911170"
---
# New-AzKeyVault

## КРАТКИй обзор
Создание хранилища ключей.

## Максимальное

```
New-AzKeyVault [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzKeyVault** создает хранилище ключей в указанной группе ресурсов. Этот командлет также предоставляет пользователям разрешения на добавление, удаление или перечисление ключей и секретных параметров в хранилище ключей.

Примечание. Если вы видите сообщение об ошибке **"не зарегистрирована подписка на использование пространства имен" Microsoft. KeyVault "** при попытке создания нового хранилища ключей, выполните команду **Register-AzResourceProvider-ProviderNamespace" Microsoft. KeyVault "** , а затем снова запустите программу **New-AzKeyVault** . Дополнительные сведения можно найти в разделе Register-AzResourceProvider.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание стандартного хранилища ключей
```
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

Эта команда создает хранилище ключей с именем Contoso03Vault в Azure Region East США. Команда добавляет хранилище ключей в группу ресурсов с именем Group14. Поскольку в команде не указано значение параметра *SKU* , создается стандартное хранилище ключа.

### Пример 2: создание хранилища ключей Premium
```
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'
```

Эта команда создает хранилище ключей, как и в предыдущем примере. Тем не менее, он задает значение Premium для параметра *SKU* для создания хранилища ключей Premium.

## ПАРАМЕТРЫ

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnabledForDeployment
Включает поставщик ресурсов Microsoft. COMPUTE для извлечения секретов из этого ключа, если это временное хранилище ссылается на создание ресурсов (например, при создании виртуальной машины).

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnabledForDiskEncryption
Позволяет службе шифрования дисков Azure получить секретные ключи и их перетекание из этого хранилища ключей.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnabledForTemplateDeployment
Позволяет диспетчеру ресурсов Azure получать секреты из этого хранилища ключей при ссылке на это хранилище ключей в развертывании шаблона.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableSoftDelete
Указывает, что функция мягкого удаления включена для этого хранилища ключей. Если включено мягкое удаление, в течение льготного периода вы можете восстановить это хранилище ключей и его содержимое после удаления.

Дополнительные сведения об этой функции можно найти в разделе Общие сведения о [мягком удалении для хранилища ключей Azure](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete). Инструкции — Узнайте, [как использовать ключевое руководство с мягким удалением с помощью PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
Указывает область Azure, в которой нужно создать хранилище ключей. С помощью команды [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) можно просмотреть варианты выбора.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя существующей группы ресурсов, в которой нужно создать хранилище ключей.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Указывает SKU экземпляра хранилища ключей. Сведения о том, какие функции доступны для каждого SKU, можно найти на веб-сайте ценообразования для Azure Key Vault ( https://go.microsoft.com/fwlink/?linkid=512521) .

```yaml
Type: SkuName
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Тег
Пары "ключ-значение" в виде хэш-таблицы. Например:

@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Задает имя создаваемого хранилища ключей. Имя может представлять собой любую комбинацию букв, цифр или дефисов. Имя должно начинаться и заканчиваться на букву или цифру. Имя должно быть универсальным уникальным.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. KeyVault. Models. PSVault

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzKeyVault](./Get-AzKeyVault.md)

[Remove-AzKeyVault](./Remove-AzKeyVault.md)
