---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 5d2bfdf2bf5f87ccb0213c006de8612b5eaf0730
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519619"
---
# <span data-ttu-id="4c4f6-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4c4f6-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="4c4f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4c4f6-102">SYNOPSIS</span></span>
<span data-ttu-id="4c4f6-103">Crea un endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c4f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c4f6-104">SYNTAX</span></span>

### <span data-ttu-id="4c4f6-105">Parametro set per i parametri dei campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4c4f6-105">Parameter Set for fields parameters (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c4f6-106">Parametro impostato per i parametri degli oggetti</span><span class="sxs-lookup"><span data-stu-id="4c4f6-106">Parameter Set for object parameters</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c4f6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c4f6-107">DESCRIPTION</span></span>
<span data-ttu-id="4c4f6-108">Il cmdlet **New-AzureRmCdnEndpoint** crea un endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="4c4f6-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="4c4f6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c4f6-109">EXAMPLES</span></span>

## <span data-ttu-id="4c4f6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4c4f6-110">PARAMETERS</span></span>

### <span data-ttu-id="4c4f6-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="4c4f6-111">-CdnProfile</span></span>
<span data-ttu-id="4c4f6-112">Specifica l'oggetto del profilo CDN a cui viene aggiunto l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c4f6-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="4c4f6-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="4c4f6-114">Specifica una matrice di tipi di contenuto da comprimere dal nodo Edge al client.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="4c4f6-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4c4f6-115">-EndpointName</span></span>
<span data-ttu-id="4c4f6-116">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="4c4f6-117">-Filtri geofiltrati</span><span class="sxs-lookup"><span data-stu-id="4c4f6-117">-GeoFilters</span></span>
<span data-ttu-id="4c4f6-118">Elenco dei filtri Geo che si applicano a questo endpoint.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-118">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="4c4f6-119">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="4c4f6-119">-HttpPort</span></span>
<span data-ttu-id="4c4f6-120">Specifica il numero di porta HTTP nel server di origine.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-120">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="4c4f6-121">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="4c4f6-121">-HttpsPort</span></span>
<span data-ttu-id="4c4f6-122">Specifica il numero di porta HTTPS nel server di origine.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-122">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="4c4f6-123">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="4c4f6-123">-IsCompressionEnabled</span></span>
<span data-ttu-id="4c4f6-124">Indica se la compressione è abilitata per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-124">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="4c4f6-125">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="4c4f6-125">-IsHttpAllowed</span></span>
<span data-ttu-id="4c4f6-126">Indica se l'endpoint Abilita il traffico HTTP.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-126">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="4c4f6-127">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="4c4f6-127">-IsHttpsAllowed</span></span>
<span data-ttu-id="4c4f6-128">Indica se l'endpoint Abilita il traffico HTTPS.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-128">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="4c4f6-129">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4c4f6-129">-Location</span></span>
<span data-ttu-id="4c4f6-130">Specifica la posizione della risorsa dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-130">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c4f6-131">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="4c4f6-131">-OptimizationType</span></span>
<span data-ttu-id="4c4f6-132">Specifica qualsiasi ottimizzazione di questo endpoint.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-132">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="4c4f6-133">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="4c4f6-133">-OriginHostHeader</span></span>
<span data-ttu-id="4c4f6-134">Specifica la testa dell'host di origine dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-134">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="4c4f6-135">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="4c4f6-135">-OriginHostName</span></span>
<span data-ttu-id="4c4f6-136">Specifica il nome host del server di origine.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-136">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="4c4f6-137">-Originname</span><span class="sxs-lookup"><span data-stu-id="4c4f6-137">-OriginName</span></span>
<span data-ttu-id="4c4f6-138">Specifica il nome della risorsa del server di origine.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-138">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="4c4f6-139">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="4c4f6-139">-OriginPath</span></span>
<span data-ttu-id="4c4f6-140">Specifica il percorso del server di origine.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-140">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="4c4f6-141">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="4c4f6-141">-ProfileName</span></span>
<span data-ttu-id="4c4f6-142">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-142">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c4f6-143">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="4c4f6-143">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="4c4f6-144">Specifica il comportamento dell'endpoint CDN quando una stringa di query si trova nell'URL della richiesta.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-144">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="4c4f6-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c4f6-145">-ResourceGroupName</span></span>
<span data-ttu-id="4c4f6-146">Specifica il nome del gruppo di risorse a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-146">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c4f6-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="4c4f6-147">-Tags</span></span>
<span data-ttu-id="4c4f6-148">Specifica una tabella hash dei tag associati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-148">Specifies a hash table of the tags that associated with this resource.</span></span>

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

### <span data-ttu-id="4c4f6-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4c4f6-149">-Confirm</span></span>
<span data-ttu-id="4c4f6-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c4f6-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c4f6-151">-WhatIf</span></span>
<span data-ttu-id="4c4f6-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c4f6-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c4f6-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c4f6-154">-DefaultProfile</span></span>
<span data-ttu-id="4c4f6-155">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c4f6-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c4f6-156">CommonParameters</span></span>
<span data-ttu-id="4c4f6-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c4f6-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c4f6-158">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c4f6-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c4f6-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4c4f6-159">INPUTS</span></span>

### <span data-ttu-id="4c4f6-160">PSProfile</span><span class="sxs-lookup"><span data-stu-id="4c4f6-160">PSProfile</span></span>
<span data-ttu-id="4c4f6-161">Il parametro ' CdnProfile ' accetta il valore di tipo ' PSProfile ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="4c4f6-161">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="4c4f6-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c4f6-162">OUTPUTS</span></span>

### <span data-ttu-id="4c4f6-163">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="4c4f6-163">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="4c4f6-164">Note</span><span class="sxs-lookup"><span data-stu-id="4c4f6-164">NOTES</span></span>

## <span data-ttu-id="4c4f6-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c4f6-165">RELATED LINKS</span></span>

[<span data-ttu-id="4c4f6-166">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4c4f6-166">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="4c4f6-167">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4c4f6-167">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="4c4f6-168">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4c4f6-168">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="4c4f6-169">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4c4f6-169">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="4c4f6-170">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4c4f6-170">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


