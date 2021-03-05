---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: 62e642208e11ece3aeaab009920a5c30b53c0636
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990679"
---
# <span data-ttu-id="f4341-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="f4341-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="f4341-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4341-102">SYNOPSIS</span></span>
<span data-ttu-id="f4341-103">Aggiunge endpoint e metadati per un'istanza di Gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4341-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="f4341-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4341-104">SYNTAX</span></span>

### <span data-ttu-id="f4341-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f4341-105">Name (Default)</span></span>
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

### <span data-ttu-id="f4341-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="f4341-106">ARMEndpoint</span></span>
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

### <span data-ttu-id="f4341-107">Individuazione</span><span class="sxs-lookup"><span data-stu-id="f4341-107">Discovery</span></span>
```
Add-AzEnvironment [-AutoDiscover] [-Uri <Uri>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4341-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f4341-108">DESCRIPTION</span></span>
<span data-ttu-id="f4341-109">Il cmdlet Add-AzEnvironment aggiunge endpoint e metadati per consentire ai cmdlet di Gestione risorse di Azure di connettersi a una nuova istanza di Gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4341-109">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="f4341-110">Gli ambienti predefiniti AzureCloud e AzureChinaCloud si basano su istanze pubbliche esistenti di Gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4341-110">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="f4341-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4341-111">EXAMPLES</span></span>

### <span data-ttu-id="f4341-112">Esempio 1: Creazione e modifica di un nuovo ambiente</span><span class="sxs-lookup"><span data-stu-id="f4341-112">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="f4341-113">In questo esempio viene creato un nuovo ambiente di Azure con endpoint di esempio con Add-AzEnvironment e quindi si modifica il valore degli attributi ActiveDirectoryEndpoint e GraphEndpoint dell'ambiente creato usando il cmdlet Set-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="f4341-113">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

### <span data-ttu-id="f4341-114">Esempio 2: Individuazione di un nuovo ambiente tramite URI</span><span class="sxs-lookup"><span data-stu-id="f4341-114">Example 2: Discovering a new environment via Uri</span></span>
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

<span data-ttu-id="f4341-115">In questo esempio viene individuato un nuovo ambiente di Azure `https://configuredmetadata.net` dall'URI.</span><span class="sxs-lookup"><span data-stu-id="f4341-115">In this example, we are discovering a new Azure environment from the `https://configuredmetadata.net` Uri.</span></span>

## <span data-ttu-id="f4341-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4341-116">PARAMETERS</span></span>

### <span data-ttu-id="f4341-117">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="f4341-117">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="f4341-118">Specifica l'autorità di base per l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f4341-118">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="f4341-119">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f4341-119">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="f4341-120">Specifica il gruppo di destinatari per token che autenticano le richieste agli endpoint di Gestione risorse o Gestione servizi (RDFE) di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4341-120">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="f4341-121">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="f4341-121">-AdTenant</span></span>
<span data-ttu-id="f4341-122">Specifica il tenant di Active Directory predefinito.</span><span class="sxs-lookup"><span data-stu-id="f4341-122">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="f4341-123">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="f4341-123">-ARMEndpoint</span></span>
<span data-ttu-id="f4341-124">Endpoint di Gestione risorse di Azure</span><span class="sxs-lookup"><span data-stu-id="f4341-124">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="f4341-125">-Individuazione automatica</span><span class="sxs-lookup"><span data-stu-id="f4341-125">-AutoDiscover</span></span>
<span data-ttu-id="f4341-126">Individua gli ambienti tramite l'endpoint predefinito o configurato.</span><span class="sxs-lookup"><span data-stu-id="f4341-126">Discovers environments via default or configured endpoint.</span></span>

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

### <span data-ttu-id="f4341-127">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f4341-127">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="f4341-128">Identificatore di risorsa della risorsa di Azure Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="f4341-128">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="f4341-129">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f4341-129">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="f4341-130">Endpoint da usare per la comunicazione con l'API analisi log di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4341-130">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="f4341-131">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f4341-131">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="f4341-132">L'identificatore di risorsa del servizio di attestazione di Azure che è il destinatario del token richiesto.</span><span class="sxs-lookup"><span data-stu-id="f4341-132">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="f4341-133">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f4341-133">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="f4341-134">Suffisso DNS del servizio di attestazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4341-134">Dns suffix of Azure Attestation service.</span></span>

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

### <span data-ttu-id="f4341-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f4341-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="f4341-136">Suffisso Dns dei servizi di catalogo e processo di Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="f4341-136">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="f4341-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f4341-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="f4341-138">Suffisso Dns del fileSystem Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f4341-138">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="f4341-139">Esempio: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="f4341-139">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="f4341-140">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f4341-140">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="f4341-141">Suffisso DNS del servizio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f4341-141">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="f4341-142">Esempio: vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="f4341-142">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="f4341-143">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f4341-143">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="f4341-144">Identificatore di risorsa del servizio dati Azure Key Vault che è il destinatario del token richiesto.</span><span class="sxs-lookup"><span data-stu-id="f4341-144">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="f4341-145">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="f4341-145">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="f4341-146">Endpoint da usare per la comunicazione con l'API analisi log di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4341-146">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="f4341-147">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f4341-147">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="f4341-148">Destinatari per l'autenticazione dei token con l'API di Analisi log di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4341-148">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="f4341-149">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f4341-149">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="f4341-150">L'identificatore di risorsa di Azure Synapse Analytics che è il destinatario del token richiesto.</span><span class="sxs-lookup"><span data-stu-id="f4341-150">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="f4341-151">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f4341-151">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="f4341-152">Suffisso DNS di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f4341-152">Dns suffix of Azure Synapse Analytics.</span></span>

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

