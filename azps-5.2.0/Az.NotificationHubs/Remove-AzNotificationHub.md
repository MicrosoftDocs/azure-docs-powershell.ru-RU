---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
ms.openlocfilehash: 66f3dae7d92b9db18db418bf9de62671f084b7c0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404887"
---
# <span data-ttu-id="4a81a-101">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="4a81a-101">Remove-AzNotificationHub</span></span>

## <span data-ttu-id="4a81a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a81a-102">SYNOPSIS</span></span>
<span data-ttu-id="4a81a-103">Удаляет существующий концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="4a81a-103">Removes an existing notification hub.</span></span>

## <span data-ttu-id="4a81a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4a81a-104">SYNTAX</span></span>

```
Remove-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a81a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a81a-105">DESCRIPTION</span></span>
<span data-ttu-id="4a81a-106">Для удаления существующего концентратора уведомлений удаляется существующий **cmdlet Remove-AzNotificationHub.**</span><span class="sxs-lookup"><span data-stu-id="4a81a-106">The **Remove-AzNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="4a81a-107">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам независимо от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="4a81a-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="4a81a-108">В число платформ входят, среди среди них iOS, Android, Windows Phone 8 и Магазин Windows.</span><span class="sxs-lookup"><span data-stu-id="4a81a-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="4a81a-109">Концентраторы уведомлений примерно равны отдельным приложениям: в каждом из приложений обычно имеется собственный концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="4a81a-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="4a81a-110">Вы можете удалить существующий концентратор уведомлений с помощью **cmdlet Remove-AzNotificationHub.**</span><span class="sxs-lookup"><span data-stu-id="4a81a-110">You can remove an existing notification hub by using the **Remove-AzNotificationHub** cmdlet.</span></span>
<span data-ttu-id="4a81a-111">После удаления концентратора его больше нельзя использовать для отправки push-уведомлений пользователям.</span><span class="sxs-lookup"><span data-stu-id="4a81a-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="4a81a-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4a81a-112">EXAMPLES</span></span>

### <span data-ttu-id="4a81a-113">Пример 1. Удаление концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="4a81a-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="4a81a-114">Эта команда удаляет концентратор уведомлений ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="4a81a-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="4a81a-115">Чтобы удалить центр, необходимо указать пространство имен, в котором он расположен, а также группу ресурсов, которой он назначен.</span><span class="sxs-lookup"><span data-stu-id="4a81a-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="4a81a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a81a-116">PARAMETERS</span></span>

### <span data-ttu-id="4a81a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a81a-117">-DefaultProfile</span></span>
<span data-ttu-id="4a81a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4a81a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a81a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4a81a-119">-Force</span></span>
<span data-ttu-id="4a81a-120">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="4a81a-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4a81a-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4a81a-121">-Namespace</span></span>
<span data-ttu-id="4a81a-122">Определяет пространство имен, которому назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="4a81a-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="4a81a-123">Пространства имен предоставляют возможность группировать и классифицировать концентраторы уведомлений.</span><span class="sxs-lookup"><span data-stu-id="4a81a-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="4a81a-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="4a81a-124">-NotificationHub</span></span>
<span data-ttu-id="4a81a-125">Указывает, что концентратор уведомлений будет удален.</span><span class="sxs-lookup"><span data-stu-id="4a81a-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="4a81a-126">Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам независимо от платформы, используемой этими клиентами.</span><span class="sxs-lookup"><span data-stu-id="4a81a-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="4a81a-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4a81a-127">-ResourceGroup</span></span>
<span data-ttu-id="4a81a-128">Группа ресурсов, которой назначен концентратор уведомлений.</span><span class="sxs-lookup"><span data-stu-id="4a81a-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="4a81a-129">Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, чтобы упрость управление запасами и администрирование Azure.</span><span class="sxs-lookup"><span data-stu-id="4a81a-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="4a81a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a81a-130">-Confirm</span></span>
<span data-ttu-id="4a81a-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a81a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a81a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a81a-132">-WhatIf</span></span>
<span data-ttu-id="4a81a-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a81a-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a81a-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4a81a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a81a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a81a-135">CommonParameters</span></span>
<span data-ttu-id="4a81a-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a81a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a81a-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a81a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a81a-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a81a-138">INPUTS</span></span>

### <span data-ttu-id="4a81a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4a81a-139">System.String</span></span>

## <span data-ttu-id="4a81a-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4a81a-140">OUTPUTS</span></span>

### <span data-ttu-id="4a81a-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="4a81a-141">System.Void</span></span>

## <span data-ttu-id="4a81a-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4a81a-142">NOTES</span></span>

## <span data-ttu-id="4a81a-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a81a-143">RELATED LINKS</span></span>

[<span data-ttu-id="4a81a-144">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="4a81a-144">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="4a81a-145">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="4a81a-145">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="4a81a-146">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="4a81a-146">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)

