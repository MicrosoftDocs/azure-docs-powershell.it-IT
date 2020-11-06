---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: f2abe6acd0406f78ba2bb691b562cd0bcbffeb35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508515"
---
# <span data-ttu-id="65e83-101">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="65e83-101">Add-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="65e83-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="65e83-102">SYNOPSIS</span></span>
<span data-ttu-id="65e83-103">Aggiunge un endpoint a un oggetto profilo di gestione traffico locale.</span><span class="sxs-lookup"><span data-stu-id="65e83-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65e83-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65e83-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65e83-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65e83-105">DESCRIPTION</span></span>
<span data-ttu-id="65e83-106">Il cmdlet **Add-AzureRmTrafficManagerEndpointConfig** aggiunge un endpoint a un oggetto profilo di Azure Traffic Manager locale.</span><span class="sxs-lookup"><span data-stu-id="65e83-106">The **Add-AzureRmTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="65e83-107">Puoi ottenere un profilo usando i cmdlet New-AzureRmTrafficManagerProfile o Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="65e83-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="65e83-108">Questo cmdlet opera nell'oggetto profilo locale.</span><span class="sxs-lookup"><span data-stu-id="65e83-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="65e83-109">Eseguire il commit delle modifiche apportate al profilo per Traffic Manager usando il cmdlet Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="65e83-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="65e83-110">Per creare un endpoint e confermare la modifica in una singola operazione, usare il cmdlet New-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="65e83-110">To create an endpoint and commit the change in a single operation, use the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="65e83-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65e83-111">EXAMPLES</span></span>

### <span data-ttu-id="65e83-112">Esempio 1: aggiungere un endpoint a un profilo</span><span class="sxs-lookup"><span data-stu-id="65e83-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="65e83-113">Il primo comando ottiene un profilo di Azure Traffic Manager usando il cmdlet **Get-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="65e83-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="65e83-114">Il comando Archivia il profilo locale nella variabile $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="65e83-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="65e83-115">Il secondo comando aggiunge un endpoint denominato Contoso al profilo archiviato in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="65e83-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="65e83-116">Il comando include i dati di configurazione per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="65e83-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="65e83-117">Questo comando modifica solo l'oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="65e83-117">This command changes only the local object.</span></span>

<span data-ttu-id="65e83-118">Il comando finale aggiorna il profilo di Traffic Manager in Azure in base al valore locale in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="65e83-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="65e83-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="65e83-119">PARAMETERS</span></span>

### <span data-ttu-id="65e83-120">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="65e83-120">-EndpointLocation</span></span>
<span data-ttu-id="65e83-121">Specifica la posizione dell'endpoint da usare nel metodo di routing del traffico delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="65e83-121">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="65e83-122">Questo parametro è applicabile solo agli endpoint del tipo ExternalEndpoints o NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="65e83-122">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="65e83-123">Devi specificare questo parametro quando viene usato il metodo di routing del traffico delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="65e83-123">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="65e83-124">Specificare un nome di area di Azure.</span><span class="sxs-lookup"><span data-stu-id="65e83-124">Specify an Azure region name.</span></span>
<span data-ttu-id="65e83-125">Per un elenco completo delle aree di Azure, vedere aree di Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="65e83-125">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="65e83-126">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="65e83-126">-EndpointName</span></span>
<span data-ttu-id="65e83-127">Specifica il nome dell'endpoint di gestione traffico che questo cmdlet aggiunge.</span><span class="sxs-lookup"><span data-stu-id="65e83-127">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

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

### <span data-ttu-id="65e83-128">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="65e83-128">-EndpointStatus</span></span>
<span data-ttu-id="65e83-129">Specifica lo stato dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="65e83-129">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="65e83-130">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="65e83-130">Valid values are:</span></span> 

- <span data-ttu-id="65e83-131">Abilitato</span><span class="sxs-lookup"><span data-stu-id="65e83-131">Enabled</span></span> 
- <span data-ttu-id="65e83-132">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="65e83-132">Disabled</span></span> 

<span data-ttu-id="65e83-133">Se lo stato è abilitato, l'endpoint viene esaminato per l'integrità dell'endpoint ed è incluso nel metodo di routing del traffico.</span><span class="sxs-lookup"><span data-stu-id="65e83-133">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65e83-134">-Geomapping</span><span class="sxs-lookup"><span data-stu-id="65e83-134">-GeoMapping</span></span>
<span data-ttu-id="65e83-135">L'elenco delle aree geografiche mappate a questo endpoint quando si usa il metodo di routing del traffico "geografico".</span><span class="sxs-lookup"><span data-stu-id="65e83-135">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="65e83-136">Consultare la documentazione di Traffic Manager per un [elenco completo dei valori accettati](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span><span class="sxs-lookup"><span data-stu-id="65e83-136">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>
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

### <span data-ttu-id="65e83-137">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="65e83-137">-MinChildEndpoints</span></span>
<span data-ttu-id="65e83-138">Specificare un nome di area di Azure.</span><span class="sxs-lookup"><span data-stu-id="65e83-138">Specify an Azure region name.</span></span>
<span data-ttu-id="65e83-139">Per un elenco completo delle aree di Azure, vedere aree di Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="65e83-139">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65e83-140">-Priorità</span><span class="sxs-lookup"><span data-stu-id="65e83-140">-Priority</span></span>
<span data-ttu-id="65e83-141">Specifica la priorità assegnata da Traffic Manager all'endpoint.</span><span class="sxs-lookup"><span data-stu-id="65e83-141">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="65e83-142">Questo parametro viene usato solo se il profilo di Traffic Manager è configurato con il metodo di routing prioritario.</span><span class="sxs-lookup"><span data-stu-id="65e83-142">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="65e83-143">I valori validi sono numeri interi compresi tra 1 e 1000.</span><span class="sxs-lookup"><span data-stu-id="65e83-143">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="65e83-144">I valori più bassi rappresentano la priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="65e83-144">Lower values represent higher priority.</span></span>

