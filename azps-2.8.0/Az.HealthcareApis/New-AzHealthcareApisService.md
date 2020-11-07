---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: 374b443157bf6ef36f39d3ee0dba34ae59419931
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720781"
---
# <span data-ttu-id="1c009-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="1c009-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="1c009-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1c009-102">SYNOPSIS</span></span>
<span data-ttu-id="1c009-103">Создает метаданные экземпляра службы.</span><span class="sxs-lookup"><span data-stu-id="1c009-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="1c009-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1c009-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-EnableSmartProxy] [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c009-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c009-105">DESCRIPTION</span></span>
<span data-ttu-id="1c009-106">Создание или обновление метаданных экземпляра службы.</span><span class="sxs-lookup"><span data-stu-id="1c009-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="1c009-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1c009-107">EXAMPLES</span></span>

### <span data-ttu-id="1c009-108">Пример 1: создание новой службы Azure healthcareapis fhir Service с именем MyService в группе ресурсов MyResourceGroup в местоположении westus2 с пропускной способностью = 400</span><span class="sxs-lookup"><span data-stu-id="1c009-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput  400

ResourceGroupName Name Location        Kind   CosmosOfferThroughput
----------------- ----------- -------------------------------
MyResourceGroup   MyService   westus2    fhir-R4   400

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

## <span data-ttu-id="1c009-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1c009-109">PARAMETERS</span></span>

### <span data-ttu-id="1c009-110">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="1c009-110">-AccessPolicyObjectId</span></span>
<span data-ttu-id="1c009-111">Список идентификаторов объектов политики доступа.</span><span class="sxs-lookup"><span data-stu-id="1c009-111">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="1c009-112">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="1c009-112">-AllowCorsCredential</span></span>
<span data-ttu-id="1c009-113">HealthcareApis Fhir Service AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="1c009-113">HealthcareApis Fhir Service AllowCorsCredential.</span></span>

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

### <span data-ttu-id="1c009-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c009-114">-AsJob</span></span>
<span data-ttu-id="1c009-115">Запустите командлет как задание в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="1c009-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="1c009-116">-Аудитория</span><span class="sxs-lookup"><span data-stu-id="1c009-116">-Audience</span></span>
<span data-ttu-id="1c009-117">Аудитория службы HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="1c009-117">HealthcareApis Fhir Service Audience.</span></span>

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

### <span data-ttu-id="1c009-118">-Authority</span><span class="sxs-lookup"><span data-stu-id="1c009-118">-Authority</span></span>
<span data-ttu-id="1c009-119">Центр обслуживания HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="1c009-119">HealthcareApis Fhir Service Authority.</span></span>

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

### <span data-ttu-id="1c009-120">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="1c009-120">-CorsHeader</span></span>
<span data-ttu-id="1c009-121">HealthcareApis Fhir Service List (Заголовок CORS).</span><span class="sxs-lookup"><span data-stu-id="1c009-121">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="1c009-122">Укажите HTTP-заголовки, которые можно использовать во время запроса.</span><span class="sxs-lookup"><span data-stu-id="1c009-122">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="1c009-123">Используйте \* для любого заголовка.</span><span class="sxs-lookup"><span data-stu-id="1c009-123">Use \* for any header.</span></span>

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

### <span data-ttu-id="1c009-124">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="1c009-124">-CorsMaxAge</span></span>
<span data-ttu-id="1c009-125">Максимальный возраст службы HealthcareApis Fhir Service CORS.</span><span class="sxs-lookup"><span data-stu-id="1c009-125">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="1c009-126">Укажите, как долго можно кэшировать результаты запроса за считанные секунды.</span><span class="sxs-lookup"><span data-stu-id="1c009-126">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="1c009-127">Пример: 600 означает 10 минут.</span><span class="sxs-lookup"><span data-stu-id="1c009-127">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="1c009-128">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="1c009-128">-CorsMethod</span></span>
<span data-ttu-id="1c009-129">Список служб HealthcareApis Fhir (метод CORS).</span><span class="sxs-lookup"><span data-stu-id="1c009-129">HealthcareApis Fhir Service List of Cors Method.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: DELETE, GET, OPTIONS, PATCH, POST, PUT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c009-130">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="1c009-130">-CorsOrigin</span></span>
<span data-ttu-id="1c009-131">HealthcareApis Fhir список служб в источнике CORS.</span><span class="sxs-lookup"><span data-stu-id="1c009-131">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="1c009-132">Укажите URL-адреса исходных сайтов, которые могут получать доступ к этому API или используйте \* для разрешения доступа с любого сайта.</span><span class="sxs-lookup"><span data-stu-id="1c009-132">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

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

### <span data-ttu-id="1c009-133">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="1c009-133">-CosmosOfferThroughput</span></span>
<span data-ttu-id="1c009-134">HealthcareApis Fhir Service CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="1c009-134">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="1c009-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c009-135">-DefaultProfile</span></span>
<span data-ttu-id="1c009-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1c009-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c009-137">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="1c009-137">-EnableSmartProxy</span></span>
<span data-ttu-id="1c009-138">HealthcareApis Fhir Service EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="1c009-138">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

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

### <span data-ttu-id="1c009-139">-FhirVersion</span><span class="sxs-lookup"><span data-stu-id="1c009-139">-FhirVersion</span></span>
<span data-ttu-id="1c009-140">Версия Fhir.</span><span class="sxs-lookup"><span data-stu-id="1c009-140">Fhir Version.</span></span>

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

### <span data-ttu-id="1c009-141">-Видах</span><span class="sxs-lookup"><span data-stu-id="1c009-141">-Kind</span></span>
<span data-ttu-id="1c009-142">Служба HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="1c009-142">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="1c009-143">Значение по умолчанию — Fhir</span><span class="sxs-lookup"><span data-stu-id="1c009-143">The default value is Fhir</span></span>

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

### <span data-ttu-id="1c009-144">-Location</span><span class="sxs-lookup"><span data-stu-id="1c009-144">-Location</span></span>
<span data-ttu-id="1c009-145">Расположение службы HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="1c009-145">HealthcareApis Service Location.</span></span>

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

### <span data-ttu-id="1c009-146">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1c009-146">-Name</span></span>
<span data-ttu-id="1c009-147">Имя службы HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="1c009-147">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="1c009-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c009-148">-ResourceGroupName</span></span>
<span data-ttu-id="1c009-149">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c009-149">Resource Group Name.</span></span>

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

### <span data-ttu-id="1c009-150">-Тег</span><span class="sxs-lookup"><span data-stu-id="1c009-150">-Tag</span></span>
<span data-ttu-id="1c009-151">HealthcareApis Fhir учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="1c009-151">HealthcareApis Fhir Service Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c009-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c009-152">-Confirm</span></span>
<span data-ttu-id="1c009-153">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1c009-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c009-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c009-154">-WhatIf</span></span>
<span data-ttu-id="1c009-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1c009-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c009-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1c009-156">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c009-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c009-157">CommonParameters</span></span>
<span data-ttu-id="1c009-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1c009-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c009-159">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c009-159">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c009-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1c009-160">INPUTS</span></span>

### <span data-ttu-id="1c009-161">System. String</span><span class="sxs-lookup"><span data-stu-id="1c009-161">System.String</span></span>

## <span data-ttu-id="1c009-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c009-162">OUTPUTS</span></span>

### <span data-ttu-id="1c009-163">Microsoft. Azure. Commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="1c009-163">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="1c009-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="1c009-164">NOTES</span></span>

## <span data-ttu-id="1c009-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c009-165">RELATED LINKS</span></span>