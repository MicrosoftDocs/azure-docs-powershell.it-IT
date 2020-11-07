---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: 36632398d95acdd16d2a7b41c09bed7172391639
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674268"
---
# <span data-ttu-id="387d7-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="387d7-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="387d7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="387d7-102">SYNOPSIS</span></span>
<span data-ttu-id="387d7-103">Aggiorna un servizio Fhir healthcareApis esistente.</span><span class="sxs-lookup"><span data-stu-id="387d7-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="387d7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="387d7-104">SYNTAX</span></span>

### <span data-ttu-id="387d7-105">ServiceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="387d7-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-AccessPolicyObjectId <String[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="387d7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="387d7-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-Authority <String>] [-Audience <String>]
 [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>]
 [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential]
 [-AccessPolicyObjectId <String[]>] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="387d7-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="387d7-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="387d7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="387d7-108">DESCRIPTION</span></span>
<span data-ttu-id="387d7-109">Aggiorna un servizio Fhir healthcareApis esistente.</span><span class="sxs-lookup"><span data-stu-id="387d7-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="387d7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="387d7-110">EXAMPLES</span></span>

### <span data-ttu-id="387d7-111">Esempio 1: aggiorna il servizio healthcareapis esistente denominato servizio nel gruppo di risorse MyResourceGroup con il cosmosdb OfferThroughput = 500.</span><span class="sxs-lookup"><span data-stu-id="387d7-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

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

### <span data-ttu-id="387d7-112">Esempio 2: aggiorna il servizio healthcareapis esistente denominato servizio nel gruppo di risorse MyResourceGroup con il cosmosdb OfferThroughput = 500.</span><span class="sxs-lookup"><span data-stu-id="387d7-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService"
PS C:\> Set-AzHealthcareApisService -ResourceId $ResourceId  -CosmosOfferThroughput 500

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
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

## <span data-ttu-id="387d7-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="387d7-113">PARAMETERS</span></span>

### <span data-ttu-id="387d7-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="387d7-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="387d7-115">Elenco di ID oggetto Criteri di accesso.</span><span class="sxs-lookup"><span data-stu-id="387d7-115">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="387d7-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="387d7-116">-AllowCorsCredential</span></span>
<span data-ttu-id="387d7-117">HealthcareApis FhirService AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="387d7-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

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

### <span data-ttu-id="387d7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="387d7-118">-AsJob</span></span>
<span data-ttu-id="387d7-119">Esegui cmdlet come processo in background.</span><span class="sxs-lookup"><span data-stu-id="387d7-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="387d7-120">-Pubblico</span><span class="sxs-lookup"><span data-stu-id="387d7-120">-Audience</span></span>
<span data-ttu-id="387d7-121">HealthcareApis FhirService audience.</span><span class="sxs-lookup"><span data-stu-id="387d7-121">HealthcareApis FhirService Audience.</span></span>

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

### <span data-ttu-id="387d7-122">-Authority</span><span class="sxs-lookup"><span data-stu-id="387d7-122">-Authority</span></span>
<span data-ttu-id="387d7-123">HealthcareApis FhirService Authority.</span><span class="sxs-lookup"><span data-stu-id="387d7-123">HealthcareApis FhirService Authority.</span></span>

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

### <span data-ttu-id="387d7-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="387d7-124">-CorsHeader</span></span>
<span data-ttu-id="387d7-125">Elenco dei servizi di HealthcareApis Fhir dell'intestazione di CORS.</span><span class="sxs-lookup"><span data-stu-id="387d7-125">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="387d7-126">Specifica le intestazioni HTTP che possono essere usate durante la richiesta.</span><span class="sxs-lookup"><span data-stu-id="387d7-126">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="387d7-127">Usare \* per qualsiasi intestazione.</span><span class="sxs-lookup"><span data-stu-id="387d7-127">Use \* for any header.</span></span>

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

