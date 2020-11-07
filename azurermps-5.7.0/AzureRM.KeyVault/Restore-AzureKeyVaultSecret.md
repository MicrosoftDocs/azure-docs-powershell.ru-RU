---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
ms.openlocfilehash: 1ba12a18c88004dcc1c6761d71fdc1983a5ba0c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566172"
---
# <span data-ttu-id="67d63-101">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="67d63-101">Restore-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="67d63-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="67d63-102">SYNOPSIS</span></span>
<span data-ttu-id="67d63-103">Создает секретный ключ из резервного хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="67d63-103">Creates a secret in a key vault from a backed-up secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67d63-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="67d63-104">SYNTAX</span></span>

### <span data-ttu-id="67d63-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="67d63-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67d63-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="67d63-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67d63-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67d63-107">DESCRIPTION</span></span>
<span data-ttu-id="67d63-108">Командлет **RESTORE-AzureKeyVaultSecret** создает секрет в указанном хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="67d63-108">The **Restore-AzureKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="67d63-109">Этот секрет — это реплика резервного файла в файле входных данных с тем же именем, что и у первоначального секрета.</span><span class="sxs-lookup"><span data-stu-id="67d63-109">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="67d63-110">Если в хранилище ключей уже есть секрет с тем же именем, этот командлет не будет работать вместо перезаписи исходного секрета.</span><span class="sxs-lookup"><span data-stu-id="67d63-110">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="67d63-111">Если резервная копия имеет несколько версий секрета, восстанавливаются все версии.</span><span class="sxs-lookup"><span data-stu-id="67d63-111">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="67d63-112">Хранилище ключей, в которое вы восстановите секретный ключ, может отличаться от того, с помощью которого вы заархивированы из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="67d63-112">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="67d63-113">Тем не менее, в одном и том же географическом хранилище вы должны использовать одну и ту же подписку, а также находиться в регионе Azure (например, в Северной Америке).</span><span class="sxs-lookup"><span data-stu-id="67d63-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="67d63-114">Просмотрите центр управления безопасностью Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) для сопоставления областей Azure с географией).</span><span class="sxs-lookup"><span data-stu-id="67d63-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="67d63-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="67d63-115">EXAMPLES</span></span>

### <span data-ttu-id="67d63-116">Пример 1: восстановление резервной копии (секретной)</span><span class="sxs-lookup"><span data-stu-id="67d63-116">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzureKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="67d63-117">Эта команда восстанавливает секрет, в том числе все его версии, из файла резервной копии с именем Backup. BLOB в хранилище ключей с именем MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="67d63-117">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="67d63-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="67d63-118">PARAMETERS</span></span>

### <span data-ttu-id="67d63-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67d63-119">-DefaultProfile</span></span>
<span data-ttu-id="67d63-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="67d63-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67d63-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="67d63-121">-InputFile</span></span>
<span data-ttu-id="67d63-122">Задает входной файл, содержащий резервную копию секрета для восстановления.</span><span class="sxs-lookup"><span data-stu-id="67d63-122">Specifies the input file that contains the backup of the secret to restore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d63-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67d63-123">-InputObject</span></span>
<span data-ttu-id="67d63-124">Объект KeyVault</span><span class="sxs-lookup"><span data-stu-id="67d63-124">KeyVault object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67d63-125">-VaultName</span><span class="sxs-lookup"><span data-stu-id="67d63-125">-VaultName</span></span>
<span data-ttu-id="67d63-126">Указывает имя хранилища ключей, в которое нужно восстановить секретный код.</span><span class="sxs-lookup"><span data-stu-id="67d63-126">Specifies the name of the key vault into which to restore the secret.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67d63-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67d63-127">-Confirm</span></span>
<span data-ttu-id="67d63-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="67d63-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67d63-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67d63-129">-WhatIf</span></span>
<span data-ttu-id="67d63-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="67d63-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67d63-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="67d63-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67d63-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67d63-132">CommonParameters</span></span>
<span data-ttu-id="67d63-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="67d63-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67d63-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67d63-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67d63-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="67d63-135">INPUTS</span></span>

### <span data-ttu-id="67d63-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="67d63-136">None</span></span>
<span data-ttu-id="67d63-137">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="67d63-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="67d63-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="67d63-138">OUTPUTS</span></span>

### <span data-ttu-id="67d63-139">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="67d63-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="67d63-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="67d63-140">NOTES</span></span>

## <span data-ttu-id="67d63-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67d63-141">RELATED LINKS</span></span>

[<span data-ttu-id="67d63-142">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="67d63-142">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="67d63-143">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="67d63-143">Backup-AzureKeyVaultSecret</span></span>](./Backup-AzureKeyVaultSecret.md)

[<span data-ttu-id="67d63-144">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="67d63-144">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="67d63-145">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="67d63-145">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
