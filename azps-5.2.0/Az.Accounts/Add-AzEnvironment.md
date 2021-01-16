---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: 92a8c816f1c5a76b0f3725b70a627b798b9de2b0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329031"
---
# <span data-ttu-id="2612a-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="2612a-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="2612a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2612a-102">SYNOPSIS</span></span>
<span data-ttu-id="2612a-103">Добавляет конечные точки и метаданные для экземпляра Диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="2612a-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="2612a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2612a-104">SYNTAX</span></span>

### <span data-ttu-id="2612a-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2612a-105">Name (Default)</span></span>
```
Add-AzEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [[-BatchEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpoint] <String>] [-AzureAnalysisServicesEndpointSuffix <String>]
 [-AzureAnalysisServicesEndpointResourceId <String>] [-AzureAttestationServiceEndpointSuffix <String>]
 [-AzureAttestationServiceEndpointResourceId <String>] [-AzureSynapseAnalyticsEndpointSuffix <String>]
 [-ContainerRegistryEndpointSuffix <String>] [-AzureSynapseAnalyticsEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2612a-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="2612a-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-ContainerRegistryEndpointSuffix <String>]
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2612a-107">Обнаружение</span><span class="sxs-lookup"><span data-stu-id="2612a-107">Discovery</span></span>
```
Add-AzEnvironment [-AutoDiscover] [-Uri <Uri>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2612a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2612a-108">DESCRIPTION</span></span>
<span data-ttu-id="2612a-109">Новый Add-AzEnvironment добавляет конечные точки и метаданные, чтобы обеспечить подключение диспетчера ресурсов Azure к новому экземпляру Диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="2612a-109">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="2612a-110">Встроенные среды AzureCloud и AzureChinaCloud нацелены на существующие общедоступные экземпляры Диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="2612a-110">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="2612a-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2612a-111">EXAMPLES</span></span>

### <span data-ttu-id="2612a-112">Пример 1. Создание и изменение новой среды</span><span class="sxs-lookup"><span data-stu-id="2612a-112">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Set-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint NewTestADEndpoint `
        -GraphEndpoint NewTestGraphEndpoint | Format-List

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
OnPremise                                         : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              :
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : NewTestADEndpoint
GraphUrl                                          : NewTestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
DataLakeEndpointResourceId                        :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
AzureOperationalInsightsEndpointResourceId        :
AzureOperationalInsightsEndpoint                  :
AzureAnalysisServicesEndpointSuffix               :
AzureAttestationServiceEndpointSuffix             :
AzureAttestationServiceEndpointResourceId         :
AzureSynapseAnalyticsEndpointSuffix               :
AzureSynapseAnalyticsEndpointResourceId           :
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :
```

<span data-ttu-id="2612a-113">В этом примере мы создаем новую среду Azure с образцами конечных точек с помощью Add-AzEnvironment, а затем изменяем значение атрибутов ActiveDirectoryEndpoint и GraphEndpoint созданной среды с помощью cmdlet Set-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="2612a-113">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

### <span data-ttu-id="2612a-114">Пример 2. Обнаружение новой среды с помощью URI</span><span class="sxs-lookup"><span data-stu-id="2612a-114">Example 2: Discovering a new environment via Uri</span></span>
```
<#
Uri https://configuredmetadata.net returns an array of environment metadata. The following example contains a payload for the AzureCloud default environment.

[
  {
    "portal": "https://portal.azure.com",
    "authentication": {
      "loginEndpoint": "https://login.microsoftonline.com/",
      "audiences": [
        "https://management.core.windows.net/"
      ],
      "tenant": "common",
      "identityProvider": "AAD"
    },
    "media": "https://rest.media.azure.net",
    "graphAudience": "https://graph.windows.net/",
    "graph": "https://graph.windows.net/",
    "name": "AzureCloud",
    "suffixes": {
      "azureDataLakeStoreFileSystem": "azuredatalakestore.net",
      "acrLoginServer": "azurecr.io",
      "sqlServerHostname": ".database.windows.net",
      "azureDataLakeAnalyticsCatalogAndJob": "azuredatalakeanalytics.net",
      "keyVaultDns": "vault.azure.net",
      "storage": "core.windows.net",
      "azureFrontDoorEndpointSuffix": "azurefd.net"
    },
    "batch": "https://batch.core.windows.net/",
    "resourceManager": "https://management.azure.com/",
    "vmImageAliasDoc": "https://raw.githubusercontent.com/Azure/azure-rest-api-specs/master/arm-compute/quickstart-templates/aliases.json",
    "activeDirectoryDataLake": "https://datalake.azure.net/",
    "sqlManagement": "https://management.core.windows.net:8443/",
    "gallery": "https://gallery.azure.com/"
  },
……
]
#>

PS C:\> Add-AzEnvironment -AutoDiscover -Uri https://configuredmetadata.net

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="2612a-115">В этом примере мы обнаруживаем новую среду Azure из `https://configuredmetadata.net` URI.</span><span class="sxs-lookup"><span data-stu-id="2612a-115">In this example, we are discovering a new Azure environment from the `https://configuredmetadata.net` Uri.</span></span>

## <span data-ttu-id="2612a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2612a-116">PARAMETERS</span></span>

### <span data-ttu-id="2612a-117">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="2612a-117">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="2612a-118">Указывает базовый орган проверки подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2612a-118">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-119">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="2612a-119">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="2612a-120">Определяет аудиторию для маркеров, которые запрашивают проверку подлинности в конечных точках диспетчера ресурсов Azure или службы управления службами.</span><span class="sxs-lookup"><span data-stu-id="2612a-120">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-121">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="2612a-121">-AdTenant</span></span>
<span data-ttu-id="2612a-122">Определяет клиент Active Directory по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2612a-122">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-123">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="2612a-123">-ARMEndpoint</span></span>
<span data-ttu-id="2612a-124">Конечная точка Диспетчера ресурсов Azure</span><span class="sxs-lookup"><span data-stu-id="2612a-124">The Azure Resource Manager endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: ARMEndpoint
Aliases: ArmUrl

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-125">-AutoDiscover</span><span class="sxs-lookup"><span data-stu-id="2612a-125">-AutoDiscover</span></span>
<span data-ttu-id="2612a-126">Обнаружение сред через стандартную или настроенную конечную точку.</span><span class="sxs-lookup"><span data-stu-id="2612a-126">Discovers environments via default or configured endpoint.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Discovery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-127">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="2612a-127">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="2612a-128">Идентификатор ресурса Служб Аналитики Azure.</span><span class="sxs-lookup"><span data-stu-id="2612a-128">The resource identifier of the Azure Analysis Services resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-129">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="2612a-129">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="2612a-130">Конечная точка, используемая при общении с azure Log Analytics API.</span><span class="sxs-lookup"><span data-stu-id="2612a-130">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-131">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="2612a-131">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="2612a-132">Идентификатор ресурса службы Azure Attestation, который является получателем запрашиваемого маркера.</span><span class="sxs-lookup"><span data-stu-id="2612a-132">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-133">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="2612a-133">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="2612a-134">DNS-суффикс службы Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="2612a-134">Dns suffix of Azure Attestation service.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="2612a-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="2612a-136">DNS-суффикс служб Azure Data Lake Analytics и служб каталога</span><span class="sxs-lookup"><span data-stu-id="2612a-136">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="2612a-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="2612a-138">Суффикс DNS для Azure Data Lake Store FileSystem.</span><span class="sxs-lookup"><span data-stu-id="2612a-138">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="2612a-139">Пример: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="2612a-139">Example: azuredatalake.net</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-140">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="2612a-140">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="2612a-141">DNS-суффикс службы хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="2612a-141">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="2612a-142">Пример: vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="2612a-142">Example is vault-int.azure-int.net</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-143">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="2612a-143">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="2612a-144">Идентификатор ресурса службы данных хранилища ключа Azure, который является получателем запрашиваемого маркера.</span><span class="sxs-lookup"><span data-stu-id="2612a-144">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-145">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="2612a-145">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="2612a-146">Конечная точка, используемая при общении с azure Log Analytics API.</span><span class="sxs-lookup"><span data-stu-id="2612a-146">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-147">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="2612a-147">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="2612a-148">Аудитория для проверки подлинности токенов с помощью API Azure Log Analytics.</span><span class="sxs-lookup"><span data-stu-id="2612a-148">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-149">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="2612a-149">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="2612a-150">Идентификатор ресурса средства аналитики Azure SynapseAnalytics, который является получателем запрашиваемого маркера.</span><span class="sxs-lookup"><span data-stu-id="2612a-150">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-151">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="2612a-151">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="2612a-152">DNS-суффикс службы Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="2612a-152">Dns suffix of Azure Synapse Analytics.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-153">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="2612a-153">-BatchEndpointResourceId</span></span>
<span data-ttu-id="2612a-154">Идентификатор ресурса службы Azure Batch, который является получателем запрашиваемого маркера.</span><span class="sxs-lookup"><span data-stu-id="2612a-154">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: BatchResourceId, BatchAudience

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-155">-ContainerRegistryEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="2612a-155">-ContainerRegistryEndpointSuffix</span></span>
<span data-ttu-id="2612a-156">Суффикс реестра контейнеров Azure.</span><span class="sxs-lookup"><span data-stu-id="2612a-156">Suffix of Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-157">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="2612a-157">-DataLakeAudience</span></span>
<span data-ttu-id="2612a-158">Аудитория маркеров для проверки подлинности с помощью конечной точки служб AD Data Lake services.</span><span class="sxs-lookup"><span data-stu-id="2612a-158">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2612a-159">-DefaultProfile</span></span>
<span data-ttu-id="2612a-160">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2612a-160">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2612a-161">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="2612a-161">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="2612a-162">Указывает на то, что разрешена проверка локальной проверки подлинности в службах федерации Active Directory (ADFS).</span><span class="sxs-lookup"><span data-stu-id="2612a-162">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Name
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-163">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="2612a-163">-GalleryEndpoint</span></span>
<span data-ttu-id="2612a-164">Указывает конечную точку для коллекции шаблонов развертывания Диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="2612a-164">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-165">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="2612a-165">-GraphAudience</span></span>
<span data-ttu-id="2612a-166">Аудитория маркеров для проверки подлинности с помощью конечной точки AD Graph.</span><span class="sxs-lookup"><span data-stu-id="2612a-166">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-167">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="2612a-167">-GraphEndpoint</span></span>
<span data-ttu-id="2612a-168">Url-адрес запросов Graph (метаданных Active Directory).</span><span class="sxs-lookup"><span data-stu-id="2612a-168">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-169">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="2612a-169">-ManagementPortalUrl</span></span>
<span data-ttu-id="2612a-170">Url-адрес портала управления.</span><span class="sxs-lookup"><span data-stu-id="2612a-170">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-171">-Name</span><span class="sxs-lookup"><span data-stu-id="2612a-171">-Name</span></span>
<span data-ttu-id="2612a-172">Указывает имя добавляемой среды.</span><span class="sxs-lookup"><span data-stu-id="2612a-172">Specifies the name of the environment to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-173">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="2612a-173">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="2612a-174">Url-адрес, с которого можно скачать файлы Publishsettings.</span><span class="sxs-lookup"><span data-stu-id="2612a-174">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-175">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2612a-175">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="2612a-176">URL-адрес запросов Диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="2612a-176">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-177">-Scope</span><span class="sxs-lookup"><span data-stu-id="2612a-177">-Scope</span></span>
<span data-ttu-id="2612a-178">Определяет область изменения контекста, например, применяются ли изменения только к текущему процессу или же к всем сеансам, на которые начал пользователь.</span><span class="sxs-lookup"><span data-stu-id="2612a-178">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-179">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="2612a-179">-ServiceEndpoint</span></span>
<span data-ttu-id="2612a-180">Указывает конечную точку для запросов на управление службами (RDFE).</span><span class="sxs-lookup"><span data-stu-id="2612a-180">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-181">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="2612a-181">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="2612a-182">Определяет суффикс доменного имени для серверов баз данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="2612a-182">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-183">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="2612a-183">-StorageEndpoint</span></span>
<span data-ttu-id="2612a-184">Указывает конечную точку доступа к хранилищу (BLOB-файлы, таблицы, очереди и файла).</span><span class="sxs-lookup"><span data-stu-id="2612a-184">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-185">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="2612a-185">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="2612a-186">Определяет суффикс доменного имени для служб Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="2612a-186">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-187">-Uri</span><span class="sxs-lookup"><span data-stu-id="2612a-187">-Uri</span></span>
<span data-ttu-id="2612a-188">Определяет URI интернет-ресурса для выборки сред.</span><span class="sxs-lookup"><span data-stu-id="2612a-188">Specifies URI of the internet resource to fetch environments.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Discovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-189">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2612a-189">-Confirm</span></span>
<span data-ttu-id="2612a-190">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2612a-190">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2612a-191">-WhatIf</span></span>
<span data-ttu-id="2612a-192">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2612a-192">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2612a-193">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2612a-193">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2612a-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2612a-194">CommonParameters</span></span>
<span data-ttu-id="2612a-195">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2612a-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2612a-196">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2612a-196">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2612a-197">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2612a-197">INPUTS</span></span>

### <span data-ttu-id="2612a-198">System.String</span><span class="sxs-lookup"><span data-stu-id="2612a-198">System.String</span></span>

### <span data-ttu-id="2612a-199">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2612a-199">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2612a-200">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2612a-200">OUTPUTS</span></span>

### <span data-ttu-id="2612a-201">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="2612a-201">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="2612a-202">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2612a-202">NOTES</span></span>

## <span data-ttu-id="2612a-203">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2612a-203">RELATED LINKS</span></span>

[<span data-ttu-id="2612a-204">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="2612a-204">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="2612a-205">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="2612a-205">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="2612a-206">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="2612a-206">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)
