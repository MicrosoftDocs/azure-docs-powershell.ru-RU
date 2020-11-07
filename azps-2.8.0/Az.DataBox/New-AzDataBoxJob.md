---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/new-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
ms.openlocfilehash: c88365a64c9102b74811fedb2d93e103346e5a50
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721571"
---
# <span data-ttu-id="12e2e-101">New-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="12e2e-101">New-AzDataBoxJob</span></span>

## <span data-ttu-id="12e2e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="12e2e-102">SYNOPSIS</span></span>
<span data-ttu-id="12e2e-103">Создает новое задание databox с использованием указанных параметров.</span><span class="sxs-lookup"><span data-stu-id="12e2e-103">Creates a new databox job using the specified parameters</span></span>

## <span data-ttu-id="12e2e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="12e2e-104">SYNTAX</span></span>

```
New-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 -Location <String> [-AddressType <AddressType>] [-CompanyName <String>] -StreetAddress1 <String>
 [-StreetAddress2 <String>] [-StreetAddress3 <String>] -PostalCode <String> -City <String>
 -StateOrProvinceCode <String> -CountryCode <String> -EmailId <String[]> -PhoneNumber <String>
 -ContactName <String> -StorageAccountResourceId <String[]> -DataBoxType <String>
 [-ExpectedDataSizeInTeraBytes <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12e2e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12e2e-105">DESCRIPTION</span></span>
<span data-ttu-id="12e2e-106">Командлет **New-AzDataBoxJob** используется для создания нового задания databox, указав сведения, необходимые для создания задания.</span><span class="sxs-lookup"><span data-stu-id="12e2e-106">The **New-AzDataBoxJob** cmdlet is used to create a new databox job by specifying the details required for the creation of the job.</span></span>

## <span data-ttu-id="12e2e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="12e2e-107">EXAMPLES</span></span>

### <span data-ttu-id="12e2e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="12e2e-108">Example 1</span></span>
```powershell
PS C:\> $s1 = <Storage Account Resource Id>
PS C:\> New-AzDataBoxJob -Location 'WestUS' -StreetAddress1 '16 TOWNSEND ST' -PostalCode 94107 -City 'San Francisco' -StateOrProvinceCode 'CA' -CountryCode 'US' -EmailId 'abc@outlook.com' -PhoneNumber 1234567891 -ContactName 'John' -StorageAccount $s1 -DataBoxType DataBox -ResourceGroupName TestRg -Name OrderTest

