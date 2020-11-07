---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: f4bc87424707fe3f26da04a4984b2ae122d98a3b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864324"
---
# <span data-ttu-id="a4f77-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="a4f77-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="a4f77-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4f77-102">SYNOPSIS</span></span>
<span data-ttu-id="a4f77-103">Crea i metadati di un'istanza di servizio.</span><span class="sxs-lookup"><span data-stu-id="a4f77-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="a4f77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4f77-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-EnableSmartProxy] [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4f77-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4f77-105">DESCRIPTION</span></span>
<span data-ttu-id="a4f77-106">Crea o aggiorna i metadati di un'istanza di servizio.</span><span class="sxs-lookup"><span data-stu-id="a4f77-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="a4f77-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4f77-107">EXAMPLES</span></span>

### <span data-ttu-id="a4f77-108">Esempio 1: crea un nuovo servizio Fhir di Azure healthcareapis denominato servizio nel gruppo di risorse MyResourceGroup in una posizione westus2 con cosmosdb offerta throughput = 400</span><span class="sxs-lookup"><span data-stu-id="a4f77-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput  400

ResourceGroupName Name Location        Kind   CosmosOfferThroughput
----------------- ----------- -------------------------------
MyResourceGroup   MyService   westus2    fhir-R4   400

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
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

## <span data-ttu-id="a4f77-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4f77-109">PARAMETERS</span></span>

### <span data-ttu-id="a4f77-110">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="a4f77-110">-AccessPolicyObjectId</span></span>
<span data-ttu-id="a4f77-111">Elenco di ID oggetto Criteri di accesso.</span><span class="sxs-lookup"><span data-stu-id="a4f77-111">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="a4f77-112">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="a4f77-112">-AllowCorsCredential</span></span>
<span data-ttu-id="a4f77-113">HealthcareApis Fhir servizio AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="a4f77-113">HealthcareApis Fhir Service AllowCorsCredential.</span></span>

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

### <span data-ttu-id="a4f77-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4f77-114">-AsJob</span></span>
<span data-ttu-id="a4f77-115">Esegui cmdlet come processo in background.</span><span class="sxs-lookup"><span data-stu-id="a4f77-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="a4f77-116">-Pubblico</span><span class="sxs-lookup"><span data-stu-id="a4f77-116">-Audience</span></span>
<span data-ttu-id="a4f77-117">HealthcareApis Fhir servizio pubblico.</span><span class="sxs-lookup"><span data-stu-id="a4f77-117">HealthcareApis Fhir Service Audience.</span></span>

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

### <span data-ttu-id="a4f77-118">-Authority</span><span class="sxs-lookup"><span data-stu-id="a4f77-118">-Authority</span></span>
<span data-ttu-id="a4f77-119">HealthcareApis Fhir Service Authority.</span><span class="sxs-lookup"><span data-stu-id="a4f77-119">HealthcareApis Fhir Service Authority.</span></span>

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

### <span data-ttu-id="a4f77-120">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="a4f77-120">-CorsHeader</span></span>
<span data-ttu-id="a4f77-121">Elenco dei servizi di HealthcareApis Fhir dell'intestazione di CORS.</span><span class="sxs-lookup"><span data-stu-id="a4f77-121">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="a4f77-122">Specifica le intestazioni HTTP che possono essere usate durante la richiesta.</span><span class="sxs-lookup"><span data-stu-id="a4f77-122">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="a4f77-123">Usare \* per qualsiasi intestazione.</span><span class="sxs-lookup"><span data-stu-id="a4f77-123">Use \* for any header.</span></span>

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

