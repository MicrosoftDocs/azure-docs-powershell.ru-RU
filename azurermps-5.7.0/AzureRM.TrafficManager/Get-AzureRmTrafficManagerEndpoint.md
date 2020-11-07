---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 488643c8f977fb59af0f5b73c9388e65b3425c1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566873"
---
# <span data-ttu-id="a68b2-101">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a68b2-101">Get-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="a68b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a68b2-102">SYNOPSIS</span></span>
<span data-ttu-id="a68b2-103">Получает конечную точку для профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="a68b2-103">Gets an endpoint for a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a68b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a68b2-104">SYNTAX</span></span>

### <span data-ttu-id="a68b2-105">»</span><span class="sxs-lookup"><span data-stu-id="a68b2-105">Fields</span></span>
```
Get-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a68b2-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="a68b2-106">Object</span></span>
```
Get-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a68b2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a68b2-107">DESCRIPTION</span></span>
<span data-ttu-id="a68b2-108">Командлет **Get-AzureRmTrafficManagerEndpoint** получает конечную точку для профиля диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="a68b2-108">The **Get-AzureRmTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="a68b2-109">Вы можете локально изменить этот объект, а затем применить изменения к профилю с помощью командлета Set-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a68b2-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="a68b2-110">Укажите конечную точку, используя параметры *Name* и *Type* .</span><span class="sxs-lookup"><span data-stu-id="a68b2-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="a68b2-111">Профиль диспетчера трафика можно задать с помощью параметров *имя_профиля* и *ResourceGroupName* , либо указав объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="a68b2-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="a68b2-112">Кроме того, вы можете передать это значение с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="a68b2-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="a68b2-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a68b2-113">EXAMPLES</span></span>

### <span data-ttu-id="a68b2-114">Пример 1: получение конечной точки</span><span class="sxs-lookup"><span data-stu-id="a68b2-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="a68b2-115">Эта команда получает конечную точку Azure с именем Contoso из профиля с именем ContosoProfile в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a68b2-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="a68b2-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a68b2-116">PARAMETERS</span></span>

### <span data-ttu-id="a68b2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a68b2-117">-DefaultProfile</span></span>
<span data-ttu-id="a68b2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a68b2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a68b2-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a68b2-119">-Name</span></span>
<span data-ttu-id="a68b2-120">Указывает имя конечной точки диспетчера трафика, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a68b2-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a68b2-121">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="a68b2-121">-ProfileName</span></span>
<span data-ttu-id="a68b2-122">Указывает имя конечной точки диспетчера трафика, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a68b2-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a68b2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a68b2-123">-ResourceGroupName</span></span>
<span data-ttu-id="a68b2-124">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a68b2-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a68b2-125">Этот командлет получает конечную точку диспетчера трафика в группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a68b2-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a68b2-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a68b2-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="a68b2-127">Указывает конечную точку диспетчера трафика, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a68b2-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

```yaml
Type: TrafficManagerEndpoint
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a68b2-128">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="a68b2-128">-Type</span></span>
<span data-ttu-id="a68b2-129">Указывает тип конечной точки, которую добавляет этот командлет к профилю диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="a68b2-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="a68b2-130">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="a68b2-130">Valid values are:</span></span> 

- <span data-ttu-id="a68b2-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="a68b2-131">AzureEndpoints</span></span>
- <span data-ttu-id="a68b2-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="a68b2-132">ExternalEndpoints</span></span>
- <span data-ttu-id="a68b2-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="a68b2-133">NestedEndpoints</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a68b2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a68b2-134">CommonParameters</span></span>
<span data-ttu-id="a68b2-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a68b2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a68b2-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a68b2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a68b2-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a68b2-137">INPUTS</span></span>

### <span data-ttu-id="a68b2-138">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a68b2-138">TrafficManagerEndpoint</span></span>
<span data-ttu-id="a68b2-139">Параметр "TrafficManagerEndpoint" принимает значение типа "TrafficManagerEndpoint" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a68b2-139">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="a68b2-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a68b2-140">OUTPUTS</span></span>

### <span data-ttu-id="a68b2-141">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a68b2-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="a68b2-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="a68b2-142">NOTES</span></span>

## <span data-ttu-id="a68b2-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a68b2-143">RELATED LINKS</span></span>

[<span data-ttu-id="a68b2-144">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a68b2-144">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="a68b2-145">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a68b2-145">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="a68b2-146">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a68b2-146">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="a68b2-147">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a68b2-147">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="a68b2-148">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a68b2-148">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)

