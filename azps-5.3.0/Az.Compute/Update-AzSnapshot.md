---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
ms.openlocfilehash: 6cfe2fd958d74740195b0bb29d3defa34f1310a2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508993"
---
# <span data-ttu-id="94cdb-101">Update-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="94cdb-101">Update-AzSnapshot</span></span>

## <span data-ttu-id="94cdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94cdb-102">SYNOPSIS</span></span>
<span data-ttu-id="94cdb-103">Обновляет моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="94cdb-103">Updates a snapshot.</span></span>

## <span data-ttu-id="94cdb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="94cdb-104">SYNTAX</span></span>

### <span data-ttu-id="94cdb-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="94cdb-105">DefaultParameter (Default)</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-SnapshotUpdate] <PSSnapshotUpdate>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94cdb-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="94cdb-106">FriendMethod</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94cdb-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94cdb-107">DESCRIPTION</span></span>
<span data-ttu-id="94cdb-108">На **снимке обновляется cmdlet Update-AzSnapshot.**</span><span class="sxs-lookup"><span data-stu-id="94cdb-108">The **Update-AzSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="94cdb-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="94cdb-109">EXAMPLES</span></span>

### <span data-ttu-id="94cdb-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="94cdb-110">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="94cdb-111">Первая команда создает локальный пустой объект обновления моментального снимка с размером 10 ГБ Premium_LRS типа учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="94cdb-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="94cdb-112">Она также задает тип ОС Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="94cdb-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="94cdb-113">Вторая и третья команды настраивают параметры ключа шифрования диска и ключа шифрования для объекта обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="94cdb-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="94cdb-114">Последняя команда принимает объект обновления моментального снимка и обновляет существующий моментальный снимок с именем "Снимок01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="94cdb-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="94cdb-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="94cdb-115">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="94cdb-116">Эта команда обновляет существующий моментальный снимок с именем "Моментальный снимок01" в группе ресурсов "Группа ресурсов01" до размера диска 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="94cdb-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="94cdb-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="94cdb-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="94cdb-118">Эти команды также обновляют существующий моментальный снимок с именем "Моментальный снимок01" в группе ресурсов "Группа ресурсов01" до размера диска 10 ГБ.</span><span class="sxs-lookup"><span data-stu-id="94cdb-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="94cdb-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94cdb-119">PARAMETERS</span></span>

### <span data-ttu-id="94cdb-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94cdb-120">-AsJob</span></span>
<span data-ttu-id="94cdb-121">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="94cdb-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="94cdb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94cdb-122">-DefaultProfile</span></span>
<span data-ttu-id="94cdb-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94cdb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94cdb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94cdb-124">-ResourceGroupName</span></span>
<span data-ttu-id="94cdb-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94cdb-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94cdb-126">-Моментальный снимок</span><span class="sxs-lookup"><span data-stu-id="94cdb-126">-Snapshot</span></span>
<span data-ttu-id="94cdb-127">Определяет локальный объект моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="94cdb-127">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94cdb-128">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="94cdb-128">-SnapshotName</span></span>
<span data-ttu-id="94cdb-129">Указывает имя моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="94cdb-129">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94cdb-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="94cdb-130">-SnapshotUpdate</span></span>
<span data-ttu-id="94cdb-131">Определяет локальный объект обновления моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="94cdb-131">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94cdb-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94cdb-132">-Confirm</span></span>
<span data-ttu-id="94cdb-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94cdb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94cdb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94cdb-134">-WhatIf</span></span>
<span data-ttu-id="94cdb-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94cdb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94cdb-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="94cdb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94cdb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94cdb-137">CommonParameters</span></span>
<span data-ttu-id="94cdb-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94cdb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94cdb-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94cdb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94cdb-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94cdb-140">INPUTS</span></span>

### <span data-ttu-id="94cdb-141">System.String</span><span class="sxs-lookup"><span data-stu-id="94cdb-141">System.String</span></span>

### <span data-ttu-id="94cdb-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="94cdb-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="94cdb-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="94cdb-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="94cdb-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="94cdb-144">OUTPUTS</span></span>

### <span data-ttu-id="94cdb-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="94cdb-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="94cdb-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="94cdb-146">NOTES</span></span>

## <span data-ttu-id="94cdb-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94cdb-147">RELATED LINKS</span></span>