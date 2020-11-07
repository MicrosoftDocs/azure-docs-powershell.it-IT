---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmEnvironment.md
ms.openlocfilehash: 468abd4edc2e60ec0e13c80d345bafdac7ad2be5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687475"
---
# <span data-ttu-id="3dc1a-101">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="3dc1a-101">Set-AzureRmEnvironment</span></span>

## <span data-ttu-id="3dc1a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3dc1a-102">SYNOPSIS</span></span>
<span data-ttu-id="3dc1a-103">Imposta le proprietà per un ambiente Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-103">Sets properties for an Azure environment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dc1a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3dc1a-104">SYNTAX</span></span>

### <span data-ttu-id="3dc1a-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3dc1a-105">Name (Default)</span></span>
```
Set-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId <String>]]
 [[-AzureOperationalInsightsEndpoint] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>] 
 [-Scope <ContextModificationScope>][-DefaultProfile <IAzureContextContainer>] 
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dc1a-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="3dc1a-106">ARMEndpoint</span></span>
```
Set-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId <String>]] [[-AzureOperationalInsightsEndpoint] <String>] 
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [-Scope <ContextModificationScope>] 
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dc1a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3dc1a-107">DESCRIPTION</span></span>
<span data-ttu-id="3dc1a-108">Il cmdlet Set-AzureRMEnvironment imposta gli endpoint e i metadati per la connessione a un'istanza di Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-108">The Set-AzureRMEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="3dc1a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3dc1a-109">EXAMPLES</span></span>

