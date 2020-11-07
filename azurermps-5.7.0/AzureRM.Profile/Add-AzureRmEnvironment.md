---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
ms.openlocfilehash: ef4f5128e92a319cb2b8ca021fc9b86f484d9b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685477"
---
# <span data-ttu-id="b386b-101">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="b386b-101">Add-AzureRmEnvironment</span></span>

## <span data-ttu-id="b386b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b386b-102">SYNOPSIS</span></span>
<span data-ttu-id="b386b-103">Aggiunge endpoint e metadati per un'istanza di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="b386b-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b386b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b386b-104">SYNTAX</span></span>

### <span data-ttu-id="b386b-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b386b-105">Name (Default)</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId <String>]]
 [[-AzureOperationalInsightsEndpoint] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>] 
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b386b-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="b386b-106">ARMEndpoint</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId <String>]]
 [[-AzureOperationalInsightsEndpoint] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>] 
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b386b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b386b-107">DESCRIPTION</span></span>
<span data-ttu-id="b386b-108">Il cmdlet Add-AzureRmEnvironment aggiunge endpoint e metadati per consentire ai cmdlet di Azure Resource Manager di connettersi con una nuova istanza di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="b386b-108">The Add-AzureRmEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="b386b-109">Gli ambienti predefiniti AzureCloud e AzureChinaCloud sono destinati alle istanze pubbliche esistenti di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="b386b-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="b386b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b386b-110">EXAMPLES</span></span>

### <span data-ttu-id="b386b-111">Esempio 1: creazione e modifica di un nuovo ambiente</span><span class="sxs-lookup"><span data-stu-id="b386b-111">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

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
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :

