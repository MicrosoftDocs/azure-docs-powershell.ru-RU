---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActionGroup.md
ms.openlocfilehash: 90bd9c7943e6e788d81f8ddec85513676afade23
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413820"
---
# <span data-ttu-id="9e208-101">Get-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="9e208-101">Get-AzActionGroup</span></span>

## <span data-ttu-id="9e208-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e208-102">SYNOPSIS</span></span>
<span data-ttu-id="9e208-103">Получает группы действий.</span><span class="sxs-lookup"><span data-stu-id="9e208-103">Gets action group(s).</span></span>

## <span data-ttu-id="9e208-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9e208-104">SYNTAX</span></span>

### <span data-ttu-id="9e208-105">BySubscriptionOrResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9e208-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e208-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9e208-106">ByName</span></span>
```
Get-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e208-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e208-107">DESCRIPTION</span></span>
<span data-ttu-id="9e208-108">Для получения одной или более групп действий возвращается **cmdlet Get-AzActionGroup.**</span><span class="sxs-lookup"><span data-stu-id="9e208-108">The **Get-AzActionGroup** cmdlet gets one or more action groups.</span></span>

## <span data-ttu-id="9e208-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9e208-109">EXAMPLES</span></span>

### <span data-ttu-id="9e208-110">Пример 1. Получить группу действий по ИД подписки</span><span class="sxs-lookup"><span data-stu-id="9e208-110">Example 1: Get an action group by subscription ID</span></span>
```
PS C:\>Get-AzActionGroup
```

<span data-ttu-id="9e208-111">Эта команда содержит список всех групп действий для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="9e208-111">This command lists all the action group for the current subscription.</span></span>

### <span data-ttu-id="9e208-112">Пример 2. Получить группы действий для данной группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9e208-112">Example 2: Get action groups for the given resource group</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts"
```

<span data-ttu-id="9e208-113">В этой команде перечислены группы действий для заданной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e208-113">This command lists action groups for the given resource group.</span></span>

### <span data-ttu-id="9e208-114">Пример 3. Получить группу действий.</span><span class="sxs-lookup"><span data-stu-id="9e208-114">Example 3: Get an action group.</span></span>
```
PS C:\>Get-AzActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

<span data-ttu-id="9e208-115">Эта команда содержит одну группу (список с одним элементом).</span><span class="sxs-lookup"><span data-stu-id="9e208-115">This command lists one (a list with a single element) action group.</span></span>

## <span data-ttu-id="9e208-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e208-116">PARAMETERS</span></span>

### <span data-ttu-id="9e208-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e208-117">-DefaultProfile</span></span>
<span data-ttu-id="9e208-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9e208-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e208-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9e208-119">-Name</span></span>
<span data-ttu-id="9e208-120">Имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="9e208-120">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e208-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e208-121">-ResourceGroupName</span></span>
<span data-ttu-id="9e208-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9e208-122">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e208-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e208-123">CommonParameters</span></span>
<span data-ttu-id="9e208-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e208-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e208-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e208-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e208-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e208-126">INPUTS</span></span>

### <span data-ttu-id="9e208-127">System.String</span><span class="sxs-lookup"><span data-stu-id="9e208-127">System.String</span></span>

## <span data-ttu-id="9e208-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9e208-128">OUTPUTS</span></span>

### <span data-ttu-id="9e208-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="9e208-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="9e208-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9e208-130">NOTES</span></span>

## <span data-ttu-id="9e208-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e208-131">RELATED LINKS</span></span>

<span data-ttu-id="9e208-132">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="9e208-132">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>