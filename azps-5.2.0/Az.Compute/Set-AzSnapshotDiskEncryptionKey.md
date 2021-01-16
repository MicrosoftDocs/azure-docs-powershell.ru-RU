---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotDiskEncryptionKey.md
ms.openlocfilehash: e4ecb281382af308176f47462e086f69c18e6163
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325656"
---
# <span data-ttu-id="441a3-101">Set-AzSnapshotDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="441a3-101">Set-AzSnapshotDiskEncryptionKey</span></span>

## <span data-ttu-id="441a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="441a3-102">SYNOPSIS</span></span>
<span data-ttu-id="441a3-103">Задает свойства ключа шифрования диска для объекта моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="441a3-103">Sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="441a3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="441a3-104">SYNTAX</span></span>

```
Set-AzSnapshotDiskEncryptionKey [-Snapshot] <PSSnapshot> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="441a3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="441a3-105">DESCRIPTION</span></span>
<span data-ttu-id="441a3-106">Cmdlet **Set-AzSnapshotDiskEncryptionKey** задает свойства ключа шифрования диска для объекта моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="441a3-106">The **Set-AzSnapshotDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="441a3-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="441a3-107">EXAMPLES</span></span>

### <span data-ttu-id="441a3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="441a3-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="441a3-109">Первая команда создает локальный пустой объект моментального снимка с размером 5 ГБ Standard_LRS типа учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="441a3-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="441a3-110">Она также задает тип ос Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="441a3-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="441a3-111">Вторая и третья команды настраивают параметры ключа шифрования диска и ключа шифрования для объекта моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="441a3-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="441a3-112">Последняя команда принимает объект моментального снимка и создает моментальный снимок с именем "Моментальный снимок01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="441a3-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="441a3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="441a3-113">PARAMETERS</span></span>

### <span data-ttu-id="441a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="441a3-114">-DefaultProfile</span></span>
<span data-ttu-id="441a3-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="441a3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="441a3-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="441a3-116">-SecretUrl</span></span>
<span data-ttu-id="441a3-117">Указывает секретный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="441a3-117">Specifies the secret Url.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="441a3-118">-Моментальный снимок</span><span class="sxs-lookup"><span data-stu-id="441a3-118">-Snapshot</span></span>
<span data-ttu-id="441a3-119">Определяет локальный объект моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="441a3-119">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="441a3-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="441a3-120">-SourceVaultId</span></span>
<span data-ttu-id="441a3-121">Определяет код источника хранилища.</span><span class="sxs-lookup"><span data-stu-id="441a3-121">Specifies the source vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="441a3-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="441a3-122">-Confirm</span></span>
<span data-ttu-id="441a3-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="441a3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="441a3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="441a3-124">-WhatIf</span></span>
<span data-ttu-id="441a3-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="441a3-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="441a3-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="441a3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="441a3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="441a3-127">CommonParameters</span></span>
<span data-ttu-id="441a3-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="441a3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="441a3-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="441a3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="441a3-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="441a3-130">INPUTS</span></span>

### <span data-ttu-id="441a3-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="441a3-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="441a3-132">System.String</span><span class="sxs-lookup"><span data-stu-id="441a3-132">System.String</span></span>

## <span data-ttu-id="441a3-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="441a3-133">OUTPUTS</span></span>

### <span data-ttu-id="441a3-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="441a3-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="441a3-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="441a3-135">NOTES</span></span>

## <span data-ttu-id="441a3-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="441a3-136">RELATED LINKS</span></span>