### <span data-ttu-id="387d7-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="387d7-128">-CorsMaxAge</span></span>
<span data-ttu-id="387d7-129">HealthcareApis Fhir Service CORS max age.</span><span class="sxs-lookup"><span data-stu-id="387d7-129">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="387d7-130">Specificare per quanto tempo un risultato di una richiesta può essere memorizzato nella cache in pochi secondi.</span><span class="sxs-lookup"><span data-stu-id="387d7-130">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="387d7-131">Esempio: 600 significa 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="387d7-131">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="387d7-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="387d7-132">-CorsMethod</span></span>
<span data-ttu-id="387d7-133">HealthcareApis FhirService elenco dei metodi CORS.</span><span class="sxs-lookup"><span data-stu-id="387d7-133">HealthcareApis FhirService List of Cors Methods.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:
Accepted values: DELETE, GET, OPTIONS, PATCH, POST, PUT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387d7-134">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="387d7-134">-CorsOrigin</span></span>
<span data-ttu-id="387d7-135">HealthcareApis FhirService elenco delle origini di CORS.</span><span class="sxs-lookup"><span data-stu-id="387d7-135">HealthcareApis FhirService List of Cors Origins.</span></span> <span data-ttu-id="387d7-136">Elenco dei servizi di HealthcareApis Fhir di origine CORS.</span><span class="sxs-lookup"><span data-stu-id="387d7-136">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="387d7-137">Specifica gli URL dei siti di origine che possono accedere a questa API o usa \* per consentire l'accesso da qualsiasi sito.</span><span class="sxs-lookup"><span data-stu-id="387d7-137">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

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

### <span data-ttu-id="387d7-138">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="387d7-138">-CosmosOfferThroughput</span></span>
<span data-ttu-id="387d7-139">HealthcareApis FhirService CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="387d7-139">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="387d7-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="387d7-140">-DefaultProfile</span></span>
<span data-ttu-id="387d7-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="387d7-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="387d7-142">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="387d7-142">-DisableCorsCredential</span></span>
<span data-ttu-id="387d7-143">HealthcareApis FhirService CorsCredentials non consentito.</span><span class="sxs-lookup"><span data-stu-id="387d7-143">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

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

### <span data-ttu-id="387d7-144">-DisableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="387d7-144">-DisableSmartProxy</span></span>
<span data-ttu-id="387d7-145">HealthcareApis FhirService DisableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="387d7-145">HealthcareApis FhirService DisableSmartProxy.</span></span>

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

### <span data-ttu-id="387d7-146">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="387d7-146">-EnableSmartProxy</span></span>
<span data-ttu-id="387d7-147">HealthcareApis FhirService EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="387d7-147">HealthcareApis FhirService EnableSmartProxy.</span></span>

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

### <span data-ttu-id="387d7-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="387d7-148">-InputObject</span></span>
<span data-ttu-id="387d7-149">HealthcareApis Fhir servizio inviato tramite pipe da Get-AzHealthcareApisFhirService.</span><span class="sxs-lookup"><span data-stu-id="387d7-149">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

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

### <span data-ttu-id="387d7-150">-Nome</span><span class="sxs-lookup"><span data-stu-id="387d7-150">-Name</span></span>
<span data-ttu-id="387d7-151">Nome servizio HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="387d7-151">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="387d7-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="387d7-152">-ResourceGroupName</span></span>
<span data-ttu-id="387d7-153">Nome del gruppo di risorse del servizio HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="387d7-153">HealthcareApis Service Resource Group Name.</span></span>

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

### <span data-ttu-id="387d7-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="387d7-154">-ResourceId</span></span>
<span data-ttu-id="387d7-155">HealthcareApis Fhir servizio ResourceId.</span><span class="sxs-lookup"><span data-stu-id="387d7-155">HealthcareApis Fhir Service ResourceId.</span></span>

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

### <span data-ttu-id="387d7-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="387d7-156">-Tag</span></span>
<span data-ttu-id="387d7-157">Tag dell'account del servizio Fhir HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="387d7-157">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="387d7-158">-Confermare</span><span class="sxs-lookup"><span data-stu-id="387d7-158">-Confirm</span></span>
<span data-ttu-id="387d7-159">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="387d7-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="387d7-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="387d7-160">-WhatIf</span></span>
<span data-ttu-id="387d7-161">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="387d7-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="387d7-162">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="387d7-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="387d7-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="387d7-163">CommonParameters</span></span>
<span data-ttu-id="387d7-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="387d7-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="387d7-165">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="387d7-165">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="387d7-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="387d7-166">INPUTS</span></span>

### <span data-ttu-id="387d7-167">System. String</span><span class="sxs-lookup"><span data-stu-id="387d7-167">System.String</span></span>

### <span data-ttu-id="387d7-168">Microsoft. Azure. Commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="387d7-168">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="387d7-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="387d7-169">OUTPUTS</span></span>

### <span data-ttu-id="387d7-170">Microsoft. Azure. Commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="387d7-170">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="387d7-171">Note</span><span class="sxs-lookup"><span data-stu-id="387d7-171">NOTES</span></span>

## <span data-ttu-id="387d7-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="387d7-172">RELATED LINKS</span></span>
