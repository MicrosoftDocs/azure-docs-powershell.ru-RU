---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
ms.openlocfilehash: cadcaccc2bb93dee5298ca92561c5bef36b5d9ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569611"
---
# <span data-ttu-id="f339d-101">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="f339d-101">Save-AzureRmVMImage</span></span>

## <span data-ttu-id="f339d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f339d-102">SYNOPSIS</span></span>
<span data-ttu-id="f339d-103">Сохранение виртуальной машины в виде VMImage.</span><span class="sxs-lookup"><span data-stu-id="f339d-103">Saves a virtual machine as a VMImage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f339d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f339d-104">SYNTAX</span></span>

### <span data-ttu-id="f339d-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f339d-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f339d-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f339d-106">IdParameterSetName</span></span>
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f339d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f339d-107">DESCRIPTION</span></span>
<span data-ttu-id="f339d-108">Командлет **Save-AzureRmVMImage** сохраняет виртуальную машину как VMImage.</span><span class="sxs-lookup"><span data-stu-id="f339d-108">The **Save-AzureRmVMImage** cmdlet saves a virtual machine as a VMImage.</span></span>
<span data-ttu-id="f339d-109">Перед созданием образа виртуальной машины выполните команду Sysprep для виртуальной машины, а затем пометьте ее как обобщенную с помощью командлета Set-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="f339d-109">Before you create a virtual machine image, sysprep the virtual machine, and then mark it as generalized by using the Set-AzureRmVM cmdlet.</span></span>

<span data-ttu-id="f339d-110">Результатом этого командлета является шаблон JSON (объектная нотация).</span><span class="sxs-lookup"><span data-stu-id="f339d-110">The output of this cmdlet is a JavaScript Object Notation (JSON) template.</span></span>
<span data-ttu-id="f339d-111">Вы можете развернуть виртуальные машины из записанного образа.</span><span class="sxs-lookup"><span data-stu-id="f339d-111">You can deploy virtual machines from your captured image.</span></span>

## <span data-ttu-id="f339d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f339d-112">EXAMPLES</span></span>

### <span data-ttu-id="f339d-113">Пример 1: запись виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="f339d-113">Example 1: Capture a virtual machine</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

<span data-ttu-id="f339d-114">Первая команда помечает виртуальную машину с именем VirtualMachine07 как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="f339d-114">The first command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

<span data-ttu-id="f339d-115">Вторая команда перехватывает виртуальную машину с именем VirtualMachine07 как VMImage.</span><span class="sxs-lookup"><span data-stu-id="f339d-115">The second command captures a virtual machine named VirtualMachine07 as a VMImage.</span></span>
<span data-ttu-id="f339d-116">Свойство **Output** ВОЗВРАЩАЕТ шаблон JSON.</span><span class="sxs-lookup"><span data-stu-id="f339d-116">The **Output** property returns a JSON template.</span></span>

## <span data-ttu-id="f339d-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f339d-117">PARAMETERS</span></span>

### <span data-ttu-id="f339d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f339d-118">-DefaultProfile</span></span>
<span data-ttu-id="f339d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f339d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f339d-120">-DestinationContainerName</span><span class="sxs-lookup"><span data-stu-id="f339d-120">-DestinationContainerName</span></span>
<span data-ttu-id="f339d-121">Указывает имя контейнера в контейнере System, который вы хотите хранить для изображений.</span><span class="sxs-lookup"><span data-stu-id="f339d-121">Specifies the name of a container inside the "system" container that you want to hold your images.</span></span>

