---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSlot.md
ms.openlocfilehash: 6c7fbd4512bfac7a369f21f85803653c6f7c9628
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568100"
---
# <span data-ttu-id="a7edc-101">New-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a7edc-101">New-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="a7edc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7edc-102">SYNOPSIS</span></span>
<span data-ttu-id="a7edc-103">Создание слота веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="a7edc-103">Creates an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7edc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7edc-104">SYNTAX</span></span>

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <PSSite>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>]
 [-ContainerImageName <String>] [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>]
 [-ContainerRegistryPassword <SecureString>] [-EnableContainerContinuousDeployment] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7edc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7edc-105">DESCRIPTION</span></span>
<span data-ttu-id="a7edc-106">Командлет **New-AzureRmWebAppSlot** создает слот веб-приложения Azure в заданной группе ресурсов, использующей указанный план служб приложений и центр обработки данных.</span><span class="sxs-lookup"><span data-stu-id="a7edc-106">The **New-AzureRmWebAppSlot** cmdlet creates an Azure Web App Slot in a given a resource group that uses the specified App Service plan and data center.</span></span>

## <span data-ttu-id="a7edc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7edc-107">EXAMPLES</span></span>

### <span data-ttu-id="a7edc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a7edc-108">Example 1</span></span>
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

<span data-ttu-id="a7edc-109">Эта команда создает слот с именем Slot001 под существующими именами веб-приложений ContosoSite в существующей группе ресурсов с именем Default-Web-WestUS в центре обработки данных Западная часть США.</span><span class="sxs-lookup"><span data-stu-id="a7edc-109">This command creates a Slot named Slot001 under an existing Web App names ContosoSite in the existing resource group named Default-Web-WestUS in data center West US.</span></span>
<span data-ttu-id="a7edc-110">В команде используется существующий план служб приложений с именем ContosoServicePlan.</span><span class="sxs-lookup"><span data-stu-id="a7edc-110">The command uses an existing App Service plan named ContosoServicePlan.</span></span>

## <span data-ttu-id="a7edc-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7edc-111">PARAMETERS</span></span>

### <span data-ttu-id="a7edc-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a7edc-112">-AppServicePlan</span></span>
<span data-ttu-id="a7edc-113">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="a7edc-113">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7edc-114">-AppSettingsOverrides</span><span class="sxs-lookup"><span data-stu-id="a7edc-114">-AppSettingsOverrides</span></span>
<span data-ttu-id="a7edc-115">Параметры приложения переопределяют хэш-таблицу</span><span class="sxs-lookup"><span data-stu-id="a7edc-115">App Settings Overrides Hashtable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7edc-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="a7edc-116">-AseName</span></span>
<span data-ttu-id="a7edc-117">Имя среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="a7edc-117">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7edc-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7edc-118">-AseResourceGroupName</span></span>
<span data-ttu-id="a7edc-119">Имя группы ресурсов среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="a7edc-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7edc-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7edc-120">-AsJob</span></span>
<span data-ttu-id="a7edc-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a7edc-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7edc-122">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="a7edc-122">-ContainerImageName</span></span>
<span data-ttu-id="a7edc-123">Имя и дополнительный тег в контейнере, например (изображение: тег)</span><span class="sxs-lookup"><span data-stu-id="a7edc-123">Container Image Name and optional tag, for example (image:tag)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7edc-124">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="a7edc-124">-ContainerRegistryPassword</span></span>
<span data-ttu-id="a7edc-125">Пароль закрытого контейнера в реестре</span><span class="sxs-lookup"><span data-stu-id="a7edc-125">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7edc-126">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="a7edc-126">-ContainerRegistryUrl</span></span>
<span data-ttu-id="a7edc-127">URL-адрес сервера реестра закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="a7edc-127">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7edc-128">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="a7edc-128">-ContainerRegistryUser</span></span>
<span data-ttu-id="a7edc-129">Имя пользователя в реестре для закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="a7edc-129">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7edc-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7edc-130">-DefaultProfile</span></span>
<span data-ttu-id="a7edc-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7edc-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7edc-132">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="a7edc-132">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="a7edc-133">Включение и отключение веб-перехватчика непрерывного развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="a7edc-133">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="a7edc-134">-IgnoreCustomHostNames</span><span class="sxs-lookup"><span data-stu-id="a7edc-134">-IgnoreCustomHostNames</span></span>
<span data-ttu-id="a7edc-135">Параметр "пропускать пользовательские HostName"</span><span class="sxs-lookup"><span data-stu-id="a7edc-135">Ignore Custom HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7edc-136">-IgnoreSourceControl</span><span class="sxs-lookup"><span data-stu-id="a7edc-136">-IgnoreSourceControl</span></span>
<span data-ttu-id="a7edc-137">Параметр "не учитывать параметры системы управления версиями"</span><span class="sxs-lookup"><span data-stu-id="a7edc-137">Ignore Source Control Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7edc-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a7edc-138">-Name</span></span>
<span data-ttu-id="a7edc-139">Имя webapp</span><span class="sxs-lookup"><span data-stu-id="a7edc-139">Webapp Name</span></span>

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

### <span data-ttu-id="a7edc-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7edc-140">-ResourceGroupName</span></span>
<span data-ttu-id="a7edc-141">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a7edc-141">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7edc-142">-Slot</span><span class="sxs-lookup"><span data-stu-id="a7edc-142">-Slot</span></span>
<span data-ttu-id="a7edc-143">Название гнезда webapp</span><span class="sxs-lookup"><span data-stu-id="a7edc-143">Webapp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7edc-144">-SourceWebApp</span><span class="sxs-lookup"><span data-stu-id="a7edc-144">-SourceWebApp</span></span>
<span data-ttu-id="a7edc-145">Исходный объект WebApp</span><span class="sxs-lookup"><span data-stu-id="a7edc-145">Source WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7edc-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7edc-146">CommonParameters</span></span>
<span data-ttu-id="a7edc-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7edc-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7edc-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7edc-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7edc-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7edc-149">INPUTS</span></span>

### <span data-ttu-id="a7edc-150">System. String</span><span class="sxs-lookup"><span data-stu-id="a7edc-150">System.String</span></span>

### <span data-ttu-id="a7edc-151">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="a7edc-151">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="a7edc-152">Параметры: SourceWebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a7edc-152">Parameters: SourceWebApp (ByValue)</span></span>

## <span data-ttu-id="a7edc-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7edc-153">OUTPUTS</span></span>

### <span data-ttu-id="a7edc-154">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="a7edc-154">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="a7edc-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7edc-155">NOTES</span></span>

## <span data-ttu-id="a7edc-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7edc-156">RELATED LINKS</span></span>

[<span data-ttu-id="a7edc-157">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a7edc-157">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="a7edc-158">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a7edc-158">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="a7edc-159">Restarting-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a7edc-159">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="a7edc-160">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a7edc-160">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="a7edc-161">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a7edc-161">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="a7edc-162">Остановить-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a7edc-162">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="a7edc-163">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a7edc-163">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="a7edc-164">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a7edc-164">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)