---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37e8952ab7337ae69e5c23ed4ab09e651acfac8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490938"
---
# <span data-ttu-id="9904c-101">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="9904c-101">Set-AzureRmEnvironment</span></span>

## <span data-ttu-id="9904c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9904c-102">SYNOPSIS</span></span>
<span data-ttu-id="9904c-103">Imposta le proprietà per un ambiente Azure.</span><span class="sxs-lookup"><span data-stu-id="9904c-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="9904c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9904c-104">SYNTAX</span></span>

```
Set-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9904c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9904c-105">DESCRIPTION</span></span>
<span data-ttu-id="9904c-106">Il cmdlet Set-AzureRMEnvironment imposta gli endpoint e i metadati per la connessione a un'istanza di Azure.</span><span class="sxs-lookup"><span data-stu-id="9904c-106">The Set-AzureRMEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="9904c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9904c-107">EXAMPLES</span></span>

### <span data-ttu-id="9904c-108">Esempio 1: creazione e modifica di un nuovo ambiente</span><span class="sxs-lookup"><span data-stu-id="9904c-108">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="9904c-109">In questo esempio creiamo un nuovo ambiente Azure con endpoint di esempio usando Add-AzureRmEnvironment e quindi modifichiamo il valore degli attributi ActiveDirectoryEndpoint e GraphEndpoint dell'ambiente creato usando il cmdlet Set-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="9904c-109">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="9904c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9904c-110">PARAMETERS</span></span>

### <span data-ttu-id="9904c-111">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="9904c-111">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="9904c-112">Specifica l'autorità di base per l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9904c-112">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="9904c-113">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="9904c-113">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="9904c-114">Specifica il gruppo di destinatari per i token che eseguono l'autenticazione delle richieste agli endpoint di Azure Resource Manager o RDFE (Service Management).</span><span class="sxs-lookup"><span data-stu-id="9904c-114">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="9904c-115">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="9904c-115">-AdTenant</span></span>
<span data-ttu-id="9904c-116">Specifica il tenant di Active Directory predefinito.</span><span class="sxs-lookup"><span data-stu-id="9904c-116">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="9904c-117">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="9904c-117">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="9904c-118">Suffisso DNS dei servizi di catalogo e lavoro di Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="9904c-118">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="9904c-119">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="9904c-119">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="9904c-120">Suffisso DNS di Azure Data Lake Store FileSystem.</span><span class="sxs-lookup"><span data-stu-id="9904c-120">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="9904c-121">Esempio: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="9904c-121">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="9904c-122">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="9904c-122">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="9904c-123">Specifica il suffisso del nome di dominio per i Servizi Key Vault.</span><span class="sxs-lookup"><span data-stu-id="9904c-123">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="9904c-124">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="9904c-124">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="9904c-125">Specifica il gruppo di destinatari per i token di accesso che autorizzano le richieste per i Servizi Key Vault.</span><span class="sxs-lookup"><span data-stu-id="9904c-125">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

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

### <span data-ttu-id="9904c-126">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="9904c-126">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="9904c-127">Indica che l'autenticazione locale di Active Directory Federation Services (ADFS) è consentita.</span><span class="sxs-lookup"><span data-stu-id="9904c-127">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="9904c-128">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="9904c-128">-GalleryEndpoint</span></span>
<span data-ttu-id="9904c-129">Specifica l'endpoint della raccolta di modelli di distribuzione di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="9904c-129">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="9904c-130">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="9904c-130">-GraphAudience</span></span>
<span data-ttu-id="9904c-131">Il gruppo di destinatari per l'autenticazione dei token con l'endpoint del grafico AD.</span><span class="sxs-lookup"><span data-stu-id="9904c-131">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="9904c-132">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="9904c-132">-GraphEndpoint</span></span>
<span data-ttu-id="9904c-133">Specifica l'URL per le richieste di grafico (metadati Active Directory).</span><span class="sxs-lookup"><span data-stu-id="9904c-133">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="9904c-134">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="9904c-134">-ManagementPortalUrl</span></span>
<span data-ttu-id="9904c-135">Specifica l'URL per il portale di gestione.</span><span class="sxs-lookup"><span data-stu-id="9904c-135">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="9904c-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="9904c-136">-Name</span></span>
<span data-ttu-id="9904c-137">Specifica il nome dell'ambiente da modificare.</span><span class="sxs-lookup"><span data-stu-id="9904c-137">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="9904c-138">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="9904c-138">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="9904c-139">Specifica l'URL da cui possono essere scaricati i file con estensione publishsettings.</span><span class="sxs-lookup"><span data-stu-id="9904c-139">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="9904c-140">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9904c-140">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="9904c-141">Specifica l'URL per le richieste di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="9904c-141">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="9904c-142">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="9904c-142">-ServiceEndpoint</span></span>
<span data-ttu-id="9904c-143">Specifica l'endpoint per le richieste di gestione dei servizi (RDFE).</span><span class="sxs-lookup"><span data-stu-id="9904c-143">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="9904c-144">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="9904c-144">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="9904c-145">Specifica il suffisso del nome di dominio per i server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="9904c-145">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="9904c-146">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="9904c-146">-StorageEndpoint</span></span>
<span data-ttu-id="9904c-147">Specifica l'endpoint per l'archiviazione (BLOB, Table, Queue e file) Access.</span><span class="sxs-lookup"><span data-stu-id="9904c-147">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="9904c-148">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="9904c-148">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="9904c-149">Specifica il suffisso del nome di dominio per i servizi di Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="9904c-149">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="9904c-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9904c-150">-Confirm</span></span>
<span data-ttu-id="9904c-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9904c-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9904c-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9904c-152">-WhatIf</span></span>
<span data-ttu-id="9904c-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9904c-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9904c-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9904c-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9904c-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9904c-155">CommonParameters</span></span>
<span data-ttu-id="9904c-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9904c-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9904c-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9904c-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9904c-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9904c-158">INPUTS</span></span>

## <span data-ttu-id="9904c-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9904c-159">OUTPUTS</span></span>

### <span data-ttu-id="9904c-160">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="9904c-160">PSAzureEnvironment</span></span>

## <span data-ttu-id="9904c-161">Note</span><span class="sxs-lookup"><span data-stu-id="9904c-161">NOTES</span></span>

## <span data-ttu-id="9904c-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9904c-162">RELATED LINKS</span></span>

[<span data-ttu-id="9904c-163">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="9904c-163">Add-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="9904c-164">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="9904c-164">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="9904c-165">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="9904c-165">Remove-AzureRMEnvironment</span></span>]()