### <span data-ttu-id="3dc1a-110">Esempio 1: creazione e modifica di un nuovo ambiente</span><span class="sxs-lookup"><span data-stu-id="3dc1a-110">Example 1: Creating and modifying a new environment</span></span>
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
BatchEndpointResourceId                           :
AzureOperationalInsightsEndpoint                  :
AzureOperationalInsightsEndpointResourceId        :

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
BatchEndpointResourceId                           :
AzureOperationalInsightsEndpoint                  :
AzureOperationalInsightsEndpointResourceId        :
```

<span data-ttu-id="3dc1a-111">In questo esempio creiamo un nuovo ambiente Azure con endpoint di esempio usando Add-AzureRmEnvironment e quindi modifichiamo il valore degli attributi ActiveDirectoryEndpoint e GraphEndpoint dell'ambiente creato usando il cmdlet Set-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="3dc1a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3dc1a-112">PARAMETERS</span></span>

### <span data-ttu-id="3dc1a-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="3dc1a-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="3dc1a-114">Specifica l'autorità di base per l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="3dc1a-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3dc1a-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="3dc1a-116">Specifica il gruppo di destinatari per i token che eseguono l'autenticazione delle richieste agli endpoint di Azure Resource Manager o RDFE (Service Management).</span><span class="sxs-lookup"><span data-stu-id="3dc1a-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="3dc1a-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="3dc1a-117">-AdTenant</span></span>
<span data-ttu-id="3dc1a-118">Specifica il tenant di Active Directory predefinito.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="3dc1a-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="3dc1a-119">-ARMEndpoint</span></span>
<span data-ttu-id="3dc1a-120">Endpoint di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="3dc1a-121">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="3dc1a-121">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="3dc1a-122">Suffisso DNS dei servizi di catalogo e lavoro di Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="3dc1a-122">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="3dc1a-123">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="3dc1a-123">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="3dc1a-124">Suffisso DNS di Azure Data Lake Store FileSystem.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-124">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="3dc1a-125">Esempio: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="3dc1a-125">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="3dc1a-126">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="3dc1a-126">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="3dc1a-127">Specifica il suffisso del nome di dominio per i Servizi Key Vault.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-127">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="3dc1a-128">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3dc1a-128">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="3dc1a-129">Specifica il gruppo di destinatari per i token di accesso che autorizzano le richieste per i Servizi Key Vault.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-129">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

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

### <span data-ttu-id="3dc1a-130">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="3dc1a-130">-DataLakeAudience</span></span>
<span data-ttu-id="3dc1a-131">Il gruppo di destinatari per l'autenticazione dei token con l'endpoint di servizi AD data Lake.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-131">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="3dc1a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dc1a-132">-DefaultProfile</span></span>
<span data-ttu-id="3dc1a-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-133">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dc1a-134">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="3dc1a-134">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="3dc1a-135">Indica che l'autenticazione locale di Active Directory Federation Services (ADFS) è consentita.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-135">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="3dc1a-136">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="3dc1a-136">-GalleryEndpoint</span></span>
<span data-ttu-id="3dc1a-137">Specifica l'endpoint della raccolta di modelli di distribuzione di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-137">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="3dc1a-138">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="3dc1a-138">-GraphAudience</span></span>
<span data-ttu-id="3dc1a-139">Il gruppo di destinatari per l'autenticazione dei token con l'endpoint del grafico AD.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-139">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="3dc1a-140">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="3dc1a-140">-GraphEndpoint</span></span>
<span data-ttu-id="3dc1a-141">Specifica l'URL per le richieste di grafico (metadati Active Directory).</span><span class="sxs-lookup"><span data-stu-id="3dc1a-141">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="3dc1a-142">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="3dc1a-142">-ManagementPortalUrl</span></span>
<span data-ttu-id="3dc1a-143">Specifica l'URL per il portale di gestione.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-143">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="3dc1a-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="3dc1a-144">-Name</span></span>
<span data-ttu-id="3dc1a-145">Specifica il nome dell'ambiente da modificare.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-145">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="3dc1a-146">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="3dc1a-146">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="3dc1a-147">Specifica l'URL da cui possono essere scaricati i file con estensione publishsettings.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-147">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="3dc1a-148">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3dc1a-148">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="3dc1a-149">Specifica l'URL per le richieste di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-149">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="3dc1a-150">-Ambito</span><span class="sxs-lookup"><span data-stu-id="3dc1a-150">-Scope</span></span>
<span data-ttu-id="3dc1a-151">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-151">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="3dc1a-152">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="3dc1a-152">-ServiceEndpoint</span></span>
<span data-ttu-id="3dc1a-153">Specifica l'endpoint per le richieste di gestione dei servizi (RDFE).</span><span class="sxs-lookup"><span data-stu-id="3dc1a-153">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="3dc1a-154">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="3dc1a-154">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="3dc1a-155">Specifica il suffisso del nome di dominio per i server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-155">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="3dc1a-156">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="3dc1a-156">-StorageEndpoint</span></span>
<span data-ttu-id="3dc1a-157">Specifica l'endpoint per l'archiviazione (BLOB, Table, Queue e file) Access.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-157">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="3dc1a-158">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="3dc1a-158">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="3dc1a-159">Specifica il suffisso del nome di dominio per i servizi di Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-159">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="3dc1a-160">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3dc1a-160">-BatchEndpointResourceId</span></span>
<span data-ttu-id="3dc1a-161">Identificatore delle risorse del servizio batch di Azure che è il destinatario del token richiesto</span><span class="sxs-lookup"><span data-stu-id="3dc1a-161">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="3dc1a-162">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="3dc1a-162">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="3dc1a-163">Specifica l'endpoint per l'accesso alla query per gli approfondimenti operativi.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-163">Specifies the endpoint for the Operational Insights query access.</span></span> 

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

### <span data-ttu-id="3dc1a-164">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3dc1a-164">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="3dc1a-165">Specifica il gruppo di destinatari per i token di accesso che autorizzano le richieste di servizi per gli approfondimenti operativi.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-165">Specifies the audience for access tokens that authorize requests for Operational Insights services.</span></span>

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

### <span data-ttu-id="3dc1a-166">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3dc1a-166">-Confirm</span></span>
<span data-ttu-id="3dc1a-167">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dc1a-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dc1a-168">-WhatIf</span></span>
<span data-ttu-id="3dc1a-169">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-169">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3dc1a-170">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dc1a-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dc1a-171">CommonParameters</span></span>
<span data-ttu-id="3dc1a-172">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dc1a-173">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dc1a-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dc1a-174">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3dc1a-174">INPUTS</span></span>

### <span data-ttu-id="3dc1a-175">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3dc1a-175">None</span></span>
<span data-ttu-id="3dc1a-176">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-176">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3dc1a-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3dc1a-177">OUTPUTS</span></span>

### <span data-ttu-id="3dc1a-178">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3dc1a-178">PSAzureEnvironment</span></span>

## <span data-ttu-id="3dc1a-179">Note</span><span class="sxs-lookup"><span data-stu-id="3dc1a-179">NOTES</span></span>

## <span data-ttu-id="3dc1a-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3dc1a-180">RELATED LINKS</span></span>

[<span data-ttu-id="3dc1a-181">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="3dc1a-181">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="3dc1a-182">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="3dc1a-182">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="3dc1a-183">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="3dc1a-183">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

