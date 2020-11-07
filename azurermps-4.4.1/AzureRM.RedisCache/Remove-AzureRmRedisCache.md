---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
ms.openlocfilehash: a9a879386bdbc22eef3094e2f1d0cf19cd42cc45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559564"
---
# <span data-ttu-id="d0f50-101">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d0f50-101">Remove-AzureRmRedisCache</span></span>

## <span data-ttu-id="d0f50-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d0f50-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f50-103">Удаление кэша Redis.</span><span class="sxs-lookup"><span data-stu-id="d0f50-103">Removes a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0f50-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d0f50-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0f50-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0f50-105">DESCRIPTION</span></span>
<span data-ttu-id="d0f50-106">Командлет **Remove-AzureRmRedisCache** удаляет кэш Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="d0f50-106">The **Remove-AzureRmRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="d0f50-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d0f50-107">EXAMPLES</span></span>

### <span data-ttu-id="d0f50-108">Пример 1: Удаление кэша Redis и возврат результата</span><span class="sxs-lookup"><span data-stu-id="d0f50-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="d0f50-109">Эта команда удаляет кэш Redis и показывает, успешно ли выполнена операция.</span><span class="sxs-lookup"><span data-stu-id="d0f50-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="d0f50-110">Пример 2: Удаление кэша Redis и не отображение результата</span><span class="sxs-lookup"><span data-stu-id="d0f50-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="d0f50-111">Эта команда удаляет кэш Redis.</span><span class="sxs-lookup"><span data-stu-id="d0f50-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="d0f50-112">Так как параметр *PassThru* не указан, результат операции не отображается.</span><span class="sxs-lookup"><span data-stu-id="d0f50-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="d0f50-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d0f50-113">PARAMETERS</span></span>

### <span data-ttu-id="d0f50-114">-Force</span><span class="sxs-lookup"><span data-stu-id="d0f50-114">-Force</span></span>
<span data-ttu-id="d0f50-115">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="d0f50-115">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f50-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d0f50-116">-Name</span></span>
<span data-ttu-id="d0f50-117">Указывает имя кэша Redis, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d0f50-117">Specifies the name of the Redis Cache to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0f50-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0f50-118">-PassThru</span></span>
<span data-ttu-id="d0f50-119">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="d0f50-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d0f50-120">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d0f50-120">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f50-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0f50-121">-ResourceGroupName</span></span>
<span data-ttu-id="d0f50-122">Указывает имя группы ресурсов, содержащей кэш Redis, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d0f50-122">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0f50-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0f50-123">-Confirm</span></span>
<span data-ttu-id="d0f50-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d0f50-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0f50-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0f50-125">-WhatIf</span></span>
<span data-ttu-id="d0f50-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d0f50-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0f50-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d0f50-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0f50-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0f50-128">-DefaultProfile</span></span>
<span data-ttu-id="d0f50-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d0f50-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0f50-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f50-130">CommonParameters</span></span>
<span data-ttu-id="d0f50-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d0f50-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f50-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0f50-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0f50-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d0f50-133">INPUTS</span></span>

### <span data-ttu-id="d0f50-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="d0f50-134">None</span></span>
<span data-ttu-id="d0f50-135">Вы можете передавать входные данные командлету по имени, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="d0f50-135">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="d0f50-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0f50-136">OUTPUTS</span></span>

### <span data-ttu-id="d0f50-137">Значением</span><span class="sxs-lookup"><span data-stu-id="d0f50-137">Boolean</span></span>
<span data-ttu-id="d0f50-138">Возвращает $True, если не возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="d0f50-138">Returns $True if no exception occurs.</span></span>

## <span data-ttu-id="d0f50-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="d0f50-139">NOTES</span></span>

## <span data-ttu-id="d0f50-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0f50-140">RELATED LINKS</span></span>

[<span data-ttu-id="d0f50-141">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d0f50-141">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="d0f50-142">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d0f50-142">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="d0f50-143">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="d0f50-143">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)

