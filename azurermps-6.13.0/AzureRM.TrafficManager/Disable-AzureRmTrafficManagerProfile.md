---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/disable-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: e714caedb86bd647ccc0692c47233833bc2db867
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558183"
---
# <span data-ttu-id="cf272-101">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cf272-101">Disable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="cf272-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf272-102">SYNOPSIS</span></span>
<span data-ttu-id="cf272-103">Отключение профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="cf272-103">Disables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf272-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf272-104">SYNTAX</span></span>

### <span data-ttu-id="cf272-105">»</span><span class="sxs-lookup"><span data-stu-id="cf272-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf272-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="cf272-106">Object</span></span>
```
Disable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf272-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf272-107">DESCRIPTION</span></span>
<span data-ttu-id="cf272-108">Командлет **Disable-AzureRmTrafficManagerProfile** отключает профиль диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="cf272-108">The **Disable-AzureRmTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="cf272-109">Вы можете указать объект профиля с помощью конвейера или значения параметра.</span><span class="sxs-lookup"><span data-stu-id="cf272-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="cf272-110">Кроме того, вы можете указать профиль с помощью параметров *Name* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="cf272-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="cf272-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf272-111">EXAMPLES</span></span>

### <span data-ttu-id="cf272-112">Пример 1: отключение профиля, указанного именем</span><span class="sxs-lookup"><span data-stu-id="cf272-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="cf272-113">Эта команда отключает профиль с именем ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="cf272-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="cf272-114">В командной строке появится запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="cf272-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="cf272-115">Пример 2: отключение профиля с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="cf272-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="cf272-116">Эта команда получает профиль с именем ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="cf272-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="cf272-117">Затем команда передает этот профиль командлету **Disable-AzureRmTrafficManagerProfile** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="cf272-117">The command then passes that profile to the **Disable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cf272-118">Этот командлет отключает этот профиль.</span><span class="sxs-lookup"><span data-stu-id="cf272-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="cf272-119">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="cf272-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="cf272-120">Поэтому он не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="cf272-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="cf272-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf272-121">PARAMETERS</span></span>

### <span data-ttu-id="cf272-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf272-122">-DefaultProfile</span></span>
<span data-ttu-id="cf272-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf272-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf272-124">-Force</span><span class="sxs-lookup"><span data-stu-id="cf272-124">-Force</span></span>
<span data-ttu-id="cf272-125">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="cf272-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cf272-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cf272-126">-Name</span></span>
<span data-ttu-id="cf272-127">Указывает имя профиля диспетчера трафика, который отключается этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="cf272-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf272-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf272-128">-ResourceGroupName</span></span>
<span data-ttu-id="cf272-129">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cf272-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="cf272-130">Этот командлет отключает профиль диспетчера трафика в группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="cf272-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf272-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cf272-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="cf272-132">Указывает объект **TrafficManagerProfile** , который нужно отключить.</span><span class="sxs-lookup"><span data-stu-id="cf272-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="cf272-133">Чтобы получить объект **TrafficManagerProfile** , используйте командлет Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="cf272-133">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf272-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf272-134">-Confirm</span></span>
<span data-ttu-id="cf272-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cf272-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf272-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf272-136">-WhatIf</span></span>
<span data-ttu-id="cf272-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cf272-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf272-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cf272-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf272-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf272-139">CommonParameters</span></span>
<span data-ttu-id="cf272-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf272-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf272-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf272-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf272-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf272-142">INPUTS</span></span>

### <span data-ttu-id="cf272-143">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cf272-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="cf272-144">Этот командлет принимает объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="cf272-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="cf272-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf272-145">OUTPUTS</span></span>

### <span data-ttu-id="cf272-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf272-146">System.Boolean</span></span>

## <span data-ttu-id="cf272-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf272-147">NOTES</span></span>

## <span data-ttu-id="cf272-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf272-148">RELATED LINKS</span></span>

[<span data-ttu-id="cf272-149">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cf272-149">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="cf272-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cf272-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="cf272-151">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cf272-151">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="cf272-152">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cf272-152">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="cf272-153">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cf272-153">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)

