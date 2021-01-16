---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: c871d8620e8c4507ec972f3888babfd259ede172
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506796"
---
# <span data-ttu-id="d5648-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d5648-101">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="d5648-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5648-102">SYNOPSIS</span></span>
<span data-ttu-id="d5648-103">Создает сопоставление контейнера azure Site Recovery Protection Container, связывая указанную политику репликации с указанным контейнером защиты asR.</span><span class="sxs-lookup"><span data-stu-id="d5648-103">Creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified ASR protection container.</span></span>

## <span data-ttu-id="d5648-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d5648-104">SYNTAX</span></span>

### <span data-ttu-id="d5648-105">EnterpriseToAzure (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d5648-105">EnterpriseToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5648-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="d5648-106">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5648-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5648-107">DESCRIPTION</span></span>
<span data-ttu-id="d5648-108">С помощью cmdlet **New-AzRecoveryServicesAsrProtectionContainerMapping** создается сопоставление контейнера Azure Site Recovery Protection Container, связывая указанную политику репликации с указанным контейнером защиты.</span><span class="sxs-lookup"><span data-stu-id="d5648-108">The **New-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating the specified replication policy to the specified protection container.</span></span>

## <span data-ttu-id="d5648-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d5648-109">EXAMPLES</span></span>

### <span data-ttu-id="d5648-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d5648-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectionContainerMapping -Name $ContainerMappingName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer

Name             : 1f32fee1-05d0-4c11-a997-1618e14b4dab
ID               : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationJobs/1f32fee1-05d0-4c11-a997-1618e14b4dab
Type             :
JobType          :
DisplayName      :
ClientRequestId  : 2870d5ab-f9be-405e-87d5-5bf20387c623 ActivityId: 24b28fc5-509b-4ad3-92c0-c8bb7ced7fb6
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="d5648-111">Запускает сопоставление контейнера защиты с указанными параметрами и возвращает задание ASR, используемую для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="d5648-111">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="d5648-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d5648-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrProtectionContainerMapping -Name $PrimaryProtectionContainerMapping -policy $Policy1 -PrimaryProtectionContainer $pc

Name             : 1f32fee1-05d0-4c11-a997-1618e14b4dab
ID               : /Subscriptions/xxxxxxxxxxxx/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/IbizaV2ATest/replicationJobs/1f32fee1-05d0-4c11-a997-1618e14b4dab
Type             :
JobType          :
DisplayName      :
ClientRequestId  : 2870d5ab-f9be-405e-87d5-5bf20387c623 ActivityId: 24b28fc5-509b-4ad3-92c0-c8bb7ced7fb6
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="d5648-113">Запускает сопоставление контейнера защиты с указанными параметрами и возвращает задание ASR, используемую для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="d5648-113">Starts the creation of the protection container mapping with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="d5648-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5648-114">PARAMETERS</span></span>

### <span data-ttu-id="d5648-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5648-115">-DefaultProfile</span></span>
<span data-ttu-id="d5648-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d5648-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d5648-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d5648-117">-Name</span></span>
<span data-ttu-id="d5648-118">Указывает имя сопоставления с контейнером защиты.</span><span class="sxs-lookup"><span data-stu-id="d5648-118">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="d5648-119">-Политика</span><span class="sxs-lookup"><span data-stu-id="d5648-119">-Policy</span></span>
<span data-ttu-id="d5648-120">Определяет объект политики репликации ASR для политики репликации, которая будет использоваться в сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="d5648-120">Specifies the ASR replication policy object for the replication policy to be used in the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5648-121">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d5648-121">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="d5648-122">Определяет объект контейнера защиты ASR для основного контейнера защиты, который будет использоваться в сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="d5648-122">Specifies the ASR protection container object for the  primary protection container to be used in the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5648-123">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d5648-123">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="d5648-124">Определяет объект контейнера защиты ASR для контейнера защиты восстановления, который будет использоваться в сопоставлении (используется при репликации в расположение восстановления, не в azure).</span><span class="sxs-lookup"><span data-stu-id="d5648-124">Specifies the ASR protection container object for the  recovery protection container to be used in the mapping (used if replicating to a recovery location that is not Azure.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5648-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5648-125">-Confirm</span></span>
<span data-ttu-id="d5648-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5648-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5648-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5648-127">-WhatIf</span></span>
<span data-ttu-id="d5648-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5648-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5648-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d5648-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5648-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5648-130">CommonParameters</span></span>
<span data-ttu-id="d5648-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5648-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5648-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5648-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5648-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5648-133">INPUTS</span></span>

### <span data-ttu-id="d5648-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="d5648-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="d5648-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d5648-135">OUTPUTS</span></span>

### <span data-ttu-id="d5648-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="d5648-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d5648-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d5648-137">NOTES</span></span>

## <span data-ttu-id="d5648-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5648-138">RELATED LINKS</span></span>

[<span data-ttu-id="d5648-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d5648-139">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="d5648-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d5648-140">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzRecoveryServicesAsrProtectionContainerMapping.md)