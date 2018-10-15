---
title: Общие сведения о PowerShell для Azure Stack | Документация Майкрософт
description: Обзор PowerShell для Azure Stack с инструкциями по установке и конфигурации.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: d514e43d82bcb51f65831dc506e58e8747db0381
ms.sourcegitcommit: a749eb729f583c9d0dd86141bbd04984d77ae9ab
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/11/2018
ms.locfileid: "48882679"
---
# <a name="azurerm-module-230"></a><span data-ttu-id="45643-103">Модуль AzureRM, версия 2.3.0</span><span class="sxs-lookup"><span data-stu-id="45643-103">AzureRM Module 2.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="45643-104">Требования:</span><span class="sxs-lookup"><span data-stu-id="45643-104">Requirements:</span></span>
<span data-ttu-id="45643-105">Минимальная поддерживаемая версия Azure Stack — 1808.</span><span class="sxs-lookup"><span data-stu-id="45643-105">Minimum supported Azure Stack version is 1808.</span></span>

<span data-ttu-id="45643-106">Примечание. Если вы используете более раннюю версию, установите версию 1.2.11.</span><span class="sxs-lookup"><span data-stu-id="45643-106">Note: If you are using an earlier version install version 1.2.11</span></span>


## <a name="install"></a><span data-ttu-id="45643-107">Install</span><span class="sxs-lookup"><span data-stu-id="45643-107">Install</span></span>
```powershell
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module -Name AzureRM -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force -ErrorAction Continue
Uninstall-Module AzureRM.AzureStackStorage -Force -ErrorAction Continue
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force
Get-Module Azure.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

```

##<a name="release-notes"></a><span data-ttu-id="45643-108">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="45643-108">Release Notes</span></span>
* <span data-ttu-id="45643-109">Выпуск 2.3.0 содержит целый ряд критических изменений.</span><span class="sxs-lookup"><span data-stu-id="45643-109">The release 2.3.0 comes with a list of breaking changes.</span></span> <span data-ttu-id="45643-110">Для обновления с версии 1.2.11 мы создали руководство по миграции, доступное по адресу https://aka.ms/azspowershellmigration.</span><span class="sxs-lookup"><span data-stu-id="45643-110">To upgrade from the 1.2.11 version, we have created a migration guide at https://aka.ms/azspowershellmigration</span></span>
* <span data-ttu-id="45643-111">Этот выпуск соответствует профилю API Azure Stack 2018-03-01-hybrid.</span><span class="sxs-lookup"><span data-stu-id="45643-111">This release corresponds to the azurestack specific api profile 2018-03-01-hybrid</span></span>
* <span data-ttu-id="45643-112">Все модули зависят от модуля AzureRm.Profile такой же или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="45643-112">All the modules are taking greater than or equal to dependency on the AzureRm.Profile module.</span></span>
* <span data-ttu-id="45643-113">Версии API, поддерживаемые каждым из модулей, обновлены.</span><span class="sxs-lookup"><span data-stu-id="45643-113">Api version suppoerted by  each of the modules are updated.</span></span> 
    * <span data-ttu-id="45643-114">Compute — 2017-03-30</span><span class="sxs-lookup"><span data-stu-id="45643-114">Compute - 2017-03-30</span></span>
    * <span data-ttu-id="45643-115">Network — 2017-10-01</span><span class="sxs-lookup"><span data-stu-id="45643-115">Network - 2017-10-01</span></span>
    * <span data-ttu-id="45643-116">Storage — 2016-01-01</span><span class="sxs-lookup"><span data-stu-id="45643-116">Storage - 2016-01-01</span></span>
    * <span data-ttu-id="45643-117">Resources — 2018-02-01</span><span class="sxs-lookup"><span data-stu-id="45643-117">Resources - 2018-02-01</span></span>
    * <span data-ttu-id="45643-118">Keyvault — 2016-10-01</span><span class="sxs-lookup"><span data-stu-id="45643-118">Keyvault - 2016-10-01</span></span>
    * <span data-ttu-id="45643-119">DNS — 2016-04-01</span><span class="sxs-lookup"><span data-stu-id="45643-119">Dns - 2016-04-01</span></span>
* <span data-ttu-id="45643-120">Полное сопоставление версий API для каждого типа ресурса можно найти в файле https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json.</span><span class="sxs-lookup"><span data-stu-id="45643-120">The complete api version map for each of the resource types can be found at https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span></span>

