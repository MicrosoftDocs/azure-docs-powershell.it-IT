---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
ms.openlocfilehash: cb7617f8db1e8aadd181fc5e978006bbeaae5c0b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673724"
---
# <span data-ttu-id="841df-101">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="841df-101">Set-AzEnvironment</span></span>

## <span data-ttu-id="841df-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="841df-102">SYNOPSIS</span></span>
<span data-ttu-id="841df-103">Imposta le proprietà per un ambiente Azure.</span><span class="sxs-lookup"><span data-stu-id="841df-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="841df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="841df-104">SYNTAX</span></span>

### <span data-ttu-id="841df-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="841df-105">Name (Default)</span></span>
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
 [-AzureAnalysisServicesEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="841df-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="841df-106">ARMEndpoint</span></span>
```
Set-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="841df-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="841df-107">DESCRIPTION</span></span>
<span data-ttu-id="841df-108">Il cmdlet Set-AzEnvironment imposta gli endpoint e i metadati per la connessione a un'istanza di Azure.</span><span class="sxs-lookup"><span data-stu-id="841df-108">The Set-AzEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="841df-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="841df-109">EXAMPLES</span></span>

### <span data-ttu-id="841df-110">Esempio 1: creazione e modifica di un nuovo ambiente</span><span class="sxs-lookup"><span data-stu-id="841df-110">Example 1: Creating and modifying a new environment</span></span>
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
```

<span data-ttu-id="841df-111">In questo esempio creiamo un nuovo ambiente Azure con endpoint di esempio usando Add-AzEnvironment e quindi modifichiamo il valore degli attributi ActiveDirectoryEndpoint e GraphEndpoint dell'ambiente creato usando il cmdlet Set-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="841df-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

## <span data-ttu-id="841df-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="841df-112">PARAMETERS</span></span>

### <span data-ttu-id="841df-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="841df-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="841df-114">Specifica l'autorità di base per l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="841df-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="841df-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="841df-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="841df-116">Specifica il gruppo di destinatari per i token che eseguono l'autenticazione delle richieste agli endpoint di Azure Resource Manager o RDFE (Service Management).</span><span class="sxs-lookup"><span data-stu-id="841df-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="841df-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="841df-117">-AdTenant</span></span>
<span data-ttu-id="841df-118">Specifica il tenant di Active Directory predefinito.</span><span class="sxs-lookup"><span data-stu-id="841df-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="841df-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="841df-119">-ARMEndpoint</span></span>
<span data-ttu-id="841df-120">Endpoint di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="841df-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="841df-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="841df-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="841df-122">Identificatore delle risorse della risorsa di Azure Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="841df-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="841df-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="841df-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="841df-124">Endpoint da usare per comunicare con l'API di analisi di Azure log.</span><span class="sxs-lookup"><span data-stu-id="841df-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="841df-125">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="841df-125">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="841df-126">Suffisso DNS dei servizi di catalogo e lavoro di Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="841df-126">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="841df-127">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="841df-127">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="841df-128">Suffisso DNS di Azure Data Lake Store FileSystem.</span><span class="sxs-lookup"><span data-stu-id="841df-128">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="841df-129">Esempio: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="841df-129">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="841df-130">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="841df-130">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="841df-131">Suffisso DNS del servizio Key Vault di Azure.</span><span class="sxs-lookup"><span data-stu-id="841df-131">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="841df-132">L'esempio è vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="841df-132">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="841df-133">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="841df-133">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="841df-134">Identificatore delle risorse del servizio dati di Azure Key Vault che è il destinatario del token richiesto.</span><span class="sxs-lookup"><span data-stu-id="841df-134">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="841df-135">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="841df-135">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="841df-136">Endpoint da usare per comunicare con l'API di analisi di Azure log.</span><span class="sxs-lookup"><span data-stu-id="841df-136">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="841df-137">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="841df-137">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="841df-138">Il gruppo di destinatari per l'autenticazione dei token con l'API di analisi del log di Azure.</span><span class="sxs-lookup"><span data-stu-id="841df-138">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="841df-139">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="841df-139">-BatchEndpointResourceId</span></span>
<span data-ttu-id="841df-140">Identificatore delle risorse del servizio batch di Azure che è il destinatario del token richiesto</span><span class="sxs-lookup"><span data-stu-id="841df-140">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="841df-141">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="841df-141">-DataLakeAudience</span></span>
<span data-ttu-id="841df-142">Il gruppo di destinatari per l'autenticazione dei token con l'endpoint di servizi AD data Lake.</span><span class="sxs-lookup"><span data-stu-id="841df-142">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="841df-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="841df-143">-DefaultProfile</span></span>
<span data-ttu-id="841df-144">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="841df-144">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="841df-145">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="841df-145">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="841df-146">Indica che l'autenticazione locale di Active Directory Federation Services (ADFS) è consentita.</span><span class="sxs-lookup"><span data-stu-id="841df-146">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="841df-147">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="841df-147">-GalleryEndpoint</span></span>
<span data-ttu-id="841df-148">Specifica l'endpoint della raccolta di modelli di distribuzione di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="841df-148">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="841df-149">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="841df-149">-GraphAudience</span></span>
<span data-ttu-id="841df-150">Il gruppo di destinatari per l'autenticazione dei token con l'endpoint del grafico AD.</span><span class="sxs-lookup"><span data-stu-id="841df-150">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="841df-151">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="841df-151">-GraphEndpoint</span></span>
<span data-ttu-id="841df-152">Specifica l'URL per le richieste di grafico (metadati Active Directory).</span><span class="sxs-lookup"><span data-stu-id="841df-152">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="841df-153">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="841df-153">-ManagementPortalUrl</span></span>
<span data-ttu-id="841df-154">Specifica l'URL per il portale di gestione.</span><span class="sxs-lookup"><span data-stu-id="841df-154">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="841df-155">-Nome</span><span class="sxs-lookup"><span data-stu-id="841df-155">-Name</span></span>
<span data-ttu-id="841df-156">Specifica il nome dell'ambiente da modificare.</span><span class="sxs-lookup"><span data-stu-id="841df-156">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="841df-157">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="841df-157">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="841df-158">Specifica l'URL da cui possono essere scaricati i file con estensione publishsettings.</span><span class="sxs-lookup"><span data-stu-id="841df-158">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="841df-159">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="841df-159">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="841df-160">Specifica l'URL per le richieste di gestione risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="841df-160">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="841df-161">-Ambito</span><span class="sxs-lookup"><span data-stu-id="841df-161">-Scope</span></span>
<span data-ttu-id="841df-162">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="841df-162">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="841df-163">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="841df-163">-ServiceEndpoint</span></span>
<span data-ttu-id="841df-164">Specifica l'endpoint per le richieste di gestione dei servizi (RDFE).</span><span class="sxs-lookup"><span data-stu-id="841df-164">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="841df-165">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="841df-165">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="841df-166">Specifica il suffisso del nome di dominio per i server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="841df-166">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="841df-167">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="841df-167">-StorageEndpoint</span></span>
<span data-ttu-id="841df-168">Specifica l'endpoint per l'archiviazione (BLOB, Table, Queue e file) Access.</span><span class="sxs-lookup"><span data-stu-id="841df-168">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="841df-169">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="841df-169">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="841df-170">Specifica il suffisso del nome di dominio per i servizi di Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="841df-170">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="841df-171">-Confermare</span><span class="sxs-lookup"><span data-stu-id="841df-171">-Confirm</span></span>
<span data-ttu-id="841df-172">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="841df-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="841df-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="841df-173">-WhatIf</span></span>
<span data-ttu-id="841df-174">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="841df-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="841df-175">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="841df-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="841df-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="841df-176">CommonParameters</span></span>
<span data-ttu-id="841df-177">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="841df-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="841df-178">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="841df-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="841df-179">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="841df-179">INPUTS</span></span>

### <span data-ttu-id="841df-180">System. String</span><span class="sxs-lookup"><span data-stu-id="841df-180">System.String</span></span>

### <span data-ttu-id="841df-181">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="841df-181">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="841df-182">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="841df-182">OUTPUTS</span></span>

### <span data-ttu-id="841df-183">Microsoft. Azure. Commands. profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="841df-183">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="841df-184">Note</span><span class="sxs-lookup"><span data-stu-id="841df-184">NOTES</span></span>

## <span data-ttu-id="841df-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="841df-185">RELATED LINKS</span></span>

[<span data-ttu-id="841df-186">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="841df-186">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="841df-187">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="841df-187">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="841df-188">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="841df-188">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

