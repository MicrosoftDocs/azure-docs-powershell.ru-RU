---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
ms.openlocfilehash: efb570c22b5345b9d75fdf96dca061dc5cf7847f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565278"
---
# <span data-ttu-id="6d559-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="6d559-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="6d559-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d559-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d559-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d559-103">SYNTAX</span></span>

### <span data-ttu-id="6d559-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="6d559-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="6d559-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="6d559-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="6d559-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d559-106">DESCRIPTION</span></span>
<span data-ttu-id="6d559-107">Командлет **RESTORE-AzureRmWebAppBackup** восстанавливает резервную копию веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="6d559-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="6d559-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d559-108">EXAMPLES</span></span>

### <span data-ttu-id="6d559-109">1:</span><span class="sxs-lookup"><span data-stu-id="6d559-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="6d559-110">Восстанавливает резервную копию указанного ContosoWebApp приложения, который находится в группе ресурсов по умолчанию — Web-WestUS in BLOB "myBlob", расположенной в https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="6d559-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="6d559-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d559-111">PARAMETERS</span></span>

### <span data-ttu-id="6d559-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6d559-112">-AppServicePlan</span></span>
<span data-ttu-id="6d559-113">Имя плана служб приложений для восстановленного приложения.</span><span class="sxs-lookup"><span data-stu-id="6d559-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="6d559-114">Если оставить это поле пустым, используется текущий план служб приложений приложения.</span><span class="sxs-lookup"><span data-stu-id="6d559-114">If left empty, the app's current App Service Plan is used.</span></span>

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

### <span data-ttu-id="6d559-115">-BlobName</span><span class="sxs-lookup"><span data-stu-id="6d559-115">-BlobName</span></span>
<span data-ttu-id="6d559-116">Имя BLOB-объекта</span><span class="sxs-lookup"><span data-stu-id="6d559-116">Blob Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d559-117">-Базы данных</span><span class="sxs-lookup"><span data-stu-id="6d559-117">-Databases</span></span>
<span data-ttu-id="6d559-118">Базы данных типа DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="6d559-118">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d559-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d559-119">-DefaultProfile</span></span>
<span data-ttu-id="6d559-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d559-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d559-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="6d559-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="6d559-122">Параметр "игнорировать конфликтующие HostName"</span><span class="sxs-lookup"><span data-stu-id="6d559-122">Ignore Conflicting HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d559-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6d559-123">-Name</span></span>
<span data-ttu-id="6d559-124">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="6d559-124">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d559-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="6d559-125">-Overwrite</span></span>
<span data-ttu-id="6d559-126">Параметр перезаписи</span><span class="sxs-lookup"><span data-stu-id="6d559-126">Overwrite Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d559-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d559-127">-ResourceGroupName</span></span>
<span data-ttu-id="6d559-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6d559-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d559-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="6d559-129">-Slot</span></span>
<span data-ttu-id="6d559-130">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="6d559-130">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d559-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="6d559-131">-StorageAccountUrl</span></span>
<span data-ttu-id="6d559-132">URL-адрес учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="6d559-132">Storage Account Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d559-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6d559-133">-WebApp</span></span>
<span data-ttu-id="6d559-134">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="6d559-134">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d559-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d559-135">CommonParameters</span></span>
<span data-ttu-id="6d559-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d559-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d559-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d559-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d559-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d559-138">INPUTS</span></span>

### <span data-ttu-id="6d559-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6d559-139">System.String</span></span>

### <span data-ttu-id="6d559-140">Microsoft. Azure. Management. website. Models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="6d559-140">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

### <span data-ttu-id="6d559-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6d559-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="6d559-142">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="6d559-142">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="6d559-143">Параметры: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6d559-143">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="6d559-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d559-144">OUTPUTS</span></span>

### <span data-ttu-id="6d559-145">System. void</span><span class="sxs-lookup"><span data-stu-id="6d559-145">System.Void</span></span>

## <span data-ttu-id="6d559-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d559-146">NOTES</span></span>

## <span data-ttu-id="6d559-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d559-147">RELATED LINKS</span></span>