<span data-ttu-id="65e83-145">Se si specifica una priorità, è necessario specificare le priorità per tutti gli endpoint nel profilo e non ci sono due endpoint che condividono lo stesso valore di priorità.</span><span class="sxs-lookup"><span data-stu-id="65e83-145">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="65e83-146">Se non specifichi le priorità, Traffic Manager assegna i valori di priorità predefiniti agli endpoint, a partire da uno (1), nell'ordine in cui il profilo elenca gli endpoint.</span><span class="sxs-lookup"><span data-stu-id="65e83-146">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65e83-147">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="65e83-147">-Target</span></span>
<span data-ttu-id="65e83-148">Specifica il nome DNS completo dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="65e83-148">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="65e83-149">Traffic Manager restituisce questo valore nelle risposte DNS quando indirizza il traffico all'endpoint.</span><span class="sxs-lookup"><span data-stu-id="65e83-149">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="65e83-150">Specifica questo parametro solo per il tipo di endpoint ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="65e83-150">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="65e83-151">Per altri tipi di endpoint, specificare invece il parametro *TargetResourceId* .</span><span class="sxs-lookup"><span data-stu-id="65e83-151">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="65e83-152">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="65e83-152">-TargetResourceId</span></span>
<span data-ttu-id="65e83-153">Specifica l'ID risorsa della destinazione.</span><span class="sxs-lookup"><span data-stu-id="65e83-153">Specifies resource ID of the target.</span></span>
<span data-ttu-id="65e83-154">Specifica questo parametro solo per i tipi di endpoint AzureEndpoints e NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="65e83-154">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="65e83-155">Per il tipo di endpoint ExternalEndpoints, specificare invece il parametro di *destinazione* .</span><span class="sxs-lookup"><span data-stu-id="65e83-155">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="65e83-156">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="65e83-156">-TrafficManagerProfile</span></span>
<span data-ttu-id="65e83-157">Specifica un oggetto **TrafficManagerProfile** locale.</span><span class="sxs-lookup"><span data-stu-id="65e83-157">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="65e83-158">Questo cmdlet modifica questo oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="65e83-158">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="65e83-159">Per ottenere un oggetto **TrafficManagerProfile** , usa il cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="65e83-159">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65e83-160">-Digitare</span><span class="sxs-lookup"><span data-stu-id="65e83-160">-Type</span></span>
<span data-ttu-id="65e83-161">Specifica il tipo di endpoint che questo cmdlet aggiunge al profilo di Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="65e83-161">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="65e83-162">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="65e83-162">Valid values are:</span></span> 

- <span data-ttu-id="65e83-163">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="65e83-163">AzureEndpoints</span></span>
- <span data-ttu-id="65e83-164">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="65e83-164">ExternalEndpoints</span></span>
- <span data-ttu-id="65e83-165">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="65e83-165">NestedEndpoints</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65e83-166">-Peso</span><span class="sxs-lookup"><span data-stu-id="65e83-166">-Weight</span></span>
<span data-ttu-id="65e83-167">Specifica il peso assegnato da Traffic Manager all'endpoint.</span><span class="sxs-lookup"><span data-stu-id="65e83-167">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="65e83-168">I valori validi sono numeri interi compresi tra 1 e 1000.</span><span class="sxs-lookup"><span data-stu-id="65e83-168">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="65e83-169">Il valore predefinito è uno (1).</span><span class="sxs-lookup"><span data-stu-id="65e83-169">The default value is one (1).</span></span>
<span data-ttu-id="65e83-170">Questo parametro viene usato solo se il profilo di Traffic Manager è configurato con il metodo di routing ponderato.</span><span class="sxs-lookup"><span data-stu-id="65e83-170">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65e83-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65e83-171">-DefaultProfile</span></span>
<span data-ttu-id="65e83-172">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="65e83-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65e83-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65e83-173">CommonParameters</span></span>
<span data-ttu-id="65e83-174">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65e83-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65e83-175">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65e83-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65e83-176">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="65e83-176">INPUTS</span></span>

### <span data-ttu-id="65e83-177">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="65e83-177">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="65e83-178">Questo cmdlet accetta un oggetto **TrafficManagerProfile** per questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65e83-178">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="65e83-179">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65e83-179">OUTPUTS</span></span>

### <span data-ttu-id="65e83-180">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="65e83-180">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="65e83-181">Questo cmdlet restituisce un oggetto **TrafficManagerProfile** modificato.</span><span class="sxs-lookup"><span data-stu-id="65e83-181">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="65e83-182">Note</span><span class="sxs-lookup"><span data-stu-id="65e83-182">NOTES</span></span>

## <span data-ttu-id="65e83-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65e83-183">RELATED LINKS</span></span>

[<span data-ttu-id="65e83-184">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="65e83-184">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="65e83-185">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="65e83-185">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="65e83-186">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="65e83-186">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="65e83-187">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="65e83-187">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


