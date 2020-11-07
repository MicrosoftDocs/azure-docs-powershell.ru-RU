---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 11a8ffe26a65bf2ecabab7807d8e54bc23b629fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556255"
---
# <span data-ttu-id="d5a6f-101">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="d5a6f-101">Get-AzureStorageQueue</span></span>

## <span data-ttu-id="d5a6f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d5a6f-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a6f-103">Выводит список очередей хранилища.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-103">Lists storage queues.</span></span>

## <span data-ttu-id="d5a6f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d5a6f-104">SYNTAX</span></span>

### <span data-ttu-id="d5a6f-105">QueueName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d5a6f-105">QueueName (Default)</span></span>
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="d5a6f-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="d5a6f-106">QueuePrefix</span></span>
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="d5a6f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5a6f-107">DESCRIPTION</span></span>
<span data-ttu-id="d5a6f-108">Командлет **Get-AzureStorageQueue** перечисляет очереди хранения, связанные с учетной записью хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-108">The **Get-AzureStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="d5a6f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d5a6f-109">EXAMPLES</span></span>

### <span data-ttu-id="d5a6f-110">Пример 1: список всех очередей хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="d5a6f-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue
```

<span data-ttu-id="d5a6f-111">Эта команда возвращает список всех очередей хранилища для текущей учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="d5a6f-112">Пример 2: список очередей хранилища Azure с использованием подстановочных знаков</span><span class="sxs-lookup"><span data-stu-id="d5a6f-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

<span data-ttu-id="d5a6f-113">Эта команда использует подстановочный знак для получения списка очередей хранилища, имя которого начинается с очереди.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="d5a6f-114">Пример 3: список очередей хранилища Azure с использованием префикса имени очереди</span><span class="sxs-lookup"><span data-stu-id="d5a6f-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

<span data-ttu-id="d5a6f-115">В этом примере используется параметр *prefix* для получения списка очередей хранилища, имена которых начинаются с очереди.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="d5a6f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d5a6f-116">PARAMETERS</span></span>

### <span data-ttu-id="d5a6f-117">-Context</span><span class="sxs-lookup"><span data-stu-id="d5a6f-117">-Context</span></span>
<span data-ttu-id="d5a6f-118">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="d5a6f-119">Вы можете создать его с помощью командлета **New-AzureStorageContext** .</span><span class="sxs-lookup"><span data-stu-id="d5a6f-119">You can create it by using the **New-AzureStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="d5a6f-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d5a6f-120">-Name</span></span>
<span data-ttu-id="d5a6f-121">Задает имя.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-121">Specifies a name.</span></span>
<span data-ttu-id="d5a6f-122">Если имя не указано, командлет возвращает список всех очередей.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-122">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="d5a6f-123">Если указано полное или частичное имя, командлет получает все очереди, соответствующие шаблону имени.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-123">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

```yaml
Type: String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a6f-124">-Prefix (префикс)</span><span class="sxs-lookup"><span data-stu-id="d5a6f-124">-Prefix</span></span>
<span data-ttu-id="d5a6f-125">Задает префикс, используемый в именах очередей, которые вы хотите получить.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-125">Specifies a prefix used in the name of the queues you want to get.</span></span>

```yaml
Type: String
Parameter Sets: QueuePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a6f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a6f-126">CommonParameters</span></span>
<span data-ttu-id="d5a6f-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a6f-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5a6f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a6f-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d5a6f-129">INPUTS</span></span>

## <span data-ttu-id="d5a6f-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5a6f-130">OUTPUTS</span></span>

## <span data-ttu-id="d5a6f-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="d5a6f-131">NOTES</span></span>

## <span data-ttu-id="d5a6f-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5a6f-132">RELATED LINKS</span></span>

[<span data-ttu-id="d5a6f-133">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="d5a6f-133">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)

[<span data-ttu-id="d5a6f-134">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="d5a6f-134">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)

