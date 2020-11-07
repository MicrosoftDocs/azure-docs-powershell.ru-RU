---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 13d8be80411e39124ab29d9a31e44edd0ebd95e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559588"
---
# <span data-ttu-id="5bc25-101">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5bc25-101">Set-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="5bc25-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5bc25-102">SYNOPSIS</span></span>
<span data-ttu-id="5bc25-103">Обновляет источник данных.</span><span class="sxs-lookup"><span data-stu-id="5bc25-103">Updates a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bc25-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5bc25-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsDataSource [-DataSource] <PSDataSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bc25-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5bc25-105">DESCRIPTION</span></span>
<span data-ttu-id="5bc25-106">Командлет **Set-AzureRmOperationalInsightsDataSource** обновляет источник данных.</span><span class="sxs-lookup"><span data-stu-id="5bc25-106">The **Set-AzureRmOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="5bc25-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5bc25-107">EXAMPLES</span></span>

## <span data-ttu-id="5bc25-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5bc25-108">PARAMETERS</span></span>

### <span data-ttu-id="5bc25-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="5bc25-109">-DataSource</span></span>
<span data-ttu-id="5bc25-110">Указывает источник данных, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="5bc25-110">Specifies the data source that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bc25-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bc25-111">-DefaultProfile</span></span>
<span data-ttu-id="5bc25-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5bc25-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bc25-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bc25-113">CommonParameters</span></span>
<span data-ttu-id="5bc25-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5bc25-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bc25-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bc25-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bc25-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5bc25-116">INPUTS</span></span>

### <span data-ttu-id="5bc25-117">PSDataSource</span><span class="sxs-lookup"><span data-stu-id="5bc25-117">PSDataSource</span></span>
<span data-ttu-id="5bc25-118">Параметр DataSource принимает значение типа "PSDataSource" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="5bc25-118">Parameter 'DataSource' accepts value of type 'PSDataSource' from the pipeline</span></span>

## <span data-ttu-id="5bc25-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5bc25-119">OUTPUTS</span></span>

### <span data-ttu-id="5bc25-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="5bc25-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="5bc25-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="5bc25-121">NOTES</span></span>
* <span data-ttu-id="5bc25-122">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, эксплуатация, аналитика</span><span class="sxs-lookup"><span data-stu-id="5bc25-122">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="5bc25-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5bc25-123">RELATED LINKS</span></span>

[<span data-ttu-id="5bc25-124">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5bc25-124">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="5bc25-125">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="5bc25-125">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)

