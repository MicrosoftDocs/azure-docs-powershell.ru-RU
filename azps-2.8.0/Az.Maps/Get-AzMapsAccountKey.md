---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccountKey.md
ms.openlocfilehash: d4523dc240c015f4dea29b86e1285a9fce9afbc2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720389"
---
# <span data-ttu-id="d0828-101">Get-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="d0828-101">Get-AzMapsAccountKey</span></span>

## <span data-ttu-id="d0828-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d0828-102">SYNOPSIS</span></span>
<span data-ttu-id="d0828-103">Возвращает ключи API для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="d0828-103">Gets the API keys for an account.</span></span>
<span data-ttu-id="d0828-104">Эти ключи являются механизмом проверки подлинности, используемым при последующих звонках на карты Azure.</span><span class="sxs-lookup"><span data-stu-id="d0828-104">These keys are the authentication mechanism used in subsequent calls to Azure Maps.</span></span>

## <span data-ttu-id="d0828-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d0828-105">SYNTAX</span></span>

### <span data-ttu-id="d0828-106">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d0828-106">NameParameterSet (Default)</span></span>
```
Get-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0828-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0828-107">InputObjectParameterSet</span></span>
```
Get-AzMapsAccountKey [-InputObject <PSMapsAccount>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0828-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0828-108">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0828-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0828-109">DESCRIPTION</span></span>
<span data-ttu-id="d0828-110">Командлет Get-AzMapsAccountKey получает ключи API для подготовленной учетной записи Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="d0828-110">The Get-AzMapsAccountKey cmdlet gets the API keys for a provisioned Azure Maps account.</span></span>
<span data-ttu-id="d0828-111">Учетная запись карт Azure имеет два ключа API: Primary и Secondary.</span><span class="sxs-lookup"><span data-stu-id="d0828-111">An Azure Maps account has two API keys: Primary and Secondary.</span></span>
<span data-ttu-id="d0828-112">Ключи обеспечивают взаимодействие с конечной точкой учетной записи карт Azure.</span><span class="sxs-lookup"><span data-stu-id="d0828-112">The keys enable interaction with the Azure Maps account endpoint.</span></span>
<span data-ttu-id="d0828-113">Для повторного создания ключа используйте New-AzMapsAccountKey (New-AzMapsAccountKey. md).</span><span class="sxs-lookup"><span data-stu-id="d0828-113">Use New-AzMapsAccountKey (New-AzMapsAccountKey.md)to regenerate a key.</span></span>

## <span data-ttu-id="d0828-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d0828-114">EXAMPLES</span></span>

### <span data-ttu-id="d0828-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d0828-115">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="d0828-116">Возвращает ключи для учетной записи с именем Моя учетная запись в группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d0828-116">Returns the keys for the account named MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="d0828-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d0828-117">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

<span data-ttu-id="d0828-118">Возвращает ключи для указанной учетной записи Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="d0828-118">Returns the keys for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="d0828-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d0828-119">PARAMETERS</span></span>

### <span data-ttu-id="d0828-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0828-120">-DefaultProfile</span></span>
<span data-ttu-id="d0828-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d0828-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0828-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0828-122">-InputObject</span></span>
<span data-ttu-id="d0828-123">Карты сопоставляются с учетной записью Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="d0828-123">Maps Account piped from Get-AzMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0828-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d0828-124">-Name</span></span>
<span data-ttu-id="d0828-125">Имя учетной записи карты.</span><span class="sxs-lookup"><span data-stu-id="d0828-125">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0828-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0828-126">-ResourceGroupName</span></span>
<span data-ttu-id="d0828-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d0828-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0828-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0828-128">-ResourceId</span></span>
<span data-ttu-id="d0828-129">Карта ResourceId для счета.</span><span class="sxs-lookup"><span data-stu-id="d0828-129">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0828-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0828-130">CommonParameters</span></span>
<span data-ttu-id="d0828-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d0828-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0828-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0828-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0828-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d0828-133">INPUTS</span></span>

### <span data-ttu-id="d0828-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d0828-134">System.String</span></span>

### <span data-ttu-id="d0828-135">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="d0828-135">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="d0828-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0828-136">OUTPUTS</span></span>

### <span data-ttu-id="d0828-137">Microsoft. Azure. Commands. Maps. Models. PSMapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d0828-137">Microsoft.Azure.Commands.Maps.Models.PSMapsAccountKeys</span></span>

## <span data-ttu-id="d0828-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="d0828-138">NOTES</span></span>

## <span data-ttu-id="d0828-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0828-139">RELATED LINKS</span></span>