---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 9992c4232bd93e9653f0723911f539b1204ce538
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393316"
---
# <span data-ttu-id="4251e-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4251e-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="4251e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4251e-102">SYNOPSIS</span></span>
<span data-ttu-id="4251e-103">Создание плана восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="4251e-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="4251e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4251e-104">SYNTAX</span></span>

### <span data-ttu-id="4251e-105">EnterpriseToEnterprise (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4251e-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4251e-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="4251e-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4251e-107">AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="4251e-107">AzureZoneToZone</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -PrimaryZone <String>
 -RecoveryZone <String> [-AzureZoneToZone] -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4251e-108">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="4251e-108">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4251e-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4251e-109">DESCRIPTION</span></span>
<span data-ttu-id="4251e-110">С **его использованием** в хранилище служб восстановления создается план восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="4251e-110">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="4251e-111">При планировании восстановления виртуальные машины, принадлежащие приложению, собираются в единицу, чтобы их можно было восстановить вместе.</span><span class="sxs-lookup"><span data-stu-id="4251e-111">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="4251e-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4251e-112">EXAMPLES</span></span>

### <span data-ttu-id="4251e-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4251e-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="4251e-114">Начало операции создания плана восстановления с указанными параметрами и возврат задания asR, используемого для ее отслеживания.</span><span class="sxs-lookup"><span data-stu-id="4251e-114">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="4251e-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4251e-115">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -PrimaryZone $pZone-RecoveryZone $rZone -ReplicationProtectedItem $RPI
```

<span data-ttu-id="4251e-116">Начало операции создания плана восстановления для зоны Azure с реплицируемыми элементами и возврат задания asR, используемого для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="4251e-116">Starts the recovery plan creation operation for Azure zone to zone replicated items and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="4251e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4251e-117">PARAMETERS</span></span>

### <span data-ttu-id="4251e-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="4251e-118">-Azure</span></span>
<span data-ttu-id="4251e-119">Параметр переключения определяет сценарий аварийного восстановления azure для azure и создания плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="4251e-119">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4251e-120">-AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="4251e-120">-AzureZoneToZone</span></span>
<span data-ttu-id="4251e-121">Параметр переключения указывает, что нужно создать реплицированный элемент в сценарии создания зоны Azure.</span><span class="sxs-lookup"><span data-stu-id="4251e-121">Switch parameter specifies creating the replicated item in azure zone to zone scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4251e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4251e-122">-DefaultProfile</span></span>
<span data-ttu-id="4251e-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4251e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="4251e-124">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="4251e-124">-FailoverDeploymentModel</span></span>
<span data-ttu-id="4251e-125">Указывает модель отбойного развертывания (классическая или диспетчер ресурсов) для элементов, защищенных репликацией, которые будут частью этого плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="4251e-125">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases:
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4251e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4251e-126">-Name</span></span>
<span data-ttu-id="4251e-127">Имя плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="4251e-127">Name of the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4251e-128">-Path</span><span class="sxs-lookup"><span data-stu-id="4251e-128">-Path</span></span>
<span data-ttu-id="4251e-129">Путь к JSON-файлу определения плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="4251e-129">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="4251e-130">Для создания плана восстановления можно использовать определение плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="4251e-130">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="4251e-131">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="4251e-131">-PrimaryFabric</span></span>
<span data-ttu-id="4251e-132">Определяет объект "Ткань ASR" для основного материала ASR защищенных репликацией элементов, которые будут в составе этого плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="4251e-132">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4251e-133">-PrimaryZone</span><span class="sxs-lookup"><span data-stu-id="4251e-133">-PrimaryZone</span></span>
<span data-ttu-id="4251e-134">Указывает основную зону 100 пунктов, защищенных репликацией, которые будут в составе этого плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="4251e-134">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4251e-135">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="4251e-135">-RecoveryFabric</span></span>
<span data-ttu-id="4251e-136">Определяет объект "Ткань ASR" для материала для восстановления объектов, защищенных репликацией, которые будут в составе этого плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="4251e-136">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4251e-137">-RecoveryZone</span><span class="sxs-lookup"><span data-stu-id="4251e-137">-RecoveryZone</span></span>
<span data-ttu-id="4251e-138">Указывает основную зону 100 пунктов, защищенных репликацией, которые будут в составе этого плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="4251e-138">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4251e-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4251e-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="4251e-140">Список элементов, защищенных репликацией, которые нужно добавить в первую группу плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="4251e-140">The list of replication protected items to add to the first group of the recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4251e-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4251e-141">-Confirm</span></span>
<span data-ttu-id="4251e-142">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4251e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4251e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4251e-143">-WhatIf</span></span>
<span data-ttu-id="4251e-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4251e-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4251e-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4251e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4251e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4251e-146">CommonParameters</span></span>
<span data-ttu-id="4251e-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4251e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4251e-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4251e-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4251e-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4251e-149">INPUTS</span></span>

### <span data-ttu-id="4251e-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="4251e-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="4251e-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4251e-151">OUTPUTS</span></span>

### <span data-ttu-id="4251e-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="4251e-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4251e-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4251e-153">NOTES</span></span>

## <span data-ttu-id="4251e-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4251e-154">RELATED LINKS</span></span>

[<span data-ttu-id="4251e-155">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4251e-155">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="4251e-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4251e-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="4251e-157">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4251e-157">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)

