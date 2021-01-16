---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
ms.openlocfilehash: 5d27610924fe0b4a92acfb5f7d1e678742d5b5c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424788"
---
# <span data-ttu-id="a4c02-101">Get-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="a4c02-101">Get-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="a4c02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4c02-102">SYNOPSIS</span></span>
<span data-ttu-id="a4c02-103">Укаймь все реплики для данного сервера.</span><span class="sxs-lookup"><span data-stu-id="a4c02-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="a4c02-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a4c02-104">SYNTAX</span></span>

```
Get-AzPostgreSqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a4c02-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4c02-105">DESCRIPTION</span></span>
<span data-ttu-id="a4c02-106">Укаймь все реплики для данного сервера.</span><span class="sxs-lookup"><span data-stu-id="a4c02-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="a4c02-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a4c02-107">EXAMPLES</span></span>

### <span data-ttu-id="a4c02-108">Пример 1. Получить репликацию сервера PostgreSql по группе ресурсов и имени сервера</span><span class="sxs-lookup"><span data-stu-id="a4c02-108">Example 1: Get PostgreSql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlReplica -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="a4c02-109">Этот cmdlet получает репликацию сервера PostgreSql по группе ресурсов и имени сервера.</span><span class="sxs-lookup"><span data-stu-id="a4c02-109">This cmdlet gets PostgreSql server replica by resource group and server name.</span></span>

## <span data-ttu-id="a4c02-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4c02-110">PARAMETERS</span></span>

### <span data-ttu-id="a4c02-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4c02-111">-DefaultProfile</span></span>
<span data-ttu-id="a4c02-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4c02-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4c02-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4c02-113">-ResourceGroupName</span></span>
<span data-ttu-id="a4c02-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a4c02-114">The name of the resource group.</span></span>
<span data-ttu-id="a4c02-115">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="a4c02-115">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4c02-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a4c02-116">-ServerName</span></span>
<span data-ttu-id="a4c02-117">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="a4c02-117">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4c02-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a4c02-118">-SubscriptionId</span></span>
<span data-ttu-id="a4c02-119">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="a4c02-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4c02-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4c02-120">CommonParameters</span></span>
<span data-ttu-id="a4c02-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4c02-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4c02-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4c02-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4c02-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4c02-123">INPUTS</span></span>

## <span data-ttu-id="a4c02-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a4c02-124">OUTPUTS</span></span>

### <span data-ttu-id="a4c02-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="a4c02-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="a4c02-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a4c02-126">NOTES</span></span>

<span data-ttu-id="a4c02-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a4c02-127">ALIASES</span></span>

## <span data-ttu-id="a4c02-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4c02-128">RELATED LINKS</span></span>
