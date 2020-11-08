---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: 2db2e90dc1292bdfe67907e5a180b08a09a54718
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201743"
---
# <span data-ttu-id="4f47c-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="4f47c-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="4f47c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4f47c-102">SYNOPSIS</span></span>
<span data-ttu-id="4f47c-103">Aggiunge endpoint e metadati per un'istanza di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="4f47c-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="4f47c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f47c-104">SYNTAX</span></span>

### <span data-ttu-id="4f47c-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4f47c-105">Name (Default)</span></span>
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
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f47c-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f47c-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-AzureSynapseAnalyticsEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f47c-107">Scoperta</span><span class="sxs-lookup"><span data-stu-id="4f47c-107">Discovery</span></span>
```
Add-AzEnvironment -AutoDiscover [-Uri <Uri>] [-Scope {Process | CurrentUser}]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f47c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f47c-108">DESCRIPTION</span></span>
<span data-ttu-id="4f47c-109">Il cmdlet Add-AzEnvironment aggiunge endpoint e metadati per consentire ai cmdlet di Azure Resource Manager di connettersi con una nuova istanza di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="4f47c-109">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="4f47c-110">Gli ambienti predefiniti AzureCloud e AzureChinaCloud sono destinati alle istanze pubbliche esistenti di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="4f47c-110">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="4f47c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f47c-111">EXAMPLES</span></span>

### <span data-ttu-id="4f47c-112">Esempio 1: creazione e modifica di un nuovo ambiente</span><span class="sxs-lookup"><span data-stu-id="4f47c-112">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="4f47c-113">In questo esempio creiamo un nuovo ambiente Azure con endpoint di esempio usando Add-AzEnvironment e quindi modifichiamo il valore degli attributi ActiveDirectoryEndpoint e GraphEndpoint dell'ambiente creato usando il cmdlet Set-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="4f47c-113">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

### <span data-ttu-id="4f47c-114">Esempio 2: individuazione di un nuovo ambiente tramite URI</span><span class="sxs-lookup"><span data-stu-id="4f47c-114">Example 2: Discovering a new environment via Uri</span></span>
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

<span data-ttu-id="4f47c-115">In questo esempio, stiamo scoprendo un nuovo ambiente Azure dall' `https://configuredmetadata.net` URI.</span><span class="sxs-lookup"><span data-stu-id="4f47c-115">In this example, we are discovering a new Azure environment from the `https://configuredmetadata.net` Uri.</span></span>

## <span data-ttu-id="4f47c-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4f47c-116">PARAMETERS</span></span>

### <span data-ttu-id="4f47c-117">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f47c-117">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="4f47c-118">Specifica l'autorità di base per l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4f47c-118">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="4f47c-119">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4f47c-119">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="4f47c-120">Specifica il gruppo di destinatari per i token che eseguono l'autenticazione delle richieste agli endpoint di Azure Resource Manager o RDFE (Service Management).</span><span class="sxs-lookup"><span data-stu-id="4f47c-120">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="4f47c-121">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="4f47c-121">-AdTenant</span></span>
<span data-ttu-id="4f47c-122">Specifica il tenant di Active Directory predefinito.</span><span class="sxs-lookup"><span data-stu-id="4f47c-122">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="4f47c-123">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f47c-123">-ARMEndpoint</span></span>
<span data-ttu-id="4f47c-124">Endpoint di Azure Resource Manager</span><span class="sxs-lookup"><span data-stu-id="4f47c-124">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="4f47c-125">-Individuazione automatica</span><span class="sxs-lookup"><span data-stu-id="4f47c-125">-AutoDiscover</span></span>
<span data-ttu-id="4f47c-126">Individua gli ambienti tramite endpoint predefinito o configurato.</span><span class="sxs-lookup"><span data-stu-id="4f47c-126">Discovers environments via default or configured endpoint.</span></span>

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

