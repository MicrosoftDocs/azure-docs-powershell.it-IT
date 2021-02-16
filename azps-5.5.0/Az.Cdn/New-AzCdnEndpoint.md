---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: 9e0b8ee74ff89f4a5903df1c73dc7b289b0371c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200823"
---
# <span data-ttu-id="e7169-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7169-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="e7169-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7169-102">SYNOPSIS</span></span>
<span data-ttu-id="e7169-103">Crea un endpoint della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="e7169-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="e7169-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e7169-104">SYNTAX</span></span>

### <span data-ttu-id="e7169-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e7169-105">ByFieldsParameterSet (Default)</span></span>
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

### <span data-ttu-id="e7169-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7169-106">ByObjectParameterSet</span></span>
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

## <span data-ttu-id="e7169-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e7169-107">DESCRIPTION</span></span>
<span data-ttu-id="e7169-108">Il cmdlet **New-AzCdnEndpoint** crea un endpoint della rete per la distribuzione di contenuti (CDN) di Azure.</span><span class="sxs-lookup"><span data-stu-id="e7169-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="e7169-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e7169-109">EXAMPLES</span></span>

## <span data-ttu-id="e7169-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7169-110">PARAMETERS</span></span>

### <span data-ttu-id="e7169-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="e7169-111">-CdnProfile</span></span>
<span data-ttu-id="e7169-112">Specifica l'oggetto profilo CDN a cui viene aggiunto l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="e7169-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

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

### <span data-ttu-id="e7169-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="e7169-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="e7169-114">Specifica una matrice di tipi di contenuto da comprimere dal nodo perimetrale al client.</span><span class="sxs-lookup"><span data-stu-id="e7169-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="e7169-115">-DefaultOriginGroup</span><span class="sxs-lookup"><span data-stu-id="e7169-115">-DefaultOriginGroup</span></span>
<span data-ttu-id="e7169-116">Il gruppo di origini predefinito.</span><span class="sxs-lookup"><span data-stu-id="e7169-116">The default origin group.</span></span>

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

### <span data-ttu-id="e7169-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7169-117">-DefaultProfile</span></span>
<span data-ttu-id="e7169-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="e7169-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7169-119">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="e7169-119">-DeliveryPolicy</span></span>
<span data-ttu-id="e7169-120">Criteri di recapito per questo endpoint.</span><span class="sxs-lookup"><span data-stu-id="e7169-120">The delivery policy for this endpoint.</span></span>

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

### <span data-ttu-id="e7169-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e7169-121">-EndpointName</span></span>
<span data-ttu-id="e7169-122">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="e7169-122">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="e7169-123">-GeoFilters</span><span class="sxs-lookup"><span data-stu-id="e7169-123">-GeoFilters</span></span>
<span data-ttu-id="e7169-124">Elenco di filtri geografici applicabili a questo endpoint.</span><span class="sxs-lookup"><span data-stu-id="e7169-124">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="e7169-125">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="e7169-125">-HttpPort</span></span>
<span data-ttu-id="e7169-126">Specifica il numero di porta HTTP nel server di origine.</span><span class="sxs-lookup"><span data-stu-id="e7169-126">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="e7169-127">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="e7169-127">-HttpsPort</span></span>
<span data-ttu-id="e7169-128">Specifica il numero di porta HTTPS nel server di origine.</span><span class="sxs-lookup"><span data-stu-id="e7169-128">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="e7169-129">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="e7169-129">-IsCompressionEnabled</span></span>
<span data-ttu-id="e7169-130">Indica se la compressione è abilitata per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="e7169-130">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="e7169-131">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="e7169-131">-IsHttpAllowed</span></span>
<span data-ttu-id="e7169-132">Indica se l'endpoint abilita il traffico HTTP.</span><span class="sxs-lookup"><span data-stu-id="e7169-132">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="e7169-133">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="e7169-133">-IsHttpsAllowed</span></span>
<span data-ttu-id="e7169-134">Indica se l'endpoint abilita il traffico HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e7169-134">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="e7169-135">-Location</span><span class="sxs-lookup"><span data-stu-id="e7169-135">-Location</span></span>
<span data-ttu-id="e7169-136">Specifica la posizione della risorsa dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="e7169-136">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="e7169-137">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="e7169-137">-OptimizationType</span></span>
<span data-ttu-id="e7169-138">Specifica qualsiasi ottimizzazione di questo endpoint.</span><span class="sxs-lookup"><span data-stu-id="e7169-138">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="e7169-139">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="e7169-139">-OriginGroupName</span></span>
<span data-ttu-id="e7169-140">Nome del gruppo di origini.</span><span class="sxs-lookup"><span data-stu-id="e7169-140">The name of the origin group.</span></span>

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

