---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7C695E83-78AA-4008-91D6-D6B23BC96B92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 5657701475e81b302d761193cd542ee38ea9c16e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565120"
---
# <span data-ttu-id="73d57-101">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="73d57-101">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="73d57-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="73d57-102">SYNOPSIS</span></span>
<span data-ttu-id="73d57-103">Удаляет план восстановления сайта из восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="73d57-103">Removes a site recovery plan from Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73d57-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="73d57-104">SYNTAX</span></span>

### <span data-ttu-id="73d57-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="73d57-105">ByObject (Default)</span></span>
```
Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73d57-106">ByName</span><span class="sxs-lookup"><span data-stu-id="73d57-106">ByName</span></span>
```
Remove-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73d57-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73d57-107">DESCRIPTION</span></span>
<span data-ttu-id="73d57-108">Командлет **Remove-AzureRmSiteRecoveryRecoveryPlan** удаляет план восстановления сайта из текущего восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="73d57-108">The **Remove-AzureRmSiteRecoveryRecoveryPlan** cmdlet removes a site recovery plan from the current Azure Site Recovery.</span></span>

## <span data-ttu-id="73d57-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="73d57-109">EXAMPLES</span></span>

### <span data-ttu-id="73d57-110">Пример 1: Удаление плана восстановления</span><span class="sxs-lookup"><span data-stu-id="73d57-110">Example 1: Remove a recovery plan</span></span>
```
PS C:\>$RecoveryPlan = Get-AzureRmSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="73d57-111">Первая команда использует командлет Get-AzureRmSiteRecoveryRecoveryPlan для получения плана восстановления сайта, а затем сохраняет его в переменной $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="73d57-111">The first command uses the Get-AzureRmSiteRecoveryRecoveryPlan cmdlet to get the Site Recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="73d57-112">Вторая команда удаляет план восстановления в $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="73d57-112">The second command removes the recovery plan in $RecoveryPlan.</span></span>

## <span data-ttu-id="73d57-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="73d57-113">PARAMETERS</span></span>

### <span data-ttu-id="73d57-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="73d57-114">-Name</span></span>
<span data-ttu-id="73d57-115">Указывает имя плана восстановления, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="73d57-115">Specifies the name of the recovery plan that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73d57-116">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="73d57-116">-RecoveryPlan</span></span>
<span data-ttu-id="73d57-117">Указывает план восстановления, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="73d57-117">Specifies the recovery plan that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73d57-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73d57-118">-DefaultProfile</span></span>
<span data-ttu-id="73d57-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73d57-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73d57-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73d57-120">CommonParameters</span></span>
<span data-ttu-id="73d57-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="73d57-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73d57-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73d57-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73d57-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="73d57-123">INPUTS</span></span>

### <span data-ttu-id="73d57-124">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="73d57-124">ASRRecoveryPlan</span></span>
<span data-ttu-id="73d57-125">Параметр "RecoveryPlan" принимает значение типа "ASRRecoveryPlan" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="73d57-125">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="73d57-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="73d57-126">OUTPUTS</span></span>

## <span data-ttu-id="73d57-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="73d57-127">NOTES</span></span>

## <span data-ttu-id="73d57-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73d57-128">RELATED LINKS</span></span>

[<span data-ttu-id="73d57-129">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="73d57-129">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="73d57-130">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="73d57-130">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="73d57-131">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="73d57-131">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)

