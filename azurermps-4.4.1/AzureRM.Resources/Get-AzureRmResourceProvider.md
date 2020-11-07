---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
ms.openlocfilehash: a7c30ee436f35bee72e786c1d219e114236248da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567078"
---
# <span data-ttu-id="9bb90-101">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="9bb90-101">Get-AzureRmResourceProvider</span></span>

## <span data-ttu-id="9bb90-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9bb90-102">SYNOPSIS</span></span>
<span data-ttu-id="9bb90-103">Возвращает поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9bb90-103">Gets a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bb90-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9bb90-104">SYNTAX</span></span>

### <span data-ttu-id="9bb90-105">ListAvailable (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9bb90-105">ListAvailable (Default)</span></span>
```
Get-AzureRmResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bb90-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="9bb90-106">IndividualProvider</span></span>
```
Get-AzureRmResourceProvider -ProviderNamespace <String> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bb90-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bb90-107">DESCRIPTION</span></span>
<span data-ttu-id="9bb90-108">Командлет **Get-AzureRmResourceProvider** Получает поставщик ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="9bb90-108">The **Get-AzureRmResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="9bb90-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9bb90-109">EXAMPLES</span></span>

## <span data-ttu-id="9bb90-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9bb90-110">PARAMETERS</span></span>

### <span data-ttu-id="9bb90-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9bb90-111">-ApiVersion</span></span>
<span data-ttu-id="9bb90-112">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9bb90-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="9bb90-113">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9bb90-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="9bb90-114">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="9bb90-114">-ListAvailable</span></span>
<span data-ttu-id="9bb90-115">Указывает на то, что эта операция получает все доступные поставщики ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9bb90-115">Indicates that this operation gets all available resource providers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bb90-116">-Location</span><span class="sxs-lookup"><span data-stu-id="9bb90-116">-Location</span></span>
<span data-ttu-id="9bb90-117">Указывает расположение поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9bb90-117">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="9bb90-118">-Pre</span><span class="sxs-lookup"><span data-stu-id="9bb90-118">-Pre</span></span>
<span data-ttu-id="9bb90-119">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="9bb90-119">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9bb90-120">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="9bb90-120">-ProviderNamespace</span></span>
<span data-ttu-id="9bb90-121">Задает пространство имен поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9bb90-121">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: IndividualProvider
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bb90-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bb90-122">-DefaultProfile</span></span>
<span data-ttu-id="9bb90-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9bb90-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bb90-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bb90-124">CommonParameters</span></span>
<span data-ttu-id="9bb90-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9bb90-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bb90-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bb90-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bb90-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9bb90-127">INPUTS</span></span>

## <span data-ttu-id="9bb90-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bb90-128">OUTPUTS</span></span>

### <span data-ttu-id="9bb90-129">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="9bb90-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="9bb90-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="9bb90-130">NOTES</span></span>

## <span data-ttu-id="9bb90-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9bb90-131">RELATED LINKS</span></span>

[<span data-ttu-id="9bb90-132">Регистрация — AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="9bb90-132">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

[<span data-ttu-id="9bb90-133">Отмена регистрации — AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="9bb90-133">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)

