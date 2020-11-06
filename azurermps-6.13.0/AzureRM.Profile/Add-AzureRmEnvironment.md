---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
ms.openlocfilehash: ed50d8e25dca0998e7e3e026783fe4ec78e6ce7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507375"
---
# <span data-ttu-id="bfcd0-101">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="bfcd0-101">Add-AzureRmEnvironment</span></span>

## <span data-ttu-id="bfcd0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bfcd0-102">SYNOPSIS</span></span>
<span data-ttu-id="bfcd0-103">Aggiunge endpoint e metadati per un'istanza di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfcd0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bfcd0-104">SYNTAX</span></span>

### <span data-ttu-id="bfcd0-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bfcd0-105">Name (Default)</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [[-BatchEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpoint] <String>] [-AzureAnalysisServicesEndpointSuffix <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfcd0-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="bfcd0-106">ARMEndpoint</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bfcd0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bfcd0-107">DESCRIPTION</span></span>
<span data-ttu-id="bfcd0-108">Il cmdlet Add-AzureRmEnvironment aggiunge endpoint e metadati per consentire ai cmdlet di Azure Resource Manager di connettersi con una nuova istanza di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-108">The Add-AzureRmEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="bfcd0-109">Gli ambienti predefiniti AzureCloud e AzureChinaCloud sono destinati alle istanze pubbliche esistenti di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="bfcd0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bfcd0-110">EXAMPLES</span></span>

### <span data-ttu-id="bfcd0-111">Esempio 1: creazione e modifica di un nuovo ambiente</span><span class="sxs-lookup"><span data-stu-id="bfcd0-111">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Set-AzureRmEnvironment -Name TestEnvironment `
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
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :

