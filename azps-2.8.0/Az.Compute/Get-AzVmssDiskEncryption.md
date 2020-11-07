---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 5219b43a1d80515f0bce02c5f6fdd2117b736a00
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721883"
---
# <span data-ttu-id="8b59c-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="8b59c-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="8b59c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8b59c-102">SYNOPSIS</span></span>
<span data-ttu-id="8b59c-103">Показывает состояние шифрования диска для набора масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="8b59c-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="8b59c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8b59c-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b59c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b59c-105">DESCRIPTION</span></span>
<span data-ttu-id="8b59c-106">Показывает состояние шифрования диска для набора масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="8b59c-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="8b59c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8b59c-107">EXAMPLES</span></span>

### <span data-ttu-id="8b59c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b59c-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="8b59c-109">Показывает состояние шифрования диска, установленное для набора виртуальных машин с именем VMSS001, которое принадлежит группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="8b59c-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="8b59c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8b59c-110">PARAMETERS</span></span>

### <span data-ttu-id="8b59c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b59c-111">-DefaultProfile</span></span>
<span data-ttu-id="8b59c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b59c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b59c-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="8b59c-113">-ExtensionName</span></span>
<span data-ttu-id="8b59c-114">Имя расширения.</span><span class="sxs-lookup"><span data-stu-id="8b59c-114">The extension name.</span></span>
<span data-ttu-id="8b59c-115">Если этот параметр не указан, используются значения по умолчанию AzureDiskEncryption для ВМ и AzureDiskEncryptionForLinux для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="8b59c-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b59c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b59c-116">-ResourceGroupName</span></span>
<span data-ttu-id="8b59c-117">Имя группы ресурсов для набора шкал виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="8b59c-117">Resource group name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b59c-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8b59c-118">-VMScaleSetName</span></span>
<span data-ttu-id="8b59c-119">Имя множества шкал виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="8b59c-119">The virtual machine scale set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b59c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b59c-120">CommonParameters</span></span>
<span data-ttu-id="8b59c-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8b59c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b59c-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b59c-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b59c-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8b59c-123">INPUTS</span></span>

### <span data-ttu-id="8b59c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="8b59c-124">System.String</span></span>

## <span data-ttu-id="8b59c-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b59c-125">OUTPUTS</span></span>

### <span data-ttu-id="8b59c-126">Microsoft. Azure. Commands. COMPUTE. Models. PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="8b59c-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="8b59c-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="8b59c-127">NOTES</span></span>

## <span data-ttu-id="8b59c-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b59c-128">RELATED LINKS</span></span>