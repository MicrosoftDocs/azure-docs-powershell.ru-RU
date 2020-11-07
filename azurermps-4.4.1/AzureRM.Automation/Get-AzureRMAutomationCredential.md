---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
ms.openlocfilehash: f00cbe95c71bdbd8c7f92f123756fa0c474d878f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570151"
---
# <span data-ttu-id="2f1a1-101">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="2f1a1-101">Get-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="2f1a1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f1a1-102">SYNOPSIS</span></span>
<span data-ttu-id="2f1a1-103">Получает учетные данные автоматизации.</span><span class="sxs-lookup"><span data-stu-id="2f1a1-103">Gets Automation credentials.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f1a1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f1a1-104">SYNTAX</span></span>

### <span data-ttu-id="2f1a1-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2f1a1-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f1a1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2f1a1-106">ByName</span></span>
```
Get-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f1a1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f1a1-107">DESCRIPTION</span></span>
<span data-ttu-id="2f1a1-108">Командлет **Get-AzureRmAutomationCredential** получает один или несколько учетных данных службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="2f1a1-108">The **Get-AzureRmAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="2f1a1-109">По умолчанию возвращаются все учетные данные.</span><span class="sxs-lookup"><span data-stu-id="2f1a1-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="2f1a1-110">Укажите имя учетных данных для получения определенных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="2f1a1-110">Specify the name of a credential to get a specific credential.</span></span>

<span data-ttu-id="2f1a1-111">В целях безопасности этот командлет не возвращает пароли учетных данных.</span><span class="sxs-lookup"><span data-stu-id="2f1a1-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="2f1a1-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f1a1-112">EXAMPLES</span></span>

### <span data-ttu-id="2f1a1-113">Пример 1: получение всех учетных данных</span><span class="sxs-lookup"><span data-stu-id="2f1a1-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="2f1a1-114">Эта команда получает метаданные для всех учетных данных в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="2f1a1-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="2f1a1-115">Пример 2: получение учетных данных</span><span class="sxs-lookup"><span data-stu-id="2f1a1-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="2f1a1-116">Эта команда получает метаданные для учетных данных с именем ContosoCredential в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="2f1a1-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="2f1a1-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f1a1-117">PARAMETERS</span></span>

### <span data-ttu-id="2f1a1-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2f1a1-118">-AutomationAccountName</span></span>
<span data-ttu-id="2f1a1-119">Указывает имя учетной записи автоматизации, для которой этот командлет извлекает учетные данные.</span><span class="sxs-lookup"><span data-stu-id="2f1a1-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="2f1a1-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2f1a1-120">-Name</span></span>
<span data-ttu-id="2f1a1-121">Указывает имя извлекаемых учетных данных.</span><span class="sxs-lookup"><span data-stu-id="2f1a1-121">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f1a1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f1a1-122">-ResourceGroupName</span></span>
<span data-ttu-id="2f1a1-123">Указывает группу ресурсов, для которой этот командлет извлекает учетные данные.</span><span class="sxs-lookup"><span data-stu-id="2f1a1-123">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="2f1a1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f1a1-124">-DefaultProfile</span></span>
<span data-ttu-id="2f1a1-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f1a1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f1a1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f1a1-126">CommonParameters</span></span>
<span data-ttu-id="2f1a1-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f1a1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f1a1-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f1a1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f1a1-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f1a1-129">INPUTS</span></span>

## <span data-ttu-id="2f1a1-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f1a1-130">OUTPUTS</span></span>

### <span data-ttu-id="2f1a1-131">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="2f1a1-131">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="2f1a1-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f1a1-132">NOTES</span></span>

## <span data-ttu-id="2f1a1-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f1a1-133">RELATED LINKS</span></span>

[<span data-ttu-id="2f1a1-134">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="2f1a1-134">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="2f1a1-135">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="2f1a1-135">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="2f1a1-136">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="2f1a1-136">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)

