---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImageDataDisk.md
ms.openlocfilehash: 9727ef5520ed067a418e32a98e4a59bedefc84b6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721786"
---
# <span data-ttu-id="3598d-101">Remove-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="3598d-101">Remove-AzImageDataDisk</span></span>

## <span data-ttu-id="3598d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3598d-102">SYNOPSIS</span></span>
<span data-ttu-id="3598d-103">Удаляет диск с данными из объекта Image.</span><span class="sxs-lookup"><span data-stu-id="3598d-103">Removes a data disk from an image object.</span></span>

## <span data-ttu-id="3598d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3598d-104">SYNTAX</span></span>

```
Remove-AzImageDataDisk [-Image] <PSImage> [-Lun] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3598d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3598d-105">DESCRIPTION</span></span>
<span data-ttu-id="3598d-106">Командлет **Remove-AzImageDataDisk** удаляет диск с данными из объекта Image.</span><span class="sxs-lookup"><span data-stu-id="3598d-106">The **Remove-AzImageDataDisk** cmdlet removes a data disk from an image object.</span></span>

## <span data-ttu-id="3598d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3598d-107">EXAMPLES</span></span>

### <span data-ttu-id="3598d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3598d-108">Example 1</span></span>
```
PS C:\> Get-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzImageDataDisk -Lun 1 | Update-AzImage;
```

<span data-ttu-id="3598d-109">Эта команда удаляет диск данных логического устройства с номером 1 из существующего образа "image01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="3598d-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="3598d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3598d-110">PARAMETERS</span></span>

### <span data-ttu-id="3598d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3598d-111">-DefaultProfile</span></span>
<span data-ttu-id="3598d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3598d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3598d-113">-Image</span><span class="sxs-lookup"><span data-stu-id="3598d-113">-Image</span></span>
<span data-ttu-id="3598d-114">Указывает локальный объект изображения.</span><span class="sxs-lookup"><span data-stu-id="3598d-114">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3598d-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="3598d-115">-Lun</span></span>
<span data-ttu-id="3598d-116">Задает логический номер устройства (LUN).</span><span class="sxs-lookup"><span data-stu-id="3598d-116">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3598d-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3598d-117">-Confirm</span></span>
<span data-ttu-id="3598d-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3598d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3598d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3598d-119">-WhatIf</span></span>
<span data-ttu-id="3598d-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3598d-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3598d-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3598d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3598d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3598d-122">CommonParameters</span></span>
<span data-ttu-id="3598d-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3598d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3598d-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3598d-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3598d-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3598d-125">INPUTS</span></span>

### <span data-ttu-id="3598d-126">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="3598d-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="3598d-127">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3598d-127">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3598d-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3598d-128">OUTPUTS</span></span>

### <span data-ttu-id="3598d-129">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="3598d-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="3598d-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="3598d-130">NOTES</span></span>

## <span data-ttu-id="3598d-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3598d-131">RELATED LINKS</span></span>