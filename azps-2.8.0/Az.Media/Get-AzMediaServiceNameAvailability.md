---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: 8c62bf114feee8f9b87e2b7ca35b4c67b423ed66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720374"
---
# <span data-ttu-id="db6d0-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="db6d0-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="db6d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db6d0-102">SYNOPSIS</span></span>
<span data-ttu-id="db6d0-103">Проверяет, доступно ли имя службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="db6d0-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="db6d0-104">Имена служб мультимедиа глобально уникальны.</span><span class="sxs-lookup"><span data-stu-id="db6d0-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="db6d0-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db6d0-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="db6d0-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db6d0-106">DESCRIPTION</span></span>
<span data-ttu-id="db6d0-107">Командлет **Get-AzMediaServiceNameAvailability** проверяет, доступно ли имя службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="db6d0-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="db6d0-108">Имена служб мультимедиа глобально уникальны.</span><span class="sxs-lookup"><span data-stu-id="db6d0-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="db6d0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db6d0-109">EXAMPLES</span></span>

### <span data-ttu-id="db6d0-110">Пример 1: Проверка наличия имени службы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="db6d0-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="db6d0-111">Эта команда проверяет, доступно ли имя MediaService1.</span><span class="sxs-lookup"><span data-stu-id="db6d0-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="db6d0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db6d0-112">PARAMETERS</span></span>

### <span data-ttu-id="db6d0-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="db6d0-113">-AccountName</span></span>
<span data-ttu-id="db6d0-114">Указывает имя службы мультимедиа, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="db6d0-114">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db6d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db6d0-115">-DefaultProfile</span></span>
<span data-ttu-id="db6d0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="db6d0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db6d0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db6d0-117">CommonParameters</span></span>
<span data-ttu-id="db6d0-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db6d0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db6d0-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db6d0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db6d0-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db6d0-120">INPUTS</span></span>

### <span data-ttu-id="db6d0-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="db6d0-121">None</span></span>

## <span data-ttu-id="db6d0-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db6d0-122">OUTPUTS</span></span>

### <span data-ttu-id="db6d0-123">Microsoft. Azure. Commands. Media. Models. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="db6d0-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="db6d0-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="db6d0-124">NOTES</span></span>

## <span data-ttu-id="db6d0-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db6d0-125">RELATED LINKS</span></span>

[<span data-ttu-id="db6d0-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="db6d0-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="db6d0-127">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="db6d0-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="db6d0-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="db6d0-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="db6d0-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="db6d0-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)

