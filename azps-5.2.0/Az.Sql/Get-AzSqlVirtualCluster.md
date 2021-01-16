---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
ms.openlocfilehash: bd12fd2067c931f05266ed1ed24fb5666ead59a9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415332"
---
# <span data-ttu-id="70ff9-101">Get-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="70ff9-101">Get-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="70ff9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70ff9-102">SYNOPSIS</span></span>
<span data-ttu-id="70ff9-103">Возвращает сведения о виртуальном кластере Azure SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="70ff9-103">Returns information about Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="70ff9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="70ff9-104">SYNTAX</span></span>

### <span data-ttu-id="70ff9-105">GetVirtualClusterByResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="70ff9-105">GetVirtualClusterByResourceGroup (Default)</span></span>
```
Get-AzSqlVirtualCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="70ff9-106">GetVirtualClusterByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="70ff9-106">GetVirtualClusterByNameAndResourceGroup</span></span>
```
Get-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70ff9-107">GetVirtualClusterByResourceId</span><span class="sxs-lookup"><span data-stu-id="70ff9-107">GetVirtualClusterByResourceId</span></span>
```
Get-AzSqlVirtualCluster [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70ff9-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="70ff9-108">DESCRIPTION</span></span>
<span data-ttu-id="70ff9-109">Cmdlet **Get-AzSqlVirtualCluster** возвращает сведения об одном или SQL виртуальных кластерах Azure.</span><span class="sxs-lookup"><span data-stu-id="70ff9-109">The **Get-AzSqlVirtualCluster** cmdlet returns information about one or more Azure SQL Virtual Clusters.</span></span>
<span data-ttu-id="70ff9-110">Укажите имя виртуального кластера, чтобы увидеть сведения только для этого кластера.</span><span class="sxs-lookup"><span data-stu-id="70ff9-110">Specify the name of a virtual cluster to see information for only that cluster.</span></span>

## <span data-ttu-id="70ff9-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="70ff9-111">EXAMPLES</span></span>

### <span data-ttu-id="70ff9-112">Пример 1. Все виртуальные кластеры, которые назначены группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="70ff9-112">Example 1: Get all virtual clusters assigned to a resource group</span></span>
```powershell
PS C:> Get-AzSqlVirtualCluster -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1

Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster2
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster2
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name2

Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster3
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster3
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name3
```

<span data-ttu-id="70ff9-113">Эта команда получает сведения обо всех виртуальных кластерах, которые назначены группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="70ff9-113">This command gets information about all Virtual Clusters assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="70ff9-114">Пример 2. Сведения об определенном виртуальном кластере</span><span class="sxs-lookup"><span data-stu-id="70ff9-114">Example 2: Get information about specific virtual cluster</span></span>
```
PS C:\>  Get-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1
```

<span data-ttu-id="70ff9-115">Эта команда получает сведения о виртуальном кластере VirtualCluster1 в группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="70ff9-115">This command gets information about the virtual cluster VirtualCluster1 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="70ff9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70ff9-116">PARAMETERS</span></span>

### <span data-ttu-id="70ff9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70ff9-117">-DefaultProfile</span></span>
<span data-ttu-id="70ff9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="70ff9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70ff9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="70ff9-119">-Name</span></span>
<span data-ttu-id="70ff9-120">Имя виртуального кластера.</span><span class="sxs-lookup"><span data-stu-id="70ff9-120">The name of the virtual cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByNameAndResourceGroup
Aliases: VirtualClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70ff9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70ff9-121">-ResourceGroupName</span></span>
<span data-ttu-id="70ff9-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="70ff9-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70ff9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70ff9-123">-ResourceId</span></span>
<span data-ttu-id="70ff9-124">ИД ресурса объекта экземпляра, который требуется получить</span><span class="sxs-lookup"><span data-stu-id="70ff9-124">The resource id of instance object to get</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70ff9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70ff9-125">CommonParameters</span></span>
<span data-ttu-id="70ff9-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70ff9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70ff9-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70ff9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70ff9-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="70ff9-128">INPUTS</span></span>

### <span data-ttu-id="70ff9-129">Нет</span><span class="sxs-lookup"><span data-stu-id="70ff9-129">None</span></span>

## <span data-ttu-id="70ff9-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="70ff9-130">OUTPUTS</span></span>

### <span data-ttu-id="70ff9-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="70ff9-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="70ff9-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="70ff9-132">NOTES</span></span>

## <span data-ttu-id="70ff9-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="70ff9-133">RELATED LINKS</span></span>