---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 45b8bc67529556e9a9d53bd3280c6475f0e60df1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396279"
---
# <span data-ttu-id="156ae-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="156ae-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="156ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="156ae-102">SYNOPSIS</span></span>
<span data-ttu-id="156ae-103">Регистрирует поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="156ae-103">Registers a resource provider.</span></span>

## <span data-ttu-id="156ae-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="156ae-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="156ae-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="156ae-105">DESCRIPTION</span></span>
<span data-ttu-id="156ae-106">**Cmdlet Register-AzResourceProvider** регистрирует поставщика ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="156ae-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="156ae-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="156ae-107">EXAMPLES</span></span>

### <span data-ttu-id="156ae-108">Пример 1. Регистрация поставщика</span><span class="sxs-lookup"><span data-stu-id="156ae-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="156ae-109">В этом случае поставщик Microsoft.Network регистрируется для вашей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="156ae-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="156ae-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="156ae-110">PARAMETERS</span></span>

### <span data-ttu-id="156ae-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="156ae-111">-ApiVersion</span></span>
<span data-ttu-id="156ae-112">Указывает версию API, которая поддерживается поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="156ae-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="156ae-113">Вы можете указать другую версию, чем версия по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="156ae-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="156ae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="156ae-114">-DefaultProfile</span></span>
<span data-ttu-id="156ae-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="156ae-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="156ae-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="156ae-116">-Pre</span></span>
<span data-ttu-id="156ae-117">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="156ae-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="156ae-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="156ae-118">-ProviderNamespace</span></span>
<span data-ttu-id="156ae-119">Определяет пространство имен поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="156ae-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="156ae-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="156ae-120">-Confirm</span></span>
<span data-ttu-id="156ae-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="156ae-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="156ae-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="156ae-122">-WhatIf</span></span>
<span data-ttu-id="156ae-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="156ae-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="156ae-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="156ae-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="156ae-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="156ae-125">CommonParameters</span></span>
<span data-ttu-id="156ae-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="156ae-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="156ae-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="156ae-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="156ae-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="156ae-128">INPUTS</span></span>

### <span data-ttu-id="156ae-129">System.String</span><span class="sxs-lookup"><span data-stu-id="156ae-129">System.String</span></span>

## <span data-ttu-id="156ae-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="156ae-130">OUTPUTS</span></span>

### <span data-ttu-id="156ae-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="156ae-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="156ae-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="156ae-132">NOTES</span></span>

## <span data-ttu-id="156ae-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="156ae-133">RELATED LINKS</span></span>

[<span data-ttu-id="156ae-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="156ae-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="156ae-135">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="156ae-135">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)

