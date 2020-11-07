---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: a871aa624aaf8b7f24d06bd0ff04a45e29b95468
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562288"
---
# <span data-ttu-id="b36e0-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b36e0-101">New-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="b36e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b36e0-102">SYNOPSIS</span></span>
<span data-ttu-id="b36e0-103">Создание политики защиты резервных копий.</span><span class="sxs-lookup"><span data-stu-id="b36e0-103">Creates a Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b36e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b36e0-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b36e0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b36e0-105">DESCRIPTION</span></span>
<span data-ttu-id="b36e0-106">Командлет **New-AzureRmRecoveryServicesBackupProtectionPolicy** создает политику защиты резервного копирования в хранилище.</span><span class="sxs-lookup"><span data-stu-id="b36e0-106">The **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet creates a Backup protection policy in a vault.</span></span>
<span data-ttu-id="b36e0-107">Политика защиты связана по крайней мере с одной политикой хранения.</span><span class="sxs-lookup"><span data-stu-id="b36e0-107">A protection policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="b36e0-108">Политика хранения определяет, как долго будет храниться резервная копия Azure.</span><span class="sxs-lookup"><span data-stu-id="b36e0-108">The retention policy defines how long a recovery point is kept with Azure Backup.</span></span>

<span data-ttu-id="b36e0-109">Вы можете использовать командлет Get-AzureRmRecoveryServicesBackupRetentionPolicyObject, чтобы получить политику хранения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b36e0-109">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get the default retention policy.</span></span>
<span data-ttu-id="b36e0-110">Вы также можете использовать командлет Get-AzureRmRecoveryServicesBackupSchedulePolicyObject для получения политики расписания по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b36e0-110">And you can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get the default schedule policy.</span></span>
<span data-ttu-id="b36e0-111">Объекты **SchedulePolicy** и **RetentionPolicy** используются в качестве входных данных для командлета **New-AzureRmRecoveryServicesBackupProtectionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="b36e0-111">The **SchedulePolicy** and **RetentionPolicy** objects are used as inputs to the **New-AzureRmRecoveryServicesBackupProtectionPolicy** cmdlet.</span></span>

<span data-ttu-id="b36e0-112">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="b36e0-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="b36e0-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b36e0-113">EXAMPLES</span></span>

