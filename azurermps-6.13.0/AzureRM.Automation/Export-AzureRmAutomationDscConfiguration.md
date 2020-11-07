---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: f690e5d7e35b819b727e2ea3f12c8f5e0b2a375f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556907"
---
# <span data-ttu-id="de8b9-101">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="de8b9-101">Export-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="de8b9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="de8b9-102">SYNOPSIS</span></span>
<span data-ttu-id="de8b9-103">Экспорт конфигурации DSC из автоматизации в локальный файл.</span><span class="sxs-lookup"><span data-stu-id="de8b9-103">Exports a DSC configuration from Automation to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de8b9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="de8b9-104">SYNTAX</span></span>

```
Export-AzureRmAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de8b9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de8b9-105">DESCRIPTION</span></span>
<span data-ttu-id="de8b9-106">Командлет **Export-AzureRmAutomationDscConfiguration** экспортирует конфигурацию нужной конфигурации ТД из Azure Automation в локальный файл.</span><span class="sxs-lookup"><span data-stu-id="de8b9-106">The **Export-AzureRmAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="de8b9-107">Экспортированный файл имеет расширение имени файла. ps1.</span><span class="sxs-lookup"><span data-stu-id="de8b9-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="de8b9-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="de8b9-108">EXAMPLES</span></span>

### <span data-ttu-id="de8b9-109">Пример 1: экспорт опубликованной версии конфигурации DSC</span><span class="sxs-lookup"><span data-stu-id="de8b9-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="de8b9-110">Эта команда экспортирует опубликованную версию конфигурации DSC из автоматизации в указанную папку, которая является рабочим столом.</span><span class="sxs-lookup"><span data-stu-id="de8b9-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="de8b9-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="de8b9-111">PARAMETERS</span></span>

### <span data-ttu-id="de8b9-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="de8b9-112">-AutomationAccountName</span></span>
<span data-ttu-id="de8b9-113">Указывает имя учетной записи автоматизации, содержащей DSC, который экспортируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="de8b9-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="de8b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de8b9-114">-DefaultProfile</span></span>
<span data-ttu-id="de8b9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="de8b9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de8b9-116">-Force</span><span class="sxs-lookup"><span data-stu-id="de8b9-116">-Force</span></span>
<span data-ttu-id="de8b9-117">Указывает на то, что этот командлет заменяет существующий локальный файл новым файлом с таким же именем.</span><span class="sxs-lookup"><span data-stu-id="de8b9-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="de8b9-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="de8b9-118">-Name</span></span>
<span data-ttu-id="de8b9-119">Указывает имя конфигурации DSC, экспортируемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="de8b9-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de8b9-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="de8b9-120">-OutputFolder</span></span>
<span data-ttu-id="de8b9-121">Указывает папку выходных данных, в которой этот командлет экспортирует конфигурацию DSC.</span><span class="sxs-lookup"><span data-stu-id="de8b9-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de8b9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de8b9-122">-ResourceGroupName</span></span>
<span data-ttu-id="de8b9-123">Указывает имя группы ресурсов, для которой этот командлет экспортирует конфигурацию DSC.</span><span class="sxs-lookup"><span data-stu-id="de8b9-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="de8b9-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="de8b9-124">-Slot</span></span>
<span data-ttu-id="de8b9-125">Указывает, какая версия конфигурации DSC экспортируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="de8b9-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="de8b9-126">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="de8b9-126">Valid values are:</span></span> 
- <span data-ttu-id="de8b9-127">Проверяем</span><span class="sxs-lookup"><span data-stu-id="de8b9-127">Draft</span></span>
- <span data-ttu-id="de8b9-128">Опубликовано значение по умолчанию — Опубликовано.</span><span class="sxs-lookup"><span data-stu-id="de8b9-128">Published The default value is Published.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de8b9-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de8b9-129">-Confirm</span></span>
<span data-ttu-id="de8b9-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="de8b9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de8b9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de8b9-131">-WhatIf</span></span>
<span data-ttu-id="de8b9-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="de8b9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de8b9-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="de8b9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de8b9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de8b9-134">CommonParameters</span></span>
<span data-ttu-id="de8b9-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="de8b9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de8b9-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de8b9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de8b9-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="de8b9-137">INPUTS</span></span>

### <span data-ttu-id="de8b9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="de8b9-138">System.String</span></span>

## <span data-ttu-id="de8b9-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="de8b9-139">OUTPUTS</span></span>

### <span data-ttu-id="de8b9-140">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="de8b9-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="de8b9-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="de8b9-141">NOTES</span></span>

## <span data-ttu-id="de8b9-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de8b9-142">RELATED LINKS</span></span>

[<span data-ttu-id="de8b9-143">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="de8b9-143">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="de8b9-144">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="de8b9-144">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)

