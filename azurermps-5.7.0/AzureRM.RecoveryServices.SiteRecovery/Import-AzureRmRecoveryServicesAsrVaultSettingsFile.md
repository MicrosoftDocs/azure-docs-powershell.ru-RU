---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/import-azurermrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: ef92265a59271e321f9e2002e75cb4ea9d64542d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566152"
---
# <span data-ttu-id="87c22-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="87c22-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="87c22-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87c22-102">SYNOPSIS</span></span>
<span data-ttu-id="87c22-103">Импортирует указанный файл параметров в хранилище ASR, чтобы задать контекст хранилища (контекст сеанса PowerShell) для последующих операций ASR в сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="87c22-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87c22-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87c22-104">SYNTAX</span></span>

```
Import-AzureRmRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87c22-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87c22-105">DESCRIPTION</span></span>
<span data-ttu-id="87c22-106">Командлет **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** импортирует файл параметров хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="87c22-106">The **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="87c22-107">Файл параметров хранилища используется для задания контекста хранилища для последующих операций восстановления сайта Azure в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="87c22-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="87c22-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87c22-108">EXAMPLES</span></span>

### <span data-ttu-id="87c22-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="87c22-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzureRmRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="87c22-110">Импортирует указанный файл параметров хранилища служб восстановления и возвращает параметры импортированного хранилища.</span><span class="sxs-lookup"><span data-stu-id="87c22-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="87c22-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87c22-111">PARAMETERS</span></span>

### <span data-ttu-id="87c22-112">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87c22-112">-Confirm</span></span>
<span data-ttu-id="87c22-113">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="87c22-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87c22-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87c22-114">-DefaultProfile</span></span>
<span data-ttu-id="87c22-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87c22-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="87c22-116">-Path</span><span class="sxs-lookup"><span data-stu-id="87c22-116">-Path</span></span>
<span data-ttu-id="87c22-117">Указывает путь к папке для файла параметров в хранилище ASR.</span><span class="sxs-lookup"><span data-stu-id="87c22-117">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="87c22-118">Этот файл можно скачать с портала хранилища служб восстановления и сохранить на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="87c22-118">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

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

### <span data-ttu-id="87c22-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87c22-119">-WhatIf</span></span>
<span data-ttu-id="87c22-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="87c22-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87c22-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="87c22-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87c22-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87c22-122">CommonParameters</span></span>
<span data-ttu-id="87c22-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87c22-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87c22-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87c22-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87c22-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87c22-125">INPUTS</span></span>

### <span data-ttu-id="87c22-126">System. String</span><span class="sxs-lookup"><span data-stu-id="87c22-126">System.String</span></span>

## <span data-ttu-id="87c22-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87c22-127">OUTPUTS</span></span>

### <span data-ttu-id="87c22-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="87c22-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="87c22-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="87c22-129">NOTES</span></span>

## <span data-ttu-id="87c22-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87c22-130">RELATED LINKS</span></span>

[<span data-ttu-id="87c22-131">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="87c22-131">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesAsrVaultSettingsFile.md)