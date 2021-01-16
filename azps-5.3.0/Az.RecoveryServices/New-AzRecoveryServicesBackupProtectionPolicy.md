---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 0a60e3bd7f07f69687766b95eb3d56be3ef1d56f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506754"
---
# <span data-ttu-id="e5a97-101">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e5a97-101">New-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="e5a97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5a97-102">SYNOPSIS</span></span>
<span data-ttu-id="e5a97-103">Создает политику защиты от резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="e5a97-103">Creates a Backup protection policy.</span></span>

## <span data-ttu-id="e5a97-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e5a97-104">SYNTAX</span></span>

```
New-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5a97-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5a97-105">DESCRIPTION</span></span>
<span data-ttu-id="e5a97-106">**Cmdlet New-AzRecoveryServicesBackupProtectionPolicy** создает политику защиты резервного копирования в хранилище.</span><span class="sxs-lookup"><span data-stu-id="e5a97-106">The **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="e5a97-107">Политика защиты связана по крайней мере с одной политикой хранения.</span><span class="sxs-lookup"><span data-stu-id="e5a97-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="e5a97-108">Политика хранения определяет срок хранения точки восстановления с помощью резервной копии Azure.</span><span class="sxs-lookup"><span data-stu-id="e5a97-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>
<span data-ttu-id="e5a97-109">Вы можете использовать Get-AzRecoveryServicesBackupRetentionPolicyObject для получения политики хранения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e5a97-109">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="e5a97-110">Вы также можете использовать Get-AzRecoveryServicesBackupSchedulePolicyObject календарный план, чтобы получить политику расписания по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e5a97-110">And you can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="e5a97-111">Объекты **SchedulePolicy** и **RetentionPolicy** используются в качестве входных данных для cmdlet **New-AzRecoveryServicesBackupProtectionPolicy.**</span><span class="sxs-lookup"><span data-stu-id="e5a97-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="e5a97-112">Прежде чем использовать текущий Set-AzRecoveryServicesVaultContext, задате контекст хранилища с помощью Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="e5a97-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="e5a97-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e5a97-113">EXAMPLES</span></span>

### <span data-ttu-id="e5a97-114">Пример 1. Создание политики защиты от резервного копирования</span><span class="sxs-lookup"><span data-stu-id="e5a97-114">Example 1: Create a Backup protection policy</span></span>
```powershell
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="e5a97-115">Первая команда получает базовое **значение SchedulePolicyObject,** а затем сохраняет его в переменной $SchPol.</span><span class="sxs-lookup"><span data-stu-id="e5a97-115">The first command gets a base **SchedulePolicyObject**, and then stores it in the $SchPol variable.</span></span>
<span data-ttu-id="e5a97-116">Вторая команда удаляет все запланированное время запуска из политики расписания в $SchPol.</span><span class="sxs-lookup"><span data-stu-id="e5a97-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>
<span data-ttu-id="e5a97-117">Третья команда использует Get-Date для получения текущих даты и времени.</span><span class="sxs-lookup"><span data-stu-id="e5a97-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>
<span data-ttu-id="e5a97-118">Четвертая команда добавляет текущую дату и время в $Dt как запланированное время запуска в политику расписания.</span><span class="sxs-lookup"><span data-stu-id="e5a97-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>
<span data-ttu-id="e5a97-119">Пятая команда получает базовый объект **RetentionPolicy** и сохраняет его в переменной $RetPol.</span><span class="sxs-lookup"><span data-stu-id="e5a97-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>
<span data-ttu-id="e5a97-120">Шестая команда задает для политики срока хранения 365 дней.</span><span class="sxs-lookup"><span data-stu-id="e5a97-120">The sixth command sets the retention duration policy to 365 days.</span></span>
<span data-ttu-id="e5a97-121">Конечная команда создает объект **BackupProtectionPolicy** на основе политик расписания и хранения, созданных предыдущими командами.</span><span class="sxs-lookup"><span data-stu-id="e5a97-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

### <span data-ttu-id="e5a97-122">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e5a97-122">Example 2</span></span>

<span data-ttu-id="e5a97-123">Создает политику защиты от резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="e5a97-123">Creates a Backup protection policy.</span></span> <span data-ttu-id="e5a97-124">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="e5a97-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzRecoveryServicesBackupProtectionPolicy -Name 'NewPolicy' -RetentionPolicy $RetPol -SchedulePolicy $SchPol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="e5a97-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5a97-125">PARAMETERS</span></span>

### <span data-ttu-id="e5a97-126">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="e5a97-126">-BackupManagementType</span></span>
<span data-ttu-id="e5a97-127">Класс защищенных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e5a97-127">The class of resources being protected.</span></span> <span data-ttu-id="e5a97-128">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="e5a97-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e5a97-129">AzureVM</span><span class="sxs-lookup"><span data-stu-id="e5a97-129">AzureVM</span></span> 
- <span data-ttu-id="e5a97-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="e5a97-130">AzureStorage</span></span>
- <span data-ttu-id="e5a97-131">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="e5a97-131">AzureWorkload</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5a97-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5a97-132">-DefaultProfile</span></span>
<span data-ttu-id="e5a97-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5a97-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5a97-134">-Name</span><span class="sxs-lookup"><span data-stu-id="e5a97-134">-Name</span></span>
<span data-ttu-id="e5a97-135">Указывает имя политики.</span><span class="sxs-lookup"><span data-stu-id="e5a97-135">Specifies the name of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5a97-136">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e5a97-136">-RetentionPolicy</span></span>
<span data-ttu-id="e5a97-137">Определяет базовый **объект RetentionPolicy.**</span><span class="sxs-lookup"><span data-stu-id="e5a97-137">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="e5a97-138">Для получения объекта RetentionPolicy Get-AzRecoveryServicesBackupRetentionPolicyObject помощью Get-AzRecoveryServicesBackupRetentionPolicyObject **RetentionPolicy.**</span><span class="sxs-lookup"><span data-stu-id="e5a97-138">You can use the Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5a97-139">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="e5a97-139">-SchedulePolicy</span></span>
<span data-ttu-id="e5a97-140">Определяет базовый **объект SchedulePolicy.**</span><span class="sxs-lookup"><span data-stu-id="e5a97-140">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="e5a97-141">Для получения объекта SchedulePolicy Get-AzRecoveryServicesBackupSchedulePolicyObject помощью Get-AzRecoveryServicesBackupSchedulePolicyObject **SchedulePolicy.**</span><span class="sxs-lookup"><span data-stu-id="e5a97-141">You can use the Get-AzRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5a97-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e5a97-142">-VaultId</span></span>
<span data-ttu-id="e5a97-143">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="e5a97-143">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5a97-144">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="e5a97-144">-WorkloadType</span></span>
<span data-ttu-id="e5a97-145">Тип рабочей нагрузки ресурса.</span><span class="sxs-lookup"><span data-stu-id="e5a97-145">Workload type of the resource.</span></span> <span data-ttu-id="e5a97-146">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="e5a97-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e5a97-147">AzureVM</span><span class="sxs-lookup"><span data-stu-id="e5a97-147">AzureVM</span></span> 
- <span data-ttu-id="e5a97-148">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="e5a97-148">AzureFiles</span></span>
- <span data-ttu-id="e5a97-149">MSSQL</span><span class="sxs-lookup"><span data-stu-id="e5a97-149">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5a97-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5a97-150">-Confirm</span></span>
<span data-ttu-id="e5a97-151">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5a97-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5a97-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5a97-152">-WhatIf</span></span>
<span data-ttu-id="e5a97-153">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5a97-153">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="e5a97-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5a97-154">CommonParameters</span></span>
<span data-ttu-id="e5a97-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5a97-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5a97-156">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5a97-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5a97-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5a97-157">INPUTS</span></span>

### <span data-ttu-id="e5a97-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span><span class="sxs-lookup"><span data-stu-id="e5a97-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType</span></span>

### <span data-ttu-id="e5a97-159">System.Nullable'1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="e5a97-159">System.Nullable\`1[[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType, Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.Models, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e5a97-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span><span class="sxs-lookup"><span data-stu-id="e5a97-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase</span></span>

### <span data-ttu-id="e5a97-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span><span class="sxs-lookup"><span data-stu-id="e5a97-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase</span></span>

### <span data-ttu-id="e5a97-162">System.String</span><span class="sxs-lookup"><span data-stu-id="e5a97-162">System.String</span></span>

## <span data-ttu-id="e5a97-163">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e5a97-163">OUTPUTS</span></span>

### <span data-ttu-id="e5a97-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span><span class="sxs-lookup"><span data-stu-id="e5a97-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="e5a97-165">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e5a97-165">NOTES</span></span>

## <span data-ttu-id="e5a97-166">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5a97-166">RELATED LINKS</span></span>

[<span data-ttu-id="e5a97-167">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="e5a97-167">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="e5a97-168">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e5a97-168">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="e5a97-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="e5a97-169">Get-AzRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="e5a97-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="e5a97-170">Get-AzRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="e5a97-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e5a97-171">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="e5a97-172">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e5a97-172">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)

