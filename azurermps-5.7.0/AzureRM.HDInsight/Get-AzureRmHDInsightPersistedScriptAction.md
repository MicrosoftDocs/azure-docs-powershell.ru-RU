---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: c70b4fecc9be5937d24ca4bc84b8aa6554daf482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569983"
---
# <span data-ttu-id="2cb26-101">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="2cb26-101">Get-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="2cb26-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2cb26-102">SYNOPSIS</span></span>
<span data-ttu-id="2cb26-103">Получает хранимые действия сценария для кластера и перечисляет их в хронологическом порядке или получает сведения о указанном сохраненном действии сценария.</span><span class="sxs-lookup"><span data-stu-id="2cb26-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cb26-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2cb26-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cb26-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cb26-105">DESCRIPTION</span></span>
<span data-ttu-id="2cb26-106">Командлет **Get-AzureRmHDInsightPersistedScriptAction** получает хранимые действия сценария для кластера HDInsight Azure и перечисляет их в хронологическом порядке или получает сведения о указанном сохраненном действии сценария.</span><span class="sxs-lookup"><span data-stu-id="2cb26-106">The **Get-AzureRmHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="2cb26-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2cb26-107">EXAMPLES</span></span>

### <span data-ttu-id="2cb26-108">Пример 1: Получение сохраненных действий сценария в кластере</span><span class="sxs-lookup"><span data-stu-id="2cb26-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="2cb26-109">Эта команда получает хранимые действия сценария в кластере с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="2cb26-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="2cb26-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2cb26-110">PARAMETERS</span></span>

### <span data-ttu-id="2cb26-111">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="2cb26-111">-ClusterName</span></span>
<span data-ttu-id="2cb26-112">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="2cb26-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb26-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cb26-113">-DefaultProfile</span></span>
<span data-ttu-id="2cb26-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2cb26-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2cb26-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2cb26-115">-Name</span></span>
<span data-ttu-id="2cb26-116">Указывает имя сохраненного действия сценария.</span><span class="sxs-lookup"><span data-stu-id="2cb26-116">Specifies the name of the persisted script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb26-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cb26-117">-ResourceGroupName</span></span>
<span data-ttu-id="2cb26-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2cb26-118">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cb26-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cb26-119">CommonParameters</span></span>
<span data-ttu-id="2cb26-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2cb26-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cb26-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cb26-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cb26-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2cb26-122">INPUTS</span></span>

### <span data-ttu-id="2cb26-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="2cb26-123">None</span></span>
<span data-ttu-id="2cb26-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="2cb26-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2cb26-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cb26-125">OUTPUTS</span></span>

### <span data-ttu-id="2cb26-126">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. HDInsight. AzureHDInsightRuntimeScriptAction]</span><span class="sxs-lookup"><span data-stu-id="2cb26-126">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction]</span></span>

## <span data-ttu-id="2cb26-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="2cb26-127">NOTES</span></span>

## <span data-ttu-id="2cb26-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2cb26-128">RELATED LINKS</span></span>

[<span data-ttu-id="2cb26-129">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="2cb26-129">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="2cb26-130">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="2cb26-130">Set-AzureRmHDInsightPersistedScriptAction</span></span>](./Set-AzureRmHDInsightPersistedScriptAction.md)

