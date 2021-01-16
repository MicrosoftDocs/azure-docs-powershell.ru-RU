---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
ms.openlocfilehash: 64677ac73fecbaeaaaa327f21bc8e67e2a933d97
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325502"
---
# <span data-ttu-id="8ac67-101">Invoke-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="8ac67-101">Invoke-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="8ac67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ac67-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac67-103">Вызывает спарк-отчет Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="8ac67-103">Invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="8ac67-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8ac67-104">SYNTAX</span></span>

### <span data-ttu-id="8ac67-105">RunSparkStatementByCodePathParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8ac67-105">RunSparkStatementByCodePathParameterSet (Default)</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ac67-106">RunSparkStatementByCodeParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ac67-106">RunSparkStatementByCodeParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ac67-107">RunSparkStatementByCodeAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ac67-107">RunSparkStatementByCodeAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ac67-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ac67-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ac67-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ac67-109">DESCRIPTION</span></span>
<span data-ttu-id="8ac67-110">**Спарклет Invoke-AzSynapseSparkStatement** вызывает спарк-отчет Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="8ac67-110">The **Invoke-AzSynapseSparkStatement** cmdlet invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="8ac67-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8ac67-111">EXAMPLES</span></span>

### <span data-ttu-id="8ac67-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8ac67-112">Example 1</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="8ac67-113">Эти команды запускают сеанс спарклайнов, а затем вызовют в конвейере спарк-линию с помощью inline Spark.</span><span class="sxs-lookup"><span data-stu-id="8ac67-113">These commands start a Spark session then invoke an inline Spark statement through pipeline.</span></span>

### <span data-ttu-id="8ac67-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8ac67-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSynapseSparkStatement -SessionId 324 -Language 'Spark' -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="8ac67-115">Эти команды запускают сеанс спарклайнов, а затем вызывают в них спарк-заявление.</span><span class="sxs-lookup"><span data-stu-id="8ac67-115">These commands start a Spark session then invoke an inline Spark statement.</span></span>

### <span data-ttu-id="8ac67-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8ac67-116">Example 3</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -FilePath C:\path\to\code.sc
```

<span data-ttu-id="8ac67-117">Эти команды запускают сеанс спарк-спарков, а затем вызывают в файле спарк-отчеты.</span><span class="sxs-lookup"><span data-stu-id="8ac67-117">These commands start a Spark session then invoke Spark statements in a file.</span></span>

## <span data-ttu-id="8ac67-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ac67-118">PARAMETERS</span></span>

### <span data-ttu-id="8ac67-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ac67-119">-AsJob</span></span>
<span data-ttu-id="8ac67-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8ac67-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8ac67-121">-Code</span><span class="sxs-lookup"><span data-stu-id="8ac67-121">-Code</span></span>
<span data-ttu-id="8ac67-122">Код выполнения.</span><span class="sxs-lookup"><span data-stu-id="8ac67-122">The execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodeParameterSet, RunSparkStatementByCodeAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac67-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ac67-123">-DefaultProfile</span></span>
<span data-ttu-id="8ac67-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ac67-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ac67-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="8ac67-125">-FilePath</span></span>
<span data-ttu-id="8ac67-126">Путь к локальному файлу, содержащий код выполнения.</span><span class="sxs-lookup"><span data-stu-id="8ac67-126">Specifies a local file path that contains the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac67-127">-Language</span><span class="sxs-lookup"><span data-stu-id="8ac67-127">-Language</span></span>
<span data-ttu-id="8ac67-128">Язык кода выполнения.</span><span class="sxs-lookup"><span data-stu-id="8ac67-128">Language of the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac67-129">-Response</span><span class="sxs-lookup"><span data-stu-id="8ac67-129">-Response</span></span>
<span data-ttu-id="8ac67-130">Означает, что должен быть возвращен полный ответ.</span><span class="sxs-lookup"><span data-stu-id="8ac67-130">Indicates full response should be return.</span></span>

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

### <span data-ttu-id="8ac67-131">-SessionId</span><span class="sxs-lookup"><span data-stu-id="8ac67-131">-SessionId</span></span>
<span data-ttu-id="8ac67-132">Идентификатор спарк-сеанса.</span><span class="sxs-lookup"><span data-stu-id="8ac67-132">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac67-133">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="8ac67-133">-SessionObject</span></span>
<span data-ttu-id="8ac67-134">Объект ввода сеанса спарк-сеанса, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="8ac67-134">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ac67-135">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="8ac67-135">-SparkPoolName</span></span>
<span data-ttu-id="8ac67-136">Имя пула спарков Synapse.</span><span class="sxs-lookup"><span data-stu-id="8ac67-136">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac67-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8ac67-137">-WorkspaceName</span></span>
<span data-ttu-id="8ac67-138">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="8ac67-138">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ac67-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ac67-139">-Confirm</span></span>
<span data-ttu-id="8ac67-140">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8ac67-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ac67-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ac67-141">-WhatIf</span></span>
<span data-ttu-id="8ac67-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ac67-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ac67-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8ac67-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ac67-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac67-144">CommonParameters</span></span>
<span data-ttu-id="8ac67-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ac67-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac67-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ac67-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac67-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ac67-147">INPUTS</span></span>

### <span data-ttu-id="8ac67-148">System.String</span><span class="sxs-lookup"><span data-stu-id="8ac67-148">System.String</span></span>

### <span data-ttu-id="8ac67-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="8ac67-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="8ac67-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8ac67-150">OUTPUTS</span></span>

### <span data-ttu-id="8ac67-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span><span class="sxs-lookup"><span data-stu-id="8ac67-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span></span>

## <span data-ttu-id="8ac67-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8ac67-152">NOTES</span></span>

## <span data-ttu-id="8ac67-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ac67-153">RELATED LINKS</span></span>