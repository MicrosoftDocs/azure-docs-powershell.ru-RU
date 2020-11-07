---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
ms.openlocfilehash: 9478e4892d4d7effdf37b7312f82348a2e8ea03a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721182"
---
# <span data-ttu-id="bf468-101">New-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="bf468-101">New-AzDataShareDataSet</span></span>

## <span data-ttu-id="bf468-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bf468-102">SYNOPSIS</span></span>
<span data-ttu-id="bf468-103">Добавляет наборы данных в общий доступ к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="bf468-103">Adds data sets to azure data share.</span></span>

## <span data-ttu-id="bf468-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bf468-104">SYNTAX</span></span>

### <span data-ttu-id="bf468-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bf468-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSet [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf468-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="bf468-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -Container <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf468-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf468-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -FileSystem <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf468-108">ByAdlsGen1DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf468-108">ByAdlsGen1DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> [-FileName <String>] -AdlsGen1FolderPath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf468-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf468-109">DESCRIPTION</span></span>
<span data-ttu-id="bf468-110">Командлет **New-AzDataShareDataSet** добавьте наборы данных в общий доступ к данным Azure учетной записи общего доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="bf468-110">The **New-AzDataShareDataSet** cmdlet add data sets in azure data share of data share account.</span></span> <span data-ttu-id="bf468-111">Вы можете добавлять наборы данных типа BLOB, ADLS Gen2 и ADLS Gen1.</span><span class="sxs-lookup"><span data-stu-id="bf468-111">You can add data sets of type Blob, ADLS Gen2 and ADLS Gen1.</span></span>

## <span data-ttu-id="bf468-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bf468-112">EXAMPLES</span></span>

### <span data-ttu-id="bf468-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bf468-113">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSet -ResourceroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="bf468-114">Эта команда добавляет набор данных с именем AdsDataSet контейнера больших двоичных объектов в Azure Data Share AdsShare.</span><span class="sxs-lookup"><span data-stu-id="bf468-114">This command adds a dataset named AdsDataSet of type blob container to azure data share AdsShare.</span></span>

## <span data-ttu-id="bf468-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bf468-115">PARAMETERS</span></span>

### <span data-ttu-id="bf468-116">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="bf468-116">-AccountName</span></span>
<span data-ttu-id="bf468-117">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="bf468-117">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf468-118">-AdlsGen1FolderPath</span><span class="sxs-lookup"><span data-stu-id="bf468-118">-AdlsGen1FolderPath</span></span>
<span data-ttu-id="bf468-119">Путь к папке ADLS Gen1 хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="bf468-119">Azure storage ADLS gen1 folder path</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf468-120">-Container</span><span class="sxs-lookup"><span data-stu-id="bf468-120">-Container</span></span>
<span data-ttu-id="bf468-121">Имя контейнера учетной записи службы хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="bf468-121">Azure storage account container name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf468-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf468-122">-DefaultProfile</span></span>
<span data-ttu-id="bf468-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bf468-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf468-124">-FileName</span><span class="sxs-lookup"><span data-stu-id="bf468-124">-FileName</span></span>
<span data-ttu-id="bf468-125">ADLS Gen1 имя файла хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="bf468-125">Azure storage ADLS gen1 file name</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen1DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf468-126">-FilePath</span><span class="sxs-lookup"><span data-stu-id="bf468-126">-FilePath</span></span>
<span data-ttu-id="bf468-127">Путь к файлу хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="bf468-127">Azure storage file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf468-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="bf468-128">-FileSystem</span></span>
<span data-ttu-id="bf468-129">Имя файловой системы для Azure ADLS Gen2</span><span class="sxs-lookup"><span data-stu-id="bf468-129">Azure ADLS gen2 file system name</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf468-130">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="bf468-130">-FolderPath</span></span>
<span data-ttu-id="bf468-131">Путь к папке хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="bf468-131">Azure storage folder path</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf468-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bf468-132">-Name</span></span>
<span data-ttu-id="bf468-133">Имя Set данных Azure</span><span class="sxs-lookup"><span data-stu-id="bf468-133">Azure data set name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf468-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf468-134">-ResourceGroupName</span></span>
<span data-ttu-id="bf468-135">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="bf468-135">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf468-136">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="bf468-136">-ShareName</span></span>
<span data-ttu-id="bf468-137">Имя общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="bf468-137">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf468-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="bf468-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="bf468-139">ResourceId для учетной записи хранения Azure</span><span class="sxs-lookup"><span data-stu-id="bf468-139">Azure storage account resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf468-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf468-140">-Confirm</span></span>
<span data-ttu-id="bf468-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bf468-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf468-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf468-142">-WhatIf</span></span>
<span data-ttu-id="bf468-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bf468-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf468-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bf468-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf468-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf468-145">CommonParameters</span></span>
<span data-ttu-id="bf468-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bf468-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf468-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf468-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf468-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bf468-148">INPUTS</span></span>

### <span data-ttu-id="bf468-149">System. String</span><span class="sxs-lookup"><span data-stu-id="bf468-149">System.String</span></span>

## <span data-ttu-id="bf468-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf468-150">OUTPUTS</span></span>

### <span data-ttu-id="bf468-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="bf468-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="bf468-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="bf468-152">NOTES</span></span>

## <span data-ttu-id="bf468-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf468-153">RELATED LINKS</span></span>