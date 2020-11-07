---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
ms.openlocfilehash: 92d94950bc4bc90494482b22b81cbd918c8b6938
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567065"
---
# <span data-ttu-id="c9910-101">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="c9910-101">Register-AzureRmResourceProvider</span></span>

## <span data-ttu-id="c9910-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c9910-102">SYNOPSIS</span></span>
<span data-ttu-id="c9910-103">Регистрация поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c9910-103">Registers a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9910-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c9910-104">SYNTAX</span></span>

```
Register-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9910-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9910-105">DESCRIPTION</span></span>
<span data-ttu-id="c9910-106">Командлет **Register-AzureRmResourceProvider** регистрирует поставщик ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="c9910-106">The **Register-AzureRmResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="c9910-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c9910-107">EXAMPLES</span></span>

## <span data-ttu-id="c9910-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c9910-108">PARAMETERS</span></span>

### <span data-ttu-id="c9910-109">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c9910-109">-ApiVersion</span></span>
<span data-ttu-id="c9910-110">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c9910-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="c9910-111">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c9910-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="c9910-112">-Pre</span><span class="sxs-lookup"><span data-stu-id="c9910-112">-Pre</span></span>
<span data-ttu-id="c9910-113">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="c9910-113">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c9910-114">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="c9910-114">-ProviderNamespace</span></span>
<span data-ttu-id="c9910-115">Задает пространство имен поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c9910-115">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="c9910-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9910-116">-Confirm</span></span>
<span data-ttu-id="c9910-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c9910-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9910-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9910-118">-WhatIf</span></span>
<span data-ttu-id="c9910-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c9910-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9910-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c9910-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9910-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9910-121">-DefaultProfile</span></span>
<span data-ttu-id="c9910-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c9910-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9910-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9910-123">CommonParameters</span></span>
<span data-ttu-id="c9910-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c9910-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9910-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9910-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9910-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c9910-126">INPUTS</span></span>

## <span data-ttu-id="c9910-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9910-127">OUTPUTS</span></span>

### <span data-ttu-id="c9910-128">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="c9910-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="c9910-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="c9910-129">NOTES</span></span>

## <span data-ttu-id="c9910-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9910-130">RELATED LINKS</span></span>

[<span data-ttu-id="c9910-131">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="c9910-131">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="c9910-132">Отмена регистрации — AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="c9910-132">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)

