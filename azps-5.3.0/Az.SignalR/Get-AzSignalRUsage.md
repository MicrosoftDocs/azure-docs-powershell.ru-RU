---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/get-azsignalrusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Get-AzSignalRUsage.md
ms.openlocfilehash: 91910bc8a8c5135672e311bd1bb1c6367ccd14f3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506690"
---
# <span data-ttu-id="d3a11-101">Get-AzSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="d3a11-101">Get-AzSignalRUsage</span></span>

## <span data-ttu-id="d3a11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3a11-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a11-103">Получите квоту использования подписки.</span><span class="sxs-lookup"><span data-stu-id="d3a11-103">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="d3a11-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d3a11-104">SYNTAX</span></span>

```
Get-AzSignalRUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3a11-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3a11-105">DESCRIPTION</span></span>
<span data-ttu-id="d3a11-106">Получите квоту использования подписки.</span><span class="sxs-lookup"><span data-stu-id="d3a11-106">Get the usage quota of a subscription.</span></span>

## <span data-ttu-id="d3a11-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d3a11-107">EXAMPLES</span></span>

### <span data-ttu-id="d3a11-108">Получить квоту использования путем ввода данных о расположении</span><span class="sxs-lookup"><span data-stu-id="d3a11-108">Get the usage quota by inputting the location</span></span>
```powershell
PS C:\> Get-AzSignalRUsage eastus

Name                 CurrentValue Limit
----                 ------------ -----
FreeTierInstances    2            5
SignalRTotalUnits    3            300
```

## <span data-ttu-id="d3a11-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3a11-109">PARAMETERS</span></span>

### <span data-ttu-id="d3a11-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a11-110">-DefaultProfile</span></span>
<span data-ttu-id="d3a11-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3a11-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3a11-112">-Location</span><span class="sxs-lookup"><span data-stu-id="d3a11-112">-Location</span></span>
<span data-ttu-id="d3a11-113">Расположение службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="d3a11-113">The SignalR service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a11-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a11-114">CommonParameters</span></span>
<span data-ttu-id="d3a11-115">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3a11-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a11-116">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3a11-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a11-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3a11-117">INPUTS</span></span>

### <span data-ttu-id="d3a11-118">Нет</span><span class="sxs-lookup"><span data-stu-id="d3a11-118">None</span></span>

## <span data-ttu-id="d3a11-119">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d3a11-119">OUTPUTS</span></span>

### <span data-ttu-id="d3a11-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span><span class="sxs-lookup"><span data-stu-id="d3a11-120">Microsoft.Azure.Commands.SignalR.Models.PSSignalRUsage</span></span>

## <span data-ttu-id="d3a11-121">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d3a11-121">NOTES</span></span>

## <span data-ttu-id="d3a11-122">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3a11-122">RELATED LINKS</span></span>