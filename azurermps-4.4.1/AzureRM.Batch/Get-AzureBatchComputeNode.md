---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 93614655-A8F2-4A67-887D-43D41AB91F82
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchComputeNode.md
ms.openlocfilehash: f503352352c31369e594325c060cf0ab68490095
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569712"
---
# <span data-ttu-id="3d201-101">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="3d201-101">Get-AzureBatchComputeNode</span></span>

## <span data-ttu-id="3d201-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d201-102">SYNOPSIS</span></span>
<span data-ttu-id="3d201-103">Получает пакетное вычисление узлов из пула.</span><span class="sxs-lookup"><span data-stu-id="3d201-103">Gets Batch compute nodes from a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d201-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d201-104">SYNTAX</span></span>

### <span data-ttu-id="3d201-105">ODataFilter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3d201-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchComputeNode [-PoolId] <String> [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d201-106">Номер</span><span class="sxs-lookup"><span data-stu-id="3d201-106">Id</span></span>
```
Get-AzureBatchComputeNode [-PoolId] <String> [[-Id] <String>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d201-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="3d201-107">ParentObject</span></span>
```
Get-AzureBatchComputeNode [[-Pool] <PSCloudPool>] [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d201-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d201-108">DESCRIPTION</span></span>
<span data-ttu-id="3d201-109">Командлет **Get-AzureBatchComputeNode** получает пакетные расчетные узлы Azure из пула.</span><span class="sxs-lookup"><span data-stu-id="3d201-109">The **Get-AzureBatchComputeNode** cmdlet gets Azure Batch compute nodes from a pool.</span></span>
<span data-ttu-id="3d201-110">Укажите параметр *PoolID* или *Pool* .</span><span class="sxs-lookup"><span data-stu-id="3d201-110">Specify either the *PoolID* or *Pool* parameter.</span></span>
<span data-ttu-id="3d201-111">Укажите параметр *ID* , чтобы получить один вычислительный узел.</span><span class="sxs-lookup"><span data-stu-id="3d201-111">Specify the *Id* parameter to get a single compute node.</span></span>
<span data-ttu-id="3d201-112">Укажите параметр *Filter* , чтобы получить вычислительные узлы, соответствующие фильтру Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="3d201-112">Specify the *Filter* parameter to get the compute nodes that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="3d201-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d201-113">EXAMPLES</span></span>

### <span data-ttu-id="3d201-114">Пример 1: получение высчитанного узла по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="3d201-114">Example 1: Get a compute node by ID</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : small
TotalTasksRun         : 1
StartTaskInformation  : 
RecentTasks           : {}
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="3d201-115">Эта команда возвращает узел COMPUTE node с ИДЕНТИФИКАТОРом TVM-2316545714_1-20150725t213220z из пула с ИД Pool06.</span><span class="sxs-lookup"><span data-stu-id="3d201-115">This command gets the compute node that has the ID tvm-2316545714_1-20150725t213220z from the pool that has the ID Pool06.</span></span>
<span data-ttu-id="3d201-116">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="3d201-116">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="3d201-117">Пример 2: получение всех бездействующих вычислительных узлов из пула</span><span class="sxs-lookup"><span data-stu-id="3d201-117">Example 2: Get all idle compute nodes from a pool</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Filter "state eq 'idle'" -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : small
TotalTasksRun         : 1
StartTaskInformation  : 
RecentTasks           : {}
StartTask             : 
CertificateReferences : 
Errors                : 

Id                    : tvm-2316545714_2-20150726t172920z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_2-20150726t172920z
State                 : Idle
StateTransitionTime   : 7/26/2015 5:33:58 PM
LastBootTime          : 7/26/2015 5:33:58 PM
AllocationTime        : 7/26/2015 5:29:20 PM
IPAddress             : 10.14.121.38
AffinityId            : TVM:tvm-2316545714_2-20150726t172920z
VirtualMachineSize    : small
TotalTasksRun         : 0
StartTaskInformation  : 
RecentTasks           : 
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="3d201-118">Эта команда получает все узлы с неактивным расчетом, содержащиеся в пуле с ИДЕНТИФИКАТОРом Pool06.</span><span class="sxs-lookup"><span data-stu-id="3d201-118">This command gets all idle compute nodes that are contained in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="3d201-119">Команда задает состояние простоя с помощью параметра " *Фильтр* ".</span><span class="sxs-lookup"><span data-stu-id="3d201-119">The command specifies the idle state by using the *Filter* parameter.</span></span>

### <span data-ttu-id="3d201-120">Пример 3: получение всех вычислительных узлов в указанном пуле</span><span class="sxs-lookup"><span data-stu-id="3d201-120">Example 3: Get all compute nodes in a specified pool</span></span>
```
PS C:\>Get-AzureBatchPool -Id "Pool07" -BatchContext $Context | Get-AzureBatchComputeNode -BatchContext $Context
Id                    : tvm-2316545714_1-20150725t213220z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_1-20150725t213220z
State                 : Idle
StateTransitionTime   : 7/25/2015 9:36:53 PM
LastBootTime          : 7/25/2015 9:36:53 PM
AllocationTime        : 7/25/2015 9:32:20 PM
IPAddress             : 10.14.121.1
AffinityId            : TVM:tvm-2316545714_1-20150725t213220z
VirtualMachineSize    : small
TotalTasksRun         : 1
StartTaskInformation  : 
RecentTasks           : {}
StartTask             : 
CertificateReferences : 
Errors                : 


Id                    : tvm-2316545714_2-20150726t172920z
Url                   : https://cmdletexample.westus.batch.azure.com/pools/MyPool/nodes/tvm-2316545714_2-20150726t172920z
State                 : Idle
StateTransitionTime   : 7/26/2015 5:33:58 PM
LastBootTime          : 7/26/2015 5:33:58 PM
AllocationTime        : 7/26/2015 5:29:20 PM

IPAddress             : 10.14.121.38
AffinityId            : TVM:tvm-2316545714_2-20150726t172920z
VirtualMachineSize    : small
TotalTasksRun         : 0
StartTaskInformation  : 
RecentTasks           : 
StartTask             : 
CertificateReferences : 
Errors                :
```

<span data-ttu-id="3d201-121">Эта команда получает пул с ИД Pool07 с помощью командлета Get-AzureBatchPool.</span><span class="sxs-lookup"><span data-stu-id="3d201-121">This command gets the pool that has the ID Pool07 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="3d201-122">Команда передает этот пул текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="3d201-122">The command passes that pool to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3d201-123">Этот командлет получает все вычислительные узлы из этого пула.</span><span class="sxs-lookup"><span data-stu-id="3d201-123">That cmdlet gets all compute nodes from that pool.</span></span>

## <span data-ttu-id="3d201-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d201-124">PARAMETERS</span></span>

### <span data-ttu-id="3d201-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3d201-125">-BatchContext</span></span>
<span data-ttu-id="3d201-126">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="3d201-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3d201-127">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="3d201-127">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d201-128">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="3d201-128">-Filter</span></span>
<span data-ttu-id="3d201-129">Задает предложение фильтра OData.</span><span class="sxs-lookup"><span data-stu-id="3d201-129">Specifies an OData filter clause.</span></span>
<span data-ttu-id="3d201-130">Этот командлет возвращает узлы COMPUTE, соответствующие фильтру, указанному в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="3d201-130">This cmdlet returns compute nodes that match the filter that this parameter specifies.</span></span>
<span data-ttu-id="3d201-131">Если фильтр не указан, этот командлет возвращает все вычислительные узлы для пула.</span><span class="sxs-lookup"><span data-stu-id="3d201-131">If you do not specify a filter, this cmdlet returns all compute nodes for the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d201-132">-ID</span><span class="sxs-lookup"><span data-stu-id="3d201-132">-Id</span></span>
<span data-ttu-id="3d201-133">Указывает идентификатор вычислительного узла, который этот командлет получает из пула.</span><span class="sxs-lookup"><span data-stu-id="3d201-133">Specifies the ID of the compute node that this cmdlet gets from the pool.</span></span>
<span data-ttu-id="3d201-134">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="3d201-134">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d201-135">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="3d201-135">-MaxCount</span></span>
<span data-ttu-id="3d201-136">Задает максимальное количество возвращаемых вычислительных узлов.</span><span class="sxs-lookup"><span data-stu-id="3d201-136">Specifies the maximum number of compute nodes to return.</span></span>
<span data-ttu-id="3d201-137">Если вы задаете нулевое значение (0) или меньше, в командлете не используется верхний предел.</span><span class="sxs-lookup"><span data-stu-id="3d201-137">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="3d201-138">Значение по умолчанию — 1000.</span><span class="sxs-lookup"><span data-stu-id="3d201-138">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter, ParentObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d201-139">-Пул</span><span class="sxs-lookup"><span data-stu-id="3d201-139">-Pool</span></span>
<span data-ttu-id="3d201-140">Определяет пул как объект **PSCloudPool** , содержащий вычислительные узлы.</span><span class="sxs-lookup"><span data-stu-id="3d201-140">Specifies the pool, as a **PSCloudPool** object, that contains the compute nodes.</span></span>
<span data-ttu-id="3d201-141">Чтобы получить объект **PSCloudPool** , используйте командлет Get-AzureBatchPool.</span><span class="sxs-lookup"><span data-stu-id="3d201-141">To obtain a **PSCloudPool** object, use the Get-AzureBatchPool cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d201-142">-PoolId</span><span class="sxs-lookup"><span data-stu-id="3d201-142">-PoolId</span></span>
<span data-ttu-id="3d201-143">Указывает идентификатор пула, который содержит вычислительные узлы.</span><span class="sxs-lookup"><span data-stu-id="3d201-143">Specifies the ID of the pool that contains the compute nodes.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter, Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d201-144">-SELECT</span><span class="sxs-lookup"><span data-stu-id="3d201-144">-Select</span></span>
<span data-ttu-id="3d201-145">Задает предложение SELECT OData.</span><span class="sxs-lookup"><span data-stu-id="3d201-145">Specifies an OData select clause.</span></span>
<span data-ttu-id="3d201-146">Укажите значение этого параметра, чтобы получить конкретные свойства, а не все свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="3d201-146">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="3d201-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d201-147">-DefaultProfile</span></span>
<span data-ttu-id="3d201-148">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3d201-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d201-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d201-149">CommonParameters</span></span>
<span data-ttu-id="3d201-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d201-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d201-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d201-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d201-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d201-152">INPUTS</span></span>

### <span data-ttu-id="3d201-153">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3d201-153">BatchAccountContext</span></span>
<span data-ttu-id="3d201-154">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3d201-154">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="3d201-155">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="3d201-155">PSCloudPool</span></span>
<span data-ttu-id="3d201-156">Параметр pool принимает значение типа "PSCloudPool" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3d201-156">Parameter 'Pool' accepts value of type 'PSCloudPool' from the pipeline</span></span>

## <span data-ttu-id="3d201-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d201-157">OUTPUTS</span></span>

### <span data-ttu-id="3d201-158">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="3d201-158">PSComputeNode</span></span>

## <span data-ttu-id="3d201-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d201-159">NOTES</span></span>

## <span data-ttu-id="3d201-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d201-160">RELATED LINKS</span></span>

[<span data-ttu-id="3d201-161">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="3d201-161">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="3d201-162">Get-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="3d201-162">Get-AzureBatchNodeFile</span></span>](./Get-AzureBatchNodeFile.md)

[<span data-ttu-id="3d201-163">Get-AzureBatchNodeFileContent</span><span class="sxs-lookup"><span data-stu-id="3d201-163">Get-AzureBatchNodeFileContent</span></span>](./Get-AzureBatchNodeFileContent.md)

[<span data-ttu-id="3d201-164">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="3d201-164">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="3d201-165">Сброс — AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="3d201-165">Reset-AzureBatchComputeNode</span></span>](./Reset-AzureBatchComputeNode.md)

[<span data-ttu-id="3d201-166">Restarting-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="3d201-166">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)

[<span data-ttu-id="3d201-167">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="3d201-167">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

