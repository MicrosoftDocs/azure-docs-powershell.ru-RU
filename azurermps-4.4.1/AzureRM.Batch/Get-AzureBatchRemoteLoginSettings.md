---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
ms.openlocfilehash: 848f0cf3d2d36b9ff5c80792c23d126956dccfbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570120"
---
# <span data-ttu-id="abb8e-101">Get-AzureBatchRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="abb8e-101">Get-AzureBatchRemoteLoginSettings</span></span>

## <span data-ttu-id="abb8e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="abb8e-102">SYNOPSIS</span></span>
<span data-ttu-id="abb8e-103">Получает параметры удаленного входа для вычислительного узла.</span><span class="sxs-lookup"><span data-stu-id="abb8e-103">Gets remote logon settings for a compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abb8e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="abb8e-104">SYNTAX</span></span>

### <span data-ttu-id="abb8e-105">ID (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="abb8e-105">Id (Default)</span></span>
```
Get-AzureBatchRemoteLoginSettings [-PoolId] <String> [-ComputeNodeId] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abb8e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="abb8e-106">InputObject</span></span>
```
Get-AzureBatchRemoteLoginSettings [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abb8e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="abb8e-107">DESCRIPTION</span></span>
<span data-ttu-id="abb8e-108">Командлет **Get-AzureBatchRemoteLoginSettings** получает параметры удаленного входа для вычислительного узла в пуле на основе инфраструктуры виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="abb8e-108">The **Get-AzureBatchRemoteLoginSettings** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="abb8e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="abb8e-109">EXAMPLES</span></span>

### <span data-ttu-id="abb8e-110">Пример 1: получение параметров удаленного входа для всех узлов в пуле</span><span class="sxs-lookup"><span data-stu-id="abb8e-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzureBatchRemoteLoginSettings -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="abb8e-111">Первая команда получает контекст учетной записи пакета, который включает клавиши доступа для вашей подписки, с помощью **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="abb8e-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="abb8e-112">Команда хранит контекст в переменной $Context для использования в следующей команде.</span><span class="sxs-lookup"><span data-stu-id="abb8e-112">The command stores the context in the $Context variable to use in the next command.</span></span>

<span data-ttu-id="abb8e-113">Вторая команда получает каждый вычислительный узел в пуле с ИД ContosoPool с помощью **Get-AzureBatchComputeNode**.</span><span class="sxs-lookup"><span data-stu-id="abb8e-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzureBatchComputeNode**.</span></span>
<span data-ttu-id="abb8e-114">Команда передает каждый узел компьютера в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="abb8e-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="abb8e-115">Команда получает параметры удаленного входа для каждого вычислительного узла.</span><span class="sxs-lookup"><span data-stu-id="abb8e-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="abb8e-116">Пример 2: получение параметров удаленного входа для узла</span><span class="sxs-lookup"><span data-stu-id="abb8e-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchRemoteLoginSettings -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="abb8e-117">Первая команда получает контекст учетной записи пакета, который содержит клавиши доступа для вашей подписки, а затем сохраняет его в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="abb8e-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>

<span data-ttu-id="abb8e-118">Вторая команда получает параметры удаленного входа для вычислительного узла с указанным ИДЕНТИФИКАТОРом в пуле с ИДЕНТИФИКАТОРом ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="abb8e-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="abb8e-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="abb8e-119">PARAMETERS</span></span>

### <span data-ttu-id="abb8e-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="abb8e-120">-BatchContext</span></span>
<span data-ttu-id="abb8e-121">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="abb8e-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="abb8e-122">Чтобы получить **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="abb8e-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="abb8e-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="abb8e-123">-ComputeNode</span></span>
<span data-ttu-id="abb8e-124">Задает вычислительный узел, как объект **PSComputeNode** , для которого этот командлет получает параметры удаленного входа.</span><span class="sxs-lookup"><span data-stu-id="abb8e-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="abb8e-125">Чтобы получить объект COMPUTE Node, используйте командлет Get-AzureBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="abb8e-125">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abb8e-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="abb8e-126">-ComputeNodeId</span></span>
<span data-ttu-id="abb8e-127">Указывает идентификатор вычислительного узла, для которого нужно получить параметры удаленного входа.</span><span class="sxs-lookup"><span data-stu-id="abb8e-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="abb8e-128">, для которого этот командлет получает параметры удаленного входа.</span><span class="sxs-lookup"><span data-stu-id="abb8e-128">for which this cmdlet gets remote logon settings.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb8e-129">-PoolId</span><span class="sxs-lookup"><span data-stu-id="abb8e-129">-PoolId</span></span>
<span data-ttu-id="abb8e-130">Указывает идентификатор пула, который содержит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="abb8e-130">Specifies the ID of the pool that contains the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb8e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abb8e-131">-DefaultProfile</span></span>
<span data-ttu-id="abb8e-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="abb8e-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abb8e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abb8e-133">CommonParameters</span></span>
<span data-ttu-id="abb8e-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="abb8e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abb8e-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abb8e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abb8e-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="abb8e-136">INPUTS</span></span>

### <span data-ttu-id="abb8e-137">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="abb8e-137">BatchAccountContext</span></span>
<span data-ttu-id="abb8e-138">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="abb8e-138">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="abb8e-139">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="abb8e-139">PSComputeNode</span></span>
<span data-ttu-id="abb8e-140">Параметр "ComputeNode" принимает значение типа "PSComputeNode" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="abb8e-140">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="abb8e-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="abb8e-141">OUTPUTS</span></span>

### <span data-ttu-id="abb8e-142">PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="abb8e-142">PSRemoteLoginSettings</span></span>

## <span data-ttu-id="abb8e-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="abb8e-143">NOTES</span></span>

## <span data-ttu-id="abb8e-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="abb8e-144">RELATED LINKS</span></span>

[<span data-ttu-id="abb8e-145">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="abb8e-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="abb8e-146">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="abb8e-146">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="abb8e-147">Get-AzureBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="abb8e-147">Get-AzureBatchRemoteDesktopProtocolFile</span></span>](./Get-AzureBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="abb8e-148">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="abb8e-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

