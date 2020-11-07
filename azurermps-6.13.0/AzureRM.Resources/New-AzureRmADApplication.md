---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
ms.openlocfilehash: e23e3db6cb574fb16b2c559c948372c808840de1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564035"
---
# <span data-ttu-id="32aa0-101">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="32aa0-101">New-AzureRmADApplication</span></span>

## <span data-ttu-id="32aa0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32aa0-102">SYNOPSIS</span></span>
<span data-ttu-id="32aa0-103">Создание нового приложения Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="32aa0-103">Creates a new azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32aa0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32aa0-104">SYNTAX</span></span>

### <span data-ttu-id="32aa0-105">ApplicationWithoutCredentialParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="32aa0-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32aa0-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="32aa0-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32aa0-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="32aa0-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32aa0-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="32aa0-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32aa0-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="32aa0-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32aa0-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32aa0-110">DESCRIPTION</span></span>
<span data-ttu-id="32aa0-111">Создание нового приложения Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="32aa0-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="32aa0-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32aa0-112">EXAMPLES</span></span>

### <span data-ttu-id="32aa0-113">Пример 1: создание нового приложения AAD.</span><span class="sxs-lookup"><span data-stu-id="32aa0-113">Example 1 - Create new AAD application.</span></span>

```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="32aa0-114">Создание нового приложения Azure Active Directory без каких-либо учетных данных.</span><span class="sxs-lookup"><span data-stu-id="32aa0-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="32aa0-115">Пример 2. Создайте новое приложение AAD с паролем.</span><span class="sxs-lookup"><span data-stu-id="32aa0-115">Example 2 - Create new AAD application with password.</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="32aa0-116">Создание нового приложения Azure Active Directory и связывание с ним учетных данных пароля.</span><span class="sxs-lookup"><span data-stu-id="32aa0-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="32aa0-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32aa0-117">PARAMETERS</span></span>

### <span data-ttu-id="32aa0-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="32aa0-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="32aa0-119">Значение, определяющее, является ли приложение единственным клиентом или несколькими клиентами.</span><span class="sxs-lookup"><span data-stu-id="32aa0-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32aa0-120">-CertValue</span><span class="sxs-lookup"><span data-stu-id="32aa0-120">-CertValue</span></span>
<span data-ttu-id="32aa0-121">Значение типа учетных данных "асимметричный".</span><span class="sxs-lookup"><span data-stu-id="32aa0-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="32aa0-122">Он представляет сертификат базового 64 в кодировке.</span><span class="sxs-lookup"><span data-stu-id="32aa0-122">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32aa0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32aa0-123">-DefaultProfile</span></span>
<span data-ttu-id="32aa0-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="32aa0-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32aa0-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="32aa0-125">-DisplayName</span></span>
<span data-ttu-id="32aa0-126">Отображаемое имя нового приложения.</span><span class="sxs-lookup"><span data-stu-id="32aa0-126">Display name of the new application.</span></span>

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

### <span data-ttu-id="32aa0-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="32aa0-127">-EndDate</span></span>
<span data-ttu-id="32aa0-128">Эффективная дата окончания использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="32aa0-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="32aa0-129">Значение даты окончания по умолчанию — это год от сегодняшнего дня.</span><span class="sxs-lookup"><span data-stu-id="32aa0-129">The default end date value is one year from today.</span></span> <span data-ttu-id="32aa0-130">Для «асимметричных» учетных данных типа это значение должно быть установлено в on или до даты, когда сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="32aa0-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32aa0-131">-Главная страница</span><span class="sxs-lookup"><span data-stu-id="32aa0-131">-HomePage</span></span>
<span data-ttu-id="32aa0-132">URL-адрес домашней страницы приложения.</span><span class="sxs-lookup"><span data-stu-id="32aa0-132">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="32aa0-133">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="32aa0-133">-IdentifierUris</span></span>
<span data-ttu-id="32aa0-134">Универсальные коды ресурсов (URI), обозначающие приложение.</span><span class="sxs-lookup"><span data-stu-id="32aa0-134">The URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32aa0-135">-KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="32aa0-135">-KeyCredentials</span></span>
<span data-ttu-id="32aa0-136">Список учетных данных сертификата, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="32aa0-136">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32aa0-137">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="32aa0-137">-Password</span></span>
<span data-ttu-id="32aa0-138">Пароль, который должен быть связан с приложением.</span><span class="sxs-lookup"><span data-stu-id="32aa0-138">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32aa0-139">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="32aa0-139">-PasswordCredentials</span></span>
<span data-ttu-id="32aa0-140">Список учетных данных пароля, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="32aa0-140">The list of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32aa0-141">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="32aa0-141">-ReplyUrls</span></span>
<span data-ttu-id="32aa0-142">URL-адреса ответа приложения.</span><span class="sxs-lookup"><span data-stu-id="32aa0-142">The application reply urls.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32aa0-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="32aa0-143">-StartDate</span></span>
<span data-ttu-id="32aa0-144">Фактическая дата начала использования учетных данных.</span><span class="sxs-lookup"><span data-stu-id="32aa0-144">The effective start date of the credential usage.</span></span>
<span data-ttu-id="32aa0-145">Значение даты начала по умолчанию — сегодня.</span><span class="sxs-lookup"><span data-stu-id="32aa0-145">The default start date value is today.</span></span> <span data-ttu-id="32aa0-146">Для «асимметричных» учетных данных типа это значение должно быть задано как on или после даты, с которой сертификат X509 является действительным.</span><span class="sxs-lookup"><span data-stu-id="32aa0-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32aa0-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32aa0-147">-Confirm</span></span>
<span data-ttu-id="32aa0-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="32aa0-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32aa0-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32aa0-149">-WhatIf</span></span>
<span data-ttu-id="32aa0-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="32aa0-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32aa0-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="32aa0-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32aa0-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32aa0-152">CommonParameters</span></span>
<span data-ttu-id="32aa0-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32aa0-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32aa0-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32aa0-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32aa0-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32aa0-155">INPUTS</span></span>

### <span data-ttu-id="32aa0-156">System. String</span><span class="sxs-lookup"><span data-stu-id="32aa0-156">System.String</span></span>

### <span data-ttu-id="32aa0-157">System. String []</span><span class="sxs-lookup"><span data-stu-id="32aa0-157">System.String[]</span></span>

### <span data-ttu-id="32aa0-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="32aa0-158">System.Boolean</span></span>

### <span data-ttu-id="32aa0-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="32aa0-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="32aa0-160">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="32aa0-160">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="32aa0-161">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="32aa0-161">System.Security.SecureString</span></span>

### <span data-ttu-id="32aa0-162">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="32aa0-162">System.DateTime</span></span>

## <span data-ttu-id="32aa0-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32aa0-163">OUTPUTS</span></span>

### <span data-ttu-id="32aa0-164">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="32aa0-164">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="32aa0-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="32aa0-165">NOTES</span></span>
<span data-ttu-id="32aa0-166">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="32aa0-166">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="32aa0-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32aa0-167">RELATED LINKS</span></span>

[<span data-ttu-id="32aa0-168">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="32aa0-168">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="32aa0-169">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="32aa0-169">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="32aa0-170">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="32aa0-170">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="32aa0-171">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="32aa0-171">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="32aa0-172">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="32aa0-172">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="32aa0-173">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="32aa0-173">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
