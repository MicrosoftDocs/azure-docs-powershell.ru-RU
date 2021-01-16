---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 6fe89822af5be532674e22dd3e1c1edd583fced4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392383"
---
# <span data-ttu-id="da0bc-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="da0bc-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="da0bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da0bc-102">SYNOPSIS</span></span>
<span data-ttu-id="da0bc-103">Создает объект конфигурации для автоматического исправления на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="da0bc-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="da0bc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="da0bc-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## <span data-ttu-id="da0bc-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da0bc-105">DESCRIPTION</span></span>
<span data-ttu-id="da0bc-106">Для автоматического исправления на виртуальной машине создается объект конфигурации **new-AzVMSqlServerAutoPatchingConfig.**</span><span class="sxs-lookup"><span data-stu-id="da0bc-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="da0bc-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="da0bc-107">EXAMPLES</span></span>

### <span data-ttu-id="da0bc-108">Пример 1. Создание объекта конфигурации для настройки автоматического исправления</span><span class="sxs-lookup"><span data-stu-id="da0bc-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="da0bc-109">Эта команда создает объект конфигурации для исправления.</span><span class="sxs-lookup"><span data-stu-id="da0bc-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="da0bc-110">Команда определяет день недели и окно обслуживания.</span><span class="sxs-lookup"><span data-stu-id="da0bc-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="da0bc-111">Эта конфигурация позволяет исправления, использующие эти значения.</span><span class="sxs-lookup"><span data-stu-id="da0bc-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="da0bc-112">Команда сохраняет результат в переменной $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="da0bc-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="da0bc-113">Вы можете указать этот элемент конфигурации для других Set-AzVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="da0bc-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="da0bc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da0bc-114">PARAMETERS</span></span>

### <span data-ttu-id="da0bc-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="da0bc-115">-DayOfWeek</span></span>
<span data-ttu-id="da0bc-116">Определяет день недели, когда должны быть установлены обновления.</span><span class="sxs-lookup"><span data-stu-id="da0bc-116">Specifies the day of the week when updates should be installed.</span></span>
<span data-ttu-id="da0bc-117">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="da0bc-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="da0bc-118">Воскресенье</span><span class="sxs-lookup"><span data-stu-id="da0bc-118">Sunday</span></span>
- <span data-ttu-id="da0bc-119">Понедельник</span><span class="sxs-lookup"><span data-stu-id="da0bc-119">Monday</span></span>
- <span data-ttu-id="da0bc-120">Вторник</span><span class="sxs-lookup"><span data-stu-id="da0bc-120">Tuesday</span></span>
- <span data-ttu-id="da0bc-121">Среда</span><span class="sxs-lookup"><span data-stu-id="da0bc-121">Wednesday</span></span>
- <span data-ttu-id="da0bc-122">Четверг</span><span class="sxs-lookup"><span data-stu-id="da0bc-122">Thursday</span></span>
- <span data-ttu-id="da0bc-123">Пятница</span><span class="sxs-lookup"><span data-stu-id="da0bc-123">Friday</span></span>
- <span data-ttu-id="da0bc-124">Суббота</span><span class="sxs-lookup"><span data-stu-id="da0bc-124">Saturday</span></span>
- <span data-ttu-id="da0bc-125">Каждый день</span><span class="sxs-lookup"><span data-stu-id="da0bc-125">Everyday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da0bc-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="da0bc-126">-Enable</span></span>
<span data-ttu-id="da0bc-127">Означает, что включено автоматическое исправление для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="da0bc-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="da0bc-128">Если включить автоматическое исправление, с помощью cmdlet вы сможете переналить Windows Update в интерактивный режим.</span><span class="sxs-lookup"><span data-stu-id="da0bc-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="da0bc-129">Если отключить автоматическое исправление, параметры Обновления Windows не изменятся.</span><span class="sxs-lookup"><span data-stu-id="da0bc-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="da0bc-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="da0bc-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="da0bc-131">Длительность (в минутах) окна обслуживания.</span><span class="sxs-lookup"><span data-stu-id="da0bc-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="da0bc-132">Автоматическое исправление не позволяет выполнять действия, которые могут повлиять на доступность виртуальной машины за пределами этого окна.</span><span class="sxs-lookup"><span data-stu-id="da0bc-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="da0bc-133">Укажите кратное 30 минут.</span><span class="sxs-lookup"><span data-stu-id="da0bc-133">Specify a multiple of 30 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da0bc-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="da0bc-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="da0bc-135">Определяет час, в который день начинается окно обслуживания.</span><span class="sxs-lookup"><span data-stu-id="da0bc-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="da0bc-136">На этот раз определяется время начала установки обновлений.</span><span class="sxs-lookup"><span data-stu-id="da0bc-136">This time defines when updates start to install.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da0bc-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="da0bc-137">-PatchCategory</span></span>
<span data-ttu-id="da0bc-138">Указывает, следует ли включать важные обновления.</span><span class="sxs-lookup"><span data-stu-id="da0bc-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da0bc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da0bc-139">CommonParameters</span></span>
<span data-ttu-id="da0bc-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da0bc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da0bc-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da0bc-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da0bc-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da0bc-142">INPUTS</span></span>

### <span data-ttu-id="da0bc-143">Нет</span><span class="sxs-lookup"><span data-stu-id="da0bc-143">None</span></span>

## <span data-ttu-id="da0bc-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="da0bc-144">OUTPUTS</span></span>

### <span data-ttu-id="da0bc-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="da0bc-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

## <span data-ttu-id="da0bc-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="da0bc-146">NOTES</span></span>

## <span data-ttu-id="da0bc-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da0bc-147">RELATED LINKS</span></span>

[<span data-ttu-id="da0bc-148">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="da0bc-148">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="da0bc-149">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="da0bc-149">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)

