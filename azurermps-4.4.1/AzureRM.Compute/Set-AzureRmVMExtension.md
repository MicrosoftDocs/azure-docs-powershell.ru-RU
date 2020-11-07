---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
ms.openlocfilehash: da46aa0e6518c9a9eb9ebea58962f3da593ad264
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565259"
---
# <span data-ttu-id="2b672-101">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="2b672-101">Set-AzureRmVMExtension</span></span>

## <span data-ttu-id="2b672-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2b672-102">SYNOPSIS</span></span>
<span data-ttu-id="2b672-103">Обновляет свойства расширения или добавляет расширение к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="2b672-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b672-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2b672-104">SYNTAX</span></span>

### <span data-ttu-id="2b672-105">Параметры (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2b672-105">Settings (Default)</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b672-106">SettingString</span><span class="sxs-lookup"><span data-stu-id="2b672-106">SettingString</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b672-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b672-107">DESCRIPTION</span></span>
<span data-ttu-id="2b672-108">Командлет **Set-AzureRmVMExtension** обновляет свойства для существующих расширений виртуальных машин или добавляет расширение к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="2b672-108">The **Set-AzureRmVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="2b672-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2b672-109">EXAMPLES</span></span>

### <span data-ttu-id="2b672-110">Пример 1: изменение параметров с помощью хэш-таблиц</span><span class="sxs-lookup"><span data-stu-id="2b672-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="2b672-111">Первые две команды используют стандартный синтаксис Windows PowerShell для создания хэш-таблиц, а затем хранят эти хэш-таблицы в переменных $Settings и $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="2b672-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="2b672-112">Для получения дополнительных сведений введите `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="2b672-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="2b672-113">Вторая команда содержит два значения, ранее созданные и хранимые в переменных.</span><span class="sxs-lookup"><span data-stu-id="2b672-113">The second command includes two values previously created and stored in variables.</span></span>

<span data-ttu-id="2b672-114">Последняя команда изменяет расширение виртуальной машины с именем VirtualMachine22 в ResourceGroup11 в соответствии с содержимым $Settings и $ProtectedSettings.</span><span class="sxs-lookup"><span data-stu-id="2b672-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="2b672-115">Команда задает другие необходимые сведения, включающие издателя и тип расширения.</span><span class="sxs-lookup"><span data-stu-id="2b672-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="2b672-116">Пример 2: изменение параметров с помощью строк</span><span class="sxs-lookup"><span data-stu-id="2b672-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="2b672-117">Первые две команды создают строки, содержащие параметры, а затем сохраняют их в переменных $SettingsString и $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="2b672-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>

<span data-ttu-id="2b672-118">Последняя команда изменяет расширение виртуальной машины с именем VirtualMachine22 в ResourceGroup11 в соответствии с содержимым $SettingsString и $ProtectedSettingsString.</span><span class="sxs-lookup"><span data-stu-id="2b672-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="2b672-119">Команда задает другие необходимые сведения, включающие издателя и тип расширения.</span><span class="sxs-lookup"><span data-stu-id="2b672-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="2b672-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2b672-120">PARAMETERS</span></span>

### <span data-ttu-id="2b672-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b672-121">-DefaultProfile</span></span>
<span data-ttu-id="2b672-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b672-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b672-123">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2b672-123">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="2b672-124">Указывает, что этот командлет запрещает гостевой агенту Azure автоматически обновлять расширения до более поздней дополнительной версии.</span><span class="sxs-lookup"><span data-stu-id="2b672-124">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="2b672-125">По умолчанию этот командлет позволяет гостевому агенту обновлять расширения.</span><span class="sxs-lookup"><span data-stu-id="2b672-125">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b672-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="2b672-126">-ExtensionType</span></span>
<span data-ttu-id="2b672-127">Указывает тип расширения.</span><span class="sxs-lookup"><span data-stu-id="2b672-127">Specifies the extension type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Type

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b672-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="2b672-128">-ForceRerun</span></span>
<span data-ttu-id="2b672-129">Указывает на то, что этот командлет принудительно выполняет повторное выполнение той же конфигурации на виртуальной машине без удаления и повторной установки расширения.</span><span class="sxs-lookup"><span data-stu-id="2b672-129">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="2b672-130">Значением может быть любая строка, отличающаяся от текущего значения.</span><span class="sxs-lookup"><span data-stu-id="2b672-130">The value can be any string different from the current value.</span></span>

