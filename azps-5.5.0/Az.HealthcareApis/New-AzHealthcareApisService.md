---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: 33f1af70b0fef7e89ccb584ed3b69f32e2810690
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196270"
---
# <span data-ttu-id="42b1a-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="42b1a-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="42b1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42b1a-102">SYNOPSIS</span></span>
<span data-ttu-id="42b1a-103">Crea i metadati di un'istanza del servizio.</span><span class="sxs-lookup"><span data-stu-id="42b1a-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="42b1a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42b1a-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>] [-ExportStorageAccountName <String>]
 [-EnableSmartProxy] [-ManagedIdentity] [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42b1a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="42b1a-105">DESCRIPTION</span></span>
<span data-ttu-id="42b1a-106">Crea o aggiorna i metadati di un'istanza del servizio.</span><span class="sxs-lookup"><span data-stu-id="42b1a-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="42b1a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42b1a-107">EXAMPLES</span></span>

### <span data-ttu-id="42b1a-108">Esempio 1: crea un nuovo servizio Azure healthcareapis fhir denominato MyService nel gruppo di risorse MyResourceGroup in una posizione westus2 con la velocità effettiva dell'offerta tramitedb = 400</span><span class="sxs-lookup"><span data-stu-id="42b1a-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput 400

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  : 
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### <span data-ttu-id="42b1a-109">Esempio 2: Crea un nuovo servizio Azure healthcareapis fhir denominato MyService nel gruppo di risorse MyResourceGroup in un percorso westus2 con offerta tramitedb di Azure = 400 e uri chiave vault chiave "https:// \<my-keyvault> .vault.azure.net/keys/ \<my-key> "</span><span class="sxs-lookup"><span data-stu-id="42b1a-109">Example 2 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput 400 -CosmosKeyVaultKeyUri "https://<my-keyvault>.vault.azure.net/keys/<my-key>"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  : https://<my-keyvault>.vault.azure.net/keys/<my-key>
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

## <span data-ttu-id="42b1a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42b1a-110">PARAMETERS</span></span>

### <span data-ttu-id="42b1a-111">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="42b1a-111">-AccessPolicyObjectId</span></span>
<span data-ttu-id="42b1a-112">Elenco di ID oggetto dei criteri di accesso.</span><span class="sxs-lookup"><span data-stu-id="42b1a-112">List of Access Policy Object IDs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b1a-113">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="42b1a-113">-AllowCorsCredential</span></span>
<span data-ttu-id="42b1a-114">HealthcareApis Fhir Service AllowCorsCredentials.</span><span class="sxs-lookup"><span data-stu-id="42b1a-114">HealthcareApis Fhir Service AllowCorsCredentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b1a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42b1a-115">-AsJob</span></span>
<span data-ttu-id="42b1a-116">Eseguire il cmdlet come processo in background.</span><span class="sxs-lookup"><span data-stu-id="42b1a-116">Run cmdlet as a job in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b1a-117">-Gruppo di destinatari</span><span class="sxs-lookup"><span data-stu-id="42b1a-117">-Audience</span></span>
<span data-ttu-id="42b1a-118">Destinatari del servizio HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="42b1a-118">HealthcareApis Fhir Service Audience.</span></span>

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

### <span data-ttu-id="42b1a-119">-Authority</span><span class="sxs-lookup"><span data-stu-id="42b1a-119">-Authority</span></span>
<span data-ttu-id="42b1a-120">HealthcareApis Fhir Service Authority.</span><span class="sxs-lookup"><span data-stu-id="42b1a-120">HealthcareApis Fhir Service Authority.</span></span>

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

### <span data-ttu-id="42b1a-121">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="42b1a-121">-CorsHeader</span></span>
<span data-ttu-id="42b1a-122">HealthcareApis Fhir Service List of Cors Header.</span><span class="sxs-lookup"><span data-stu-id="42b1a-122">HealthcareApis Fhir Service List of Cors Header.</span></span>
<span data-ttu-id="42b1a-123">Specificare le intestazioni HTTP che possono essere usate durante la richiesta.</span><span class="sxs-lookup"><span data-stu-id="42b1a-123">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="42b1a-124">Usare " \* " per qualsiasi intestazione.</span><span class="sxs-lookup"><span data-stu-id="42b1a-124">Use " \* " for any header.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b1a-125">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="42b1a-125">-CorsMaxAge</span></span>
<span data-ttu-id="42b1a-126">HealthcareApis Fhir Service Cors Max Age.</span><span class="sxs-lookup"><span data-stu-id="42b1a-126">HealthcareApis Fhir Service Cors Max Age.</span></span>
<span data-ttu-id="42b1a-127">Specificare per quanto tempo un risultato di una richiesta può essere memorizzato nella cache in secondi.</span><span class="sxs-lookup"><span data-stu-id="42b1a-127">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="42b1a-128">Ad esempio: 600 significa 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="42b1a-128">Example: 600 means 10 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b1a-129">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="42b1a-129">-CorsMethod</span></span>
<span data-ttu-id="42b1a-130">HealthcareApis Fhir Service List of Cors Method.</span><span class="sxs-lookup"><span data-stu-id="42b1a-130">HealthcareApis Fhir Service List of Cors Method.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b1a-131">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="42b1a-131">-CorsOrigin</span></span>
<span data-ttu-id="42b1a-132">HealthcareApis Fhir Service List of Cors Origin.</span><span class="sxs-lookup"><span data-stu-id="42b1a-132">HealthcareApis Fhir Service List of Cors Origin.</span></span>
<span data-ttu-id="42b1a-133">Specificare gli URL dei siti di origine che possono accedere a questa API oppure usare " \* " per consentire l'accesso da qualsiasi sito.</span><span class="sxs-lookup"><span data-stu-id="42b1a-133">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b1a-134">-SottochiaviKeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="42b1a-134">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="42b1a-135">HealthcareApis Fhir ServiceKeyVaultKeyUri.</span><span class="sxs-lookup"><span data-stu-id="42b1a-135">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="42b1a-136">URI della chiave gestita dal cliente per il database di supporto.</span><span class="sxs-lookup"><span data-stu-id="42b1a-136">The URI of the customer-managed key for the backing database.</span></span>

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

### <span data-ttu-id="42b1a-137">-MasOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="42b1a-137">-CosmosOfferThroughput</span></span>
<span data-ttu-id="42b1a-138">HealthcareApis Fhir Service ClustersOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="42b1a-138">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b1a-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42b1a-139">-DefaultProfile</span></span>
<span data-ttu-id="42b1a-140">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42b1a-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42b1a-141">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="42b1a-141">-EnableSmartProxy</span></span>
<span data-ttu-id="42b1a-142">HealthcareApis Fhir Service EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="42b1a-142">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b1a-143">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="42b1a-143">-ExportStorageAccountName</span></span>
<span data-ttu-id="42b1a-144">Nome dell'account di archiviazione di esportazione del servizio HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="42b1a-144">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="42b1a-145">-FhirVersion</span><span class="sxs-lookup"><span data-stu-id="42b1a-145">-FhirVersion</span></span>
<span data-ttu-id="42b1a-146">Versione Fhir.</span><span class="sxs-lookup"><span data-stu-id="42b1a-146">Fhir Version.</span></span>

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

### <span data-ttu-id="42b1a-147">-Kind</span><span class="sxs-lookup"><span data-stu-id="42b1a-147">-Kind</span></span>
<span data-ttu-id="42b1a-148">Tipo di servizio HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="42b1a-148">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="42b1a-149">Il valore predefinito è Fhir</span><span class="sxs-lookup"><span data-stu-id="42b1a-149">The default value is Fhir</span></span>

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

### <span data-ttu-id="42b1a-150">-Location</span><span class="sxs-lookup"><span data-stu-id="42b1a-150">-Location</span></span>
<span data-ttu-id="42b1a-151">Posizione del servizio HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="42b1a-151">HealthcareApis Service Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b1a-152">-ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="42b1a-152">-ManagedIdentity</span></span>
<span data-ttu-id="42b1a-153">Usare l'identità gestita?</span><span class="sxs-lookup"><span data-stu-id="42b1a-153">Use Managed Identity?</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b1a-154">-Name</span><span class="sxs-lookup"><span data-stu-id="42b1a-154">-Name</span></span>
<span data-ttu-id="42b1a-155">Nome del servizio HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="42b1a-155">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b1a-156">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="42b1a-156">-PublicNetworkAccess</span></span>
<span data-ttu-id="42b1a-157">Tipo di accesso di rete per il servizio Fhir.</span><span class="sxs-lookup"><span data-stu-id="42b1a-157">The network access type for Fhir service.</span></span> <span data-ttu-id="42b1a-158">Comunemente `Enabled` o `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="42b1a-158">Commonly `Enabled` or `Disabled`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b1a-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42b1a-159">-ResourceGroupName</span></span>
<span data-ttu-id="42b1a-160">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="42b1a-160">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42b1a-161">-Tag</span><span class="sxs-lookup"><span data-stu-id="42b1a-161">-Tag</span></span>
<span data-ttu-id="42b1a-162">Tag dell'account di servizio di HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="42b1a-162">HealthcareApis Fhir Service Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b1a-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42b1a-163">-Confirm</span></span>
<span data-ttu-id="42b1a-164">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42b1a-164">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b1a-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42b1a-165">-WhatIf</span></span>
<span data-ttu-id="42b1a-166">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42b1a-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42b1a-167">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42b1a-167">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b1a-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42b1a-168">CommonParameters</span></span>
<span data-ttu-id="42b1a-169">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42b1a-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42b1a-170">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="42b1a-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42b1a-171">INPUT</span><span class="sxs-lookup"><span data-stu-id="42b1a-171">INPUTS</span></span>

### <span data-ttu-id="42b1a-172">System.String</span><span class="sxs-lookup"><span data-stu-id="42b1a-172">System.String</span></span>

## <span data-ttu-id="42b1a-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42b1a-173">OUTPUTS</span></span>

### <span data-ttu-id="42b1a-174">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="42b1a-174">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="42b1a-175">NOTE</span><span class="sxs-lookup"><span data-stu-id="42b1a-175">NOTES</span></span>

## <span data-ttu-id="42b1a-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42b1a-176">RELATED LINKS</span></span>
