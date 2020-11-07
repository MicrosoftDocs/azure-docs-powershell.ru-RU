---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRmAutomationDscNode.md
ms.openlocfilehash: 1a0fd95df118e734ed594cf1efe35eb8f8476f50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566327"
---
# <span data-ttu-id="3a80c-101">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3a80c-101">Register-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="3a80c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3a80c-102">SYNOPSIS</span></span>
<span data-ttu-id="3a80c-103">Регистрирует виртуальную машину Azure как узел DSC для учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="3a80c-103">Registers an Azure virtual machine as a DSC node for an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a80c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3a80c-104">SYNTAX</span></span>

```
Register-AzureRmAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a80c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a80c-105">DESCRIPTION</span></span>
<span data-ttu-id="3a80c-106">Командлет **Register-AzureRmAutomationDscNode** регистрирует виртуальную машину Azure как узел конфигурации нужного состояния ТД в учетной записи службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="3a80c-106">The **Register-AzureRmAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span>

## <span data-ttu-id="3a80c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3a80c-107">EXAMPLES</span></span>

### <span data-ttu-id="3a80c-108">Пример 1: регистрация виртуальной машины Azure в качестве узла Azure DSC</span><span class="sxs-lookup"><span data-stu-id="3a80c-108">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzureRmAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="3a80c-109">Эта команда регистрирует виртуальную машину Azure с именем VirtualMachine01 в качестве узла DSC в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3a80c-109">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="3a80c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3a80c-110">PARAMETERS</span></span>

### <span data-ttu-id="3a80c-111">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="3a80c-111">-ActionAfterReboot</span></span>
<span data-ttu-id="3a80c-112">Указывает действие, выполняемое виртуальной машиной после перезапуска.</span><span class="sxs-lookup"><span data-stu-id="3a80c-112">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="3a80c-113">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="3a80c-113">Valid values are:</span></span> 

- <span data-ttu-id="3a80c-114">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a80c-114">ContinueConfiguration</span></span> 
- <span data-ttu-id="3a80c-115">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a80c-115">StopConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: ContinueConfiguration, StopConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a80c-116">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="3a80c-116">-AllowModuleOverwrite</span></span>
<span data-ttu-id="3a80c-117">Указывает, будут ли новые конфигурации, загружаемые этим узлом DSC, с опрашивающего сервера Azure Automation DSC заменять существующие модули, уже имеющиеся на целевом узле.</span><span class="sxs-lookup"><span data-stu-id="3a80c-117">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a80c-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3a80c-118">-AutomationAccountName</span></span>
<span data-ttu-id="3a80c-119">Указывает имя учетной записи автоматизации, в которой этот командлет регистрирует виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="3a80c-119">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="3a80c-120">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="3a80c-120">-AzureVMLocation</span></span>
<span data-ttu-id="3a80c-121">Указывает расположение, в котором этот командлет регистрирует виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="3a80c-121">Specifies the location in which this cmdlet registers a virtual machine.</span></span>
<span data-ttu-id="3a80c-122">Для получения допустимых местоположений используйте командлет Get-AzureRMLocation.</span><span class="sxs-lookup"><span data-stu-id="3a80c-122">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

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

### <span data-ttu-id="3a80c-123">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="3a80c-123">-AzureVMName</span></span>
<span data-ttu-id="3a80c-124">Указывает имя виртуальной машины Azure, которая регистрируется этим командлетом для управления.</span><span class="sxs-lookup"><span data-stu-id="3a80c-124">Specifies the name of the Azure virtual machine that this cmdlet registers for management.</span></span>

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

### <span data-ttu-id="3a80c-125">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3a80c-125">-AzureVMResourceGroup</span></span>
<span data-ttu-id="3a80c-126">Указывает имя группы ресурсов виртуальной машины Azure, которая регистрируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="3a80c-126">Specifies the name of the resource group of the Azure virtual machine that this cmdlet registers.</span></span>

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

### <span data-ttu-id="3a80c-127">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="3a80c-127">-ConfigurationMode</span></span>
<span data-ttu-id="3a80c-128">Задает режим конфигурации DSC.</span><span class="sxs-lookup"><span data-stu-id="3a80c-128">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="3a80c-129">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="3a80c-129">Valid values are:</span></span> 

- <span data-ttu-id="3a80c-130">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="3a80c-130">ApplyAndMonitor</span></span> 
- <span data-ttu-id="3a80c-131">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="3a80c-131">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="3a80c-132">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="3a80c-132">ApplyOnly</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: ApplyAndMonitor, ApplyAndAutocorrect, ApplyOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a80c-133">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="3a80c-133">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="3a80c-134">Указывает частоту (в минутах), с которой фоновое приложение DSC пытается реализовать текущую конфигурацию на целевом узле.</span><span class="sxs-lookup"><span data-stu-id="3a80c-134">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a80c-135">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3a80c-135">-NodeConfigurationName</span></span>
<span data-ttu-id="3a80c-136">Указывает имя конфигурации узла, которую этот командлет настраивает для виртуальной машины, чтобы извлечь ее из Azure Automation DSC.</span><span class="sxs-lookup"><span data-stu-id="3a80c-136">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="3a80c-137">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="3a80c-137">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="3a80c-138">Указывает, следует ли перезапускать виртуальную машину при необходимости.</span><span class="sxs-lookup"><span data-stu-id="3a80c-138">Specifies whether to restart the virtual machine, if needed.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a80c-139">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="3a80c-139">-RefreshFrequencyMins</span></span>
<span data-ttu-id="3a80c-140">Указывает частоту (в минутах), с которой локальный диспетчер конфигураций связывается с сервером Azure Automation DSC, чтобы скачать последнюю конфигурацию узла.</span><span class="sxs-lookup"><span data-stu-id="3a80c-140">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a80c-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a80c-141">-ResourceGroupName</span></span>
<span data-ttu-id="3a80c-142">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3a80c-142">Specifies the name of a resource group.</span></span>
<span data-ttu-id="3a80c-143">Учетная запись автоматизации, с помощью которой этот командлет регистрирует виртуальную машину, принадлежит к группе ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="3a80c-143">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3a80c-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a80c-144">-DefaultProfile</span></span>
<span data-ttu-id="3a80c-145">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3a80c-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a80c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a80c-146">CommonParameters</span></span>
<span data-ttu-id="3a80c-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3a80c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a80c-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a80c-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a80c-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3a80c-149">INPUTS</span></span>

## <span data-ttu-id="3a80c-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a80c-150">OUTPUTS</span></span>

## <span data-ttu-id="3a80c-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="3a80c-151">NOTES</span></span>

## <span data-ttu-id="3a80c-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a80c-152">RELATED LINKS</span></span>

[<span data-ttu-id="3a80c-153">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3a80c-153">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="3a80c-154">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3a80c-154">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)

[<span data-ttu-id="3a80c-155">Отмена регистрации — AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3a80c-155">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)

