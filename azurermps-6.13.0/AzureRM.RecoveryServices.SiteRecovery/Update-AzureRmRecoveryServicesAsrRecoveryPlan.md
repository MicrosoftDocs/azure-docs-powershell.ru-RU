---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: eb42cdf74482a5161ab75df459c78d88749fde7e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564092"
---
# <span data-ttu-id="7684a-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7684a-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="7684a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7684a-102">SYNOPSIS</span></span>
<span data-ttu-id="7684a-103">Обновляет содержимое плана восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="7684a-103">Updates the contents of an Azure Site recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7684a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7684a-104">SYNTAX</span></span>

### <span data-ttu-id="7684a-105">ByRPObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7684a-105">ByRPObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7684a-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="7684a-106">ByRPFile</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7684a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7684a-107">DESCRIPTION</span></span>
<span data-ttu-id="7684a-108">Командлет **Update-AzureRmRecoveryServicesAsrRecoveryPlan** обновляет содержимое плана восстановления с помощью содержимого указанного объекта плана восстановления ASR или JSON-файла определения плана восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="7684a-108">The **Update-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="7684a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7684a-109">EXAMPLES</span></span>

### <span data-ttu-id="7684a-110">Пример 1: Обновление плана восстановления</span><span class="sxs-lookup"><span data-stu-id="7684a-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="7684a-111">Запуск операции обновления плана восстановления с помощью содержимого указанного объекта плана восстановления ASR и возврат задания ASR, используемого для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="7684a-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7684a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7684a-112">PARAMETERS</span></span>

### <span data-ttu-id="7684a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7684a-113">-DefaultProfile</span></span>
<span data-ttu-id="7684a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7684a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7684a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7684a-115">-InputObject</span></span>
<span data-ttu-id="7684a-116">Входной объект для командлета: определяет объект плана восстановления ASR, содержимое которого используется для обновления плана восстановления, на который ссылается объект.</span><span class="sxs-lookup"><span data-stu-id="7684a-116">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7684a-117">-Path</span><span class="sxs-lookup"><span data-stu-id="7684a-117">-Path</span></span>
<span data-ttu-id="7684a-118">Указывает путь JSON файла определения плана восстановления, используемого для обновления плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="7684a-118">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7684a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7684a-119">-Confirm</span></span>
<span data-ttu-id="7684a-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7684a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7684a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7684a-121">-WhatIf</span></span>
<span data-ttu-id="7684a-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7684a-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7684a-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7684a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7684a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7684a-124">CommonParameters</span></span>
<span data-ttu-id="7684a-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7684a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7684a-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7684a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7684a-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7684a-127">INPUTS</span></span>

### <span data-ttu-id="7684a-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7684a-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="7684a-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7684a-129">OUTPUTS</span></span>

### <span data-ttu-id="7684a-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="7684a-130">System.Object</span></span>

## <span data-ttu-id="7684a-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="7684a-131">NOTES</span></span>

## <span data-ttu-id="7684a-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7684a-132">RELATED LINKS</span></span>

[<span data-ttu-id="7684a-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7684a-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="7684a-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7684a-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="7684a-135">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7684a-135">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)