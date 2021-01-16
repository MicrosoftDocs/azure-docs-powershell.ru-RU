---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 46927e25fb4e32aae9ea1870ef9eeaedd5efe008
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399703"
---
# <span data-ttu-id="01ede-101">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="01ede-101">Get-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="01ede-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01ede-102">SYNOPSIS</span></span>
<span data-ttu-id="01ede-103">Получает сертификаты учетной записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="01ede-103">Gets integration account certificates from a resource group.</span></span>

## <span data-ttu-id="01ede-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="01ede-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>] [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01ede-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01ede-105">DESCRIPTION</span></span>
<span data-ttu-id="01ede-106">**Cmdlet Get-AzIntegrationAccountCertificate** получает сертификаты учетных записей интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="01ede-106">The **Get-AzIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="01ede-107">Укажите имя учетной записи интеграции, имя группы ресурсов и имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="01ede-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="01ede-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="01ede-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="01ede-109">Чтобы использовать динамический параметр, введите его в команду.</span><span class="sxs-lookup"><span data-stu-id="01ede-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="01ede-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени cmdlet, а затем нажимая клавишу TAB для циклическиго перебора доступных параметров.</span><span class="sxs-lookup"><span data-stu-id="01ede-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="01ede-111">Если не задан параметр обязательного шаблона, будет выдан запрос на его значение.</span><span class="sxs-lookup"><span data-stu-id="01ede-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="01ede-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="01ede-112">EXAMPLES</span></span>

### <span data-ttu-id="01ede-113">Пример 1. Получить сертификат учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="01ede-113">Example 1: Get an integration account certificate</span></span>
```
PS C:\>Get-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="01ede-114">Эта команда получает сертификат учетной записи интеграции IntegrationAccountCertificate01.</span><span class="sxs-lookup"><span data-stu-id="01ede-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="01ede-115">Пример 2. Получить сертификаты учетной записи интеграции по имени учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="01ede-115">Example 2: Get integration account certificates by integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="01ede-116">Эта команда получает сертификаты учетной записи интеграции для учетной записи IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="01ede-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="01ede-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01ede-117">PARAMETERS</span></span>

### <span data-ttu-id="01ede-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="01ede-118">-CertificateName</span></span>
<span data-ttu-id="01ede-119">Указывает имя сертификата учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="01ede-119">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="01ede-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01ede-120">-DefaultProfile</span></span>
<span data-ttu-id="01ede-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="01ede-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01ede-122">-Name</span><span class="sxs-lookup"><span data-stu-id="01ede-122">-Name</span></span>
<span data-ttu-id="01ede-123">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="01ede-123">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01ede-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01ede-124">-ResourceGroupName</span></span>
<span data-ttu-id="01ede-125">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="01ede-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="01ede-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01ede-126">CommonParameters</span></span>
<span data-ttu-id="01ede-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01ede-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01ede-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01ede-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01ede-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01ede-129">INPUTS</span></span>

### <span data-ttu-id="01ede-130">System.String</span><span class="sxs-lookup"><span data-stu-id="01ede-130">System.String</span></span>

## <span data-ttu-id="01ede-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="01ede-131">OUTPUTS</span></span>

### <span data-ttu-id="01ede-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="01ede-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="01ede-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="01ede-133">NOTES</span></span>

## <span data-ttu-id="01ede-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01ede-134">RELATED LINKS</span></span>

[<span data-ttu-id="01ede-135">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="01ede-135">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="01ede-136">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="01ede-136">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="01ede-137">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="01ede-137">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)

