---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: d79a717fcf5d2422f86df4184d9c0344ebc32d28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568695"
---
# <span data-ttu-id="11320-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="11320-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="11320-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="11320-102">SYNOPSIS</span></span>
<span data-ttu-id="11320-103">Получает доступные (обнаруженные) классификации хранилища ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="11320-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11320-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="11320-104">SYNTAX</span></span>

### <span data-ttu-id="11320-105">ByFabricObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="11320-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="11320-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="11320-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="11320-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="11320-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [<CommonParameters>]
```

## <span data-ttu-id="11320-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11320-108">DESCRIPTION</span></span>
<span data-ttu-id="11320-109">Командлет **Get-AzureRmRecoveryServicesAsrStorageClassification** получает сведения о обнаруженных классификациях хранилища ASR в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="11320-109">The **Get-AzureRmRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="11320-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="11320-110">EXAMPLES</span></span>

### <span data-ttu-id="11320-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="11320-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="11320-112">Перечислите обнаруженные классификации хранилища, соответствующие указанной структуре ASR.</span><span class="sxs-lookup"><span data-stu-id="11320-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="11320-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="11320-113">PARAMETERS</span></span>

### <span data-ttu-id="11320-114">-Fabric</span><span class="sxs-lookup"><span data-stu-id="11320-114">-Fabric</span></span>
<span data-ttu-id="11320-115">Указывает объект Fabric ASR.</span><span class="sxs-lookup"><span data-stu-id="11320-115">Specifies an ASR fabric object.</span></span> <span data-ttu-id="11320-116">Командлет получает подробные сведения о обнаруженных классификациях хранилища, соответствующих указанной структуре ASR.</span><span class="sxs-lookup"><span data-stu-id="11320-116">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11320-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="11320-117">-FriendlyName</span></span>
<span data-ttu-id="11320-118">Указывает понятное имя объекта классификации хранилища, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="11320-118">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="11320-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="11320-119">-Name</span></span>
<span data-ttu-id="11320-120">Указывает имя объекта классификации хранилища, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="11320-120">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="11320-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11320-121">CommonParameters</span></span>
<span data-ttu-id="11320-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="11320-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11320-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11320-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11320-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="11320-124">INPUTS</span></span>

### <span data-ttu-id="11320-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="11320-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="11320-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="11320-126">OUTPUTS</span></span>

### <span data-ttu-id="11320-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="11320-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="11320-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="11320-128">NOTES</span></span>

## <span data-ttu-id="11320-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11320-129">RELATED LINKS</span></span>
