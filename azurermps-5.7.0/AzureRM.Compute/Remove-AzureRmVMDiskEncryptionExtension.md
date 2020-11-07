---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiskEncryptionExtension.md
ms.openlocfilehash: 9c9f7dca5bd698a0eda76637618fe946b723a576
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563648"
---
# <span data-ttu-id="f73e9-101">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="f73e9-101">Remove-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="f73e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f73e9-102">SYNOPSIS</span></span>
<span data-ttu-id="f73e9-103">Удаляет расширение шифрования диска из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f73e9-103">Removes the disk encryption extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f73e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f73e9-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f73e9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f73e9-105">DESCRIPTION</span></span>
<span data-ttu-id="f73e9-106">Командлет **Remove-AzureRmVMDiskEncryptionExtension** удаляет расширение шифрования диска из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f73e9-106">The **Remove-AzureRmVMDiskEncryptionExtension** cmdlet removes the disk encryption extension from a virtual machine.</span></span>
<span data-ttu-id="f73e9-107">Если имя расширения не задано, этот командлет удаляет расширение с именем по умолчанию AzureDiskEncryption для виртуальных машин, работающих под управлением операционной системы Windows или AzureDiskEncryptionForLinux для виртуальных машин на базе Linux.</span><span class="sxs-lookup"><span data-stu-id="f73e9-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span>
<span data-ttu-id="f73e9-108">Этот командлет не отключает шифрование на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f73e9-108">This cmdlet does not disable encryption on the virtual machine.</span></span>
<span data-ttu-id="f73e9-109">Она удаляет расширение и связанную конфигурацию расширения из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f73e9-109">It removes the extension and the associated extension configuration from the virtual machine.</span></span>

## <span data-ttu-id="f73e9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f73e9-110">EXAMPLES</span></span>

### <span data-ttu-id="f73e9-111">Пример 1: Удалите расширение шифрования диска из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f73e9-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="f73e9-112">Эта команда удаляет расширение с именем по умолчанию AzureDiskEncryption для виртуальной машины под управлением операционной системы Windows или AzureDiskEncryptionForLinux для виртуальной машины на базе Linux с именем MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="f73e9-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="f73e9-113">Пример 2: удаление определенного расширения шифрования диска из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f73e9-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="f73e9-114">Эта команда удаляет расширение шифрования с именем MyDiskEncryptionExtension из виртуальной машины с именем MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="f73e9-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="f73e9-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f73e9-115">PARAMETERS</span></span>

### <span data-ttu-id="f73e9-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f73e9-116">-Force</span></span>
<span data-ttu-id="f73e9-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f73e9-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f73e9-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f73e9-118">-Name</span></span>
<span data-ttu-id="f73e9-119">Указывает имя ресурса диспетчера ресурсов Azure, представляющего расширение.</span><span class="sxs-lookup"><span data-stu-id="f73e9-119">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="f73e9-120">Командлет Set-AzureRmVMDiskEncryptionExtension задает для этого имени имя AzureDiskEncryption виртуальных машин, работающих под управлением операционной системы Windows и AzureDiskEncryptionForLinux для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="f73e9-120">The Set-AzureRmVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="f73e9-121">Указывайте этот параметр только в том случае, если вы изменили имя по умолчанию в командлете **Set-AzureRmVMDiskEncryptionExtension** или использовали другое имя ресурса в шаблоне диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f73e9-121">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f73e9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f73e9-122">-ResourceGroupName</span></span>
<span data-ttu-id="f73e9-123">Указывает имя группы ресурсов для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f73e9-123">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="f73e9-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="f73e9-124">-VMName</span></span>
<span data-ttu-id="f73e9-125">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f73e9-125">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f73e9-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f73e9-126">-Confirm</span></span>
<span data-ttu-id="f73e9-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f73e9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f73e9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f73e9-128">-WhatIf</span></span>
<span data-ttu-id="f73e9-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f73e9-129">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f73e9-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f73e9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f73e9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f73e9-131">CommonParameters</span></span>
<span data-ttu-id="f73e9-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f73e9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f73e9-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f73e9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f73e9-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f73e9-134">INPUTS</span></span>

### <span data-ttu-id="f73e9-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="f73e9-135">None</span></span>
<span data-ttu-id="f73e9-136">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f73e9-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f73e9-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f73e9-137">OUTPUTS</span></span>

## <span data-ttu-id="f73e9-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="f73e9-138">NOTES</span></span>

## <span data-ttu-id="f73e9-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f73e9-139">RELATED LINKS</span></span>

[<span data-ttu-id="f73e9-140">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="f73e9-140">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="f73e9-141">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="f73e9-141">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)