### <span data-ttu-id="a4f77-124">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="a4f77-124">-CorsMaxAge</span></span>
<span data-ttu-id="a4f77-125">HealthcareApis Fhir Service CORS max age.</span><span class="sxs-lookup"><span data-stu-id="a4f77-125">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="a4f77-126">Specificare per quanto tempo un risultato di una richiesta può essere memorizzato nella cache in pochi secondi.</span><span class="sxs-lookup"><span data-stu-id="a4f77-126">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="a4f77-127">Esempio: 600 significa 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="a4f77-127">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="a4f77-128">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="a4f77-128">-CorsMethod</span></span>
<span data-ttu-id="a4f77-129">HealthcareApis Fhir CORS.</span><span class="sxs-lookup"><span data-stu-id="a4f77-129">HealthcareApis Fhir Service List of Cors Method.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: DELETE, GET, OPTIONS, PATCH, POST, PUT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f77-130">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="a4f77-130">-CorsOrigin</span></span>
<span data-ttu-id="a4f77-131">Elenco dei servizi di HealthcareApis Fhir di origine CORS.</span><span class="sxs-lookup"><span data-stu-id="a4f77-131">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="a4f77-132">Specifica gli URL dei siti di origine che possono accedere a questa API o usa \* per consentire l'accesso da qualsiasi sito.</span><span class="sxs-lookup"><span data-stu-id="a4f77-132">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

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

### <span data-ttu-id="a4f77-133">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="a4f77-133">-CosmosOfferThroughput</span></span>
<span data-ttu-id="a4f77-134">HealthcareApis Fhir servizio CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="a4f77-134">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="a4f77-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4f77-135">-DefaultProfile</span></span>
<span data-ttu-id="a4f77-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4f77-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4f77-137">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="a4f77-137">-EnableSmartProxy</span></span>
<span data-ttu-id="a4f77-138">HealthcareApis Fhir servizio EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="a4f77-138">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

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

### <span data-ttu-id="a4f77-139">-FhirVersion</span><span class="sxs-lookup"><span data-stu-id="a4f77-139">-FhirVersion</span></span>
<span data-ttu-id="a4f77-140">Versione Fhir.</span><span class="sxs-lookup"><span data-stu-id="a4f77-140">Fhir Version.</span></span>

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

### <span data-ttu-id="a4f77-141">-Tipo</span><span class="sxs-lookup"><span data-stu-id="a4f77-141">-Kind</span></span>
<span data-ttu-id="a4f77-142">Tipo di servizio HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="a4f77-142">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="a4f77-143">Il valore predefinito è Fhir</span><span class="sxs-lookup"><span data-stu-id="a4f77-143">The default value is Fhir</span></span>

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

### <span data-ttu-id="a4f77-144">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a4f77-144">-Location</span></span>
<span data-ttu-id="a4f77-145">Posizione del servizio HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="a4f77-145">HealthcareApis Service Location.</span></span>

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

### <span data-ttu-id="a4f77-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4f77-146">-Name</span></span>
<span data-ttu-id="a4f77-147">Nome servizio HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="a4f77-147">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="a4f77-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4f77-148">-ResourceGroupName</span></span>
<span data-ttu-id="a4f77-149">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a4f77-149">Resource Group Name.</span></span>

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

### <span data-ttu-id="a4f77-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="a4f77-150">-Tag</span></span>
<span data-ttu-id="a4f77-151">Tag dell'account del servizio Fhir HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="a4f77-151">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="a4f77-152">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a4f77-152">-Confirm</span></span>
<span data-ttu-id="a4f77-153">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4f77-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4f77-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4f77-154">-WhatIf</span></span>
<span data-ttu-id="a4f77-155">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4f77-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4f77-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4f77-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4f77-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4f77-157">CommonParameters</span></span>
<span data-ttu-id="a4f77-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4f77-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4f77-159">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4f77-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4f77-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4f77-160">INPUTS</span></span>

### <span data-ttu-id="a4f77-161">System. String</span><span class="sxs-lookup"><span data-stu-id="a4f77-161">System.String</span></span>

## <span data-ttu-id="a4f77-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4f77-162">OUTPUTS</span></span>

### <span data-ttu-id="a4f77-163">Microsoft. Azure. Commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="a4f77-163">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="a4f77-164">Note</span><span class="sxs-lookup"><span data-stu-id="a4f77-164">NOTES</span></span>

## <span data-ttu-id="a4f77-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4f77-165">RELATED LINKS</span></span>
