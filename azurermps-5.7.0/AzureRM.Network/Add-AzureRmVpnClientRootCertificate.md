---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 11b4d3cca8d7cad8d3fb4cfcc4e256d1934592d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559032"
---
# <span data-ttu-id="de3fd-101">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="de3fd-101">Add-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="de3fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="de3fd-102">SYNOPSIS</span></span>
<span data-ttu-id="de3fd-103">Добавляет корневой сертификат VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="de3fd-103">Adds a VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de3fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="de3fd-104">SYNTAX</span></span>

```
Add-AzureRmVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de3fd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de3fd-105">DESCRIPTION</span></span>
<span data-ttu-id="de3fd-106">Командлет **Add-AzureRmVpnClientRootCertificate** добавляет корневой сертификат в шлюз виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="de3fd-106">The **Add-AzureRmVpnClientRootCertificate** cmdlet adds a root certificate to a virtual network gateway.</span></span>
<span data-ttu-id="de3fd-107">Корневые сертификаты — это сертификаты X. 509, определяющие корневой центр сертификации.</span><span class="sxs-lookup"><span data-stu-id="de3fd-107">Root certificates are X.509 certificates that identify your Root Certification Authority.</span></span>
<span data-ttu-id="de3fd-108">По дизайну все сертификаты, используемые на шлюзе, доверяют корневому сертификату.</span><span class="sxs-lookup"><span data-stu-id="de3fd-108">By design, all certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="de3fd-109">Этот командлет назначает существующий сертификат как корневой сертификат шлюза.</span><span class="sxs-lookup"><span data-stu-id="de3fd-109">This cmdlet assigns an existing certificate as a gateway root certificate.</span></span>
<span data-ttu-id="de3fd-110">Если у вас нет сертификата X. 509, вы можете создать его с помощью инфраструктуры открытых ключей или использовать генератор сертификатов, например makecert.exe.</span><span class="sxs-lookup"><span data-stu-id="de3fd-110">If you do not have an X.509 certificate available you can generate one through your public key infrastructure or use a certificate generator such as makecert.exe.</span></span>

<span data-ttu-id="de3fd-111">Чтобы добавить корневой сертификат, необходимо указать имя сертификата и предоставить текстовое представление сертификата (Подробнее об этом можно узнать в параметре *PublicCertData* ).</span><span class="sxs-lookup"><span data-stu-id="de3fd-111">To add a root certificate, you must specify the certificate name and provide a text-only representation of the certificate (see *the PublicCertData* parameter for more information).</span></span>
<span data-ttu-id="de3fd-112">Azure позволяет назначать шлюзу более одного корневого сертификата.</span><span class="sxs-lookup"><span data-stu-id="de3fd-112">Azure allows you to assign more than one root certificate to a gateway.</span></span>
<span data-ttu-id="de3fd-113">Множественные корневые сертификаты часто развертываются организациями, которые включают пользователей из нескольких компаний.</span><span class="sxs-lookup"><span data-stu-id="de3fd-113">Multiple root certificates are often deployed by organizations that include users from more than one company.</span></span>

## <span data-ttu-id="de3fd-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="de3fd-114">EXAMPLES</span></span>

### <span data-ttu-id="de3fd-115">Пример 1: Добавление корневого сертификата клиента на виртуальный шлюз</span><span class="sxs-lookup"><span data-stu-id="de3fd-115">Example 1: Add a client root certificate to a virtual gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

<span data-ttu-id="de3fd-116">В этом примере добавляется корневой сертификат клиента на виртуальный шлюз с именем ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="de3fd-116">This example adds a client root certificate to a virtual gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="de3fd-117">Первая команда использует командлет **Get-Content** для получения ранее экспортированного текстового представления корневого сертификата и сохраняет эти текстовые данные переменной с именем $text.</span><span class="sxs-lookup"><span data-stu-id="de3fd-117">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the root certificate and stores that text data the variable named $Text.</span></span>

<span data-ttu-id="de3fd-118">Вторая команда использует цикл for для извлечения всего текста за исключением первой строки и последней строки.</span><span class="sxs-lookup"><span data-stu-id="de3fd-118">The second command then uses a for loop to extract all the text except for the first line and the last line.</span></span>
<span data-ttu-id="de3fd-119">Извлеченный текст хранится в переменной с именем $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="de3fd-119">The extracted text is stored in a variable named $CertificateText.</span></span>

<span data-ttu-id="de3fd-120">Третья команда затем использует текст, хранящийся в $CertificateText, с помощью командлета **Add-AzureRmVpnClientRootCertificate** , чтобы добавить корневой сертификат в шлюз.</span><span class="sxs-lookup"><span data-stu-id="de3fd-120">The third command then uses the text stored in $CertificateText with the **Add-AzureRmVpnClientRootCertificate** cmdlet to add the root certificate to the gateway.</span></span>

## <span data-ttu-id="de3fd-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="de3fd-121">PARAMETERS</span></span>

### <span data-ttu-id="de3fd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de3fd-122">-DefaultProfile</span></span>
<span data-ttu-id="de3fd-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="de3fd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de3fd-124">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="de3fd-124">-PublicCertData</span></span>
<span data-ttu-id="de3fd-125">Указывает текстовое представление корневого сертификата, который нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="de3fd-125">Specifies the text representation of the root certificate to be added.</span></span>
<span data-ttu-id="de3fd-126">Чтобы получить текстовое представление, экспортируйте его в формате CER (с помощью кодировки Base64), а затем откройте полученный файл в текстовом редакторе.</span><span class="sxs-lookup"><span data-stu-id="de3fd-126">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="de3fd-127">После этого вывод будет выглядеть примерно так: Обратите внимание на то, что фактический результат будет содержать гораздо больше строк, чем сокращенный образец, показанный здесь.</span><span class="sxs-lookup"><span data-stu-id="de3fd-127">When you do that, you will see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="de3fd-128">-----"Начало-----сертификата" MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----конец сертификата-----</span><span class="sxs-lookup"><span data-stu-id="de3fd-128">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="de3fd-129">PublicCertData состоит из всех строк между первой строкой (-----"начало-----сертификата") и последней строки (-----конец сертификата-----) в файле.</span><span class="sxs-lookup"><span data-stu-id="de3fd-129">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="de3fd-130">Эти данные можно получить с помощью команд Windows PowerShell, подобных приведенным ниже. `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span><span class="sxs-lookup"><span data-stu-id="de3fd-130">You can retrieve this data  by using Windows PowerShell commands similar to this: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de3fd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de3fd-131">-ResourceGroupName</span></span>
<span data-ttu-id="de3fd-132">Указывает имя группы ресурсов, которой назначен корневой сертификат.</span><span class="sxs-lookup"><span data-stu-id="de3fd-132">Specifies the name of the resource group that the root certificate is assigned to.</span></span>

