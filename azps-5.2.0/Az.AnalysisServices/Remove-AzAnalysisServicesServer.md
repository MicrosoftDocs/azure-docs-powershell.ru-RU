---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/remove-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
ms.openlocfilehash: 9076df0ae023539560b690723dd9abc92d922e45
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406420"
---
# <span data-ttu-id="d4eba-101">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d4eba-101">Remove-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="d4eba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4eba-102">SYNOPSIS</span></span>
<span data-ttu-id="d4eba-103">Удаление экземпляра сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="d4eba-103">Deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="d4eba-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d4eba-104">SYNTAX</span></span>

```
Remove-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4eba-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4eba-105">DESCRIPTION</span></span>
<span data-ttu-id="d4eba-106">С Remove-AzAnalysisServicesServer-сервера служб Analysis Services удаляется экземпляр</span><span class="sxs-lookup"><span data-stu-id="d4eba-106">The Remove-AzAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="d4eba-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d4eba-107">EXAMPLES</span></span>

### <span data-ttu-id="d4eba-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d4eba-108">Example 1</span></span>
```
PS C:\> Remove-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="d4eba-109">Эта команда удаляет сервер testerver из тестовой группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d4eba-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="d4eba-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4eba-110">PARAMETERS</span></span>

### <span data-ttu-id="d4eba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4eba-111">-DefaultProfile</span></span>
<span data-ttu-id="d4eba-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4eba-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4eba-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d4eba-113">-Name</span></span>
<span data-ttu-id="d4eba-114">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="d4eba-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="d4eba-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4eba-115">-PassThru</span></span>
<span data-ttu-id="d4eba-116">Возвращает удаленные сведения о сервере, если операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="d4eba-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="d4eba-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4eba-117">-ResourceGroupName</span></span>
<span data-ttu-id="d4eba-118">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="d4eba-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="d4eba-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4eba-119">-Confirm</span></span>
<span data-ttu-id="d4eba-120">Запрос на подтверждение выполнения операции</span><span class="sxs-lookup"><span data-stu-id="d4eba-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="d4eba-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4eba-121">-WhatIf</span></span>
<span data-ttu-id="d4eba-122">В нем описываются действия, выполняемые в ходе текущей операции без их выполнения.</span><span class="sxs-lookup"><span data-stu-id="d4eba-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="d4eba-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4eba-123">CommonParameters</span></span>
<span data-ttu-id="d4eba-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4eba-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4eba-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4eba-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4eba-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4eba-126">INPUTS</span></span>

### <span data-ttu-id="d4eba-127">System.String</span><span class="sxs-lookup"><span data-stu-id="d4eba-127">System.String</span></span>

## <span data-ttu-id="d4eba-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d4eba-128">OUTPUTS</span></span>

### <span data-ttu-id="d4eba-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d4eba-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="d4eba-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d4eba-130">NOTES</span></span>
<span data-ttu-id="d4eba-131">Псевдоним: Remove-AzAs</span><span class="sxs-lookup"><span data-stu-id="d4eba-131">Alias: Remove-AzAs</span></span>

## <span data-ttu-id="d4eba-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4eba-132">RELATED LINKS</span></span>

[<span data-ttu-id="d4eba-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d4eba-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="d4eba-134">New-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="d4eba-134">New-AzAnalysisServicesServer</span></span>](./New-AzAnalysisServicesServer.md)