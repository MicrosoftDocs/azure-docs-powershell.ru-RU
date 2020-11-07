---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 5CEA7323-4CF7-42B2-BA94-BB3C8F73D2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaService.md
ms.openlocfilehash: 77ae2d0713f2b873f40e8335457683dcfbf5eafb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720372"
---
# <span data-ttu-id="1ac04-101">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1ac04-101">New-AzMediaService</span></span>

## <span data-ttu-id="1ac04-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1ac04-102">SYNOPSIS</span></span>
<span data-ttu-id="1ac04-103">Создание службы мультимедиа если служба мультимедиа уже существует, все ее свойства будут обновлены с учетом предоставленных входных данных.</span><span class="sxs-lookup"><span data-stu-id="1ac04-103">Creates a media service if the media service already exists, all its properties are updated with the input provided.</span></span>

## <span data-ttu-id="1ac04-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1ac04-104">SYNTAX</span></span>

### <span data-ttu-id="1ac04-105">StorageAccountIdParamSet</span><span class="sxs-lookup"><span data-stu-id="1ac04-105">StorageAccountIdParamSet</span></span>
```
New-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccountId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ac04-106">StorageAccountsParamSet</span><span class="sxs-lookup"><span data-stu-id="1ac04-106">StorageAccountsParamSet</span></span>
```
New-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccounts] <PSStorageAccount[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ac04-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ac04-107">DESCRIPTION</span></span>
<span data-ttu-id="1ac04-108">Командлет **New-AzMediaService** создает службу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1ac04-108">The **New-AzMediaService** cmdlet creates a media service.</span></span>
<span data-ttu-id="1ac04-109">Если служба мультимедиа уже существует, этот командлет обновит его свойства.</span><span class="sxs-lookup"><span data-stu-id="1ac04-109">If the media service already exists, this cmdlet update its properties.</span></span>

## <span data-ttu-id="1ac04-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1ac04-110">EXAMPLES</span></span>

### <span data-ttu-id="1ac04-111">Example1: создание службы мультимедиа только для основной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="1ac04-111">Example1: Create a media service with the primary storage account only</span></span>
```
PS C:\># Variables
## Global
$ResourceGroupName = "ResourceGroup001"
$Location = "East US"

## Storage
$StorageName = "Storage1"
$StorageType = "Standard_GRS"

## Media Service
$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
$MediaServiceName = "MediaService1"

# Resource Group
PS C:\> New-AzResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Location $Location -Type $StorageType

# Media Service
PS C:\> New-AzMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccountId $StorageAccount.Id -Tag $Tags
```

<span data-ttu-id="1ac04-112">В этом примере показано, как создать службу мультимедиа с указанием только основной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="1ac04-112">This example shows how to  create a media service with specifying primary storage account only.</span></span>
<span data-ttu-id="1ac04-113">Этот сценарий использует несколько других командлетов.</span><span class="sxs-lookup"><span data-stu-id="1ac04-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="1ac04-114">Пример 2: создание службы мультимедиа с несколькими хранилищами</span><span class="sxs-lookup"><span data-stu-id="1ac04-114">Example 2: Create a media service with multiple storage</span></span>
```
PS C:\># Variables

## Global
$ResourceGroupName = "ResourceGroup001"
$Location = "East US"

## Storage
$StorageName1 = "storage1"
$StorageName2 = "storage2"
$StorageType = "Standard_GRS"

## Media Service
$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
$MediaServiceName = "MediaService1"

# Resource Group
PS C:\> New-AzResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount1 = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName1 -Location $Location -Type $StorageType


$StorageAccount2 = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName2 -Location $Location -Type $StorageType

# Media Service

## Setup the storage configuration object.
PS C:\> $PrimaryStorageAccount = New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount1.Id -IsPrimary
PS C:\> $SecondaryStorageAccount = New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount2.Id
PS C:\> $StorageAccounts = @($PrimaryStorageAccount, $SecondaryStorageAccount)

## Create a media service.New-AzMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccounts $StorageAccounts -Tag $Tags
```

<span data-ttu-id="1ac04-115">В этом примере показано, как создать службу мультимедиа с несколькими учетными записями хранения.</span><span class="sxs-lookup"><span data-stu-id="1ac04-115">This example shows how to create a media service with multiple storage accounts.</span></span>
<span data-ttu-id="1ac04-116">Этот сценарий использует несколько других командлетов.</span><span class="sxs-lookup"><span data-stu-id="1ac04-116">This script uses several other cmdlets.</span></span>

## <span data-ttu-id="1ac04-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1ac04-117">PARAMETERS</span></span>

### <span data-ttu-id="1ac04-118">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="1ac04-118">-AccountName</span></span>
<span data-ttu-id="1ac04-119">Указывает имя службы мультимедиа, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="1ac04-119">Specifies the name of the media service that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac04-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ac04-120">-DefaultProfile</span></span>
<span data-ttu-id="1ac04-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1ac04-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ac04-122">-Location</span><span class="sxs-lookup"><span data-stu-id="1ac04-122">-Location</span></span>
<span data-ttu-id="1ac04-123">Указывает область, в которой этот командлет создает службу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1ac04-123">Specifies the region that this cmdlet creates the media service in.</span></span>

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

### <span data-ttu-id="1ac04-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ac04-124">-ResourceGroupName</span></span>
<span data-ttu-id="1ac04-125">Указывает имя группы ресурсов, которой назначена служба мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1ac04-125">Specifies the name of the resource group that the media service is assigned to.</span></span>

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

### <span data-ttu-id="1ac04-126">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1ac04-126">-StorageAccountId</span></span>
<span data-ttu-id="1ac04-127">Указывает учетную запись хранения, связанную с учетной записью службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1ac04-127">Specifies the storage account associated with the media service account.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageAccountIdParamSet
Aliases: Id

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac04-128">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="1ac04-128">-StorageAccounts</span></span>
<span data-ttu-id="1ac04-129">Указывает массив учетных записей хранения, которые нужно связать с службой мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1ac04-129">Specifies an array of storage accounts to associate with the media service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: StorageAccountsParamSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac04-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="1ac04-130">-Tag</span></span>
<span data-ttu-id="1ac04-131">Теги, связанные с учетной записью службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1ac04-131">The tags associated with the media service account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac04-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ac04-132">-Confirm</span></span>
<span data-ttu-id="1ac04-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1ac04-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac04-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ac04-134">-WhatIf</span></span>
<span data-ttu-id="1ac04-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1ac04-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ac04-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1ac04-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac04-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ac04-137">CommonParameters</span></span>
<span data-ttu-id="1ac04-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1ac04-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ac04-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ac04-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ac04-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1ac04-140">INPUTS</span></span>

### <span data-ttu-id="1ac04-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1ac04-141">System.String</span></span>

### <span data-ttu-id="1ac04-142">Microsoft. Azure. Commands. Media. Models. PSStorageAccount []</span><span class="sxs-lookup"><span data-stu-id="1ac04-142">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="1ac04-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ac04-143">OUTPUTS</span></span>

### <span data-ttu-id="1ac04-144">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="1ac04-144">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="1ac04-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="1ac04-145">NOTES</span></span>

## <span data-ttu-id="1ac04-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ac04-146">RELATED LINKS</span></span>

[<span data-ttu-id="1ac04-147">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1ac04-147">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="1ac04-148">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1ac04-148">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="1ac04-149">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1ac04-149">Set-AzMediaService</span></span>](./Set-AzMediaService.md)

