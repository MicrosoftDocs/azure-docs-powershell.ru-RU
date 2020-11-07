---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
ms.openlocfilehash: 6c8fcc5476ea2defda78ea03cc1acce7b7e3dea9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567986"
---
# <span data-ttu-id="cb40f-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="cb40f-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="cb40f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cb40f-102">SYNOPSIS</span></span>
<span data-ttu-id="cb40f-103">Удаляет сертификат из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="cb40f-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb40f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cb40f-104">SYNTAX</span></span>

### <span data-ttu-id="cb40f-105">ByVaultNameAndName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cb40f-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb40f-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="cb40f-106">ByObject</span></span>
```
Remove-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb40f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb40f-107">DESCRIPTION</span></span>
<span data-ttu-id="cb40f-108">Командлет **Remove-AzureKeyVaultCertificate** Удаляет сертификат из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="cb40f-108">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="cb40f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cb40f-109">EXAMPLES</span></span>

### <span data-ttu-id="cb40f-110">Пример 1: Удаление сертификата</span><span class="sxs-lookup"><span data-stu-id="cb40f-110">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force
Name        : selfSigned01
Certificate : 
Thumbprint  : 
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:29:33 PM
Updated     : 2/8/2016 11:29:33 PM
```

<span data-ttu-id="cb40f-111">Эта команда удаляет сертификат с именем SelfSigned01 из хранилища ключей с именем ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="cb40f-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="cb40f-112">Эта команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="cb40f-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="cb40f-113">Таким образом, командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="cb40f-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="cb40f-114">Пример 3: Удаление удаленного сертификата из хранилища ключей без возможности восстановления</span><span class="sxs-lookup"><span data-stu-id="cb40f-114">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="cb40f-115">Эта команда окончательно удаляет сертификат с именем "MyCert" из хранилища ключей с именем "contoso".</span><span class="sxs-lookup"><span data-stu-id="cb40f-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="cb40f-116">Для выполнения этого командлета требуется разрешение на очистку, которое должно быть ранее и явно предоставлено пользователю в этом хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="cb40f-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="cb40f-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cb40f-117">PARAMETERS</span></span>

### <span data-ttu-id="cb40f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb40f-118">-DefaultProfile</span></span>
<span data-ttu-id="cb40f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cb40f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb40f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="cb40f-120">-Force</span></span>
<span data-ttu-id="cb40f-121">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="cb40f-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cb40f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb40f-122">-InputObject</span></span>
<span data-ttu-id="cb40f-123">Объект сертификата.</span><span class="sxs-lookup"><span data-stu-id="cb40f-123">Certificate Object.</span></span>

```yaml
Type: PSKeyVaultCertificateIdentityItem
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb40f-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="cb40f-124">-InRemovedState</span></span>
<span data-ttu-id="cb40f-125">Если он указан, окончательно удаляет ранее удаленный сертификат.</span><span class="sxs-lookup"><span data-stu-id="cb40f-125">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="cb40f-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cb40f-126">-Name</span></span>
<span data-ttu-id="cb40f-127">Указывает имя сертификата, который этот командлет удаляет из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="cb40f-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="cb40f-128">Этот командлет создает полное доменное имя (FQDN) сертификата на основе имени, которое указывает этот параметр, имя хранилища ключей и текущую среду.</span><span class="sxs-lookup"><span data-stu-id="cb40f-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb40f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb40f-129">-PassThru</span></span>
<span data-ttu-id="cb40f-130">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="cb40f-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cb40f-131">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="cb40f-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cb40f-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="cb40f-132">-VaultName</span></span>
<span data-ttu-id="cb40f-133">Указывает имя хранилища ключей, из которого этот командлет удаляет сертификат.</span><span class="sxs-lookup"><span data-stu-id="cb40f-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="cb40f-134">Этот командлет создает полное доменное имя хранилища ключей, основываясь на имени, указанном этим параметром, и текущей среде.</span><span class="sxs-lookup"><span data-stu-id="cb40f-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb40f-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb40f-135">-Confirm</span></span>
<span data-ttu-id="cb40f-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cb40f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb40f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb40f-137">-WhatIf</span></span>
<span data-ttu-id="cb40f-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cb40f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb40f-139">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cb40f-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb40f-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cb40f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb40f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb40f-141">CommonParameters</span></span>
<span data-ttu-id="cb40f-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cb40f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb40f-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb40f-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb40f-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cb40f-144">INPUTS</span></span>

### <span data-ttu-id="cb40f-145">Ничего</span><span class="sxs-lookup"><span data-stu-id="cb40f-145">None</span></span>
<span data-ttu-id="cb40f-146">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="cb40f-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cb40f-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb40f-147">OUTPUTS</span></span>

### <span data-ttu-id="cb40f-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="cb40f-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="cb40f-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="cb40f-149">NOTES</span></span>

## <span data-ttu-id="cb40f-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb40f-150">RELATED LINKS</span></span>

[<span data-ttu-id="cb40f-151">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="cb40f-151">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="cb40f-152">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="cb40f-152">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="cb40f-153">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="cb40f-153">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="cb40f-154">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="cb40f-154">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)