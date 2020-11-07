---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
ms.openlocfilehash: 39ee23006490ce1dfbca1387a1e058df49850c5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721670"
---
# <span data-ttu-id="9352d-101">Set-AzVMPlan</span><span class="sxs-lookup"><span data-stu-id="9352d-101">Set-AzVMPlan</span></span>

## <span data-ttu-id="9352d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9352d-102">SYNOPSIS</span></span>
<span data-ttu-id="9352d-103">Задает сведения о плане рынка на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="9352d-103">Sets the Marketplace plan information on a virtual machine.</span></span>

## <span data-ttu-id="9352d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9352d-104">SYNTAX</span></span>

```
Set-AzVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9352d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9352d-105">DESCRIPTION</span></span>
<span data-ttu-id="9352d-106">Командлет **Set-AzVMPlan** задает сведения о плане Azure Marketplace для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9352d-106">The **Set-AzVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>
<span data-ttu-id="9352d-107">Прежде чем развертывать изображение Marketplace с помощью командной строки, необходимо включить программный доступ или выполнить развертывание виртуальной машины с помощью портала Azure.</span><span class="sxs-lookup"><span data-stu-id="9352d-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="9352d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9352d-108">EXAMPLES</span></span>

## <span data-ttu-id="9352d-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9352d-109">PARAMETERS</span></span>

### <span data-ttu-id="9352d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9352d-110">-DefaultProfile</span></span>
<span data-ttu-id="9352d-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9352d-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9352d-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9352d-112">-Name</span></span>
<span data-ttu-id="9352d-113">Указывает имя изображения из Marketplace.</span><span class="sxs-lookup"><span data-stu-id="9352d-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="9352d-114">Это то же значение, которое возвращает командлет Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="9352d-114">This is the same value that is returned by the Get-AzVMImageSku cmdlet.</span></span>
<span data-ttu-id="9352d-115">Дополнительные сведения о поиске изображений можно найти в разделе Навигация и выбор образов виртуальных машин Azure с помощью PowerShell и инфраструктуры Azure CLI https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ ( https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) в документации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9352d-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9352d-116">-Product</span><span class="sxs-lookup"><span data-stu-id="9352d-116">-Product</span></span>
<span data-ttu-id="9352d-117">Определяет произведение изображения на рынке.</span><span class="sxs-lookup"><span data-stu-id="9352d-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="9352d-118">Это та же информация, что и значение **предложения** элемента **imageReference** .</span><span class="sxs-lookup"><span data-stu-id="9352d-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

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

### <span data-ttu-id="9352d-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="9352d-119">-PromotionCode</span></span>
<span data-ttu-id="9352d-120">Указывает код рекламной акции.</span><span class="sxs-lookup"><span data-stu-id="9352d-120">Specifies a promotion code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9352d-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="9352d-121">-Publisher</span></span>
<span data-ttu-id="9352d-122">Указывает издателя изображения.</span><span class="sxs-lookup"><span data-stu-id="9352d-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="9352d-123">Эти сведения можно найти с помощью командлета Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="9352d-123">You can find this information by using the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9352d-124">-VM</span><span class="sxs-lookup"><span data-stu-id="9352d-124">-VM</span></span>
<span data-ttu-id="9352d-125">Указывает объект виртуальной машины, для которого нужно задать план Marketplace.</span><span class="sxs-lookup"><span data-stu-id="9352d-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="9352d-126">Вы можете использовать командлет Get-AzVM для получения объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9352d-126">You can use the Get-AzVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="9352d-127">Вы можете использовать командлет New-AzVMConfig для создания объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9352d-127">You can use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9352d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9352d-128">CommonParameters</span></span>
<span data-ttu-id="9352d-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9352d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9352d-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9352d-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9352d-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9352d-131">INPUTS</span></span>

### <span data-ttu-id="9352d-132">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9352d-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="9352d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9352d-133">System.String</span></span>

## <span data-ttu-id="9352d-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9352d-134">OUTPUTS</span></span>

### <span data-ttu-id="9352d-135">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9352d-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="9352d-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="9352d-136">NOTES</span></span>

## <span data-ttu-id="9352d-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9352d-137">RELATED LINKS</span></span>

[<span data-ttu-id="9352d-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="9352d-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="9352d-139">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9352d-139">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="9352d-140">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="9352d-140">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="9352d-141">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="9352d-141">New-AzVMConfig</span></span>](./New-AzVMConfig.md)