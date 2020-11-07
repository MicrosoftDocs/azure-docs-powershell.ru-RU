---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeploymentOperation.md
ms.openlocfilehash: 557aa312200a2e5c49e33f8a176079ee4b27b629
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561551"
---
# <span data-ttu-id="4554b-101">Get-AzureRmResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="4554b-101">Get-AzureRmResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="4554b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4554b-102">SYNOPSIS</span></span>
<span data-ttu-id="4554b-103">Получает операцию развертывания группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4554b-103">Gets the resource group deployment operation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4554b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4554b-104">SYNTAX</span></span>

```
Get-AzureRmResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4554b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4554b-105">DESCRIPTION</span></span>
<span data-ttu-id="4554b-106">Командлет **Get-AzureRmResourceGroupDeploymentOperation** перечисляет все операции, которые были частью развертывания, чтобы помочь вам найти и получить дополнительные сведения об операциях, которые не удалось выполнить для определенного развертывания.</span><span class="sxs-lookup"><span data-stu-id="4554b-106">The **Get-AzureRmResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="4554b-107">Он также может Показать ответ и содержимое запроса для каждой операции развертывания.</span><span class="sxs-lookup"><span data-stu-id="4554b-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="4554b-108">Это та же информация, которая указана в разделе сведения о развертывании на портале.</span><span class="sxs-lookup"><span data-stu-id="4554b-108">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="4554b-109">Чтобы получить содержимое запроса и ответа, включите параметр при отправке развертывания с помощью **New-AzureRmResourceGroupDeployment**.</span><span class="sxs-lookup"><span data-stu-id="4554b-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzureRmResourceGroupDeployment**.</span></span>
<span data-ttu-id="4554b-110">Она может потенциально регистрировать и представлять секреты, например пароли, используемые в свойстве ресурса или операциях **listKeys** , которые возвращаются при извлечении операций развертывания.</span><span class="sxs-lookup"><span data-stu-id="4554b-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="4554b-111">Дополнительные сведения об этом параметре и инструкции по его включению можно найти в разделе New-AzureRmResourceGroupDeployment и Отладка развертывания шаблонов ARM</span><span class="sxs-lookup"><span data-stu-id="4554b-111">For more on this setting and how to enable it, see New-AzureRmResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="4554b-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4554b-112">EXAMPLES</span></span>

### <span data-ttu-id="4554b-113">Get1</span><span class="sxs-lookup"><span data-stu-id="4554b-113">Get1</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="4554b-114">Возвращает операцию развертывания с именем "тест" в группе ресурсов "тест"</span><span class="sxs-lookup"><span data-stu-id="4554b-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="4554b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4554b-115">PARAMETERS</span></span>

### <span data-ttu-id="4554b-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4554b-116">-ApiVersion</span></span>
<span data-ttu-id="4554b-117">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4554b-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="4554b-118">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="4554b-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="4554b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4554b-119">-DefaultProfile</span></span>
<span data-ttu-id="4554b-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4554b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4554b-121">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="4554b-121">-DeploymentName</span></span>
<span data-ttu-id="4554b-122">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="4554b-122">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4554b-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4554b-123">-InformationAction</span></span>
<span data-ttu-id="4554b-124">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="4554b-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4554b-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4554b-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4554b-126">Продолжал</span><span class="sxs-lookup"><span data-stu-id="4554b-126">Continue</span></span>
- <span data-ttu-id="4554b-127">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="4554b-127">Ignore</span></span>
- <span data-ttu-id="4554b-128">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="4554b-128">Inquire</span></span>
- <span data-ttu-id="4554b-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4554b-129">SilentlyContinue</span></span>
- <span data-ttu-id="4554b-130">Остановить</span><span class="sxs-lookup"><span data-stu-id="4554b-130">Stop</span></span>
- <span data-ttu-id="4554b-131">Рвать</span><span class="sxs-lookup"><span data-stu-id="4554b-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4554b-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4554b-132">-InformationVariable</span></span>
<span data-ttu-id="4554b-133">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="4554b-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4554b-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="4554b-134">-Pre</span></span>
<span data-ttu-id="4554b-135">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="4554b-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4554b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4554b-136">-ResourceGroupName</span></span>
<span data-ttu-id="4554b-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4554b-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4554b-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4554b-138">-SubscriptionId</span></span>
<span data-ttu-id="4554b-139">Подписку на использование.</span><span class="sxs-lookup"><span data-stu-id="4554b-139">The subscription to use.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4554b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4554b-140">CommonParameters</span></span>
<span data-ttu-id="4554b-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4554b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4554b-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4554b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4554b-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4554b-143">INPUTS</span></span>

### <span data-ttu-id="4554b-144">GUID</span><span class="sxs-lookup"><span data-stu-id="4554b-144">Guid</span></span>
<span data-ttu-id="4554b-145">Параметр "SubscriptionId" принимает значение типа GUID из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4554b-145">Parameter 'SubscriptionId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="4554b-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4554b-146">OUTPUTS</span></span>

### <span data-ttu-id="4554b-147">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4554b-147">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4554b-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="4554b-148">NOTES</span></span>

## <span data-ttu-id="4554b-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4554b-149">RELATED LINKS</span></span>