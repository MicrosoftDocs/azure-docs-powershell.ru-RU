---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
ms.openlocfilehash: 1f9f0258bf107ae0ca7be7050f8db8e3db8b1ffa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721207"
---
# <span data-ttu-id="90173-101">Get-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="90173-101">Get-AzDataShareInvitation</span></span>

## <span data-ttu-id="90173-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="90173-102">SYNOPSIS</span></span>
<span data-ttu-id="90173-103">Получение сведений о соотношении общего доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="90173-103">Gets information invitation of data share.</span></span>

## <span data-ttu-id="90173-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="90173-104">SYNTAX</span></span>

### <span data-ttu-id="90173-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="90173-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90173-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="90173-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareInvitation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90173-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90173-107">DESCRIPTION</span></span>
<span data-ttu-id="90173-108">Командлет **Get-AzDataShareInvitation** получает сведения о приглашениях, добавленных в общий доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="90173-108">The **Get-AzDataShareInvitation** cmdlet gets information on invitations added in data share.</span></span> <span data-ttu-id="90173-109">Если вы задаете имя приглашения, этот командлет получает сведения о приглашении.</span><span class="sxs-lookup"><span data-stu-id="90173-109">If you specify the name of the invitation, this cmdlet gets information about the invitation.</span></span> <span data-ttu-id="90173-110">Если имя не задано, этот командлет получает сведения обо всех приглашениях в общем доступе.</span><span class="sxs-lookup"><span data-stu-id="90173-110">If you do not specify a name, this cmdlet gets information about all the invitations in a share.</span></span>

## <span data-ttu-id="90173-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="90173-111">EXAMPLES</span></span>

### <span data-ttu-id="90173-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="90173-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareInvitation -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsInvitation"

InvitationId     : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus : Pending
Sender           : adsprovider@microsoft.com
SentAt           : 7/8/2019 10:47:10 PM
TargetEmail      : adstest@microsoft.com
TargetObjectId   :
TargetTenantId   :
Id               : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/invitations/AdsInvitation
Name             : AdsInvitation
Type             : Microsoft.DataShare/Invitations
```

<span data-ttu-id="90173-113">Эти команды предоставляют сведения о приглашении AdsInvitation в общем доступе к данным AdsShare.</span><span class="sxs-lookup"><span data-stu-id="90173-113">This commands provides information about invitation AdsInvitation present in data share AdsShare.</span></span>

## <span data-ttu-id="90173-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="90173-114">PARAMETERS</span></span>

### <span data-ttu-id="90173-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="90173-115">-AccountName</span></span>
<span data-ttu-id="90173-116">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="90173-116">Azure data share account name</span></span>

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

### <span data-ttu-id="90173-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90173-117">-DefaultProfile</span></span>
<span data-ttu-id="90173-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90173-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90173-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="90173-119">-Name</span></span>
<span data-ttu-id="90173-120">Имя приглашения на предоставление данных Azure</span><span class="sxs-lookup"><span data-stu-id="90173-120">Azure data share invitation name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90173-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90173-121">-ResourceGroupName</span></span>
<span data-ttu-id="90173-122">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="90173-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="90173-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90173-123">-ResourceId</span></span>
<span data-ttu-id="90173-124">Идентификатор ресурса для приглашения на доступ к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="90173-124">The resource id of the azure data share invitation</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90173-125">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="90173-125">-ShareName</span></span>
<span data-ttu-id="90173-126">Имя общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="90173-126">Azure data share name</span></span>

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

### <span data-ttu-id="90173-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90173-127">CommonParameters</span></span>
<span data-ttu-id="90173-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="90173-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90173-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90173-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90173-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="90173-130">INPUTS</span></span>

### <span data-ttu-id="90173-131">System. String</span><span class="sxs-lookup"><span data-stu-id="90173-131">System.String</span></span>

## <span data-ttu-id="90173-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="90173-132">OUTPUTS</span></span>

### <span data-ttu-id="90173-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="90173-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="90173-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="90173-134">NOTES</span></span>

## <span data-ttu-id="90173-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90173-135">RELATED LINKS</span></span>