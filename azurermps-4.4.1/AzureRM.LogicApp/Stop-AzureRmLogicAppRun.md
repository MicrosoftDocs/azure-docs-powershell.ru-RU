---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 3308F901-4C9F-424D-8BEB-877A6038B246
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Stop-AzureRmLogicAppRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Stop-AzureRmLogicAppRun.md
ms.openlocfilehash: c6c2c356557d2d9d40a4012a7deee5aec0e73aa4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570371"
---
# <span data-ttu-id="d0091-101">Stop-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="d0091-101">Stop-AzureRmLogicAppRun</span></span>

## <span data-ttu-id="d0091-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d0091-102">SYNOPSIS</span></span>
<span data-ttu-id="d0091-103">Отменяет выполнение логики приложения.</span><span class="sxs-lookup"><span data-stu-id="d0091-103">Cancels a run of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0091-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d0091-104">SYNTAX</span></span>

```
Stop-AzureRmLogicAppRun -ResourceGroupName <String> -Name <String> -RunName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0091-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0091-105">DESCRIPTION</span></span>
<span data-ttu-id="d0091-106">Командлет **Stop-AzureRmLogicAppRun** отменяет выполнение логического приложения.</span><span class="sxs-lookup"><span data-stu-id="d0091-106">The **Stop-AzureRmLogicAppRun** cmdlet cancels a run of a logic app.</span></span>
<span data-ttu-id="d0091-107">Укажите логическое приложение, группу ресурсов и запуск.</span><span class="sxs-lookup"><span data-stu-id="d0091-107">Specify the logic app, resource group, and run.</span></span>

<span data-ttu-id="d0091-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="d0091-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d0091-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="d0091-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d0091-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="d0091-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d0091-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="d0091-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d0091-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d0091-112">EXAMPLES</span></span>

### <span data-ttu-id="d0091-113">Пример 1: Отмена выполнения приложения логики</span><span class="sxs-lookup"><span data-stu-id="d0091-113">Example 1: Cancel a run of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -RunName "08587489104702792076"
```

<span data-ttu-id="d0091-114">Эта команда отменяет выполнение логического приложения с именем LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="d0091-114">This command cancels a run of the logic app named LogicApp03.</span></span>

## <span data-ttu-id="d0091-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d0091-115">PARAMETERS</span></span>

### <span data-ttu-id="d0091-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d0091-116">-Force</span></span>
<span data-ttu-id="d0091-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="d0091-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d0091-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d0091-118">-Name</span></span>
<span data-ttu-id="d0091-119">Указывает имя логического приложения, для которого этот командлет отменяет выполнение.</span><span class="sxs-lookup"><span data-stu-id="d0091-119">Specifies the name of a logic app for which this cmdlet cancels a run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0091-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0091-120">-ResourceGroupName</span></span>
<span data-ttu-id="d0091-121">Указывает имя группы ресурсов, в которой этот командлет отменяет выполнение.</span><span class="sxs-lookup"><span data-stu-id="d0091-121">Specifies the name for a resource group in which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="d0091-122">-RunName</span><span class="sxs-lookup"><span data-stu-id="d0091-122">-RunName</span></span>
<span data-ttu-id="d0091-123">Указывает имя приложения логики, которое отменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d0091-123">Specifies the name of a logic app run that this cmdlet cancels.</span></span>

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

### <span data-ttu-id="d0091-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0091-124">-Confirm</span></span>
<span data-ttu-id="d0091-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d0091-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0091-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0091-126">-WhatIf</span></span>
<span data-ttu-id="d0091-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d0091-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0091-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d0091-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0091-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0091-129">-DefaultProfile</span></span>
<span data-ttu-id="d0091-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d0091-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0091-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0091-131">CommonParameters</span></span>
<span data-ttu-id="d0091-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d0091-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0091-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0091-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0091-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d0091-134">INPUTS</span></span>

## <span data-ttu-id="d0091-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0091-135">OUTPUTS</span></span>

### <span data-ttu-id="d0091-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="d0091-136">System.Object</span></span>

## <span data-ttu-id="d0091-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="d0091-137">NOTES</span></span>

## <span data-ttu-id="d0091-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0091-138">RELATED LINKS</span></span>

[<span data-ttu-id="d0091-139">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="d0091-139">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)

