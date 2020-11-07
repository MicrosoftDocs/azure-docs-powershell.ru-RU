---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9FF4F649-F50C-4C27-842F-1CD6C5BC7A2B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
ms.openlocfilehash: 1cb5ccf56a2ef6888231ca81df0e352f5d505e7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559971"
---
# <span data-ttu-id="7abb1-101">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="7abb1-101">Backup-AzureRmBackupItem</span></span>

## <span data-ttu-id="7abb1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7abb1-102">SYNOPSIS</span></span>
<span data-ttu-id="7abb1-103">Запуск резервного копирования для элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="7abb1-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7abb1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7abb1-104">SYNTAX</span></span>

```
Backup-AzureRmBackupItem [-Item] <AzureRMBackupItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7abb1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7abb1-105">DESCRIPTION</span></span>
<span data-ttu-id="7abb1-106">Командлет **BACKUP-AzureRmBackupItem** запускает резервное копирование для защищенного элемента резервного копирования Azure, не привязанного к расписанию резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="7abb1-106">The **Backup-AzureRmBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="7abb1-107">Вы можете выполнить начальную архивацию немедленно, после того как вы включите защиту или начнете создание резервной копии после сбоя архивации по расписанию.</span><span class="sxs-lookup"><span data-stu-id="7abb1-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>

<span data-ttu-id="7abb1-108">При выполнении существующего задания резервного копирования этот командлет завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="7abb1-108">If an existing backup job is running, this cmdlet fails.</span></span>

## <span data-ttu-id="7abb1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7abb1-109">EXAMPLES</span></span>

### <span data-ttu-id="7abb1-110">Пример 1: Начало создания резервной копии виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="7abb1-110">Example 1: Start to back up a virtual machine</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container | Backup-AzureRmBackupItem
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
```

<span data-ttu-id="7abb1-111">Первая команда получает хранилище с именем Vault03 с помощью командлета Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="7abb1-111">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="7abb1-112">Команда сохраняет этот объект в переменной $Vault.</span><span class="sxs-lookup"><span data-stu-id="7abb1-112">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="7abb1-113">Вторая команда получает контейнер с указанным именем в хранилище $Vault с помощью командлета Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="7abb1-113">The second command gets a container that has the specified name in the vault in $Vault by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="7abb1-114">Команда сохраняет этот объект в переменной $Container.</span><span class="sxs-lookup"><span data-stu-id="7abb1-114">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="7abb1-115">Последняя команда получает элементы резервного копирования в $Container с помощью командлета Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="7abb1-115">The last command gets the backup items in $Container by using the Get-AzureRmBackupItem cmdlet.</span></span>
<span data-ttu-id="7abb1-116">Команда передает элементы в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="7abb1-116">The command passes the items to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7abb1-117">Текущий командлет запускает резервное копирование виртуальной машины в контейнере.</span><span class="sxs-lookup"><span data-stu-id="7abb1-117">The current cmdlet starts backing up the virtual machine in the container.</span></span>

## <span data-ttu-id="7abb1-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7abb1-118">PARAMETERS</span></span>

### <span data-ttu-id="7abb1-119">-Item</span><span class="sxs-lookup"><span data-stu-id="7abb1-119">-Item</span></span>
<span data-ttu-id="7abb1-120">Указывает элемент резервного копирования, для которого этот командлет запускает операцию резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="7abb1-120">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7abb1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7abb1-121">-DefaultProfile</span></span>
<span data-ttu-id="7abb1-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7abb1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7abb1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7abb1-123">CommonParameters</span></span>
<span data-ttu-id="7abb1-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7abb1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7abb1-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7abb1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7abb1-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7abb1-126">INPUTS</span></span>

### <span data-ttu-id="7abb1-127">AzureRMBackupItem</span><span class="sxs-lookup"><span data-stu-id="7abb1-127">AzureRMBackupItem</span></span>

## <span data-ttu-id="7abb1-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7abb1-128">OUTPUTS</span></span>

### <span data-ttu-id="7abb1-129">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="7abb1-129">AzureRmBackupJob</span></span>

## <span data-ttu-id="7abb1-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="7abb1-130">NOTES</span></span>

## <span data-ttu-id="7abb1-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7abb1-131">RELATED LINKS</span></span>

[<span data-ttu-id="7abb1-132">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="7abb1-132">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="7abb1-133">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="7abb1-133">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="7abb1-134">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="7abb1-134">Restore-AzureRmBackupItem</span></span>](./Restore-AzureRmBackupItem.md)

