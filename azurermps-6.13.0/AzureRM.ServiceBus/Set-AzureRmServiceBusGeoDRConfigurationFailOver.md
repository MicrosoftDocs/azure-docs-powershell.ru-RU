---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 274563165beefdc8a5d7575bd32328f68bf40efa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567689"
---
# <span data-ttu-id="9b584-101">Set-AzureRmServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="9b584-101">Set-AzureRmServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="9b584-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b584-102">SYNOPSIS</span></span>
<span data-ttu-id="9b584-103">Вызывает отработку отказа географического восстановления и повторно конфигурирует псевдоним, чтобы он указывал на дополнительное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="9b584-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b584-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b584-104">SYNTAX</span></span>

### <span data-ttu-id="9b584-105">GeoDRPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9b584-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b584-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9b584-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b584-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b584-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b584-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b584-108">DESCRIPTION</span></span>
<span data-ttu-id="9b584-109">Командлет **Set-AzureRmServiceBusGeoDRConfigurationFailOver** envokes отработки отказа в географическом процессе и повторно настройте его, чтобы он указывал на дополнительное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="9b584-109">The **Set-AzureRmServiceBusGeoDRConfigurationFailOver** cmdlet envokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="9b584-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b584-110">EXAMPLES</span></span>

### <span data-ttu-id="9b584-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9b584-111">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="9b584-112">Вызывает отработку отказа для псевдонима "SampleDRCongifName", перестраивает и указывает на дополнительное пространство имен "SampleNamespace_Secondary".</span><span class="sxs-lookup"><span data-stu-id="9b584-112">Invokes the Failover over alias "SampleDRCongifName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="9b584-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b584-113">PARAMETERS</span></span>

### <span data-ttu-id="9b584-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b584-114">-DefaultProfile</span></span>
<span data-ttu-id="9b584-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b584-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b584-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b584-116">-InputObject</span></span>
<span data-ttu-id="9b584-117">Объект конфигурации служебной шины GeoDR</span><span class="sxs-lookup"><span data-stu-id="9b584-117">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b584-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9b584-118">-Name</span></span>
<span data-ttu-id="9b584-119">Имя конфигурации DR — псевдоним</span><span class="sxs-lookup"><span data-stu-id="9b584-119">DR Configuration Name - Alias</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b584-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9b584-120">-Namespace</span></span>
<span data-ttu-id="9b584-121">Имя пространства имен — дополнительное пространство имен</span><span class="sxs-lookup"><span data-stu-id="9b584-121">Namespace Name - Secondary Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b584-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b584-122">-PassThru</span></span>
<span data-ttu-id="9b584-123">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="9b584-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9b584-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9b584-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9b584-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b584-125">-ResourceGroupName</span></span>
<span data-ttu-id="9b584-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9b584-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b584-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b584-127">-ResourceId</span></span>
<span data-ttu-id="9b584-128">Идентификатор ресурса GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b584-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b584-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b584-129">-Confirm</span></span>
<span data-ttu-id="9b584-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9b584-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b584-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b584-131">-WhatIf</span></span>
<span data-ttu-id="9b584-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9b584-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b584-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9b584-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b584-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b584-134">CommonParameters</span></span>
<span data-ttu-id="9b584-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b584-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b584-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b584-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b584-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b584-137">INPUTS</span></span>

### <span data-ttu-id="9b584-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9b584-138">System.String</span></span>

### <span data-ttu-id="9b584-139">Microsoft. Azure. Commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="9b584-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="9b584-140">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9b584-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="9b584-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b584-141">OUTPUTS</span></span>

### <span data-ttu-id="9b584-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9b584-142">System.Boolean</span></span>

## <span data-ttu-id="9b584-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b584-143">NOTES</span></span>

## <span data-ttu-id="9b584-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b584-144">RELATED LINKS</span></span>