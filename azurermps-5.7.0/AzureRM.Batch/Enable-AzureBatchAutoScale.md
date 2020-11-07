---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
ms.openlocfilehash: 73c1efe9e25fa02dc06f367eae1d010562eba56e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570255"
---
# <span data-ttu-id="31dc7-101">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="31dc7-101">Enable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="31dc7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="31dc7-103">Включает автоматическое масштабирование пула.</span><span class="sxs-lookup"><span data-stu-id="31dc7-103">Enables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31dc7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31dc7-104">SYNTAX</span></span>

```
Enable-AzureBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31dc7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31dc7-105">DESCRIPTION</span></span>
<span data-ttu-id="31dc7-106">Командлет **Enable-AzureBatchAutoScale** включает автоматическое масштабирование указанного пула.</span><span class="sxs-lookup"><span data-stu-id="31dc7-106">The **Enable-AzureBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="31dc7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31dc7-107">EXAMPLES</span></span>

### <span data-ttu-id="31dc7-108">Пример 1: Включение автоматического масштабирования для пула</span><span class="sxs-lookup"><span data-stu-id="31dc7-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzureBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="31dc7-109">Первая команда определяет формулу, а затем сохраняет ее в $Formula переменной.</span><span class="sxs-lookup"><span data-stu-id="31dc7-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>

<span data-ttu-id="31dc7-110">Вторая команда включает автоматическое масштабирование в пуле с именем MyPool, используя формулу в $Formula.</span><span class="sxs-lookup"><span data-stu-id="31dc7-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="31dc7-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31dc7-111">PARAMETERS</span></span>

### <span data-ttu-id="31dc7-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="31dc7-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="31dc7-113">Определяет интервал времени (в минутах), по истечении которого размер пула будет автоматически скорректирован согласно формуле автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="31dc7-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="31dc7-114">По умолчанию используется значение 15 минут, а минимальное — 5 минут.</span><span class="sxs-lookup"><span data-stu-id="31dc7-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31dc7-115">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="31dc7-115">-AutoScaleFormula</span></span>
<span data-ttu-id="31dc7-116">Задает формулу для требуемого количества вычислительных узлов в пуле.</span><span class="sxs-lookup"><span data-stu-id="31dc7-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31dc7-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="31dc7-117">-BatchContext</span></span>
<span data-ttu-id="31dc7-118">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="31dc7-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="31dc7-119">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="31dc7-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="31dc7-120">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="31dc7-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="31dc7-121">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="31dc7-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="31dc7-122">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="31dc7-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31dc7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31dc7-123">-DefaultProfile</span></span>
<span data-ttu-id="31dc7-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31dc7-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31dc7-125">-ID</span><span class="sxs-lookup"><span data-stu-id="31dc7-125">-Id</span></span>
<span data-ttu-id="31dc7-126">Указывает идентификатор объекта пула, для которого нужно включить автоматическое масштабирование.</span><span class="sxs-lookup"><span data-stu-id="31dc7-126">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31dc7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31dc7-127">CommonParameters</span></span>
<span data-ttu-id="31dc7-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31dc7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31dc7-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31dc7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31dc7-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31dc7-130">INPUTS</span></span>

### <span data-ttu-id="31dc7-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="31dc7-131">BatchAccountContext</span></span>
<span data-ttu-id="31dc7-132">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="31dc7-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="31dc7-133">Подстрок</span><span class="sxs-lookup"><span data-stu-id="31dc7-133">String</span></span>
<span data-ttu-id="31dc7-134">Параметр ID принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="31dc7-134">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="31dc7-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31dc7-135">OUTPUTS</span></span>

## <span data-ttu-id="31dc7-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="31dc7-136">NOTES</span></span>

## <span data-ttu-id="31dc7-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31dc7-137">RELATED LINKS</span></span>

[<span data-ttu-id="31dc7-138">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="31dc7-138">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="31dc7-139">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="31dc7-139">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="31dc7-140">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="31dc7-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

