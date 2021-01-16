---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: 33f1af70b0fef7e89ccb584ed3b69f32e2810690
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368773"
---
# <span data-ttu-id="ff466-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="ff466-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="ff466-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff466-102">SYNOPSIS</span></span>
<span data-ttu-id="ff466-103">Crea i metadati di un'istanza di servizio.</span><span class="sxs-lookup"><span data-stu-id="ff466-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="ff466-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff466-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>] [-ExportStorageAccountName <String>]
 [-EnableSmartProxy] [-ManagedIdentity] [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff466-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff466-105">DESCRIPTION</span></span>
<span data-ttu-id="ff466-106">Crea o aggiorna i metadati di un'istanza di servizio.</span><span class="sxs-lookup"><span data-stu-id="ff466-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="ff466-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff466-107">EXAMPLES</span></span>

### <span data-ttu-id="ff466-108">Esempio 1: crea un nuovo servizio Fhir di Azure healthcareapis denominato servizio nel gruppo di risorse MyResourceGroup in una posizione westus2 con cosmosdb offerta throughput = 400</span><span class="sxs-lookup"><span data-stu-id="ff466-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
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

### <span data-ttu-id="ff466-109">Esempio 2: crea un nuovo servizio Fhir di Azure healthcareapis denominato servizio nel gruppo di risorse MyResourceGroup in una posizione westus2 con cosmosdb offerta throughput = 400 e l'URI della chiave del Vault Key "https:// \<my-keyvault> . Vault.Azure.NET/Keys/ \<my-key> "</span><span class="sxs-lookup"><span data-stu-id="ff466-109">Example 2 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>
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

## <span data-ttu-id="ff466-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff466-110">PARAMETERS</span></span>

### <span data-ttu-id="ff466-111">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="ff466-111">-AccessPolicyObjectId</span></span>
<span data-ttu-id="ff466-112">Elenco di ID oggetto Criteri di accesso.</span><span class="sxs-lookup"><span data-stu-id="ff466-112">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="ff466-113">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="ff466-113">-AllowCorsCredential</span></span>
<span data-ttu-id="ff466-114">HealthcareApis Fhir servizio AllowCorsCredentials.</span><span class="sxs-lookup"><span data-stu-id="ff466-114">HealthcareApis Fhir Service AllowCorsCredentials.</span></span>

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

### <span data-ttu-id="ff466-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff466-115">-AsJob</span></span>
<span data-ttu-id="ff466-116">Esegui cmdlet come processo in background.</span><span class="sxs-lookup"><span data-stu-id="ff466-116">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="ff466-117">-Pubblico</span><span class="sxs-lookup"><span data-stu-id="ff466-117">-Audience</span></span>
<span data-ttu-id="ff466-118">HealthcareApis Fhir servizio pubblico.</span><span class="sxs-lookup"><span data-stu-id="ff466-118">HealthcareApis Fhir Service Audience.</span></span>

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

### <span data-ttu-id="ff466-119">-Authority</span><span class="sxs-lookup"><span data-stu-id="ff466-119">-Authority</span></span>
<span data-ttu-id="ff466-120">HealthcareApis Fhir Service Authority.</span><span class="sxs-lookup"><span data-stu-id="ff466-120">HealthcareApis Fhir Service Authority.</span></span>

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

### <span data-ttu-id="ff466-121">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="ff466-121">-CorsHeader</span></span>
<span data-ttu-id="ff466-122">Elenco dei servizi di HealthcareApis Fhir dell'intestazione di CORS.</span><span class="sxs-lookup"><span data-stu-id="ff466-122">HealthcareApis Fhir Service List of Cors Header.</span></span>
<span data-ttu-id="ff466-123">Specifica le intestazioni HTTP che possono essere usate durante la richiesta.</span><span class="sxs-lookup"><span data-stu-id="ff466-123">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="ff466-124">Usare "\*" per qualsiasi intestazione.</span><span class="sxs-lookup"><span data-stu-id="ff466-124">Use " \* " for any header.</span></span>

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

### <span data-ttu-id="ff466-125">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="ff466-125">-CorsMaxAge</span></span>
<span data-ttu-id="ff466-126">HealthcareApis Fhir Service CORS max age.</span><span class="sxs-lookup"><span data-stu-id="ff466-126">HealthcareApis Fhir Service Cors Max Age.</span></span>
<span data-ttu-id="ff466-127">Specificare per quanto tempo un risultato di una richiesta può essere memorizzato nella cache in pochi secondi.</span><span class="sxs-lookup"><span data-stu-id="ff466-127">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="ff466-128">Esempio: 600 significa 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="ff466-128">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="ff466-129">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="ff466-129">-CorsMethod</span></span>
<span data-ttu-id="ff466-130">HealthcareApis Fhir CORS.</span><span class="sxs-lookup"><span data-stu-id="ff466-130">HealthcareApis Fhir Service List of Cors Method.</span></span>

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

### <span data-ttu-id="ff466-131">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="ff466-131">-CorsOrigin</span></span>
<span data-ttu-id="ff466-132">Elenco dei servizi di HealthcareApis Fhir di origine CORS.</span><span class="sxs-lookup"><span data-stu-id="ff466-132">HealthcareApis Fhir Service List of Cors Origin.</span></span>
<span data-ttu-id="ff466-133">Specifica gli URL dei siti di origine che possono accedere a questa API oppure usa "\*" per consentire l'accesso da qualsiasi sito.</span><span class="sxs-lookup"><span data-stu-id="ff466-133">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

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

### <span data-ttu-id="ff466-134">-CosmosKeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="ff466-134">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="ff466-135">HealthcareApis Fhir servizio CosmosKeyVaultKeyUri.</span><span class="sxs-lookup"><span data-stu-id="ff466-135">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="ff466-136">URI della chiave gestita dal cliente per il database di supporto.</span><span class="sxs-lookup"><span data-stu-id="ff466-136">The URI of the customer-managed key for the backing database.</span></span>

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

### <span data-ttu-id="ff466-137">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="ff466-137">-CosmosOfferThroughput</span></span>
<span data-ttu-id="ff466-138">HealthcareApis Fhir servizio CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="ff466-138">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="ff466-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff466-139">-DefaultProfile</span></span>
<span data-ttu-id="ff466-140">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ff466-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff466-141">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="ff466-141">-EnableSmartProxy</span></span>
<span data-ttu-id="ff466-142">HealthcareApis Fhir servizio EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="ff466-142">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

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

### <span data-ttu-id="ff466-143">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ff466-143">-ExportStorageAccountName</span></span>
<span data-ttu-id="ff466-144">HealthcareApis Fhir servizio Esporta il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ff466-144">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="ff466-145">-FhirVersion</span><span class="sxs-lookup"><span data-stu-id="ff466-145">-FhirVersion</span></span>
<span data-ttu-id="ff466-146">Versione Fhir.</span><span class="sxs-lookup"><span data-stu-id="ff466-146">Fhir Version.</span></span>

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

### <span data-ttu-id="ff466-147">-Tipo</span><span class="sxs-lookup"><span data-stu-id="ff466-147">-Kind</span></span>
<span data-ttu-id="ff466-148">Tipo di servizio HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="ff466-148">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="ff466-149">Il valore predefinito è Fhir</span><span class="sxs-lookup"><span data-stu-id="ff466-149">The default value is Fhir</span></span>

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

### <span data-ttu-id="ff466-150">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ff466-150">-Location</span></span>
<span data-ttu-id="ff466-151">Posizione del servizio HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="ff466-151">HealthcareApis Service Location.</span></span>

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

### <span data-ttu-id="ff466-152">-ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="ff466-152">-ManagedIdentity</span></span>
<span data-ttu-id="ff466-153">Usare l'identità gestita?</span><span class="sxs-lookup"><span data-stu-id="ff466-153">Use Managed Identity?</span></span>

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

### <span data-ttu-id="ff466-154">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff466-154">-Name</span></span>
<span data-ttu-id="ff466-155">Nome servizio HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="ff466-155">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="ff466-156">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="ff466-156">-PublicNetworkAccess</span></span>
<span data-ttu-id="ff466-157">Tipo di accesso alla rete per il servizio Fhir.</span><span class="sxs-lookup"><span data-stu-id="ff466-157">The network access type for Fhir service.</span></span> <span data-ttu-id="ff466-158">Comunemente `Enabled` o `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="ff466-158">Commonly `Enabled` or `Disabled`.</span></span>

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

### <span data-ttu-id="ff466-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff466-159">-ResourceGroupName</span></span>
<span data-ttu-id="ff466-160">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ff466-160">Resource Group Name.</span></span>

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

### <span data-ttu-id="ff466-161">-Tag</span><span class="sxs-lookup"><span data-stu-id="ff466-161">-Tag</span></span>
<span data-ttu-id="ff466-162">Tag dell'account del servizio Fhir HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="ff466-162">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="ff466-163">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ff466-163">-Confirm</span></span>
<span data-ttu-id="ff466-164">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff466-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff466-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff466-165">-WhatIf</span></span>
<span data-ttu-id="ff466-166">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff466-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff466-167">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff466-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff466-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff466-168">CommonParameters</span></span>
<span data-ttu-id="ff466-169">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff466-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff466-170">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff466-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff466-171">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff466-171">INPUTS</span></span>

### <span data-ttu-id="ff466-172">System. String</span><span class="sxs-lookup"><span data-stu-id="ff466-172">System.String</span></span>

## <span data-ttu-id="ff466-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff466-173">OUTPUTS</span></span>

### <span data-ttu-id="ff466-174">Microsoft. Azure. Commands. HealthcareApis. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="ff466-174">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="ff466-175">Note</span><span class="sxs-lookup"><span data-stu-id="ff466-175">NOTES</span></span>

## <span data-ttu-id="ff466-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff466-176">RELATED LINKS</span></span>
