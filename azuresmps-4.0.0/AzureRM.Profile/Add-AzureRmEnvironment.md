---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 650b5e2c930577101337c4fe0f33db9c32160e1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490830"
---
# <span data-ttu-id="f1778-101">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="f1778-101">Add-AzureRmEnvironment</span></span>

## <span data-ttu-id="f1778-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f1778-102">SYNOPSIS</span></span>
<span data-ttu-id="f1778-103">Aggiunge endpoint e metadati per un'istanza di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="f1778-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="f1778-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f1778-104">SYNTAX</span></span>

```
Add-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1778-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1778-105">DESCRIPTION</span></span>
<span data-ttu-id="f1778-106">Il cmdlet Add-AzureRmEnvironment aggiunge endpoint e metadati per consentire ai cmdlet di Azure Resource Manager di connettersi con una nuova istanza di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="f1778-106">The Add-AzureRmEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="f1778-107">Gli ambienti predefiniti AzureCloud e AzureChinaCloud sono destinati alle istanze pubbliche esistenti di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="f1778-107">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="f1778-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f1778-108">EXAMPLES</span></span>

### <span data-ttu-id="f1778-109">Esempio 1: creazione e modifica di un nuovo ambiente</span><span class="sxs-lookup"><span data-stu-id="f1778-109">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="f1778-110">In questo esempio creiamo un nuovo ambiente Azure con endpoint di esempio usando Add-AzureRmEnvironment e quindi modifichiamo il valore degli attributi ActiveDirectoryEndpoint e GraphEndpoint dell'ambiente creato usando il cmdlet Set-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="f1778-110">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="f1778-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f1778-111">PARAMETERS</span></span>

### <span data-ttu-id="f1778-112">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1778-112">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="f1778-113">Specifica l'autorità di base per l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f1778-113">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1778-114">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f1778-114">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="f1778-115">Specifica il gruppo di destinatari per i token che eseguono l'autenticazione delle richieste agli endpoint di Azure Resource Manager o RDFE (Service Management).</span><span class="sxs-lookup"><span data-stu-id="f1778-115">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1778-116">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="f1778-116">-AdTenant</span></span>
<span data-ttu-id="f1778-117">Specifica il tenant di Active Directory predefinito.</span><span class="sxs-lookup"><span data-stu-id="f1778-117">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1778-118">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f1778-118">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="f1778-119">Suffisso DNS dei servizi di catalogo e lavoro di Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="f1778-119">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1778-120">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f1778-120">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="f1778-121">Suffisso DNS di Azure Data Lake Store FileSystem.</span><span class="sxs-lookup"><span data-stu-id="f1778-121">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="f1778-122">Esempio: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="f1778-122">Example: azuredatalake.net</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1778-123">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f1778-123">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="f1778-124">Specifica il suffisso del nome di dominio per i Servizi Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f1778-124">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="f1778-125">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f1778-125">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="f1778-126">Specifica il gruppo di destinatari per i token di accesso che autorizzano le richieste per i Servizi Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f1778-126">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

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

### <span data-ttu-id="f1778-127">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="f1778-127">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="f1778-128">Indica che l'autenticazione locale di Active Directory Federation Services (ADFS) è consentita.</span><span class="sxs-lookup"><span data-stu-id="f1778-128">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1778-129">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1778-129">-GalleryEndpoint</span></span>
<span data-ttu-id="f1778-130">Specifica l'endpoint della raccolta di modelli di distribuzione di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="f1778-130">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1778-131">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="f1778-131">-GraphAudience</span></span>
<span data-ttu-id="f1778-132">Il gruppo di destinatari per l'autenticazione dei token con l'endpoint del grafico AD.</span><span class="sxs-lookup"><span data-stu-id="f1778-132">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1778-133">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1778-133">-GraphEndpoint</span></span>
<span data-ttu-id="f1778-134">Specifica l'URL per le richieste di grafico (metadati Active Directory).</span><span class="sxs-lookup"><span data-stu-id="f1778-134">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1778-135">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="f1778-135">-ManagementPortalUrl</span></span>
<span data-ttu-id="f1778-136">Specifica l'URL per il portale di gestione.</span><span class="sxs-lookup"><span data-stu-id="f1778-136">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1778-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1778-137">-Name</span></span>
<span data-ttu-id="f1778-138">Specifica il nome dell'ambiente da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="f1778-138">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="f1778-139">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="f1778-139">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="f1778-140">Specifica l'URL da cui possono essere scaricati i file con estensione publishsettings.</span><span class="sxs-lookup"><span data-stu-id="f1778-140">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1778-141">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1778-141">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="f1778-142">Specifica l'URL per le richieste di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="f1778-142">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1778-143">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1778-143">-ServiceEndpoint</span></span>
<span data-ttu-id="f1778-144">Specifica l'endpoint per le richieste di gestione dei servizi (RDFE).</span><span class="sxs-lookup"><span data-stu-id="f1778-144">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1778-145">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f1778-145">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="f1778-146">Specifica il suffisso del nome di dominio per i server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="f1778-146">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1778-147">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="f1778-147">-StorageEndpoint</span></span>
<span data-ttu-id="f1778-148">Specifica l'endpoint per l'archiviazione (BLOB, Table, Queue e file) Access.</span><span class="sxs-lookup"><span data-stu-id="f1778-148">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="f1778-149">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f1778-149">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="f1778-150">Specifica il suffisso del nome di dominio per i servizi di Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="f1778-150">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1778-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f1778-151">-Confirm</span></span>
<span data-ttu-id="f1778-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1778-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1778-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1778-153">-WhatIf</span></span>
<span data-ttu-id="f1778-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f1778-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1778-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f1778-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1778-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1778-156">CommonParameters</span></span>
<span data-ttu-id="f1778-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1778-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1778-158">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1778-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1778-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f1778-159">INPUTS</span></span>

## <span data-ttu-id="f1778-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f1778-160">OUTPUTS</span></span>

### <span data-ttu-id="f1778-161">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="f1778-161">PSAzureEnvironment</span></span>
<span data-ttu-id="f1778-162">Questo cmdlet restituisce il set di endpoint e metadati necessari per comunicare con un'istanza di Azure.</span><span class="sxs-lookup"><span data-stu-id="f1778-162">This cmdlet returns the set of endpoints and metadata needed to communicate with an instance of Azure.</span></span>

## <span data-ttu-id="f1778-163">Note</span><span class="sxs-lookup"><span data-stu-id="f1778-163">NOTES</span></span>

## <span data-ttu-id="f1778-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f1778-164">RELATED LINKS</span></span>

[<span data-ttu-id="f1778-165">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="f1778-165">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="f1778-166">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="f1778-166">Remove-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="f1778-167">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="f1778-167">Set-AzureRMEnvironment</span></span>]()

