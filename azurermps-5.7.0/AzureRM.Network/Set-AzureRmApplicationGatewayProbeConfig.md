---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 65825e1cbb5da41d1557d30b0f152ee456e6e86b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566579"
---
# <span data-ttu-id="e88f6-101">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e88f6-101">Set-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="e88f6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e88f6-102">SYNOPSIS</span></span>
<span data-ttu-id="e88f6-103">Настройка конфигурации проверки работоспособности на существующем шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="e88f6-103">Sets the health probe configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e88f6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e88f6-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e88f6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e88f6-105">DESCRIPTION</span></span>
<span data-ttu-id="e88f6-106">Командлет Set-AzureRmApplicationGatewayProbeConfig задает конфигурацию проверки работоспособности на существующем шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="e88f6-106">The Set-AzureRmApplicationGatewayProbeConfig cmdlet sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="e88f6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e88f6-107">EXAMPLES</span></span>

### <span data-ttu-id="e88f6-108">Пример 1: Настройка конфигурации для проверки работоспособности на шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="e88f6-108">Example 1: Set the configuration for a health probe on an application gateway</span></span>
```
PS C:\>Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="e88f6-109">Эта команда задает конфигурацию для проверки работоспособности с именем Probe05 для шлюза приложения с именем Gateway.</span><span class="sxs-lookup"><span data-stu-id="e88f6-109">This command sets the configuration for a health probe named Probe05 for the application gateway named Gateway.</span></span>
<span data-ttu-id="e88f6-110">Кроме того, команда устанавливает для порога неработоспособности 8 повторных попыток и время ожидания после 120 секунд.</span><span class="sxs-lookup"><span data-stu-id="e88f6-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="e88f6-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e88f6-111">PARAMETERS</span></span>

### <span data-ttu-id="e88f6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e88f6-112">-ApplicationGateway</span></span>
<span data-ttu-id="e88f6-113">Указывает шлюз приложения, которому этот командлет отправляет зонд.</span><span class="sxs-lookup"><span data-stu-id="e88f6-113">Specifies the application gateway to which this cmdlet sends a probe.</span></span>

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

### <span data-ttu-id="e88f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e88f6-114">-DefaultProfile</span></span>
<span data-ttu-id="e88f6-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e88f6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e88f6-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="e88f6-116">-HostName</span></span>
<span data-ttu-id="e88f6-117">Указывает имя хоста, на которое этот командлет отправляет зонд.</span><span class="sxs-lookup"><span data-stu-id="e88f6-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="e88f6-118">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="e88f6-118">-Interval</span></span>
<span data-ttu-id="e88f6-119">Задает интервал проверки в секундах.</span><span class="sxs-lookup"><span data-stu-id="e88f6-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="e88f6-120">Это интервал времени между двумя последовательными зондами.</span><span class="sxs-lookup"><span data-stu-id="e88f6-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="e88f6-121">Это значение находится в диапазоне от 1 секунды до 86400 секунд.</span><span class="sxs-lookup"><span data-stu-id="e88f6-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="e88f6-122">-Match</span><span class="sxs-lookup"><span data-stu-id="e88f6-122">-Match</span></span>
<span data-ttu-id="e88f6-123">Текст, который должен содержаться в ответе работоспособности.</span><span class="sxs-lookup"><span data-stu-id="e88f6-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="e88f6-124">Пустое значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e88f6-124">Default value is empty</span></span>

```yaml
Type: PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88f6-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="e88f6-125">-MinServers</span></span>
<span data-ttu-id="e88f6-126">Минимальное количество серверов, которые всегда помечаются как работоспособные.</span><span class="sxs-lookup"><span data-stu-id="e88f6-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="e88f6-127">Значение по умолчанию: 0</span><span class="sxs-lookup"><span data-stu-id="e88f6-127">Default value is 0</span></span>

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

### <span data-ttu-id="e88f6-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e88f6-128">-Name</span></span>
<span data-ttu-id="e88f6-129">Указывает имя зонда.</span><span class="sxs-lookup"><span data-stu-id="e88f6-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="e88f6-130">-Path</span><span class="sxs-lookup"><span data-stu-id="e88f6-130">-Path</span></span>
<span data-ttu-id="e88f6-131">Указывает относительный путь к зонду.</span><span class="sxs-lookup"><span data-stu-id="e88f6-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="e88f6-132">Допустимый путь начинается с символа косой черты (/).</span><span class="sxs-lookup"><span data-stu-id="e88f6-132">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="e88f6-133">Пробный зонд отправляется в \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="e88f6-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="e88f6-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e88f6-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="e88f6-135">Следует ли выбирать заголовок узла из параметров внутреннего HTTP-сервера.</span><span class="sxs-lookup"><span data-stu-id="e88f6-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="e88f6-136">Значение по умолчанию: ложь</span><span class="sxs-lookup"><span data-stu-id="e88f6-136">Default value is false</span></span>

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

### <span data-ttu-id="e88f6-137">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="e88f6-137">-Protocol</span></span>
<span data-ttu-id="e88f6-138">Указывает протокол, используемый для отправки пробной проверки.</span><span class="sxs-lookup"><span data-stu-id="e88f6-138">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="e88f6-139">-Timeout</span><span class="sxs-lookup"><span data-stu-id="e88f6-139">-Timeout</span></span>
<span data-ttu-id="e88f6-140">Задает время ожидания пробы в секундах.</span><span class="sxs-lookup"><span data-stu-id="e88f6-140">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="e88f6-141">Этот командлет помечает пробу как сбой, если допустимый ответ не получен за этот период ожидания.</span><span class="sxs-lookup"><span data-stu-id="e88f6-141">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="e88f6-142">Допустимые значения: от 1 секунды до 86400 секунд.</span><span class="sxs-lookup"><span data-stu-id="e88f6-142">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="e88f6-143">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="e88f6-143">-UnhealthyThreshold</span></span>
<span data-ttu-id="e88f6-144">Указывает число повторных попыток проверки.</span><span class="sxs-lookup"><span data-stu-id="e88f6-144">Specifies the probe retry count.</span></span>
<span data-ttu-id="e88f6-145">Внутренний сервер помечается вниз после появления счетчика неудачных последовательностей проверки появления нерабочего порогового значения.</span><span class="sxs-lookup"><span data-stu-id="e88f6-145">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="e88f6-146">Допустимые значения находятся в диапазоне от 1 секунды до 20 секунд.</span><span class="sxs-lookup"><span data-stu-id="e88f6-146">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="e88f6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e88f6-147">CommonParameters</span></span>
<span data-ttu-id="e88f6-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e88f6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e88f6-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e88f6-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e88f6-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e88f6-150">INPUTS</span></span>

### <span data-ttu-id="e88f6-151">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e88f6-151">PSApplicationGateway</span></span>
<span data-ttu-id="e88f6-152">Параметр "ApplicationGateway" принимает значение типа "PSApplicationGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e88f6-152">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="e88f6-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e88f6-153">OUTPUTS</span></span>

### <span data-ttu-id="e88f6-154">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e88f6-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e88f6-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="e88f6-155">NOTES</span></span>

## <span data-ttu-id="e88f6-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e88f6-156">RELATED LINKS</span></span>

[<span data-ttu-id="e88f6-157">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e88f6-157">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="e88f6-158">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e88f6-158">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="e88f6-159">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e88f6-159">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="e88f6-160">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e88f6-160">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()
