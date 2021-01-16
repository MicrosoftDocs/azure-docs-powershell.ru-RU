---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: bde840903c53dae9ba47b9eb30634ce90f80ee9e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410527"
---
# <span data-ttu-id="a8eba-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a8eba-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="a8eba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8eba-102">SYNOPSIS</span></span>
<span data-ttu-id="a8eba-103">Включает репликацию для защищенного элемента ASR путем создания элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="a8eba-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

## <span data-ttu-id="a8eba-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a8eba-104">SYNTAX</span></span>

### <span data-ttu-id="a8eba-105">EnterpriseToEnterprise (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a8eba-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8eba-106">VMwareToAzureWithDiskType</span><span class="sxs-lookup"><span data-stu-id="a8eba-106">VMwareToAzureWithDiskType</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] -DiskType <String> [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8eba-107">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="a8eba-107">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-InMageAzureV2DiskInput <AsrInMageAzureV2DiskInput[]>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8eba-108">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="a8eba-108">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8eba-109">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="a8eba-109">HyperVSiteToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8eba-110">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="a8eba-110">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DiskEncryptionVaultId <String>]
 [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>] [-KeyEncryptionVaultId <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8eba-111">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="a8eba-111">AzureToAzureWithoutDiskDetails</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure] -AzureVmId <String> -Name <String>
 [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureStorageAccountId <String>] -LogStorageAccountId <String> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-RecoveryAvailabilityZone <String>] [-RecoveryProximityPlacementGroupId <String>]
 [-RecoveryAvailabilitySetId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8eba-112">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8eba-112">DESCRIPTION</span></span>
<span data-ttu-id="a8eba-113">Для создания нового элемента, защищенного репликацией, создается новый элемент, защищенный службой **AzRecoveryServicesAsrReplicationProtectedItem.**</span><span class="sxs-lookup"><span data-stu-id="a8eba-113">The **New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="a8eba-114">Используйте этот cmdlet, чтобы включить репликацию для защищенного элемента ASR.</span><span class="sxs-lookup"><span data-stu-id="a8eba-114">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="a8eba-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a8eba-115">EXAMPLES</span></span>

### <span data-ttu-id="a8eba-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a8eba-116">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="a8eba-117">Запускает операцию создания элемента, защищенного репликацией, для указанного защищенного элемента ASR и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="a8eba-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="a8eba-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a8eba-118">Example 2</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] `
-RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name `
-ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm `
-RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

<span data-ttu-id="a8eba-119">Запускает операцию создания элемента, защищенного репликацией, для указанного защищенного элемента ASR и возвращает задание ASR, используемое для отслеживания операции (сценарий vmWare в Azure).</span><span class="sxs-lookup"><span data-stu-id="a8eba-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="a8eba-120">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a8eba-120">Example 3</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="a8eba-121">Запускает операцию создания элемента, защищенного репликацией, для указанного защищенного элемента ASR и возвращает задание ASR, используемое для отслеживания операции (сценарий Azure в Azure).</span><span class="sxs-lookup"><span data-stu-id="a8eba-121">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="a8eba-122">Пример 4</span><span class="sxs-lookup"><span data-stu-id="a8eba-122">Example 4</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -RecoveryAzureNetworkId $RecoveryAzureNetworkId -RecoveryAzureSubnetName $RecoveryAzureSubnetName
```

<span data-ttu-id="a8eba-123">Запускает операцию создания защищенных репликацией элементов для указанного VmId и возвращает задание ASR, используемую для отслеживания операции (сценарий Azure в Azure).</span><span class="sxs-lookup"><span data-stu-id="a8eba-123">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="a8eba-124">Пример 5</span><span class="sxs-lookup"><span data-stu-id="a8eba-124">Example 5</span></span>
```
PS C:\>$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
PS C:\>$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2

PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

<span data-ttu-id="a8eba-125">Запускает операцию создания элемента, защищенного репликацией, для указанного защищенного элемента ASR, включая выборочные диски, и возвращает задание ASR, используемое для отслеживания операции (сценарий vmWare в Azure) с выбранными дисками.</span><span class="sxs-lookup"><span data-stu-id="a8eba-125">Starts the replication protected item creation operation for the specified ASR protectable item including selective disks and returns the ASR job used to track the operation(vmWare to Azure scenario) with selected disks.</span></span>

### <span data-ttu-id="a8eba-126">Пример 6</span><span class="sxs-lookup"><span data-stu-id="a8eba-126">Example 6</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -DiskType Standard_LRS

Starts the replication protected item creation operation for the specified ASR protectable item with default disk type and returns the ASR job used to track the operation(vmWare to Azure scenario).
```

### <span data-ttu-id="a8eba-127">Пример 7</span><span class="sxs-lookup"><span data-stu-id="a8eba-127">Example 7</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="a8eba-128">Запускает операцию создания защищенных репликацией элементов для указанного VmId и возвращает задание ASR, используемую для отслеживания операции (сценарий Azure в Azure). Для отбойной VM-информации, переданной в cmdlet для шифрования, будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="a8eba-128">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).For the failover VM details passed in cmdlet for encryption will be used .</span></span>

### <span data-ttu-id="a8eba-129">Пример 8</span><span class="sxs-lookup"><span data-stu-id="a8eba-129">Example 8</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="a8eba-130">Запускает операцию создания защищенных репликацией элементов для виртуальной машины внутри группы расположения близости и возвращает задание ASR, используемую для отслеживания операции (сценарий От Azure к Azure).</span><span class="sxs-lookup"><span data-stu-id="a8eba-130">Starts the replication protected item creation operation for a Virtual Machine inside Proximity placement group and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="a8eba-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8eba-131">PARAMETERS</span></span>

### <span data-ttu-id="a8eba-132">-Account</span><span class="sxs-lookup"><span data-stu-id="a8eba-132">-Account</span></span>
<span data-ttu-id="a8eba-133">Запустите как учетную запись, которая будет использоваться для push-установки службы мобильной установки при необходимости.</span><span class="sxs-lookup"><span data-stu-id="a8eba-133">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="a8eba-134">Должен быть в списке "Выполнить как учетные записи" в материале ASR.</span><span class="sxs-lookup"><span data-stu-id="a8eba-134">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-135">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="a8eba-135">-AzureToAzure</span></span>
<span data-ttu-id="a8eba-136">Параметр переключения указывает, что нужно создать реплицированный элемент в сценарии Azure.</span><span class="sxs-lookup"><span data-stu-id="a8eba-136">Switch parameter specifies creating the replicated item in azure to azure scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-137">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8eba-137">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="a8eba-138">Определяет конфигурацию диска, которая используется в сценарии аварийного восстановления VM для Azure.</span><span class="sxs-lookup"><span data-stu-id="a8eba-138">Specifies the disk configuration to used Vm for Azure to Azure disaster recovery scenario.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-139">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="a8eba-139">-AzureVmId</span></span>
<span data-ttu-id="a8eba-140">Указывает VM-id Azure для защиты от аварийного восстановления в регионе восстановления.</span><span class="sxs-lookup"><span data-stu-id="a8eba-140">Specifies the Azure VM id for disaster recovery protection in recovery region.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8eba-141">-DefaultProfile</span></span>
<span data-ttu-id="a8eba-142">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a8eba-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a8eba-143">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="a8eba-143">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="a8eba-144">Указывает секретный URL-адрес шифрования диска с версией (шифрованием диска Azure), который будет использоваться для восстановления VM после отбойного канала.</span><span class="sxs-lookup"><span data-stu-id="a8eba-144">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-145">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="a8eba-145">-DiskEncryptionSetId</span></span>
<span data-ttu-id="a8eba-146">Определяет код ресурса набора шифрования диска, который будет использоваться для шифрования управляемых дисков.</span><span class="sxs-lookup"><span data-stu-id="a8eba-146">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-147">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="a8eba-147">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="a8eba-148">Определяет код секретного сейфа шифрования диска (шифрование диска Azure), который будет использоваться для восстановления VM после отбойного сбойа.</span><span class="sxs-lookup"><span data-stu-id="a8eba-148">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-149">-DiskType</span><span class="sxs-lookup"><span data-stu-id="a8eba-149">-DiskType</span></span>
<span data-ttu-id="a8eba-150">Определяет тип диска для восстановления VM.</span><span class="sxs-lookup"><span data-stu-id="a8eba-150">Specifies the Recovery VM managed disk type.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="a8eba-151">-HyperVToAzure</span></span>
<span data-ttu-id="a8eba-152">Параметр переключения для указания реплицируемых элементов является виртуальной машиной Hyper-V, которая реплицируется в Azure.</span><span class="sxs-lookup"><span data-stu-id="a8eba-152">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-153">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="a8eba-153">-IncludeDiskId</span></span>
<span data-ttu-id="a8eba-154">Список дисков для репликации.</span><span class="sxs-lookup"><span data-stu-id="a8eba-154">The list of disks to include for replication.</span></span> <span data-ttu-id="a8eba-155">По умолчанию включены все диски.</span><span class="sxs-lookup"><span data-stu-id="a8eba-155">By default all disks are included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-156">-InMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="a8eba-156">-InMageAzureV2DiskInput</span></span>
<span data-ttu-id="a8eba-157">Определяет конфигурацию диска, вводимую для защиты от указанного защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="a8eba-157">Specifies the disk configuration input for vMWare disk id to protect from specified protectable item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput[]
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-158">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="a8eba-158">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="a8eba-159">Указывает URL-адрес ключа шифрования диска с версией (шифрованием диска Azure), который будет использоваться для восстановления VM после отбойного сбойа.</span><span class="sxs-lookup"><span data-stu-id="a8eba-159">Specifies the disk encryption key URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-160">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="a8eba-160">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="a8eba-161">Определяет код хранилища ключей ключа шифрования диска (шифрование диска Azure), который будет использоваться для восстановления VM после отбойной системы.</span><span class="sxs-lookup"><span data-stu-id="a8eba-161">Specifies the disk encryption key key-vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-162">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a8eba-162">-LogStorageAccountId</span></span>
<span data-ttu-id="a8eba-163">Определяет ИД учетной записи хранения журнала или кэша, который будет использоваться для хранения журналов репликации.</span><span class="sxs-lookup"><span data-stu-id="a8eba-163">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-164">-Name</span><span class="sxs-lookup"><span data-stu-id="a8eba-164">-Name</span></span>
<span data-ttu-id="a8eba-165">Указывает имя элемента, защищенного репликацией ASR.</span><span class="sxs-lookup"><span data-stu-id="a8eba-165">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="a8eba-166">Имя должно быть уникальным в пределах сейфа.</span><span class="sxs-lookup"><span data-stu-id="a8eba-166">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="a8eba-167">-OS</span><span class="sxs-lookup"><span data-stu-id="a8eba-167">-OS</span></span>
<span data-ttu-id="a8eba-168">Определяет семейство операционных систем.</span><span class="sxs-lookup"><span data-stu-id="a8eba-168">Specifies the operating system family.</span></span>
<span data-ttu-id="a8eba-169">Допустимыми значениями для этого параметра являются: Windows или Linux.</span><span class="sxs-lookup"><span data-stu-id="a8eba-169">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-170">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="a8eba-170">-OSDiskName</span></span>
<span data-ttu-id="a8eba-171">Указывает имя диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a8eba-171">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-172">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="a8eba-172">-ProcessServer</span></span>
<span data-ttu-id="a8eba-173">Сервер обработки, который будет использовать для репликации этого компьютера.</span><span class="sxs-lookup"><span data-stu-id="a8eba-173">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="a8eba-174">Чтобы указать сервер, используйте список серверов процессов в материале ASR, который соответствует серверу Конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a8eba-174">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-175">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a8eba-175">-ProtectableItem</span></span>
<span data-ttu-id="a8eba-176">Определяет объект защищенного элемента ASR, для которого включена репликация.</span><span class="sxs-lookup"><span data-stu-id="a8eba-176">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-177">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="a8eba-177">-ProtectionContainerMapping</span></span>
<span data-ttu-id="a8eba-178">Определяет объект сопоставления контейнера защиты ASR, соответствующий политике репликации, которая будет использоваться для репликации.</span><span class="sxs-lookup"><span data-stu-id="a8eba-178">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-179">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="a8eba-179">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="a8eba-180">ИД AvailabilitySet, который нужно восстановить на компьютере в случае отостановки.</span><span class="sxs-lookup"><span data-stu-id="a8eba-180">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-181">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="a8eba-181">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="a8eba-182">Определяет зону доступности VM для восстановления после отбойного процесса.</span><span class="sxs-lookup"><span data-stu-id="a8eba-182">Specifies the recovery VM availability zone after failover.</span></span>


```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-183">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="a8eba-183">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="a8eba-184">ИД виртуальной сети Azure, который нужно восстановить на компьютере в случае отсеев.</span><span class="sxs-lookup"><span data-stu-id="a8eba-184">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-185">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a8eba-185">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="a8eba-186">Определяет ИД учетной записи хранения Azure, на который нужно реплицировать.</span><span class="sxs-lookup"><span data-stu-id="a8eba-186">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-187">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="a8eba-187">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="a8eba-188">Подсеть в сети восстановления виртуальной сети Azure, в которую в случае сбойного работы на виртуальной машине был вложен сбой.</span><span class="sxs-lookup"><span data-stu-id="a8eba-188">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-189">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a8eba-189">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="a8eba-190">Указывает учетную запись хранения для диагностики загрузки для восстановления Azure VM.</span><span class="sxs-lookup"><span data-stu-id="a8eba-190">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-191">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="a8eba-191">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="a8eba-192">Определяет ИД ресурса облачной службы восстановления, для который эта виртуальная машине будет перенаправиться на эту виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="a8eba-192">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-193">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="a8eba-193">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="a8eba-194">Укажите ИД группы расположения близости, который будет использоваться VM-сбойом в целевом регионе восстановления.</span><span class="sxs-lookup"><span data-stu-id="a8eba-194">Specify the proximity placement group Id to used by the failover Vm in target recovery region.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-195">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="a8eba-195">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="a8eba-196">Определяет идентификатор ARM группы ресурсов, в которой будет создана виртуальная машину в случае отбойного сбойа.</span><span class="sxs-lookup"><span data-stu-id="a8eba-196">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-197">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="a8eba-197">-RecoveryVmName</span></span>
<span data-ttu-id="a8eba-198">Имя VM-части восстановления, созданной после отбойного процесса.</span><span class="sxs-lookup"><span data-stu-id="a8eba-198">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-199">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="a8eba-199">-ReplicationGroupName</span></span>
<span data-ttu-id="a8eba-200">Указывает имя группы репликации, используемой для создания точек восстановления с несколькими VM-данными.</span><span class="sxs-lookup"><span data-stu-id="a8eba-200">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="a8eba-201">По умолчанию каждый элемент, защищенный репликацией, создается в отдельной группе, и не создаются согласованные точки восстановления с несколькими VM-копиями.</span><span class="sxs-lookup"><span data-stu-id="a8eba-201">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="a8eba-202">Используйте этот параметр только в том случае, если вам нужно создать согласованные точки восстановления с несколькими VM-устройствами для группы компьютеров, защищив все компьютеры с одной и той же группой репликации.</span><span class="sxs-lookup"><span data-stu-id="a8eba-202">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-203">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="a8eba-203">-VmmToVmm</span></span>
<span data-ttu-id="a8eba-204">Параметр переключения для указания реплицированный элемент является виртуальной машиной Hyper-V, которая реплицируется между сайтами VMM Managed Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="a8eba-204">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-205">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="a8eba-205">-VMwareToAzure</span></span>
<span data-ttu-id="a8eba-206">Параметр переключения, чтобы указать реплицированный элемент, является виртуальной машиной VMware или физическим сервером, который будет реплицироваться в Azure.</span><span class="sxs-lookup"><span data-stu-id="a8eba-206">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8eba-207">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="a8eba-207">-WaitForCompletion</span></span>
<span data-ttu-id="a8eba-208">Указывает, что перед возвратом cmdlet должен дождаться завершения операции.</span><span class="sxs-lookup"><span data-stu-id="a8eba-208">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="a8eba-209">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8eba-209">-Confirm</span></span>
<span data-ttu-id="a8eba-210">Запрос на подтверждение перед началом операции.</span><span class="sxs-lookup"><span data-stu-id="a8eba-210">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="a8eba-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8eba-211">-WhatIf</span></span>
<span data-ttu-id="a8eba-212">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8eba-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8eba-213">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a8eba-213">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8eba-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8eba-214">CommonParameters</span></span>
<span data-ttu-id="a8eba-215">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8eba-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8eba-216">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8eba-216">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8eba-217">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8eba-217">INPUTS</span></span>

### <span data-ttu-id="a8eba-218">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a8eba-218">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="a8eba-219">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a8eba-219">OUTPUTS</span></span>

### <span data-ttu-id="a8eba-220">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="a8eba-220">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a8eba-221">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a8eba-221">NOTES</span></span>

## <span data-ttu-id="a8eba-222">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8eba-222">RELATED LINKS</span></span>

[<span data-ttu-id="a8eba-223">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a8eba-223">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="a8eba-224">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a8eba-224">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="a8eba-225">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a8eba-225">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)