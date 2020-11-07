---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultSecret.md
ms.openlocfilehash: 1a2445509aca49c28320ad1fc1685daa0127fa50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561772"
---
# <span data-ttu-id="11e04-101">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="11e04-101">Backup-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="11e04-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="11e04-102">SYNOPSIS</span></span>
<span data-ttu-id="11e04-103">Резервное копирование секрета в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="11e04-103">Backs up a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11e04-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="11e04-104">SYNTAX</span></span>

### <span data-ttu-id="11e04-105">BySecretName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="11e04-105">BySecretName (Default)</span></span>
```
Backup-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11e04-106">BySecret</span><span class="sxs-lookup"><span data-stu-id="11e04-106">BySecret</span></span>
```
Backup-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11e04-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11e04-107">DESCRIPTION</span></span>
<span data-ttu-id="11e04-108">Командлет **BACKUP-AzureKeyVaultSecret** производит резервное копирование указанного секрета в качестве ключа, загружая его и сохраняя в файле.</span><span class="sxs-lookup"><span data-stu-id="11e04-108">The **Backup-AzureKeyVaultSecret** cmdlet backs up a specified secret in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="11e04-109">Если существует несколько версий секрета, в резервную копию включаются все версии.</span><span class="sxs-lookup"><span data-stu-id="11e04-109">If there are multiple versions of the secret, all versions are included in the backup.</span></span>
<span data-ttu-id="11e04-110">Поскольку загруженное содержимое зашифровано, оно не может использоваться за пределами хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="11e04-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="11e04-111">Вы можете восстановить резервные копии в любом хранилище ключей в подписке, из которой она была создана.</span><span class="sxs-lookup"><span data-stu-id="11e04-111">You can restore a backed-up secret to any key vault in the subscription that it was backed up from.</span></span>

<span data-ttu-id="11e04-112">Ниже приведены основные причины использования этого командлета.</span><span class="sxs-lookup"><span data-stu-id="11e04-112">Typical reasons to use this cmdlet are:</span></span>

- <span data-ttu-id="11e04-113">Вы хотите пополнить свою копию секрета, чтобы иметь возможность использовать автономную копию на случай, если вы случайно удалили свой секрет в своем вашем хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="11e04-113">You want to escrow a copy of your secret, so that you have an offline copy in case you accidentally delete your secret in your key vault.</span></span>
- <span data-ttu-id="11e04-114">Вы добавили секрет в хранилище ключей и теперь хотите клонировать секрет в другой регион Azure, чтобы его можно было использовать из всех экземпляров распределенного приложения.</span><span class="sxs-lookup"><span data-stu-id="11e04-114">You added a secret to a key vault and now want to clone the secret into a different Azure region, so that you can use it from all instances of your distributed application.</span></span> <span data-ttu-id="11e04-115">С помощью командлета Backup-AzureKeyVaultSecret можно получить секретный код в зашифрованном формате, а затем использовать командлет Restore-AzureKeyVaultSecret и указать в качестве него ключевое хранилище во втором регионе.</span><span class="sxs-lookup"><span data-stu-id="11e04-115">Use the Backup-AzureKeyVaultSecret cmdlet to retrieve the secret in encrypted format and then use the Restore-AzureKeyVaultSecret cmdlet and specify a key vault in the second region.</span></span> <span data-ttu-id="11e04-116">(Обратите внимание, что регионы должны принадлежать одному и тому же географическому элементу.)</span><span class="sxs-lookup"><span data-stu-id="11e04-116">(Note that the regions must belong to the same geography.)</span></span>

## <span data-ttu-id="11e04-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="11e04-117">EXAMPLES</span></span>

### <span data-ttu-id="11e04-118">Пример 1: резервное копирование секрета с автоматически сгенерированным именем файла</span><span class="sxs-lookup"><span data-stu-id="11e04-118">Example 1: Back up a secret with an automatically generated file name</span></span>
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="11e04-119">Эта команда извлекает секретный файл с именем MySecret из хранилища ключей с именем MyKeyVault и сохраняет резервную копию этого секрета в файле, который будет автоматически называться, и выводит имя файла.</span><span class="sxs-lookup"><span data-stu-id="11e04-119">This command retrieves the secret named MySecret from the key vault named MyKeyVault and saves a backup of that secret to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="11e04-120">Пример 2: создание резервной копии секретного файла с заданным именем и перезапись существующего файла без запроса</span><span class="sxs-lookup"><span data-stu-id="11e04-120">Example 2: Back up a secret to a specified file name, overwriting the existing file without prompting</span></span>
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force
```

<span data-ttu-id="11e04-121">Эта команда извлекает секрет с именем MySecret из ключа vaultnamed MyKeyVault и сохраняет резервную копию этого секрета в файле с именем Backup. BLOB.</span><span class="sxs-lookup"><span data-stu-id="11e04-121">This command retrieves the secret named MySecret from the key vaultnamed MyKeyVault and saves a backup of that secret to a file named Backup.blob.</span></span>

### <span data-ttu-id="11e04-122">Пример 3: создание резервной копии ранее извлеченного секретного файла с указанным именем</span><span class="sxs-lookup"><span data-stu-id="11e04-122">Example 3: Back up a secret previously retrieved to a specified file name</span></span>
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\>Backup-AzureKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'
```

