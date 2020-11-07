---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
ms.openlocfilehash: 510e191f29936b04e1d3e49b71ca1a6dfa160d20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688000"
---
# <span data-ttu-id="3c858-101">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="3c858-101">Add-AzureRmEnvironment</span></span>

## <span data-ttu-id="3c858-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3c858-102">SYNOPSIS</span></span>
<span data-ttu-id="3c858-103">Aggiunge endpoint e metadati per un'istanza di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="3c858-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c858-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c858-104">SYNTAX</span></span>

### <span data-ttu-id="3c858-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3c858-105">Name (Default)</span></span>
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
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c858-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c858-106">ARMEndpoint</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-DataLakeAudience] <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c858-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c858-107">DESCRIPTION</span></span>
<span data-ttu-id="3c858-108">Il cmdlet Add-AzureRmEnvironment aggiunge endpoint e metadati per consentire ai cmdlet di Azure Resource Manager di connettersi con una nuova istanza di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="3c858-108">The Add-AzureRmEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="3c858-109">Gli ambienti predefiniti AzureCloud e AzureChinaCloud sono destinati alle istanze pubbliche esistenti di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="3c858-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="3c858-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c858-110">EXAMPLES</span></span>

### <span data-ttu-id="3c858-111">Esempio 1: creazione e modifica di un nuovo ambiente</span><span class="sxs-lookup"><span data-stu-id="3c858-111">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="3c858-112">In questo esempio creiamo un nuovo ambiente Azure con endpoint di esempio usando Add-AzureRmEnvironment e quindi modifichiamo il valore degli attributi ActiveDirectoryEndpoint e GraphEndpoint dell'ambiente creato usando il cmdlet Set-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="3c858-112">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="3c858-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c858-113">PARAMETERS</span></span>

