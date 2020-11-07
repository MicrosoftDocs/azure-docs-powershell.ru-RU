---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: d3971c2838b3fed04e1aa38d96e2cd27b2e8276e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567347"
---
# <span data-ttu-id="dc426-101">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="dc426-101">New-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="dc426-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc426-102">SYNOPSIS</span></span>
<span data-ttu-id="dc426-103">Создание привязки сертификата SSL для веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="dc426-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc426-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc426-104">SYNTAX</span></span>

### <span data-ttu-id="dc426-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="dc426-105">S1</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc426-106">S2</span><span class="sxs-lookup"><span data-stu-id="dc426-106">S2</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc426-107">Режима</span><span class="sxs-lookup"><span data-stu-id="dc426-107">S3</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc426-108">Режим</span><span class="sxs-lookup"><span data-stu-id="dc426-108">S4</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc426-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc426-109">DESCRIPTION</span></span>
<span data-ttu-id="dc426-110">Командлет **New-AzureRmWebAppSSLBinding** создает для веб-приложения Azure Связывание сертификата Secure Socket Layer (SSL).</span><span class="sxs-lookup"><span data-stu-id="dc426-110">The **New-AzureRmWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="dc426-111">Командлет создает привязку SSL двумя способами:</span><span class="sxs-lookup"><span data-stu-id="dc426-111">The cmdlet creates an SSL binding in two ways:</span></span> 

- <span data-ttu-id="dc426-112">Вы можете привязать веб-приложение к существующему сертификату.</span><span class="sxs-lookup"><span data-stu-id="dc426-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="dc426-113">Вы можете добавить новый сертификат и затем привязать веб-приложение к этому новому сертификату.</span><span class="sxs-lookup"><span data-stu-id="dc426-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>

<span data-ttu-id="dc426-114">Независимо от того, какой подход вы используете, сертификат и веб-приложение должны быть связаны с одной и той же группой ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="dc426-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="dc426-115">Если у вас есть веб-приложение в группе ресурсов а и вы хотите привязать это веб-приложение к сертификату в группе ресурсов B, единственным способом является Отправка копии сертификата в группу ресурсов A.</span><span class="sxs-lookup"><span data-stu-id="dc426-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A.</span></span>

<span data-ttu-id="dc426-116">Если вы загрузили новый сертификат, имейте в виду следующие требования для SSL-сертификата Azure:</span><span class="sxs-lookup"><span data-stu-id="dc426-116">If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 

- <span data-ttu-id="dc426-117">Сертификат должен содержать закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="dc426-117">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="dc426-118">Сертификат должен использовать формат почтового обмена личной информацией (PFX).</span><span class="sxs-lookup"><span data-stu-id="dc426-118">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="dc426-119">Имя субъекта сертификата должно соответствовать домену, который используется для доступа к веб-приложению.</span><span class="sxs-lookup"><span data-stu-id="dc426-119">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="dc426-120">Сертификат должен использовать не менее 2048-битного шифрования.</span><span class="sxs-lookup"><span data-stu-id="dc426-120">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="dc426-121">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc426-121">EXAMPLES</span></span>

### <span data-ttu-id="dc426-122">Пример 1: привязка сертификата к веб-приложению</span><span class="sxs-lookup"><span data-stu-id="dc426-122">Example 1: Bind a certificate to a Web App</span></span>
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="dc426-123">Эта команда привязывает существующий сертификат Azure (сертификат с отпечатным E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) к веб-приложению с именем ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="dc426-123">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

## <span data-ttu-id="dc426-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc426-124">PARAMETERS</span></span>

### <span data-ttu-id="dc426-125">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="dc426-125">-CertificateFilePath</span></span>
<span data-ttu-id="dc426-126">Задает путь к файлу для сертификата, который нужно отправить.</span><span class="sxs-lookup"><span data-stu-id="dc426-126">Specifies the file path for the certificate to be uploaded.</span></span>

