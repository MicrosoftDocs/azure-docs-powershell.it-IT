---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: c8eb7c58300e3252422d8b599422a3a14eb5c1fe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192478"
---
# <span data-ttu-id="cd195-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="cd195-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="cd195-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd195-102">SYNOPSIS</span></span>
<span data-ttu-id="cd195-103">Aggiorna un servizio healthcareApis fhir esistente.</span><span class="sxs-lookup"><span data-stu-id="cd195-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="cd195-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd195-104">SYNTAX</span></span>

### <span data-ttu-id="cd195-105">ServiceNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cd195-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-CosmosKeyVaultKeyUri <String>] [-Authority <String>] [-Audience <String>] [-EnableSmartProxy]
 [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>] [-CorsMethod <String[]>]
 [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential] [-ExportStorageAccountName <String>]
 [-AccessPolicyObjectId <String[]>] [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>]
 [-AsJob] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd195-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd195-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-ExportStorageAccountName <String>] [-AccessPolicyObjectId <String[]>]
 [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd195-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd195-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd195-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cd195-108">DESCRIPTION</span></span>
<span data-ttu-id="cd195-109">Aggiorna un servizio healthcareApis fhir esistente.</span><span class="sxs-lookup"><span data-stu-id="cd195-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="cd195-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd195-110">EXAMPLES</span></span>

### <span data-ttu-id="cd195-111">Esempio 1: aggiorna il servizio healthcareapis esistente denominato MyService nel gruppo di risorse MyResourceGroup con il database database OfferThroughput = 500.</span><span class="sxs-lookup"><span data-stu-id="cd195-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

```powershell
PS C:\> Set-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -CosmosOfferThroughput 500

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosKeyVaultKeyUri    : 
CosmosDbOfferThroughput : 500
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

### <span data-ttu-id="cd195-112">Esempio 2: aggiorna il servizio healthcareapis esistente denominato MyService nel gruppo di risorse MyResourceGroup con il database database OfferThroughput = 500 e l'URI chiave vault chiave "https:// \<my-keyvault> .vault.azure.net/keys/ \<my-key> "</span><span class="sxs-lookup"><span data-stu-id="cd195-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>

```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService"
PS C:\> Set-AzHealthcareApisService -ResourceId $ResourceId  -CosmosOfferThroughput 500 -CosmosKeyVaultKeyUri "https://<my-keyvault>.vault.azure.net/keys/<my-key>"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosKeyVaultKeyUri    : https://<my-keyvault>.vault.azure.net/keys/<my-key>
CosmosDbOfferThroughput : 500
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

## <span data-ttu-id="cd195-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd195-113">PARAMETERS</span></span>

### <span data-ttu-id="cd195-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="cd195-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="cd195-115">Elenco di ID oggetto dei criteri di accesso.</span><span class="sxs-lookup"><span data-stu-id="cd195-115">List of Access Policy Object IDs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd195-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="cd195-116">-AllowCorsCredential</span></span>
<span data-ttu-id="cd195-117">HealthcareApis FhirService AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="cd195-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd195-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd195-118">-AsJob</span></span>
<span data-ttu-id="cd195-119">Eseguire il cmdlet come processo in background.</span><span class="sxs-lookup"><span data-stu-id="cd195-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="cd195-120">-Gruppo di destinatari</span><span class="sxs-lookup"><span data-stu-id="cd195-120">-Audience</span></span>
<span data-ttu-id="cd195-121">Audience HealthcareApis FhirService.</span><span class="sxs-lookup"><span data-stu-id="cd195-121">HealthcareApis FhirService Audience.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd195-122">-Authority</span><span class="sxs-lookup"><span data-stu-id="cd195-122">-Authority</span></span>
<span data-ttu-id="cd195-123">HealthcareApis FhirService Authority.</span><span class="sxs-lookup"><span data-stu-id="cd195-123">HealthcareApis FhirService Authority.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd195-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="cd195-124">-CorsHeader</span></span>
<span data-ttu-id="cd195-125">HealthcareApis FhirService List of Cors Headers.</span><span class="sxs-lookup"><span data-stu-id="cd195-125">HealthcareApis FhirService List of Cors Headers.</span></span>
<span data-ttu-id="cd195-126">Specificare le intestazioni HTTP che possono essere usate durante la richiesta.</span><span class="sxs-lookup"><span data-stu-id="cd195-126">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="cd195-127">Usare " \* " per qualsiasi intestazione.</span><span class="sxs-lookup"><span data-stu-id="cd195-127">Use " \* " for any header.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd195-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="cd195-128">-CorsMaxAge</span></span>
<span data-ttu-id="cd195-129">HealthcareApis FhirService Cors Max Age.</span><span class="sxs-lookup"><span data-stu-id="cd195-129">HealthcareApis FhirService Cors Max Age.</span></span>
<span data-ttu-id="cd195-130">Specificare per quanto tempo un risultato di una richiesta può essere memorizzato nella cache in secondi.</span><span class="sxs-lookup"><span data-stu-id="cd195-130">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="cd195-131">Ad esempio: 600 significa 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="cd195-131">Example: 600 means 10 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd195-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="cd195-132">-CorsMethod</span></span>
<span data-ttu-id="cd195-133">Elenco dei metodi Cors di HealthcareApis FhirService.</span><span class="sxs-lookup"><span data-stu-id="cd195-133">HealthcareApis FhirService List of Cors Methods.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd195-134">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="cd195-134">-CorsOrigin</span></span>
<span data-ttu-id="cd195-135">HealthcareApis FhirService List of Cors Origins.</span><span class="sxs-lookup"><span data-stu-id="cd195-135">HealthcareApis FhirService List of Cors Origins.</span></span>
<span data-ttu-id="cd195-136">Specificare gli URL dei siti di origine che possono accedere a questa API oppure usare " \* " per consentire l'accesso da qualsiasi sito.</span><span class="sxs-lookup"><span data-stu-id="cd195-136">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd195-137">-SottochiaviKeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="cd195-137">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="cd195-138">HealthcareApis Fhir ServiceKeyVaultKeyUri.</span><span class="sxs-lookup"><span data-stu-id="cd195-138">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="cd195-139">URI della chiave gestita dal cliente per il database di supporto.</span><span class="sxs-lookup"><span data-stu-id="cd195-139">The URI of the customer-managed key for the backing database.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd195-140">-MasOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="cd195-140">-CosmosOfferThroughput</span></span>
<span data-ttu-id="cd195-141">HealthcareApis FhirServiceFerenzasOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="cd195-141">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd195-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd195-142">-DefaultProfile</span></span>
<span data-ttu-id="cd195-143">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd195-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd195-144">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="cd195-144">-DisableCorsCredential</span></span>
<span data-ttu-id="cd195-145">HealthcareApis FhirService CorsCredentials Not Allowed.</span><span class="sxs-lookup"><span data-stu-id="cd195-145">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd195-146">-DisableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="cd195-146">-DisableManagedIdentity</span></span>
<span data-ttu-id="cd195-147">Disabilitare l'identità gestita.</span><span class="sxs-lookup"><span data-stu-id="cd195-147">Disable Managed Identity.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd195-148">-DisableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="cd195-148">-DisableSmartProxy</span></span>
<span data-ttu-id="cd195-149">HealthcareApis FhirService DisableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="cd195-149">HealthcareApis FhirService DisableSmartProxy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd195-150">-EnableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="cd195-150">-EnableManagedIdentity</span></span>
<span data-ttu-id="cd195-151">Abilitare l'identità gestita.</span><span class="sxs-lookup"><span data-stu-id="cd195-151">Enable Managed Identity.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd195-152">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="cd195-152">-EnableSmartProxy</span></span>
<span data-ttu-id="cd195-153">HealthcareApis FhirService EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="cd195-153">HealthcareApis FhirService EnableSmartProxy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd195-154">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cd195-154">-ExportStorageAccountName</span></span>
<span data-ttu-id="cd195-155">Nome dell'account di archiviazione di esportazione del servizio HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="cd195-155">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd195-156">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd195-156">-InputObject</span></span>
<span data-ttu-id="cd195-157">Il servizio HealthcareApis fhir è stato reindirizzato da Get-AzHealthcareApisFhirService.</span><span class="sxs-lookup"><span data-stu-id="cd195-157">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd195-158">-Name</span><span class="sxs-lookup"><span data-stu-id="cd195-158">-Name</span></span>
<span data-ttu-id="cd195-159">Nome del servizio HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="cd195-159">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd195-160">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="cd195-160">-PublicNetworkAccess</span></span>
<span data-ttu-id="cd195-161">Tipo di accesso di rete per il servizio Fhir.</span><span class="sxs-lookup"><span data-stu-id="cd195-161">The network access type for Fhir service.</span></span> <span data-ttu-id="cd195-162">Comunemente `Enabled` o `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="cd195-162">Commonly `Enabled` or `Disabled`.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd195-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd195-163">-ResourceGroupName</span></span>
<span data-ttu-id="cd195-164">Nome del gruppo di risorse del servizio HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="cd195-164">HealthcareApis Service Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd195-165">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd195-165">-ResourceId</span></span>
<span data-ttu-id="cd195-166">HealthcareApis Fhir Service ResourceId.</span><span class="sxs-lookup"><span data-stu-id="cd195-166">HealthcareApis Fhir Service ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd195-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="cd195-167">-Tag</span></span>
<span data-ttu-id="cd195-168">Tag dell'account di servizio di HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="cd195-168">HealthcareApis Fhir Service Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd195-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd195-169">-Confirm</span></span>
<span data-ttu-id="cd195-170">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd195-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd195-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd195-171">-WhatIf</span></span>
<span data-ttu-id="cd195-172">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd195-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd195-173">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd195-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd195-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd195-174">CommonParameters</span></span>
<span data-ttu-id="cd195-175">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd195-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd195-176">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cd195-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd195-177">INPUT</span><span class="sxs-lookup"><span data-stu-id="cd195-177">INPUTS</span></span>

### <span data-ttu-id="cd195-178">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="cd195-178">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

### <span data-ttu-id="cd195-179">System.String</span><span class="sxs-lookup"><span data-stu-id="cd195-179">System.String</span></span>

## <span data-ttu-id="cd195-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd195-180">OUTPUTS</span></span>

### <span data-ttu-id="cd195-181">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="cd195-181">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="cd195-182">NOTE</span><span class="sxs-lookup"><span data-stu-id="cd195-182">NOTES</span></span>

## <span data-ttu-id="cd195-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd195-183">RELATED LINKS</span></span>
