---
title: Обзор модуля администрирования PowerShell для Azure Stack | Документация Майкрософт
description: Обзор модуля администрирования PowerShell для Azure Stack с инструкциями по установке и конфигурации.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/06/2019
ms.openlocfilehash: b77e09f6fcd5b7752af9f51a42d357db4f1b13db
ms.sourcegitcommit: febbbd3f75c8dd1a296281d265289f015b6cb537
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/12/2019
ms.locfileid: "67037667"
---
# <a name="azure-stack-module-172"></a><span data-ttu-id="ebd8e-103">Модуль Azure Stack 1.7.2</span><span class="sxs-lookup"><span data-stu-id="ebd8e-103">Azure Stack Module 1.7.2</span></span>

## <a name="requirements"></a><span data-ttu-id="ebd8e-104">Требования:</span><span class="sxs-lookup"><span data-stu-id="ebd8e-104">Requirements:</span></span>

<span data-ttu-id="ebd8e-105">Минимальная поддерживаемая версия Azure Stack — 1904.</span><span class="sxs-lookup"><span data-stu-id="ebd8e-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="ebd8e-106">Примечание. Сведения о более ранних версиях Azure Stack см. в разделе [Установка PowerShell для Azure Stack](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell).</span><span class="sxs-lookup"><span data-stu-id="ebd8e-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="ebd8e-107">Install</span><span class="sxs-lookup"><span data-stu-id="ebd8e-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.5.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

## <a name="release-notes"></a><span data-ttu-id="ebd8e-108">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="ebd8e-108">Release Notes</span></span>

* <span data-ttu-id="ebd8e-109">Поддерживается в обновлении 1904.</span><span class="sxs-lookup"><span data-stu-id="ebd8e-109">Supported with 1904 update</span></span>
* <span data-ttu-id="ebd8e-110">Это критическое изменение выпуска.</span><span class="sxs-lookup"><span data-stu-id="ebd8e-110">This a breaking change release.</span></span> <span data-ttu-id="ebd8e-111">Дополнительные сведения о критических изменениях находятся по ссылке <https://aka.ms/azspshmigration170>.</span><span class="sxs-lookup"><span data-stu-id="ebd8e-111">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="ebd8e-112">Критическое изменение. Изменения резервного копирования в режиме шифрования на основе сертификатов.</span><span class="sxs-lookup"><span data-stu-id="ebd8e-112">Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="ebd8e-113">Прекращена поддержка симметричных ключей.</span><span class="sxs-lookup"><span data-stu-id="ebd8e-113">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="ebd8e-114">Дополнительные сведения о критических изменениях находятся по ссылке https://aka.ms/azspshmigration170.</span><span class="sxs-lookup"><span data-stu-id="ebd8e-114">For details on the breaking changes, refer to https://aka.ms/azspshmigration170</span></span>
* <span data-ttu-id="ebd8e-115">Модуль Azs.Storage.Admin</span><span class="sxs-lookup"><span data-stu-id="ebd8e-115">Azs.Storage.Admin Module</span></span> 
* <span data-ttu-id="ebd8e-116">Исправления: новая квота хранилища использует значения по умолчанию, если значения отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="ebd8e-116">Bug fix - New Storage Quota uses defaults if none provided.</span></span>