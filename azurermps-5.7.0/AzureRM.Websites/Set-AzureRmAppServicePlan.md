---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 16b2c8df737047619366ebf6b75a4c2ed2264fdc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567345"
---
# <span data-ttu-id="c4625-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c4625-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="c4625-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c4625-102">SYNOPSIS</span></span>
<span data-ttu-id="c4625-103">Задает план служб приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="c4625-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4625-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c4625-104">SYNTAX</span></span>

### <span data-ttu-id="c4625-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="c4625-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4625-106">S2</span><span class="sxs-lookup"><span data-stu-id="c4625-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
[-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4625-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4625-107">DESCRIPTION</span></span>
<span data-ttu-id="c4625-108">Командлет **Set-AzureRmAppServicePlan** задает план служб приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="c4625-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="c4625-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c4625-109">EXAMPLES</span></span>

### <span data-ttu-id="c4625-110">1: изменение плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="c4625-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="c4625-111">Эта команда устанавливает для параметра PerSiteScaling значение true для плана служб приложений с именем ContosoASP, который принадлежит группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="c4625-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="c4625-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c4625-112">PARAMETERS</span></span>

### <span data-ttu-id="c4625-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="c4625-113">-AdminSiteName</span></span>
<span data-ttu-id="c4625-114">Имя сайта администратора</span><span class="sxs-lookup"><span data-stu-id="c4625-114">Admin Site Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4625-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c4625-115">-AppServicePlan</span></span>
<span data-ttu-id="c4625-116">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="c4625-116">App Service Plan Object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4625-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4625-117">-DefaultProfile</span></span>
<span data-ttu-id="c4625-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4625-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4625-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c4625-119">-Name</span></span>
<span data-ttu-id="c4625-120">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="c4625-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4625-121">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="c4625-121">-NumberofWorkers</span></span>
<span data-ttu-id="c4625-122">Количество сотрудников</span><span class="sxs-lookup"><span data-stu-id="c4625-122">Number Of Workers</span></span>

```yaml
Type: Int32
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4625-123">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="c4625-123">-PerSiteScaling</span></span>
<span data-ttu-id="c4625-124">Логическое масштабирование на уровне сайта</span><span class="sxs-lookup"><span data-stu-id="c4625-124">Per Site Scaling Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4625-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4625-125">-ResourceGroupName</span></span>
<span data-ttu-id="c4625-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c4625-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4625-127">Уровень</span><span class="sxs-lookup"><span data-stu-id="c4625-127">-Tier</span></span>
<span data-ttu-id="c4625-128">Уровневый</span><span class="sxs-lookup"><span data-stu-id="c4625-128">Tier</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium, PremiumV2

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4625-129">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="c4625-129">-WorkerSize</span></span>
<span data-ttu-id="c4625-130">Размер рабочего процесса</span><span class="sxs-lookup"><span data-stu-id="c4625-130">Worker Size</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="c4625-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4625-131">-AsJob</span></span>
<span data-ttu-id="c4625-132">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c4625-132">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4625-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4625-133">CommonParameters</span></span>
<span data-ttu-id="c4625-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c4625-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4625-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4625-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4625-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c4625-136">INPUTS</span></span>

### <span data-ttu-id="c4625-137">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="c4625-137">ServerFarmWithRichSku</span></span>
<span data-ttu-id="c4625-138">Параметр "AppServicePlan" принимает значение типа "ServerFarmWithRichSku" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c4625-138">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="c4625-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4625-139">OUTPUTS</span></span>

### <span data-ttu-id="c4625-140">Microsoft. Azure. Management. website. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="c4625-140">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="c4625-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="c4625-141">NOTES</span></span>

## <span data-ttu-id="c4625-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4625-142">RELATED LINKS</span></span>

[<span data-ttu-id="c4625-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c4625-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="c4625-144">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c4625-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="c4625-145">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c4625-145">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="c4625-146">Restarting-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c4625-146">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="c4625-147">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c4625-147">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="c4625-148">Остановить-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c4625-148">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)