### <span data-ttu-id="4f47c-127">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4f47c-127">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="4f47c-128">Identificatore delle risorse della risorsa di Azure Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="4f47c-128">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="4f47c-129">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4f47c-129">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="4f47c-130">Endpoint da usare per comunicare con l'API di analisi di Azure log.</span><span class="sxs-lookup"><span data-stu-id="4f47c-130">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="4f47c-131">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4f47c-131">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="4f47c-132">Identificatore della risorsa del servizio di attestazione di Azure che è il destinatario del token richiesto.</span><span class="sxs-lookup"><span data-stu-id="4f47c-132">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="4f47c-133">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4f47c-133">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="4f47c-134">Suffisso DNS del servizio di attestazione Azure.</span><span class="sxs-lookup"><span data-stu-id="4f47c-134">Dns suffix of Azure Attestation service.</span></span>

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

### <span data-ttu-id="4f47c-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4f47c-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="4f47c-136">Suffisso DNS dei servizi di catalogo e lavoro di Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="4f47c-136">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="4f47c-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4f47c-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="4f47c-138">Suffisso DNS di Azure Data Lake Store FileSystem.</span><span class="sxs-lookup"><span data-stu-id="4f47c-138">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="4f47c-139">Esempio: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="4f47c-139">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="4f47c-140">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="4f47c-140">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="4f47c-141">Suffisso DNS del servizio Key Vault di Azure.</span><span class="sxs-lookup"><span data-stu-id="4f47c-141">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="4f47c-142">L'esempio è vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="4f47c-142">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="4f47c-143">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4f47c-143">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="4f47c-144">Identificatore delle risorse del servizio dati di Azure Key Vault che è il destinatario del token richiesto.</span><span class="sxs-lookup"><span data-stu-id="4f47c-144">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="4f47c-145">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f47c-145">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="4f47c-146">Endpoint da usare per comunicare con l'API di analisi di Azure log.</span><span class="sxs-lookup"><span data-stu-id="4f47c-146">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="4f47c-147">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4f47c-147">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="4f47c-148">Il gruppo di destinatari per l'autenticazione dei token con l'API di analisi del log di Azure.</span><span class="sxs-lookup"><span data-stu-id="4f47c-148">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="4f47c-149">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4f47c-149">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="4f47c-150">Identificatore della risorsa dell'analisi delle sinapsi di Azure che rappresenta il destinatario del token richiesto.</span><span class="sxs-lookup"><span data-stu-id="4f47c-150">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="4f47c-151">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4f47c-151">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="4f47c-152">Suffisso DNS di Azure sinapsi Analytics.</span><span class="sxs-lookup"><span data-stu-id="4f47c-152">Dns suffix of Azure Synapse Analytics.</span></span>

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