In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.
```

## <span data-ttu-id="bfcd0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bfcd0-112">PARAMETERS</span></span>

### <span data-ttu-id="bfcd0-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="bfcd0-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="bfcd0-114">Specifica l'autorità di base per l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="bfcd0-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="bfcd0-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="bfcd0-116">Specifica il gruppo di destinatari per i token che eseguono l'autenticazione delle richieste agli endpoint di Azure Resource Manager o RDFE (Service Management).</span><span class="sxs-lookup"><span data-stu-id="bfcd0-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="bfcd0-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="bfcd0-117">-AdTenant</span></span>
<span data-ttu-id="bfcd0-118">Specifica il tenant di Active Directory predefinito.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="bfcd0-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="bfcd0-119">-ARMEndpoint</span></span>
<span data-ttu-id="bfcd0-120">Endpoint di Azure Resource Manager</span><span class="sxs-lookup"><span data-stu-id="bfcd0-120">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="bfcd0-121">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="bfcd0-121">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="bfcd0-122">Suffisso DNS degli endpoint del servizio di Analysis Services Azure</span><span class="sxs-lookup"><span data-stu-id="bfcd0-122">Dns Suffix of Azure Analysis Services service endpoints</span></span>

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


### <span data-ttu-id="bfcd0-123">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="bfcd0-123">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="bfcd0-124">Suffisso DNS dei servizi di catalogo e lavoro di Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="bfcd0-124">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="bfcd0-125">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="bfcd0-125">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="bfcd0-126">Suffisso DNS di Azure Data Lake Store FileSystem.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-126">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="bfcd0-127">Esempio: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="bfcd0-127">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="bfcd0-128">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="bfcd0-128">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="bfcd0-129">Specifica il suffisso del nome di dominio per i Servizi Key Vault.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-129">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="bfcd0-130">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="bfcd0-130">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="bfcd0-131">Specifica il gruppo di destinatari per i token di accesso che autorizzano le richieste per i Servizi Key Vault.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-131">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

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

### <span data-ttu-id="bfcd0-132">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="bfcd0-132">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="bfcd0-133">Specifica l'endpoint per l'accesso alla query per gli approfondimenti operativi.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-133">Specifies the endpoint for the Operational Insights query access.</span></span> 

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

### <span data-ttu-id="bfcd0-134">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="bfcd0-134">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="bfcd0-135">Specifica il gruppo di destinatari per i token di accesso che autorizzano le richieste di servizi per gli approfondimenti operativi.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-135">Specifies the audience for access tokens that authorize requests for Operational Insights services.</span></span>

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

### <span data-ttu-id="bfcd0-136">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="bfcd0-136">-BatchEndpointResourceId</span></span>
<span data-ttu-id="bfcd0-137">Identificatore delle risorse del servizio batch di Azure che è il destinatario del token richiesto</span><span class="sxs-lookup"><span data-stu-id="bfcd0-137">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="bfcd0-138">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="bfcd0-138">-DataLakeAudience</span></span>
<span data-ttu-id="bfcd0-139">Il gruppo di destinatari per l'autenticazione dei token con l'endpoint di servizi AD data Lake.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-139">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="bfcd0-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfcd0-140">-DefaultProfile</span></span>
<span data-ttu-id="bfcd0-141">Credeetnails, tenant e Subscription usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bfcd0-141">The credeetnails, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bfcd0-142">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="bfcd0-142">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="bfcd0-143">Indica che l'autenticazione locale di Active Directory Federation Services (ADFS) è consentita.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-143">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="bfcd0-144">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="bfcd0-144">-GalleryEndpoint</span></span>
<span data-ttu-id="bfcd0-145">Specifica l'endpoint della raccolta di modelli di distribuzione di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-145">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="bfcd0-146">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="bfcd0-146">-GraphAudience</span></span>
<span data-ttu-id="bfcd0-147">Il gruppo di destinatari per l'autenticazione dei token con l'endpoint del grafico AD.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-147">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="bfcd0-148">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="bfcd0-148">-GraphEndpoint</span></span>
<span data-ttu-id="bfcd0-149">Specifica l'URL per le richieste di grafico (metadati Active Directory).</span><span class="sxs-lookup"><span data-stu-id="bfcd0-149">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="bfcd0-150">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="bfcd0-150">-ManagementPortalUrl</span></span>
<span data-ttu-id="bfcd0-151">Specifica l'URL per il portale di gestione.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-151">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="bfcd0-152">-Nome</span><span class="sxs-lookup"><span data-stu-id="bfcd0-152">-Name</span></span>
<span data-ttu-id="bfcd0-153">Specifica il nome dell'ambiente da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-153">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="bfcd0-154">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="bfcd0-154">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="bfcd0-155">Specifica l'URL da cui possono essere scaricati i file con estensione publishsettings.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-155">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="bfcd0-156">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bfcd0-156">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="bfcd0-157">Specifica l'URL per le richieste di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-157">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="bfcd0-158">-Ambito</span><span class="sxs-lookup"><span data-stu-id="bfcd0-158">-Scope</span></span>
<span data-ttu-id="bfcd0-159">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-159">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="bfcd0-160">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="bfcd0-160">-ServiceEndpoint</span></span>
<span data-ttu-id="bfcd0-161">Specifica l'endpoint per le richieste di gestione dei servizi (RDFE).</span><span class="sxs-lookup"><span data-stu-id="bfcd0-161">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="bfcd0-162">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="bfcd0-162">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="bfcd0-163">Specifica il suffisso del nome di dominio per i server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-163">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="bfcd0-164">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="bfcd0-164">-StorageEndpoint</span></span>
<span data-ttu-id="bfcd0-165">Specifica l'endpoint per l'archiviazione (BLOB, Table, Queue e file) Access.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-165">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="bfcd0-166">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="bfcd0-166">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="bfcd0-167">Specifica il suffisso del nome di dominio per i servizi di Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-167">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="bfcd0-168">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bfcd0-168">-Confirm</span></span>
<span data-ttu-id="bfcd0-169">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfcd0-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfcd0-170">-WhatIf</span></span>
<span data-ttu-id="bfcd0-171">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bfcd0-172">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfcd0-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfcd0-173">CommonParameters</span></span>
<span data-ttu-id="bfcd0-174">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfcd0-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfcd0-175">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfcd0-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfcd0-176">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bfcd0-176">INPUTS</span></span>

### <span data-ttu-id="bfcd0-177">System. String</span><span class="sxs-lookup"><span data-stu-id="bfcd0-177">System.String</span></span>

### <span data-ttu-id="bfcd0-178">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bfcd0-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bfcd0-179">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bfcd0-179">OUTPUTS</span></span>

### <span data-ttu-id="bfcd0-180">Microsoft. Azure. Commands. profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="bfcd0-180">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="bfcd0-181">Note</span><span class="sxs-lookup"><span data-stu-id="bfcd0-181">NOTES</span></span>

## <span data-ttu-id="bfcd0-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bfcd0-182">RELATED LINKS</span></span>

[<span data-ttu-id="bfcd0-183">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="bfcd0-183">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="bfcd0-184">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="bfcd0-184">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="bfcd0-185">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="bfcd0-185">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

