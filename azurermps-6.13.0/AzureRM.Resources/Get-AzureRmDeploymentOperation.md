---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmDeploymentOperation.md
ms.openlocfilehash: 16d52fcc41f642b942b521872b629caff4b4d880
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564059"
---
# <span data-ttu-id="395a3-101">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="395a3-101">Get-AzureRmDeploymentOperation</span></span>

## <span data-ttu-id="395a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="395a3-102">SYNOPSIS</span></span>
<span data-ttu-id="395a3-103">Операция получения развертывания</span><span class="sxs-lookup"><span data-stu-id="395a3-103">Get deployment operation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="395a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="395a3-104">SYNTAX</span></span>

### <span data-ttu-id="395a3-105">GetByDeploymentName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="395a3-105">GetByDeploymentName (Default)</span></span>
```
Get-AzureRmDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="395a3-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="395a3-106">GetByDeploymentObject</span></span>
```
Get-AzureRmDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="395a3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="395a3-107">DESCRIPTION</span></span>
<span data-ttu-id="395a3-108">Командлет **Get-AzureRmDeploymentOperation** перечисляет все операции, которые были частью развертывания, чтобы помочь вам найти и получить дополнительные сведения об операциях, которые не удалось выполнить для определенного развертывания.</span><span class="sxs-lookup"><span data-stu-id="395a3-108">The **Get-AzureRmDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="395a3-109">Он также может Показать ответ и содержимое запроса для каждой операции развертывания.</span><span class="sxs-lookup"><span data-stu-id="395a3-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="395a3-110">Это та же информация, которая указана в разделе сведения о развертывании на портале.</span><span class="sxs-lookup"><span data-stu-id="395a3-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="395a3-111">Чтобы получить содержимое запроса и ответа, включите параметр при отправке развертывания с помощью **New-AzureRmDeployment**.</span><span class="sxs-lookup"><span data-stu-id="395a3-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzureRmDeployment**.</span></span>
<span data-ttu-id="395a3-112">Она может потенциально регистрировать и представлять секреты, например пароли, используемые в свойстве ресурса или операциях **listKeys** , которые возвращаются при извлечении операций развертывания.</span><span class="sxs-lookup"><span data-stu-id="395a3-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="395a3-113">Дополнительные сведения об этом параметре и инструкции по его включению можно найти в разделе New-AzureRmDeployment и Отладка развертывания шаблонов ARM</span><span class="sxs-lookup"><span data-stu-id="395a3-113">For more on this setting and how to enable it, see New-AzureRmDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="395a3-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="395a3-114">EXAMPLES</span></span>

### <span data-ttu-id="395a3-115">Получение операций развертывания с заданным именем развертывания</span><span class="sxs-lookup"><span data-stu-id="395a3-115">Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzureRmDeploymentOperation -DeploymentName test
```

<span data-ttu-id="395a3-116">Возвращает операцию развертывания с именем Test в текущей области подписки.</span><span class="sxs-lookup"><span data-stu-id="395a3-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="395a3-117">Получение развертывания и получение его операций развертывания</span><span class="sxs-lookup"><span data-stu-id="395a3-117">Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "test" | Get-AzureRmDeploymentOperation
```

<span data-ttu-id="395a3-118">Эта команда возвращает "тест" в текущей области подписки и получение ее операций развертывания.</span><span class="sxs-lookup"><span data-stu-id="395a3-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="395a3-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="395a3-119">PARAMETERS</span></span>

### <span data-ttu-id="395a3-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="395a3-120">-ApiVersion</span></span>
<span data-ttu-id="395a3-121">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="395a3-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="395a3-122">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="395a3-122">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="395a3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="395a3-123">-DefaultProfile</span></span>
<span data-ttu-id="395a3-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="395a3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="395a3-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="395a3-125">-DeploymentName</span></span>
<span data-ttu-id="395a3-126">Имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="395a3-126">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395a3-127">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="395a3-127">-DeploymentObject</span></span>
<span data-ttu-id="395a3-128">Объект развертывания.</span><span class="sxs-lookup"><span data-stu-id="395a3-128">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="395a3-129">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="395a3-129">-OperationId</span></span>
<span data-ttu-id="395a3-130">Идентификатор операции развертывания.</span><span class="sxs-lookup"><span data-stu-id="395a3-130">The deployment operation Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395a3-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="395a3-131">-Pre</span></span>
<span data-ttu-id="395a3-132">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="395a3-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="395a3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="395a3-133">CommonParameters</span></span>
<span data-ttu-id="395a3-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="395a3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="395a3-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="395a3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="395a3-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="395a3-136">INPUTS</span></span>

### <span data-ttu-id="395a3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="395a3-137">System.String</span></span>
<span data-ttu-id="395a3-138">System. Nullable "1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="395a3-138">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="395a3-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="395a3-139">OUTPUTS</span></span>

### <span data-ttu-id="395a3-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="395a3-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="395a3-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="395a3-141">NOTES</span></span>

## <span data-ttu-id="395a3-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="395a3-142">RELATED LINKS</span></span>