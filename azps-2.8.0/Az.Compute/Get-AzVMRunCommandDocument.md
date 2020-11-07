---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 3b66cdc6574397de7d43dfef0677a5ddac772a31
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721891"
---
# <span data-ttu-id="13061-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="13061-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="13061-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13061-102">SYNOPSIS</span></span>
<span data-ttu-id="13061-103">Получение документа команды "выполнить".</span><span class="sxs-lookup"><span data-stu-id="13061-103">Get a run command document.</span></span>

## <span data-ttu-id="13061-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13061-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13061-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13061-105">DESCRIPTION</span></span>
<span data-ttu-id="13061-106">Получение документа команды "выполнить".</span><span class="sxs-lookup"><span data-stu-id="13061-106">Get a run command document.</span></span>

## <span data-ttu-id="13061-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13061-107">EXAMPLES</span></span>

### <span data-ttu-id="13061-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="13061-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="13061-109">Возвращает определенный документ команды запуска для "RunPowerShellScript" в "westus".</span><span class="sxs-lookup"><span data-stu-id="13061-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>

### <span data-ttu-id="13061-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="13061-110">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="13061-111">Список всех доступных команд выполнения в "westus".</span><span class="sxs-lookup"><span data-stu-id="13061-111">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="13061-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13061-112">PARAMETERS</span></span>

### <span data-ttu-id="13061-113">-CommandId</span><span class="sxs-lookup"><span data-stu-id="13061-113">-CommandId</span></span>
<span data-ttu-id="13061-114">Идентификатор команды.</span><span class="sxs-lookup"><span data-stu-id="13061-114">The command ID.</span></span>

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

### <span data-ttu-id="13061-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13061-115">-DefaultProfile</span></span>
<span data-ttu-id="13061-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13061-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13061-117">-Location</span><span class="sxs-lookup"><span data-stu-id="13061-117">-Location</span></span>
<span data-ttu-id="13061-118">Расположение, в котором запрашиваются команды выполнения.</span><span class="sxs-lookup"><span data-stu-id="13061-118">The location upon which run commands are queried.</span></span>

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

### <span data-ttu-id="13061-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13061-119">CommonParameters</span></span>
<span data-ttu-id="13061-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13061-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13061-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13061-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13061-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13061-122">INPUTS</span></span>

### <span data-ttu-id="13061-123">System. String</span><span class="sxs-lookup"><span data-stu-id="13061-123">System.String</span></span>

## <span data-ttu-id="13061-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13061-124">OUTPUTS</span></span>

### <span data-ttu-id="13061-125">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="13061-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="13061-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="13061-126">NOTES</span></span>

## <span data-ttu-id="13061-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13061-127">RELATED LINKS</span></span>