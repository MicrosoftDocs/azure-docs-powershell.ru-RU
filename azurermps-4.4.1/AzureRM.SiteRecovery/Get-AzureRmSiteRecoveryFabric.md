---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 28EEB54B-C8C9-4C20-9454-5069C23583B9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 591cbcbc4663bde7b9d6e9bd4e35a1e91728cd85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562112"
---
# <span data-ttu-id="5c374-101">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="5c374-101">Get-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="5c374-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5c374-102">SYNOPSIS</span></span>
<span data-ttu-id="5c374-103">Получение свойств структуры восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="5c374-103">Get the properties of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c374-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5c374-104">SYNTAX</span></span>

### <span data-ttu-id="5c374-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5c374-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c374-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5c374-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c374-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="5c374-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c374-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c374-108">DESCRIPTION</span></span>
<span data-ttu-id="5c374-109">Командлет **Get-AzureRmSiteRecoveryFabric** получает свойства указанной структуры восстановления сайта Azure или всех структур восстановления сайта Azure в хранилище службы восстановления.</span><span class="sxs-lookup"><span data-stu-id="5c374-109">The **Get-AzureRmSiteRecoveryFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="5c374-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5c374-110">EXAMPLES</span></span>

## <span data-ttu-id="5c374-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5c374-111">PARAMETERS</span></span>

### <span data-ttu-id="5c374-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5c374-112">-FriendlyName</span></span>
<span data-ttu-id="5c374-113">Указывает понятное имя структуры восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="5c374-113">Specifies the friendly name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c374-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5c374-114">-Name</span></span>
<span data-ttu-id="5c374-115">Указывает имя структуры восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="5c374-115">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c374-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c374-116">-DefaultProfile</span></span>
<span data-ttu-id="5c374-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5c374-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c374-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c374-118">CommonParameters</span></span>
<span data-ttu-id="5c374-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5c374-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c374-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c374-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c374-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5c374-121">INPUTS</span></span>

## <span data-ttu-id="5c374-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c374-122">OUTPUTS</span></span>

### <span data-ttu-id="5c374-123">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRFabric, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="5c374-123">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5c374-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="5c374-124">NOTES</span></span>

## <span data-ttu-id="5c374-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c374-125">RELATED LINKS</span></span>

[<span data-ttu-id="5c374-126">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="5c374-126">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="5c374-127">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="5c374-127">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)