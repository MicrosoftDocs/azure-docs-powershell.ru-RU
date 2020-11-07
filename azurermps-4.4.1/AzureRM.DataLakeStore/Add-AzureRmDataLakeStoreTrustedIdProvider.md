---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 5C788778-58A4-4798-AB66-1D3562BB9338
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: f71fefdce069f1786125f8c65ba94d66fb67fa56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559839"
---
# <span data-ttu-id="2b3bf-101">Add-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="2b3bf-101">Add-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="2b3bf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2b3bf-102">SYNOPSIS</span></span>
<span data-ttu-id="2b3bf-103">Добавляет доверенный поставщик удостоверений в указанную учетную запись Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2b3bf-103">Adds a trusted identity provider to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b3bf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2b3bf-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [-Name] <String> [-ProviderEndpoint] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b3bf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b3bf-105">DESCRIPTION</span></span>
<span data-ttu-id="2b3bf-106">Командлет **Add-AzureRmDataLakeStoreTrustedIdProvider** добавляет доверенный поставщик удостоверений в указанную учетную запись Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2b3bf-106">The **Add-AzureRmDataLakeStoreTrustedIdProvider** cmdlet adds a trusted identity provider to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="2b3bf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2b3bf-107">EXAMPLES</span></span>

### <span data-ttu-id="2b3bf-108">Пример 1: Добавление надежного поставщика удостоверений</span><span class="sxs-lookup"><span data-stu-id="2b3bf-108">Example 1: Add a trusted identity provider</span></span>
```
PS C:\> Add-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider -ProviderEndpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"
```

<span data-ttu-id="2b3bf-109">Добавляет поставщика "MyProvider" для учетной записи "ContosoADL" с конечной точкой поставщика " https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150 "</span><span class="sxs-lookup"><span data-stu-id="2b3bf-109">Adds the provider "MyProvider" to account "ContosoADL" with the provider endpoint "https://sts.windows.net/6b04908c-b91f-40ce-8024-7ee8a4fd6150"</span></span>

## <span data-ttu-id="2b3bf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2b3bf-110">PARAMETERS</span></span>

### <span data-ttu-id="2b3bf-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="2b3bf-111">-Account</span></span>
<span data-ttu-id="2b3bf-112">Имя учетной записи Data Lake Store, в которую нужно добавить указанного доверенного поставщика удостоверений.</span><span class="sxs-lookup"><span data-stu-id="2b3bf-112">The name of the Data Lake Store account to add the specified trusted identity provider to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b3bf-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2b3bf-113">-Name</span></span>
<span data-ttu-id="2b3bf-114">Имя доверенного поставщика удостоверений, который нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="2b3bf-114">The name of the trusted identity provider to add</span></span>

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

### <span data-ttu-id="2b3bf-115">-ProviderEndpoint</span><span class="sxs-lookup"><span data-stu-id="2b3bf-115">-ProviderEndpoint</span></span>
<span data-ttu-id="2b3bf-116">Правильная конечная точка доверенного поставщика в https://sts.windows.net/ формате: \<provider identity\></span><span class="sxs-lookup"><span data-stu-id="2b3bf-116">The valid trusted provider endpoint in the format: https://sts.windows.net/\<provider identity\>"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b3bf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b3bf-117">-ResourceGroupName</span></span>
<span data-ttu-id="2b3bf-118">Имя группы ресурсов, под которой учетная запись добавляет доверенный поставщик удостоверений.</span><span class="sxs-lookup"><span data-stu-id="2b3bf-118">Name of resource group under which the account to add the trusted identity provider is.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b3bf-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b3bf-119">-Confirm</span></span>
<span data-ttu-id="2b3bf-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2b3bf-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3bf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b3bf-121">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3bf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b3bf-122">-DefaultProfile</span></span>
<span data-ttu-id="2b3bf-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b3bf-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b3bf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b3bf-124">CommonParameters</span></span>
<span data-ttu-id="2b3bf-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2b3bf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b3bf-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b3bf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b3bf-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2b3bf-127">INPUTS</span></span>

## <span data-ttu-id="2b3bf-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b3bf-128">OUTPUTS</span></span>

### <span data-ttu-id="2b3bf-129">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="2b3bf-129">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="2b3bf-130">Добавленный доверенный поставщик удостоверений.</span><span class="sxs-lookup"><span data-stu-id="2b3bf-130">The added Trusted Identity Provider.</span></span>

## <span data-ttu-id="2b3bf-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="2b3bf-131">NOTES</span></span>

## <span data-ttu-id="2b3bf-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b3bf-132">RELATED LINKS</span></span>
