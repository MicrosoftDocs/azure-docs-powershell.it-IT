---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
ms.openlocfilehash: a749c90a77c486e9e3e75f5a5fdbb48488a23559
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031513"
---
# <span data-ttu-id="25039-101">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="25039-101">Set-AzEnvironment</span></span>

## <span data-ttu-id="25039-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="25039-102">SYNOPSIS</span></span>
<span data-ttu-id="25039-103">Imposta le proprietà per un ambiente Azure.</span><span class="sxs-lookup"><span data-stu-id="25039-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="25039-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="25039-104">SYNTAX</span></span>

### <span data-ttu-id="25039-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="25039-105">Name (Default)</span></span>
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
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25039-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="25039-106">ARMEndpoint</span></span>
```
Set-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-AzureSynapseAnalyticsEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25039-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25039-107">DESCRIPTION</span></span>
<span data-ttu-id="25039-108">Il cmdlet Set-AzEnvironment imposta gli endpoint e i metadati per la connessione a un'istanza di Azure.</span><span class="sxs-lookup"><span data-stu-id="25039-108">The Set-AzEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="25039-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="25039-109">EXAMPLES</span></span>

### <span data-ttu-id="25039-110">Esempio 1: creazione e modifica di un nuovo ambiente</span><span class="sxs-lookup"><span data-stu-id="25039-110">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="25039-111">In questo esempio creiamo un nuovo ambiente Azure con endpoint di esempio usando Add-AzEnvironment e quindi modifichiamo il valore degli attributi ActiveDirectoryEndpoint e GraphEndpoint dell'ambiente creato usando il cmdlet Set-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="25039-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

## <span data-ttu-id="25039-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="25039-112">PARAMETERS</span></span>

### <span data-ttu-id="25039-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="25039-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="25039-114">Specifica l'autorità di base per l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="25039-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="25039-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="25039-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="25039-116">Specifica il gruppo di destinatari per i token che eseguono l'autenticazione delle richieste agli endpoint di Azure Resource Manager o RDFE (Service Management).</span><span class="sxs-lookup"><span data-stu-id="25039-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="25039-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="25039-117">-AdTenant</span></span>
<span data-ttu-id="25039-118">Specifica il tenant di Active Directory predefinito.</span><span class="sxs-lookup"><span data-stu-id="25039-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="25039-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="25039-119">-ARMEndpoint</span></span>
<span data-ttu-id="25039-120">Endpoint di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="25039-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="25039-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="25039-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="25039-122">Identificatore delle risorse della risorsa di Azure Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="25039-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="25039-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="25039-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="25039-124">Endpoint da usare per comunicare con l'API di analisi di Azure log.</span><span class="sxs-lookup"><span data-stu-id="25039-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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
### <span data-ttu-id="25039-125">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="25039-125">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="25039-126">Identificatore della risorsa del servizio di attestazione di Azure che è il destinatario del token richiesto.</span><span class="sxs-lookup"><span data-stu-id="25039-126">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="25039-127">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="25039-127">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="25039-128">Suffisso DNS del servizio di attestazione Azure.</span><span class="sxs-lookup"><span data-stu-id="25039-128">Dns suffix of Azure Attestation service.</span></span>

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

### <span data-ttu-id="25039-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="25039-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="25039-130">Suffisso DNS dei servizi di catalogo e lavoro di Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="25039-130">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="25039-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="25039-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="25039-132">Suffisso DNS di Azure Data Lake Store FileSystem.</span><span class="sxs-lookup"><span data-stu-id="25039-132">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="25039-133">Esempio: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="25039-133">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="25039-134">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="25039-134">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="25039-135">Suffisso DNS del servizio Key Vault di Azure.</span><span class="sxs-lookup"><span data-stu-id="25039-135">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="25039-136">L'esempio è vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="25039-136">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="25039-137">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="25039-137">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="25039-138">Identificatore delle risorse del servizio dati di Azure Key Vault che è il destinatario del token richiesto.</span><span class="sxs-lookup"><span data-stu-id="25039-138">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="25039-139">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="25039-139">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="25039-140">Endpoint da usare per comunicare con l'API di analisi di Azure log.</span><span class="sxs-lookup"><span data-stu-id="25039-140">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="25039-141">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="25039-141">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="25039-142">Il gruppo di destinatari per l'autenticazione dei token con l'API di analisi del log di Azure.</span><span class="sxs-lookup"><span data-stu-id="25039-142">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="25039-143">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="25039-143">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="25039-144">Identificatore della risorsa dell'analisi delle sinapsi di Azure che rappresenta il destinatario del token richiesto.</span><span class="sxs-lookup"><span data-stu-id="25039-144">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="25039-145">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="25039-145">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="25039-146">Suffisso DNS di Azure sinapsi Analytics.</span><span class="sxs-lookup"><span data-stu-id="25039-146">Dns suffix of Azure Synapse Analytics.</span></span>

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

### <span data-ttu-id="25039-147">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="25039-147">-BatchEndpointResourceId</span></span>
<span data-ttu-id="25039-148">Identificatore delle risorse del servizio batch di Azure che è il destinatario del token richiesto</span><span class="sxs-lookup"><span data-stu-id="25039-148">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="25039-149">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="25039-149">-DataLakeAudience</span></span>
<span data-ttu-id="25039-150">Il gruppo di destinatari per l'autenticazione dei token con l'endpoint di servizi AD data Lake.</span><span class="sxs-lookup"><span data-stu-id="25039-150">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="25039-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25039-151">-DefaultProfile</span></span>
<span data-ttu-id="25039-152">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="25039-152">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25039-153">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="25039-153">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="25039-154">Indica che l'autenticazione locale di Active Directory Federation Services (ADFS) è consentita.</span><span class="sxs-lookup"><span data-stu-id="25039-154">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="25039-155">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="25039-155">-GalleryEndpoint</span></span>
<span data-ttu-id="25039-156">Specifica l'endpoint della raccolta di modelli di distribuzione di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="25039-156">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="25039-157">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="25039-157">-GraphAudience</span></span>
<span data-ttu-id="25039-158">Il gruppo di destinatari per l'autenticazione dei token con l'endpoint del grafico AD.</span><span class="sxs-lookup"><span data-stu-id="25039-158">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="25039-159">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="25039-159">-GraphEndpoint</span></span>
<span data-ttu-id="25039-160">Specifica l'URL per le richieste di grafico (metadati Active Directory).</span><span class="sxs-lookup"><span data-stu-id="25039-160">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="25039-161">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="25039-161">-ManagementPortalUrl</span></span>
<span data-ttu-id="25039-162">Specifica l'URL per il portale di gestione.</span><span class="sxs-lookup"><span data-stu-id="25039-162">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="25039-163">-Nome</span><span class="sxs-lookup"><span data-stu-id="25039-163">-Name</span></span>
<span data-ttu-id="25039-164">Specifica il nome dell'ambiente da modificare.</span><span class="sxs-lookup"><span data-stu-id="25039-164">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="25039-165">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="25039-165">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="25039-166">Specifica l'URL da cui possono essere scaricati i file con estensione publishsettings.</span><span class="sxs-lookup"><span data-stu-id="25039-166">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="25039-167">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="25039-167">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="25039-168">Specifica l'URL per le richieste di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="25039-168">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="25039-169">-Ambito</span><span class="sxs-lookup"><span data-stu-id="25039-169">-Scope</span></span>
<span data-ttu-id="25039-170">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="25039-170">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="25039-171">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="25039-171">-ServiceEndpoint</span></span>
<span data-ttu-id="25039-172">Specifica l'endpoint per le richieste di gestione dei servizi (RDFE).</span><span class="sxs-lookup"><span data-stu-id="25039-172">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="25039-173">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="25039-173">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="25039-174">Specifica il suffisso del nome di dominio per i server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="25039-174">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="25039-175">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="25039-175">-StorageEndpoint</span></span>
<span data-ttu-id="25039-176">Specifica l'endpoint per l'archiviazione (BLOB, Table, Queue e file) Access.</span><span class="sxs-lookup"><span data-stu-id="25039-176">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="25039-177">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="25039-177">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="25039-178">Specifica il suffisso del nome di dominio per i servizi di Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="25039-178">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="25039-179">-Confermare</span><span class="sxs-lookup"><span data-stu-id="25039-179">-Confirm</span></span>
<span data-ttu-id="25039-180">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25039-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25039-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25039-181">-WhatIf</span></span>
<span data-ttu-id="25039-182">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="25039-182">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25039-183">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="25039-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25039-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25039-184">CommonParameters</span></span>
<span data-ttu-id="25039-185">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25039-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25039-186">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25039-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25039-187">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="25039-187">INPUTS</span></span>

### <span data-ttu-id="25039-188">System. String</span><span class="sxs-lookup"><span data-stu-id="25039-188">System.String</span></span>

### <span data-ttu-id="25039-189">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="25039-189">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="25039-190">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="25039-190">OUTPUTS</span></span>

### <span data-ttu-id="25039-191">Microsoft. Azure. Commands. profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="25039-191">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="25039-192">Note</span><span class="sxs-lookup"><span data-stu-id="25039-192">NOTES</span></span>

## <span data-ttu-id="25039-193">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="25039-193">RELATED LINKS</span></span>

[<span data-ttu-id="25039-194">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="25039-194">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="25039-195">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="25039-195">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="25039-196">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="25039-196">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

