---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: 6ea805f1e3a3711c2efe6faefd73edf06c4b51fd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394820"
---
# <span data-ttu-id="9e719-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="9e719-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="9e719-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e719-102">SYNOPSIS</span></span>

## <span data-ttu-id="9e719-103">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9e719-103">SYNTAX</span></span>

### <span data-ttu-id="9e719-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="9e719-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e719-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="9e719-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e719-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e719-106">DESCRIPTION</span></span>
<span data-ttu-id="9e719-107">С **помощью cmdlet Get-AzWebAppBackupList** можно получить список резервных копий для Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="9e719-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="9e719-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9e719-108">EXAMPLES</span></span>

### <span data-ttu-id="9e719-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9e719-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="9e719-110">Эта команда возвращает список резервных копий webApp WebAppStandard, связанный с группой ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9e719-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="9e719-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e719-111">PARAMETERS</span></span>

### <span data-ttu-id="9e719-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e719-112">-DefaultProfile</span></span>
<span data-ttu-id="9e719-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e719-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e719-114">-Name</span><span class="sxs-lookup"><span data-stu-id="9e719-114">-Name</span></span>
<span data-ttu-id="9e719-115">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="9e719-115">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e719-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e719-116">-ResourceGroupName</span></span>
<span data-ttu-id="9e719-117">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9e719-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e719-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="9e719-118">-Slot</span></span>
<span data-ttu-id="9e719-119">Название слота</span><span class="sxs-lookup"><span data-stu-id="9e719-119">Slot name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e719-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="9e719-120">-WebApp</span></span>
<span data-ttu-id="9e719-121">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="9e719-121">Piped WebApp</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e719-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e719-122">CommonParameters</span></span>
<span data-ttu-id="9e719-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e719-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e719-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e719-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e719-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e719-125">INPUTS</span></span>

### <span data-ttu-id="9e719-126">System.String</span><span class="sxs-lookup"><span data-stu-id="9e719-126">System.String</span></span>

### <span data-ttu-id="9e719-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="9e719-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9e719-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9e719-128">OUTPUTS</span></span>

### <span data-ttu-id="9e719-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="9e719-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="9e719-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9e719-130">NOTES</span></span>

## <span data-ttu-id="9e719-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e719-131">RELATED LINKS</span></span>