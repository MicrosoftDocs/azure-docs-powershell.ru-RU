---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
ms.openlocfilehash: 352e40aa64adf5eea98950ac9271f0237e634ab6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392412"
---
# <span data-ttu-id="1a9f1-101">New-AzApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1a9f1-101">New-AzApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="1a9f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a9f1-102">SYNOPSIS</span></span>
<span data-ttu-id="1a9f1-103">Создает объект `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="1a9f1-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

## <span data-ttu-id="1a9f1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1a9f1-104">SYNTAX</span></span>

```
New-AzApiManagementBackendServiceFabric -ManagementEndpoint <String[]> -ClientCertificateThumbprint <String>
 [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>] [-ServerCertificateThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a9f1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a9f1-105">DESCRIPTION</span></span>

<span data-ttu-id="1a9f1-106">Для выполнения cmdlet **New-AzApiManagementBackendServiceFabric** создается объект, который будет использоваться в `PsApiManagementServiceFabric` cmdlet **New-AzApiManagementBackend** и **Set-AzApiManagementBackend.**</span><span class="sxs-lookup"><span data-stu-id="1a9f1-106">The **New-AzApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzApiManagementBackend** and **Set-AzApiManagementBackend**.</span></span>

## <span data-ttu-id="1a9f1-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1a9f1-107">EXAMPLES</span></span>

### <span data-ttu-id="1a9f1-108">Пример 1. Создание объекта "Ткань из In-Memory службы"</span><span class="sxs-lookup"><span data-stu-id="1a9f1-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="1a9f1-109">Создание контракта с структурой службы</span><span class="sxs-lookup"><span data-stu-id="1a9f1-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="1a9f1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a9f1-110">PARAMETERS</span></span>

### <span data-ttu-id="1a9f1-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="1a9f1-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="1a9f1-112">Эскиз клиентского сертификата для конечной точки управления.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="1a9f1-113">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="1a9f1-113">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a9f1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a9f1-114">-DefaultProfile</span></span>
<span data-ttu-id="1a9f1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a9f1-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a9f1-116">-ManagementEndpoint</span></span>
<span data-ttu-id="1a9f1-117">Конечные точки управления "Ткань службы".</span><span class="sxs-lookup"><span data-stu-id="1a9f1-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="1a9f1-118">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="1a9f1-118">This parameter is required.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a9f1-119">-MaxPartitionResolutionRetry</span><span class="sxs-lookup"><span data-stu-id="1a9f1-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="1a9f1-120">Максимальное количество ирисов при разрешении раздела "Ткань услуги".</span><span class="sxs-lookup"><span data-stu-id="1a9f1-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="1a9f1-121">Этот параметр необязателен, а значение по умолчанию — 5.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-121">This parameter is optional and default value is 5.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a9f1-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="1a9f1-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="1a9f1-123">Thumbprint of certificates cluster management service uses for tls communication. Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a9f1-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="1a9f1-124">-ServerX509Name</span></span>
<span data-ttu-id="1a9f1-125">Коллекция имен сертификатов Сервера X509.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="1a9f1-126">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-126">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a9f1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a9f1-127">CommonParameters</span></span>
<span data-ttu-id="1a9f1-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a9f1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a9f1-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a9f1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a9f1-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1a9f1-130">INPUTS</span></span>

### <span data-ttu-id="1a9f1-131">System.String</span><span class="sxs-lookup"><span data-stu-id="1a9f1-131">System.String</span></span>

## <span data-ttu-id="1a9f1-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1a9f1-132">OUTPUTS</span></span>

### <span data-ttu-id="1a9f1-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="1a9f1-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="1a9f1-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1a9f1-134">NOTES</span></span>

## <span data-ttu-id="1a9f1-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a9f1-135">RELATED LINKS</span></span>

[<span data-ttu-id="1a9f1-136">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1a9f1-136">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="1a9f1-137">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1a9f1-137">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="1a9f1-138">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="1a9f1-138">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="1a9f1-139">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1a9f1-139">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="1a9f1-140">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="1a9f1-140">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)