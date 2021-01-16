---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationOrder.md
ms.openlocfilehash: 15faf94ae7e0afac7200423dcd36d8edf2964c21
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506728"
---
# <span data-ttu-id="c5e75-101">Get-AzReservationOrder</span><span class="sxs-lookup"><span data-stu-id="c5e75-101">Get-AzReservationOrder</span></span>

## <span data-ttu-id="c5e75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5e75-102">SYNOPSIS</span></span>
<span data-ttu-id="c5e75-103">Получить `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="c5e75-103">Get `ReservationOrder`</span></span>

## <span data-ttu-id="c5e75-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c5e75-104">SYNTAX</span></span>

```
Get-AzReservationOrder [-ReservationOrderId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5e75-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5e75-105">DESCRIPTION</span></span>
<span data-ttu-id="c5e75-106">Список всех `ReservationOrder` клиентов, к которые у пользователя есть доступ в текущем клиенте.</span><span class="sxs-lookup"><span data-stu-id="c5e75-106">List of all the `ReservationOrder`s that the user has access to in the current tenant.</span></span> <span data-ttu-id="c5e75-107">Если параметр ReservationOrderId задан, получите определенный резервирование.</span><span class="sxs-lookup"><span data-stu-id="c5e75-107">If ReservationOrderId parameter is set, get that specific ReservationOrder.</span></span>

## <span data-ttu-id="c5e75-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c5e75-108">EXAMPLES</span></span>

### <span data-ttu-id="c5e75-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c5e75-109">Example 1</span></span>
```
PS C:\> Get-AzReservationOrder
```

<span data-ttu-id="c5e75-110">`ReservationOrder`Укаймь все, к чем у пользователя есть доступ в текущем клиенте</span><span class="sxs-lookup"><span data-stu-id="c5e75-110">List all `ReservationOrder` that the user has access to in the current tenant</span></span>

### <span data-ttu-id="c5e75-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c5e75-111">Example 2</span></span>
```
PS C:\> Get-AzReservationOrder -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff"
```

<span data-ttu-id="c5e75-112">Получить `ReservationOrder` с указанным ИД Резервирования</span><span class="sxs-lookup"><span data-stu-id="c5e75-112">Get `ReservationOrder` with the specified ReservationOrderId</span></span>

## <span data-ttu-id="c5e75-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5e75-113">PARAMETERS</span></span>

### <span data-ttu-id="c5e75-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5e75-114">-DefaultProfile</span></span>
<span data-ttu-id="c5e75-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c5e75-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5e75-116">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="c5e75-116">-ReservationOrderId</span></span>
<span data-ttu-id="c5e75-117">Id of the specific ReservationOrder that user wants to see</span><span class="sxs-lookup"><span data-stu-id="c5e75-117">Id of the specific ReservationOrder that user wants to see</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e75-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5e75-118">CommonParameters</span></span>
<span data-ttu-id="c5e75-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5e75-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5e75-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5e75-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5e75-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5e75-121">INPUTS</span></span>

### <span data-ttu-id="c5e75-122">Нет</span><span class="sxs-lookup"><span data-stu-id="c5e75-122">None</span></span>

## <span data-ttu-id="c5e75-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c5e75-123">OUTPUTS</span></span>

### <span data-ttu-id="c5e75-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="c5e75-124">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

### <span data-ttu-id="c5e75-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="c5e75-125">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

## <span data-ttu-id="c5e75-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c5e75-126">NOTES</span></span>

## <span data-ttu-id="c5e75-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5e75-127">RELATED LINKS</span></span>