### <span data-ttu-id="b36e0-114">Пример 1: Создание политики защиты резервных копий</span><span class="sxs-lookup"><span data-stu-id="b36e0-114">Example 1: Create a Backup protection policy</span></span>
```
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

<span data-ttu-id="b36e0-115">Первая команда получает базовый **SchedulePolicyObject** и сохраняет ее в переменной $SchPol.</span><span class="sxs-lookup"><span data-stu-id="b36e0-115">The first command gets a base **SchedulePolicyObject** , and then stores it in the $SchPol variable.</span></span>

<span data-ttu-id="b36e0-116">Вторая команда удаляет все запланированные значения времени выполнения из политики расписания в $SchPol.</span><span class="sxs-lookup"><span data-stu-id="b36e0-116">The second command removes all scheduled run times from the schedule policy in $SchPol.</span></span>

<span data-ttu-id="b36e0-117">Третья команда использует командлет Get-Date, чтобы получить текущую дату и время.</span><span class="sxs-lookup"><span data-stu-id="b36e0-117">The third command uses the Get-Date cmdlet to get the current date and time.</span></span>

<span data-ttu-id="b36e0-118">Четвертая команда добавляет текущую дату и время в $Dt как запланированное время выполнения для политики расписания.</span><span class="sxs-lookup"><span data-stu-id="b36e0-118">The fourth command adds the current date and time in $Dt as the scheduled run time to the schedule policy.</span></span>

<span data-ttu-id="b36e0-119">Пятая команда получает базовый объект **RetentionPolicy** , а затем сохраняет его в переменной $RetPol.</span><span class="sxs-lookup"><span data-stu-id="b36e0-119">The fifth command gets a base **RetentionPolicy** object, and then stores it in the $RetPol variable.</span></span>

<span data-ttu-id="b36e0-120">Шестая команда задает для политики продолжительность хранения 365 дней.</span><span class="sxs-lookup"><span data-stu-id="b36e0-120">The sixth command sets the retention duration policy to 365 days.</span></span>

<span data-ttu-id="b36e0-121">Последняя команда создает объект **BackupProtectionPolicy** на основе политики расписания и хранения, созданной предыдущими командами.</span><span class="sxs-lookup"><span data-stu-id="b36e0-121">The final command creates a **BackupProtectionPolicy** object based on the schedule and retention policies created by the previous commands.</span></span>

## <span data-ttu-id="b36e0-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b36e0-122">PARAMETERS</span></span>

### <span data-ttu-id="b36e0-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="b36e0-123">-BackupManagementType</span></span>
<span data-ttu-id="b36e0-124">Указывает тип управления резервным копированием.</span><span class="sxs-lookup"><span data-stu-id="b36e0-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="b36e0-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b36e0-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b36e0-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="b36e0-126">AzureVM</span></span> 
- <span data-ttu-id="b36e0-127">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="b36e0-127">AzureSQLDatabase</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b36e0-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b36e0-128">-Name</span></span>
<span data-ttu-id="b36e0-129">Указывает имя политики.</span><span class="sxs-lookup"><span data-stu-id="b36e0-129">Specifies the name of the policy.</span></span>

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

### <span data-ttu-id="b36e0-130">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b36e0-130">-RetentionPolicy</span></span>
<span data-ttu-id="b36e0-131">Указывает базовый объект **RetentionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="b36e0-131">Specifies the base **RetentionPolicy** object.</span></span>
<span data-ttu-id="b36e0-132">Вы можете использовать командлет Get-AzureRmRecoveryServicesBackupRetentionPolicyObject, чтобы получить объект **RetentionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="b36e0-132">You can use the Get-AzureRmRecoveryServicesBackupRetentionPolicyObject cmdlet to get a **RetentionPolicy** object.</span></span>

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

### <span data-ttu-id="b36e0-133">-SchedulePolicy</span><span class="sxs-lookup"><span data-stu-id="b36e0-133">-SchedulePolicy</span></span>
<span data-ttu-id="b36e0-134">Указывает базовый объект **SchedulePolicy** .</span><span class="sxs-lookup"><span data-stu-id="b36e0-134">Specifies the base **SchedulePolicy** object.</span></span>
<span data-ttu-id="b36e0-135">Вы можете использовать командлет Get-AzureRmRecoveryServicesBackupSchedulePolicyObject, чтобы получить объект **SchedulePolicy** .</span><span class="sxs-lookup"><span data-stu-id="b36e0-135">You can use the Get-AzureRmRecoveryServicesBackupSchedulePolicyObject cmdlet to get a **SchedulePolicy** object.</span></span>

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

### <span data-ttu-id="b36e0-136">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="b36e0-136">-WorkloadType</span></span>
<span data-ttu-id="b36e0-137">Указывает тип рабочей нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b36e0-137">Specifies the workload type.</span></span>
<span data-ttu-id="b36e0-138">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b36e0-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b36e0-139">AzureVM</span><span class="sxs-lookup"><span data-stu-id="b36e0-139">AzureVM</span></span> 
- <span data-ttu-id="b36e0-140">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="b36e0-140">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b36e0-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b36e0-141">-DefaultProfile</span></span>
<span data-ttu-id="b36e0-142">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b36e0-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b36e0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b36e0-143">CommonParameters</span></span>
<span data-ttu-id="b36e0-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b36e0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b36e0-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b36e0-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b36e0-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b36e0-146">INPUTS</span></span>

## <span data-ttu-id="b36e0-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b36e0-147">OUTPUTS</span></span>

### <span data-ttu-id="b36e0-148">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="b36e0-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="b36e0-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="b36e0-149">NOTES</span></span>

## <span data-ttu-id="b36e0-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b36e0-150">RELATED LINKS</span></span>

[<span data-ttu-id="b36e0-151">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="b36e0-151">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="b36e0-152">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b36e0-152">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="b36e0-153">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="b36e0-153">Get-AzureRmRecoveryServicesBackupRetentionPolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[<span data-ttu-id="b36e0-154">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span><span class="sxs-lookup"><span data-stu-id="b36e0-154">Get-AzureRmRecoveryServicesBackupSchedulePolicyObject</span></span>](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[<span data-ttu-id="b36e0-155">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b36e0-155">Remove-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="b36e0-156">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b36e0-156">Set-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)

