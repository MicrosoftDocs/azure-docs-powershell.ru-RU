---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 22eac04b24e8fec1778578f4e54792b5dcde6d1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569040"
---
# <span data-ttu-id="d7592-101">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d7592-101">Set-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="d7592-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d7592-102">SYNOPSIS</span></span>
<span data-ttu-id="d7592-103">Изменение учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d7592-103">Modifies a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7592-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d7592-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7592-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7592-105">DESCRIPTION</span></span>
<span data-ttu-id="d7592-106">Командлет **Set-AzureRmDataLakeStoreAccount** изменяет учетную запись Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d7592-106">The **Set-AzureRmDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="d7592-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d7592-107">EXAMPLES</span></span>

### <span data-ttu-id="d7592-108">Пример 1: Добавление тега для учетной записи</span><span class="sxs-lookup"><span data-stu-id="d7592-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="d7592-109">Эта команда добавляет указанный тег в учетную запись Data Lake Store с именем ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="d7592-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="d7592-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d7592-110">PARAMETERS</span></span>

### <span data-ttu-id="d7592-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="d7592-111">-AllowAzureIpState</span></span>
<span data-ttu-id="d7592-112">При необходимости разрешите или запретите в Azure IP-адреса, которые поступают через брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="d7592-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: FirewallAllowAzureIpsState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7592-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="d7592-113">-DefaultGroup</span></span>
<span data-ttu-id="d7592-114">Указывает идентификатор группы каталогов AzureActive.</span><span class="sxs-lookup"><span data-stu-id="d7592-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="d7592-115">Эта группа является группой по умолчанию для файлов и папок, которые вы создаете.</span><span class="sxs-lookup"><span data-stu-id="d7592-115">This group is the default group for files and folders that you create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7592-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7592-116">-DefaultProfile</span></span>
<span data-ttu-id="d7592-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d7592-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7592-118">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="d7592-118">-FirewallState</span></span>
<span data-ttu-id="d7592-119">При необходимости включите или отключите существующие правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="d7592-119">Optionally enable or disable existing firewall rules.</span></span>

```yaml
Type: FirewallState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7592-120">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="d7592-120">-KeyVersion</span></span>
<span data-ttu-id="d7592-121">Если тип шифрования назначен пользователю, пользователь может поворачивать его ключевую версию с помощью этого параметра.</span><span class="sxs-lookup"><span data-stu-id="d7592-121">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7592-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d7592-122">-Name</span></span>
<span data-ttu-id="d7592-123">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d7592-123">Specifies the name of a Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7592-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7592-124">-ResourceGroupName</span></span>
<span data-ttu-id="d7592-125">Указывает имя группы ресурсов, которая содержит учетную запись Data Lake Store, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="d7592-125">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7592-126">-Тег</span><span class="sxs-lookup"><span data-stu-id="d7592-126">-Tag</span></span>
<span data-ttu-id="d7592-127">Определяет теги как пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="d7592-127">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="d7592-128">Вы можете использовать теги для идентификации учетной записи Data Lake Store из других ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="d7592-128">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7592-129">Уровень</span><span class="sxs-lookup"><span data-stu-id="d7592-129">-Tier</span></span>
<span data-ttu-id="d7592-130">Требуемый уровень обязательства для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="d7592-130">The desired commitment tier for this account to use.</span></span>

```yaml
Type: TierType
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7592-131">-TrustedIdProviderState</span><span class="sxs-lookup"><span data-stu-id="d7592-131">-TrustedIdProviderState</span></span>
<span data-ttu-id="d7592-132">При необходимости включите или отключите существующих доверенных поставщиков УДОСТОВЕРЕНий.</span><span class="sxs-lookup"><span data-stu-id="d7592-132">Optionally enable or disable the existing trusted ID providers.</span></span>

```yaml
Type: TrustedIdProviderState
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7592-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7592-133">CommonParameters</span></span>
<span data-ttu-id="d7592-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d7592-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7592-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7592-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7592-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d7592-136">INPUTS</span></span>

### <span data-ttu-id="d7592-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="d7592-137">None</span></span>
<span data-ttu-id="d7592-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d7592-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d7592-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7592-139">OUTPUTS</span></span>

### <span data-ttu-id="d7592-140">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d7592-140">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="d7592-141">Обновленные сведения об учетной записи.</span><span class="sxs-lookup"><span data-stu-id="d7592-141">The updated account details.</span></span>

## <span data-ttu-id="d7592-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="d7592-142">NOTES</span></span>

## <span data-ttu-id="d7592-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7592-143">RELATED LINKS</span></span>

[<span data-ttu-id="d7592-144">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d7592-144">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="d7592-145">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d7592-145">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="d7592-146">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d7592-146">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="d7592-147">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d7592-147">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)

