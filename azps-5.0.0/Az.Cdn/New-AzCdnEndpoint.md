---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: 9e0b8ee74ff89f4a5903df1c73dc7b289b0371c4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199728"
---
# <span data-ttu-id="48284-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="48284-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="48284-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="48284-102">SYNOPSIS</span></span>
<span data-ttu-id="48284-103">Crea un endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="48284-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="48284-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48284-104">SYNTAX</span></span>

### <span data-ttu-id="48284-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="48284-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> -Location <String>
 [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultOriginGroup <String>] [-Priority <Int32>] [-Weight <Int32>] [-PrivateLinkApprovalMessage <String>]
 [-PrivateLinkLocation <String>] [-PrivateLinkResourceId <String>]
 [-OriginId <System.Collections.Generic.List`1[System.String]>] [-OriginGroupName <String>]
 [-OriginGroupProbeIntervalInSeconds <Int32>] [-OriginGroupProbePath <String>]
 [-OriginGroupProbeProtocol <String>] [-OriginGroupProbeRequestType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48284-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48284-106">ByObjectParameterSet</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultOriginGroup <String>] [-Priority <Int32>] [-Weight <Int32>] [-PrivateLinkApprovalMessage <String>]
 [-PrivateLinkLocation <String>] [-PrivateLinkResourceId <String>]
 [-OriginId <System.Collections.Generic.List`1[System.String]>] [-OriginGroupName <String>]
 [-OriginGroupProbeIntervalInSeconds <Int32>] [-OriginGroupProbePath <String>]
 [-OriginGroupProbeProtocol <String>] [-OriginGroupProbeRequestType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48284-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48284-107">DESCRIPTION</span></span>
<span data-ttu-id="48284-108">Il cmdlet **New-AzCdnEndpoint** crea un endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="48284-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="48284-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48284-109">EXAMPLES</span></span>

## <span data-ttu-id="48284-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="48284-110">PARAMETERS</span></span>

### <span data-ttu-id="48284-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="48284-111">-CdnProfile</span></span>
<span data-ttu-id="48284-112">Specifica l'oggetto del profilo CDN a cui viene aggiunto l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="48284-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48284-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="48284-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="48284-114">Specifica una matrice di tipi di contenuto da comprimere dal nodo Edge al client.</span><span class="sxs-lookup"><span data-stu-id="48284-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="48284-115">-DefaultOriginGroup</span><span class="sxs-lookup"><span data-stu-id="48284-115">-DefaultOriginGroup</span></span>
<span data-ttu-id="48284-116">Gruppo di origine predefinito.</span><span class="sxs-lookup"><span data-stu-id="48284-116">The default origin group.</span></span>

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

### <span data-ttu-id="48284-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48284-117">-DefaultProfile</span></span>
<span data-ttu-id="48284-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="48284-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48284-119">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="48284-119">-DeliveryPolicy</span></span>
<span data-ttu-id="48284-120">Criteri di recapito per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="48284-120">The delivery policy for this endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48284-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="48284-121">-EndpointName</span></span>
<span data-ttu-id="48284-122">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="48284-122">Specifies the name of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48284-123">-Filtri geofiltrati</span><span class="sxs-lookup"><span data-stu-id="48284-123">-GeoFilters</span></span>
<span data-ttu-id="48284-124">Elenco dei filtri Geo che si applicano a questo endpoint.</span><span class="sxs-lookup"><span data-stu-id="48284-124">The list of geo filters that applies to this endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSGeoFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48284-125">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="48284-125">-HttpPort</span></span>
<span data-ttu-id="48284-126">Specifica il numero di porta HTTP nel server di origine.</span><span class="sxs-lookup"><span data-stu-id="48284-126">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="48284-127">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="48284-127">-HttpsPort</span></span>
<span data-ttu-id="48284-128">Specifica il numero di porta HTTPS nel server di origine.</span><span class="sxs-lookup"><span data-stu-id="48284-128">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="48284-129">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="48284-129">-IsCompressionEnabled</span></span>
<span data-ttu-id="48284-130">Indica se la compressione è abilitata per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="48284-130">Indicates whether compression is enabled for the endpoint.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48284-131">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="48284-131">-IsHttpAllowed</span></span>
<span data-ttu-id="48284-132">Indica se l'endpoint Abilita il traffico HTTP.</span><span class="sxs-lookup"><span data-stu-id="48284-132">Indicates whether the endpoint enables HTTP traffic.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48284-133">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="48284-133">-IsHttpsAllowed</span></span>
<span data-ttu-id="48284-134">Indica se l'endpoint Abilita il traffico HTTPS.</span><span class="sxs-lookup"><span data-stu-id="48284-134">Indicates whether the endpoint enables HTTPS traffic.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48284-135">-Posizione</span><span class="sxs-lookup"><span data-stu-id="48284-135">-Location</span></span>
<span data-ttu-id="48284-136">Specifica la posizione della risorsa dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="48284-136">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48284-137">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="48284-137">-OptimizationType</span></span>
<span data-ttu-id="48284-138">Specifica qualsiasi ottimizzazione di questo endpoint.</span><span class="sxs-lookup"><span data-stu-id="48284-138">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="48284-139">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="48284-139">-OriginGroupName</span></span>
<span data-ttu-id="48284-140">Il nome del gruppo di origine.</span><span class="sxs-lookup"><span data-stu-id="48284-140">The name of the origin group.</span></span>

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

### <span data-ttu-id="48284-141">-OriginGroupProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="48284-141">-OriginGroupProbeIntervalInSeconds</span></span>
<span data-ttu-id="48284-142">Numero di secondi tra le sonde di integrità.</span><span class="sxs-lookup"><span data-stu-id="48284-142">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="48284-143">-OriginGroupProbePath</span><span class="sxs-lookup"><span data-stu-id="48284-143">-OriginGroupProbePath</span></span>
<span data-ttu-id="48284-144">Il percorso relativo all'origine che viene usato per determinare lo stato dell'origine.</span><span class="sxs-lookup"><span data-stu-id="48284-144">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="48284-145">-OriginGroupProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="48284-145">-OriginGroupProbeProtocol</span></span>
<span data-ttu-id="48284-146">Protocollo da usare per la sonda integrità.</span><span class="sxs-lookup"><span data-stu-id="48284-146">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="48284-147">-OriginGroupProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="48284-147">-OriginGroupProbeRequestType</span></span>
<span data-ttu-id="48284-148">Tipo di richiesta di probe di integrità effettuata.</span><span class="sxs-lookup"><span data-stu-id="48284-148">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="48284-149">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="48284-149">-OriginHostHeader</span></span>
<span data-ttu-id="48284-150">Specifica la testa dell'host di origine dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="48284-150">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="48284-151">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="48284-151">-OriginHostName</span></span>
<span data-ttu-id="48284-152">Specifica il nome host del server di origine.</span><span class="sxs-lookup"><span data-stu-id="48284-152">Specifies the host name of the origin server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48284-153">-OriginId</span><span class="sxs-lookup"><span data-stu-id="48284-153">-OriginId</span></span>
<span data-ttu-id="48284-154">ID del gruppo di origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="48284-154">Azure CDN origin group ids.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48284-155">-Originname</span><span class="sxs-lookup"><span data-stu-id="48284-155">-OriginName</span></span>
<span data-ttu-id="48284-156">Specifica il nome della risorsa del server di origine.</span><span class="sxs-lookup"><span data-stu-id="48284-156">Specifies the resource name of the origin server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48284-157">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="48284-157">-OriginPath</span></span>
<span data-ttu-id="48284-158">Specifica il percorso del server di origine.</span><span class="sxs-lookup"><span data-stu-id="48284-158">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="48284-159">-Priorità</span><span class="sxs-lookup"><span data-stu-id="48284-159">-Priority</span></span>
<span data-ttu-id="48284-160">Priorità di origine della rete CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="48284-160">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="48284-161">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="48284-161">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="48284-162">Messaggio personalizzato da includere nella richiesta di approvazione per la connessione al collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="48284-162">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="48284-163">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="48284-163">-PrivateLinkLocation</span></span>
<span data-ttu-id="48284-164">Posizione del collegamento privato in Azure CDN Origin.</span><span class="sxs-lookup"><span data-stu-id="48284-164">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="48284-165">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="48284-165">-PrivateLinkResourceId</span></span>
<span data-ttu-id="48284-166">ID risorsa collegamento privato di Azure CDN Origin.</span><span class="sxs-lookup"><span data-stu-id="48284-166">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="48284-167">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="48284-167">-ProbePath</span></span>
<span data-ttu-id="48284-168">Specifica il percorso della sonda per l'accelerazione dinamica del sito</span><span class="sxs-lookup"><span data-stu-id="48284-168">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="48284-169">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="48284-169">-ProfileName</span></span>
<span data-ttu-id="48284-170">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="48284-170">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48284-171">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="48284-171">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="48284-172">Specifica il comportamento dell'endpoint CDN quando una stringa di query si trova nell'URL della richiesta.</span><span class="sxs-lookup"><span data-stu-id="48284-172">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSQueryStringCachingBehavior]
Parameter Sets: (All)
Aliases:
Accepted values: IgnoreQueryString, BypassCaching, UseQueryString, NotSet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48284-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48284-173">-ResourceGroupName</span></span>
<span data-ttu-id="48284-174">Specifica il nome del gruppo di risorse a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="48284-174">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48284-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="48284-175">-Tag</span></span>
<span data-ttu-id="48284-176">Tag da associare all'endpoint di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="48284-176">The tags to associate with the Azure CDN endpoint.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48284-177">-Peso</span><span class="sxs-lookup"><span data-stu-id="48284-177">-Weight</span></span>
<span data-ttu-id="48284-178">Peso origine di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="48284-178">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="48284-179">-Confermare</span><span class="sxs-lookup"><span data-stu-id="48284-179">-Confirm</span></span>
<span data-ttu-id="48284-180">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48284-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48284-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48284-181">-WhatIf</span></span>
<span data-ttu-id="48284-182">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="48284-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48284-183">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="48284-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48284-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48284-184">CommonParameters</span></span>
<span data-ttu-id="48284-185">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48284-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48284-186">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48284-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48284-187">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="48284-187">INPUTS</span></span>

### <span data-ttu-id="48284-188">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="48284-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="48284-189">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48284-189">OUTPUTS</span></span>

### <span data-ttu-id="48284-190">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="48284-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="48284-191">Note</span><span class="sxs-lookup"><span data-stu-id="48284-191">NOTES</span></span>

## <span data-ttu-id="48284-192">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48284-192">RELATED LINKS</span></span>

[<span data-ttu-id="48284-193">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="48284-193">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="48284-194">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="48284-194">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="48284-195">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="48284-195">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="48284-196">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="48284-196">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="48284-197">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="48284-197">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)