### <span data-ttu-id="3c858-114">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c858-114">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="3c858-115">Specifica l'autorità di base per l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3c858-115">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="3c858-116">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3c858-116">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="3c858-117">Specifica il gruppo di destinatari per i token che eseguono l'autenticazione delle richieste agli endpoint di Azure Resource Manager o RDFE (Service Management).</span><span class="sxs-lookup"><span data-stu-id="3c858-117">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="3c858-118">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="3c858-118">-AdTenant</span></span>
<span data-ttu-id="3c858-119">Specifica il tenant di Active Directory predefinito.</span><span class="sxs-lookup"><span data-stu-id="3c858-119">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="3c858-120">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c858-120">-ARMEndpoint</span></span>
<span data-ttu-id="3c858-121">Endpoint di Azure Resource Manager</span><span class="sxs-lookup"><span data-stu-id="3c858-121">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="3c858-122">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="3c858-122">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="3c858-123">Suffisso DNS dei servizi di catalogo e lavoro di Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="3c858-123">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="3c858-124">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="3c858-124">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="3c858-125">Suffisso DNS di Azure Data Lake Store FileSystem.</span><span class="sxs-lookup"><span data-stu-id="3c858-125">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="3c858-126">Esempio: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="3c858-126">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="3c858-127">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="3c858-127">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="3c858-128">Specifica il suffisso del nome di dominio per i Servizi Key Vault.</span><span class="sxs-lookup"><span data-stu-id="3c858-128">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="3c858-129">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3c858-129">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="3c858-130">Specifica il gruppo di destinatari per i token di accesso che autorizzano le richieste per i Servizi Key Vault.</span><span class="sxs-lookup"><span data-stu-id="3c858-130">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c858-131">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="3c858-131">-DataLakeAudience</span></span>
<span data-ttu-id="3c858-132">Il gruppo di destinatari per l'autenticazione dei token con l'endpoint di servizi AD data Lake.</span><span class="sxs-lookup"><span data-stu-id="3c858-132">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="3c858-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c858-133">-DefaultProfile</span></span>
<span data-ttu-id="3c858-134">Credeetnails, tenant e Subscription usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3c858-134">The credeetnails, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c858-135">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="3c858-135">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="3c858-136">Indica che l'autenticazione locale di Active Directory Federation Services (ADFS) è consentita.</span><span class="sxs-lookup"><span data-stu-id="3c858-136">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="3c858-137">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c858-137">-GalleryEndpoint</span></span>
<span data-ttu-id="3c858-138">Specifica l'endpoint della raccolta di modelli di distribuzione di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="3c858-138">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="3c858-139">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="3c858-139">-GraphAudience</span></span>
<span data-ttu-id="3c858-140">Il gruppo di destinatari per l'autenticazione dei token con l'endpoint del grafico AD.</span><span class="sxs-lookup"><span data-stu-id="3c858-140">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="3c858-141">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c858-141">-GraphEndpoint</span></span>
<span data-ttu-id="3c858-142">Specifica l'URL per le richieste di grafico (metadati Active Directory).</span><span class="sxs-lookup"><span data-stu-id="3c858-142">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="3c858-143">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="3c858-143">-ManagementPortalUrl</span></span>
<span data-ttu-id="3c858-144">Specifica l'URL per il portale di gestione.</span><span class="sxs-lookup"><span data-stu-id="3c858-144">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="3c858-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c858-145">-Name</span></span>
<span data-ttu-id="3c858-146">Specifica il nome dell'ambiente da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="3c858-146">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="3c858-147">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="3c858-147">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="3c858-148">Specifica l'URL da cui possono essere scaricati i file con estensione publishsettings.</span><span class="sxs-lookup"><span data-stu-id="3c858-148">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="3c858-149">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c858-149">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="3c858-150">Specifica l'URL per le richieste di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="3c858-150">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="3c858-151">-Ambito</span><span class="sxs-lookup"><span data-stu-id="3c858-151">-Scope</span></span>
<span data-ttu-id="3c858-152">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="3c858-152">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="3c858-153">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c858-153">-ServiceEndpoint</span></span>
<span data-ttu-id="3c858-154">Specifica l'endpoint per le richieste di gestione dei servizi (RDFE).</span><span class="sxs-lookup"><span data-stu-id="3c858-154">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="3c858-155">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="3c858-155">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="3c858-156">Specifica il suffisso del nome di dominio per i server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="3c858-156">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="3c858-157">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c858-157">-StorageEndpoint</span></span>
<span data-ttu-id="3c858-158">Specifica l'endpoint per l'archiviazione (BLOB, Table, Queue e file) Access.</span><span class="sxs-lookup"><span data-stu-id="3c858-158">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="3c858-159">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="3c858-159">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="3c858-160">Specifica il suffisso del nome di dominio per i servizi di Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="3c858-160">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="3c858-161">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3c858-161">-Confirm</span></span>
<span data-ttu-id="3c858-162">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c858-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c858-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c858-163">-WhatIf</span></span>
<span data-ttu-id="3c858-164">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c858-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c858-165">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c858-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c858-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c858-166">CommonParameters</span></span>
<span data-ttu-id="3c858-167">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c858-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c858-168">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c858-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c858-169">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3c858-169">INPUTS</span></span>

## <span data-ttu-id="3c858-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c858-170">OUTPUTS</span></span>

### <span data-ttu-id="3c858-171">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3c858-171">PSAzureEnvironment</span></span>
<span data-ttu-id="3c858-172">Questo cmdlet restituisce il set di endpoint e metadati necessari per comunicare con un'istanza di Azure.</span><span class="sxs-lookup"><span data-stu-id="3c858-172">This cmdlet returns the set of endpoints and metadata needed to communicate with an instance of Azure.</span></span>

## <span data-ttu-id="3c858-173">Note</span><span class="sxs-lookup"><span data-stu-id="3c858-173">NOTES</span></span>

## <span data-ttu-id="3c858-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c858-174">RELATED LINKS</span></span>

[<span data-ttu-id="3c858-175">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="3c858-175">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="3c858-176">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="3c858-176">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="3c858-177">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="3c858-177">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