<span data-ttu-id="2b672-131">Если forceUpdateTag не меняется, обновления открытых и защищенных параметров по-прежнему применяются обработчиком.</span><span class="sxs-lookup"><span data-stu-id="2b672-131">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="2b672-132">-Location</span><span class="sxs-lookup"><span data-stu-id="2b672-132">-Location</span></span>
<span data-ttu-id="2b672-133">Указывает расположение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2b672-133">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="2b672-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2b672-134">-Name</span></span>
<span data-ttu-id="2b672-135">Указывает имя расширения.</span><span class="sxs-lookup"><span data-stu-id="2b672-135">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b672-136">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="2b672-136">-ProtectedSettings</span></span>
<span data-ttu-id="2b672-137">Задает частную конфигурацию для расширения в качестве хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="2b672-137">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="2b672-138">Этот командлет шифрует закрытую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="2b672-138">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Settings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b672-139">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="2b672-139">-ProtectedSettingString</span></span>
<span data-ttu-id="2b672-140">Задает частную конфигурацию для расширения в виде строки.</span><span class="sxs-lookup"><span data-stu-id="2b672-140">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="2b672-141">Этот командлет шифрует закрытую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="2b672-141">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SettingString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b672-142">-Publisher</span><span class="sxs-lookup"><span data-stu-id="2b672-142">-Publisher</span></span>
<span data-ttu-id="2b672-143">Указывает имя издателя расширений.</span><span class="sxs-lookup"><span data-stu-id="2b672-143">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="2b672-144">Издатель предоставляет имя, когда Publisher регистрирует расширение.</span><span class="sxs-lookup"><span data-stu-id="2b672-144">The publisher provides a name when the publisher registers an extension.</span></span>

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

### <span data-ttu-id="2b672-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b672-145">-ResourceGroupName</span></span>
<span data-ttu-id="2b672-146">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2b672-146">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2b672-147">-Параметры</span><span class="sxs-lookup"><span data-stu-id="2b672-147">-Settings</span></span>
<span data-ttu-id="2b672-148">Задает общедоступную конфигурацию для расширения в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="2b672-148">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="2b672-149">Этот командлет не шифрует общедоступную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="2b672-149">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Settings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b672-150">-SettingString</span><span class="sxs-lookup"><span data-stu-id="2b672-150">-SettingString</span></span>
<span data-ttu-id="2b672-151">Указывает открытую конфигурацию для расширения в виде строки.</span><span class="sxs-lookup"><span data-stu-id="2b672-151">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="2b672-152">Этот командлет не шифрует общедоступную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="2b672-152">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SettingString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b672-153">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2b672-153">-TypeHandlerVersion</span></span>
<span data-ttu-id="2b672-154">Указывает версию расширения, используемую для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2b672-154">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b672-155">-VMName</span><span class="sxs-lookup"><span data-stu-id="2b672-155">-VMName</span></span>
<span data-ttu-id="2b672-156">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2b672-156">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="2b672-157">Этот командлет изменяет расширения для виртуальной машины, указанную в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="2b672-157">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b672-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b672-158">-Confirm</span></span>
<span data-ttu-id="2b672-159">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2b672-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b672-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b672-160">-WhatIf</span></span>
<span data-ttu-id="2b672-161">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2b672-161">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="2b672-162">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2b672-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b672-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b672-163">CommonParameters</span></span>
<span data-ttu-id="2b672-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2b672-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b672-165">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b672-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b672-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2b672-166">INPUTS</span></span>

## <span data-ttu-id="2b672-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b672-167">OUTPUTS</span></span>

## <span data-ttu-id="2b672-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="2b672-168">NOTES</span></span>

## <span data-ttu-id="2b672-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b672-169">RELATED LINKS</span></span>

[<span data-ttu-id="2b672-170">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="2b672-170">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="2b672-171">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="2b672-171">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)

