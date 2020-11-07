---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: ff384b456d6cbaac3fa0c28f01038a60b211dfca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720661"
---
# <span data-ttu-id="17fd6-101">Get-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="17fd6-101">Get-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="17fd6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="17fd6-102">SYNOPSIS</span></span>
<span data-ttu-id="17fd6-103">Получение определений SAS хранилища, управляемого основным хранилищем.</span><span class="sxs-lookup"><span data-stu-id="17fd6-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

## <span data-ttu-id="17fd6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="17fd6-104">SYNTAX</span></span>

### <span data-ttu-id="17fd6-105">ByDefinitionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="17fd6-105">ByDefinitionName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [[-Name] <String>]
 [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17fd6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="17fd6-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-Name] <String>] [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17fd6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17fd6-107">DESCRIPTION</span></span>
<span data-ttu-id="17fd6-108">Возвращает определение SAS хранилища управляемых хранилищ, если указано имя определения.</span><span class="sxs-lookup"><span data-stu-id="17fd6-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="17fd6-109">Если имя определения не задано, в списке будут перечислены все определения SAS, связанные с указанной учетной записью в хранилище ключей, управляемой в хранилище.</span><span class="sxs-lookup"><span data-stu-id="17fd6-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="17fd6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="17fd6-110">EXAMPLES</span></span>

### <span data-ttu-id="17fd6-111">Пример 1: список всех определений SAS хранилища, управляемых основным хранилищем</span><span class="sxs-lookup"><span data-stu-id="17fd6-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="17fd6-112">В этой статье перечислены все определения SAS, связанные с учетной записью хранилища с управляемым хранилищем "mystorageaccount", управляемой хранилищем "myvault"</span><span class="sxs-lookup"><span data-stu-id="17fd6-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="17fd6-113">Пример 2: получение учетной записи хранилища с управляемым хранилищем ключей</span><span class="sxs-lookup"><span data-stu-id="17fd6-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'accountsas'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Secret Id   : https://myvault.vault.azure.net/secrets/mystorageaccount-accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Parameter   :
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="17fd6-114">Получает подробные сведения об определении SAS "accountsas", связанном с учетной записью хранилища с управляемым хранилищем "mystorageaccount", управляемой хранилищем "myvault".</span><span class="sxs-lookup"><span data-stu-id="17fd6-114">Gets the details of SAS Definition 'accountsas' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

### <span data-ttu-id="17fd6-115">Пример 3: перечисление всех определений управляемых хранилищ данных для хранилища ключей с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="17fd6-115">Example 3: List all Key Vault managed Storage SAS Definitions using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name "account*"

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas1
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas1
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas2
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas2
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="17fd6-116">В этой статье перечислены все определения SAS, связанные с учетной записью хранилища с управляемым хранилищем "mystorageaccount", управляемой хранилищем "myvault", которое начинается с "учетная запись".</span><span class="sxs-lookup"><span data-stu-id="17fd6-116">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault' that start with "account".</span></span>

## <span data-ttu-id="17fd6-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="17fd6-117">PARAMETERS</span></span>

### <span data-ttu-id="17fd6-118">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="17fd6-118">-AccountName</span></span>
<span data-ttu-id="17fd6-119">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="17fd6-119">Vault name.</span></span>
<span data-ttu-id="17fd6-120">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="17fd6-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17fd6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17fd6-121">-DefaultProfile</span></span>
<span data-ttu-id="17fd6-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="17fd6-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17fd6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17fd6-123">-InputObject</span></span>
<span data-ttu-id="17fd6-124">Объект ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="17fd6-124">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17fd6-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="17fd6-125">-InRemovedState</span></span>
<span data-ttu-id="17fd6-126">Указывает, следует ли отображать ранее удаленные определения SAS хранилища в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="17fd6-126">Specifies whether to show the previously deleted storage sas definitions in the output.</span></span>

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

### <span data-ttu-id="17fd6-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="17fd6-127">-Name</span></span>
<span data-ttu-id="17fd6-128">Имя определения SAS хранилища.</span><span class="sxs-lookup"><span data-stu-id="17fd6-128">Storage sas definition name.</span></span>
<span data-ttu-id="17fd6-129">Командлет создает полное доменное имя определения SAS хранилища из имени хранилища, выбранной среды, имени учетной записи хранения и имени определения SAS.</span><span class="sxs-lookup"><span data-stu-id="17fd6-129">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17fd6-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="17fd6-130">-VaultName</span></span>
<span data-ttu-id="17fd6-131">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="17fd6-131">Vault name.</span></span>
<span data-ttu-id="17fd6-132">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="17fd6-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17fd6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17fd6-133">CommonParameters</span></span>
<span data-ttu-id="17fd6-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="17fd6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17fd6-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17fd6-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17fd6-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="17fd6-136">INPUTS</span></span>

### <span data-ttu-id="17fd6-137">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="17fd6-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="17fd6-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="17fd6-138">OUTPUTS</span></span>

### <span data-ttu-id="17fd6-139">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="17fd6-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

### <span data-ttu-id="17fd6-140">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="17fd6-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="17fd6-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="17fd6-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="17fd6-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="17fd6-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="17fd6-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="17fd6-143">NOTES</span></span>

## <span data-ttu-id="17fd6-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17fd6-144">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)
