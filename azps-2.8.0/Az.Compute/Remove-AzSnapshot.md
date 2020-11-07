---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
ms.openlocfilehash: 4e9a427a6e78848858773a1c661b949f91f0ffff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721783"
---
# <span data-ttu-id="94725-101">Remove-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="94725-101">Remove-AzSnapshot</span></span>

## <span data-ttu-id="94725-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94725-102">SYNOPSIS</span></span>
<span data-ttu-id="94725-103">Удаляет снимок.</span><span class="sxs-lookup"><span data-stu-id="94725-103">Removes a snapshot.</span></span>

## <span data-ttu-id="94725-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94725-104">SYNTAX</span></span>

```
Remove-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94725-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94725-105">DESCRIPTION</span></span>
<span data-ttu-id="94725-106">Командлет **Remove-AzSnapshot** удаляет моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="94725-106">The **Remove-AzSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="94725-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94725-107">EXAMPLES</span></span>

### <span data-ttu-id="94725-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="94725-108">Example 1</span></span>
```
PS C:\> Remove-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="94725-109">Эта команда удаляет моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="94725-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="94725-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94725-110">PARAMETERS</span></span>

### <span data-ttu-id="94725-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94725-111">-AsJob</span></span>
<span data-ttu-id="94725-112">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="94725-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="94725-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94725-113">-DefaultProfile</span></span>
<span data-ttu-id="94725-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94725-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94725-115">-Force</span><span class="sxs-lookup"><span data-stu-id="94725-115">-Force</span></span>
<span data-ttu-id="94725-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="94725-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="94725-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94725-117">-ResourceGroupName</span></span>
<span data-ttu-id="94725-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94725-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="94725-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="94725-119">-SnapshotName</span></span>
<span data-ttu-id="94725-120">Указывает имя снимка.</span><span class="sxs-lookup"><span data-stu-id="94725-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="94725-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94725-121">-Confirm</span></span>
<span data-ttu-id="94725-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="94725-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94725-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94725-123">-WhatIf</span></span>
<span data-ttu-id="94725-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="94725-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94725-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="94725-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94725-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94725-126">CommonParameters</span></span>
<span data-ttu-id="94725-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94725-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94725-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94725-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94725-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94725-129">INPUTS</span></span>

### <span data-ttu-id="94725-130">System. String</span><span class="sxs-lookup"><span data-stu-id="94725-130">System.String</span></span>

## <span data-ttu-id="94725-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94725-131">OUTPUTS</span></span>

### <span data-ttu-id="94725-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="94725-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="94725-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="94725-133">NOTES</span></span>

## <span data-ttu-id="94725-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94725-134">RELATED LINKS</span></span>