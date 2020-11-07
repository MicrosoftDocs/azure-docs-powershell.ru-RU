---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: fcf88fcb9b54adec01b8a04b50f557b6a74e7ca8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556983"
---
# <span data-ttu-id="6e387-101">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6e387-101">Get-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="6e387-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6e387-102">SYNOPSIS</span></span>
<span data-ttu-id="6e387-103">Получает указанную политику области.</span><span class="sxs-lookup"><span data-stu-id="6e387-103">Gets the specified scope policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e387-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6e387-104">SYNTAX</span></span>

### <span data-ttu-id="6e387-105">GetTenantLevel (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6e387-105">GetTenantLevel (Default)</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e387-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="6e387-106">GetProductLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e387-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="6e387-107">GetApiLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e387-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="6e387-108">GetOperationLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e387-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e387-109">DESCRIPTION</span></span>
<span data-ttu-id="6e387-110">Командлет **Get-AzureRmApiManagementPolicy** получает указанную политику области.</span><span class="sxs-lookup"><span data-stu-id="6e387-110">The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="6e387-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6e387-111">EXAMPLES</span></span>

### <span data-ttu-id="6e387-112">Пример 1: получение политики уровня клиента</span><span class="sxs-lookup"><span data-stu-id="6e387-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="6e387-113">Эта команда получает политику уровня клиента и сохраняет ее в файле с именем tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="6e387-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="6e387-114">Пример 2: получение политики для области продукта</span><span class="sxs-lookup"><span data-stu-id="6e387-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="6e387-115">Эта команда получает политику области продукта</span><span class="sxs-lookup"><span data-stu-id="6e387-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="6e387-116">Пример 3: получение политики области API</span><span class="sxs-lookup"><span data-stu-id="6e387-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="6e387-117">Эта команда получает политику области API.</span><span class="sxs-lookup"><span data-stu-id="6e387-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="6e387-118">Пример 4: получение политики области действия для операции</span><span class="sxs-lookup"><span data-stu-id="6e387-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="6e387-119">Эта команда получает политику области действия.</span><span class="sxs-lookup"><span data-stu-id="6e387-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="6e387-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6e387-120">PARAMETERS</span></span>

### <span data-ttu-id="6e387-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6e387-121">-ApiId</span></span>
<span data-ttu-id="6e387-122">Указывает идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="6e387-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="6e387-123">Если указать этот параметр, командлет возвращает политику области API.</span><span class="sxs-lookup"><span data-stu-id="6e387-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e387-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="6e387-124">-ApiRevision</span></span>
<span data-ttu-id="6e387-125">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="6e387-125">Identifier of API Revision.</span></span> <span data-ttu-id="6e387-126">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6e387-126">This parameter is optional.</span></span> <span data-ttu-id="6e387-127">Если не указано, политика будет получена из текущей активной версии API.</span><span class="sxs-lookup"><span data-stu-id="6e387-127">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e387-128">-Context</span><span class="sxs-lookup"><span data-stu-id="6e387-128">-Context</span></span>
<span data-ttu-id="6e387-129">Указывает экземпляр **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="6e387-129">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="6e387-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e387-130">-DefaultProfile</span></span>
<span data-ttu-id="6e387-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6e387-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e387-132">-Force</span><span class="sxs-lookup"><span data-stu-id="6e387-132">-Force</span></span>
<span data-ttu-id="6e387-133">ps_force</span><span class="sxs-lookup"><span data-stu-id="6e387-133">ps_force</span></span>

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

### <span data-ttu-id="6e387-134">-Format</span><span class="sxs-lookup"><span data-stu-id="6e387-134">-Format</span></span>
<span data-ttu-id="6e387-135">Задает формат политики управления API.</span><span class="sxs-lookup"><span data-stu-id="6e387-135">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="6e387-136">Значением по умолчанию для этого параметра является "application/vnd. MS-Azure-apim. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="6e387-136">The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="6e387-137">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="6e387-137">-OperationId</span></span>
<span data-ttu-id="6e387-138">Указывает идентификатор существующей операции API.</span><span class="sxs-lookup"><span data-stu-id="6e387-138">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="6e387-139">Если указать этот параметр в *ApiId* , командлет возвращает политику области действия.</span><span class="sxs-lookup"><span data-stu-id="6e387-139">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e387-140">-ProductId</span><span class="sxs-lookup"><span data-stu-id="6e387-140">-ProductId</span></span>
<span data-ttu-id="6e387-141">Указывает идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="6e387-141">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="6e387-142">Если указать этот параметр, командлет возвращает политику области продукта.</span><span class="sxs-lookup"><span data-stu-id="6e387-142">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e387-143">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="6e387-143">-SaveAs</span></span>
<span data-ttu-id="6e387-144">Задает путь к файлу, в который нужно сохранить результат.</span><span class="sxs-lookup"><span data-stu-id="6e387-144">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="6e387-145">Если этот параметр не указан, результат будет конвейерная, как Sting.</span><span class="sxs-lookup"><span data-stu-id="6e387-145">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="6e387-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e387-146">-Confirm</span></span>
<span data-ttu-id="6e387-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6e387-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e387-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e387-148">-WhatIf</span></span>
<span data-ttu-id="6e387-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6e387-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e387-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6e387-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e387-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e387-151">CommonParameters</span></span>
<span data-ttu-id="6e387-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6e387-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e387-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e387-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e387-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6e387-154">INPUTS</span></span>

### <span data-ttu-id="6e387-155">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6e387-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6e387-156">System. String</span><span class="sxs-lookup"><span data-stu-id="6e387-156">System.String</span></span>

### <span data-ttu-id="6e387-157">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6e387-157">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6e387-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e387-158">OUTPUTS</span></span>

### <span data-ttu-id="6e387-159">System. String</span><span class="sxs-lookup"><span data-stu-id="6e387-159">System.String</span></span>

## <span data-ttu-id="6e387-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="6e387-160">NOTES</span></span>

## <span data-ttu-id="6e387-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e387-161">RELATED LINKS</span></span>

[<span data-ttu-id="6e387-162">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6e387-162">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="6e387-163">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6e387-163">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)

