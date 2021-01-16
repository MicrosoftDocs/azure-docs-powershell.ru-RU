---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F26CB715-D66A-4672-AA47-F3B316957FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 94963c8c5d61c91e2d53cdf7b12cc333acc566a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393308"
---
# <span data-ttu-id="f6150-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="f6150-101">Get-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="f6150-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6150-102">SYNOPSIS</span></span>
<span data-ttu-id="f6150-103">Получает дополнительные параметры защиты от угроз для сервера.</span><span class="sxs-lookup"><span data-stu-id="f6150-103">Gets the advanced threat protection settings for a server.</span></span>

## <span data-ttu-id="f6150-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f6150-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionSetting -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6150-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6150-105">DESCRIPTION</span></span>
<span data-ttu-id="f6150-106">Чтобы **получить дополнительные** параметры защиты от угроз для сервера Azure SQL, можно получить дополнительные параметры защиты от SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f6150-106">The **Get-AzSqlServerAdvancedThreatProtectionSetting** cmdlet gets the advanced threat protection settings of an Azure SQL server.</span></span>
<span data-ttu-id="f6150-107">Чтобы использовать этот cmdlet, укажите параметры *ResourceGroupName* и *ServerName,* определяя сервер, для которого этот cmdlet получает параметры.</span><span class="sxs-lookup"><span data-stu-id="f6150-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the server for which this cmdlet gets the settings.</span></span>

## <span data-ttu-id="f6150-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f6150-108">EXAMPLES</span></span>

### <span data-ttu-id="f6150-109">Пример 1. Расширенные параметры защиты от угроз для сервера</span><span class="sxs-lookup"><span data-stu-id="f6150-109">Example 1: Get the advanced threat protection settings for a server</span></span>
```
PS C:\>Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

<span data-ttu-id="f6150-110">Эта команда получает расширенные параметры защиты от угроз для сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="f6150-110">This command gets the advanced threat protection settings for a server named Server01.</span></span>
<span data-ttu-id="f6150-111">Серверу назначена группа ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f6150-111">The server is assigned to the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="f6150-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6150-112">PARAMETERS</span></span>

### <span data-ttu-id="f6150-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6150-113">-DefaultProfile</span></span>
<span data-ttu-id="f6150-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f6150-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6150-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6150-115">-ResourceGroupName</span></span>
<span data-ttu-id="f6150-116">Имя группы ресурсов, к которой принадлежит сервер.</span><span class="sxs-lookup"><span data-stu-id="f6150-116">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="f6150-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f6150-117">-ServerName</span></span>
<span data-ttu-id="f6150-118">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="f6150-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="f6150-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6150-119">-Confirm</span></span>
<span data-ttu-id="f6150-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f6150-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6150-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6150-121">-WhatIf</span></span>
<span data-ttu-id="f6150-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6150-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6150-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f6150-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6150-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6150-124">CommonParameters</span></span>
<span data-ttu-id="f6150-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6150-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6150-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6150-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6150-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6150-127">INPUTS</span></span>

### <span data-ttu-id="f6150-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f6150-128">System.String</span></span>

## <span data-ttu-id="f6150-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f6150-129">OUTPUTS</span></span>

### <span data-ttu-id="f6150-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span><span class="sxs-lookup"><span data-stu-id="f6150-130">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerAdvancedThreatProtectionSettingsModel</span></span>

## <span data-ttu-id="f6150-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f6150-131">NOTES</span></span>

## <span data-ttu-id="f6150-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6150-132">RELATED LINKS</span></span>

[<span data-ttu-id="f6150-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="f6150-133">Remove-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>](./Remove-AzSqlDatabaseAdvancedThreatProtectionSetting.md)

[<span data-ttu-id="f6150-134">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="f6150-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

