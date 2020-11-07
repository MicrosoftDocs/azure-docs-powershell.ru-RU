---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
ms.openlocfilehash: d43754e1b04dadc447de3d727769902f5454f79a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565903"
---
# <span data-ttu-id="14876-101">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="14876-101">Stop-AzureBatchCertificateDeletion</span></span>

## <span data-ttu-id="14876-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14876-102">SYNOPSIS</span></span>
<span data-ttu-id="14876-103">Отмена неудачного удаления сертификата.</span><span class="sxs-lookup"><span data-stu-id="14876-103">Cancels a failed deletion of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14876-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14876-104">SYNTAX</span></span>

```
Stop-AzureBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14876-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14876-105">DESCRIPTION</span></span>
<span data-ttu-id="14876-106">Командлет **Stop-AzureBatchCertificateDeletion** отменяет сбой при удалении сертификата в пакетной службе Azure.</span><span class="sxs-lookup"><span data-stu-id="14876-106">The **Stop-AzureBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="14876-107">Вы можете прекратить удаление только в том случае, если сертификат находится в состоянии **DeleteFailed** .</span><span class="sxs-lookup"><span data-stu-id="14876-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="14876-108">Этот cmldet восстанавливает состояние сертификата в **активном** состоянии.</span><span class="sxs-lookup"><span data-stu-id="14876-108">This cmldet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="14876-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14876-109">EXAMPLES</span></span>

### <span data-ttu-id="14876-110">Пример 1: Отмена удаления</span><span class="sxs-lookup"><span data-stu-id="14876-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzureBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="14876-111">Эта команда отменяет Удаление сертификата, для которого указан отпечаток.</span><span class="sxs-lookup"><span data-stu-id="14876-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="14876-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14876-112">PARAMETERS</span></span>

### <span data-ttu-id="14876-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="14876-113">-BatchContext</span></span>
<span data-ttu-id="14876-114">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="14876-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="14876-115">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="14876-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="14876-116">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="14876-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="14876-117">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="14876-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="14876-118">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="14876-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="14876-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14876-119">-DefaultProfile</span></span>
<span data-ttu-id="14876-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14876-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14876-121">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="14876-121">-Thumbprint</span></span>
<span data-ttu-id="14876-122">Указывает отпечаток сертификата, который этот командлет восстанавливает в **активном** состоянии.</span><span class="sxs-lookup"><span data-stu-id="14876-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14876-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="14876-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="14876-124">Указывает алгоритм, используемый для получения параметра *отпечатка* .</span><span class="sxs-lookup"><span data-stu-id="14876-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="14876-125">В настоящее время единственным допустимым значением является SHA1.</span><span class="sxs-lookup"><span data-stu-id="14876-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="14876-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14876-126">CommonParameters</span></span>
<span data-ttu-id="14876-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14876-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14876-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14876-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14876-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14876-129">INPUTS</span></span>

### <span data-ttu-id="14876-130">System. String</span><span class="sxs-lookup"><span data-stu-id="14876-130">System.String</span></span>

### <span data-ttu-id="14876-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="14876-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="14876-132">Параметры: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="14876-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="14876-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14876-133">OUTPUTS</span></span>

### <span data-ttu-id="14876-134">System. void</span><span class="sxs-lookup"><span data-stu-id="14876-134">System.Void</span></span>

## <span data-ttu-id="14876-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="14876-135">NOTES</span></span>

## <span data-ttu-id="14876-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14876-136">RELATED LINKS</span></span>

[<span data-ttu-id="14876-137">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="14876-137">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="14876-138">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="14876-138">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="14876-139">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="14876-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

