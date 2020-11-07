---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareprovidersharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
ms.openlocfilehash: 9d95eceac8f80280dcfadfbb20424078e6f85fce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721209"
---
# <span data-ttu-id="980ad-101">Get-AzDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="980ad-101">Get-AzDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="980ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="980ad-102">SYNOPSIS</span></span>
<span data-ttu-id="980ad-103">Получение сведений о подписках на стороне поставщика с предоставлением общего доступа для потребителей.</span><span class="sxs-lookup"><span data-stu-id="980ad-103">Gets information about consumer share subscriptions on provider side.</span></span>

## <span data-ttu-id="980ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="980ad-104">SYNTAX</span></span>

### <span data-ttu-id="980ad-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="980ad-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareProviderShareSubscription -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-ShareSubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="980ad-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="980ad-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Get-AzDataShareProviderShareSubscription [-ShareSubscriptionId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="980ad-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="980ad-107">DESCRIPTION</span></span>
<span data-ttu-id="980ad-108">Командлет **Get-AzDataShareProviderSubscription** получает сведения о совместном использовании подписок для потребителей на стороне поставщика.</span><span class="sxs-lookup"><span data-stu-id="980ad-108">The **Get-AzDataShareProviderSubscription** cmdlet gets information about consumer share subscriptions on provider side.</span></span> <span data-ttu-id="980ad-109">Если вы укажете идентификатор общего доступа подписку, этот командлет получает сведения о подписке на общий доступ.</span><span class="sxs-lookup"><span data-stu-id="980ad-109">If you specify the share subscrption id, this cmdlet gets information about the share subscription.</span></span> <span data-ttu-id="980ad-110">Если вы не укажете идентификатор подписку на общий доступ, этот командлет получает сведения обо всех потребительских подписках, связанных с общим доступом.</span><span class="sxs-lookup"><span data-stu-id="980ad-110">If you do not specify the share subscription id, this cmdlet gets information about all the consumer share subscriptions in associated with the share.</span></span>

## <span data-ttu-id="980ad-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="980ad-111">EXAMPLES</span></span>

### <span data-ttu-id="980ad-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="980ad-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareProviderShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -ShareSubscriptionId "/subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a"

Company                   : ADS Test
CreatedAt                 : 6/30/2019 12:42:12 AM
CreatedBy                 : adstest@microsoft.com
SharedAt                  : 6/30/2019 12:41:37 AM
SharedBy                  : adsprovider@microsoft.com
ShareSubscriptionObjectId : 505c3500-b2ff-46ab-96bf-50f5ec89d75a
ShareSubscriptionStatus   : Active
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a
Name                      : AdsShareSubscription
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="980ad-113">Эти команды предоставляют сведения о подписке, связанной с предоставлением общего доступа к AdsShare, в WikiAds учетной записи общего доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="980ad-113">This commands provides information about consumer share subscription associated with share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="980ad-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="980ad-114">PARAMETERS</span></span>

### <span data-ttu-id="980ad-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="980ad-115">-AccountName</span></span>
<span data-ttu-id="980ad-116">Имя учетной записи для общего доступа к Azure.</span><span class="sxs-lookup"><span data-stu-id="980ad-116">Azure DataShare Account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="980ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="980ad-117">-DefaultProfile</span></span>
<span data-ttu-id="980ad-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="980ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="980ad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="980ad-119">-ResourceGroupName</span></span>
<span data-ttu-id="980ad-120">Группа ресурсов для учетной записи "общий доступ к файлам Azure".</span><span class="sxs-lookup"><span data-stu-id="980ad-120">The resource group of the Azure DataShare Account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="980ad-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="980ad-121">-ResourceId</span></span>
<span data-ttu-id="980ad-122">Идентификатор ресурса общего доступа</span><span class="sxs-lookup"><span data-stu-id="980ad-122">The resource id of the share</span></span>

```yaml
Type: System.String
Parameter Sets: ByProviderShareSubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="980ad-123">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="980ad-123">-ShareName</span></span>
<span data-ttu-id="980ad-124">Имя общего ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="980ad-124">Azure DataShare name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="980ad-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="980ad-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="980ad-126">Идентификатор подписки на общий доступ для потребителей</span><span class="sxs-lookup"><span data-stu-id="980ad-126">The id of consumer share subscription</span></span>

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

### <span data-ttu-id="980ad-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="980ad-127">CommonParameters</span></span>
<span data-ttu-id="980ad-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="980ad-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="980ad-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="980ad-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="980ad-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="980ad-130">INPUTS</span></span>

### <span data-ttu-id="980ad-131">System. String</span><span class="sxs-lookup"><span data-stu-id="980ad-131">System.String</span></span>

## <span data-ttu-id="980ad-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="980ad-132">OUTPUTS</span></span>

### <span data-ttu-id="980ad-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="980ad-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="980ad-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="980ad-134">NOTES</span></span>

## <span data-ttu-id="980ad-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="980ad-135">RELATED LINKS</span></span>