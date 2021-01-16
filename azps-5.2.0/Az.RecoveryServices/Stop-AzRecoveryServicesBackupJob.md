---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 41234c91d5c833f15a4914d2af2de93c9c5bf288
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392268"
---
# <span data-ttu-id="fc776-101">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="fc776-101">Stop-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="fc776-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc776-102">SYNOPSIS</span></span>
<span data-ttu-id="fc776-103">Отменяет задание.</span><span class="sxs-lookup"><span data-stu-id="fc776-103">Cancels a running job.</span></span>

## <span data-ttu-id="fc776-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fc776-104">SYNTAX</span></span>

### <span data-ttu-id="fc776-105">JobFilterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fc776-105">JobFilterSet (Default)</span></span>
```
Stop-AzRecoveryServicesBackupJob [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc776-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="fc776-106">IdFilterSet</span></span>
```
Stop-AzRecoveryServicesBackupJob [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc776-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc776-107">DESCRIPTION</span></span>
<span data-ttu-id="fc776-108">Выполнение существующего задания резервного копирования Azure отменено с использованием cmdlet **Stop-AzRecoveryServicesBackupJob.**</span><span class="sxs-lookup"><span data-stu-id="fc776-108">The **Stop-AzRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="fc776-109">Используйте этот cmdlet, чтобы остановить задание, которое занимает слишком много времени, и блокирует другие действия.</span><span class="sxs-lookup"><span data-stu-id="fc776-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="fc776-110">Отменять можно только типы резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="fc776-110">You can cancel only Backup and Restore job types.</span></span>
<span data-ttu-id="fc776-111">Прежде чем использовать текущий Set-AzRecoveryServicesVaultContext, задате контекст хранилища с помощью Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="fc776-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="fc776-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fc776-112">EXAMPLES</span></span>

### <span data-ttu-id="fc776-113">Пример 1. Остановка задания резервного копирования</span><span class="sxs-lookup"><span data-stu-id="fc776-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="fc776-114">Первая команда получает задание резервного копирования, а затем сохраняет его в переменной $Job.</span><span class="sxs-lookup"><span data-stu-id="fc776-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>
<span data-ttu-id="fc776-115">Последняя команда останавливает задание, указав код экземпляра задания резервного копирования в $Job.</span><span class="sxs-lookup"><span data-stu-id="fc776-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="fc776-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc776-116">PARAMETERS</span></span>

### <span data-ttu-id="fc776-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc776-117">-DefaultProfile</span></span>
<span data-ttu-id="fc776-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fc776-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc776-119">-Job</span><span class="sxs-lookup"><span data-stu-id="fc776-119">-Job</span></span>
<span data-ttu-id="fc776-120">Задание, которое этот cmdlet отменяет.</span><span class="sxs-lookup"><span data-stu-id="fc776-120">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="fc776-121">Чтобы получить объект **BackupJob,** воспользуйтесь Get-AzRecoveryServicesBackupJob..</span><span class="sxs-lookup"><span data-stu-id="fc776-121">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: JobFilterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc776-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="fc776-122">-JobId</span></span>
<span data-ttu-id="fc776-123">Определяет ИД отменяемого задания.</span><span class="sxs-lookup"><span data-stu-id="fc776-123">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="fc776-124">Код — это свойство InstanceId объекта **BackupJob.**</span><span class="sxs-lookup"><span data-stu-id="fc776-124">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="fc776-125">Чтобы получить объект **BackupJob,** используйте Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="fc776-125">To obtain an **BackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFilterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc776-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="fc776-126">-VaultId</span></span>
<span data-ttu-id="fc776-127">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="fc776-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="fc776-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc776-128">-Confirm</span></span>
<span data-ttu-id="fc776-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc776-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc776-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc776-130">-WhatIf</span></span>
<span data-ttu-id="fc776-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc776-131">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="fc776-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc776-132">CommonParameters</span></span>
<span data-ttu-id="fc776-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc776-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc776-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc776-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc776-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc776-135">INPUTS</span></span>

### <span data-ttu-id="fc776-136">System.String</span><span class="sxs-lookup"><span data-stu-id="fc776-136">System.String</span></span>

## <span data-ttu-id="fc776-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fc776-137">OUTPUTS</span></span>

### <span data-ttu-id="fc776-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="fc776-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="fc776-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fc776-139">NOTES</span></span>

## <span data-ttu-id="fc776-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc776-140">RELATED LINKS</span></span>

[<span data-ttu-id="fc776-141">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="fc776-141">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="fc776-142">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="fc776-142">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)