<span data-ttu-id="de3fd-133">Группы ресурсов классифицируют элементы для облегчения управления запасами и общего администрирования Azure.</span><span class="sxs-lookup"><span data-stu-id="de3fd-133">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de3fd-134">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="de3fd-134">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="de3fd-135">Указывает имя шлюза виртуальной сети, в который добавляется сертификат.</span><span class="sxs-lookup"><span data-stu-id="de3fd-135">Specifies the name of the virtual network gateway where the certificate is added.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de3fd-136">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="de3fd-136">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="de3fd-137">Указывает имя корневого сертификата клиента, который добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="de3fd-137">Specifies the name of the client root certificate that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de3fd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de3fd-138">CommonParameters</span></span>
<span data-ttu-id="de3fd-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="de3fd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de3fd-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de3fd-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de3fd-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="de3fd-141">INPUTS</span></span>

### <span data-ttu-id="de3fd-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="de3fd-142">None</span></span>
<span data-ttu-id="de3fd-143">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="de3fd-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="de3fd-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="de3fd-144">OUTPUTS</span></span>

### <span data-ttu-id="de3fd-145">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="de3fd-145">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="de3fd-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="de3fd-146">NOTES</span></span>

## <span data-ttu-id="de3fd-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de3fd-147">RELATED LINKS</span></span>

[<span data-ttu-id="de3fd-148">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="de3fd-148">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="de3fd-149">New-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="de3fd-149">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="de3fd-150">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="de3fd-150">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)

