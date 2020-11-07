---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: d0ba19efaf0cf3dc1f997d06231e056fb20b02f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562139"
---
# <span data-ttu-id="5b213-101">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5b213-101">Remove-AzureRmServiceFabricClientCertificate</span></span>

## <span data-ttu-id="5b213-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5b213-102">SYNOPSIS</span></span>
<span data-ttu-id="5b213-103">Для проверки подлинности клиента в кластере удалите клиентские сертификаты или имена субъектов сертификата (-ов).</span><span class="sxs-lookup"><span data-stu-id="5b213-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b213-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5b213-104">SYNTAX</span></span>

### <span data-ttu-id="5b213-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="5b213-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b213-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="5b213-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b213-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="5b213-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b213-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="5b213-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b213-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b213-109">DESCRIPTION</span></span>
<span data-ttu-id="5b213-110">С помощью средства **Remove-AzureRmServiceFabricClientCertificate** можно удалить из домена клиентские сертификаты или имена субъектов сертификатов для проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="5b213-110">Use **Remove-AzureRmServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="5b213-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5b213-111">EXAMPLES</span></span>

### <span data-ttu-id="5b213-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5b213-112">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="5b213-113">Эта команда удалит сертификат клиента с отпечатком "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" из кластера.</span><span class="sxs-lookup"><span data-stu-id="5b213-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="5b213-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5b213-114">PARAMETERS</span></span>

### <span data-ttu-id="5b213-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="5b213-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="5b213-116">Укажите отпечаток сертификата клиента, у которого есть разрешение администратора.</span><span class="sxs-lookup"><span data-stu-id="5b213-116">Specify client certificate thumbprint that only has admin permission.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b213-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="5b213-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="5b213-118">Укажите общее имя клиента, отпечаток поставщика и тип проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="5b213-118">Specify client common name, issuer thumbprint, and authentication type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b213-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="5b213-119">-CommonName</span></span>
<span data-ttu-id="5b213-120">Укажите общее имя сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="5b213-120">Specify client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b213-121">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="5b213-121">-IssuerThumbprint</span></span>
<span data-ttu-id="5b213-122">Укажите отпечаток поставщика сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="5b213-122">Specify client certificate issuer thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b213-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5b213-123">-Name</span></span>
<span data-ttu-id="5b213-124">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="5b213-124">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b213-125">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="5b213-125">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="5b213-126">Укажите отпечаток сертификата клиента с разрешением только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5b213-126">Specify client certificate thumbprint that has read only permission.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b213-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b213-127">-ResourceGroupName</span></span>
<span data-ttu-id="5b213-128">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5b213-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5b213-129">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="5b213-129">-Thumbprint</span></span>
<span data-ttu-id="5b213-130">Укажите отпечаток сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="5b213-130">Specify client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b213-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b213-131">-Confirm</span></span>
<span data-ttu-id="5b213-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5b213-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b213-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b213-133">-WhatIf</span></span>
<span data-ttu-id="5b213-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5b213-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b213-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5b213-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b213-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b213-136">-DefaultProfile</span></span>
<span data-ttu-id="5b213-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b213-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b213-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b213-138">CommonParameters</span></span>
<span data-ttu-id="5b213-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5b213-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b213-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b213-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b213-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5b213-141">INPUTS</span></span>

### <span data-ttu-id="5b213-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5b213-142">System.Collections.Hashtable</span></span>
<span data-ttu-id="5b213-143">System. String</span><span class="sxs-lookup"><span data-stu-id="5b213-143">System.String</span></span>

<span data-ttu-id="5b213-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5b213-144">System.Boolean</span></span>

## <span data-ttu-id="5b213-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b213-145">OUTPUTS</span></span>

### <span data-ttu-id="5b213-146">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="5b213-146">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="5b213-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="5b213-147">NOTES</span></span>

## <span data-ttu-id="5b213-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b213-148">RELATED LINKS</span></span>

[<span data-ttu-id="5b213-149">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5b213-149">Add-AzureRmServiceFabricClientCertificate</span></span>](./Add-AzureRmServiceFabricClientCertificate.md)