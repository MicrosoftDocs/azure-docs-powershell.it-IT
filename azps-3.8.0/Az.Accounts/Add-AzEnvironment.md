---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: c1df1917a4133cf43f7cf0db89f1d59ad2c9c151
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021000"
---
# <span data-ttu-id="19d5d-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="19d5d-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="19d5d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19d5d-102">SYNOPSIS</span></span>
<span data-ttu-id="19d5d-103">Aggiunge endpoint e metadati per un'istanza di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="19d5d-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="19d5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19d5d-104">SYNTAX</span></span>

### <span data-ttu-id="19d5d-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="19d5d-105">Name (Default)</span></span>
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
 [-AzureAttestationServiceEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19d5d-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="19d5d-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19d5d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19d5d-107">DESCRIPTION</span></span>
<span data-ttu-id="19d5d-108">Il cmdlet Add-AzEnvironment aggiunge endpoint e metadati per consentire ai cmdlet di Azure Resource Manager di connettersi con una nuova istanza di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="19d5d-108">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="19d5d-109">Gli ambienti predefiniti AzureCloud e AzureChinaCloud sono destinati alle istanze pubbliche esistenti di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="19d5d-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="19d5d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19d5d-110">EXAMPLES</span></span>

### <span data-ttu-id="19d5d-111">Esempio 1: creazione e modifica di un nuovo ambiente</span><span class="sxs-lookup"><span data-stu-id="19d5d-111">Example 1: Creating and modifying a new environment</span></span>
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
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :

In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.
```

## <span data-ttu-id="19d5d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19d5d-112">PARAMETERS</span></span>

### <span data-ttu-id="19d5d-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="19d5d-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="19d5d-114">Specifica l'autorità di base per l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="19d5d-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="19d5d-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="19d5d-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="19d5d-116">Specifica il gruppo di destinatari per i token che eseguono l'autenticazione delle richieste agli endpoint di Azure Resource Manager o RDFE (Service Management).</span><span class="sxs-lookup"><span data-stu-id="19d5d-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="19d5d-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="19d5d-117">-AdTenant</span></span>
<span data-ttu-id="19d5d-118">Specifica il tenant di Active Directory predefinito.</span><span class="sxs-lookup"><span data-stu-id="19d5d-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="19d5d-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="19d5d-119">-ARMEndpoint</span></span>
<span data-ttu-id="19d5d-120">Endpoint di Azure Resource Manager</span><span class="sxs-lookup"><span data-stu-id="19d5d-120">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="19d5d-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="19d5d-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="19d5d-122">Identificatore delle risorse della risorsa di Azure Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="19d5d-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="19d5d-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="19d5d-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="19d5d-124">Endpoint da usare per comunicare con l'API di analisi di Azure log.</span><span class="sxs-lookup"><span data-stu-id="19d5d-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="19d5d-125">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="19d5d-125">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="19d5d-126">Identificatore della risorsa del servizio di attestazione di Azure che è il destinatario del token richiesto.</span><span class="sxs-lookup"><span data-stu-id="19d5d-126">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="19d5d-127">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="19d5d-127">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="19d5d-128">Suffisso DNS del servizio di attestazione Azure.</span><span class="sxs-lookup"><span data-stu-id="19d5d-128">Dns suffix of Azure Attestation service.</span></span>

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

### <span data-ttu-id="19d5d-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="19d5d-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="19d5d-130">Suffisso DNS dei servizi di catalogo e lavoro di Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="19d5d-130">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="19d5d-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="19d5d-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="19d5d-132">Suffisso DNS di Azure Data Lake Store FileSystem.</span><span class="sxs-lookup"><span data-stu-id="19d5d-132">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="19d5d-133">Esempio: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="19d5d-133">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="19d5d-134">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="19d5d-134">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="19d5d-135">Suffisso DNS del servizio Key Vault di Azure.</span><span class="sxs-lookup"><span data-stu-id="19d5d-135">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="19d5d-136">L'esempio è vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="19d5d-136">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="19d5d-137">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="19d5d-137">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="19d5d-138">Identificatore delle risorse del servizio dati di Azure Key Vault che è il destinatario del token richiesto.</span><span class="sxs-lookup"><span data-stu-id="19d5d-138">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="19d5d-139">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="19d5d-139">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="19d5d-140">Endpoint da usare per comunicare con l'API di analisi di Azure log.</span><span class="sxs-lookup"><span data-stu-id="19d5d-140">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="19d5d-141">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="19d5d-141">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="19d5d-142">Il gruppo di destinatari per l'autenticazione dei token con l'API di analisi del log di Azure.</span><span class="sxs-lookup"><span data-stu-id="19d5d-142">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="19d5d-143">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="19d5d-143">-BatchEndpointResourceId</span></span>
<span data-ttu-id="19d5d-144">Identificatore delle risorse del servizio batch di Azure che è il destinatario del token richiesto</span><span class="sxs-lookup"><span data-stu-id="19d5d-144">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="19d5d-145">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="19d5d-145">-DataLakeAudience</span></span>
<span data-ttu-id="19d5d-146">Il gruppo di destinatari per l'autenticazione dei token con l'endpoint di servizi AD data Lake.</span><span class="sxs-lookup"><span data-stu-id="19d5d-146">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="19d5d-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19d5d-147">-DefaultProfile</span></span>
<span data-ttu-id="19d5d-148">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="19d5d-148">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19d5d-149">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="19d5d-149">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="19d5d-150">Indica che l'autenticazione locale di Active Directory Federation Services (ADFS) è consentita.</span><span class="sxs-lookup"><span data-stu-id="19d5d-150">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="19d5d-151">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="19d5d-151">-GalleryEndpoint</span></span>
<span data-ttu-id="19d5d-152">Specifica l'endpoint della raccolta di modelli di distribuzione di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="19d5d-152">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="19d5d-153">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="19d5d-153">-GraphAudience</span></span>
<span data-ttu-id="19d5d-154">Il gruppo di destinatari per l'autenticazione dei token con l'endpoint del grafico AD.</span><span class="sxs-lookup"><span data-stu-id="19d5d-154">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="19d5d-155">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="19d5d-155">-GraphEndpoint</span></span>
<span data-ttu-id="19d5d-156">Specifica l'URL per le richieste di grafico (metadati Active Directory).</span><span class="sxs-lookup"><span data-stu-id="19d5d-156">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="19d5d-157">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="19d5d-157">-ManagementPortalUrl</span></span>
<span data-ttu-id="19d5d-158">Specifica l'URL per il portale di gestione.</span><span class="sxs-lookup"><span data-stu-id="19d5d-158">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="19d5d-159">-Nome</span><span class="sxs-lookup"><span data-stu-id="19d5d-159">-Name</span></span>
<span data-ttu-id="19d5d-160">Specifica il nome dell'ambiente da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="19d5d-160">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="19d5d-161">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="19d5d-161">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="19d5d-162">Specifica l'URL da cui possono essere scaricati i file con estensione publishsettings.</span><span class="sxs-lookup"><span data-stu-id="19d5d-162">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="19d5d-163">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="19d5d-163">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="19d5d-164">Specifica l'URL per le richieste di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="19d5d-164">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="19d5d-165">-Ambito</span><span class="sxs-lookup"><span data-stu-id="19d5d-165">-Scope</span></span>
<span data-ttu-id="19d5d-166">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="19d5d-166">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="19d5d-167">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="19d5d-167">-ServiceEndpoint</span></span>
<span data-ttu-id="19d5d-168">Specifica l'endpoint per le richieste di gestione dei servizi (RDFE).</span><span class="sxs-lookup"><span data-stu-id="19d5d-168">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="19d5d-169">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="19d5d-169">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="19d5d-170">Specifica il suffisso del nome di dominio per i server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="19d5d-170">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="19d5d-171">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="19d5d-171">-StorageEndpoint</span></span>
<span data-ttu-id="19d5d-172">Specifica l'endpoint per l'archiviazione (BLOB, Table, Queue e file) Access.</span><span class="sxs-lookup"><span data-stu-id="19d5d-172">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="19d5d-173">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="19d5d-173">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="19d5d-174">Specifica il suffisso del nome di dominio per i servizi di Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="19d5d-174">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="19d5d-175">-Confermare</span><span class="sxs-lookup"><span data-stu-id="19d5d-175">-Confirm</span></span>
<span data-ttu-id="19d5d-176">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19d5d-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19d5d-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19d5d-177">-WhatIf</span></span>
<span data-ttu-id="19d5d-178">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19d5d-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19d5d-179">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19d5d-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19d5d-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19d5d-180">CommonParameters</span></span>
<span data-ttu-id="19d5d-181">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19d5d-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19d5d-182">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19d5d-182">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19d5d-183">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19d5d-183">INPUTS</span></span>

### <span data-ttu-id="19d5d-184">System. String</span><span class="sxs-lookup"><span data-stu-id="19d5d-184">System.String</span></span>

### <span data-ttu-id="19d5d-185">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="19d5d-185">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="19d5d-186">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19d5d-186">OUTPUTS</span></span>

### <span data-ttu-id="19d5d-187">Microsoft. Azure. Commands. profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="19d5d-187">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="19d5d-188">Note</span><span class="sxs-lookup"><span data-stu-id="19d5d-188">NOTES</span></span>

## <span data-ttu-id="19d5d-189">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19d5d-189">RELATED LINKS</span></span>

[<span data-ttu-id="19d5d-190">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="19d5d-190">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="19d5d-191">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="19d5d-191">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="19d5d-192">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="19d5d-192">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

