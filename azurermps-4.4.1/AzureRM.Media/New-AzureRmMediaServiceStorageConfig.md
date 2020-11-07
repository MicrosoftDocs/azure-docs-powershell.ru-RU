---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaServiceStorageConfig.md
ms.openlocfilehash: 236486af937a99812f4979ed4db089002fb9ad30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567114"
---
# <span data-ttu-id="7aa96-101">New-AzureRmMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="7aa96-101">New-AzureRmMediaServiceStorageConfig</span></span>

## <span data-ttu-id="7aa96-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7aa96-102">SYNOPSIS</span></span>
<span data-ttu-id="7aa96-103">Создайте конфигурацию учетной записи хранения для командлетов службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7aa96-103">Create a storage account configuration for the media service cmdlets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7aa96-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7aa96-104">SYNTAX</span></span>

```
New-AzureRmMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7aa96-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7aa96-105">DESCRIPTION</span></span>
<span data-ttu-id="7aa96-106">Командлет **New-AzureRmMediaServiceStorageConfig** создает конфигурацию учетной записи хранения для командлетов службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7aa96-106">The **New-AzureRmMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="7aa96-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7aa96-107">EXAMPLES</span></span>

### <span data-ttu-id="7aa96-108">Пример 1: создание конфигурации учетной записи хранения для командлетов службы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="7aa96-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="7aa96-109">Первая команда создает объект учетной записи хранения с помощью командлета **New-AzureRmStorageAccount** .</span><span class="sxs-lookup"><span data-stu-id="7aa96-109">The first command creates a storage account object by using **the New-AzureRmStorageAccount** cmdlet.</span></span>
<span data-ttu-id="7aa96-110">Команда называет эту учетную запись хранения Storage1 и тип с именем Standard_GRS и сохраняет результат в переменной с именем $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="7aa96-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>

<span data-ttu-id="7aa96-111">Вторая команда создает объект конфигурации хранилища в качестве основной учетной записи хранилища, связанной со службой мультимедиа, с помощью ИДЕНТИФИКАЦИОНных данных учетной записи хранения, сохраненных в переменной $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="7aa96-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="7aa96-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7aa96-112">PARAMETERS</span></span>

### <span data-ttu-id="7aa96-113">-Primary</span><span class="sxs-lookup"><span data-stu-id="7aa96-113">-IsPrimary</span></span>
<span data-ttu-id="7aa96-114">Указывает на то, что командлет создает учетную запись хранения в качестве основного хранилища для службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7aa96-114">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aa96-115">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7aa96-115">-StorageAccountId</span></span>
<span data-ttu-id="7aa96-116">Указывает идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7aa96-116">Specifies the ID of the storage account.</span></span>

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

### <span data-ttu-id="7aa96-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7aa96-117">-Confirm</span></span>
<span data-ttu-id="7aa96-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7aa96-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aa96-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7aa96-119">-WhatIf</span></span>
<span data-ttu-id="7aa96-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7aa96-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7aa96-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7aa96-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aa96-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aa96-122">-DefaultProfile</span></span>
<span data-ttu-id="7aa96-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7aa96-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7aa96-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aa96-124">CommonParameters</span></span>
<span data-ttu-id="7aa96-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7aa96-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aa96-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7aa96-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aa96-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7aa96-127">INPUTS</span></span>

## <span data-ttu-id="7aa96-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7aa96-128">OUTPUTS</span></span>

### <span data-ttu-id="7aa96-129">Microsoft. Azure. Commands. Media. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7aa96-129">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="7aa96-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="7aa96-130">NOTES</span></span>

## <span data-ttu-id="7aa96-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7aa96-131">RELATED LINKS</span></span>

[<span data-ttu-id="7aa96-132">Sync (синхронизация) — AzureRmMediaServiceStorageKeys</span><span class="sxs-lookup"><span data-stu-id="7aa96-132">Sync-AzureRmMediaServiceStorageKeys</span></span>](./Sync-AzureRmMediaServiceStorageKeys.md)

