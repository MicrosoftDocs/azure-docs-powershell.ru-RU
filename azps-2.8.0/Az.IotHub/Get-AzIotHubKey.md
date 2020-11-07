---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: c38965a99dfc152f76e606c05802009b9b14faf9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720746"
---
# <span data-ttu-id="c61fd-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="c61fd-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="c61fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c61fd-102">SYNOPSIS</span></span>
<span data-ttu-id="c61fd-103">Возвращает IotHub клавишу.</span><span class="sxs-lookup"><span data-stu-id="c61fd-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="c61fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c61fd-104">SYNTAX</span></span>

### <span data-ttu-id="c61fd-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c61fd-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c61fd-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c61fd-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c61fd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c61fd-107">DESCRIPTION</span></span>
<span data-ttu-id="c61fd-108">Возвращает IotHub клавишу.</span><span class="sxs-lookup"><span data-stu-id="c61fd-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="c61fd-109">Вы можете либо вывести список всех ключей, либо отфильтровать список по определенному названию ключа.</span><span class="sxs-lookup"><span data-stu-id="c61fd-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="c61fd-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c61fd-110">EXAMPLES</span></span>

### <span data-ttu-id="c61fd-111">Пример 1 получить все клавиши</span><span class="sxs-lookup"><span data-stu-id="c61fd-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="c61fd-112">Возвращает все клавиши для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="c61fd-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="c61fd-113">Пример 2 получение сведений о конкретном ключе</span><span class="sxs-lookup"><span data-stu-id="c61fd-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="c61fd-114">Получает сведения для ключа с именем "iothubowner" для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="c61fd-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="c61fd-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c61fd-115">PARAMETERS</span></span>

### <span data-ttu-id="c61fd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c61fd-116">-DefaultProfile</span></span>
<span data-ttu-id="c61fd-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c61fd-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c61fd-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="c61fd-118">-HubId</span></span>
<span data-ttu-id="c61fd-119">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="c61fd-119">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c61fd-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="c61fd-120">-KeyName</span></span>
<span data-ttu-id="c61fd-121">Имя ключа</span><span class="sxs-lookup"><span data-stu-id="c61fd-121">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c61fd-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c61fd-122">-Name</span></span>
<span data-ttu-id="c61fd-123">Имя центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="c61fd-123">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c61fd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c61fd-124">-ResourceGroupName</span></span>
<span data-ttu-id="c61fd-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c61fd-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c61fd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c61fd-126">CommonParameters</span></span>
<span data-ttu-id="c61fd-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c61fd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c61fd-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c61fd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c61fd-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c61fd-129">INPUTS</span></span>

### <span data-ttu-id="c61fd-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c61fd-130">System.String</span></span>

## <span data-ttu-id="c61fd-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c61fd-131">OUTPUTS</span></span>

### <span data-ttu-id="c61fd-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c61fd-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="c61fd-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="c61fd-133">NOTES</span></span>

## <span data-ttu-id="c61fd-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c61fd-134">RELATED LINKS</span></span>