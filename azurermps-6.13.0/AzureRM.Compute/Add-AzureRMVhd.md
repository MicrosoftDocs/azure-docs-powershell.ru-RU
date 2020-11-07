---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRMVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRMVhd.md
ms.openlocfilehash: aee844d36fb2083e56415b34032cf928cb01d99e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567289"
---
# <span data-ttu-id="99b13-101">Add-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="99b13-101">Add-AzureRmVhd</span></span>

## <span data-ttu-id="99b13-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="99b13-102">SYNOPSIS</span></span>
<span data-ttu-id="99b13-103">Передача виртуального жесткого диска из локальной виртуальной машины в большой двоичный объект в учетной записи облачного хранилища в Azure.</span><span class="sxs-lookup"><span data-stu-id="99b13-103">Uploads a virtual hard disk from an on-premises virtual machine to a blob in a cloud storage account in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99b13-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="99b13-104">SYNTAX</span></span>

```
Add-AzureRmVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99b13-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99b13-105">DESCRIPTION</span></span>
<span data-ttu-id="99b13-106">Командлет **Add-AzureRmVhd** отправляет локальные виртуальные жесткие диски в формате VHD в учетную запись хранения BLOB как фиксированные виртуальные жесткие диски.</span><span class="sxs-lookup"><span data-stu-id="99b13-106">The **Add-AzureRmVhd** cmdlet uploads on-premises virtual hard disks, in .vhd file format, to a blob storage account as fixed virtual hard disks.</span></span>
<span data-ttu-id="99b13-107">Вы можете настроить количество потоков передачи данных, которые будут использоваться, или перезаписать существующий BLOB-объект в указанном URI назначения.</span><span class="sxs-lookup"><span data-stu-id="99b13-107">You can configure the number of uploader threads that will be used or overwrite an existing blob in the specified destination URI.</span></span>
<span data-ttu-id="99b13-108">Кроме того, поддерживается возможность отправки исправленной версии локального файла VHD.</span><span class="sxs-lookup"><span data-stu-id="99b13-108">Also supported is the ability to upload a patched version of an on-premises .vhd file.</span></span>
<span data-ttu-id="99b13-109">После отправки базового виртуального жесткого диска вы можете отправлять разностные диски, в которых в качестве родительских используются базовые образы.</span><span class="sxs-lookup"><span data-stu-id="99b13-109">When a base virtual hard disk has already been uploaded, you can upload differencing disks that use the base image as the parent.</span></span>
<span data-ttu-id="99b13-110">URI-адрес подписи общего доступа (SAS) также поддерживается.</span><span class="sxs-lookup"><span data-stu-id="99b13-110">Shared access signature (SAS) URI is supported also.</span></span>

## <span data-ttu-id="99b13-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="99b13-111">EXAMPLES</span></span>

### <span data-ttu-id="99b13-112">Пример 1: Добавление VHD-файла</span><span class="sxs-lookup"><span data-stu-id="99b13-112">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="99b13-113">Эта команда добавляет VHD-файл в учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="99b13-113">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="99b13-114">Пример 2: Добавление файла виртуального жесткого диска и переопределение места назначения</span><span class="sxs-lookup"><span data-stu-id="99b13-114">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="99b13-115">Эта команда добавляет VHD-файл в учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="99b13-115">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="99b13-116">Команда перезапишет существующий файл.</span><span class="sxs-lookup"><span data-stu-id="99b13-116">The command overwrites an existing file.</span></span>

### <span data-ttu-id="99b13-117">Пример 3: Добавление файла виртуального жесткого диска и указание количества потоков</span><span class="sxs-lookup"><span data-stu-id="99b13-117">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

<span data-ttu-id="99b13-118">Эта команда добавляет VHD-файл в учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="99b13-118">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="99b13-119">Команда задает количество потоков, используемых для отправки файла.</span><span class="sxs-lookup"><span data-stu-id="99b13-119">The command specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="99b13-120">Пример 4: Добавление файла виртуального жесткого диска и указание URI SAS</span><span class="sxs-lookup"><span data-stu-id="99b13-120">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="99b13-121">Эта команда добавляет VHD-файл в учетную запись хранения и определяет универсальный код ресурса (URI) SAS.</span><span class="sxs-lookup"><span data-stu-id="99b13-121">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="99b13-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="99b13-122">PARAMETERS</span></span>

### <span data-ttu-id="99b13-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99b13-123">-AsJob</span></span>
<span data-ttu-id="99b13-124">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="99b13-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="99b13-125">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="99b13-125">-BaseImageUriToPatch</span></span>
<span data-ttu-id="99b13-126">Задает универсальный код ресурса (URI) базового изображения в хранилище BLOB-объектов Azure.</span><span class="sxs-lookup"><span data-stu-id="99b13-126">Specifies the URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="99b13-127">В качестве значения этого параметра можно указать SAS.</span><span class="sxs-lookup"><span data-stu-id="99b13-127">An SAS can be specified as the value for this parameter.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b13-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99b13-128">-DefaultProfile</span></span>
<span data-ttu-id="99b13-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99b13-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99b13-130">-Destination</span><span class="sxs-lookup"><span data-stu-id="99b13-130">-Destination</span></span>
<span data-ttu-id="99b13-131">Задает универсальный код ресурса (URI) большого двоичного объекта в хранилище BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="99b13-131">Specifies the URI of a blob in Blob Storage.</span></span>
<span data-ttu-id="99b13-132">Параметр поддерживает URI SAS, хотя назначение сценариев для установки не может быть URI SAS.</span><span class="sxs-lookup"><span data-stu-id="99b13-132">The parameter supports SAS URI, although patching scenarios destination cannot be an SAS URI.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b13-133">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="99b13-133">-LocalFilePath</span></span>
<span data-ttu-id="99b13-134">Задает путь к локальному VHD-файлу.</span><span class="sxs-lookup"><span data-stu-id="99b13-134">Specifies the path of the local .vhd file.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b13-135">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="99b13-135">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="99b13-136">Указывает количество потоков данных, которые будут использоваться при загрузке VHD-файла.</span><span class="sxs-lookup"><span data-stu-id="99b13-136">Specifies the number of uploader threads to be used when uploading the .vhd file.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b13-137">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="99b13-137">-OverWrite</span></span>
<span data-ttu-id="99b13-138">Указывает на то, что этот командлет перезаписывает существующий большой двоичный объект в указанном URI назначения, если он существует.</span><span class="sxs-lookup"><span data-stu-id="99b13-138">Indicates that this cmdlet overwrites an existing blob in the specified destination URI, if one exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b13-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99b13-139">-ResourceGroupName</span></span>
<span data-ttu-id="99b13-140">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="99b13-140">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="99b13-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99b13-141">CommonParameters</span></span>
<span data-ttu-id="99b13-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="99b13-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99b13-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99b13-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99b13-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="99b13-144">INPUTS</span></span>

### <span data-ttu-id="99b13-145">System. String</span><span class="sxs-lookup"><span data-stu-id="99b13-145">System.String</span></span>

### <span data-ttu-id="99b13-146">System. URI</span><span class="sxs-lookup"><span data-stu-id="99b13-146">System.Uri</span></span>

### <span data-ttu-id="99b13-147">System. IO. FileInfo</span><span class="sxs-lookup"><span data-stu-id="99b13-147">System.IO.FileInfo</span></span>

### <span data-ttu-id="99b13-148">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="99b13-148">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="99b13-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="99b13-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="99b13-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="99b13-150">OUTPUTS</span></span>

### <span data-ttu-id="99b13-151">Microsoft. Azure. Commands. COMPUTE. Models. VhdUploadContext</span><span class="sxs-lookup"><span data-stu-id="99b13-151">Microsoft.Azure.Commands.Compute.Models.VhdUploadContext</span></span>

## <span data-ttu-id="99b13-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="99b13-152">NOTES</span></span>

## <span data-ttu-id="99b13-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99b13-153">RELATED LINKS</span></span>

[<span data-ttu-id="99b13-154">Сохранить — AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="99b13-154">Save-AzureRmVhd</span></span>](./Save-AzureRmVhd.md)

