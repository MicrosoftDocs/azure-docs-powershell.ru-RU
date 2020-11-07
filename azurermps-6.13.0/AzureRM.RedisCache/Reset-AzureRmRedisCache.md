---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/reset-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
ms.openlocfilehash: 8aad14bde950a5e98d8d9331428a62e957cb0afe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568416"
---
# <span data-ttu-id="29cc5-101">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="29cc5-101">Reset-AzureRmRedisCache</span></span>

## <span data-ttu-id="29cc5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="29cc5-102">SYNOPSIS</span></span>
<span data-ttu-id="29cc5-103">Перезапускает узлы кэша.</span><span class="sxs-lookup"><span data-stu-id="29cc5-103">Restarts nodes of a cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29cc5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="29cc5-104">SYNTAX</span></span>

```
Reset-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29cc5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29cc5-105">DESCRIPTION</span></span>
<span data-ttu-id="29cc5-106">Командлет **Reset-AzureRmRedisCache** перезапустит узлы экземпляра кэша Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="29cc5-106">The **Reset-AzureRmRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="29cc5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="29cc5-107">EXAMPLES</span></span>

### <span data-ttu-id="29cc5-108">Пример 1: перезапуск обоих узлов</span><span class="sxs-lookup"><span data-stu-id="29cc5-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="29cc5-109">Эта команда перезапустит оба узла для кэша с именем RedisCache06.</span><span class="sxs-lookup"><span data-stu-id="29cc5-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="29cc5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="29cc5-110">PARAMETERS</span></span>

### <span data-ttu-id="29cc5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29cc5-111">-DefaultProfile</span></span>
<span data-ttu-id="29cc5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="29cc5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29cc5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="29cc5-113">-Force</span></span>
<span data-ttu-id="29cc5-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="29cc5-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="29cc5-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="29cc5-115">-Name</span></span>
<span data-ttu-id="29cc5-116">Указывает имя кэша.</span><span class="sxs-lookup"><span data-stu-id="29cc5-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="29cc5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29cc5-117">-PassThru</span></span>
<span data-ttu-id="29cc5-118">Указывает на то, что этот командлет возвращает логическое значение, которое указывает, успешно ли выполняется операция.</span><span class="sxs-lookup"><span data-stu-id="29cc5-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="29cc5-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="29cc5-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="29cc5-120">-RebootType</span><span class="sxs-lookup"><span data-stu-id="29cc5-120">-RebootType</span></span>
<span data-ttu-id="29cc5-121">Указывает, какой узел или узлы нужно перезапустить.</span><span class="sxs-lookup"><span data-stu-id="29cc5-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="29cc5-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="29cc5-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="29cc5-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="29cc5-123">PrimaryNode</span></span> 
- <span data-ttu-id="29cc5-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="29cc5-124">SecondaryNode</span></span> 
- <span data-ttu-id="29cc5-125">AllNodes</span><span class="sxs-lookup"><span data-stu-id="29cc5-125">AllNodes</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryNode, SecondaryNode, AllNodes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29cc5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29cc5-126">-ResourceGroupName</span></span>
<span data-ttu-id="29cc5-127">Указывает имя группы ресурсов, содержащей кэш.</span><span class="sxs-lookup"><span data-stu-id="29cc5-127">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29cc5-128">-ShardId</span><span class="sxs-lookup"><span data-stu-id="29cc5-128">-ShardId</span></span>
<span data-ttu-id="29cc5-129">Указывает идентификатор сегмента, который перезапускает этот командлет для расширенного кэша с включенной кластеризацией.</span><span class="sxs-lookup"><span data-stu-id="29cc5-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29cc5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29cc5-130">-Confirm</span></span>
<span data-ttu-id="29cc5-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="29cc5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29cc5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29cc5-132">-WhatIf</span></span>
<span data-ttu-id="29cc5-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="29cc5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29cc5-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="29cc5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29cc5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29cc5-135">CommonParameters</span></span>
<span data-ttu-id="29cc5-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="29cc5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29cc5-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29cc5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29cc5-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="29cc5-138">INPUTS</span></span>

### <span data-ttu-id="29cc5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="29cc5-139">System.String</span></span>

### <span data-ttu-id="29cc5-140">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="29cc5-140">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="29cc5-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="29cc5-141">OUTPUTS</span></span>

### <span data-ttu-id="29cc5-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="29cc5-142">System.Boolean</span></span>

## <span data-ttu-id="29cc5-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="29cc5-143">NOTES</span></span>
* <span data-ttu-id="29cc5-144">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Redis, кэш, Интернет, webapp, веб-сайт</span><span class="sxs-lookup"><span data-stu-id="29cc5-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="29cc5-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29cc5-145">RELATED LINKS</span></span>

[<span data-ttu-id="29cc5-146">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="29cc5-146">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="29cc5-147">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="29cc5-147">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="29cc5-148">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="29cc5-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="29cc5-149">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="29cc5-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="29cc5-150">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="29cc5-150">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)

