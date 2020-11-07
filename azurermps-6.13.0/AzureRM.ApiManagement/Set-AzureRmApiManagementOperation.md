---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
ms.openlocfilehash: e50e912c55a09ef5d036bee668bc45f58fc42c19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558627"
---
# <span data-ttu-id="e5876-101">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e5876-101">Set-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="e5876-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5876-102">SYNOPSIS</span></span>
<span data-ttu-id="e5876-103">Задает сведения об операции API.</span><span class="sxs-lookup"><span data-stu-id="e5876-103">Sets API operation details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5876-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5876-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5876-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5876-105">DESCRIPTION</span></span>
<span data-ttu-id="e5876-106">Командлет **Set-AzureRmApiManagementOperation** задает сведения об операциях API.</span><span class="sxs-lookup"><span data-stu-id="e5876-106">The **Set-AzureRmApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="e5876-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5876-107">EXAMPLES</span></span>

### <span data-ttu-id="e5876-108">Пример 1: Настройка сведений об операции</span><span class="sxs-lookup"><span data-stu-id="e5876-108">Example 1: Set the operation details</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="e5876-109">Эта команда задает сведения об операциях для управления API.</span><span class="sxs-lookup"><span data-stu-id="e5876-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="e5876-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5876-110">PARAMETERS</span></span>

### <span data-ttu-id="e5876-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e5876-111">-ApiId</span></span>
<span data-ttu-id="e5876-112">Указывает идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="e5876-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="e5876-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="e5876-113">-ApiRevision</span></span>
<span data-ttu-id="e5876-114">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="e5876-114">Identifier of API Revision.</span></span> <span data-ttu-id="e5876-115">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e5876-115">This parameter is optional.</span></span> <span data-ttu-id="e5876-116">Если этот элемент не указан, операция будет обновлена в текущей активной редакции API.</span><span class="sxs-lookup"><span data-stu-id="e5876-116">If not specified, the operation will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="e5876-117">-Context</span><span class="sxs-lookup"><span data-stu-id="e5876-117">-Context</span></span>
<span data-ttu-id="e5876-118">Указывает экземпляр **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="e5876-118">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5876-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5876-119">-DefaultProfile</span></span>
<span data-ttu-id="e5876-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5876-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5876-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="e5876-121">-Description</span></span>
<span data-ttu-id="e5876-122">Задает описание новой операции.</span><span class="sxs-lookup"><span data-stu-id="e5876-122">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="e5876-123">-Method</span><span class="sxs-lookup"><span data-stu-id="e5876-123">-Method</span></span>
<span data-ttu-id="e5876-124">Задает метод HTTP для новой операции.</span><span class="sxs-lookup"><span data-stu-id="e5876-124">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="e5876-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e5876-125">-Name</span></span>
<span data-ttu-id="e5876-126">Указывает отображаемое имя для новой операции.</span><span class="sxs-lookup"><span data-stu-id="e5876-126">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="e5876-127">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="e5876-127">-OperationId</span></span>
<span data-ttu-id="e5876-128">Указывает идентификатор существующей операции.</span><span class="sxs-lookup"><span data-stu-id="e5876-128">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="e5876-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5876-129">-PassThru</span></span>
<span data-ttu-id="e5876-130">PassThru</span><span class="sxs-lookup"><span data-stu-id="e5876-130">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5876-131">-Request</span><span class="sxs-lookup"><span data-stu-id="e5876-131">-Request</span></span>
<span data-ttu-id="e5876-132">Задает сведения о запросе операции.</span><span class="sxs-lookup"><span data-stu-id="e5876-132">Specifies the operation request details.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5876-133">-Ответы</span><span class="sxs-lookup"><span data-stu-id="e5876-133">-Responses</span></span>
<span data-ttu-id="e5876-134">Указывает массив возможных ответов операций.</span><span class="sxs-lookup"><span data-stu-id="e5876-134">Specifies an array of possible operation responses.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5876-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="e5876-135">-TemplateParameters</span></span>
<span data-ttu-id="e5876-136">Задает массив или параметры, определенные в параметре *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="e5876-136">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="e5876-137">Если значение не задано, на основе UrlTemplate будет создано значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e5876-137">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="e5876-138">С помощью этого параметра можно получить дополнительные сведения о таких параметрах, как описание, тип и другие возможные значения.</span><span class="sxs-lookup"><span data-stu-id="e5876-138">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5876-139">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="e5876-139">-UrlTemplate</span></span>
<span data-ttu-id="e5876-140">Задает шаблон URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="e5876-140">Specifies the URL template.</span></span>
<span data-ttu-id="e5876-141">Например: Customers/{CID}/заказы/{OID}/? Дата = {Date}.</span><span class="sxs-lookup"><span data-stu-id="e5876-141">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="e5876-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5876-142">CommonParameters</span></span>
<span data-ttu-id="e5876-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5876-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5876-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5876-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5876-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5876-145">INPUTS</span></span>

### <span data-ttu-id="e5876-146">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e5876-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e5876-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e5876-147">System.String</span></span>

### <span data-ttu-id="e5876-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementParameter []</span><span class="sxs-lookup"><span data-stu-id="e5876-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="e5876-149">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="e5876-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="e5876-150">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementResponse []</span><span class="sxs-lookup"><span data-stu-id="e5876-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

### <span data-ttu-id="e5876-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e5876-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e5876-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5876-152">OUTPUTS</span></span>

### <span data-ttu-id="e5876-153">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e5876-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="e5876-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5876-154">NOTES</span></span>

## <span data-ttu-id="e5876-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5876-155">RELATED LINKS</span></span>

[<span data-ttu-id="e5876-156">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e5876-156">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="e5876-157">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e5876-157">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="e5876-158">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e5876-158">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