## <a name="content"></a><span data-ttu-id="45643-121">Содержимое:</span><span class="sxs-lookup"><span data-stu-id="45643-121">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="45643-122">Мост Azure</span><span class="sxs-lookup"><span data-stu-id="45643-122">Azure Bridge</span></span>
<span data-ttu-id="45643-123">Предварительная версия модуля для администраторов компонента Azure Stack "Мост Azure", которая позволяет объединять образы из Azure.</span><span class="sxs-lookup"><span data-stu-id="45643-123">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="45643-124">Azure Backup</span><span class="sxs-lookup"><span data-stu-id="45643-124">Backup</span></span>
<span data-ttu-id="45643-125">Предварительная версия модуля для администраторов службы Backup, которая позволяет администраторам:</span><span class="sxs-lookup"><span data-stu-id="45643-125">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="45643-126">настраивать расположение для хранения резервных копий;</span><span class="sxs-lookup"><span data-stu-id="45643-126">Configure where backups are stored</span></span>
- <span data-ttu-id="45643-127">выполнять резервное копирование;</span><span class="sxs-lookup"><span data-stu-id="45643-127">Perform backups</span></span>
- <span data-ttu-id="45643-128">выводить список созданных резервных копий и выполнять на их основе восстановление.</span><span class="sxs-lookup"><span data-stu-id="45643-128">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="45643-129">Приложения для коммерции</span><span class="sxs-lookup"><span data-stu-id="45643-129">Commerce</span></span>
<span data-ttu-id="45643-130">Предварительная версия модуля для администраторов средства коммерции в Azure Stack, которая позволяет просматривать статистические сведения об использовании данных для всей системы Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="45643-130">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="45643-131">Службы вычислений</span><span class="sxs-lookup"><span data-stu-id="45643-131">Compute</span></span>
<span data-ttu-id="45643-132">Предварительная версия модуля для администраторов вычислительных ресурсов в Azure Stack, которая предоставляет функции управления квотами вычислительных ресурсов, образами платформ, управляемыми дисками и расширениями виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="45643-132">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="45643-133">Fabric</span><span class="sxs-lookup"><span data-stu-id="45643-133">Fabric</span></span>
<span data-ttu-id="45643-134">Предварительная версия модуля для администраторов Fabric в Azure Stack, которая позволяет администраторам просматривать компоненты инфраструктуры и управлять ими, выполняя следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="45643-134">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="45643-135">остановка, запуск и завершение работы для узлов единиц масштабирования;</span><span class="sxs-lookup"><span data-stu-id="45643-135">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="45643-136">очистка и возобновление работы узлов единиц масштабирования для связанных действий FRU;</span><span class="sxs-lookup"><span data-stu-id="45643-136">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="45643-137">исправление узлов единиц масштабирования;</span><span class="sxs-lookup"><span data-stu-id="45643-137">Repair of scale unit nodes</span></span>
- <span data-ttu-id="45643-138">перезапуск роли инфраструктуры;</span><span class="sxs-lookup"><span data-stu-id="45643-138">Restart of Infrastructure role</span></span>
- <span data-ttu-id="45643-139">остановка, запуск и завершение работы экземпляров роли инфраструктуры;</span><span class="sxs-lookup"><span data-stu-id="45643-139">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="45643-140">создание пулов IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="45643-140">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="45643-141">Коллекция</span><span class="sxs-lookup"><span data-stu-id="45643-141">Gallery</span></span>
<span data-ttu-id="45643-142">Предварительная версия модуля для администраторов коллекций Azure Stack, которая предоставляет функции для управления элементами коллекции в Azure Stack Marketplace.</span><span class="sxs-lookup"><span data-stu-id="45643-142">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="45643-143">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="45643-143">Infrastructure Insights</span></span>
<span data-ttu-id="45643-144">Предварительная версия модуля для администраторов Infrastructure Insights, которая позволяет администраторам:</span><span class="sxs-lookup"><span data-stu-id="45643-144">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="45643-145">просматривать сведения о работоспособности ресурсов отметок в Azure Stack;</span><span class="sxs-lookup"><span data-stu-id="45643-145">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="45643-146">просматривать оповещения и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="45643-146">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="45643-147">Хранилище ключей</span><span class="sxs-lookup"><span data-stu-id="45643-147">KeyVault</span></span>
<span data-ttu-id="45643-148">Предварительная версия модуля для администраторов Key Vault в Azure Stack, которая позволяет администратору просматривать квоты Key Vault.</span><span class="sxs-lookup"><span data-stu-id="45643-148">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="45643-149">Сеть</span><span class="sxs-lookup"><span data-stu-id="45643-149">Network</span></span>
<span data-ttu-id="45643-150">Предварительная версия модуля для администраторов сетей, которая позволяет:</span><span class="sxs-lookup"><span data-stu-id="45643-150">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="45643-151">управлять квотами сети;</span><span class="sxs-lookup"><span data-stu-id="45643-151">Management of network quotas</span></span>
- <span data-ttu-id="45643-152">просматривать выделенные сетевые ресурсы, например общедоступные IP-адреса, виртуальные сети, подсистемы балансировки нагрузки;</span><span class="sxs-lookup"><span data-stu-id="45643-152">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="45643-153">использовать командлет для отображения общих сведений об администраторе.</span><span class="sxs-lookup"><span data-stu-id="45643-153">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="45643-154">Хранилище</span><span class="sxs-lookup"><span data-stu-id="45643-154">Storage</span></span>
<span data-ttu-id="45643-155">Предварительная версия модуля для администраторов хранилища Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="45643-155">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="45643-156">В этом выпуске мы предоставляем следующие функции:</span><span class="sxs-lookup"><span data-stu-id="45643-156">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="45643-157">управление квотами хранилища;</span><span class="sxs-lookup"><span data-stu-id="45643-157">Manage storage quotas</span></span>
- <span data-ttu-id="45643-158">сборка мусора для удаленных ресурсов хранилища;</span><span class="sxs-lookup"><span data-stu-id="45643-158">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="45643-159">восстановление удаленных учетных записей хранения;</span><span class="sxs-lookup"><span data-stu-id="45643-159">Restore deleted storage accounts</span></span>
- <span data-ttu-id="45643-160">перенос контейнеров из одной общей папки в другую;</span><span class="sxs-lookup"><span data-stu-id="45643-160">Migrate containers from one share to another</span></span>
- <span data-ttu-id="45643-161">просмотр сведений об отдельных компонентах хранилища;</span><span class="sxs-lookup"><span data-stu-id="45643-161">View information about the individual storage components</span></span>
- <span data-ttu-id="45643-162">просмотр сведений об использовании и производительности.</span><span class="sxs-lookup"><span data-stu-id="45643-162">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="45643-163">Администратор подписки</span><span class="sxs-lookup"><span data-stu-id="45643-163">Subscription Admin</span></span>
<span data-ttu-id="45643-164">Предварительная версия модуля для администраторов подписки Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="45643-164">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="45643-165">Этот модуль предоставляет следующие функции для администраторов:</span><span class="sxs-lookup"><span data-stu-id="45643-165">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="45643-166">управление планами и предложениями;</span><span class="sxs-lookup"><span data-stu-id="45643-166">Manage plans and offers</span></span>
- <span data-ttu-id="45643-167">просмотр сведений об использовании и производительности.</span><span class="sxs-lookup"><span data-stu-id="45643-167">View usage and performance information</span></span>
- <span data-ttu-id="45643-168">Управление RBAC</span><span class="sxs-lookup"><span data-stu-id="45643-168">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="45643-169">Подписка</span><span class="sxs-lookup"><span data-stu-id="45643-169">Subscription</span></span>
<span data-ttu-id="45643-170">Предварительная версия модуля подписки Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="45643-170">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="45643-171">Этот модуль предоставляет следующие функции для пользователей:</span><span class="sxs-lookup"><span data-stu-id="45643-171">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="45643-172">создание, удаление и изменение подписок.</span><span class="sxs-lookup"><span data-stu-id="45643-172">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="45643-173">Блокировка изменений</span><span class="sxs-lookup"><span data-stu-id="45643-173">Update</span></span>
<span data-ttu-id="45643-174">Предварительная версия модуля для администраторов обновлений Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="45643-174">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="45643-175">В этом модуле администраторы могут:</span><span class="sxs-lookup"><span data-stu-id="45643-175">In this module administrators can:</span></span>
- <span data-ttu-id="45643-176">выводить список и устанавливать доступные обновления;</span><span class="sxs-lookup"><span data-stu-id="45643-176">List and install available updates</span></span>
- <span data-ttu-id="45643-177">возобновлять прерванную установку обновлений;</span><span class="sxs-lookup"><span data-stu-id="45643-177">Resume interrupted updates</span></span>
- <span data-ttu-id="45643-178">просматривать установленные обновления.</span><span class="sxs-lookup"><span data-stu-id="45643-178">View installed updates</span></span>