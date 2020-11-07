---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
ms.openlocfilehash: 0754bd515a846f8524bc7fd9826d36d19d79843a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721277"
---
# <span data-ttu-id="dcece-101">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dcece-101">Set-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="dcece-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dcece-102">SYNOPSIS</span></span>
<span data-ttu-id="dcece-103">Изменение учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="dcece-103">Modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="dcece-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dcece-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcece-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcece-105">DESCRIPTION</span></span>
<span data-ttu-id="dcece-106">Командлет **Set-AzDataLakeStoreAccount** изменяет учетную запись Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="dcece-106">The **Set-AzDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="dcece-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dcece-107">EXAMPLES</span></span>

### <span data-ttu-id="dcece-108">Пример 1: Добавление тега для учетной записи</span><span class="sxs-lookup"><span data-stu-id="dcece-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="dcece-109">Эта команда добавляет указанный тег в учетную запись Data Lake Store с именем ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="dcece-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="dcece-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dcece-110">PARAMETERS</span></span>

### <span data-ttu-id="dcece-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="dcece-111">-AllowAzureIpState</span></span>
<span data-ttu-id="dcece-112">При необходимости разрешите или запретите в Azure IP-адреса, которые поступают через брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="dcece-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcece-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="dcece-113">-DefaultGroup</span></span>
<span data-ttu-id="dcece-114">Указывает идентификатор группы каталогов AzureActive.</span><span class="sxs-lookup"><span data-stu-id="dcece-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="dcece-115">Эта группа является группой по умолчанию для файлов и папок, которые вы создаете.</span><span class="sxs-lookup"><span data-stu-id="dcece-115">This group is the default group for files and folders that you create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcece-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcece-116">-DefaultProfile</span></span>
<span data-ttu-id="dcece-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dcece-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dcece-118">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="dcece-118">-FirewallState</span></span>
<span data-ttu-id="dcece-119">При необходимости включите или отключите существующие правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="dcece-119">Optionally enable or disable existing firewall rules.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcece-120">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="dcece-120">-KeyVersion</span></span>
<span data-ttu-id="dcece-121">Если тип шифрования назначен пользователю, пользователь может поворачивать его ключевую версию с помощью этого параметра.</span><span class="sxs-lookup"><span data-stu-id="dcece-121">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

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

### <span data-ttu-id="dcece-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dcece-122">-Name</span></span>
<span data-ttu-id="dcece-123">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="dcece-123">Specifies the name of a Data Lake Store account.</span></span>

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

### <span data-ttu-id="dcece-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcece-124">-ResourceGroupName</span></span>
<span data-ttu-id="dcece-125">Указывает имя группы ресурсов, которая содержит учетную запись Data Lake Store, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="dcece-125">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

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

### <span data-ttu-id="dcece-126">-Тег</span><span class="sxs-lookup"><span data-stu-id="dcece-126">-Tag</span></span>
<span data-ttu-id="dcece-127">Определяет теги как пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="dcece-127">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="dcece-128">Вы можете использовать теги для идентификации учетной записи Data Lake Store из других ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="dcece-128">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcece-129">Уровень</span><span class="sxs-lookup"><span data-stu-id="dcece-129">-Tier</span></span>
<span data-ttu-id="dcece-130">Требуемый уровень обязательства для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="dcece-130">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcece-131">-TrustedIdProviderState</span><span class="sxs-lookup"><span data-stu-id="dcece-131">-TrustedIdProviderState</span></span>
<span data-ttu-id="dcece-132">При необходимости включите или отключите существующих доверенных поставщиков УДОСТОВЕРЕНий.</span><span class="sxs-lookup"><span data-stu-id="dcece-132">Optionally enable or disable the existing trusted ID providers.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcece-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcece-133">CommonParameters</span></span>
<span data-ttu-id="dcece-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dcece-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcece-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcece-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcece-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dcece-136">INPUTS</span></span>

### <span data-ttu-id="dcece-137">System. String</span><span class="sxs-lookup"><span data-stu-id="dcece-137">System.String</span></span>

### <span data-ttu-id="dcece-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dcece-138">System.Collections.Hashtable</span></span>

### <span data-ttu-id="dcece-139">System. Nullable "1 [[Microsoft. Azure. Management. DataStore. Store. TrustedIdProviderState, Microsoft. Azure. Management. DataStore. Store, Version = 2.0.0.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="dcece-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="dcece-140">System. Nullable "1 [[Microsoft. Azure. Management. DataStore. Store. FirewallState, Microsoft. Azure. Management. DataStore. Store, Version = 2.0.0.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="dcece-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="dcece-141">System. Nullable "1 [[Microsoft. Azure. Management. DataStore. Store. TierType, Microsoft. Azure. Management. DataStore. Store, Version = 2.0.0.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="dcece-141">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="dcece-142">System. Nullable "1 [[Microsoft. Azure. Management. DataStore. Store. FirewallAllowAzureIpsState, Microsoft. Azure. Management. DataStore. Store, Version = 2.0.0.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="dcece-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="dcece-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcece-143">OUTPUTS</span></span>

### <span data-ttu-id="dcece-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dcece-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="dcece-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="dcece-145">NOTES</span></span>

## <span data-ttu-id="dcece-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dcece-146">RELATED LINKS</span></span>

[<span data-ttu-id="dcece-147">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dcece-147">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="dcece-148">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dcece-148">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="dcece-149">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dcece-149">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="dcece-150">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dcece-150">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)

