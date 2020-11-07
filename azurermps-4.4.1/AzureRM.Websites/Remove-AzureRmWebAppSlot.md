---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: 65393bc3dd2e9e6b51699a21baf0e6d3750464bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569123"
---
# <span data-ttu-id="44307-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44307-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="44307-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44307-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44307-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44307-103">SYNTAX</span></span>

### <span data-ttu-id="44307-104">Состояний</span><span class="sxs-lookup"><span data-stu-id="44307-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44307-105">S2</span><span class="sxs-lookup"><span data-stu-id="44307-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44307-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44307-106">DESCRIPTION</span></span>
<span data-ttu-id="44307-107">Командлет **Remove-AzureRmWebAppSlot** удаляет слот веб-приложения Azure, который предоставил группу ресурсов и имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="44307-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="44307-108">Этот командлет по умолчанию также удаляет все слоты и метрики.</span><span class="sxs-lookup"><span data-stu-id="44307-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="44307-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44307-109">EXAMPLES</span></span>

### <span data-ttu-id="44307-110">Пример 1: удаление слота веб-приложения</span><span class="sxs-lookup"><span data-stu-id="44307-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="44307-111">Эта команда удаляет гнездо с именем Slot001, связанное с ContosoSite веб-приложения, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="44307-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="44307-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44307-112">PARAMETERS</span></span>

### <span data-ttu-id="44307-113">-Force</span><span class="sxs-lookup"><span data-stu-id="44307-113">-Force</span></span>
<span data-ttu-id="44307-114">Параметр принудительного удаления</span><span class="sxs-lookup"><span data-stu-id="44307-114">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="44307-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="44307-115">-Name</span></span>
<span data-ttu-id="44307-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="44307-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44307-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44307-117">-ResourceGroupName</span></span>
<span data-ttu-id="44307-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="44307-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44307-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="44307-119">-Slot</span></span>
<span data-ttu-id="44307-120">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="44307-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44307-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="44307-121">-WebApp</span></span>
<span data-ttu-id="44307-122">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="44307-122">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44307-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44307-123">-Confirm</span></span>
<span data-ttu-id="44307-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="44307-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44307-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44307-125">-WhatIf</span></span>
<span data-ttu-id="44307-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="44307-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44307-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="44307-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44307-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44307-128">-DefaultProfile</span></span>
<span data-ttu-id="44307-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44307-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44307-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44307-130">CommonParameters</span></span>
<span data-ttu-id="44307-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44307-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44307-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44307-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44307-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44307-133">INPUTS</span></span>

### <span data-ttu-id="44307-134">Семейств</span><span class="sxs-lookup"><span data-stu-id="44307-134">Site</span></span>
<span data-ttu-id="44307-135">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="44307-135">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="44307-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44307-136">OUTPUTS</span></span>

### <span data-ttu-id="44307-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="44307-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="44307-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="44307-138">NOTES</span></span>

## <span data-ttu-id="44307-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44307-139">RELATED LINKS</span></span>

[<span data-ttu-id="44307-140">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44307-140">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="44307-141">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44307-141">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="44307-142">Restarting-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44307-142">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="44307-143">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44307-143">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="44307-144">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44307-144">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="44307-145">Остановить-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="44307-145">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="44307-146">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="44307-146">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)