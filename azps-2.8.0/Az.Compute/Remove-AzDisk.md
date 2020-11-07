---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
ms.openlocfilehash: 46cbb87d54d1eb80857d3d0fbc786cb8296f4ac0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721801"
---
# <span data-ttu-id="eac53-101">Remove-AzDisk</span><span class="sxs-lookup"><span data-stu-id="eac53-101">Remove-AzDisk</span></span>

## <span data-ttu-id="eac53-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eac53-102">SYNOPSIS</span></span>
<span data-ttu-id="eac53-103">Удаление диска.</span><span class="sxs-lookup"><span data-stu-id="eac53-103">Removes a disk.</span></span>

## <span data-ttu-id="eac53-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eac53-104">SYNTAX</span></span>

```
Remove-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eac53-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eac53-105">DESCRIPTION</span></span>
<span data-ttu-id="eac53-106">Командлет **Remove-AzDisk** удаляет диск.</span><span class="sxs-lookup"><span data-stu-id="eac53-106">The **Remove-AzDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="eac53-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eac53-107">EXAMPLES</span></span>

### <span data-ttu-id="eac53-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eac53-108">Example 1</span></span>
```
PS C:\> Remove-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="eac53-109">Эта команда удаляет диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="eac53-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="eac53-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eac53-110">PARAMETERS</span></span>

### <span data-ttu-id="eac53-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eac53-111">-AsJob</span></span>
<span data-ttu-id="eac53-112">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="eac53-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="eac53-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eac53-113">-DefaultProfile</span></span>
<span data-ttu-id="eac53-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eac53-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eac53-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="eac53-115">-DiskName</span></span>
<span data-ttu-id="eac53-116">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="eac53-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="eac53-117">-Force</span><span class="sxs-lookup"><span data-stu-id="eac53-117">-Force</span></span>
<span data-ttu-id="eac53-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="eac53-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eac53-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eac53-119">-ResourceGroupName</span></span>
<span data-ttu-id="eac53-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eac53-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="eac53-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eac53-121">-Confirm</span></span>
<span data-ttu-id="eac53-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eac53-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eac53-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eac53-123">-WhatIf</span></span>
<span data-ttu-id="eac53-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eac53-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eac53-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eac53-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eac53-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eac53-126">CommonParameters</span></span>
<span data-ttu-id="eac53-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eac53-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eac53-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eac53-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eac53-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eac53-129">INPUTS</span></span>

### <span data-ttu-id="eac53-130">System. String</span><span class="sxs-lookup"><span data-stu-id="eac53-130">System.String</span></span>

## <span data-ttu-id="eac53-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eac53-131">OUTPUTS</span></span>

### <span data-ttu-id="eac53-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="eac53-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="eac53-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="eac53-133">NOTES</span></span>

## <span data-ttu-id="eac53-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eac53-134">RELATED LINKS</span></span>