### <span data-ttu-id="4f47c-153">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4f47c-153">-BatchEndpointResourceId</span></span>
<span data-ttu-id="4f47c-154">Identificatore delle risorse del servizio batch di Azure che è il destinatario del token richiesto</span><span class="sxs-lookup"><span data-stu-id="4f47c-154">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="4f47c-155">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="4f47c-155">-DataLakeAudience</span></span>
<span data-ttu-id="4f47c-156">Il gruppo di destinatari per l'autenticazione dei token con l'endpoint di servizi AD data Lake.</span><span class="sxs-lookup"><span data-stu-id="4f47c-156">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="4f47c-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f47c-157">-DefaultProfile</span></span>
<span data-ttu-id="4f47c-158">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4f47c-158">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f47c-159">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="4f47c-159">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="4f47c-160">Indica che l'autenticazione locale di Active Directory Federation Services (ADFS) è consentita.</span><span class="sxs-lookup"><span data-stu-id="4f47c-160">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="4f47c-161">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f47c-161">-GalleryEndpoint</span></span>
<span data-ttu-id="4f47c-162">Specifica l'endpoint della raccolta di modelli di distribuzione di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="4f47c-162">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="4f47c-163">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="4f47c-163">-GraphAudience</span></span>
<span data-ttu-id="4f47c-164">Il gruppo di destinatari per l'autenticazione dei token con l'endpoint del grafico AD.</span><span class="sxs-lookup"><span data-stu-id="4f47c-164">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="4f47c-165">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f47c-165">-GraphEndpoint</span></span>
<span data-ttu-id="4f47c-166">Specifica l'URL per le richieste di grafico (metadati Active Directory).</span><span class="sxs-lookup"><span data-stu-id="4f47c-166">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="4f47c-167">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="4f47c-167">-ManagementPortalUrl</span></span>
<span data-ttu-id="4f47c-168">Specifica l'URL per il portale di gestione.</span><span class="sxs-lookup"><span data-stu-id="4f47c-168">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="4f47c-169">-Nome</span><span class="sxs-lookup"><span data-stu-id="4f47c-169">-Name</span></span>
<span data-ttu-id="4f47c-170">Specifica il nome dell'ambiente da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="4f47c-170">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="4f47c-171">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="4f47c-171">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="4f47c-172">Specifica l'URL da cui possono essere scaricati i file con estensione publishsettings.</span><span class="sxs-lookup"><span data-stu-id="4f47c-172">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="4f47c-173">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f47c-173">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="4f47c-174">Specifica l'URL per le richieste di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="4f47c-174">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="4f47c-175">-Ambito</span><span class="sxs-lookup"><span data-stu-id="4f47c-175">-Scope</span></span>
<span data-ttu-id="4f47c-176">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="4f47c-176">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="4f47c-177">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f47c-177">-ServiceEndpoint</span></span>
<span data-ttu-id="4f47c-178">Specifica l'endpoint per le richieste di gestione dei servizi (RDFE).</span><span class="sxs-lookup"><span data-stu-id="4f47c-178">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="4f47c-179">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="4f47c-179">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="4f47c-180">Specifica il suffisso del nome di dominio per i server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4f47c-180">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="4f47c-181">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f47c-181">-StorageEndpoint</span></span>
<span data-ttu-id="4f47c-182">Specifica l'endpoint per l'archiviazione (BLOB, Table, Queue e file) Access.</span><span class="sxs-lookup"><span data-stu-id="4f47c-182">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="4f47c-183">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="4f47c-183">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="4f47c-184">Specifica il suffisso del nome di dominio per i servizi di Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="4f47c-184">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="4f47c-185">-URI</span><span class="sxs-lookup"><span data-stu-id="4f47c-185">-Uri</span></span>
<span data-ttu-id="4f47c-186">Specifica l'URI della risorsa Internet per recuperare gli ambienti.</span><span class="sxs-lookup"><span data-stu-id="4f47c-186">Specifies URI of the internet resource to fetch environments.</span></span>

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

### <span data-ttu-id="4f47c-187">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4f47c-187">-Confirm</span></span>
<span data-ttu-id="4f47c-188">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f47c-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f47c-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f47c-189">-WhatIf</span></span>
<span data-ttu-id="4f47c-190">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f47c-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f47c-191">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f47c-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f47c-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f47c-192">CommonParameters</span></span>
<span data-ttu-id="4f47c-193">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f47c-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f47c-194">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f47c-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f47c-195">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4f47c-195">INPUTS</span></span>

### <span data-ttu-id="4f47c-196">System. String</span><span class="sxs-lookup"><span data-stu-id="4f47c-196">System.String</span></span>

### <span data-ttu-id="4f47c-197">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4f47c-197">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4f47c-198">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f47c-198">OUTPUTS</span></span>

### <span data-ttu-id="4f47c-199">Microsoft. Azure. Commands. profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="4f47c-199">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="4f47c-200">Note</span><span class="sxs-lookup"><span data-stu-id="4f47c-200">NOTES</span></span>

## <span data-ttu-id="4f47c-201">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f47c-201">RELATED LINKS</span></span>

[<span data-ttu-id="4f47c-202">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="4f47c-202">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="4f47c-203">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="4f47c-203">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="4f47c-204">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="4f47c-204">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

