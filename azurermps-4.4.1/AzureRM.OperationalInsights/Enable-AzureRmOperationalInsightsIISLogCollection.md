---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: b9ab24915af941cec866fb78003d2b0e9c11267c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567556"
---
# <span data-ttu-id="a263f-101">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="a263f-101">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="a263f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a263f-102">SYNOPSIS</span></span>
<span data-ttu-id="a263f-103">Запускает сбор журналов IIS на компьютерах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a263f-103">Starts collection of IIS logs from computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a263f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a263f-104">SYNTAX</span></span>

### <span data-ttu-id="a263f-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a263f-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a263f-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a263f-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a263f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a263f-107">DESCRIPTION</span></span>
<span data-ttu-id="a263f-108">Командлет **Enable-AzureRmOperationalInsightsIISLogCollection** запускает сбор журналов служб IIS с подключенных компьютеров в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="a263f-108">The **Enable-AzureRmOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="a263f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a263f-109">EXAMPLES</span></span>

## <span data-ttu-id="a263f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a263f-110">PARAMETERS</span></span>

### <span data-ttu-id="a263f-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a263f-111">-ResourceGroupName</span></span>
<span data-ttu-id="a263f-112">Указывает имя группы ресурсов, содержащей компьютеры.</span><span class="sxs-lookup"><span data-stu-id="a263f-112">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="a263f-113">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="a263f-113">-Workspace</span></span>
<span data-ttu-id="a263f-114">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a263f-114">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="a263f-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a263f-115">-WorkspaceName</span></span>
<span data-ttu-id="a263f-116">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a263f-116">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="a263f-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a263f-117">-Confirm</span></span>
<span data-ttu-id="a263f-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a263f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a263f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a263f-119">-WhatIf</span></span>
<span data-ttu-id="a263f-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a263f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a263f-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a263f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a263f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a263f-122">-DefaultProfile</span></span>
<span data-ttu-id="a263f-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a263f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a263f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a263f-124">CommonParameters</span></span>
<span data-ttu-id="a263f-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a263f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a263f-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a263f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a263f-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a263f-127">INPUTS</span></span>

### <span data-ttu-id="a263f-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a263f-128">PSWorkspace</span></span>
<span data-ttu-id="a263f-129">Параметр "Рабочая область" принимает значение типа "PSWorkspace" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a263f-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="a263f-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a263f-130">OUTPUTS</span></span>

### <span data-ttu-id="a263f-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="a263f-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="a263f-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="a263f-132">NOTES</span></span>

## <span data-ttu-id="a263f-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a263f-133">RELATED LINKS</span></span>

[<span data-ttu-id="a263f-134">Disable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="a263f-134">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Disable-AzureRmOperationalInsightsIISLogCollection.md)

