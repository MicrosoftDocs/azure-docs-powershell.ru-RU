---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothubimportdevices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubImportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubImportDevices.md
ms.openlocfilehash: 84b8224c83e6455e7f59b8a5fe2b330f34e61ac5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563488"
---
# <span data-ttu-id="b49ef-101">New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="b49ef-101">New-AzureRmIotHubImportDevices</span></span>

## <span data-ttu-id="b49ef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b49ef-102">SYNOPSIS</span></span>
<span data-ttu-id="b49ef-103">Создает новое задание "импорт устройств".</span><span class="sxs-lookup"><span data-stu-id="b49ef-103">Creates a new import devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b49ef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b49ef-104">SYNTAX</span></span>

```
New-AzureRmIotHubImportDevices [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b49ef-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b49ef-105">DESCRIPTION</span></span>
<span data-ttu-id="b49ef-106">Создает новое задание "импорт устройств" для IotHub.</span><span class="sxs-lookup"><span data-stu-id="b49ef-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="b49ef-107">Это приведет к импорту всех устройств в IotHub из указанного контейнера.</span><span class="sxs-lookup"><span data-stu-id="b49ef-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="b49ef-108">Обратитесь к следующей статье о том, как создать URI SAS.</span><span class="sxs-lookup"><span data-stu-id="b49ef-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="b49ef-109"> https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span><span class="sxs-lookup"><span data-stu-id="b49ef-109">https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span></span>

## <span data-ttu-id="b49ef-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b49ef-110">EXAMPLES</span></span>

### <span data-ttu-id="b49ef-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b49ef-111">Example 1</span></span>
```
PS C:\> New-AzureRmIotHubImportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="b49ef-112">Создает новый запрос на импорт устройства для IotHub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="b49ef-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="b49ef-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b49ef-113">PARAMETERS</span></span>

### <span data-ttu-id="b49ef-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b49ef-114">-DefaultProfile</span></span>
<span data-ttu-id="b49ef-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b49ef-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b49ef-116">-InputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="b49ef-116">-InputBlobContainerUri</span></span>
<span data-ttu-id="b49ef-117">URI контейнера BLOB-объектов ввода для FileUpload</span><span class="sxs-lookup"><span data-stu-id="b49ef-117">Input Blob Container Uri for FileUpload</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b49ef-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b49ef-118">-Name</span></span>
<span data-ttu-id="b49ef-119">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="b49ef-119">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b49ef-120">-OutputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="b49ef-120">-OutputBlobContainerUri</span></span>
<span data-ttu-id="b49ef-121">Универсальный код ресурса (URI) для записи выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b49ef-121">The Uri to write the output to.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b49ef-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b49ef-122">-ResourceGroupName</span></span>
<span data-ttu-id="b49ef-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b49ef-123">Resource Group Name</span></span>

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

### <span data-ttu-id="b49ef-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b49ef-124">-Confirm</span></span>
<span data-ttu-id="b49ef-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b49ef-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b49ef-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b49ef-126">-WhatIf</span></span>
<span data-ttu-id="b49ef-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b49ef-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b49ef-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b49ef-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b49ef-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b49ef-129">CommonParameters</span></span>
<span data-ttu-id="b49ef-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b49ef-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b49ef-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b49ef-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b49ef-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b49ef-132">INPUTS</span></span>

### <span data-ttu-id="b49ef-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b49ef-133">System.String</span></span>

## <span data-ttu-id="b49ef-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b49ef-134">OUTPUTS</span></span>

### <span data-ttu-id="b49ef-135">Microsoft. Azure. Management. IotHub. Models. JobResponse</span><span class="sxs-lookup"><span data-stu-id="b49ef-135">Microsoft.Azure.Management.IotHub.Models.JobResponse</span></span>

## <span data-ttu-id="b49ef-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="b49ef-136">NOTES</span></span>

## <span data-ttu-id="b49ef-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b49ef-137">RELATED LINKS</span></span>
