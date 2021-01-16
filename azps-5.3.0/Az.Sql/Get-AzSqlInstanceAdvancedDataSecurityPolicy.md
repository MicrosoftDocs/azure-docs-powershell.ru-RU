---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceadvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 8adb699375a1b53f20e6027f35772642c658928b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506673"
---
# <span data-ttu-id="d0012-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="d0012-101">Get-AzSqlInstanceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="d0012-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0012-102">SYNOPSIS</span></span>
<span data-ttu-id="d0012-103">Получает политику advanced Data Security для управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d0012-103">Gets Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="d0012-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d0012-104">SYNTAX</span></span>

```
Get-AzSqlInstanceAdvancedDataSecurityPolicy [-InputObject <AzureSqlManagedInstanceModel>]
 -InstanceName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0012-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0012-105">DESCRIPTION</span></span>
<span data-ttu-id="d0012-106">Cmdlet **Get-AzSqlInstanceAdvancedDataSecurityPolicy** извлекает политику Advanced Data Security для управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d0012-106">The **Get-AzSqlInstanceAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a managed instance.</span></span>

## <span data-ttu-id="d0012-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d0012-107">EXAMPLES</span></span>

### <span data-ttu-id="d0012-108">Пример 1. Получает управляемый экземпляр Advanced Data Security</span><span class="sxs-lookup"><span data-stu-id="d0012-108">Example 1: Gets managed instance Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlInstanceAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -InstanceName "ManagedInstance01" `

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

### <span data-ttu-id="d0012-109">Пример 2. Получает управляемый экземпляр Advanced Data Security от ресурса управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="d0012-109">Example 2: Gets managed instance Advanced Data Security from managed instance resource</span></span>
```powershell
PS C:\>  Get-AzSqlInstance `
           -ResourceGroupName "ResourceGroup01" `
           -Name "ManagedInstance01" `
           | Get-AzSqlInstanceAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ManagedInstanceName          : ManagedInstance01
IsEnabled                    : True
```

## <span data-ttu-id="d0012-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0012-110">PARAMETERS</span></span>

### <span data-ttu-id="d0012-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0012-111">-DefaultProfile</span></span>
<span data-ttu-id="d0012-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d0012-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0012-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0012-113">-InputObject</span></span>
<span data-ttu-id="d0012-114">Объект управляемого экземпляра, который используется с операцией advanced Data Security</span><span class="sxs-lookup"><span data-stu-id="d0012-114">The managed instance object to use with Advanced Data Security policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0012-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d0012-115">-InstanceName</span></span>
<span data-ttu-id="d0012-116">SQL имени экземпляра, управляемого базой данных.</span><span class="sxs-lookup"><span data-stu-id="d0012-116">SQL Database managed instance name.</span></span>

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

### <span data-ttu-id="d0012-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0012-117">-ResourceGroupName</span></span>
<span data-ttu-id="d0012-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d0012-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="d0012-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0012-119">CommonParameters</span></span>
<span data-ttu-id="d0012-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0012-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0012-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0012-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0012-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0012-122">INPUTS</span></span>

### <span data-ttu-id="d0012-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="d0012-123">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="d0012-124">System.String</span><span class="sxs-lookup"><span data-stu-id="d0012-124">System.String</span></span>

## <span data-ttu-id="d0012-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d0012-125">OUTPUTS</span></span>

### <span data-ttu-id="d0012-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d0012-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ManagedInstanceAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="d0012-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d0012-127">NOTES</span></span>

## <span data-ttu-id="d0012-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0012-128">RELATED LINKS</span></span>