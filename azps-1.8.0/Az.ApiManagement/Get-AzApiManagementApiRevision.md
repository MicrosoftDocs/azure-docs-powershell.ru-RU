---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
ms.openlocfilehash: 87292946f41da6d56f44351edc6a0ec8bbbfe3c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720168"
---
# <span data-ttu-id="06fa1-101">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="06fa1-101">Get-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="06fa1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="06fa1-102">SYNOPSIS</span></span>
<span data-ttu-id="06fa1-103">Получение подробных сведений о всех редакциях API для API</span><span class="sxs-lookup"><span data-stu-id="06fa1-103">Gets details of all the API Revisions of an API</span></span>

## <span data-ttu-id="06fa1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="06fa1-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06fa1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06fa1-105">DESCRIPTION</span></span>
<span data-ttu-id="06fa1-106">Командлет **Get-AzApiManagementApiRevision** получает подробные сведения обо всех РЕДАКЦИЯх API.</span><span class="sxs-lookup"><span data-stu-id="06fa1-106">The **Get-AzApiManagementApiRevision** cmdlet gets the details of all revisions of an API</span></span>

## <span data-ttu-id="06fa1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="06fa1-107">EXAMPLES</span></span>

### <span data-ttu-id="06fa1-108">Пример 1: получение всех редакций API для API</span><span class="sxs-lookup"><span data-stu-id="06fa1-108">Example 1: Get all API Revisions of an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "5adf6fbf0faadf3ad8558065"

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=3
ApiRevision     : 3
CreatedDateTime : 4/26/2018 10:57:42 PM
UpdatedDateTime : 4/26/2018 10:57:42 PM
Description     : ddsds
PrivateUrl      : /httpbin/v1;rev=3
IsOnline        : True
IsCurrent       : False

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=2
ApiRevision     : 2
CreatedDateTime : 4/26/2018 10:57:33 PM
UpdatedDateTime : 4/26/2018 10:57:33 PM
Description     : AA
PrivateUrl      : /httpbin/v1
IsOnline        : True
IsCurrent       : True

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=1
ApiRevision     : 1
CreatedDateTime : 4/24/2018 5:56:17 PM
UpdatedDateTime : 5/9/2018 9:29:06 PM
Description     :
PrivateUrl      : /httpbin/v1;rev=1
IsOnline        : True
IsCurrent       : False
```

<span data-ttu-id="06fa1-109">Эта команда возвращает все редакции API указанного API для определенного контекста ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="06fa1-109">This command gets all of the API revision of specified API for particular ApiManagement Context.</span></span>

## <span data-ttu-id="06fa1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="06fa1-110">PARAMETERS</span></span>

### <span data-ttu-id="06fa1-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="06fa1-111">-ApiId</span></span>
<span data-ttu-id="06fa1-112">Идентификатор API, для которого нужно создать список исправлений.</span><span class="sxs-lookup"><span data-stu-id="06fa1-112">API identifier whose revisions we want to list.</span></span>
<span data-ttu-id="06fa1-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="06fa1-113">This parameter is required.</span></span>

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

### <span data-ttu-id="06fa1-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="06fa1-114">-ApiRevision</span></span>
<span data-ttu-id="06fa1-115">Идентификатор редакции определенной редакции API.</span><span class="sxs-lookup"><span data-stu-id="06fa1-115">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="06fa1-116">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="06fa1-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06fa1-117">-Context</span><span class="sxs-lookup"><span data-stu-id="06fa1-117">-Context</span></span>
<span data-ttu-id="06fa1-118">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="06fa1-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="06fa1-119">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="06fa1-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06fa1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06fa1-120">-DefaultProfile</span></span>
<span data-ttu-id="06fa1-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="06fa1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06fa1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06fa1-122">CommonParameters</span></span>
<span data-ttu-id="06fa1-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="06fa1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06fa1-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06fa1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06fa1-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="06fa1-125">INPUTS</span></span>

### <span data-ttu-id="06fa1-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="06fa1-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="06fa1-127">System. String</span><span class="sxs-lookup"><span data-stu-id="06fa1-127">System.String</span></span>

## <span data-ttu-id="06fa1-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="06fa1-128">OUTPUTS</span></span>

### <span data-ttu-id="06fa1-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="06fa1-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span></span>

## <span data-ttu-id="06fa1-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="06fa1-130">NOTES</span></span>

## <span data-ttu-id="06fa1-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06fa1-131">RELATED LINKS</span></span>