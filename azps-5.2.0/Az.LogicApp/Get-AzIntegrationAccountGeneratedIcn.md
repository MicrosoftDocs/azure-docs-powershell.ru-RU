---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 0dffb7a99e29ea4cc595cad1b5b92450e83289f4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399684"
---
# <span data-ttu-id="c05a9-101">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="c05a9-101">Get-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="c05a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c05a9-102">SYNOPSIS</span></span>
<span data-ttu-id="c05a9-103">Этот cmdlet извлекает текущее значение сгенерированного номера управления для обмена в рамках соглашения.</span><span class="sxs-lookup"><span data-stu-id="c05a9-103">This cmdlet retrieves the current value of the generated interchange control number per agreement.</span></span>

## <span data-ttu-id="c05a9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c05a9-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c05a9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c05a9-105">DESCRIPTION</span></span>
<span data-ttu-id="c05a9-106">Этот cmdlet предназначен для использования в сценариях аварийного восстановления для получения текущего значения сгенерированного номера управления обмена, чтобы записать увеличенное значение с помощью Set-AzIntegrationAccountGeneratedIcn.</span><span class="sxs-lookup"><span data-stu-id="c05a9-106">This cmdlet is meant to be used in disaster recovery scenarios to retrieve the current value of the generated interchange control number so to write back an increased value with Set-AzIntegrationAccountGeneratedIcn.</span></span>
<span data-ttu-id="c05a9-107">Номер управления обмена данными следует увеличить, чтобы избежать дублирования чисел, которые еще нельзя реплицировать в пассивную область, когда произошла катастрофа в активной области.</span><span class="sxs-lookup"><span data-stu-id="c05a9-107">The interchange control number should be increased to avoid duplicate interchange control numbers for the numbers that could not yet be replicated to the passive region when the disaster happened in the active region.</span></span>
<span data-ttu-id="c05a9-108">Укажите параметр "-AgreementType", чтобы указать, должны ли возвращаться номера управления X12 или Edifact</span><span class="sxs-lookup"><span data-stu-id="c05a9-108">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="c05a9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c05a9-109">EXAMPLES</span></span>

### <span data-ttu-id="c05a9-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c05a9-110">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="c05a9-111">Эта команда получает сгенерированную учетную запись интеграции номер управления X12 по имени соглашения.</span><span class="sxs-lookup"><span data-stu-id="c05a9-111">This command gets the integration account generated X12 interchange control number by agreement name.</span></span> <span data-ttu-id="c05a9-112">Убедитесь, что соглашение задано в типе "X12"</span><span class="sxs-lookup"><span data-stu-id="c05a9-112">Please make sure agreement specified is of type "X12"</span></span>

### <span data-ttu-id="c05a9-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c05a9-113">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="c05a9-114">Эта команда получает учетную запись интеграции, сгенерированную для управления Edifact interchange, по имени соглашения.</span><span class="sxs-lookup"><span data-stu-id="c05a9-114">This command gets the integration account generated Edifact interchange control number by agreement name.</span></span> <span data-ttu-id="c05a9-115">Убедитесь, что соглашение задано в типе "Edifact"</span><span class="sxs-lookup"><span data-stu-id="c05a9-115">Please make sure agreement specified is of type "Edifact"</span></span>

### <span data-ttu-id="c05a9-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c05a9-116">Example 3</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1"
ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement1
IsMessageProcessingFailed:

ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement2
IsMessageProcessingFailed:

ControlNumber            : No generated control number was found for this agreement.
ControlNumberChangedTime : 1/1/0001 12:00:00 AM
AgreementName            : X12IntegrationAccountAgreement3
IsMessageProcessingFailed:
```

<span data-ttu-id="c05a9-117">Эта команда получает все созданные номера управления X12 по имени учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="c05a9-117">This command gets all the generated X12 interchange control numbers by integration account name.</span></span>

## <span data-ttu-id="c05a9-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c05a9-118">PARAMETERS</span></span>

### <span data-ttu-id="c05a9-119">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="c05a9-119">-AgreementName</span></span>
<span data-ttu-id="c05a9-120">Имя соглашения об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="c05a9-120">The integration account agreement name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c05a9-121">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="c05a9-121">-AgreementType</span></span>
<span data-ttu-id="c05a9-122">Тип соглашения об учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="c05a9-122">The integration account agreement type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c05a9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c05a9-123">-DefaultProfile</span></span>
<span data-ttu-id="c05a9-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c05a9-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c05a9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c05a9-125">-Name</span></span>
<span data-ttu-id="c05a9-126">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="c05a9-126">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c05a9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c05a9-127">-ResourceGroupName</span></span>
<span data-ttu-id="c05a9-128">Имя группы ресурсов учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="c05a9-128">The integration account resource group name.</span></span>

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

### <span data-ttu-id="c05a9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c05a9-129">CommonParameters</span></span>
<span data-ttu-id="c05a9-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c05a9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c05a9-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c05a9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c05a9-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c05a9-132">INPUTS</span></span>

### <span data-ttu-id="c05a9-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c05a9-133">System.String</span></span>

## <span data-ttu-id="c05a9-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c05a9-134">OUTPUTS</span></span>

### <span data-ttu-id="c05a9-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="c05a9-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="c05a9-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c05a9-136">NOTES</span></span>

## <span data-ttu-id="c05a9-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c05a9-137">RELATED LINKS</span></span>

[<span data-ttu-id="c05a9-138">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="c05a9-138">Set-AzIntegrationAccountGeneratedIcn</span></span>](./Set-AzIntegrationAccountGeneratedIcn.md)
