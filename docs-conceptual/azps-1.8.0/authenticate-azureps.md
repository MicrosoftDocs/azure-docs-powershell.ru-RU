---
title: Вход с помощью Azure PowerShell
description: Сведения о том, как с помощью Azure PowerShell выполнить вход в роли пользователя, субъекта-службы или с помощью управляемых удостоверений для ресурсов Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/20/2019
ms.openlocfilehash: 1e25d4650cc20d7b6613e0efb12ec60d424608c4
ms.sourcegitcommit: 5bdedc77b27b66998387486761ec67ed9326f169
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2019
ms.locfileid: "67345345"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="4a5a1-103">Вход с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4a5a1-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="4a5a1-104">Azure PowerShell поддерживает несколько методов проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="4a5a1-105">Проще всего приступить к работе можно с помощью оболочки [Azure Cloud Shell](/azure/cloud-shell/overview), которая автоматически выполняет вход в вашу учетную запись.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="4a5a1-106">Если используется локальная установка, вы можете выполнить вход в интерактивном режиме с помощью браузера.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="4a5a1-107">При написании скриптов автоматизации рекомендуется использовать [субъект-службу](create-azure-service-principal-azureps.md) с необходимыми разрешениями.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="4a5a1-108">Максимально ограничьте разрешения на вход для своего варианта использования, чтобы обеспечить защиту ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="4a5a1-109">Когда вы войдете, команды будут выполняться в вашей подписке по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="4a5a1-110">Чтобы изменить активную подписку для сеанса, используйте командлет [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="4a5a1-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="4a5a1-111">Чтобы изменить подписку по умолчанию, используемую при входе в систему с помощью Azure PowerShell, используйте командлет [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span><span class="sxs-lookup"><span data-stu-id="4a5a1-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="4a5a1-112">Одни учетные данные можно использовать в нескольких сеансах PowerShell, пока вы остаетесь в системе.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="4a5a1-113">Дополнительные сведения см. в статье [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="4a5a1-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="4a5a1-114">Интерактивный вход</span><span class="sxs-lookup"><span data-stu-id="4a5a1-114">Sign in interactively</span></span>

<span data-ttu-id="4a5a1-115">Чтобы выполнить вход в интерактивном режиме, используйте командлет [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="4a5a1-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="4a5a1-116">При запуске этот командлет представит строку токена.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-116">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="4a5a1-117">Чтобы войти, скопируйте эту строку и вставьте ее в https://microsoft.com/devicelogin в браузере.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-117">To sign in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="4a5a1-118">Сеанс PowerShell пройдет аутентификацию для подключения к Azure.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-118">Your PowerShell session will be authenticated to connect to Azure.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="4a5a1-119">Авторизация с учетными данными (на основе имени пользователя и пароля) была отключена в Azure PowerShell из-за изменений в способах авторизации Active Directory и по соображениям безопасности.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-119">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span>
> <span data-ttu-id="4a5a1-120">Если вы используете авторизацию с учетными данными, чтобы автоматизировать процесс, [создайте субъект-службу](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="4a5a1-120">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

## <a name="sign-in-with-a-service-principal-a-namesp-signin"></a><span data-ttu-id="4a5a1-121">Вход с использованием субъекта-службы <a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="4a5a1-121">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="4a5a1-122">Субъекты-службы не являются интерактивными учетными записями Azure.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-122">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="4a5a1-123">Как и для других учетных записей пользователей, для управления их разрешениями используется Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-123">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="4a5a1-124">Предоставив субъекту-службе только необходимые разрешения, вы обеспечите защиту скриптов автоматизации.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-124">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="4a5a1-125">Сведения о том, как создать субъект-службу для использования с помощью Azure PowerShell, см. в [этой статье](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="4a5a1-125">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="4a5a1-126">Чтобы выполнить вход с помощью субъекта-службы, используйте аргумент `-ServicePrincipal` с командлетом `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-126">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="4a5a1-127">Также потребуется идентификатор приложения субъекта-службы, учетные данные для входа и сопоставление идентификатора клиента с субъектом-службой.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-127">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="4a5a1-128">Способ входа с использованием субъекта-службы будет зависеть от способа аутентификации: на основе пароля или сертификата.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-128">How you sign in with a service principal will depend on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="4a5a1-129">Аутентификация на основе пароля</span><span class="sxs-lookup"><span data-stu-id="4a5a1-129">Password-based authentication</span></span>

<span data-ttu-id="4a5a1-130">Чтобы получить учетные данные субъекта-службы как соответствующий объект, используйте командлет [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="4a5a1-130">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="4a5a1-131">Этот командлет отображает запрос на ввод имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-131">This cmdlet will present a prompt for a username and password.</span></span> <span data-ttu-id="4a5a1-132">Используйте идентификатор субъекта-службы для указанного имени пользователя.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-132">Use the service principal ID for the username.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $pscredential -TenantId $tenantId
```

<span data-ttu-id="4a5a1-133">Если вы используете сценарии автоматизации, вам необходимо создать учетные данные на основе имени пользователя и защищенной строки:</span><span class="sxs-lookup"><span data-stu-id="4a5a1-133">For automation scenarios, you need to create credentials from a user name and secure string:</span></span>

```azurepowershell-interactive
$passwd = ConvertTo-SecureString <use a secure password here> -AsPlainText -Force
$pscredential = New-Object System.Management.Automation.PSCredential('service principal name/id', $passwd)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -TenantId $tenantId
```

<span data-ttu-id="4a5a1-134">При автоматизации подключений субъекта-службы обязательно придерживайтесь рекомендаций по использованию паролей.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-134">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="4a5a1-135">Аутентификация на основе сертификата</span><span class="sxs-lookup"><span data-stu-id="4a5a1-135">Certificate-based authentication</span></span>

<span data-ttu-id="4a5a1-136">Для аутентификации на основе сертификата обязательно, чтобы среда Azure PowerShell могла извлекать данные из локального хранилища сертификатов по отпечатку сертификата.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-136">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>
```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -TenantId $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="4a5a1-137">В PowerShell 5.1 проверять и администрировать хранилище сертификатов можно с помощью модуля [PKI](/powershell/module/pkiclient).</span><span class="sxs-lookup"><span data-stu-id="4a5a1-137">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="4a5a1-138">В PowerShell версии 6.х и выше это не настолько просто.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-138">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="4a5a1-139">Приведенные ниже скрипты демонстрируют, как импортировать существующий сертификат в хранилище сертификатов, к которому имеет доступ PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-139">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="4a5a1-140">Импорт сертификата в PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="4a5a1-140">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="4a5a1-141">Импорт сертификата в PowerShell версии 6.х и выше</span><span class="sxs-lookup"><span data-stu-id="4a5a1-141">Import a certificate in PowerShell Core 6.x and later</span></span>

```azurepowershell-interactive
# Import a PFX
$storeName = [System.Security.Cryptography.X509Certificates.StoreName]::My 
$storeLocation = [System.Security.Cryptography.X509Certificates.StoreLocation]::CurrentUser 
$store = [System.Security.Cryptography.X509Certificates.X509Store]::new($storeName, $storeLocation) 
$certPath = <path to certificate>
$credentials = Get-Credential -Message "Provide PFX private key password"
$flag = [System.Security.Cryptography.X509Certificates.X509KeyStorageFlags]::Exportable 
$certificate = [System.Security.Cryptography.X509Certificates.X509Certificate2]::new($certPath, $credentials.Password, $flag) 
$store.Open([System.Security.Cryptography.X509Certificates.OpenFlags]::ReadWrite) 
$store.Add($Certificate) 
$store.Close()
```

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="4a5a1-142">Вход с использованием управляемого удостоверения</span><span class="sxs-lookup"><span data-stu-id="4a5a1-142">Sign in using a managed identity</span></span> 

<span data-ttu-id="4a5a1-143">Управляемые удостоверения — это функция Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-143">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="4a5a1-144">Они представляют собой субъекты-службы, назначенные ресурсам в Azure.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-144">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="4a5a1-145">Вы можете использовать субъект-службу управляемых удостоверений для входа и получения маркера доступа только для приложений, обеспечив возможность обращения к другим ресурсам.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-145">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="4a5a1-146">Управляемые удостоверения доступны только в ресурсах в облаке Azure.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-146">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="4a5a1-147">Дополнительные сведения об управляемых удостоверениях для ресурсов Azure см. в статье [Как использовать управляемые удостоверения для ресурсов Azure на виртуальной машине Azure для получения маркера доступа](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="4a5a1-147">To learn more about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="4a5a1-148">Вход с использованием нестандартного клиента или в качестве поставщика облачных решений (CSP)</span><span class="sxs-lookup"><span data-stu-id="4a5a1-148">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="4a5a1-149">Если ваша учетная запись связана с несколькими клиентами, для входа в систему обязательно используйте параметр `-TenantId` при подключении.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-149">If your account is associated with more than one tenant, sign-in requires the use of the `-TenantId` parameter when connecting.</span></span> <span data-ttu-id="4a5a1-150">Этот параметр можно применить с любым методом входа.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-150">This parameter will work with any other sign-in method.</span></span> <span data-ttu-id="4a5a1-151">При входе в систему в качестве значения для этого параметра можно указать идентификатор объекта Azure клиента (идентификатор клиента) или полное доменное имя клиента.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-151">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="4a5a1-152">Если вы являетесь [поставщиком облачных решений](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), значением для `-TenantId` **должен** быть идентификатор клиента.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-152">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), the `-TenantId` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="4a5a1-153">Вход в другое облако</span><span class="sxs-lookup"><span data-stu-id="4a5a1-153">Sign in to another Cloud</span></span>

<span data-ttu-id="4a5a1-154">Облачные службы Azure предоставляют среды, которые соответствуют региональным законам об обработке данных.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-154">Azure cloud services offer environments compliant with regional data-handling laws.</span></span>
<span data-ttu-id="4a5a1-155">Для учетных записей в региональном облаке нужно при входе указать среду с помощью аргумента `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="4a5a1-155">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="4a5a1-156">Например, если ваша учетная запись находится в облаке для Китая, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="4a5a1-156">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="4a5a1-157">Следующая команда позволяет получить список доступных сред:</span><span class="sxs-lookup"><span data-stu-id="4a5a1-157">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```