---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: b1217a9ca49d81cf084d97983e8ec5ebd99ed84a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562371"
---
# <span data-ttu-id="8add1-101">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="8add1-101">Get-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="8add1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8add1-102">SYNOPSIS</span></span>
<span data-ttu-id="8add1-103">Получает сведения о пространстве имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8add1-103">Gets information about a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8add1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8add1-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8add1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8add1-105">DESCRIPTION</span></span>
<span data-ttu-id="8add1-106">Командлет **Get-AzureRmNotificationHubsNamespace** получает сведения о пространствах имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8add1-106">**The Get-AzureRmNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="8add1-107">Этот командлет предоставляет возможность получения сведений обо всех пространствах имен, а также сведения о пространствах имен, назначенных определенной группе ресурсов; или для возврата сведений о конкретном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="8add1-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>

<span data-ttu-id="8add1-108">Пространства имен — это логические контейнеры, помогающие упорядочивать концентраторы уведомлений и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="8add1-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="8add1-109">Необходимо иметь по крайней мере одно пространство имен концентратора уведомлений: все концентраторы уведомлений должны быть назначены пространству имен.</span><span class="sxs-lookup"><span data-stu-id="8add1-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="8add1-110">Одно пространство имен может быть размещено на нескольких концентраторах, что означает, что вам потребуется только одно пространство имен в Организации.</span><span class="sxs-lookup"><span data-stu-id="8add1-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="8add1-111">Однако вы также можете использовать несколько пространств имен для более эффективной организации концентраторов или предоставить конкретным пользователям разрешение на управление выбранной подмножеством концентраторов.</span><span class="sxs-lookup"><span data-stu-id="8add1-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>

<span data-ttu-id="8add1-112">Командлет **Get-AzureRmNotificationHubsNamespace** возвращает основные сведения о пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="8add1-112">The **Get-AzureRmNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="8add1-113">Чтобы получить сведения о правилах авторизации, связанных с пространством имен, используйте Get-AzureRmNotificationHubsNamespaceAuthorizationRules.</span><span class="sxs-lookup"><span data-stu-id="8add1-113">To get information about the authorization rules associated with a namespace use Get-AzureRmNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="8add1-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8add1-114">EXAMPLES</span></span>

### <span data-ttu-id="8add1-115">Пример 1: получение сведений для всех пространств имен концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="8add1-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace
```

<span data-ttu-id="8add1-116">Эта команда возвращает сведения обо всех пространствах имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8add1-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="8add1-117">Пример 2: получение сведений для одного пространства имен концентратора уведомлений</span><span class="sxs-lookup"><span data-stu-id="8add1-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="8add1-118">Эта команда получает сведения для одного пространства имен концентратора уведомлений: ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="8add1-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="8add1-119">Пример 3: получение сведений для всех концентраторов уведомлений, назначенных определенному пространству имен</span><span class="sxs-lookup"><span data-stu-id="8add1-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="8add1-120">Эта команда получает сведения обо всех пространствах имен концентратора уведомлений, назначенных группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="8add1-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="8add1-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8add1-121">PARAMETERS</span></span>

### <span data-ttu-id="8add1-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8add1-122">-Namespace</span></span>
<span data-ttu-id="8add1-123">Задает уникальное имя для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="8add1-123">Specifies a unique name for the namespace.</span></span>

<span data-ttu-id="8add1-124">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8add1-124">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="8add1-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8add1-125">-ResourceGroup</span></span>
<span data-ttu-id="8add1-126">Указывает группу ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="8add1-126">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="8add1-127">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="8add1-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8add1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8add1-128">-DefaultProfile</span></span>
<span data-ttu-id="8add1-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8add1-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8add1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8add1-130">CommonParameters</span></span>
<span data-ttu-id="8add1-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8add1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8add1-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8add1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8add1-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8add1-133">INPUTS</span></span>

## <span data-ttu-id="8add1-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8add1-134">OUTPUTS</span></span>

### <span data-ttu-id="8add1-135">System. Collections. Generic. List ' 1 [Microsoft. Azure. NamespaceAttributes]</span><span class="sxs-lookup"><span data-stu-id="8add1-135">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes]</span></span>

## <span data-ttu-id="8add1-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="8add1-136">NOTES</span></span>

## <span data-ttu-id="8add1-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8add1-137">RELATED LINKS</span></span>

[<span data-ttu-id="8add1-138">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="8add1-138">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="8add1-139">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="8add1-139">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="8add1-140">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="8add1-140">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="8add1-141">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="8add1-141">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)

