---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
ms.openlocfilehash: dcb9d6e58a743f37aa71d91b0b73772c239f252e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721255"
---
# <span data-ttu-id="41cf1-101">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="41cf1-101">Get-AzDataMigrationService</span></span>

## <span data-ttu-id="41cf1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41cf1-102">SYNOPSIS</span></span>
<span data-ttu-id="41cf1-103">Извлекает свойства, связанные с экземпляром службы миграции баз данных Azure.</span><span class="sxs-lookup"><span data-stu-id="41cf1-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

## <span data-ttu-id="41cf1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41cf1-104">SYNTAX</span></span>

### <span data-ttu-id="41cf1-105">ResourceGroupSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="41cf1-105">ResourceGroupSet (Default)</span></span>
```
Get-AzDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="41cf1-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41cf1-106">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="41cf1-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="41cf1-107">ServiceNameGroupSet</span></span>
```
Get-AzDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41cf1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41cf1-108">DESCRIPTION</span></span>
<span data-ttu-id="41cf1-109">Командлет Get-AzDataMigrationService извлекает свойства, связанные с экземпляром службы миграции баз данных Azure, на основе имени службы и имени группы ресурсов Azure в качестве входных параметров.</span><span class="sxs-lookup"><span data-stu-id="41cf1-109">The Get-AzDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="41cf1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41cf1-110">EXAMPLES</span></span>

### <span data-ttu-id="41cf1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="41cf1-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="41cf1-112">В приведенном выше примере извлекаются свойства экземпляра службы миграции баз данных Azure с именем testService.</span><span class="sxs-lookup"><span data-stu-id="41cf1-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="41cf1-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="41cf1-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup
```

<span data-ttu-id="41cf1-114">В приведенном выше примере выполняется получение служб миграции баз данных Azure в группе ресурсов с именем testResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="41cf1-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="41cf1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41cf1-115">PARAMETERS</span></span>

### <span data-ttu-id="41cf1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41cf1-116">-DefaultProfile</span></span>
<span data-ttu-id="41cf1-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41cf1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41cf1-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="41cf1-118">-Name</span></span>
<span data-ttu-id="41cf1-119">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="41cf1-119">Name of Database Migration Service.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41cf1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41cf1-120">-ResourceGroupName</span></span>
<span data-ttu-id="41cf1-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="41cf1-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41cf1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41cf1-122">-ResourceId</span></span>
<span data-ttu-id="41cf1-123">Идентификатор ресурса DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="41cf1-123">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="41cf1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41cf1-124">CommonParameters</span></span>
<span data-ttu-id="41cf1-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41cf1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41cf1-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41cf1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41cf1-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41cf1-127">INPUTS</span></span>

### <span data-ttu-id="41cf1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="41cf1-128">System.String</span></span>

## <span data-ttu-id="41cf1-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41cf1-129">OUTPUTS</span></span>

### <span data-ttu-id="41cf1-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="41cf1-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="41cf1-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="41cf1-131">NOTES</span></span>

## <span data-ttu-id="41cf1-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41cf1-132">RELATED LINKS</span></span>