PS C:\> Set-AzureRmEnvironment -Name TestEnvironment
        -ActiveDirectoryEndpoint NewTestADEndpoint
        -GraphEndpoint NewTestGraphEndpoint

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
```

<span data-ttu-id="b386b-112">In questo esempio creiamo un nuovo ambiente Azure con endpoint di esempio usando Add-AzureRmEnvironment e quindi modifichiamo il valore degli attributi ActiveDirectoryEndpoint e GraphEndpoint dell'ambiente creato usando il cmdlet Set-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="b386b-112">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="b386b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b386b-113">PARAMETERS</span></span>

### <span data-ttu-id="b386b-114">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="b386b-114">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="b386b-115">Specifica l'autorità di base per l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b386b-115">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-116">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b386b-116">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="b386b-117">Specifica il gruppo di destinatari per i token che eseguono l'autenticazione delle richieste agli endpoint di Azure Resource Manager o RDFE (Service Management).</span><span class="sxs-lookup"><span data-stu-id="b386b-117">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-118">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="b386b-118">-AdTenant</span></span>
<span data-ttu-id="b386b-119">Specifica il tenant di Active Directory predefinito.</span><span class="sxs-lookup"><span data-stu-id="b386b-119">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-120">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="b386b-120">-ARMEndpoint</span></span>
<span data-ttu-id="b386b-121">Endpoint di Azure Resource Manager</span><span class="sxs-lookup"><span data-stu-id="b386b-121">The Azure Resource Manager endpoint</span></span>

```yaml
Type: String
Parameter Sets: ARMEndpoint
Aliases: ArmUrl

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-122">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="b386b-122">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="b386b-123">Suffisso DNS dei servizi di catalogo e lavoro di Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="b386b-123">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-124">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="b386b-124">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="b386b-125">Suffisso DNS di Azure Data Lake Store FileSystem.</span><span class="sxs-lookup"><span data-stu-id="b386b-125">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="b386b-126">Esempio: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="b386b-126">Example: azuredatalake.net</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-127">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="b386b-127">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="b386b-128">Specifica il suffisso del nome di dominio per i Servizi Key Vault.</span><span class="sxs-lookup"><span data-stu-id="b386b-128">Specifies the domain name suffix for Key Vault services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-129">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b386b-129">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="b386b-130">Specifica il gruppo di destinatari per i token di accesso che autorizzano le richieste per i Servizi Key Vault.</span><span class="sxs-lookup"><span data-stu-id="b386b-130">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-131">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="b386b-131">-DataLakeAudience</span></span>
<span data-ttu-id="b386b-132">Il gruppo di destinatari per l'autenticazione dei token con l'endpoint di servizi AD data Lake.</span><span class="sxs-lookup"><span data-stu-id="b386b-132">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b386b-133">-DefaultProfile</span></span>
<span data-ttu-id="b386b-134">Credeetnails, tenant e Subscription usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b386b-134">The credeetnails, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b386b-135">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="b386b-135">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="b386b-136">Indica che l'autenticazione locale di Active Directory Federation Services (ADFS) è consentita.</span><span class="sxs-lookup"><span data-stu-id="b386b-136">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Name
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-137">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="b386b-137">-GalleryEndpoint</span></span>
<span data-ttu-id="b386b-138">Specifica l'endpoint della raccolta di modelli di distribuzione di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="b386b-138">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-139">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="b386b-139">-GraphAudience</span></span>
<span data-ttu-id="b386b-140">Il gruppo di destinatari per l'autenticazione dei token con l'endpoint del grafico AD.</span><span class="sxs-lookup"><span data-stu-id="b386b-140">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-141">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="b386b-141">-GraphEndpoint</span></span>
<span data-ttu-id="b386b-142">Specifica l'URL per le richieste di grafico (metadati Active Directory).</span><span class="sxs-lookup"><span data-stu-id="b386b-142">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-143">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="b386b-143">-ManagementPortalUrl</span></span>
<span data-ttu-id="b386b-144">Specifica l'URL per il portale di gestione.</span><span class="sxs-lookup"><span data-stu-id="b386b-144">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="b386b-145">-Name</span></span>
<span data-ttu-id="b386b-146">Specifica il nome dell'ambiente da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="b386b-146">Specifies the name of the environment to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-147">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="b386b-147">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="b386b-148">Specifica l'URL da cui possono essere scaricati i file con estensione publishsettings.</span><span class="sxs-lookup"><span data-stu-id="b386b-148">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-149">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b386b-149">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="b386b-150">Specifica l'URL per le richieste di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="b386b-150">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-151">-Ambito</span><span class="sxs-lookup"><span data-stu-id="b386b-151">-Scope</span></span>
<span data-ttu-id="b386b-152">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="b386b-152">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-153">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b386b-153">-ServiceEndpoint</span></span>
<span data-ttu-id="b386b-154">Specifica l'endpoint per le richieste di gestione dei servizi (RDFE).</span><span class="sxs-lookup"><span data-stu-id="b386b-154">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-155">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="b386b-155">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="b386b-156">Specifica il suffisso del nome di dominio per i server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b386b-156">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-157">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="b386b-157">-StorageEndpoint</span></span>
<span data-ttu-id="b386b-158">Specifica l'endpoint per l'archiviazione (BLOB, Table, Queue e file) Access.</span><span class="sxs-lookup"><span data-stu-id="b386b-158">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-159">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="b386b-159">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="b386b-160">Specifica il suffisso del nome di dominio per i servizi di Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="b386b-160">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-161">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b386b-161">-BatchEndpointResourceId</span></span>
<span data-ttu-id="b386b-162">Identificatore delle risorse del servizio batch di Azure che è il destinatario del token richiesto</span><span class="sxs-lookup"><span data-stu-id="b386b-162">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-163">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="b386b-163">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="b386b-164">Specifica l'endpoint per l'accesso alla query per gli approfondimenti operativi.</span><span class="sxs-lookup"><span data-stu-id="b386b-164">Specifies the endpoint for the Operational Insights query access.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-165">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b386b-165">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="b386b-166">Specifica il gruppo di destinatari per i token di accesso che autorizzano le richieste di servizi per gli approfondimenti operativi.</span><span class="sxs-lookup"><span data-stu-id="b386b-166">Specifies the audience for access tokens that authorize requests for Operational Insights services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-167">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b386b-167">-Confirm</span></span>
<span data-ttu-id="b386b-168">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b386b-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b386b-169">-WhatIf</span></span>
<span data-ttu-id="b386b-170">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b386b-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b386b-171">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b386b-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b386b-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b386b-172">CommonParameters</span></span>
<span data-ttu-id="b386b-173">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b386b-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b386b-174">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b386b-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b386b-175">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b386b-175">INPUTS</span></span>

### <span data-ttu-id="b386b-176">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b386b-176">None</span></span>
<span data-ttu-id="b386b-177">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b386b-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b386b-178">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b386b-178">OUTPUTS</span></span>

### <span data-ttu-id="b386b-179">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="b386b-179">PSAzureEnvironment</span></span>
<span data-ttu-id="b386b-180">Questo cmdlet restituisce il set di endpoint e metadati necessari per comunicare con un'istanza di Azure.</span><span class="sxs-lookup"><span data-stu-id="b386b-180">This cmdlet returns the set of endpoints and metadata needed to communicate with an instance of Azure.</span></span>

## <span data-ttu-id="b386b-181">Note</span><span class="sxs-lookup"><span data-stu-id="b386b-181">NOTES</span></span>

## <span data-ttu-id="b386b-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b386b-182">RELATED LINKS</span></span>

[<span data-ttu-id="b386b-183">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="b386b-183">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="b386b-184">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="b386b-184">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="b386b-185">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="b386b-185">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

