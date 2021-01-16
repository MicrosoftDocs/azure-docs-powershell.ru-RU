---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DC870E11-2129-4906-8357-D9BC1CF2E08E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzLocation.md
ms.openlocfilehash: f14da4760f70c8e4ba95136b81a884f830f4f44a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325321"
---
# <span data-ttu-id="e1d3f-101">Get-AzLocation</span><span class="sxs-lookup"><span data-stu-id="e1d3f-101">Get-AzLocation</span></span>

## <span data-ttu-id="e1d3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1d3f-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d3f-103">Возвращает все расположения и поддерживаемые поставщики ресурсов для каждого расположения.</span><span class="sxs-lookup"><span data-stu-id="e1d3f-103">Gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="e1d3f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e1d3f-104">SYNTAX</span></span>

```
Get-AzLocation [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1d3f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1d3f-105">DESCRIPTION</span></span>
<span data-ttu-id="e1d3f-106">Для **каждого из них можно получить все** расположения и поддерживаемых поставщиков ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e1d3f-106">The **Get-AzLocation** cmdlet gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="e1d3f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e1d3f-107">EXAMPLES</span></span>

### <span data-ttu-id="e1d3f-108">Пример 1. Получить все расположения и поддерживаемых поставщиков ресурсов</span><span class="sxs-lookup"><span data-stu-id="e1d3f-108">Example 1: Get all locations and the supported resource providers</span></span>
```
PS C:\>Get-AzLocation
```

<span data-ttu-id="e1d3f-109">Эта команда получает все расположения и поддерживаемые поставщики ресурсов для каждого расположения.</span><span class="sxs-lookup"><span data-stu-id="e1d3f-109">This command gets all locations and the supported resource providers for each location.</span></span>

## <span data-ttu-id="e1d3f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1d3f-110">PARAMETERS</span></span>

### <span data-ttu-id="e1d3f-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e1d3f-111">-ApiVersion</span></span>
<span data-ttu-id="e1d3f-112">Указывает версию API, которая поддерживается поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e1d3f-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e1d3f-113">Вы можете указать другую версию, чем версия по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e1d3f-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e1d3f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d3f-114">-DefaultProfile</span></span>
<span data-ttu-id="e1d3f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e1d3f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1d3f-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="e1d3f-116">-Pre</span></span>
<span data-ttu-id="e1d3f-117">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="e1d3f-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e1d3f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d3f-118">CommonParameters</span></span>
<span data-ttu-id="e1d3f-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1d3f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d3f-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1d3f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d3f-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1d3f-121">INPUTS</span></span>

### <span data-ttu-id="e1d3f-122">Нет</span><span class="sxs-lookup"><span data-stu-id="e1d3f-122">None</span></span>

## <span data-ttu-id="e1d3f-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e1d3f-123">OUTPUTS</span></span>

### <span data-ttu-id="e1d3f-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span><span class="sxs-lookup"><span data-stu-id="e1d3f-124">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProviderLocation</span></span>

## <span data-ttu-id="e1d3f-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e1d3f-125">NOTES</span></span>

## <span data-ttu-id="e1d3f-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1d3f-126">RELATED LINKS</span></span>