<span data-ttu-id="f339d-122">Если контейнер не существует, он создается для вас.</span><span class="sxs-lookup"><span data-stu-id="f339d-122">If the container doesn't exist, it is created for you.</span></span>
<span data-ttu-id="f339d-123">Виртуальные жесткие диски (VHD), составляющие VMImage, находятся в контейнере, указанном в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="f339d-123">The virtual hard disks (VHDs) that constitute the VMImage reside in the container that this parameter specifies.</span></span>
<span data-ttu-id="f339d-124">Если виртуальные жесткие диски распределены между несколькими учетными записями хранения, этот командлет создает один контейнер с этим именем в каждой учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f339d-124">If the VHDs are spread across multiple storage accounts, this cmdlet creates one container that has this name in each storage account.</span></span>
<span data-ttu-id="f339d-125">URL-адрес сохраненного изображения подобен:</span><span class="sxs-lookup"><span data-stu-id="f339d-125">The URL of the saved image is similar to:</span></span> 

<span data-ttu-id="f339d-126"> HTTPS:// \<storageAccountName\> . BLOB.Core.Windows.NET/System/Microsoft.COMPUTE/Images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX. VHD.</span><span class="sxs-lookup"><span data-stu-id="f339d-126">https://\<storageAccountName\>.blob.core.windows.net/system/Microsoft.Compute/Images/\<imagesContainer\>/\<vhdPrefix-osDisk\>.xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.vhd.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f339d-127">-ID</span><span class="sxs-lookup"><span data-stu-id="f339d-127">-Id</span></span>
<span data-ttu-id="f339d-128">Указывает идентификатор ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f339d-128">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f339d-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f339d-129">-Name</span></span>
<span data-ttu-id="f339d-130">Задает имя.</span><span class="sxs-lookup"><span data-stu-id="f339d-130">Specifies a name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f339d-131">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="f339d-131">-Overwrite</span></span>
<span data-ttu-id="f339d-132">Указывает на то, что этот командлет перезаписывает все виртуальные жесткие диски с таким же префиксом в конечном контейнере.</span><span class="sxs-lookup"><span data-stu-id="f339d-132">Indicates that this cmdlet overwrites any VHDs that have the same prefix in the destination container.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f339d-133">-Path</span><span class="sxs-lookup"><span data-stu-id="f339d-133">-Path</span></span>
<span data-ttu-id="f339d-134">Указывает путь к виртуальному жесткому диску.</span><span class="sxs-lookup"><span data-stu-id="f339d-134">Specifies the path of the VHD.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f339d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f339d-135">-ResourceGroupName</span></span>
<span data-ttu-id="f339d-136">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f339d-136">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f339d-137">-VHDNamePrefix</span><span class="sxs-lookup"><span data-stu-id="f339d-137">-VHDNamePrefix</span></span>
<span data-ttu-id="f339d-138">Указывает префикс в имени больших двоичных объектов, составляющих профиль хранилища для VMImage.</span><span class="sxs-lookup"><span data-stu-id="f339d-138">Specifies the prefix in the name of the blobs that constitute the storage profile of the VMImage.</span></span>

<span data-ttu-id="f339d-139">Например, префикс vhdPrefix для диска операционной системы приводит к присвоению имени vhdPrefix-osdisk. \<guid\> . VHD.</span><span class="sxs-lookup"><span data-stu-id="f339d-139">For example, a prefix vhdPrefix for an operating system disk results in the name vhdPrefix-osdisk.\<guid\>.vhd.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f339d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f339d-140">CommonParameters</span></span>
<span data-ttu-id="f339d-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f339d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f339d-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f339d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f339d-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f339d-143">INPUTS</span></span>

## <span data-ttu-id="f339d-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f339d-144">OUTPUTS</span></span>

## <span data-ttu-id="f339d-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="f339d-145">NOTES</span></span>

## <span data-ttu-id="f339d-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f339d-146">RELATED LINKS</span></span>

[<span data-ttu-id="f339d-147">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="f339d-147">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="f339d-148">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="f339d-148">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="f339d-149">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f339d-149">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="f339d-150">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="f339d-150">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="f339d-151">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f339d-151">Set-AzureRmVM</span></span>](./Set-AzureRmVM.md)

