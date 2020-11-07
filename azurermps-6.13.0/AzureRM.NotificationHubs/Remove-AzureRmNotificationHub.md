---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
ms.openlocfilehash: f4dc14fd922852fa67085588c78847623eb5eb64
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564176"
---
# <span data-ttu-id="bd26b-101">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="bd26b-101">Remove-AzureRmNotificationHub</span></span>

## <span data-ttu-id="bd26b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd26b-102">SYNOPSIS</span></span>
<span data-ttu-id="bd26b-103">Удаляет существующий концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="bd26b-103">Removes an existing notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd26b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd26b-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd26b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd26b-105">DESCRIPTION</span></span>
<span data-ttu-id="bd26b-106">Командлет **Remove-AzureRmNotificationHub** удаляет существующий концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="bd26b-106">The **Remove-AzureRmNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="bd26b-107">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="bd26b-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="bd26b-108">Платформы включают, но не ограничиваются: iOS, Android, Windows Phone 8 и магазин Windows.</span><span class="sxs-lookup"><span data-stu-id="bd26b-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="bd26b-109">Концентраторы уведомлений примерно эквивалентны отдельным приложениям: каждое из ваших приложений обычно имеет собственный концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="bd26b-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="bd26b-110">Вы можете удалить существующий центр уведомлений с помощью командлета **Remove-AzureRmNotificationHub** .</span><span class="sxs-lookup"><span data-stu-id="bd26b-110">You can remove an existing notification hub by using the **Remove-AzureRmNotificationHub** cmdlet.</span></span>
<span data-ttu-id="bd26b-111">После того как концентратор будет удален, вы больше не сможете использовать этот концентратор для отправки push-уведомлений пользователям.</span><span class="sxs-lookup"><span data-stu-id="bd26b-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="bd26b-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd26b-112">EXAMPLES</span></span>

### <span data-ttu-id="bd26b-113">Пример 1: удаление концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="bd26b-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="bd26b-114">Эта команда удаляет концентратор уведомлений с именем ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="bd26b-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="bd26b-115">Для удаления концентратора необходимо указать пространство имен, в котором расположен концентратор, а также группу ресурсов, которой назначен концентратор.</span><span class="sxs-lookup"><span data-stu-id="bd26b-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="bd26b-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd26b-116">PARAMETERS</span></span>

### <span data-ttu-id="bd26b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd26b-117">-DefaultProfile</span></span>
<span data-ttu-id="bd26b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bd26b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd26b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="bd26b-119">-Force</span></span>
<span data-ttu-id="bd26b-120">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="bd26b-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bd26b-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bd26b-121">-Namespace</span></span>
<span data-ttu-id="bd26b-122">Задает пространство имен, которому назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="bd26b-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="bd26b-123">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="bd26b-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd26b-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="bd26b-124">-NotificationHub</span></span>
<span data-ttu-id="bd26b-125">Указывает удаляемый центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="bd26b-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="bd26b-126">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="bd26b-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd26b-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bd26b-127">-ResourceGroup</span></span>
<span data-ttu-id="bd26b-128">Указывает группу ресурсов, которой назначен Центр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="bd26b-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="bd26b-129">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="bd26b-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="bd26b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd26b-130">-Confirm</span></span>
<span data-ttu-id="bd26b-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bd26b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd26b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd26b-132">-WhatIf</span></span>
<span data-ttu-id="bd26b-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bd26b-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd26b-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bd26b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd26b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd26b-135">CommonParameters</span></span>
<span data-ttu-id="bd26b-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd26b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd26b-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd26b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd26b-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd26b-138">INPUTS</span></span>

### <span data-ttu-id="bd26b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bd26b-139">System.String</span></span>

## <span data-ttu-id="bd26b-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd26b-140">OUTPUTS</span></span>

### <span data-ttu-id="bd26b-141">System. void</span><span class="sxs-lookup"><span data-stu-id="bd26b-141">System.Void</span></span>

## <span data-ttu-id="bd26b-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd26b-142">NOTES</span></span>

## <span data-ttu-id="bd26b-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd26b-143">RELATED LINKS</span></span>

[<span data-ttu-id="bd26b-144">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="bd26b-144">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="bd26b-145">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="bd26b-145">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="bd26b-146">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="bd26b-146">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)

