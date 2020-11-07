---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 49674f372e477ee7050a6ccf7d833aaee59bac3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562304"
---
# <span data-ttu-id="74384-101">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="74384-101">Remove-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="74384-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74384-102">SYNOPSIS</span></span>
<span data-ttu-id="74384-103">Удаляет источник данных.</span><span class="sxs-lookup"><span data-stu-id="74384-103">Deletes a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74384-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74384-104">SYNTAX</span></span>

### <span data-ttu-id="74384-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="74384-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74384-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="74384-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74384-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74384-107">DESCRIPTION</span></span>
<span data-ttu-id="74384-108">Командлет **Remove-AzureRmOperationalInsightsDataSource** удаляет источник данных.</span><span class="sxs-lookup"><span data-stu-id="74384-108">The **Remove-AzureRmOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="74384-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74384-109">EXAMPLES</span></span>

## <span data-ttu-id="74384-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74384-110">PARAMETERS</span></span>

### <span data-ttu-id="74384-111">-Force</span><span class="sxs-lookup"><span data-stu-id="74384-111">-Force</span></span>
<span data-ttu-id="74384-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="74384-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="74384-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="74384-113">-Name</span></span>
<span data-ttu-id="74384-114">Указывает имя источника данных, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="74384-114">Specifies the name of a data source to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74384-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74384-115">-ResourceGroupName</span></span>
<span data-ttu-id="74384-116">Указывает имя группы ресурсов, содержащей компьютеры.</span><span class="sxs-lookup"><span data-stu-id="74384-116">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="74384-117">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="74384-117">-Workspace</span></span>
<span data-ttu-id="74384-118">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="74384-118">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="74384-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="74384-119">-WorkspaceName</span></span>
<span data-ttu-id="74384-120">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="74384-120">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="74384-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74384-121">-Confirm</span></span>
<span data-ttu-id="74384-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="74384-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74384-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74384-123">-WhatIf</span></span>
<span data-ttu-id="74384-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="74384-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74384-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="74384-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74384-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74384-126">-DefaultProfile</span></span>
<span data-ttu-id="74384-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74384-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74384-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74384-128">CommonParameters</span></span>
<span data-ttu-id="74384-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74384-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74384-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74384-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74384-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74384-131">INPUTS</span></span>

### <span data-ttu-id="74384-132">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="74384-132">PSWorkspace</span></span>
<span data-ttu-id="74384-133">Параметр "Рабочая область" принимает значение типа "PSWorkspace" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="74384-133">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="74384-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74384-134">OUTPUTS</span></span>

## <span data-ttu-id="74384-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="74384-135">NOTES</span></span>
* <span data-ttu-id="74384-136">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, эксплуатация, аналитика</span><span class="sxs-lookup"><span data-stu-id="74384-136">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="74384-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74384-137">RELATED LINKS</span></span>

[<span data-ttu-id="74384-138">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="74384-138">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="74384-139">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="74384-139">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)

