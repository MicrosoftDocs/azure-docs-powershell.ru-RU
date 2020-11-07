---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: 876d30cd3c046136acc24a8492425c69fc845f3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561623"
---
# <span data-ttu-id="92ba4-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="92ba4-101">Get-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="92ba4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92ba4-102">SYNOPSIS</span></span>
<span data-ttu-id="92ba4-103">Получение защищенных элементов в контейнере защиты ASR.</span><span class="sxs-lookup"><span data-stu-id="92ba4-103">Get the protectable items in an ASR protection container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92ba4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92ba4-104">SYNTAX</span></span>

### <span data-ttu-id="92ba4-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="92ba4-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92ba4-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="92ba4-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92ba4-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="92ba4-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectableItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92ba4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92ba4-108">DESCRIPTION</span></span>
<span data-ttu-id="92ba4-109">Командлет **Get-AzureRmRecoveryServicesAsrProtectableItem** получает защищенные элементы в контейнере защиты Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="92ba4-109">The **Get-AzureRmRecoveryServicesAsrProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="92ba4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92ba4-110">EXAMPLES</span></span>

### <span data-ttu-id="92ba4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="92ba4-111">Example 1</span></span>
```
PS C:\> $ProtectableItems = Get-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer $Container
```

<span data-ttu-id="92ba4-112">Получает все защищенные элементы в указанном контейнере защиты ASR.</span><span class="sxs-lookup"><span data-stu-id="92ba4-112">Gets all the protectable items in specified ASR protection container.</span></span>

### <span data-ttu-id="92ba4-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="92ba4-113">Example 2</span></span>
```
PS C:\> Get-ASRProtectableItem -ProtectionContainer $pc -FriendlyName $piFriendlyName

Disks                         : {}
FabricObjectId                :
FabricSpecificVMDetails       : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificVMDetails
FriendlyName                  : V2A-W2K12-400
ID                            : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replicationProt
                                ectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectableItems/22d47502-7df0-11e7-9373-0050568f2e8f
Name                          : 22d47502-7df0-11e7-9373-0050568f2e8f
OS                            : WINDOWS
OSDiskId                      :
OSDiskName                    :
ProtectionContainerId         : cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078
ProtectionReadinessErrors     :
ProtectionStatus              : Unprotected
ReplicationProtectedItemId    :
SupportedReplicationProviders : {InMage, InMageAzureV2}
```

<span data-ttu-id="92ba4-114">Получить защищенные элементы в указанном контейнере защиты ASR и с заданным понятным именем.</span><span class="sxs-lookup"><span data-stu-id="92ba4-114">Get the protectable items in specified ASR protection container and with given friendly name.</span></span>

### <span data-ttu-id="92ba4-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="92ba4-115">Example 3</span></span>
```
PS C:\> Get-ASRProtectableItem -ProtectionContainer $pc -Name $piName

Disks                         : {}
FabricObjectId                :
FabricSpecificVMDetails       : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificVMDetails
FriendlyName                  : V2A-W2K12-400
ID                            : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationFabrics/d011a5abf48190235963ee3a88ad188ee6bca8a4c6cd0c8d7ce5d439aa77ffd9/replicationProt
                                ectionContainers/cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078/replicationProtectableItems/22d47502-7df0-11e7-9373-0050568f2e8f
Name                          : 22d47502-7df0-11e7-9373-0050568f2e8f
OS                            : WINDOWS
OSDiskId                      :
OSDiskName                    :
ProtectionContainerId         : cloud_5dc96260-9f00-42e4-aca7-24ad27fc2078
ProtectionReadinessErrors     :
ProtectionStatus              : Unprotected
ReplicationProtectedItemId    :
SupportedReplicationProviders : {InMage, InMageAzureV2}
```

<span data-ttu-id="92ba4-116">Получает все защищенные элементы в указанном контейнере защиты ASR.</span><span class="sxs-lookup"><span data-stu-id="92ba4-116">Gets all the protectable items in specified ASR protection container.</span></span>

## <span data-ttu-id="92ba4-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92ba4-117">PARAMETERS</span></span>

### <span data-ttu-id="92ba4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92ba4-118">-DefaultProfile</span></span>
<span data-ttu-id="92ba4-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92ba4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="92ba4-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="92ba4-120">-FriendlyName</span></span>
<span data-ttu-id="92ba4-121">Указывает понятное имя защищенного элемента ASR.</span><span class="sxs-lookup"><span data-stu-id="92ba4-121">Specifies the friendly name of the ASR protectable item.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92ba4-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="92ba4-122">-Name</span></span>
<span data-ttu-id="92ba4-123">Указывает имя защищенного элемента ASR.</span><span class="sxs-lookup"><span data-stu-id="92ba4-123">Specifies the name of the ASR protectable item.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92ba4-124">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="92ba4-124">-ProtectionContainer</span></span>
<span data-ttu-id="92ba4-125">Указывает объект контейнера защиты Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="92ba4-125">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92ba4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92ba4-126">CommonParameters</span></span>
<span data-ttu-id="92ba4-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92ba4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92ba4-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92ba4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92ba4-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92ba4-129">INPUTS</span></span>

### <span data-ttu-id="92ba4-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="92ba4-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="92ba4-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92ba4-131">OUTPUTS</span></span>

### <span data-ttu-id="92ba4-132">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="92ba4-132">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="92ba4-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="92ba4-133">NOTES</span></span>

## <span data-ttu-id="92ba4-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92ba4-134">RELATED LINKS</span></span>

[<span data-ttu-id="92ba4-135">Get-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="92ba4-135">Get-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionEntity.md)

[<span data-ttu-id="92ba4-136">Set-AzureRmRecoveryServicesAsrProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="92ba4-136">Set-AzureRmRecoveryServicesAsrProtectionEntity</span></span>](./Set-AzureRmRecoveryServicesAsrProtectionEntity.md)