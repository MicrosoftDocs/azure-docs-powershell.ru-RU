---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
ms.openlocfilehash: 2e474462983f15c0d58f8ada60b907c100508c6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563747"
---
# <span data-ttu-id="cf4bc-101">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cf4bc-101">Remove-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="cf4bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf4bc-102">SYNOPSIS</span></span>
<span data-ttu-id="cf4bc-103">Удаляет расписание пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="cf4bc-103">Removes a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf4bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf4bc-104">SYNTAX</span></span>

```
Remove-AzureBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf4bc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf4bc-105">DESCRIPTION</span></span>
<span data-ttu-id="cf4bc-106">Командлет **Remove-AzureBatchJobSchedule** Удаляет расписание пакетного задания Azure.</span><span class="sxs-lookup"><span data-stu-id="cf4bc-106">The **Remove-AzureBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="cf4bc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf4bc-107">EXAMPLES</span></span>

## <span data-ttu-id="cf4bc-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf4bc-108">PARAMETERS</span></span>

### <span data-ttu-id="cf4bc-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cf4bc-109">-BatchContext</span></span>
<span data-ttu-id="cf4bc-110">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="cf4bc-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cf4bc-111">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="cf4bc-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cf4bc-112">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="cf4bc-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cf4bc-113">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="cf4bc-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cf4bc-114">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="cf4bc-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cf4bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf4bc-115">-DefaultProfile</span></span>
<span data-ttu-id="cf4bc-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf4bc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf4bc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="cf4bc-117">-Force</span></span>
<span data-ttu-id="cf4bc-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="cf4bc-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf4bc-119">-ID</span><span class="sxs-lookup"><span data-stu-id="cf4bc-119">-Id</span></span>
<span data-ttu-id="cf4bc-120">Указывает идентификатор расписания задания, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="cf4bc-120">Specifies the ID of the job schedule to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf4bc-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf4bc-121">-Confirm</span></span>
<span data-ttu-id="cf4bc-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cf4bc-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf4bc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf4bc-123">-WhatIf</span></span>
<span data-ttu-id="cf4bc-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cf4bc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf4bc-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cf4bc-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf4bc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf4bc-126">CommonParameters</span></span>
<span data-ttu-id="cf4bc-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf4bc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf4bc-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf4bc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf4bc-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf4bc-129">INPUTS</span></span>

### <span data-ttu-id="cf4bc-130">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cf4bc-130">BatchAccountContext</span></span>
<span data-ttu-id="cf4bc-131">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="cf4bc-131">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="cf4bc-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf4bc-132">OUTPUTS</span></span>

## <span data-ttu-id="cf4bc-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf4bc-133">NOTES</span></span>

## <span data-ttu-id="cf4bc-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf4bc-134">RELATED LINKS</span></span>

[<span data-ttu-id="cf4bc-135">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cf4bc-135">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="cf4bc-136">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cf4bc-136">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="cf4bc-137">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cf4bc-137">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="cf4bc-138">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cf4bc-138">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="cf4bc-139">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cf4bc-139">Set-AzureBatchJobSchedule</span></span>](./Set-AzureBatchJobSchedule.md)

[<span data-ttu-id="cf4bc-140">Остановить-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="cf4bc-140">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

