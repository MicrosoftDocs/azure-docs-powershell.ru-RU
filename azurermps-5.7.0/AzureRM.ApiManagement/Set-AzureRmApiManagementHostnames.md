---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F9CE8705-F7B1-45AB-98BC-FC6DC023D38D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementhostnames
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
ms.openlocfilehash: d48d1913a30fc03ca0ebaf86195b981a6ebe70fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569083"
---
# <span data-ttu-id="a5036-101">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="a5036-101">Set-AzureRmApiManagementHostnames</span></span>

## <span data-ttu-id="a5036-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a5036-102">SYNOPSIS</span></span>
<span data-ttu-id="a5036-103">Задает настраиваемую конфигурацию hostname для прокси-сервера или портала службы управления API.</span><span class="sxs-lookup"><span data-stu-id="a5036-103">Sets a custom hostname configuration for an API Management service proxy or portal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5036-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a5036-104">SYNTAX</span></span>

### <span data-ttu-id="a5036-105">SetSpecificService (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a5036-105">SetSpecificService (Default)</span></span>
```
Set-AzureRmApiManagementHostnames -ResourceGroupName <String> -Name <String>
 [-PortalHostnameConfiguration <PsApiManagementHostnameConfiguration>]
 [-ProxyHostnameConfiguration <PsApiManagementHostnameConfiguration>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5036-106">SetFromPsApiManagementInstance</span><span class="sxs-lookup"><span data-stu-id="a5036-106">SetFromPsApiManagementInstance</span></span>
```
Set-AzureRmApiManagementHostnames -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5036-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5036-107">DESCRIPTION</span></span>
<span data-ttu-id="a5036-108">Командлет **Set-AzureRmApiManagementHostnames** применяет настраиваемую конфигурацию hostname для прокси-сервера или портала службы управления API.</span><span class="sxs-lookup"><span data-stu-id="a5036-108">The **Set-AzureRmApiManagementHostnames** cmdlet applies a custom hostname configuration for an API Management service proxy or portal.</span></span>

## <span data-ttu-id="a5036-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a5036-109">EXAMPLES</span></span>

### <span data-ttu-id="a5036-110">Пример 1: Настройка конфигурации настраиваемого hostname для прокси-сервера и портала</span><span class="sxs-lookup"><span data-stu-id="a5036-110">Example 1: Set the custom hostname configuration for a proxy and portal</span></span>
```
PS C:\>Set-AzureRmApiManagementHostnames -Name ContosoApi -ResourceGroupName Contoso -PortalHostnameConfiguration $portalHostnameConf -ProxyHostnameConfiguration $proxyHostnameConf
```

<span data-ttu-id="a5036-111">Эта команда задает настраиваемое имя HostName Configuration для прокси-сервера и портала.</span><span class="sxs-lookup"><span data-stu-id="a5036-111">This command sets the custom hostname configuration for proxy and portal.</span></span>

### <span data-ttu-id="a5036-112">Пример 2: Настройка настраиваемого имени узла для прокси-сервера и портала</span><span class="sxs-lookup"><span data-stu-id="a5036-112">Example 2: Configure a custom hostname for a proxy and portal</span></span>
```
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name ContosoApi -ResourceGroupName "Contoso" -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
PS C:\> Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName "Contoso" -HostnameType "Portal" -PfxPath "C:\portalcert.pfx" -PfxPassword "CertSecret"
PS C:\> $PortalHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
PS C:\> $ProxyHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "proxy.contoso.com" -CertificateThumbprint "5DD7CCF6A1E74E0987DD2873406B7264"
PS C:\> Set-AzureRmApiManagementHostnames -Name "ContosoApi" -ResourceGroupName "Contoso" -PortalHostnameConfiguration $PortalHostnameConf -ProxyHostnameConfiguration $ProxyHostnameConf
```

