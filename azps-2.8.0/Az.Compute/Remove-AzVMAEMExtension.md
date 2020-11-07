---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 343ecb5159b252c97af05cffc89152e05028583b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721779"
---
# <span data-ttu-id="027a5-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="027a5-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="027a5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="027a5-102">SYNOPSIS</span></span>
<span data-ttu-id="027a5-103">Удаляет расширение AEM из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="027a5-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="027a5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="027a5-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="027a5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="027a5-105">DESCRIPTION</span></span>
<span data-ttu-id="027a5-106">Командлет **Remove-AzVMAEMExtension** удаляет расширение службы улучшенного мониторинга Azure (AEM) с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="027a5-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="027a5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="027a5-107">EXAMPLES</span></span>

### <span data-ttu-id="027a5-108">Пример 1: удаление расширения AEM</span><span class="sxs-lookup"><span data-stu-id="027a5-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="027a5-109">Эта команда удаляет расширение AEM для виртуальной машины с именем Contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="027a5-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="027a5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="027a5-110">PARAMETERS</span></span>

### <span data-ttu-id="027a5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="027a5-111">-DefaultProfile</span></span>
<span data-ttu-id="027a5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="027a5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="027a5-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="027a5-113">-Name</span></span>
<span data-ttu-id="027a5-114">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение AEM.</span><span class="sxs-lookup"><span data-stu-id="027a5-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="027a5-115">-Wait</span><span class="sxs-lookup"><span data-stu-id="027a5-115">-NoWait</span></span>
<span data-ttu-id="027a5-116">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="027a5-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="027a5-117">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="027a5-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="027a5-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="027a5-118">-OSType</span></span>
<span data-ttu-id="027a5-119">Указывает тип операционной системы диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="027a5-119">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="027a5-120">Если диск операционной системы не имеет типа, необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="027a5-120">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="027a5-121">Допустимые значения этого параметра: Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="027a5-121">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="027a5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="027a5-122">-ResourceGroupName</span></span>
<span data-ttu-id="027a5-123">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="027a5-123">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="027a5-124">Этот командлет удаляет расширение AEM из этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="027a5-124">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="027a5-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="027a5-125">-VMName</span></span>
<span data-ttu-id="027a5-126">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="027a5-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="027a5-127">Этот командлет удаляет расширение AEM для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="027a5-127">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="027a5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="027a5-128">CommonParameters</span></span>
<span data-ttu-id="027a5-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="027a5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="027a5-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="027a5-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="027a5-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="027a5-131">INPUTS</span></span>

### <span data-ttu-id="027a5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="027a5-132">System.String</span></span>

## <span data-ttu-id="027a5-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="027a5-133">OUTPUTS</span></span>

### <span data-ttu-id="027a5-134">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="027a5-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="027a5-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="027a5-135">NOTES</span></span>

## <span data-ttu-id="027a5-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="027a5-136">RELATED LINKS</span></span>

[<span data-ttu-id="027a5-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="027a5-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="027a5-138">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="027a5-138">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="027a5-139">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="027a5-139">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)

