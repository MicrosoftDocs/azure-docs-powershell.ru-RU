---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
ms.openlocfilehash: dfe9324644115d00054961e8e159c672d1aba588
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570467"
---
# <span data-ttu-id="ef765-101">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="ef765-101">Get-AzureRmVMBootDiagnosticsData</span></span>

## <span data-ttu-id="ef765-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef765-102">SYNOPSIS</span></span>
<span data-ttu-id="ef765-103">Получение данных диагностики загрузки для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ef765-103">Gets boot diagnostics data for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef765-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef765-104">SYNTAX</span></span>

### <span data-ttu-id="ef765-105">WindowsParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ef765-105">WindowsParamSet (Default)</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef765-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="ef765-106">LinuxParamSet</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef765-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef765-107">DESCRIPTION</span></span>
<span data-ttu-id="ef765-108">Командлет **Get-AzureRmVMBootDiagnosticsData** получает данные диагностики загрузки для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ef765-108">The **Get-AzureRmVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="ef765-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef765-109">EXAMPLES</span></span>

### <span data-ttu-id="ef765-110">Пример 1: получение данных диагностики загрузки</span><span class="sxs-lookup"><span data-stu-id="ef765-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzureRmVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="ef765-111">Эта команда возвращает данные диагностики загрузки для виртуальной машины с именем ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="ef765-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="ef765-112">Эта виртуальная машина запускает операционную систему Windows.</span><span class="sxs-lookup"><span data-stu-id="ef765-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="ef765-113">Команда сохраняет данные в указанном локальном пути.</span><span class="sxs-lookup"><span data-stu-id="ef765-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="ef765-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef765-114">PARAMETERS</span></span>

### <span data-ttu-id="ef765-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef765-115">-DefaultProfile</span></span>
<span data-ttu-id="ef765-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef765-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef765-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="ef765-117">-Linux</span></span>
<span data-ttu-id="ef765-118">Указывает на то, что виртуальная машина работает под управлением операционной системы Linux.</span><span class="sxs-lookup"><span data-stu-id="ef765-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef765-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="ef765-119">-LocalPath</span></span>
<span data-ttu-id="ef765-120">Указывает локальный путь для данных диагностики загрузки.</span><span class="sxs-lookup"><span data-stu-id="ef765-120">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: LinuxParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef765-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ef765-121">-Name</span></span>
<span data-ttu-id="ef765-122">Указывает имя виртуальной машины, для которой этот командлет получает данные диагностики.</span><span class="sxs-lookup"><span data-stu-id="ef765-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef765-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef765-123">-ResourceGroupName</span></span>
<span data-ttu-id="ef765-124">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ef765-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ef765-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="ef765-125">-Windows</span></span>
<span data-ttu-id="ef765-126">Указывает на то, что виртуальная машина работает под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="ef765-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef765-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef765-127">CommonParameters</span></span>
<span data-ttu-id="ef765-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef765-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef765-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef765-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef765-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef765-130">INPUTS</span></span>

## <span data-ttu-id="ef765-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef765-131">OUTPUTS</span></span>

## <span data-ttu-id="ef765-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef765-132">NOTES</span></span>

## <span data-ttu-id="ef765-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef765-133">RELATED LINKS</span></span>

[<span data-ttu-id="ef765-134">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ef765-134">Set-AzureRmVMBootDiagnostics</span></span>](./Set-AzureRmVMBootDiagnostics.md)

