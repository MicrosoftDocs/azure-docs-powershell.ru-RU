---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/remove-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
ms.openlocfilehash: ba474ca3ea3a975262eec8b98df1fb99b0f336cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720384"
---
# <span data-ttu-id="fa79b-101">Remove-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="fa79b-101">Remove-AzMapsAccount</span></span>

## <span data-ttu-id="fa79b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fa79b-102">SYNOPSIS</span></span>
<span data-ttu-id="fa79b-103">Удаление учетной записи карт Azure.</span><span class="sxs-lookup"><span data-stu-id="fa79b-103">Deletes an Azure Maps account.</span></span>

## <span data-ttu-id="fa79b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fa79b-104">SYNTAX</span></span>

### <span data-ttu-id="fa79b-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fa79b-105">NameParameterSet (Default)</span></span>
```
Remove-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa79b-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa79b-106">InputObjectParameterSet</span></span>
```
Remove-AzMapsAccount [-InputObject <PSMapsAccount>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa79b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa79b-107">ResourceIdParameterSet</span></span>
```
Remove-AzMapsAccount [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa79b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa79b-108">DESCRIPTION</span></span>
<span data-ttu-id="fa79b-109">Командлет Remove-AzMapsAccount удаляет указанную учетную запись карт Azure.</span><span class="sxs-lookup"><span data-stu-id="fa79b-109">The Remove-AzMapsAccount cmdlet deletes the specified Azure Maps account.</span></span>

## <span data-ttu-id="fa79b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fa79b-110">EXAMPLES</span></span>

### <span data-ttu-id="fa79b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fa79b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="fa79b-112">Удаление учетной записи Моя учетная запись из группы ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fa79b-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="fa79b-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fa79b-113">Example 2</span></span>
```
PS C:\> Remove-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="fa79b-114">Удаляет указанную учетную запись карт Azure.</span><span class="sxs-lookup"><span data-stu-id="fa79b-114">Deletes the specified Azure Maps Account.</span></span>

## <span data-ttu-id="fa79b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fa79b-115">PARAMETERS</span></span>

### <span data-ttu-id="fa79b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa79b-116">-DefaultProfile</span></span>
<span data-ttu-id="fa79b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fa79b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa79b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa79b-118">-InputObject</span></span>
<span data-ttu-id="fa79b-119">Карты сопоставляются с учетной записью Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="fa79b-119">Maps Account piped from Get-AzMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa79b-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fa79b-120">-Name</span></span>
<span data-ttu-id="fa79b-121">Имя учетной записи карты.</span><span class="sxs-lookup"><span data-stu-id="fa79b-121">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa79b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa79b-122">-PassThru</span></span>
<span data-ttu-id="fa79b-123">Возвращает данные о том, успешно ли удалена указанная учетная запись.</span><span class="sxs-lookup"><span data-stu-id="fa79b-123">Return whether the specified account was successfully deleted or not.</span></span>

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

### <span data-ttu-id="fa79b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa79b-124">-ResourceGroupName</span></span>
<span data-ttu-id="fa79b-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fa79b-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa79b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa79b-126">-ResourceId</span></span>
<span data-ttu-id="fa79b-127">Карта ResourceId для счета.</span><span class="sxs-lookup"><span data-stu-id="fa79b-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa79b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa79b-128">-Confirm</span></span>
<span data-ttu-id="fa79b-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fa79b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa79b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa79b-130">-WhatIf</span></span>
<span data-ttu-id="fa79b-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fa79b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa79b-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fa79b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa79b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa79b-133">CommonParameters</span></span>
<span data-ttu-id="fa79b-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fa79b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa79b-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa79b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa79b-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fa79b-136">INPUTS</span></span>

### <span data-ttu-id="fa79b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fa79b-137">System.String</span></span>

### <span data-ttu-id="fa79b-138">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="fa79b-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="fa79b-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa79b-139">OUTPUTS</span></span>

### <span data-ttu-id="fa79b-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fa79b-140">System.Boolean</span></span>

## <span data-ttu-id="fa79b-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="fa79b-141">NOTES</span></span>

## <span data-ttu-id="fa79b-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa79b-142">RELATED LINKS</span></span>