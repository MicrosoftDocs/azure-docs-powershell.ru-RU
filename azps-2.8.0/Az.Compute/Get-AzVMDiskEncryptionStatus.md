---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
ms.openlocfilehash: 1b2a3855703c1d91a17cfd164f6a65ce218da486
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721911"
---
# <span data-ttu-id="d3aa6-101">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="d3aa6-101">Get-AzVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="d3aa6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3aa6-102">SYNOPSIS</span></span>
<span data-ttu-id="d3aa6-103">Возвращает состояние шифрования виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d3aa6-103">Gets the encryption status of the virtual machine.</span></span>

## <span data-ttu-id="d3aa6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3aa6-104">SYNTAX</span></span>

```
Get-AzVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3aa6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3aa6-105">DESCRIPTION</span></span>
<span data-ttu-id="d3aa6-106">Командлет **Get-AzVMDiskEncryptionStatus** получает состояние шифрования виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d3aa6-106">The **Get-AzVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="d3aa6-107">Отображается состояние шифрования операционной системы и томов данных.</span><span class="sxs-lookup"><span data-stu-id="d3aa6-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="d3aa6-108">Помимо состояния шифрования, в нем также отображаются секретный URL-адрес шифрования, URL-адрес ключа шифрования, идентификаторы ресурсов **KeyVaults** , в котором находится ключ шифрования и ключ шифрования для тома операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d3aa6-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="d3aa6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3aa6-109">EXAMPLES</span></span>

### <span data-ttu-id="d3aa6-110">Пример 1: получение состояния шифрования виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="d3aa6-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="d3aa6-111">Эта команда возвращает состояние шифрования виртуальной машины с именем VM001.</span><span class="sxs-lookup"><span data-stu-id="d3aa6-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="d3aa6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3aa6-112">PARAMETERS</span></span>

### <span data-ttu-id="d3aa6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3aa6-113">-DefaultProfile</span></span>
<span data-ttu-id="d3aa6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3aa6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3aa6-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="d3aa6-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="d3aa6-116">Имя издателя расширения.</span><span class="sxs-lookup"><span data-stu-id="d3aa6-116">The extension publisher name.</span></span> <span data-ttu-id="d3aa6-117">Указывайте этот параметр только для переопределения значения по умолчанию Microsoft. Azure. Security.</span><span class="sxs-lookup"><span data-stu-id="d3aa6-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3aa6-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="d3aa6-118">-ExtensionType</span></span>
<span data-ttu-id="d3aa6-119">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="d3aa6-119">The extension type.</span></span> <span data-ttu-id="d3aa6-120">Укажите этот параметр для переопределения значения по умолчанию "AzureDiskEncryption" для виртуальных машин и "AzureDiskEncryptionForLinux" для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="d3aa6-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3aa6-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d3aa6-121">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3aa6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3aa6-122">-ResourceGroupName</span></span>
<span data-ttu-id="d3aa6-123">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d3aa6-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d3aa6-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="d3aa6-124">-VMName</span></span>
<span data-ttu-id="d3aa6-125">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d3aa6-125">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3aa6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3aa6-126">CommonParameters</span></span>
<span data-ttu-id="d3aa6-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3aa6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3aa6-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3aa6-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3aa6-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3aa6-129">INPUTS</span></span>

### <span data-ttu-id="d3aa6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d3aa6-130">System.String</span></span>

## <span data-ttu-id="d3aa6-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3aa6-131">OUTPUTS</span></span>

### <span data-ttu-id="d3aa6-132">Microsoft. Azure. Commands. COMPUTE. extension. AzureDiskEncryption. AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="d3aa6-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="d3aa6-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3aa6-133">NOTES</span></span>

## <span data-ttu-id="d3aa6-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3aa6-134">RELATED LINKS</span></span>

[<span data-ttu-id="d3aa6-135">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="d3aa6-135">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="d3aa6-136">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="d3aa6-136">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)

