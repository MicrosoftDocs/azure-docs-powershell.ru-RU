---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: cfa8abf93fcb7eb4cd3848b1a5f69cf28a5fe6ab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506747"
---
# <span data-ttu-id="4e0ea-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="4e0ea-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="4e0ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e0ea-102">SYNOPSIS</span></span>
<span data-ttu-id="4e0ea-103">Командлет **Register-AzRecoveryServicesBackupContainer** регистрирует azure VM для AzureWorkloads с определенным типом рабочей нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4e0ea-103">The **Register-AzRecoveryServicesBackupContainer** cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="4e0ea-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4e0ea-104">SYNTAX</span></span>

### <span data-ttu-id="4e0ea-105">Регистрация (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e0ea-105">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e0ea-106">ReRegister</span><span class="sxs-lookup"><span data-stu-id="4e0ea-106">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e0ea-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e0ea-107">DESCRIPTION</span></span>
<span data-ttu-id="4e0ea-108">Эта команда позволяет резервной копии Azure преобразовать ресурс в контейнер резервной копии, который затем регистрируется в заданном хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="4e0ea-108">This command allows Azure Backup to convert the Resource to a Backup Container which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="4e0ea-109">Служба резервного копирования Azure затем может обнаружить рабочие нагрузки данного типа рабочей нагрузки в этом контейнере, чтобы защититься в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="4e0ea-109">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="4e0ea-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4e0ea-110">EXAMPLES</span></span>

### <span data-ttu-id="4e0ea-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4e0ea-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="4e0ea-112">Этот cmdlet регистрирует azure VM в качестве контейнера для рабочей нагрузки MSSQL.</span><span class="sxs-lookup"><span data-stu-id="4e0ea-112">The cmdlet registers an azure VM as a container for the workload MSSQL.</span></span>

## <span data-ttu-id="4e0ea-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e0ea-113">PARAMETERS</span></span>

### <span data-ttu-id="4e0ea-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="4e0ea-114">-BackupManagementType</span></span>
<span data-ttu-id="4e0ea-115">Класс защищенных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e0ea-115">The class of resources being protected.</span></span> <span data-ttu-id="4e0ea-116">В настоящее время для этого командлета поддерживается AzureWorkload.</span><span class="sxs-lookup"><span data-stu-id="4e0ea-116">Currently the value supported for this cmdlet is AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e0ea-117">-Container</span><span class="sxs-lookup"><span data-stu-id="4e0ea-117">-Container</span></span>
<span data-ttu-id="4e0ea-118">Контейнер, в котором находится элемент</span><span class="sxs-lookup"><span data-stu-id="4e0ea-118">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: ReRegister
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e0ea-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e0ea-119">-DefaultProfile</span></span>
<span data-ttu-id="4e0ea-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e0ea-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e0ea-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4e0ea-121">-Force</span></span>
<span data-ttu-id="4e0ea-122">Принудительно регистрирует контейнер (диалоговое окно подтверждения не позволяет).</span><span class="sxs-lookup"><span data-stu-id="4e0ea-122">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="4e0ea-123">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="4e0ea-123">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e0ea-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e0ea-124">-ResourceId</span></span>
<span data-ttu-id="4e0ea-125">ИД ресурса Azure, представитель которого нужно проверить, если он уже защищен хранилищем RecoveryServices в подписке.</span><span class="sxs-lookup"><span data-stu-id="4e0ea-125">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Register
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e0ea-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4e0ea-126">-VaultId</span></span>
<span data-ttu-id="4e0ea-127">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="4e0ea-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4e0ea-128">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="4e0ea-128">-WorkloadType</span></span>
<span data-ttu-id="4e0ea-129">Тип рабочей нагрузки ресурса.</span><span class="sxs-lookup"><span data-stu-id="4e0ea-129">Workload type of the resource.</span></span> <span data-ttu-id="4e0ea-130">В настоящее время поддерживается значение AzureVM, WindowsServer, AzureFiles, MSSQL.</span><span class="sxs-lookup"><span data-stu-id="4e0ea-130">The current supported value is AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e0ea-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e0ea-131">-Confirm</span></span>
<span data-ttu-id="4e0ea-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4e0ea-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e0ea-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e0ea-133">-WhatIf</span></span>
<span data-ttu-id="4e0ea-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e0ea-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="4e0ea-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e0ea-135">CommonParameters</span></span>
<span data-ttu-id="4e0ea-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e0ea-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e0ea-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e0ea-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e0ea-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e0ea-138">INPUTS</span></span>

### <span data-ttu-id="4e0ea-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4e0ea-139">System.String</span></span>

## <span data-ttu-id="4e0ea-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4e0ea-140">OUTPUTS</span></span>

### <span data-ttu-id="4e0ea-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="4e0ea-141">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="4e0ea-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4e0ea-142">NOTES</span></span>

## <span data-ttu-id="4e0ea-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e0ea-143">RELATED LINKS</span></span>