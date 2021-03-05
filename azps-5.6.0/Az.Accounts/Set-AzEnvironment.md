---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/set-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
ms.openlocfilehash: 502a15c4d102932e32fb103a80f55c8b3acfee3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967117"
---
# <span data-ttu-id="9cde6-101">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="9cde6-101">Set-AzEnvironment</span></span>

## <span data-ttu-id="9cde6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cde6-102">SYNOPSIS</span></span>
<span data-ttu-id="9cde6-103">Imposta le proprietà per un ambiente Azure.</span><span class="sxs-lookup"><span data-stu-id="9cde6-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="9cde6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9cde6-104">SYNTAX</span></span>

### <span data-ttu-id="9cde6-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9cde6-105">Name (Default)</span></span>
```
Set-AzEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
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

### <span data-ttu-id="9cde6-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="9cde6-106">ARMEndpoint</span></span>
```
Set-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-ContainerRegistryEndpointSuffix <String>]
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cde6-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9cde6-107">DESCRIPTION</span></span>
<span data-ttu-id="9cde6-108">Il cmdlet Set-AzEnvironment configura endpoint e metadati per la connessione a un'istanza di Azure.</span><span class="sxs-lookup"><span data-stu-id="9cde6-108">The Set-AzEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="9cde6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9cde6-109">EXAMPLES</span></span>

### <span data-ttu-id="9cde6-110">Esempio 1: Creazione e modifica di un nuovo ambiente</span><span class="sxs-lookup"><span data-stu-id="9cde6-110">Example 1: Creating and modifying a new environment</span></span>
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

