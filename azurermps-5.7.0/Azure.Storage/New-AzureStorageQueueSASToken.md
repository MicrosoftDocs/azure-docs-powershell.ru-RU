---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 42C669B6-B621-454C-B897-262E1C8E76E3
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeuesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueSASToken.md
ms.openlocfilehash: da9394d4d255a4ac09c8de437ee72b9d399cda35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565066"
---
# <span data-ttu-id="251d0-101">New-AzureStorageQueueSASToken</span><span class="sxs-lookup"><span data-stu-id="251d0-101">New-AzureStorageQueueSASToken</span></span>

## <span data-ttu-id="251d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="251d0-102">SYNOPSIS</span></span>
<span data-ttu-id="251d0-103">Создание маркера подписи общего доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="251d0-103">Generates a shared access signature token for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="251d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="251d0-104">SYNTAX</span></span>

### <span data-ttu-id="251d0-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="251d0-105">SasPolicy</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="251d0-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="251d0-106">SasPermission</span></span>
```
New-AzureStorageQueueSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="251d0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="251d0-107">DESCRIPTION</span></span>
<span data-ttu-id="251d0-108">Командлет **New-AzureStorageQueueSASToken** создает маркер подписи общего доступа для очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="251d0-108">The **New-AzureStorageQueueSASToken** cmdlet generates shared access signature token for an Azure storage queue.</span></span>

## <span data-ttu-id="251d0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="251d0-109">EXAMPLES</span></span>

### <span data-ttu-id="251d0-110">Пример 1: создание маркера SAS очереди с полным разрешением</span><span class="sxs-lookup"><span data-stu-id="251d0-110">Example 1: Generate a queue SAS token with full permission</span></span>
```
PS C:\>New-AzureStorageQueueSASToken -Name "Test" -Permission raup
```

<span data-ttu-id="251d0-111">В этом примере создается маркер SAS очереди с полным разрешением.</span><span class="sxs-lookup"><span data-stu-id="251d0-111">This example generates a queue SAS token with full permission.</span></span>

## <span data-ttu-id="251d0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="251d0-112">PARAMETERS</span></span>

### <span data-ttu-id="251d0-113">-Context</span><span class="sxs-lookup"><span data-stu-id="251d0-113">-Context</span></span>
<span data-ttu-id="251d0-114">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="251d0-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="251d0-115">Вы можете создать его с помощью New-AzureStorageContext командлета.</span><span class="sxs-lookup"><span data-stu-id="251d0-115">You can create it by New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="251d0-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="251d0-116">-ExpiryTime</span></span>
<span data-ttu-id="251d0-117">Указывает, что подпись общего доступа больше не действительна.</span><span class="sxs-lookup"><span data-stu-id="251d0-117">Specifies when the shared access signature is no longer valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251d0-118">-FullUri</span><span class="sxs-lookup"><span data-stu-id="251d0-118">-FullUri</span></span>
<span data-ttu-id="251d0-119">Указывает на то, что этот командлет возвращает полный URI большого двоичного объекта и маркер подписи общего доступа.</span><span class="sxs-lookup"><span data-stu-id="251d0-119">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="251d0-120">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="251d0-120">-IPAddressOrRange</span></span>
<span data-ttu-id="251d0-121">Указывает IP-адрес или диапазон IP-адресов, из которых нужно принимать запросы (например, 168.1.5.65 или 168.1.5.60-168.1.5.70).</span><span class="sxs-lookup"><span data-stu-id="251d0-121">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="251d0-122">Диапазон — включительно.</span><span class="sxs-lookup"><span data-stu-id="251d0-122">The range is inclusive.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251d0-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="251d0-123">-Name</span></span>
<span data-ttu-id="251d0-124">Указывает имя очереди хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="251d0-124">Specifies an Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="251d0-125">-Разрешения</span><span class="sxs-lookup"><span data-stu-id="251d0-125">-Permission</span></span>
<span data-ttu-id="251d0-126">Задает разрешения для очереди хранилища.</span><span class="sxs-lookup"><span data-stu-id="251d0-126">Specifies permissions for a storage queue.</span></span>

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251d0-127">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="251d0-127">-Policy</span></span>
<span data-ttu-id="251d0-128">Указывает политику сохраненного доступа Azure.</span><span class="sxs-lookup"><span data-stu-id="251d0-128">Specifies an Azure stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251d0-129">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="251d0-129">-Protocol</span></span>
<span data-ttu-id="251d0-130">Указывает протокол, разрешенный для запроса.</span><span class="sxs-lookup"><span data-stu-id="251d0-130">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="251d0-131">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="251d0-131">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="251d0-132">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="251d0-132">HttpsOnly</span></span>
* <span data-ttu-id="251d0-133">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="251d0-133">HttpsOrHttp</span></span>

<span data-ttu-id="251d0-134">Значением по умолчанию является HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="251d0-134">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251d0-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="251d0-135">-StartTime</span></span>
<span data-ttu-id="251d0-136">Указывает, когда подпись общего доступа становится действительной.</span><span class="sxs-lookup"><span data-stu-id="251d0-136">Specifies when the shared access signature becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251d0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="251d0-137">CommonParameters</span></span>
<span data-ttu-id="251d0-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="251d0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="251d0-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="251d0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="251d0-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="251d0-140">INPUTS</span></span>

### <span data-ttu-id="251d0-141">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="251d0-141">IStorageContext</span></span>

<span data-ttu-id="251d0-142">Параметр "Context" принимает значение типа "IStorageContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="251d0-142">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="251d0-143">Подстрок</span><span class="sxs-lookup"><span data-stu-id="251d0-143">String</span></span>

<span data-ttu-id="251d0-144">Параметр Name принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="251d0-144">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="251d0-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="251d0-145">OUTPUTS</span></span>

### <span data-ttu-id="251d0-146">System. String</span><span class="sxs-lookup"><span data-stu-id="251d0-146">System.String</span></span>

## <span data-ttu-id="251d0-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="251d0-147">NOTES</span></span>

## <span data-ttu-id="251d0-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="251d0-148">RELATED LINKS</span></span>
