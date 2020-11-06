---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 682c12270608f9c75e86cea742fd411e0eb657a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510055"
---
# <span data-ttu-id="147fe-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="147fe-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="147fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="147fe-102">SYNOPSIS</span></span>
<span data-ttu-id="147fe-103">Crea un endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="147fe-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="147fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="147fe-104">SYNTAX</span></span>

### <span data-ttu-id="147fe-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="147fe-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="147fe-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="147fe-106">ByObjectParameterSet</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="147fe-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="147fe-107">DESCRIPTION</span></span>
<span data-ttu-id="147fe-108">Il cmdlet **New-AzureRmCdnEndpoint** crea un endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="147fe-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="147fe-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="147fe-109">EXAMPLES</span></span>

## <span data-ttu-id="147fe-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="147fe-110">PARAMETERS</span></span>

### <span data-ttu-id="147fe-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="147fe-111">-CdnProfile</span></span>
<span data-ttu-id="147fe-112">Specifica l'oggetto del profilo CDN a cui viene aggiunto l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="147fe-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="147fe-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="147fe-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="147fe-114">Specifica una matrice di tipi di contenuto da comprimere dal nodo Edge al client.</span><span class="sxs-lookup"><span data-stu-id="147fe-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="147fe-115">-DefaultProfile</span></span>
<span data-ttu-id="147fe-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="147fe-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fe-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="147fe-117">-EndpointName</span></span>
<span data-ttu-id="147fe-118">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="147fe-118">Specifies the name of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fe-119">-Filtri geofiltrati</span><span class="sxs-lookup"><span data-stu-id="147fe-119">-GeoFilters</span></span>
<span data-ttu-id="147fe-120">Elenco dei filtri Geo che si applicano a questo endpoint.</span><span class="sxs-lookup"><span data-stu-id="147fe-120">The list of geo filters that applies to this endpoint.</span></span>

```yaml
Type: PSGeoFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fe-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="147fe-121">-HttpPort</span></span>
<span data-ttu-id="147fe-122">Specifica il numero di porta HTTP nel server di origine.</span><span class="sxs-lookup"><span data-stu-id="147fe-122">Specifies the HTTP port number on the origin server.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fe-123">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="147fe-123">-HttpsPort</span></span>
<span data-ttu-id="147fe-124">Specifica il numero di porta HTTPS nel server di origine.</span><span class="sxs-lookup"><span data-stu-id="147fe-124">Specifies the HTTPS port number on the origin server.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fe-125">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="147fe-125">-IsCompressionEnabled</span></span>
<span data-ttu-id="147fe-126">Indica se la compressione è abilitata per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="147fe-126">Indicates whether compression is enabled for the endpoint.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fe-127">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="147fe-127">-IsHttpAllowed</span></span>
<span data-ttu-id="147fe-128">Indica se l'endpoint Abilita il traffico HTTP.</span><span class="sxs-lookup"><span data-stu-id="147fe-128">Indicates whether the endpoint enables HTTP traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fe-129">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="147fe-129">-IsHttpsAllowed</span></span>
<span data-ttu-id="147fe-130">Indica se l'endpoint Abilita il traffico HTTPS.</span><span class="sxs-lookup"><span data-stu-id="147fe-130">Indicates whether the endpoint enables HTTPS traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fe-131">-Posizione</span><span class="sxs-lookup"><span data-stu-id="147fe-131">-Location</span></span>
<span data-ttu-id="147fe-132">Specifica la posizione della risorsa dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="147fe-132">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fe-133">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="147fe-133">-OptimizationType</span></span>
<span data-ttu-id="147fe-134">Specifica qualsiasi ottimizzazione di questo endpoint.</span><span class="sxs-lookup"><span data-stu-id="147fe-134">Specifies any optimization this endpoint has.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fe-135">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="147fe-135">-OriginHostHeader</span></span>
<span data-ttu-id="147fe-136">Specifica la testa dell'host di origine dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="147fe-136">Specifies the origin host head of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fe-137">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="147fe-137">-OriginHostName</span></span>
<span data-ttu-id="147fe-138">Specifica il nome host del server di origine.</span><span class="sxs-lookup"><span data-stu-id="147fe-138">Specifies the host name of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fe-139">-Originname</span><span class="sxs-lookup"><span data-stu-id="147fe-139">-OriginName</span></span>
<span data-ttu-id="147fe-140">Specifica il nome della risorsa del server di origine.</span><span class="sxs-lookup"><span data-stu-id="147fe-140">Specifies the resource name of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fe-141">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="147fe-141">-OriginPath</span></span>
<span data-ttu-id="147fe-142">Specifica il percorso del server di origine.</span><span class="sxs-lookup"><span data-stu-id="147fe-142">Specifies the path of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fe-143">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="147fe-143">-ProfileName</span></span>
<span data-ttu-id="147fe-144">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="147fe-144">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fe-145">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="147fe-145">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="147fe-146">Specifica il comportamento dell'endpoint CDN quando una stringa di query si trova nell'URL della richiesta.</span><span class="sxs-lookup"><span data-stu-id="147fe-146">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

```yaml
Type: PSQueryStringCachingBehavior
Parameter Sets: (All)
Aliases:
Accepted values: IgnoreQueryString, BypassCaching, UseQueryString, NotSet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fe-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="147fe-147">-ResourceGroupName</span></span>
<span data-ttu-id="147fe-148">Specifica il nome del gruppo di risorse a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="147fe-148">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fe-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="147fe-149">-Tag</span></span>
<span data-ttu-id="147fe-150">Tag da associare all'endpoint di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="147fe-150">The tags to associate with the Azure CDN endpoint.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fe-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="147fe-151">-Confirm</span></span>
<span data-ttu-id="147fe-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="147fe-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fe-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="147fe-153">-WhatIf</span></span>
<span data-ttu-id="147fe-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="147fe-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="147fe-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="147fe-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fe-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="147fe-156">CommonParameters</span></span>
<span data-ttu-id="147fe-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="147fe-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="147fe-158">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="147fe-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="147fe-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="147fe-159">INPUTS</span></span>

### <span data-ttu-id="147fe-160">PSProfile</span><span class="sxs-lookup"><span data-stu-id="147fe-160">PSProfile</span></span>
<span data-ttu-id="147fe-161">Il parametro ' CdnProfile ' accetta il valore di tipo ' PSProfile ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="147fe-161">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="147fe-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="147fe-162">OUTPUTS</span></span>

### <span data-ttu-id="147fe-163">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="147fe-163">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="147fe-164">Note</span><span class="sxs-lookup"><span data-stu-id="147fe-164">NOTES</span></span>

## <span data-ttu-id="147fe-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="147fe-165">RELATED LINKS</span></span>

[<span data-ttu-id="147fe-166">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="147fe-166">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="147fe-167">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="147fe-167">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="147fe-168">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="147fe-168">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="147fe-169">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="147fe-169">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="147fe-170">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="147fe-170">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


