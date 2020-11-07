---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 784c71a284e2cf7711f50e86ea1b726d83eb6e40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570240"
---
# <span data-ttu-id="1883d-101">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1883d-101">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="1883d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1883d-102">SYNOPSIS</span></span>
<span data-ttu-id="1883d-103">Обновляет параметры HTTP для шлюза приложения на сервер.</span><span class="sxs-lookup"><span data-stu-id="1883d-103">Updates back-end HTTP settings for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1883d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1883d-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1883d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1883d-105">DESCRIPTION</span></span>
<span data-ttu-id="1883d-106">Командлет Set-AzureRmApplicationGatewayBackendHttpSettings обновляет параметры HTTP-протокола для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="1883d-106">The Set-AzureRmApplicationGatewayBackendHttpSettings cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="1883d-107">Серверные параметры HTTP применяются ко всем внутренним серверам в пуле.</span><span class="sxs-lookup"><span data-stu-id="1883d-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="1883d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1883d-108">EXAMPLES</span></span>

### <span data-ttu-id="1883d-109">Пример 1: Обновление параметров HTTP для шлюза приложения на сервер</span><span class="sxs-lookup"><span data-stu-id="1883d-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="1883d-110">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="1883d-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="1883d-111">Вторая команда обновляет параметры HTTP для шлюза приложений в переменной $AppGw, чтобы использовать порт 88, протокол HTTP и допускает сходство на основе файлов cookie.</span><span class="sxs-lookup"><span data-stu-id="1883d-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="1883d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1883d-112">PARAMETERS</span></span>

### <span data-ttu-id="1883d-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="1883d-113">-AffinityCookieName</span></span>
<span data-ttu-id="1883d-114">Имя cookie-файла, используемое для файла cookie схожести</span><span class="sxs-lookup"><span data-stu-id="1883d-114">Cookie name to use for the affinity cookie</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1883d-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1883d-115">-ApplicationGateway</span></span>
<span data-ttu-id="1883d-116">Указывает объект шлюза приложения, с которым этот командлет связывает серверные параметры HTTP.</span><span class="sxs-lookup"><span data-stu-id="1883d-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1883d-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="1883d-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="1883d-118">Определяет сертификаты проверки подлинности для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="1883d-118">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1883d-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="1883d-119">-ConnectionDraining</span></span>
<span data-ttu-id="1883d-120">Сток подключений для ресурса внутренних HTTP-параметров.</span><span class="sxs-lookup"><span data-stu-id="1883d-120">Connection draining of the backend http settings resource.</span></span>

```yaml
Type: PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1883d-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="1883d-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="1883d-122">Указывает, следует ли включать или отключать сходство на основе файлов cookie для пула серверов внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="1883d-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="1883d-123">Допустимые значения этого параметра: "отключено" и "включено".</span><span class="sxs-lookup"><span data-stu-id="1883d-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1883d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1883d-124">-DefaultProfile</span></span>
<span data-ttu-id="1883d-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1883d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1883d-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="1883d-126">-HostName</span></span>
<span data-ttu-id="1883d-127">Задает заголовок hosts, который будет отправляться внутренним серверам.</span><span class="sxs-lookup"><span data-stu-id="1883d-127">Sets host header to be sent to the backend servers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1883d-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1883d-128">-Name</span></span>
<span data-ttu-id="1883d-129">Указывает имя объекта параметров HTTP для серверного элемента.</span><span class="sxs-lookup"><span data-stu-id="1883d-129">Specifies the name of the back-end HTTP settings object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1883d-130">-Path</span><span class="sxs-lookup"><span data-stu-id="1883d-130">-Path</span></span>
<span data-ttu-id="1883d-131">Путь, который должен использоваться в качестве префикса для всех HTTP-запросов.</span><span class="sxs-lookup"><span data-stu-id="1883d-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="1883d-132">Если для этого параметра не задано значение, путь не будет иметь префикса.</span><span class="sxs-lookup"><span data-stu-id="1883d-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1883d-133">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="1883d-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="1883d-134">Флаг, если заголовок узла должен быть выбран из имени узла внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="1883d-134">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="1883d-135">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="1883d-135">-Port</span></span>
<span data-ttu-id="1883d-136">Указывает порт, который будет использоваться для каждого сервера в пуле на внутреннем сервере.</span><span class="sxs-lookup"><span data-stu-id="1883d-136">Specifies the port to use for each server in the back-end server pool.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1883d-137">-Зонд</span><span class="sxs-lookup"><span data-stu-id="1883d-137">-Probe</span></span>
<span data-ttu-id="1883d-138">Указывает зонд для связи с параметрами HTTP для веб-части.</span><span class="sxs-lookup"><span data-stu-id="1883d-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

```yaml
Type: PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1883d-139">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="1883d-139">-ProbeEnabled</span></span>
<span data-ttu-id="1883d-140">Флажок, если зонд должен быть включен.</span><span class="sxs-lookup"><span data-stu-id="1883d-140">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="1883d-141">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="1883d-141">-ProbeId</span></span>
<span data-ttu-id="1883d-142">Указывает идентификатор зонда, который нужно связать с параметрами HTTP для серверного элемента.</span><span class="sxs-lookup"><span data-stu-id="1883d-142">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1883d-143">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="1883d-143">-Protocol</span></span>
<span data-ttu-id="1883d-144">Указывает протокол для обмена данными между шлюзом приложения и внутренними серверами.</span><span class="sxs-lookup"><span data-stu-id="1883d-144">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="1883d-145">Допустимые значения этого параметра: HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="1883d-145">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="1883d-146">Этот параметр учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="1883d-146">This parameter is case-sensitive.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1883d-147">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="1883d-147">-RequestTimeout</span></span>
<span data-ttu-id="1883d-148">Указывает значение времени ожидания запроса.</span><span class="sxs-lookup"><span data-stu-id="1883d-148">Specifies a request time-out value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1883d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1883d-149">CommonParameters</span></span>
<span data-ttu-id="1883d-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1883d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1883d-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1883d-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1883d-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1883d-152">INPUTS</span></span>

### <span data-ttu-id="1883d-153">System. String</span><span class="sxs-lookup"><span data-stu-id="1883d-153">System.String</span></span>

## <span data-ttu-id="1883d-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1883d-154">OUTPUTS</span></span>

### <span data-ttu-id="1883d-155">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1883d-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1883d-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="1883d-156">NOTES</span></span>

## <span data-ttu-id="1883d-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1883d-157">RELATED LINKS</span></span>

[<span data-ttu-id="1883d-158">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1883d-158">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="1883d-159">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1883d-159">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="1883d-160">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1883d-160">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="1883d-161">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1883d-161">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()
