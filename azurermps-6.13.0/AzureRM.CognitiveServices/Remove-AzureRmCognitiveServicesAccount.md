---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/remove-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 2c8496af209cc72ebb6cb9a2ed40ae6033ce7268
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568214"
---
# <span data-ttu-id="db4bd-101">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="db4bd-101">Remove-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="db4bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db4bd-102">SYNOPSIS</span></span>
<span data-ttu-id="db4bd-103">Удаление учетной записи службы для восприятия.</span><span class="sxs-lookup"><span data-stu-id="db4bd-103">Deletes a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db4bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db4bd-104">SYNTAX</span></span>

```
Remove-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db4bd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db4bd-105">DESCRIPTION</span></span>
<span data-ttu-id="db4bd-106">Командлет **Remove-AzureRmCognitiveServicesAccount** удаляет указанную учетную запись службы.</span><span class="sxs-lookup"><span data-stu-id="db4bd-106">The **Remove-AzureRmCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="db4bd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db4bd-107">EXAMPLES</span></span>

### <span data-ttu-id="db4bd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="db4bd-108">Example 1</span></span>
<span data-ttu-id="db4bd-109">Эта команда ничего не возвращает.</span><span class="sxs-lookup"><span data-stu-id="db4bd-109">This command doesn't return anything.</span></span>

```powershell
PS C:\> Remove-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## <span data-ttu-id="db4bd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db4bd-110">PARAMETERS</span></span>

### <span data-ttu-id="db4bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db4bd-111">-DefaultProfile</span></span>
<span data-ttu-id="db4bd-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="db4bd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db4bd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="db4bd-113">-Force</span></span>
<span data-ttu-id="db4bd-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="db4bd-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="db4bd-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="db4bd-115">-Name</span></span>
<span data-ttu-id="db4bd-116">Указывает имя учетной записи, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="db4bd-116">Specifies the name of the account to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db4bd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db4bd-117">-ResourceGroupName</span></span>
<span data-ttu-id="db4bd-118">Указывает имя группы ресурсов, которой назначена учетная запись службы.</span><span class="sxs-lookup"><span data-stu-id="db4bd-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db4bd-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db4bd-119">-Confirm</span></span>
<span data-ttu-id="db4bd-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="db4bd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db4bd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db4bd-121">-WhatIf</span></span>
<span data-ttu-id="db4bd-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="db4bd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db4bd-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="db4bd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db4bd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db4bd-124">CommonParameters</span></span>
<span data-ttu-id="db4bd-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db4bd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db4bd-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db4bd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db4bd-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db4bd-127">INPUTS</span></span>

### <span data-ttu-id="db4bd-128">System. String</span><span class="sxs-lookup"><span data-stu-id="db4bd-128">System.String</span></span>

## <span data-ttu-id="db4bd-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db4bd-129">OUTPUTS</span></span>

### <span data-ttu-id="db4bd-130">System. void</span><span class="sxs-lookup"><span data-stu-id="db4bd-130">System.Void</span></span>

## <span data-ttu-id="db4bd-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="db4bd-131">NOTES</span></span>

## <span data-ttu-id="db4bd-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db4bd-132">RELATED LINKS</span></span>

[<span data-ttu-id="db4bd-133">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="db4bd-133">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="db4bd-134">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="db4bd-134">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="db4bd-135">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="db4bd-135">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)

