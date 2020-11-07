---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: bafa671431c617807fa28e2d4fbfed57236fc6a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564103"
---
# <span data-ttu-id="d9b7e-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d9b7e-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="d9b7e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d9b7e-102">SYNOPSIS</span></span>
<span data-ttu-id="d9b7e-103">Удаляет указанное сопоставление классификации хранилища ASR.</span><span class="sxs-lookup"><span data-stu-id="d9b7e-103">Deletes the specified ASR storage classification mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9b7e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d9b7e-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9b7e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9b7e-105">DESCRIPTION</span></span>
<span data-ttu-id="d9b7e-106">Командлет **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** удаляет указанное сопоставление классификации хранилища для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="d9b7e-106">The **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="d9b7e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d9b7e-107">EXAMPLES</span></span>

### <span data-ttu-id="d9b7e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d9b7e-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="d9b7e-109">Запускает удаление указанного сопоставления классификации хранилища и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="d9b7e-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d9b7e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d9b7e-110">PARAMETERS</span></span>

### <span data-ttu-id="d9b7e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9b7e-111">-DefaultProfile</span></span>
<span data-ttu-id="d9b7e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d9b7e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d9b7e-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9b7e-113">-InputObject</span></span>
<span data-ttu-id="d9b7e-114">Входной объект для командлета: объект сопоставления классификации хранилища ASR, соответствующий сопоставлению классификации хранилища ASR, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d9b7e-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9b7e-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9b7e-115">-Confirm</span></span>
<span data-ttu-id="d9b7e-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d9b7e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9b7e-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9b7e-117">-WhatIf</span></span>
<span data-ttu-id="d9b7e-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d9b7e-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9b7e-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d9b7e-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9b7e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9b7e-120">CommonParameters</span></span>
<span data-ttu-id="d9b7e-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d9b7e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9b7e-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9b7e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9b7e-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d9b7e-123">INPUTS</span></span>

### <span data-ttu-id="d9b7e-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d9b7e-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="d9b7e-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9b7e-125">OUTPUTS</span></span>

### <span data-ttu-id="d9b7e-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d9b7e-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d9b7e-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="d9b7e-127">NOTES</span></span>

## <span data-ttu-id="d9b7e-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9b7e-128">RELATED LINKS</span></span>

[<span data-ttu-id="d9b7e-129">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d9b7e-129">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="d9b7e-130">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d9b7e-130">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)