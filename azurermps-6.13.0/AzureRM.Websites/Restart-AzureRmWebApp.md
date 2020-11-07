---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebApp.md
ms.openlocfilehash: 42b561707dd1b4240cf0542adfb196250aafc8d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565287"
---
# <span data-ttu-id="53bdc-101">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="53bdc-101">Restart-AzureRmWebApp</span></span>

## <span data-ttu-id="53bdc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="53bdc-102">SYNOPSIS</span></span>
<span data-ttu-id="53bdc-103">Перезапускает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="53bdc-103">Restarts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53bdc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="53bdc-104">SYNTAX</span></span>

### <span data-ttu-id="53bdc-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="53bdc-105">S1</span></span>
```
Restart-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="53bdc-106">S2</span><span class="sxs-lookup"><span data-stu-id="53bdc-106">S2</span></span>
```
Restart-AzureRmWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53bdc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53bdc-107">DESCRIPTION</span></span>
<span data-ttu-id="53bdc-108">Командлет **restart-AzureRmWebApp** останавливается, а затем запускает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="53bdc-108">The **Restart-AzureRmWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="53bdc-109">Если веб-приложение находится в остановленном состоянии, используйте командлет Start-AzureRmWebApp.</span><span class="sxs-lookup"><span data-stu-id="53bdc-109">If the Web App is in a stopped state, use the Start-AzureRmWebApp cmdlet.</span></span>

## <span data-ttu-id="53bdc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="53bdc-110">EXAMPLES</span></span>

### <span data-ttu-id="53bdc-111">Пример 1: перезагрузка веб-приложения</span><span class="sxs-lookup"><span data-stu-id="53bdc-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="53bdc-112">Эта команда останавливает веб-приложение Azure с именем ContosoSite, которое принадлежит группе ресурсов Default-Web-WestUS, а затем перезапускает ее.</span><span class="sxs-lookup"><span data-stu-id="53bdc-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="53bdc-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="53bdc-113">PARAMETERS</span></span>

### <span data-ttu-id="53bdc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53bdc-114">-DefaultProfile</span></span>
<span data-ttu-id="53bdc-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="53bdc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53bdc-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="53bdc-116">-Name</span></span>
<span data-ttu-id="53bdc-117">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="53bdc-117">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bdc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53bdc-118">-ResourceGroupName</span></span>
<span data-ttu-id="53bdc-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="53bdc-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53bdc-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="53bdc-120">-WebApp</span></span>
<span data-ttu-id="53bdc-121">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="53bdc-121">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53bdc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53bdc-122">CommonParameters</span></span>
<span data-ttu-id="53bdc-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="53bdc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53bdc-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53bdc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53bdc-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="53bdc-125">INPUTS</span></span>

### <span data-ttu-id="53bdc-126">System. String</span><span class="sxs-lookup"><span data-stu-id="53bdc-126">System.String</span></span>

### <span data-ttu-id="53bdc-127">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="53bdc-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="53bdc-128">Параметры: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="53bdc-128">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="53bdc-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="53bdc-129">OUTPUTS</span></span>

### <span data-ttu-id="53bdc-130">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="53bdc-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="53bdc-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="53bdc-131">NOTES</span></span>

## <span data-ttu-id="53bdc-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53bdc-132">RELATED LINKS</span></span>

[<span data-ttu-id="53bdc-133">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="53bdc-133">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="53bdc-134">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="53bdc-134">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="53bdc-135">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="53bdc-135">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="53bdc-136">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="53bdc-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="53bdc-137">Остановить-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="53bdc-137">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)

