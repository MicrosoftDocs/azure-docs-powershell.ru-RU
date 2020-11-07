---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: 459ae0e3d18056c6579d4fd6248548155e1471cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563540"
---
# <span data-ttu-id="0cd30-101">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="0cd30-101">Set-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="0cd30-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0cd30-102">SYNOPSIS</span></span>
<span data-ttu-id="0cd30-103">Задает политику виртуальных машин на пользователя лаборатории в DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="0cd30-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cd30-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0cd30-104">SYNTAX</span></span>

### <span data-ttu-id="0cd30-105">Включить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0cd30-105">Enable (Default)</span></span>
```
Set-AzureRmDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cd30-106">Ключив</span><span class="sxs-lookup"><span data-stu-id="0cd30-106">Disable</span></span>
```
Set-AzureRmDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cd30-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0cd30-107">DESCRIPTION</span></span>
<span data-ttu-id="0cd30-108">Командлет **Set-AzureRmDtlVMsPerUserPolicy** задает максимальное количество виртуальных машин, разрешенных для одного пользователя, в пользовательском параметрах лаборатории для виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="0cd30-108">The **Set-AzureRmDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="0cd30-109">Для настройки политики командлет использует указанную группу ресурсов и имя лаборатории.</span><span class="sxs-lookup"><span data-stu-id="0cd30-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="0cd30-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0cd30-110">EXAMPLES</span></span>

## <span data-ttu-id="0cd30-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0cd30-111">PARAMETERS</span></span>

### <span data-ttu-id="0cd30-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cd30-112">-DefaultProfile</span></span>
<span data-ttu-id="0cd30-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0cd30-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cd30-114">-Отключение</span><span class="sxs-lookup"><span data-stu-id="0cd30-114">-Disable</span></span>
<span data-ttu-id="0cd30-115">Указывает на то, что этот командлет отключает политику для лаборатории.</span><span class="sxs-lookup"><span data-stu-id="0cd30-115">Indicates that this cmdlet disables the policy for the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disable
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cd30-116">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="0cd30-116">-Enable</span></span>
<span data-ttu-id="0cd30-117">Указывает на то, что этот командлет включает политику для лаборатории.</span><span class="sxs-lookup"><span data-stu-id="0cd30-117">Indicates that this cmdlet enables the policy for the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Enable
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cd30-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="0cd30-118">-LabName</span></span>
<span data-ttu-id="0cd30-119">Указывает имя лаборатории, для которой этот командлет задает политику виртуальных машин на пользователя.</span><span class="sxs-lookup"><span data-stu-id="0cd30-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cd30-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="0cd30-120">-MaxVMs</span></span>
<span data-ttu-id="0cd30-121">Указывает максимальное количество виртуальных машин, которые можно создать в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="0cd30-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cd30-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cd30-122">-ResourceGroupName</span></span>
<span data-ttu-id="0cd30-123">Указывает имя группы ресурсов, которой принадлежит лаборатория.</span><span class="sxs-lookup"><span data-stu-id="0cd30-123">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cd30-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0cd30-124">-Confirm</span></span>
<span data-ttu-id="0cd30-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0cd30-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cd30-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cd30-126">-WhatIf</span></span>
<span data-ttu-id="0cd30-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0cd30-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cd30-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0cd30-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cd30-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cd30-129">CommonParameters</span></span>
<span data-ttu-id="0cd30-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0cd30-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cd30-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cd30-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cd30-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0cd30-132">INPUTS</span></span>

### <span data-ttu-id="0cd30-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="0cd30-133">None</span></span>
<span data-ttu-id="0cd30-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="0cd30-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0cd30-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0cd30-135">OUTPUTS</span></span>

### <span data-ttu-id="0cd30-136">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="0cd30-136">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="0cd30-137">Этот командлет возвращает политику, указывающую максимальное количество виртуальных машин, которые могут быть созданы пользователем в лаборатории.</span><span class="sxs-lookup"><span data-stu-id="0cd30-137">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created by a user in the lab.</span></span>

## <span data-ttu-id="0cd30-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="0cd30-138">NOTES</span></span>

## <span data-ttu-id="0cd30-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0cd30-139">RELATED LINKS</span></span>

[<span data-ttu-id="0cd30-140">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="0cd30-140">Get-AzureRmDtlVMsPerUserPolicy</span></span>](./Get-AzureRmDtlVMsPerUserPolicy.md)

