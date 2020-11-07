---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: 49cd2fdb2d482621ea52f1df88c9bcd95521badd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567310"
---
# <span data-ttu-id="cf58f-101">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf58f-101">Import-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="cf58f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf58f-102">SYNOPSIS</span></span>
<span data-ttu-id="cf58f-103">Импортирует MOF-документ как конфигурацию узла DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="cf58f-103">Imports a MOF document as a DSC node configuration in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf58f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf58f-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf58f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf58f-105">DESCRIPTION</span></span>
<span data-ttu-id="cf58f-106">Командлет **Import-AzureRmAutomationDscConfiguration** импортирует документ конфигурации MOF (Managed Object Format) в Azure Automation как конфигурацию узла нужной конфигурации состояния (DSC).</span><span class="sxs-lookup"><span data-stu-id="cf58f-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports a Managed Object Format (MOF) configuration document into Azure Automation as a Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="cf58f-107">Укажите путь к MOF-файлу.</span><span class="sxs-lookup"><span data-stu-id="cf58f-107">Specify the path of a .mof file.</span></span>

## <span data-ttu-id="cf58f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf58f-108">EXAMPLES</span></span>

### <span data-ttu-id="cf58f-109">Пример 1: импорт конфигурации узла DSC в автоматизацию</span><span class="sxs-lookup"><span data-stu-id="cf58f-109">Example 1: Import a DSC node configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

<span data-ttu-id="cf58f-110">Эта команда импортирует конфигурацию узла DSC из файла с именем "веб-сервер. mof" в учетную запись службы автоматизации с именем Contoso17 в разделе Конфигурация DSC ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cf58f-110">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="cf58f-111">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="cf58f-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="cf58f-112">Если у вас уже есть конфигурация узла DSC с именем ContosoConfiguration...... Эта команда заменяет ее.</span><span class="sxs-lookup"><span data-stu-id="cf58f-112">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command replaces it.</span></span>

### <span data-ttu-id="cf58f-113">Пример 2: импорт конфигурации узла DSC в автоматизацию и создание новой версии сборки и не перезапись существующих NodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cf58f-113">Example 2: Import a DSC node configuration into Automation and create a new build version and not overwrite existing NodeConfiguration.</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="cf58f-114">Эта команда импортирует конфигурацию узла DSC из файла с именем "веб-сервер. mof" в учетную запись службы автоматизации с именем Contoso17 в разделе Конфигурация DSC ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cf58f-114">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="cf58f-115">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="cf58f-115">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="cf58f-116">Если у вас уже есть конфигурация узла DSC с именем ContosoConfiguration. веб-сервер, эта команда добавляет новую версию сборки с именем ContosoConfiguration [2]. веб-сервер.</span><span class="sxs-lookup"><span data-stu-id="cf58f-116">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command adds a new build version with the name ContosoConfiguration[2].webserver.</span></span>

## <span data-ttu-id="cf58f-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf58f-117">PARAMETERS</span></span>

### <span data-ttu-id="cf58f-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cf58f-118">-AutomationAccountName</span></span>
<span data-ttu-id="cf58f-119">Указывает имя учетной записи автоматизации, на которую этот командлет импортирует конфигурацию узла DSC.</span><span class="sxs-lookup"><span data-stu-id="cf58f-119">Specifies the name of the Automation account into which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="cf58f-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="cf58f-120">-ConfigurationName</span></span>
<span data-ttu-id="cf58f-121">Задает имя конфигурации DSC в автоматизации для использования в качестве пространства имен и контейнера для конфигурации узла, которую нужно импортировать.</span><span class="sxs-lookup"><span data-stu-id="cf58f-121">Specifies the name of a DSC configuration in Automation to use as the namespace and container for the node configuration to import.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf58f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf58f-122">-DefaultProfile</span></span>
<span data-ttu-id="cf58f-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cf58f-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf58f-124">-Force</span><span class="sxs-lookup"><span data-stu-id="cf58f-124">-Force</span></span>
<span data-ttu-id="cf58f-125">Указывает на то, что этот командлет заменяет существующую конфигурацию узла DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="cf58f-125">Indicates that this cmdlet replaces an existing DSC node configuration in Automation.</span></span>

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

### <span data-ttu-id="cf58f-126">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="cf58f-126">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="cf58f-127">Создает новую версию сборки конфигурации узла.</span><span class="sxs-lookup"><span data-stu-id="cf58f-127">Creates a new Node Configuration build version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf58f-128">-Path</span><span class="sxs-lookup"><span data-stu-id="cf58f-128">-Path</span></span>
<span data-ttu-id="cf58f-129">Указывает путь к документу конфигурации MOF, который этот командлет импортирует.</span><span class="sxs-lookup"><span data-stu-id="cf58f-129">Specifies the path of the MOF configuration document that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf58f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf58f-130">-ResourceGroupName</span></span>
<span data-ttu-id="cf58f-131">Указывает имя группы ресурсов, для которой этот командлет импортирует конфигурацию узла DSC.</span><span class="sxs-lookup"><span data-stu-id="cf58f-131">Specifies the name of a resource group for which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="cf58f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf58f-132">-Confirm</span></span>
<span data-ttu-id="cf58f-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cf58f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf58f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf58f-134">-WhatIf</span></span>
<span data-ttu-id="cf58f-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cf58f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf58f-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cf58f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf58f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf58f-137">CommonParameters</span></span>
<span data-ttu-id="cf58f-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf58f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf58f-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf58f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf58f-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf58f-140">INPUTS</span></span>

### <span data-ttu-id="cf58f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="cf58f-141">System.String</span></span>

## <span data-ttu-id="cf58f-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf58f-142">OUTPUTS</span></span>

### <span data-ttu-id="cf58f-143">Microsoft. Azure. Commands. Automation. Model. NodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf58f-143">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span></span>

## <span data-ttu-id="cf58f-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf58f-144">NOTES</span></span>

## <span data-ttu-id="cf58f-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf58f-145">RELATED LINKS</span></span>

[<span data-ttu-id="cf58f-146">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf58f-146">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="cf58f-147">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf58f-147">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