### <span data-ttu-id="e7169-141">-OriginGroupProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e7169-141">-OriginGroupProbeIntervalInSeconds</span></span>
<span data-ttu-id="e7169-142">Il numero di secondi tra l'integrità.</span><span class="sxs-lookup"><span data-stu-id="e7169-142">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="e7169-143">-OriginGroupProbePath</span><span class="sxs-lookup"><span data-stu-id="e7169-143">-OriginGroupProbePath</span></span>
<span data-ttu-id="e7169-144">Percorso relativo all'origine usato per determinare l'integrità dell'origine.</span><span class="sxs-lookup"><span data-stu-id="e7169-144">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="e7169-145">-OriginGroupProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="e7169-145">-OriginGroupProbeProtocol</span></span>
<span data-ttu-id="e7169-146">Protocollo da usare per l'integrità.</span><span class="sxs-lookup"><span data-stu-id="e7169-146">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="e7169-147">-OriginGroupProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="e7169-147">-OriginGroupProbeRequestType</span></span>
<span data-ttu-id="e7169-148">Tipo di richiesta di integrità richiesta.</span><span class="sxs-lookup"><span data-stu-id="e7169-148">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="e7169-149">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="e7169-149">-OriginHostHeader</span></span>
<span data-ttu-id="e7169-150">Specifica l'intestazione dell'host di origine dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="e7169-150">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="e7169-151">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="e7169-151">-OriginHostName</span></span>
<span data-ttu-id="e7169-152">Specifica il nome host del server di origine.</span><span class="sxs-lookup"><span data-stu-id="e7169-152">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="e7169-153">-OriginId</span><span class="sxs-lookup"><span data-stu-id="e7169-153">-OriginId</span></span>
<span data-ttu-id="e7169-154">ID del gruppo di origine della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="e7169-154">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="e7169-155">-OriginName</span><span class="sxs-lookup"><span data-stu-id="e7169-155">-OriginName</span></span>
<span data-ttu-id="e7169-156">Specifica il nome della risorsa del server di origine.</span><span class="sxs-lookup"><span data-stu-id="e7169-156">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="e7169-157">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="e7169-157">-OriginPath</span></span>
<span data-ttu-id="e7169-158">Specifica il percorso del server di origine.</span><span class="sxs-lookup"><span data-stu-id="e7169-158">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="e7169-159">-Priority</span><span class="sxs-lookup"><span data-stu-id="e7169-159">-Priority</span></span>
<span data-ttu-id="e7169-160">Priorità origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="e7169-160">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="e7169-161">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="e7169-161">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="e7169-162">Messaggio personalizzato da includere nella richiesta di approvazione per la connessione al collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="e7169-162">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="e7169-163">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="e7169-163">-PrivateLinkLocation</span></span>
<span data-ttu-id="e7169-164">Percorso del collegamento privato di origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="e7169-164">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="e7169-165">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="e7169-165">-PrivateLinkResourceId</span></span>
<span data-ttu-id="e7169-166">ID risorsa collegamento privato origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="e7169-166">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="e7169-167">-Path</span><span class="sxs-lookup"><span data-stu-id="e7169-167">-ProbePath</span></span>
<span data-ttu-id="e7169-168">Specifica il percorso di accelerazione dinamica del sito</span><span class="sxs-lookup"><span data-stu-id="e7169-168">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="e7169-169">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e7169-169">-ProfileName</span></span>
<span data-ttu-id="e7169-170">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="e7169-170">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="e7169-171">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="e7169-171">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="e7169-172">Specifica il comportamento dell'endpoint CDN quando una stringa di query è nell'URL della richiesta.</span><span class="sxs-lookup"><span data-stu-id="e7169-172">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="e7169-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7169-173">-ResourceGroupName</span></span>
<span data-ttu-id="e7169-174">Specifica il nome del gruppo di risorse a cui appartiene questo endpoint.</span><span class="sxs-lookup"><span data-stu-id="e7169-174">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="e7169-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="e7169-175">-Tag</span></span>
<span data-ttu-id="e7169-176">I tag da associare all'endpoint della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="e7169-176">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="e7169-177">-Spessore</span><span class="sxs-lookup"><span data-stu-id="e7169-177">-Weight</span></span>
<span data-ttu-id="e7169-178">Peso origine rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="e7169-178">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="e7169-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7169-179">-Confirm</span></span>
<span data-ttu-id="e7169-180">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7169-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7169-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7169-181">-WhatIf</span></span>
<span data-ttu-id="e7169-182">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e7169-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7169-183">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e7169-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7169-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7169-184">CommonParameters</span></span>
<span data-ttu-id="e7169-185">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7169-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7169-186">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e7169-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7169-187">INPUT</span><span class="sxs-lookup"><span data-stu-id="e7169-187">INPUTS</span></span>

### <span data-ttu-id="e7169-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="e7169-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="e7169-189">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e7169-189">OUTPUTS</span></span>

### <span data-ttu-id="e7169-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7169-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="e7169-191">NOTE</span><span class="sxs-lookup"><span data-stu-id="e7169-191">NOTES</span></span>

## <span data-ttu-id="e7169-192">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e7169-192">RELATED LINKS</span></span>

[<span data-ttu-id="e7169-193">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7169-193">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="e7169-194">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7169-194">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="e7169-195">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7169-195">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="e7169-196">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7169-196">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="e7169-197">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7169-197">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


