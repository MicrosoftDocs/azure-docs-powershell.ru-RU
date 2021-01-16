---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: cfd32e7ee70ffb387bd1d2a52fdbf5eb60f2e148
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402711"
---
# <span data-ttu-id="a998e-101">Get-AzPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="a998e-101">Get-AzPolicyMetadata</span></span>

## <span data-ttu-id="a998e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a998e-102">SYNOPSIS</span></span>
<span data-ttu-id="a998e-103">Ресурсы по метаданным политики</span><span class="sxs-lookup"><span data-stu-id="a998e-103">Gets Policy Metadata resources</span></span>

## <span data-ttu-id="a998e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a998e-104">SYNTAX</span></span>

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a998e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a998e-105">DESCRIPTION</span></span>
<span data-ttu-id="a998e-106">С **помощью cmdlet Get-AzPolicyRemediation** можно получить все ресурсы метаданных политики или определенный ресурс метаданных политики.</span><span class="sxs-lookup"><span data-stu-id="a998e-106">The **Get-AzPolicyRemediation** cmdlet gets all policy metadata resources or a particular policy metadata resource.</span></span>

## <span data-ttu-id="a998e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a998e-107">EXAMPLES</span></span>

### <span data-ttu-id="a998e-108">Пример 1. Получить все ресурсы метаданных политики</span><span class="sxs-lookup"><span data-stu-id="a998e-108">Example 1: Get all policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata
```

<span data-ttu-id="a998e-109">Эта команда получает все ресурсы метаданных политики.</span><span class="sxs-lookup"><span data-stu-id="a998e-109">This command gets all policy metadata resources</span></span>

### <span data-ttu-id="a998e-110">Пример 2. Получить набор из 10 ресурсов метаданных политики</span><span class="sxs-lookup"><span data-stu-id="a998e-110">Example 2: Get a collection of 10 policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

<span data-ttu-id="a998e-111">Эта команда получает набор из 10 ресурсов метаданных политики.</span><span class="sxs-lookup"><span data-stu-id="a998e-111">This command gets a collection of 10 policy metadata resources</span></span>

### <span data-ttu-id="a998e-112">Пример 3. Получить один ресурс метаданных политики с именем ACF1348</span><span class="sxs-lookup"><span data-stu-id="a998e-112">Example 3: Get a single policy metadata resource with the name 'ACF1348'</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

<span data-ttu-id="a998e-113">Эта команда получает один ресурс метаданных политики с именем ACF1348.</span><span class="sxs-lookup"><span data-stu-id="a998e-113">This command gets a single policy metadata resource with the name 'ACF1348'</span></span>

## <span data-ttu-id="a998e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a998e-114">PARAMETERS</span></span>

### <span data-ttu-id="a998e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a998e-115">-DefaultProfile</span></span>
<span data-ttu-id="a998e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a998e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a998e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a998e-117">-Name</span></span>
<span data-ttu-id="a998e-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="a998e-118">Resource name.</span></span>

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

### <span data-ttu-id="a998e-119">-Top</span><span class="sxs-lookup"><span data-stu-id="a998e-119">-Top</span></span>
<span data-ttu-id="a998e-120">Максимальное количество возвращаемых ресурсов метаданных политики.</span><span class="sxs-lookup"><span data-stu-id="a998e-120">Maximum number of policy metadata resources to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a998e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a998e-121">CommonParameters</span></span>
<span data-ttu-id="a998e-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a998e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a998e-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a998e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a998e-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a998e-124">INPUTS</span></span>

### <span data-ttu-id="a998e-125">System.String</span><span class="sxs-lookup"><span data-stu-id="a998e-125">System.String</span></span>

## <span data-ttu-id="a998e-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a998e-126">OUTPUTS</span></span>

### <span data-ttu-id="a998e-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="a998e-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span></span>

## <span data-ttu-id="a998e-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a998e-128">NOTES</span></span>

## <span data-ttu-id="a998e-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a998e-129">RELATED LINKS</span></span>