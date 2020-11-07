---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultCertificate.md
ms.openlocfilehash: 7f75f07ee8f53a57cdb2e359fb4addb51b1d7f76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560168"
---
# <span data-ttu-id="5b89f-101">Backup-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="5b89f-101">Backup-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="5b89f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5b89f-102">SYNOPSIS</span></span>
<span data-ttu-id="5b89f-103">Создание резервной копии сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="5b89f-103">Backs up a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b89f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5b89f-104">SYNTAX</span></span>

### <span data-ttu-id="5b89f-105">ByCertificateName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5b89f-105">ByCertificateName (Default)</span></span>
```
Backup-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b89f-106">ByCertificate</span><span class="sxs-lookup"><span data-stu-id="5b89f-106">ByCertificate</span></span>
```
Backup-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b89f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b89f-107">DESCRIPTION</span></span>
<span data-ttu-id="5b89f-108">Командлет **BACKUP-AzureKeyVaultCertificate** производит резервное копирование указанного сертификата в хранилище ключей, загружая его и сохраняя в файле.</span><span class="sxs-lookup"><span data-stu-id="5b89f-108">The **Backup-AzureKeyVaultCertificate** cmdlet backs up a specified certificate in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="5b89f-109">Если у сертификата есть несколько версий, все их версии будут включены в резервную копию.</span><span class="sxs-lookup"><span data-stu-id="5b89f-109">If the certificate has multiple versions, all its versions will be included in the backup.</span></span>
<span data-ttu-id="5b89f-110">Поскольку загруженное содержимое зашифровано, оно не может использоваться за пределами хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="5b89f-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="5b89f-111">Вы можете восстановить резервную копию сертификата в любом хранилище ключей в подписке, из которой она была создана, пока она находится в том же географическом расположении Azure.</span><span class="sxs-lookup"><span data-stu-id="5b89f-111">You can restore a backed-up certificate to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="5b89f-112">Ниже приведены основные причины использования этого командлета.</span><span class="sxs-lookup"><span data-stu-id="5b89f-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="5b89f-113">Вы хотите сохранить автономную копию сертификата на случай, если вы случайно удалили оригинал из хранилища.</span><span class="sxs-lookup"><span data-stu-id="5b89f-113">You want to retain an offline copy of the certificate in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="5b89f-114">Вы создали сертификат с помощью ключа Vault и теперь хотите клонировать объект в другой регион Azure, чтобы его можно было использовать из всех экземпляров распределенного приложения.</span><span class="sxs-lookup"><span data-stu-id="5b89f-114">You created a certificate using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="5b89f-115">С помощью командлета **BACKUP-AzureKeyVaultCertificate** можно получить сертификат в зашифрованном формате, а затем использовать командлет **RESTORE-AzureKeyVaultCertificate** и указав для него хранилище ключей во втором регионе.</span><span class="sxs-lookup"><span data-stu-id="5b89f-115">Use the **Backup-AzureKeyVaultCertificate** cmdlet to retrieve the certificate in encrypted format and then use the **Restore-AzureKeyVaultCertificate** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="5b89f-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5b89f-116">EXAMPLES</span></span>

### <span data-ttu-id="5b89f-117">Пример 1: создание резервной копии сертификата с автоматически сгенерированным именем файла</span><span class="sxs-lookup"><span data-stu-id="5b89f-117">Example 1: Back up a certificate with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

