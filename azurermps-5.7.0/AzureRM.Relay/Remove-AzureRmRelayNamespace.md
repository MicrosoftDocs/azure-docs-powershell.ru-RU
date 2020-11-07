---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
ms.openlocfilehash: 52abd413f94d0c190a6f03b3707efdb544a4b72a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561576"
---
# <span data-ttu-id="b7c8e-101">Remove-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="b7c8e-101">Remove-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="b7c8e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b7c8e-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c8e-103">Удаляет пространство имен из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b7c8e-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7c8e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b7c8e-104">SYNTAX</span></span>

```
Remove-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7c8e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7c8e-105">DESCRIPTION</span></span>
<span data-ttu-id="b7c8e-106">Командлет **Remove-AzureRmRelayNamespace** удаляет пространство имен из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b7c8e-106">The **Remove-AzureRmRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="b7c8e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b7c8e-107">EXAMPLES</span></span>

### <span data-ttu-id="b7c8e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b7c8e-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="b7c8e-109">Удаляет пространство имен ретрансляции `TestNameSpace-Relay1` из указанной группы ресурсов `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="b7c8e-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="b7c8e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b7c8e-110">PARAMETERS</span></span>

### <span data-ttu-id="b7c8e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7c8e-111">-DefaultProfile</span></span>
<span data-ttu-id="b7c8e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7c8e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7c8e-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b7c8e-113">-Name</span></span>
<span data-ttu-id="b7c8e-114">Имя пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="b7c8e-114">Relay Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c8e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7c8e-115">-ResourceGroupName</span></span>
<span data-ttu-id="b7c8e-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b7c8e-116">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c8e-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7c8e-117">-Confirm</span></span>
<span data-ttu-id="b7c8e-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b7c8e-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c8e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7c8e-119">-WhatIf</span></span>
<span data-ttu-id="b7c8e-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b7c8e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7c8e-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b7c8e-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c8e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c8e-122">CommonParameters</span></span>
<span data-ttu-id="b7c8e-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b7c8e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7c8e-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7c8e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c8e-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b7c8e-125">INPUTS</span></span>

### <span data-ttu-id="b7c8e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7c8e-126">-ResourceGroupName</span></span>
 <span data-ttu-id="b7c8e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b7c8e-127">System.String</span></span>

### <span data-ttu-id="b7c8e-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b7c8e-128">-Name</span></span>
 <span data-ttu-id="b7c8e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b7c8e-129">System.String</span></span>

## <span data-ttu-id="b7c8e-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7c8e-130">OUTPUTS</span></span>

### <span data-ttu-id="b7c8e-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="b7c8e-131">System.Object</span></span>

## <span data-ttu-id="b7c8e-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="b7c8e-132">NOTES</span></span>

## <span data-ttu-id="b7c8e-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7c8e-133">RELATED LINKS</span></span>
