---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
ms.openlocfilehash: fbbac617687712208730393b978a3df5b404aeb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565133"
---
# <span data-ttu-id="de6cc-101">Get-AzureRmServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="de6cc-101">Get-AzureRmServiceBusOperation</span></span>

## <span data-ttu-id="de6cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="de6cc-102">SYNOPSIS</span></span>
<span data-ttu-id="de6cc-103">Список поддерживаемых операций ServiceBus</span><span class="sxs-lookup"><span data-stu-id="de6cc-103">List supported ServiceBus Operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de6cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="de6cc-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de6cc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de6cc-105">DESCRIPTION</span></span>
<span data-ttu-id="de6cc-106">Командлет **Get-AzureRmServiceBusOperation** содержит список поддерживаемых операций servicebus.</span><span class="sxs-lookup"><span data-stu-id="de6cc-106">The **Get-AzureRmServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="de6cc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="de6cc-107">EXAMPLES</span></span>

### <span data-ttu-id="de6cc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="de6cc-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusOperation
```

<span data-ttu-id="de6cc-109">Список поддерживаемых операций ServiceBus</span><span class="sxs-lookup"><span data-stu-id="de6cc-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="de6cc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="de6cc-110">PARAMETERS</span></span>

### <span data-ttu-id="de6cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de6cc-111">-DefaultProfile</span></span>
<span data-ttu-id="de6cc-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="de6cc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de6cc-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de6cc-113">CommonParameters</span></span>
<span data-ttu-id="de6cc-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="de6cc-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de6cc-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de6cc-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de6cc-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="de6cc-116">INPUTS</span></span>

### <span data-ttu-id="de6cc-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="de6cc-117">None</span></span>

### <span data-ttu-id="de6cc-118">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. OperationAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.4.2.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="de6cc-118">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.OperationAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.4.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="de6cc-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="de6cc-119">OUTPUTS</span></span>

### <span data-ttu-id="de6cc-120">System. Collections. Generic. List ' 1 [Microsoft. Azure. OperationAttributes]</span><span class="sxs-lookup"><span data-stu-id="de6cc-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ServiceBus.Models.OperationAttributes]</span></span>

## <span data-ttu-id="de6cc-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="de6cc-121">NOTES</span></span>

## <span data-ttu-id="de6cc-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de6cc-122">RELATED LINKS</span></span>
