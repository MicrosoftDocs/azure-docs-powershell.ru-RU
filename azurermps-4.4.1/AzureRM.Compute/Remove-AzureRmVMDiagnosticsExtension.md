---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
ms.openlocfilehash: 6a47e5a248c5de3c2dd87af67393f60d215e44c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557888"
---
# <span data-ttu-id="5230f-101">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5230f-101">Remove-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="5230f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5230f-102">SYNOPSIS</span></span>
<span data-ttu-id="5230f-103">Удаление расширения диагностики из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5230f-103">Removes the Diagnostics extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5230f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5230f-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5230f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5230f-105">DESCRIPTION</span></span>
<span data-ttu-id="5230f-106">Командлет **Remove-AzureRmVMDiagnosticsExtension** удаляет расширение диагностики Azure из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5230f-106">The **Remove-AzureRmVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="5230f-107">Для реализации изменений необходимо передать результат этого командлета в командлет Update-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="5230f-107">You must pass the output of this cmdlet to the Update-AzureRmVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="5230f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5230f-108">EXAMPLES</span></span>

### <span data-ttu-id="5230f-109">Пример 1: удаление расширения диагностики из виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="5230f-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzureRmVM
```

<span data-ttu-id="5230f-110">Эта команда удаляет расширение диагностики из виртуальной машины с именем ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="5230f-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="5230f-111">Команда передает результат в командлет Update-AzureRmVM с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="5230f-111">The command passes the result to the Update-AzureRmVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5230f-112">Эта команда обновляет виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="5230f-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="5230f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5230f-113">PARAMETERS</span></span>

### <span data-ttu-id="5230f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5230f-114">-DefaultProfile</span></span>
<span data-ttu-id="5230f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5230f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5230f-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5230f-116">-Name</span></span>
<span data-ttu-id="5230f-117">Указывает имя расширения диагностики, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5230f-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5230f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5230f-118">-ResourceGroupName</span></span>
<span data-ttu-id="5230f-119">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5230f-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5230f-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="5230f-120">-VMName</span></span>
<span data-ttu-id="5230f-121">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение диагностики.</span><span class="sxs-lookup"><span data-stu-id="5230f-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="5230f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5230f-122">CommonParameters</span></span>
<span data-ttu-id="5230f-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5230f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5230f-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5230f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5230f-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5230f-125">INPUTS</span></span>

## <span data-ttu-id="5230f-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5230f-126">OUTPUTS</span></span>

## <span data-ttu-id="5230f-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="5230f-127">NOTES</span></span>

## <span data-ttu-id="5230f-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5230f-128">RELATED LINKS</span></span>

[<span data-ttu-id="5230f-129">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5230f-129">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="5230f-130">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5230f-130">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="5230f-131">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5230f-131">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