<span data-ttu-id="a5036-113">В этом примере осуществляется настройка настраиваемого имени узла для прокси-сервера и портала.</span><span class="sxs-lookup"><span data-stu-id="a5036-113">This example configures a custom hostname for proxy and portal.</span></span>
<span data-ttu-id="a5036-114">Вам нужно импортировать соответствующие сертификаты и затем применить пользовательские имена узлов.</span><span class="sxs-lookup"><span data-stu-id="a5036-114">You need to import corresponding certificates and then apply the custom hostnames.</span></span>

## <span data-ttu-id="a5036-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a5036-115">PARAMETERS</span></span>

### <span data-ttu-id="a5036-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a5036-116">-ApiManagement</span></span>
<span data-ttu-id="a5036-117">Указывает экземпляр **PsApiManagement** , который этот командлет получает для параметров *PortalHostnameConfiguration* и *ProxyHostnameConfiguration* .</span><span class="sxs-lookup"><span data-stu-id="a5036-117">Specifies the **PsApiManagement** instance that this cmdlet gets the *PortalHostnameConfiguration* and *ProxyHostnameConfiguration* parameters from.</span></span>

```yaml
Type: PsApiManagement
Parameter Sets: SetFromPsApiManagementInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5036-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5036-118">-DefaultProfile</span></span>
<span data-ttu-id="a5036-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5036-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="a5036-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a5036-120">-Name</span></span>
<span data-ttu-id="a5036-121">Указывает имя экземпляра управления API.</span><span class="sxs-lookup"><span data-stu-id="a5036-121">Specifies the name of the API Management instance.</span></span>

```yaml
Type: String
Parameter Sets: SetSpecificService
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5036-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5036-122">-PassThru</span></span>
<span data-ttu-id="a5036-123">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="a5036-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a5036-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a5036-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5036-125">-PortalHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5036-125">-PortalHostnameConfiguration</span></span>
<span data-ttu-id="a5036-126">Указывает конфигурацию узла настраиваемого портала.</span><span class="sxs-lookup"><span data-stu-id="a5036-126">Specifies the custom portal hostname configuration.</span></span>
<span data-ttu-id="a5036-127">Передача $null командлету задает имя узла по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a5036-127">Passing $null to the cmdlet sets the default hostname.</span></span>

```yaml
Type: PsApiManagementHostnameConfiguration
Parameter Sets: SetSpecificService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5036-128">-ProxyHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5036-128">-ProxyHostnameConfiguration</span></span>
<span data-ttu-id="a5036-129">Указывает конфигурацию имени пользователя прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="a5036-129">Specifies the custom proxy hostname configuration.</span></span>
<span data-ttu-id="a5036-130">Передача $null задает имя узла по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a5036-130">Passing $null sets the default hostname.</span></span>

```yaml
Type: PsApiManagementHostnameConfiguration
Parameter Sets: SetSpecificService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5036-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5036-131">-ResourceGroupName</span></span>
<span data-ttu-id="a5036-132">Указывает имя группы ресурсов, в которой находится экземпляр управления API.</span><span class="sxs-lookup"><span data-stu-id="a5036-132">Specifies the name of the resource group under which the API Management instance exists.</span></span>

```yaml
Type: String
Parameter Sets: SetSpecificService
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5036-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5036-133">CommonParameters</span></span>
<span data-ttu-id="a5036-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a5036-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5036-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5036-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5036-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a5036-136">INPUTS</span></span>

### <span data-ttu-id="a5036-137">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="a5036-137">PsApiManagement</span></span>
<span data-ttu-id="a5036-138">Параметр "ApiManagement" принимает значение типа "PsApiManagement" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a5036-138">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="a5036-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5036-139">OUTPUTS</span></span>

### <span data-ttu-id="a5036-140">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="a5036-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="a5036-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="a5036-141">NOTES</span></span>

## <span data-ttu-id="a5036-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5036-142">RELATED LINKS</span></span>

[<span data-ttu-id="a5036-143">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="a5036-143">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="a5036-144">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5036-144">New-AzureRmApiManagementHostnameConfiguration</span></span>](./New-AzureRmApiManagementHostnameConfiguration.md)

