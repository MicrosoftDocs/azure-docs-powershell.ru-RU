---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
ms.openlocfilehash: df871dff0f59bc9c1e319e1470bbaa37750542e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565629"
---
# <span data-ttu-id="02261-101">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="02261-101">Test-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="02261-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="02261-102">SYNOPSIS</span></span>
<span data-ttu-id="02261-103">Проверяет, можно ли добавить в конечную точку настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="02261-103">Checks whether a custom domain can be added to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02261-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="02261-104">SYNTAX</span></span>

### <span data-ttu-id="02261-105">Параметры, заданные для параметров полей (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="02261-105">Parameter Set for fields parameters (Default)</span></span>
```
Test-AzureRmCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02261-106">Параметр, заданный для параметров объекта</span><span class="sxs-lookup"><span data-stu-id="02261-106">Parameter Set for object parameters</span></span>
```
Test-AzureRmCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02261-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02261-107">DESCRIPTION</span></span>
<span data-ttu-id="02261-108">Командлет **Test-AzureRmCdnCustomDomain** проверяет, можно ли добавить настраиваемый домен в конечную точку, проверив сопоставление CNAME.</span><span class="sxs-lookup"><span data-stu-id="02261-108">The **Test-AzureRmCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="02261-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="02261-109">EXAMPLES</span></span>

## <span data-ttu-id="02261-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="02261-110">PARAMETERS</span></span>

### <span data-ttu-id="02261-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="02261-111">-CdnEndpoint</span></span>
<span data-ttu-id="02261-112">Задает конечную точку, в которую вы хотите добавить настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="02261-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02261-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="02261-113">-CustomDomainHostName</span></span>
<span data-ttu-id="02261-114">Указывает имя узла для настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="02261-114">Specifies the host name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02261-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="02261-115">-EndpointName</span></span>
<span data-ttu-id="02261-116">Указывает имя конечной точки, в которую вы хотите добавить настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="02261-116">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02261-117">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="02261-117">-ProfileName</span></span>
<span data-ttu-id="02261-118">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="02261-118">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02261-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02261-119">-ResourceGroupName</span></span>
<span data-ttu-id="02261-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="02261-120">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02261-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02261-121">-DefaultProfile</span></span>
<span data-ttu-id="02261-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="02261-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02261-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02261-123">CommonParameters</span></span>
<span data-ttu-id="02261-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="02261-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02261-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02261-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02261-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="02261-126">INPUTS</span></span>

### <span data-ttu-id="02261-127">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="02261-127">PSEndpoint</span></span>
<span data-ttu-id="02261-128">Параметр "CdnEndpoint" принимает значение типа "PSEndpoint" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="02261-128">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="02261-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="02261-129">OUTPUTS</span></span>

### <span data-ttu-id="02261-130">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="02261-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="02261-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="02261-131">NOTES</span></span>

## <span data-ttu-id="02261-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02261-132">RELATED LINKS</span></span>

[<span data-ttu-id="02261-133">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="02261-133">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="02261-134">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="02261-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="02261-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="02261-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)

