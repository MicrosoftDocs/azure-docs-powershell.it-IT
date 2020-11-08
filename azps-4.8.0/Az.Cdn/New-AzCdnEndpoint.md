---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: ba06dcabe874161c9f801841a5be8b0337614799
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031929"
---
# <span data-ttu-id="a3d03-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3d03-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="a3d03-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a3d03-102">SYNOPSIS</span></span>
<span data-ttu-id="a3d03-103">Crea un endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="a3d03-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="a3d03-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3d03-104">SYNTAX</span></span>

### <span data-ttu-id="a3d03-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a3d03-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> -Location <String>
 [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3d03-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3d03-106">ByObjectParameterSet</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3d03-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3d03-107">DESCRIPTION</span></span>
<span data-ttu-id="a3d03-108">Il cmdlet **New-AzCdnEndpoint** crea un endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="a3d03-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="a3d03-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3d03-109">EXAMPLES</span></span>

## <span data-ttu-id="a3d03-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a3d03-110">PARAMETERS</span></span>

### <span data-ttu-id="a3d03-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="a3d03-111">-CdnProfile</span></span>
<span data-ttu-id="a3d03-112">Specifica l'oggetto del profilo CDN a cui viene aggiunto l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="a3d03-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

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

### <span data-ttu-id="a3d03-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="a3d03-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="a3d03-114">Specifica una matrice di tipi di contenuto da comprimere dal nodo Edge al client.</span><span class="sxs-lookup"><span data-stu-id="a3d03-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="a3d03-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3d03-115">-DefaultProfile</span></span>
<span data-ttu-id="a3d03-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a3d03-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3d03-117">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="a3d03-117">-DeliveryPolicy</span></span>
<span data-ttu-id="a3d03-118">Criteri di recapito per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="a3d03-118">The delivery policy for this endpoint.</span></span>

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

### <span data-ttu-id="a3d03-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a3d03-119">-EndpointName</span></span>
<span data-ttu-id="a3d03-120">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="a3d03-120">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="a3d03-121">-Filtri geofiltrati</span><span class="sxs-lookup"><span data-stu-id="a3d03-121">-GeoFilters</span></span>
<span data-ttu-id="a3d03-122">Elenco dei filtri Geo che si applicano a questo endpoint.</span><span class="sxs-lookup"><span data-stu-id="a3d03-122">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="a3d03-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="a3d03-123">-HttpPort</span></span>
<span data-ttu-id="a3d03-124">Specifica il numero di porta HTTP nel server di origine.</span><span class="sxs-lookup"><span data-stu-id="a3d03-124">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="a3d03-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="a3d03-125">-HttpsPort</span></span>
<span data-ttu-id="a3d03-126">Specifica il numero di porta HTTPS nel server di origine.</span><span class="sxs-lookup"><span data-stu-id="a3d03-126">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="a3d03-127">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="a3d03-127">-IsCompressionEnabled</span></span>
<span data-ttu-id="a3d03-128">Indica se la compressione è abilitata per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="a3d03-128">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="a3d03-129">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="a3d03-129">-IsHttpAllowed</span></span>
<span data-ttu-id="a3d03-130">Indica se l'endpoint Abilita il traffico HTTP.</span><span class="sxs-lookup"><span data-stu-id="a3d03-130">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="a3d03-131">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="a3d03-131">-IsHttpsAllowed</span></span>
<span data-ttu-id="a3d03-132">Indica se l'endpoint Abilita il traffico HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a3d03-132">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="a3d03-133">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a3d03-133">-Location</span></span>
<span data-ttu-id="a3d03-134">Specifica la posizione della risorsa dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="a3d03-134">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="a3d03-135">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="a3d03-135">-OptimizationType</span></span>
<span data-ttu-id="a3d03-136">Specifica qualsiasi ottimizzazione di questo endpoint.</span><span class="sxs-lookup"><span data-stu-id="a3d03-136">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="a3d03-137">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="a3d03-137">-OriginHostHeader</span></span>
<span data-ttu-id="a3d03-138">Specifica la testa dell'host di origine dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="a3d03-138">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="a3d03-139">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="a3d03-139">-OriginHostName</span></span>
<span data-ttu-id="a3d03-140">Specifica il nome host del server di origine.</span><span class="sxs-lookup"><span data-stu-id="a3d03-140">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="a3d03-141">-Originname</span><span class="sxs-lookup"><span data-stu-id="a3d03-141">-OriginName</span></span>
<span data-ttu-id="a3d03-142">Specifica il nome della risorsa del server di origine.</span><span class="sxs-lookup"><span data-stu-id="a3d03-142">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="a3d03-143">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="a3d03-143">-OriginPath</span></span>
<span data-ttu-id="a3d03-144">Specifica il percorso del server di origine.</span><span class="sxs-lookup"><span data-stu-id="a3d03-144">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="a3d03-145">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="a3d03-145">-ProbePath</span></span>
<span data-ttu-id="a3d03-146">Specifica il percorso della sonda per l'accelerazione dinamica del sito</span><span class="sxs-lookup"><span data-stu-id="a3d03-146">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="a3d03-147">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a3d03-147">-ProfileName</span></span>
<span data-ttu-id="a3d03-148">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="a3d03-148">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="a3d03-149">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="a3d03-149">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="a3d03-150">Specifica il comportamento dell'endpoint CDN quando una stringa di query si trova nell'URL della richiesta.</span><span class="sxs-lookup"><span data-stu-id="a3d03-150">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="a3d03-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3d03-151">-ResourceGroupName</span></span>
<span data-ttu-id="a3d03-152">Specifica il nome del gruppo di risorse a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="a3d03-152">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="a3d03-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="a3d03-153">-Tag</span></span>
<span data-ttu-id="a3d03-154">Tag da associare all'endpoint di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="a3d03-154">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="a3d03-155">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a3d03-155">-Confirm</span></span>
<span data-ttu-id="a3d03-156">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3d03-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3d03-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3d03-157">-WhatIf</span></span>
<span data-ttu-id="a3d03-158">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3d03-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3d03-159">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3d03-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3d03-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3d03-160">CommonParameters</span></span>
<span data-ttu-id="a3d03-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3d03-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3d03-162">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3d03-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3d03-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a3d03-163">INPUTS</span></span>

### <span data-ttu-id="a3d03-164">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="a3d03-164">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="a3d03-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3d03-165">OUTPUTS</span></span>

### <span data-ttu-id="a3d03-166">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3d03-166">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="a3d03-167">Note</span><span class="sxs-lookup"><span data-stu-id="a3d03-167">NOTES</span></span>

## <span data-ttu-id="a3d03-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3d03-168">RELATED LINKS</span></span>

[<span data-ttu-id="a3d03-169">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3d03-169">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="a3d03-170">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3d03-170">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="a3d03-171">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3d03-171">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="a3d03-172">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3d03-172">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="a3d03-173">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a3d03-173">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