jobResource.Name jobResource.Sku.Name jobResource.Status jobResource.StartTime jobResource.Location ResourceGroup
---------------- -------------------- ------------------ --------------------- -------------------- -------------
OrderTest       DataBox              DeviceOrdered      05-07-2019 05:25:30   westus               TestRg
```

<span data-ttu-id="12e2e-109">Командлет берет все необходимые параметры и некоторые необязательные параметры для создания задания databox.</span><span class="sxs-lookup"><span data-stu-id="12e2e-109">The cmdlet takes all the required parameters and some optional parameters to create the databox job.</span></span>

## <span data-ttu-id="12e2e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="12e2e-110">PARAMETERS</span></span>

### <span data-ttu-id="12e2e-111">-AddressType</span><span class="sxs-lookup"><span data-stu-id="12e2e-111">-AddressType</span></span>
<span data-ttu-id="12e2e-112">Тип адреса.</span><span class="sxs-lookup"><span data-stu-id="12e2e-112">Type of Address.</span></span> <span data-ttu-id="12e2e-113">Доступные значения: AddressType. None (по умолчанию), AddressType. жилых, AddressType. Коммерческий</span><span class="sxs-lookup"><span data-stu-id="12e2e-113">Available values : AddressType.None (default), AddressType.Residential, AddressType.Commercial</span></span>

```yaml
Type: Microsoft.Azure.Management.DataBox.Models.AddressType
Parameter Sets: (All)
Aliases:
Accepted values: None, Residential, Commercial

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e2e-114">-Город</span><span class="sxs-lookup"><span data-stu-id="12e2e-114">-City</span></span>
<span data-ttu-id="12e2e-115">Название города.</span><span class="sxs-lookup"><span data-stu-id="12e2e-115">Name of the City.</span></span> <span data-ttu-id="12e2e-116">Пример: Сан – Франциско</span><span class="sxs-lookup"><span data-stu-id="12e2e-116">Ex : San Francisco</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e2e-117">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="12e2e-117">-CompanyName</span></span>
<span data-ttu-id="12e2e-118">Название компании</span><span class="sxs-lookup"><span data-stu-id="12e2e-118">Name of the company</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e2e-119">-ContactName</span><span class="sxs-lookup"><span data-stu-id="12e2e-119">-ContactName</span></span>
<span data-ttu-id="12e2e-120">Имя контакта</span><span class="sxs-lookup"><span data-stu-id="12e2e-120">Contact Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e2e-121">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="12e2e-121">-CountryCode</span></span>
<span data-ttu-id="12e2e-122">Код страны.</span><span class="sxs-lookup"><span data-stu-id="12e2e-122">Country Code.</span></span> <span data-ttu-id="12e2e-123">Пример: US</span><span class="sxs-lookup"><span data-stu-id="12e2e-123">Ex: US</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e2e-124">-DataBoxType</span><span class="sxs-lookup"><span data-stu-id="12e2e-124">-DataBoxType</span></span>
<span data-ttu-id="12e2e-125">Тип SKU Databox.</span><span class="sxs-lookup"><span data-stu-id="12e2e-125">Sku type of Databox.</span></span>  <span data-ttu-id="12e2e-126">Доступные значения: DataBoxDisk, Databox, DataBoxHeavy</span><span class="sxs-lookup"><span data-stu-id="12e2e-126">Available values : DataBoxDisk, Databox, DataBoxHeavy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DataBoxDisk, Databox, DataBoxHeavy

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e2e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e2e-127">-DefaultProfile</span></span>
<span data-ttu-id="12e2e-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="12e2e-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12e2e-129">-EmailId</span><span class="sxs-lookup"><span data-stu-id="12e2e-129">-EmailId</span></span>
<span data-ttu-id="12e2e-130">Может быть указан список EmailIds.</span><span class="sxs-lookup"><span data-stu-id="12e2e-130">List of EmailIds can be provided.</span></span> <span data-ttu-id="12e2e-131">Хотя бы один является обязательным</span><span class="sxs-lookup"><span data-stu-id="12e2e-131">Atleast one is mandatory</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e2e-132">-ExpectedDataSizeInTeraBytes</span><span class="sxs-lookup"><span data-stu-id="12e2e-132">-ExpectedDataSizeInTeraBytes</span></span>
<span data-ttu-id="12e2e-133">В DataBoxDisk заказе указывается, что ожидаемые данные в терабайтах являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="12e2e-133">For DataBoxDisk order, specifying the expected data in terabytes is mandatory.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e2e-134">-Location</span><span class="sxs-lookup"><span data-stu-id="12e2e-134">-Location</span></span>
<span data-ttu-id="12e2e-135">Расположение подписки</span><span class="sxs-lookup"><span data-stu-id="12e2e-135">Location of the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e2e-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="12e2e-136">-Name</span></span>
<span data-ttu-id="12e2e-137">Имя создаваемого задания databox</span><span class="sxs-lookup"><span data-stu-id="12e2e-137">Name of the databox job to be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e2e-138">-Заданный</span><span class="sxs-lookup"><span data-stu-id="12e2e-138">-PhoneNumber</span></span>
<span data-ttu-id="12e2e-139">Номер контакта</span><span class="sxs-lookup"><span data-stu-id="12e2e-139">Contact Number</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e2e-140">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="12e2e-140">-PostalCode</span></span>
<span data-ttu-id="12e2e-141">Почтовый индекс</span><span class="sxs-lookup"><span data-stu-id="12e2e-141">Postal Code</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e2e-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12e2e-142">-ResourceGroupName</span></span>
<span data-ttu-id="12e2e-143">Имя группы ресурсов, в которой должно быть создано задание databox.</span><span class="sxs-lookup"><span data-stu-id="12e2e-143">Resource Group Name under which the databox job has to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e2e-144">-StateOrProvinceCode</span><span class="sxs-lookup"><span data-stu-id="12e2e-144">-StateOrProvinceCode</span></span>
<span data-ttu-id="12e2e-145">Введите код области или Республики.</span><span class="sxs-lookup"><span data-stu-id="12e2e-145">Input the state or province code.</span></span> <span data-ttu-id="12e2e-146">Например, CA — Калифорния; Флорида — Флорида; Нью-Йорк</span><span class="sxs-lookup"><span data-stu-id="12e2e-146">Like CA - California; FL - Florida; NY - New York</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e2e-147">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="12e2e-147">-StorageAccountResourceId</span></span>
<span data-ttu-id="12e2e-148">Список идентификаторов ресурсов для учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="12e2e-148">List of Resource Ids of Storage Accounts.</span></span> <span data-ttu-id="12e2e-149">По крайней мере один является обязательным.</span><span class="sxs-lookup"><span data-stu-id="12e2e-149">Atleast one is mandatory.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12e2e-150">-StreetAddress1</span><span class="sxs-lookup"><span data-stu-id="12e2e-150">-StreetAddress1</span></span>
<span data-ttu-id="12e2e-151">Почтовый адрес</span><span class="sxs-lookup"><span data-stu-id="12e2e-151">Street Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e2e-152">-StreetAddress2</span><span class="sxs-lookup"><span data-stu-id="12e2e-152">-StreetAddress2</span></span>
<span data-ttu-id="12e2e-153">Дополнительный почтовый адрес</span><span class="sxs-lookup"><span data-stu-id="12e2e-153">Additional Street Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e2e-154">-StreetAddress3</span><span class="sxs-lookup"><span data-stu-id="12e2e-154">-StreetAddress3</span></span>
<span data-ttu-id="12e2e-155">Дополнительный почтовый адрес</span><span class="sxs-lookup"><span data-stu-id="12e2e-155">Additional Street Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e2e-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12e2e-156">-Confirm</span></span>
<span data-ttu-id="12e2e-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="12e2e-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12e2e-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12e2e-158">-WhatIf</span></span>
<span data-ttu-id="12e2e-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="12e2e-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12e2e-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="12e2e-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12e2e-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e2e-161">CommonParameters</span></span>
<span data-ttu-id="12e2e-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="12e2e-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e2e-163">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12e2e-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e2e-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="12e2e-164">INPUTS</span></span>

### <span data-ttu-id="12e2e-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="12e2e-165">System.String[]</span></span>

## <span data-ttu-id="12e2e-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="12e2e-166">OUTPUTS</span></span>

### <span data-ttu-id="12e2e-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="12e2e-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="12e2e-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="12e2e-168">NOTES</span></span>

## <span data-ttu-id="12e2e-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12e2e-169">RELATED LINKS</span></span>