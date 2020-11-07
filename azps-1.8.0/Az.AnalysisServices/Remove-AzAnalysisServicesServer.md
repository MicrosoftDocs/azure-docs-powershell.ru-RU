---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/remove-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Remove-AzAnalysisServicesServer.md
ms.openlocfilehash: b64ba86a6aab80910ac09bd3757565df433690dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720195"
---
# <span data-ttu-id="618ad-101">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="618ad-101">Remove-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="618ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="618ad-102">SYNOPSIS</span></span>
<span data-ttu-id="618ad-103">Удаляет экземпляр сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="618ad-103">Deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="618ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="618ad-104">SYNTAX</span></span>

```
Remove-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="618ad-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="618ad-105">DESCRIPTION</span></span>
<span data-ttu-id="618ad-106">Командлет Remove-AzAnalysisServicesServer удаляет экземпляр сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="618ad-106">The Remove-AzAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="618ad-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="618ad-107">EXAMPLES</span></span>

### <span data-ttu-id="618ad-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="618ad-108">Example 1</span></span>
```
PS C:\> Remove-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="618ad-109">Эта команда удалит сервер с именем TestServer в области "resourcegroup" testgroup</span><span class="sxs-lookup"><span data-stu-id="618ad-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="618ad-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="618ad-110">PARAMETERS</span></span>

### <span data-ttu-id="618ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="618ad-111">-DefaultProfile</span></span>
<span data-ttu-id="618ad-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="618ad-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="618ad-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="618ad-113">-Name</span></span>
<span data-ttu-id="618ad-114">Имя сервера служб Analysis Services</span><span class="sxs-lookup"><span data-stu-id="618ad-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="618ad-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="618ad-115">-PassThru</span></span>
<span data-ttu-id="618ad-116">При успешном завершении операции будут возвращены удаленные сведения о сервере.</span><span class="sxs-lookup"><span data-stu-id="618ad-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="618ad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="618ad-117">-ResourceGroupName</span></span>
<span data-ttu-id="618ad-118">Имя группы ресурсов Azure, к которой принадлежит сервер</span><span class="sxs-lookup"><span data-stu-id="618ad-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="618ad-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="618ad-119">-Confirm</span></span>
<span data-ttu-id="618ad-120">Предлагает пользователю подтвердить необходимость выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="618ad-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="618ad-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="618ad-121">-WhatIf</span></span>
<span data-ttu-id="618ad-122">Описывает действия, которые будет выполнять текущая операция без их фактического выполнения.</span><span class="sxs-lookup"><span data-stu-id="618ad-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="618ad-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="618ad-123">CommonParameters</span></span>
<span data-ttu-id="618ad-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="618ad-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="618ad-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="618ad-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="618ad-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="618ad-126">INPUTS</span></span>

### <span data-ttu-id="618ad-127">System. String</span><span class="sxs-lookup"><span data-stu-id="618ad-127">System.String</span></span>

## <span data-ttu-id="618ad-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="618ad-128">OUTPUTS</span></span>

### <span data-ttu-id="618ad-129">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="618ad-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="618ad-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="618ad-130">NOTES</span></span>
<span data-ttu-id="618ad-131">Alias (псевдоним): Remove-AzAs</span><span class="sxs-lookup"><span data-stu-id="618ad-131">Alias: Remove-AzAs</span></span>

## <span data-ttu-id="618ad-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="618ad-132">RELATED LINKS</span></span>

[<span data-ttu-id="618ad-133">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="618ad-133">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="618ad-134">New-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="618ad-134">New-AzAnalysisServicesServer</span></span>](./New-AzAnalysisServicesServer.md)