---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: D4188DC6-A8AB-4B45-9781-94B74C338C63
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultCertificate.md
ms.openlocfilehash: 6591b96257a1c94cd2da9d0bc6f2995dc2034a40
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720657"
---
# <span data-ttu-id="0a529-101">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0a529-101">Import-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="0a529-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a529-102">SYNOPSIS</span></span>
<span data-ttu-id="0a529-103">Импорт сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="0a529-103">Imports a certificate to a key vault.</span></span>

## <span data-ttu-id="0a529-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a529-104">SYNTAX</span></span>

### <span data-ttu-id="0a529-105">ImportCertificateFromFile (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0a529-105">ImportCertificateFromFile (Default)</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -FilePath <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a529-106">ImportWithPrivateKeyFromString</span><span class="sxs-lookup"><span data-stu-id="0a529-106">ImportWithPrivateKeyFromString</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> -CertificateString <String>
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a529-107">ImportWithPrivateKeyFromCollection</span><span class="sxs-lookup"><span data-stu-id="0a529-107">ImportWithPrivateKeyFromCollection</span></span>
```
Import-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String>
 [-CertificateCollection] <X509Certificate2Collection> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a529-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a529-108">DESCRIPTION</span></span>
<span data-ttu-id="0a529-109">Командлет **Import-AzKeyVaultCertificate** импортирует сертификат в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="0a529-109">The **Import-AzKeyVaultCertificate** cmdlet imports a certificate into a key vault.</span></span>
<span data-ttu-id="0a529-110">Вы можете создать сертификат для импорта с помощью одного из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="0a529-110">You can create the certificate to import by using one of the following methods:</span></span>
- <span data-ttu-id="0a529-111">Используйте командлет New-AzKeyVaultCertificateSigningRequest, чтобы создать запрос на подписывание сертификата и отправить его в центр сертификации.</span><span class="sxs-lookup"><span data-stu-id="0a529-111">Use the New-AzKeyVaultCertificateSigningRequest cmdlet to create a certificate signing request and submit it to a certificate authority.</span></span>
- <span data-ttu-id="0a529-112">Используйте существующий файл пакета сертификата, например PFX или P12, который включает в себя сертификат и закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="0a529-112">Use an existing certificate package file, such as a .pfx or .p12 file, which contains both the certificate and private key.</span></span>

## <span data-ttu-id="0a529-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a529-113">EXAMPLES</span></span>

### <span data-ttu-id="0a529-114">Пример 1: Импорт сертификата хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="0a529-114">Example 1: Import a key vault certificate</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS C:\> Import-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "ImportCert01" -FilePath "C:\Users\contosoUser\Desktop\import.pfx" -Password $Password

Name        : importCert01
Certificate : [Subject]
                CN=contoso.com

              [Issuer]
                CN=contoso.com

              [Serial Number]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before]
                2/8/2016 3:11:45 PM

              [Not After]
                8/8/2016 4:21:45 PM

              [Thumbprint]
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        :
Enabled     : True
Created     : 2/8/2016 11:50:43 PM
Updated     : 2/8/2016 11:50:43 PM
```

<span data-ttu-id="0a529-115">Первая команда использует командлет ConvertTo-SecureString для создания защищенного пароля и сохраняет его в переменной $Password.</span><span class="sxs-lookup"><span data-stu-id="0a529-115">The first command uses the ConvertTo-SecureString cmdlet to create a secure password, and then stores it in the $Password variable.</span></span>
<span data-ttu-id="0a529-116">Вторая команда импортирует сертификат с именем ImportCert01 в хранилище ключей CosotosoKV01.</span><span class="sxs-lookup"><span data-stu-id="0a529-116">The second command imports the certificate named ImportCert01 into the CosotosoKV01 key vault.</span></span>

## <span data-ttu-id="0a529-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a529-117">PARAMETERS</span></span>

### <span data-ttu-id="0a529-118">-CertificateCollection</span><span class="sxs-lookup"><span data-stu-id="0a529-118">-CertificateCollection</span></span>
<span data-ttu-id="0a529-119">Указывает коллекцию сертификатов, которую нужно добавить в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="0a529-119">Specifies the certificate collection to add to a key vault.</span></span>

```yaml
Type: System.Security.Cryptography.X509Certificates.X509Certificate2Collection
Parameter Sets: ImportWithPrivateKeyFromCollection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a529-120">-CertificateString</span><span class="sxs-lookup"><span data-stu-id="0a529-120">-CertificateString</span></span>
<span data-ttu-id="0a529-121">Указывает строку сертификата.</span><span class="sxs-lookup"><span data-stu-id="0a529-121">Specifies a certificate string.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportWithPrivateKeyFromString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a529-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a529-122">-DefaultProfile</span></span>
<span data-ttu-id="0a529-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0a529-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a529-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="0a529-124">-FilePath</span></span>
<span data-ttu-id="0a529-125">Задает путь к файлу сертификата, который импортируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="0a529-125">Specifies the path of the certificate file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a529-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0a529-126">-Name</span></span>
<span data-ttu-id="0a529-127">Указывает имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="0a529-127">Specifies the certificate name.</span></span> <span data-ttu-id="0a529-128">Этот командлет создает полное доменное имя (FQDN) сертификата из имени хранилища ключей, выбранной в данный момент среды и имени сертификата.</span><span class="sxs-lookup"><span data-stu-id="0a529-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate from key vault name, currently selected environment, and certificate name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a529-129">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="0a529-129">-Password</span></span>
<span data-ttu-id="0a529-130">Указывает пароль для файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="0a529-130">Specifies the password for a certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ImportCertificateFromFile, ImportWithPrivateKeyFromString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a529-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="0a529-131">-Tag</span></span>
<span data-ttu-id="0a529-132">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="0a529-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0a529-133">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="0a529-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a529-134">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0a529-134">-VaultName</span></span>
<span data-ttu-id="0a529-135">Указывает имя хранилища ключей, в которое этот командлет импортирует сертификаты.</span><span class="sxs-lookup"><span data-stu-id="0a529-135">Specifies the key vault name into which this cmdlet imports certificates.</span></span>
<span data-ttu-id="0a529-136">Этот командлет создает полное доменное имя (FQDN) для хранилища ключей, основываясь на имени и выбранной в данный момент среде.</span><span class="sxs-lookup"><span data-stu-id="0a529-136">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a529-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a529-137">-Confirm</span></span>
<span data-ttu-id="0a529-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0a529-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a529-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a529-139">-WhatIf</span></span>
<span data-ttu-id="0a529-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0a529-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a529-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0a529-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a529-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a529-142">CommonParameters</span></span>
<span data-ttu-id="0a529-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a529-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a529-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a529-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a529-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a529-145">INPUTS</span></span>

### <span data-ttu-id="0a529-146">System. String</span><span class="sxs-lookup"><span data-stu-id="0a529-146">System.String</span></span>

### <span data-ttu-id="0a529-147">System. Security. Cryptography. X509Certificates. X509Certificate2Collection</span><span class="sxs-lookup"><span data-stu-id="0a529-147">System.Security.Cryptography.X509Certificates.X509Certificate2Collection</span></span>

### <span data-ttu-id="0a529-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0a529-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0a529-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a529-149">OUTPUTS</span></span>

### <span data-ttu-id="0a529-150">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0a529-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="0a529-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a529-151">NOTES</span></span>

## <span data-ttu-id="0a529-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a529-152">RELATED LINKS</span></span>

[<span data-ttu-id="0a529-153">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0a529-153">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)