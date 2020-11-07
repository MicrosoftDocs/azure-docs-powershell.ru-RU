---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 2fb349628a686bb96df5685bff8a4329c0173212
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564164"
---
# <span data-ttu-id="5a60b-101">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="5a60b-101">Set-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="5a60b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a60b-102">SYNOPSIS</span></span>
<span data-ttu-id="5a60b-103">Задает значения свойств для пространства имен центра уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5a60b-103">Sets property values for a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a60b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a60b-104">SYNTAX</span></span>

```
Set-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a60b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a60b-105">DESCRIPTION</span></span>
<span data-ttu-id="5a60b-106">Командлет **Set-AzureRmNotificationHubsNamespace** задает значения свойств существующего пространства имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5a60b-106">The **Set-AzureRmNotificationHubsNamespace** cmdlet sets the property values of an existing notification hub namespace.</span></span>
<span data-ttu-id="5a60b-107">Пространства имен — это логические контейнеры, помогающие упорядочивать концентраторы уведомлений и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="5a60b-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="5a60b-108">Необходимо иметь по крайней мере одно пространство имен концентратора уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5a60b-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="5a60b-109">Кроме того, все концентраторы уведомлений должны иметь назначенное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="5a60b-109">Additionally, all notification hubs must have an assigned namespace.</span></span>
<span data-ttu-id="5a60b-110">Этот командлет используется преимущественно для включения и отключения пространства имен.</span><span class="sxs-lookup"><span data-stu-id="5a60b-110">This cmdlet is primarily used to enable and disable a namespace.</span></span>
<span data-ttu-id="5a60b-111">Если пространство имен отключено, пользователи не могут подключаться к каким-либо концентраторам уведомлений в пространстве имен, а также не могут использовать эти концентраторы для отправки push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5a60b-111">When a namespace is disabled, users cannot connect to any of the notification hubs in the namespace, nor can administrators use those hubs to send push notifications.</span></span>
<span data-ttu-id="5a60b-112">Чтобы повторно включить отключенное пространство имен, используйте этот командлет, чтобы задать для свойства **State** пространства имен значение "активно".</span><span class="sxs-lookup"><span data-stu-id="5a60b-112">To re-enable a disabled namespace, use this cmdlet to set the **State** property of the namespace to Active.</span></span>
<span data-ttu-id="5a60b-113">Вы также можете использовать этот командлет, чтобы пометить пространство имен как критическое.</span><span class="sxs-lookup"><span data-stu-id="5a60b-113">You can also use this cmdlet to tag a namespace as critical.</span></span>
<span data-ttu-id="5a60b-114">Это предотвратит удаление пространства имен.</span><span class="sxs-lookup"><span data-stu-id="5a60b-114">This prevents the namespace from being deleted.</span></span>
<span data-ttu-id="5a60b-115">Чтобы удалить критическое пространство имен, необходимо сначала удалить критический тег.</span><span class="sxs-lookup"><span data-stu-id="5a60b-115">To remove a critical namespace you must first remove the Critical tag.</span></span>

## <span data-ttu-id="5a60b-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a60b-116">EXAMPLES</span></span>

### <span data-ttu-id="5a60b-117">Пример 1: Отключение пространства имен</span><span class="sxs-lookup"><span data-stu-id="5a60b-117">Example 1: Disable a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

<span data-ttu-id="5a60b-118">Эта команда отключает пространство имен с именем ContosoPartners, находящееся в центре обработки данных "Западная часть США" и назначенное группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="5a60b-118">This command disables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="5a60b-119">Пример 2: включение пространства имен</span><span class="sxs-lookup"><span data-stu-id="5a60b-119">Example 2: Enable a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

<span data-ttu-id="5a60b-120">Эта команда включает пространство имен с именем ContosoPartners, которое находится в центре обработки данных "Западная часть США" и назначено группе ресурсов ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="5a60b-120">This command enables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

## <span data-ttu-id="5a60b-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a60b-121">PARAMETERS</span></span>

### <span data-ttu-id="5a60b-122">-Критический уровень</span><span class="sxs-lookup"><span data-stu-id="5a60b-122">-Critical</span></span>
<span data-ttu-id="5a60b-123">Указывает, является ли пространство имен критическим для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="5a60b-123">Indicates whether the namespace is a critical namespace.</span></span>
<span data-ttu-id="5a60b-124">Не удается удалить критические пространства имен.</span><span class="sxs-lookup"><span data-stu-id="5a60b-124">Critical namespaces cannot be deleted.</span></span>
<span data-ttu-id="5a60b-125">Чтобы удалить критическое пространство имен, необходимо установить для этого свойства значение false, чтобы помечать пространство имен как некритическое.</span><span class="sxs-lookup"><span data-stu-id="5a60b-125">To delete a critical namespace, you must set the value of this property to False in order to mark the namespace as non-critical.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a60b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a60b-126">-DefaultProfile</span></span>
<span data-ttu-id="5a60b-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5a60b-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a60b-128">-Force</span><span class="sxs-lookup"><span data-stu-id="5a60b-128">-Force</span></span>
<span data-ttu-id="5a60b-129">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="5a60b-129">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5a60b-130">-Location</span><span class="sxs-lookup"><span data-stu-id="5a60b-130">-Location</span></span>
<span data-ttu-id="5a60b-131">Указывает отображаемое имя центра обработки данных, на котором размещается пространство имен.</span><span class="sxs-lookup"><span data-stu-id="5a60b-131">Specifies the display name of the datacenter that hosts the namespace.</span></span>
<span data-ttu-id="5a60b-132">Несмотря на то, что вы можете установить для этого параметра любое допустимое расположение Azure, для оптимальной производительности следует использовать центр обработки данных, расположенный рядом с большинством пользователей.</span><span class="sxs-lookup"><span data-stu-id="5a60b-132">Although you can set this parameter to any valid Azure location, for optimal performance you should use a datacenter located near the majority of your users.</span></span>
<span data-ttu-id="5a60b-133">Чтобы получить актуальный список местоположений Azure, выполните следующую команду: `Get-AzureLocation | Select-Object DisplayName`</span><span class="sxs-lookup"><span data-stu-id="5a60b-133">To get an up-to-date list of Azure locations run the following command: `Get-AzureLocation | Select-Object DisplayName`</span></span>

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

### <span data-ttu-id="5a60b-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5a60b-134">-Namespace</span></span>
<span data-ttu-id="5a60b-135">Задает пространство имен, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5a60b-135">Specifies the namespace that this cmdlet modifies.</span></span>
<span data-ttu-id="5a60b-136">Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5a60b-136">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="5a60b-137">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5a60b-137">-ResourceGroup</span></span>
<span data-ttu-id="5a60b-138">Указывает группу ресурсов, которой назначено пространство имен.</span><span class="sxs-lookup"><span data-stu-id="5a60b-138">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="5a60b-139">Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="5a60b-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="5a60b-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="5a60b-140">-SkuTier</span></span>
<span data-ttu-id="5a60b-141">Уровень SKU пространства имен</span><span class="sxs-lookup"><span data-stu-id="5a60b-141">Sku tier of the namespace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a60b-142">-State</span><span class="sxs-lookup"><span data-stu-id="5a60b-142">-State</span></span>
<span data-ttu-id="5a60b-143">Указывает текущее состояние пространства имен.</span><span class="sxs-lookup"><span data-stu-id="5a60b-143">Specifies the current state of the namespace.</span></span>
<span data-ttu-id="5a60b-144">Допустимые значения этого параметра: активны и отключены.</span><span class="sxs-lookup"><span data-stu-id="5a60b-144">The acceptable values for this parameter are: Active and Disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a60b-145">-Тег</span><span class="sxs-lookup"><span data-stu-id="5a60b-145">-Tag</span></span>
<span data-ttu-id="5a60b-146">Указывает пары "имя-значение", которые можно использовать для классификации и упорядочения элементов Azure.</span><span class="sxs-lookup"><span data-stu-id="5a60b-146">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="5a60b-147">Теги похожи на ключевые слова и работают в рамках развертывания.</span><span class="sxs-lookup"><span data-stu-id="5a60b-147">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="5a60b-148">Например, если вы ищете все элементы в отделе тегов: поиск вернет все элементы Azure с таким тегом, независимо от того, как тип элемента, расположение или группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5a60b-148">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="5a60b-149">Отдельный тег состоит из двух частей: *имени* и (необязательно) *значения*.</span><span class="sxs-lookup"><span data-stu-id="5a60b-149">An individual tag consists of two parts: the *Name* and (optionally) the *Value*.</span></span>
<span data-ttu-id="5a60b-150">Например, в отделе: имя тега — "Отдел", а значение тега —.</span><span class="sxs-lookup"><span data-stu-id="5a60b-150">For example, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="5a60b-151">Чтобы добавить тег, используйте синтаксис хэш-таблицы, аналогичный приведенному ниже, который создает тег CalendarYear: 2016:-Tags @ {Name = "CalendarYear"; Value = "2016"} чтобы добавить несколько тегов в одной команде, разделите отдельные Теги с помощью запятых:-Tag @ {Name = "CalendarYear"; Value = "2016"}, @ {Name = "FiscalYear"; Value = "2017"}</span><span class="sxs-lookup"><span data-stu-id="5a60b-151">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016: -Tags @{Name="CalendarYear";Value="2016"} To add multiple tags in the same command, separate the individual tags by using commas: -Tag @{Name="CalendarYear";Value="2016"}, @{Name="FiscalYear";Value="2017"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a60b-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a60b-152">-Confirm</span></span>
<span data-ttu-id="5a60b-153">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5a60b-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a60b-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a60b-154">-WhatIf</span></span>
<span data-ttu-id="5a60b-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5a60b-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a60b-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5a60b-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a60b-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a60b-157">CommonParameters</span></span>
<span data-ttu-id="5a60b-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a60b-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a60b-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a60b-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a60b-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a60b-160">INPUTS</span></span>

### <span data-ttu-id="5a60b-161">System. String</span><span class="sxs-lookup"><span data-stu-id="5a60b-161">System.String</span></span>

### <span data-ttu-id="5a60b-162">Microsoft. Azure. Commands. NotificationHubs. Models. NamespaceState</span><span class="sxs-lookup"><span data-stu-id="5a60b-162">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState</span></span>

### <span data-ttu-id="5a60b-163">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5a60b-163">System.Boolean</span></span>

### <span data-ttu-id="5a60b-164">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5a60b-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5a60b-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a60b-165">OUTPUTS</span></span>

### <span data-ttu-id="5a60b-166">Microsoft. Azure. Commands. NotificationHubs. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="5a60b-166">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="5a60b-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a60b-167">NOTES</span></span>

## <span data-ttu-id="5a60b-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a60b-168">RELATED LINKS</span></span>

[<span data-ttu-id="5a60b-169">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="5a60b-169">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="5a60b-170">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="5a60b-170">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="5a60b-171">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="5a60b-171">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

