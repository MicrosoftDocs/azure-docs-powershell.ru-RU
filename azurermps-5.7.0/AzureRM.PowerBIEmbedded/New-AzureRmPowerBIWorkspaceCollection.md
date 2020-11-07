---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 56cf34fce43465594a0a8862194bb15b117dda6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557300"
---
# <span data-ttu-id="af2c4-101">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="af2c4-101">New-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="af2c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af2c4-102">SYNOPSIS</span></span>
<span data-ttu-id="af2c4-103">Создает набор рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="af2c4-103">Creates a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af2c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af2c4-104">SYNTAX</span></span>

```
New-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af2c4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af2c4-105">DESCRIPTION</span></span>
<span data-ttu-id="af2c4-106">Командлет **New-AzureRmPowerBIWorkspaceCollection** создает набор рабочих областей Power BI для подписки Azure в указанной группе ресурсов и расположении.</span><span class="sxs-lookup"><span data-stu-id="af2c4-106">The **New-AzureRmPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="af2c4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af2c4-107">EXAMPLES</span></span>

### <span data-ttu-id="af2c4-108">Пример 1: создание коллекции рабочих областей</span><span class="sxs-lookup"><span data-stu-id="af2c4-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="af2c4-109">Эта команда создает коллекцию рабочих областей с именем WCN11 в указанной группе ресурсов в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="af2c4-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="af2c4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af2c4-110">PARAMETERS</span></span>

### <span data-ttu-id="af2c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af2c4-111">-DefaultProfile</span></span>
<span data-ttu-id="af2c4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="af2c4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af2c4-113">-Location</span><span class="sxs-lookup"><span data-stu-id="af2c4-113">-Location</span></span>
<span data-ttu-id="af2c4-114">Указывает расположение Azure, в котором этот командлет создает коллекцию рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="af2c4-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af2c4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af2c4-115">-ResourceGroupName</span></span>
<span data-ttu-id="af2c4-116">Указывает имя группы ресурсов, в которой этот командлет создает коллекцию рабочих областей.</span><span class="sxs-lookup"><span data-stu-id="af2c4-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af2c4-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="af2c4-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="af2c4-118">Задает имя коллекции рабочих областей Power BI.</span><span class="sxs-lookup"><span data-stu-id="af2c4-118">Specifies a name for the Power BI workspace collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af2c4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af2c4-119">-Confirm</span></span>
<span data-ttu-id="af2c4-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="af2c4-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af2c4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af2c4-121">-WhatIf</span></span>
<span data-ttu-id="af2c4-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="af2c4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af2c4-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="af2c4-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af2c4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af2c4-124">CommonParameters</span></span>
<span data-ttu-id="af2c4-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af2c4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af2c4-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af2c4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af2c4-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af2c4-127">INPUTS</span></span>

### <span data-ttu-id="af2c4-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="af2c4-128">None</span></span>
<span data-ttu-id="af2c4-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="af2c4-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="af2c4-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af2c4-130">OUTPUTS</span></span>

### <span data-ttu-id="af2c4-131">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="af2c4-131">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="af2c4-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="af2c4-132">NOTES</span></span>

## <span data-ttu-id="af2c4-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af2c4-133">RELATED LINKS</span></span>

[<span data-ttu-id="af2c4-134">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="af2c4-134">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="af2c4-135">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="af2c4-135">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)