<span data-ttu-id="5b89f-118">Эта команда извлекает сертификат с именем MyCert из хранилища ключей с именем MyKeyVault и сохраняет резервную копию этого сертификата в файл с автоматическим именем и выводит имя файла.</span><span class="sxs-lookup"><span data-stu-id="5b89f-118">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="5b89f-119">Пример 2: создание резервной копии сертификата для указанного имени файла</span><span class="sxs-lookup"><span data-stu-id="5b89f-119">Example 2: Back up a certificate to a specified file name</span></span>
```powershell
PS C:\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="5b89f-120">Эта команда извлекает сертификат с именем MyCert из хранилища ключей с именем MyKeyVault и сохраняет резервную копию этого сертификата в файле с именем Backup. BLOB.</span><span class="sxs-lookup"><span data-stu-id="5b89f-120">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file named Backup.blob.</span></span>

### <span data-ttu-id="5b89f-121">Пример 3: создание резервной копии ранее полученного сертификата по указанному имени файла с перезазаписьм конечного файла без запроса.</span><span class="sxs-lookup"><span data-stu-id="5b89f-121">Example 3: Back up a previously retrieved certificate to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $cert = Get-AzureKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzureKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="5b89f-122">Эта команда создает резервную копию сертификата с именем $cert. Имя в хранилище с именем $cert. VaultName файл с именем Backup. BLOB, перезапись файла без уведомления, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="5b89f-122">This command creates a backup of the certificate named $cert.Name in the vault named $cert.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="5b89f-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5b89f-123">PARAMETERS</span></span>

### <span data-ttu-id="5b89f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b89f-124">-DefaultProfile</span></span>
<span data-ttu-id="5b89f-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b89f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b89f-126">-Force</span><span class="sxs-lookup"><span data-stu-id="5b89f-126">-Force</span></span>
<span data-ttu-id="5b89f-127">Перезаписать заданный файл, если он существует</span><span class="sxs-lookup"><span data-stu-id="5b89f-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="5b89f-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b89f-128">-InputObject</span></span>
<span data-ttu-id="5b89f-129">Секрет, для которого необходимо создать резервную копию, конвейер из результатов запроса на получение.</span><span class="sxs-lookup"><span data-stu-id="5b89f-129">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByCertificate
Aliases: Certificate

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b89f-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5b89f-130">-Name</span></span>
<span data-ttu-id="5b89f-131">Имя секрета.</span><span class="sxs-lookup"><span data-stu-id="5b89f-131">Secret name.</span></span>
<span data-ttu-id="5b89f-132">Командлет создает полное доменное имя секрета из имени хранилища, выбранного в настоящее время среды и имени секрета.</span><span class="sxs-lookup"><span data-stu-id="5b89f-132">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b89f-133">-Выходной_файл</span><span class="sxs-lookup"><span data-stu-id="5b89f-133">-OutputFile</span></span>
<span data-ttu-id="5b89f-134">Выходной файл.</span><span class="sxs-lookup"><span data-stu-id="5b89f-134">Output file.</span></span>
<span data-ttu-id="5b89f-135">Выходной файл, в котором будет храниться резервная копия сертификата.</span><span class="sxs-lookup"><span data-stu-id="5b89f-135">The output file to store the backup of the certificate.</span></span>
<span data-ttu-id="5b89f-136">Если не указано, будет создано имя файла по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5b89f-136">If not specified, a default filename will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b89f-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5b89f-137">-VaultName</span></span>
<span data-ttu-id="5b89f-138">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="5b89f-138">Vault name.</span></span>
<span data-ttu-id="5b89f-139">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="5b89f-139">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b89f-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b89f-140">-Confirm</span></span>
<span data-ttu-id="5b89f-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5b89f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b89f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b89f-142">-WhatIf</span></span>
<span data-ttu-id="5b89f-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5b89f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b89f-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5b89f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b89f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b89f-145">CommonParameters</span></span>
<span data-ttu-id="5b89f-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5b89f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b89f-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b89f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b89f-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5b89f-148">INPUTS</span></span>

### <span data-ttu-id="5b89f-149">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="5b89f-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="5b89f-150">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5b89f-150">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="5b89f-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b89f-151">OUTPUTS</span></span>

### <span data-ttu-id="5b89f-152">System. String</span><span class="sxs-lookup"><span data-stu-id="5b89f-152">System.String</span></span>

## <span data-ttu-id="5b89f-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="5b89f-153">NOTES</span></span>

## <span data-ttu-id="5b89f-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b89f-154">RELATED LINKS</span></span>