<span data-ttu-id="dc426-127">Параметр *CertificateFilePath* требуется только в том случае, если сертификат еще не был загружен в Azure.</span><span class="sxs-lookup"><span data-stu-id="dc426-127">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc426-128">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="dc426-128">-CertificatePassword</span></span>
<span data-ttu-id="dc426-129">Задает пароль для расшифровки сертификата.</span><span class="sxs-lookup"><span data-stu-id="dc426-129">Specifies the decryption password for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc426-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc426-130">-DefaultProfile</span></span>
<span data-ttu-id="dc426-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc426-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc426-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dc426-132">-Name</span></span>
<span data-ttu-id="dc426-133">Указывает имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="dc426-133">Specifies the name of the Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc426-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc426-134">-ResourceGroupName</span></span>
<span data-ttu-id="dc426-135">Указывает имя группы ресурсов, которой назначен сертификат.</span><span class="sxs-lookup"><span data-stu-id="dc426-135">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="dc426-136">В одной команде нельзя использовать параметры *ResourceGroupName* и *webapp* .</span><span class="sxs-lookup"><span data-stu-id="dc426-136">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc426-137">-Slot</span><span class="sxs-lookup"><span data-stu-id="dc426-137">-Slot</span></span>
<span data-ttu-id="dc426-138">Указывает имя слота развертывания веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="dc426-138">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="dc426-139">Вы можете использовать командлет Get-AzureRMWebAppSlot, чтобы получить доступ к ячейкам.</span><span class="sxs-lookup"><span data-stu-id="dc426-139">You can use the Get-AzureRMWebAppSlot cmdlet to get a slot.</span></span>

<span data-ttu-id="dc426-140">Слоты развертывания предоставляют способ для размещения и проверки веб-приложений без доступа к этим приложениям через Интернет.</span><span class="sxs-lookup"><span data-stu-id="dc426-140">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="dc426-141">Обычно изменения развертываются на промежуточный сайт, проверяют эти изменения, а затем развертываются на рабочем сайте (доступ к Интернету).</span><span class="sxs-lookup"><span data-stu-id="dc426-141">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc426-142">-SslState</span><span class="sxs-lookup"><span data-stu-id="dc426-142">-SslState</span></span>
<span data-ttu-id="dc426-143">Указывает, включен ли сертификат.</span><span class="sxs-lookup"><span data-stu-id="dc426-143">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="dc426-144">Установите для параметра *SSLState* значение 1, чтобы включить сертификат, или установите для *SSLState* значение 0, чтобы отключить сертификат.</span><span class="sxs-lookup"><span data-stu-id="dc426-144">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

```yaml
Type: SslState
Parameter Sets: (All)
Aliases: 
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc426-145">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="dc426-145">-Thumbprint</span></span>
<span data-ttu-id="dc426-146">Указывает уникальный идентификатор сертификата.</span><span class="sxs-lookup"><span data-stu-id="dc426-146">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: S2, S4
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc426-147">-WebApp</span><span class="sxs-lookup"><span data-stu-id="dc426-147">-WebApp</span></span>
<span data-ttu-id="dc426-148">Указывает веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="dc426-148">Specifies a Web App.</span></span>
<span data-ttu-id="dc426-149">Чтобы получить веб-приложение, используйте командлет Get-AzureRmWebApp.</span><span class="sxs-lookup"><span data-stu-id="dc426-149">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

<span data-ttu-id="dc426-150">Параметр *webapp* нельзя использовать в той же команде, что и параметр *ResourceGroupName* , и (или) *WebAppName*.</span><span class="sxs-lookup"><span data-stu-id="dc426-150">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Site
Parameter Sets: S3, S4
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc426-151">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="dc426-151">-WebAppName</span></span>
<span data-ttu-id="dc426-152">Указывает имя веб-приложения, для которого создается новая привязка SSL.</span><span class="sxs-lookup"><span data-stu-id="dc426-152">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>

<span data-ttu-id="dc426-153">В одной команде нельзя использовать параметры *WebAppName* и *webapp* .</span><span class="sxs-lookup"><span data-stu-id="dc426-153">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc426-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc426-154">CommonParameters</span></span>
<span data-ttu-id="dc426-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc426-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc426-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc426-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc426-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc426-157">INPUTS</span></span>

### <span data-ttu-id="dc426-158">Семейств</span><span class="sxs-lookup"><span data-stu-id="dc426-158">Site</span></span>
<span data-ttu-id="dc426-159">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="dc426-159">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="dc426-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc426-160">OUTPUTS</span></span>

## <span data-ttu-id="dc426-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc426-161">NOTES</span></span>

## <span data-ttu-id="dc426-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc426-162">RELATED LINKS</span></span>

[<span data-ttu-id="dc426-163">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="dc426-163">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="dc426-164">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="dc426-164">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="dc426-165">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dc426-165">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="dc426-166">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="dc426-166">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

