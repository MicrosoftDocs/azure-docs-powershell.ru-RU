---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: bc3704c3594826f19399c1967bbe86ed7f1e8773
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325475"
---
# <span data-ttu-id="325b1-101">Модуль Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="325b1-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="325b1-102">Описание</span><span class="sxs-lookup"><span data-stu-id="325b1-102">Description</span></span>
<span data-ttu-id="325b1-103">С помощью командлетов в модуле синхронизации хранилища вы можете управлять операциями, касающимися синхронизации файлов Azure в PowerShell.</span><span class="sxs-lookup"><span data-stu-id="325b1-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="325b1-104">Az.StorageSync Cmdlets</span><span class="sxs-lookup"><span data-stu-id="325b1-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="325b1-105">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="325b1-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="325b1-106">Эта команда содержит список всех облачных конечных точек в заданной группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="325b1-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="325b1-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="325b1-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="325b1-108">Эта команда содержит список всех групп синхронизации в заданной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="325b1-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="325b1-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="325b1-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="325b1-110">Эта команда содержит список всех серверов, зарегистрированных в данной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="325b1-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="325b1-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="325b1-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="325b1-112">Эта команда содержит список всех конечных точек сервера в заданной группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="325b1-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="325b1-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="325b1-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="325b1-114">Эта команда содержит список всех служб синхронизации хранилища в рамках группы подписок и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="325b1-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="325b1-115">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="325b1-115">Invoke-AzStorageSyncChangeDetection</span></span>](Invoke-AzStorageSyncChangeDetection.md)
<span data-ttu-id="325b1-116">Эту команду можно использовать для инициалов обнаружения изменений пространства имен вручную.</span><span class="sxs-lookup"><span data-stu-id="325b1-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="325b1-117">Его можно настроить для всей папки, вемеской папки или набора файлов.</span><span class="sxs-lookup"><span data-stu-id="325b1-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="325b1-118">Можно обнаружить не более 10 000 изменений.</span><span class="sxs-lookup"><span data-stu-id="325b1-118">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="325b1-119">Если известна область изменений, ограничьте выполнение этой команды частями пространства имен, чтобы обнаружение изменений можно было быстро завершить в пределах 10 000 изменений.</span><span class="sxs-lookup"><span data-stu-id="325b1-119">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

### [<span data-ttu-id="325b1-120">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="325b1-120">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="325b1-121">Проверяет наличие возможных проблем совместимости между системой и службой Azure File Sync.</span><span class="sxs-lookup"><span data-stu-id="325b1-121">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="325b1-122">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="325b1-122">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="325b1-123">Эта команда отзывит все многоуровневые файлы на локальный диск.</span><span class="sxs-lookup"><span data-stu-id="325b1-123">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="325b1-124">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="325b1-124">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="325b1-125">Эта команда создает облачную конечную точку синхронизации файлов Azure в группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="325b1-125">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="325b1-126">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="325b1-126">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="325b1-127">Эта команда создает новую группу синхронизации в указанной службе синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="325b1-127">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="325b1-128">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="325b1-128">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="325b1-129">Эта команда создает конечную точку сервера на зарегистрированном сервере.</span><span class="sxs-lookup"><span data-stu-id="325b1-129">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="325b1-130">Это позволяет заданный путь на сервере начать синхронизацию файлов с другими конечными точками в группе синхронизации.</span><span class="sxs-lookup"><span data-stu-id="325b1-130">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="325b1-131">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="325b1-131">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="325b1-132">Эта команда создает новую службу синхронизации хранилища в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="325b1-132">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="325b1-133">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="325b1-133">Set-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="325b1-134">Эта команда задает службу синхронизации хранилища в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="325b1-134">This command sets a storage sync service in a resource group.</span></span>

### [<span data-ttu-id="325b1-135">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="325b1-135">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="325b1-136">Эта команда регистрирует сервер в службе синхронизации хранилища, что создает отношение доверия.</span><span class="sxs-lookup"><span data-stu-id="325b1-136">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="325b1-137">Затем для настройки синхронизации на этом сервере можно использовать PowerShell или портал Azure.</span><span class="sxs-lookup"><span data-stu-id="325b1-137">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="325b1-138">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="325b1-138">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="325b1-139">Эта команда удаляет указанную конечную точку облака из группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="325b1-139">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="325b1-140">Без хотя бы одной облачной конечной точки другие конечные точки сервера в этой группе синхронизации не будут синхронизироваться.</span><span class="sxs-lookup"><span data-stu-id="325b1-140">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="325b1-141">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="325b1-141">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="325b1-142">Эта команда удалит указанную группу синхронизации.</span><span class="sxs-lookup"><span data-stu-id="325b1-142">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="325b1-143">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="325b1-143">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="325b1-144">Эта команда удалит указанную конечную точку сервера.</span><span class="sxs-lookup"><span data-stu-id="325b1-144">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="325b1-145">Синхронизация с этой расположением остановится немедленно.</span><span class="sxs-lookup"><span data-stu-id="325b1-145">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="325b1-146">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="325b1-146">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="325b1-147">Эта команда удалит указанную службу синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="325b1-147">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="325b1-148">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="325b1-148">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="325b1-149">Используется только для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="325b1-149">Use for troubleshooting only.</span></span> <span data-ttu-id="325b1-150">Эта команда позволит свернуть сертификат сервера синхронизации хранилища, используемый для описания идентификаторов сервера, в службу синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="325b1-150">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="325b1-151">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="325b1-151">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="325b1-152">Эта команда позволяет вносить изменения в настраиваемые параметры конечной точки сервера.</span><span class="sxs-lookup"><span data-stu-id="325b1-152">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="325b1-153">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="325b1-153">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="325b1-154">Предупреждение. Если отрегистрить сервер, это приведет к каскадным удалениям всех конечных точек сервера на этом сервере.</span><span class="sxs-lookup"><span data-stu-id="325b1-154">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="325b1-155">Эта команда отстранит сервер из его службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="325b1-155">This command will unregister a server from it's storage sync service.</span></span>