### <span data-ttu-id="f4341-153">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f4341-153">-BatchEndpointResourceId</span></span>
<span data-ttu-id="f4341-154">L'identificatore di risorsa del servizio batch di Azure che è il destinatario del token richiesto</span><span class="sxs-lookup"><span data-stu-id="f4341-154">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="f4341-155">-ContainerRegistryEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f4341-155">-ContainerRegistryEndpointSuffix</span></span>
<span data-ttu-id="f4341-156">Suffisso del Registro di sistema del contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4341-156">Suffix of Azure Container Registry.</span></span>

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

### <span data-ttu-id="f4341-157">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="f4341-157">-DataLakeAudience</span></span>
<span data-ttu-id="f4341-158">Destinatari per token di autenticazione con l'Endpoint di Ad Data Lake Services.</span><span class="sxs-lookup"><span data-stu-id="f4341-158">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="f4341-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4341-159">-DefaultProfile</span></span>
<span data-ttu-id="f4341-160">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f4341-160">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4341-161">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="f4341-161">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="f4341-162">Indica che è consentita l'autenticazione locale di Active Directory Federation Services (ADFS).</span><span class="sxs-lookup"><span data-stu-id="f4341-162">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="f4341-163">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="f4341-163">-GalleryEndpoint</span></span>
<span data-ttu-id="f4341-164">Specifica l'endpoint per la raccolta di modelli di distribuzione di Gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4341-164">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="f4341-165">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="f4341-165">-GraphAudience</span></span>
<span data-ttu-id="f4341-166">Gruppo di destinatari per l'autenticazione dei token con l'endpoint di Ad Graph.</span><span class="sxs-lookup"><span data-stu-id="f4341-166">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="f4341-167">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="f4341-167">-GraphEndpoint</span></span>
<span data-ttu-id="f4341-168">Specifica l'URL per le richieste Graph (metadati di Active Directory).</span><span class="sxs-lookup"><span data-stu-id="f4341-168">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="f4341-169">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="f4341-169">-ManagementPortalUrl</span></span>
<span data-ttu-id="f4341-170">Specifica l'URL per il portale di gestione.</span><span class="sxs-lookup"><span data-stu-id="f4341-170">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="f4341-171">-Name</span><span class="sxs-lookup"><span data-stu-id="f4341-171">-Name</span></span>
<span data-ttu-id="f4341-172">Specifica il nome dell'ambiente da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="f4341-172">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="f4341-173">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="f4341-173">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="f4341-174">Specifica l'URL da cui è possibile scaricare i file con estensione publishsettings.</span><span class="sxs-lookup"><span data-stu-id="f4341-174">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="f4341-175">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f4341-175">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="f4341-176">Specifica l'URL per le richieste di Gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4341-176">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="f4341-177">-Scope</span><span class="sxs-lookup"><span data-stu-id="f4341-177">-Scope</span></span>
<span data-ttu-id="f4341-178">Determina l'ambito delle modifiche di contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="f4341-178">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="f4341-179">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f4341-179">-ServiceEndpoint</span></span>
<span data-ttu-id="f4341-180">Specifica l'endpoint per le richieste di gestione del servizio (RDFE).</span><span class="sxs-lookup"><span data-stu-id="f4341-180">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="f4341-181">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f4341-181">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="f4341-182">Specifica il suffisso del nome di dominio per i server di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f4341-182">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="f4341-183">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="f4341-183">-StorageEndpoint</span></span>
<span data-ttu-id="f4341-184">Specifica l'endpoint per l'accesso (BLOB, tabella, coda e file).</span><span class="sxs-lookup"><span data-stu-id="f4341-184">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="f4341-185">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f4341-185">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="f4341-186">Specifica il suffisso del nome di dominio per i servizi di Gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4341-186">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="f4341-187">-Uri</span><span class="sxs-lookup"><span data-stu-id="f4341-187">-Uri</span></span>
<span data-ttu-id="f4341-188">Specifica l'URI della risorsa Internet per recuperare gli ambienti.</span><span class="sxs-lookup"><span data-stu-id="f4341-188">Specifies URI of the internet resource to fetch environments.</span></span>

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

### <span data-ttu-id="f4341-189">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4341-189">-Confirm</span></span>
<span data-ttu-id="f4341-190">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4341-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4341-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4341-191">-WhatIf</span></span>
<span data-ttu-id="f4341-192">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4341-192">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4341-193">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4341-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4341-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4341-194">CommonParameters</span></span>
<span data-ttu-id="f4341-195">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4341-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4341-196">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f4341-196">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4341-197">INPUT</span><span class="sxs-lookup"><span data-stu-id="f4341-197">INPUTS</span></span>

### <span data-ttu-id="f4341-198">System.String</span><span class="sxs-lookup"><span data-stu-id="f4341-198">System.String</span></span>

### <span data-ttu-id="f4341-199">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f4341-199">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f4341-200">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4341-200">OUTPUTS</span></span>

### <span data-ttu-id="f4341-201">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="f4341-201">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="f4341-202">NOTE</span><span class="sxs-lookup"><span data-stu-id="f4341-202">NOTES</span></span>

## <span data-ttu-id="f4341-203">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4341-203">RELATED LINKS</span></span>

[<span data-ttu-id="f4341-204">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="f4341-204">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="f4341-205">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="f4341-205">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="f4341-206">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="f4341-206">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

