---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: 242060652ea84d7fd85bc0907379ccb5b6eba478
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721581"
---
# <span data-ttu-id="0344f-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0344f-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="0344f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0344f-102">SYNOPSIS</span></span>
<span data-ttu-id="0344f-103">Обновляет реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="0344f-103">Updates a container registry.</span></span>

## <span data-ttu-id="0344f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0344f-104">SYNTAX</span></span>

### <span data-ttu-id="0344f-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0344f-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0344f-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0344f-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0344f-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0344f-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0344f-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0344f-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0344f-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0344f-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0344f-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0344f-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0344f-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0344f-111">DESCRIPTION</span></span>
<span data-ttu-id="0344f-112">Командлет Update-AzContainerRegistry обновляет реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="0344f-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="0344f-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0344f-113">EXAMPLES</span></span>

### <span data-ttu-id="0344f-114">Пример 1: включение учетной записи пользователя администратора для указанного контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="0344f-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="0344f-115">Эта команда позволяет пользователю администратора для указанного контейнера реестра.</span><span class="sxs-lookup"><span data-stu-id="0344f-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="0344f-116">Пример 2: Настройка учетной записи хранения, используемой в указанном контейнере реестра</span><span class="sxs-lookup"><span data-stu-id="0344f-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="0344f-117">Эта команда задает для указанного контейнера реестра использование существующей учетной записи хранения \` mystorageaccount \` в той же подписке.</span><span class="sxs-lookup"><span data-stu-id="0344f-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="0344f-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0344f-118">PARAMETERS</span></span>

### <span data-ttu-id="0344f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0344f-119">-DefaultProfile</span></span>
<span data-ttu-id="0344f-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0344f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0344f-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="0344f-121">-DisableAdminUser</span></span>
<span data-ttu-id="0344f-122">Включите для пользователя администратора контейнер реестра.</span><span class="sxs-lookup"><span data-stu-id="0344f-122">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceIdParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0344f-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="0344f-123">-EnableAdminUser</span></span>
<span data-ttu-id="0344f-124">Включите для пользователя администратора контейнер реестра.</span><span class="sxs-lookup"><span data-stu-id="0344f-124">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserByResourceNameParameterSet, EnableAdminUserByResourceIdParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0344f-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0344f-125">-Name</span></span>
<span data-ttu-id="0344f-126">Имя контейнера в реестре.</span><span class="sxs-lookup"><span data-stu-id="0344f-126">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0344f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0344f-127">-ResourceGroupName</span></span>
<span data-ttu-id="0344f-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0344f-128">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0344f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0344f-129">-ResourceId</span></span>
<span data-ttu-id="0344f-130">Идентификатор ресурса реестра контейнера</span><span class="sxs-lookup"><span data-stu-id="0344f-130">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceIdParameterSet, DisableAdminUserByResourceIdParameterSet, ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0344f-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="0344f-131">-Sku</span></span>
<span data-ttu-id="0344f-132">SKU реестра Container.</span><span class="sxs-lookup"><span data-stu-id="0344f-132">Container Registry SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Classic, Basic, Premium, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0344f-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0344f-133">-StorageAccountName</span></span>
<span data-ttu-id="0344f-134">Имя существующей учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0344f-134">The name of an existing storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0344f-135">-Тег</span><span class="sxs-lookup"><span data-stu-id="0344f-135">-Tag</span></span>
<span data-ttu-id="0344f-136">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="0344f-136">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="0344f-137">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="0344f-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0344f-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0344f-138">-Confirm</span></span>
<span data-ttu-id="0344f-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0344f-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0344f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0344f-140">-WhatIf</span></span>
<span data-ttu-id="0344f-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0344f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0344f-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0344f-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0344f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0344f-143">CommonParameters</span></span>
<span data-ttu-id="0344f-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0344f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0344f-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0344f-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0344f-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0344f-146">INPUTS</span></span>

### <span data-ttu-id="0344f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="0344f-147">System.String</span></span>

## <span data-ttu-id="0344f-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0344f-148">OUTPUTS</span></span>

### <span data-ttu-id="0344f-149">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0344f-149">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="0344f-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="0344f-150">NOTES</span></span>

## <span data-ttu-id="0344f-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0344f-151">RELATED LINKS</span></span>

[<span data-ttu-id="0344f-152">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0344f-152">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="0344f-153">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0344f-153">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="0344f-154">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0344f-154">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)