PS C:\> Set-AzEnvironment -Name TestEnvironment
        -ActiveDirectoryEndpoint NewTestADEndpoint
        -GraphEndpoint NewTestGraphEndpoint | Format-List

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
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
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
BatchEndpointResourceId                           :
AzureOperationalInsightsEndpoint                  :
AzureOperationalInsightsEndpointResourceId        :
AzureAttestationServiceEndpointSuffix             :
AzureAttestationServiceEndpointResourceId         :
AzureSynapseAnalyticsEndpointSuffix               :
AzureSynapseAnalyticsEndpointResourceId           :
```

<span data-ttu-id="9cde6-111">In questo esempio viene creato un nuovo ambiente di Azure con endpoint di esempio con Add-AzEnvironment e quindi si modifica il valore degli attributi ActiveDirectoryEndpoint e GraphEndpoint dell'ambiente creato usando il cmdlet Set-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="9cde6-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

## <span data-ttu-id="9cde6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cde6-112">PARAMETERS</span></span>

### <span data-ttu-id="9cde6-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="9cde6-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="9cde6-114">Specifica l'autorità di base per l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9cde6-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="9cde6-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="9cde6-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="9cde6-116">Specifica il gruppo di destinatari per i token che autenticano le richieste agli endpoint di Gestione risorse o Gestione servizi (RDFE) di Azure.</span><span class="sxs-lookup"><span data-stu-id="9cde6-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="9cde6-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="9cde6-117">-AdTenant</span></span>
<span data-ttu-id="9cde6-118">Specifica il tenant di Active Directory predefinito.</span><span class="sxs-lookup"><span data-stu-id="9cde6-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="9cde6-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="9cde6-119">-ARMEndpoint</span></span>
<span data-ttu-id="9cde6-120">Endpoint di Gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="9cde6-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="9cde6-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="9cde6-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="9cde6-122">Identificatore di risorsa della risorsa di Azure Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="9cde6-122">The resource identifier of the Azure Analysis Services resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cde6-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="9cde6-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="9cde6-124">Endpoint da usare per la comunicazione con l'API analisi log di Azure.</span><span class="sxs-lookup"><span data-stu-id="9cde6-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cde6-125">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="9cde6-125">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="9cde6-126">L'identificatore di risorsa del servizio di attestazione di Azure che è il destinatario del token richiesto.</span><span class="sxs-lookup"><span data-stu-id="9cde6-126">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="9cde6-127">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="9cde6-127">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="9cde6-128">Suffisso DNS del servizio di attestazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9cde6-128">Dns suffix of Azure Attestation service.</span></span>

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

### <span data-ttu-id="9cde6-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="9cde6-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="9cde6-130">Suffisso Dns dei servizi di catalogo e processo di Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="9cde6-130">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="9cde6-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="9cde6-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="9cde6-132">Suffisso Dns del fileSystem Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9cde6-132">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="9cde6-133">Esempio: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="9cde6-133">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="9cde6-134">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="9cde6-134">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="9cde6-135">Suffisso DNS del servizio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="9cde6-135">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="9cde6-136">Esempio: vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="9cde6-136">Example is vault-int.azure-int.net</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cde6-137">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="9cde6-137">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="9cde6-138">Identificatore di risorsa del servizio dati Azure Key Vault che è il destinatario del token richiesto.</span><span class="sxs-lookup"><span data-stu-id="9cde6-138">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cde6-139">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="9cde6-139">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="9cde6-140">Endpoint da usare per la comunicazione con l'API Analisi log di Azure.</span><span class="sxs-lookup"><span data-stu-id="9cde6-140">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cde6-141">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="9cde6-141">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="9cde6-142">Gruppo di destinatari per l'autenticazione dei token con l'API Analisi log di Azure.</span><span class="sxs-lookup"><span data-stu-id="9cde6-142">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cde6-143">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="9cde6-143">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="9cde6-144">L'identificatore di risorsa di Azure Synapse Analytics che è il destinatario del token richiesto.</span><span class="sxs-lookup"><span data-stu-id="9cde6-144">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="9cde6-145">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="9cde6-145">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="9cde6-146">Suffisso DNS di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="9cde6-146">Dns suffix of Azure Synapse Analytics.</span></span>

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

### <span data-ttu-id="9cde6-147">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="9cde6-147">-BatchEndpointResourceId</span></span>
<span data-ttu-id="9cde6-148">L'identificatore di risorsa del servizio batch di Azure che è il destinatario del token richiesto</span><span class="sxs-lookup"><span data-stu-id="9cde6-148">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchResourceId, BatchAudience

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cde6-149">-ContainerRegistryEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="9cde6-149">-ContainerRegistryEndpointSuffix</span></span>
<span data-ttu-id="9cde6-150">Suffisso del Registro di sistema del contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="9cde6-150">Suffix of Azure Container Registry.</span></span>

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

### <span data-ttu-id="9cde6-151">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="9cde6-151">-DataLakeAudience</span></span>
<span data-ttu-id="9cde6-152">Destinatari per token di autenticazione con l'Endpoint di Ad Data Lake Services.</span><span class="sxs-lookup"><span data-stu-id="9cde6-152">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cde6-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cde6-153">-DefaultProfile</span></span>
<span data-ttu-id="9cde6-154">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9cde6-154">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cde6-155">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="9cde6-155">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="9cde6-156">Indica che è consentita l'autenticazione locale di Active Directory Federation Services (ADFS).</span><span class="sxs-lookup"><span data-stu-id="9cde6-156">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="9cde6-157">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="9cde6-157">-GalleryEndpoint</span></span>
<span data-ttu-id="9cde6-158">Specifica l'endpoint per la raccolta di modelli di distribuzione di Gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="9cde6-158">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="9cde6-159">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="9cde6-159">-GraphAudience</span></span>
<span data-ttu-id="9cde6-160">Gruppo di destinatari per l'autenticazione dei token con l'endpoint di Ad Graph.</span><span class="sxs-lookup"><span data-stu-id="9cde6-160">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="9cde6-161">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="9cde6-161">-GraphEndpoint</span></span>
<span data-ttu-id="9cde6-162">Specifica l'URL per le richieste Graph (metadati di Active Directory).</span><span class="sxs-lookup"><span data-stu-id="9cde6-162">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="9cde6-163">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="9cde6-163">-ManagementPortalUrl</span></span>
<span data-ttu-id="9cde6-164">Specifica l'URL per il portale di gestione.</span><span class="sxs-lookup"><span data-stu-id="9cde6-164">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="9cde6-165">-Name</span><span class="sxs-lookup"><span data-stu-id="9cde6-165">-Name</span></span>
<span data-ttu-id="9cde6-166">Specifica il nome dell'ambiente da modificare.</span><span class="sxs-lookup"><span data-stu-id="9cde6-166">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="9cde6-167">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="9cde6-167">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="9cde6-168">Specifica l'URL da cui è possibile scaricare i file .publishsettings.</span><span class="sxs-lookup"><span data-stu-id="9cde6-168">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="9cde6-169">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9cde6-169">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="9cde6-170">Specifica l'URL per le richieste di Gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="9cde6-170">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="9cde6-171">-Scope</span><span class="sxs-lookup"><span data-stu-id="9cde6-171">-Scope</span></span>
<span data-ttu-id="9cde6-172">Determina l'ambito delle modifiche di contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="9cde6-172">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="9cde6-173">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="9cde6-173">-ServiceEndpoint</span></span>
<span data-ttu-id="9cde6-174">Specifica l'endpoint per le richieste di gestione del servizio (RDFE).</span><span class="sxs-lookup"><span data-stu-id="9cde6-174">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="9cde6-175">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="9cde6-175">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="9cde6-176">Specifica il suffisso del nome di dominio per i server di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9cde6-176">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="9cde6-177">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="9cde6-177">-StorageEndpoint</span></span>
<span data-ttu-id="9cde6-178">Specifica l'endpoint per l'accesso (BLOB, tabella, coda e file).</span><span class="sxs-lookup"><span data-stu-id="9cde6-178">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cde6-179">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="9cde6-179">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="9cde6-180">Specifica il suffisso del nome di dominio per i servizi di Gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="9cde6-180">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="9cde6-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9cde6-181">-Confirm</span></span>
<span data-ttu-id="9cde6-182">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cde6-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cde6-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cde6-183">-WhatIf</span></span>
<span data-ttu-id="9cde6-184">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9cde6-184">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9cde6-185">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9cde6-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cde6-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cde6-186">CommonParameters</span></span>
<span data-ttu-id="9cde6-187">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cde6-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cde6-188">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9cde6-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cde6-189">INPUT</span><span class="sxs-lookup"><span data-stu-id="9cde6-189">INPUTS</span></span>

### <span data-ttu-id="9cde6-190">System.String</span><span class="sxs-lookup"><span data-stu-id="9cde6-190">System.String</span></span>

### <span data-ttu-id="9cde6-191">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9cde6-191">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9cde6-192">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9cde6-192">OUTPUTS</span></span>

### <span data-ttu-id="9cde6-193">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="9cde6-193">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="9cde6-194">NOTE</span><span class="sxs-lookup"><span data-stu-id="9cde6-194">NOTES</span></span>

## <span data-ttu-id="9cde6-195">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9cde6-195">RELATED LINKS</span></span>

[<span data-ttu-id="9cde6-196">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="9cde6-196">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="9cde6-197">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="9cde6-197">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="9cde6-198">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="9cde6-198">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

