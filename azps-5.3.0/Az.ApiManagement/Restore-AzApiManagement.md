---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/restore-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
ms.openlocfilehash: d99db4c9fe2c69e2177d9b35e15b49957e910014
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423287"
---
# <span data-ttu-id="7ed7f-101">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ed7f-101">Restore-AzApiManagement</span></span>

## <span data-ttu-id="7ed7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ed7f-102">SYNOPSIS</span></span>
<span data-ttu-id="7ed7f-103">Восстановление службы управления API из указанного BLOB-проекта хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7ed7f-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

## <span data-ttu-id="7ed7f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7ed7f-104">SYNTAX</span></span>

```
Restore-AzApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7ed7f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ed7f-105">DESCRIPTION</span></span>
<span data-ttu-id="7ed7f-106">**Cmdlet Restore-AzApiManagement** восстанавливает службу управления API из указанной резервной копии, которая находится в BLOB-проекте Azurestorage.</span><span class="sxs-lookup"><span data-stu-id="7ed7f-106">The **Restore-AzApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="7ed7f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7ed7f-107">EXAMPLES</span></span>

### <span data-ttu-id="7ed7f-108">Пример 1. Восстановление службы управления API</span><span class="sxs-lookup"><span data-stu-id="7ed7f-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="7ed7f-109">Эта команда восстанавливает службу управления API из BLOB-проекта хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7ed7f-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="7ed7f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ed7f-110">PARAMETERS</span></span>

### <span data-ttu-id="7ed7f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ed7f-111">-DefaultProfile</span></span>
<span data-ttu-id="7ed7f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7ed7f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ed7f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7ed7f-113">-Name</span></span>
<span data-ttu-id="7ed7f-114">Указывает имя экземпляра управления API, который будет восстановлен с помощью резервной копии.</span><span class="sxs-lookup"><span data-stu-id="7ed7f-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ed7f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ed7f-115">-PassThru</span></span>
<span data-ttu-id="7ed7f-116">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="7ed7f-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7ed7f-117">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="7ed7f-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7ed7f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ed7f-118">-ResourceGroupName</span></span>
<span data-ttu-id="7ed7f-119">Имя группы ресурсов, под которой находится управление API.</span><span class="sxs-lookup"><span data-stu-id="7ed7f-119">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ed7f-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="7ed7f-120">-SourceBlobName</span></span>
<span data-ttu-id="7ed7f-121">Имя BLOB-имени резервного копирования хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7ed7f-121">Specifies the name of the Azure storage backup source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ed7f-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="7ed7f-122">-SourceContainerName</span></span>
<span data-ttu-id="7ed7f-123">Имя контейнера источника резервной копии хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7ed7f-123">Specifies the name of the Azure storage backup source container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ed7f-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="7ed7f-124">-StorageContext</span></span>
<span data-ttu-id="7ed7f-125">Определяет контекст подключения к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="7ed7f-125">Specifies the storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ed7f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ed7f-126">CommonParameters</span></span>
<span data-ttu-id="7ed7f-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ed7f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ed7f-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ed7f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ed7f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ed7f-129">INPUTS</span></span>

### <span data-ttu-id="7ed7f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7ed7f-130">System.String</span></span>

## <span data-ttu-id="7ed7f-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7ed7f-131">OUTPUTS</span></span>

### <span data-ttu-id="7ed7f-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ed7f-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="7ed7f-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7ed7f-133">NOTES</span></span>

## <span data-ttu-id="7ed7f-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7ed7f-134">RELATED LINKS</span></span>

[<span data-ttu-id="7ed7f-135">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ed7f-135">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="7ed7f-136">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ed7f-136">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="7ed7f-137">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ed7f-137">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="7ed7f-138">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="7ed7f-138">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