<span data-ttu-id="11e04-123">Эта команда использует имя и имя хранилища объекта $secret, чтобы получить секрет и сохранит его резервную копию в файле с именем Backup. BLOB.</span><span class="sxs-lookup"><span data-stu-id="11e04-123">This command uses the $secret object's vault name and name to retrieves the secret and saves its backup to a file named Backup.blob.</span></span>

## <span data-ttu-id="11e04-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="11e04-124">PARAMETERS</span></span>

### <span data-ttu-id="11e04-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e04-125">-DefaultProfile</span></span>
<span data-ttu-id="11e04-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="11e04-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11e04-127">-Force</span><span class="sxs-lookup"><span data-stu-id="11e04-127">-Force</span></span>
<span data-ttu-id="11e04-128">Запрашивает подтверждение перед перезаписью выходного файла, если он существует.</span><span class="sxs-lookup"><span data-stu-id="11e04-128">Prompts you for confirmation before overwriting the output file, if that exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11e04-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11e04-129">-InputObject</span></span>
<span data-ttu-id="11e04-130">Секрет, для которого необходимо создать резервную копию, конвейер из результатов запроса на получение.</span><span class="sxs-lookup"><span data-stu-id="11e04-130">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: PSKeyVaultSecretIdentityItem
Parameter Sets: BySecret
Aliases: Secret

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11e04-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="11e04-131">-Name</span></span>
<span data-ttu-id="11e04-132">Задает имя секрета для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="11e04-132">Specifies the name of the secret to back up.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11e04-133">-Выходной_файл</span><span class="sxs-lookup"><span data-stu-id="11e04-133">-OutputFile</span></span>
<span data-ttu-id="11e04-134">Указывает выходной файл, в котором хранится резервная копия (BLOB-объект).</span><span class="sxs-lookup"><span data-stu-id="11e04-134">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="11e04-135">Если этот параметр не указан, этот командлет создаст имя файла.</span><span class="sxs-lookup"><span data-stu-id="11e04-135">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="11e04-136">Если вы задаете имя существующего выходного файла, операция не завершится и вернет сообщение об ошибке, в котором файл резервной копии уже существует.</span><span class="sxs-lookup"><span data-stu-id="11e04-136">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11e04-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="11e04-137">-VaultName</span></span>
<span data-ttu-id="11e04-138">Указывает имя хранилища ключей, содержащего секрет для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="11e04-138">Specifies the name of the key vault that contains the secret to back up.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11e04-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11e04-139">-Confirm</span></span>
<span data-ttu-id="11e04-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="11e04-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11e04-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11e04-141">-WhatIf</span></span>
<span data-ttu-id="11e04-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="11e04-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11e04-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="11e04-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11e04-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e04-144">CommonParameters</span></span>
<span data-ttu-id="11e04-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="11e04-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e04-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11e04-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e04-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="11e04-147">INPUTS</span></span>

### <span data-ttu-id="11e04-148">Ничего</span><span class="sxs-lookup"><span data-stu-id="11e04-148">None</span></span>
<span data-ttu-id="11e04-149">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="11e04-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="11e04-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="11e04-150">OUTPUTS</span></span>

### <span data-ttu-id="11e04-151">Подстрок</span><span class="sxs-lookup"><span data-stu-id="11e04-151">String</span></span>
<span data-ttu-id="11e04-152">Командлет возвращает путь к выходному файлу, содержащему резервную копию ключа.</span><span class="sxs-lookup"><span data-stu-id="11e04-152">The cmdlet returns the path of the output file containing the backup of the key.</span></span>

## <span data-ttu-id="11e04-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="11e04-153">NOTES</span></span>

## <span data-ttu-id="11e04-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11e04-154">RELATED LINKS</span></span>

[<span data-ttu-id="11e04-155">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="11e04-155">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="11e04-156">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="11e04-156">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="11e04-157">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="11e04-157">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="11e04-158">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="11e04-158">Restore-AzureKeyVaultSecret</span></span>](./Restore-AzureKeyVaultSecret.md)
