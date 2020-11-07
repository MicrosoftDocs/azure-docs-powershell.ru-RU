---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: EF3FE3F1-1C8F-41EB-990E-F2B30BD9D082
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: f222f075ec80162324d7ebcacfb4569371b59741
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568722"
---
# <span data-ttu-id="becb5-101">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="becb5-101">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="becb5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="becb5-102">SYNOPSIS</span></span>
<span data-ttu-id="becb5-103">Останавливает сбор настраиваемых журналов на компьютерах с ОС Linux.</span><span class="sxs-lookup"><span data-stu-id="becb5-103">Stops collection of custom logs from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="becb5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="becb5-104">SYNTAX</span></span>

### <span data-ttu-id="becb5-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="becb5-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="becb5-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="becb5-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="becb5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="becb5-107">DESCRIPTION</span></span>
<span data-ttu-id="becb5-108">Командлет **Disable-AzureRmOperationalInsightsLinuxCustomLogCollection** останавливает сбор настраиваемых журналов из подключенных компьютеров Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="becb5-108">The **Disable-AzureRmOperationalInsightsLinuxCustomLogCollection** cmdlet stops collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="becb5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="becb5-109">EXAMPLES</span></span>

## <span data-ttu-id="becb5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="becb5-110">PARAMETERS</span></span>

### <span data-ttu-id="becb5-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="becb5-111">-ResourceGroupName</span></span>
<span data-ttu-id="becb5-112">Указывает имя группы ресурсов, которая содержит компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="becb5-112">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="becb5-113">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="becb5-113">-Workspace</span></span>
<span data-ttu-id="becb5-114">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="becb5-114">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="becb5-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="becb5-115">-WorkspaceName</span></span>
<span data-ttu-id="becb5-116">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="becb5-116">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="becb5-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="becb5-117">-Confirm</span></span>
<span data-ttu-id="becb5-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="becb5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="becb5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="becb5-119">-WhatIf</span></span>
<span data-ttu-id="becb5-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="becb5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="becb5-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="becb5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="becb5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="becb5-122">-DefaultProfile</span></span>
<span data-ttu-id="becb5-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="becb5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="becb5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="becb5-124">CommonParameters</span></span>
<span data-ttu-id="becb5-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="becb5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="becb5-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="becb5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="becb5-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="becb5-127">INPUTS</span></span>

### <span data-ttu-id="becb5-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="becb5-128">PSWorkspace</span></span>
<span data-ttu-id="becb5-129">Параметр "Рабочая область" принимает значение типа "PSWorkspace" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="becb5-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="becb5-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="becb5-130">OUTPUTS</span></span>

### <span data-ttu-id="becb5-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="becb5-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="becb5-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="becb5-132">NOTES</span></span>
* <span data-ttu-id="becb5-133">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, эксплуатация, аналитика</span><span class="sxs-lookup"><span data-stu-id="becb5-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="becb5-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="becb5-134">RELATED LINKS</span></span>

[<span data-ttu-id="becb5-135">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="becb5-135">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)

