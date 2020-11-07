---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/update-azurermstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: d167061692e3d5cccfd54a3f990af8312446ac67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565772"
---
# <span data-ttu-id="b0080-101">Update-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b0080-101">Update-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="b0080-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b0080-102">SYNOPSIS</span></span>
<span data-ttu-id="b0080-103">Обновление свойства NetworkRule учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="b0080-103">Update the NetworkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0080-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b0080-104">SYNTAX</span></span>

```
Update-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0080-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0080-105">DESCRIPTION</span></span>
<span data-ttu-id="b0080-106">Командлет **Update-AzureRmStorageAccountNetworkRuleSet** обновляет свойство NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b0080-106">The **Update-AzureRmStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="b0080-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b0080-107">EXAMPLES</span></span>

### <span data-ttu-id="b0080-108">Пример 1: обновление всех свойств NetworkRule, правил ввода с помощью JSON</span><span class="sxs-lookup"><span data-stu-id="b0080-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="b0080-109">Эта команда обновляет все свойства NetworkRule, правила ввода с помощью JSON.</span><span class="sxs-lookup"><span data-stu-id="b0080-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="b0080-110">Пример 2: обновление свойства обхода для NetworkRule</span><span class="sxs-lookup"><span data-stu-id="b0080-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="b0080-111">Это обновление свойства обхода для NetworkRule (другие свойства не изменяются).</span><span class="sxs-lookup"><span data-stu-id="b0080-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="b0080-112">Пример 3: Очистка правил NetworkRule учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="b0080-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="b0080-113">Эта команда очищает правила для NetworkRule учетной записи хранения (другие свойства не изменяются).</span><span class="sxs-lookup"><span data-stu-id="b0080-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="b0080-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b0080-114">PARAMETERS</span></span>

### <span data-ttu-id="b0080-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0080-115">-AsJob</span></span>
<span data-ttu-id="b0080-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b0080-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0080-117">-Обход</span><span class="sxs-lookup"><span data-stu-id="b0080-117">-Bypass</span></span>
<span data-ttu-id="b0080-118">Значение пропуска для обновления свойства NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b0080-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="b0080-119">Разрешенное значение — None (нет) или любое сочетание: • ведение журнала • метрическая система мер • Azureservices</span><span class="sxs-lookup"><span data-stu-id="b0080-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleBypassEnum
Parameter Sets: (All)
Aliases:
Accepted values: None, Logging, Metrics, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0080-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="b0080-120">-DefaultAction</span></span>
<span data-ttu-id="b0080-121">Значение DefaultAction, которое требуется обновить, на свойство NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b0080-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="b0080-122">Разрешенные варианты: • разрешить • запретить</span><span class="sxs-lookup"><span data-stu-id="b0080-122">The allowed Options: • Allow • Deny</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0080-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0080-123">-DefaultProfile</span></span>
<span data-ttu-id="b0080-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0080-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0080-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="b0080-125">-IPRule</span></span>
<span data-ttu-id="b0080-126">Массив объектов IpRule, которые нужно обновить, на свойство NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b0080-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0080-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b0080-127">-Name</span></span>
<span data-ttu-id="b0080-128">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b0080-128">Specifies the name of the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0080-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0080-129">-ResourceGroupName</span></span>
<span data-ttu-id="b0080-130">Указывает, что имя группы ресурсов содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="b0080-130">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="b0080-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b0080-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="b0080-132">Массив объектов VirtualNetworkRule, которые нужно обновить, на свойство NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b0080-132">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0080-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0080-133">-Confirm</span></span>
<span data-ttu-id="b0080-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b0080-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0080-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0080-135">-WhatIf</span></span>
<span data-ttu-id="b0080-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b0080-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0080-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b0080-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0080-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0080-138">CommonParameters</span></span>
<span data-ttu-id="b0080-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b0080-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0080-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0080-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0080-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b0080-141">INPUTS</span></span>

### <span data-ttu-id="b0080-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b0080-142">System.String</span></span>

### <span data-ttu-id="b0080-143">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="b0080-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>
<span data-ttu-id="b0080-144">Параметры: IPRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b0080-144">Parameters: IPRule (ByValue)</span></span>

### <span data-ttu-id="b0080-145">Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="b0080-145">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>
<span data-ttu-id="b0080-146">Параметры: VirtualNetworkRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b0080-146">Parameters: VirtualNetworkRule (ByValue)</span></span>

## <span data-ttu-id="b0080-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0080-147">OUTPUTS</span></span>

### <span data-ttu-id="b0080-148">Microsoft. Azure. Commands. Management. Storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="b0080-148">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="b0080-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="b0080-149">NOTES</span></span>

## <span data-ttu-id="b0080-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0080-150">RELATED LINKS</span></span>