---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85b62b8ffbdcdcefff5bbb5c984a19ef0b7cb644
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555695"
---
# <span data-ttu-id="0c70d-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="0c70d-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="0c70d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0c70d-102">SYNOPSIS</span></span>
<span data-ttu-id="0c70d-103">Удаление существующей квоты</span><span class="sxs-lookup"><span data-stu-id="0c70d-103">Delete an existing quota</span></span>

## <span data-ttu-id="0c70d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0c70d-104">SYNTAX</span></span>

### <span data-ttu-id="0c70d-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0c70d-105">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c70d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c70d-106">ResourceId</span></span>
```
Remove-AzsStorageQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c70d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c70d-107">DESCRIPTION</span></span>
<span data-ttu-id="0c70d-108">Удаление существующей квоты</span><span class="sxs-lookup"><span data-stu-id="0c70d-108">Delete an existing quota</span></span>

## <span data-ttu-id="0c70d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0c70d-109">EXAMPLES</span></span>

### <span data-ttu-id="0c70d-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0c70d-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsStorageQuota -Name 'TestDeleteStorageQuota'
```

<span data-ttu-id="0c70d-111">Удалите квоту хранилища по имени.</span><span class="sxs-lookup"><span data-stu-id="0c70d-111">Remove a storage quota by name.</span></span>

### <span data-ttu-id="0c70d-112">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="0c70d-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageQuota -Name 'testquota' | Remove-AzsStorageQuota
```

<span data-ttu-id="0c70d-113">Удалите квоту хранилища посредством конвейера.</span><span class="sxs-lookup"><span data-stu-id="0c70d-113">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="0c70d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0c70d-114">PARAMETERS</span></span>

### <span data-ttu-id="0c70d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0c70d-115">-Force</span></span>
<span data-ttu-id="0c70d-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="0c70d-116">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c70d-117">-Location</span><span class="sxs-lookup"><span data-stu-id="0c70d-117">-Location</span></span>
<span data-ttu-id="0c70d-118">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="0c70d-118">Resource location.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c70d-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0c70d-119">-Name</span></span>
<span data-ttu-id="0c70d-120">Имя квоты хранилища.</span><span class="sxs-lookup"><span data-stu-id="0c70d-120">The name of the storage quota.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c70d-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c70d-121">-ResourceId</span></span>
<span data-ttu-id="0c70d-122">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="0c70d-122">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c70d-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c70d-123">-Confirm</span></span>
<span data-ttu-id="0c70d-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0c70d-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c70d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c70d-125">-WhatIf</span></span>
<span data-ttu-id="0c70d-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0c70d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c70d-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0c70d-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c70d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c70d-128">CommonParameters</span></span>
<span data-ttu-id="0c70d-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0c70d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c70d-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c70d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c70d-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0c70d-131">INPUTS</span></span>

## <span data-ttu-id="0c70d-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c70d-132">OUTPUTS</span></span>

## <span data-ttu-id="0c70d-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="0c70d-133">NOTES</span></span>

## <span data-ttu-id="0c70d-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c70d-134">RELATED LINKS</span></span>
