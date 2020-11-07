---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 41271853dc1e8bbfa0781d4264594e899c75175e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676380"
---
# <span data-ttu-id="950c3-101">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="950c3-101">Add-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="950c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="950c3-102">SYNOPSIS</span></span>
<span data-ttu-id="950c3-103">Aggiunge un endpoint a un oggetto profilo di gestione traffico locale.</span><span class="sxs-lookup"><span data-stu-id="950c3-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="950c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="950c3-104">SYNTAX</span></span>

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="950c3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="950c3-105">DESCRIPTION</span></span>
<span data-ttu-id="950c3-106">Il cmdlet **Add-AzTrafficManagerEndpointConfig** aggiunge un endpoint a un oggetto profilo di Azure Traffic Manager locale.</span><span class="sxs-lookup"><span data-stu-id="950c3-106">The **Add-AzTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="950c3-107">Puoi ottenere un profilo usando i cmdlet New-AzTrafficManagerProfile o Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="950c3-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="950c3-108">Questo cmdlet opera nell'oggetto profilo locale.</span><span class="sxs-lookup"><span data-stu-id="950c3-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="950c3-109">Eseguire il commit delle modifiche apportate al profilo per Traffic Manager usando il cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="950c3-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="950c3-110">Per creare un endpoint e confermare la modifica in una singola operazione, usare il cmdlet New-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="950c3-110">To create an endpoint and commit the change in a single operation, use the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="950c3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="950c3-111">EXAMPLES</span></span>

### <span data-ttu-id="950c3-112">Esempio 1: aggiungere un endpoint a un profilo</span><span class="sxs-lookup"><span data-stu-id="950c3-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="950c3-113">Il primo comando ottiene un profilo di Azure Traffic Manager usando il cmdlet **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="950c3-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="950c3-114">Il comando Archivia il profilo locale nella variabile $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="950c3-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="950c3-115">Il secondo comando aggiunge un endpoint denominato Contoso al profilo archiviato in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="950c3-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="950c3-116">Il comando include i dati di configurazione per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="950c3-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="950c3-117">Questo comando modifica solo l'oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="950c3-117">This command changes only the local object.</span></span>

<span data-ttu-id="950c3-118">Il comando finale aggiorna il profilo di Traffic Manager in Azure in base al valore locale in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="950c3-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="950c3-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="950c3-119">PARAMETERS</span></span>

### <span data-ttu-id="950c3-120">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="950c3-120">-CustomHeader</span></span>
<span data-ttu-id="950c3-121">Elenco delle coppie nome intestazione personalizzate e valore per le richieste di probe.</span><span class="sxs-lookup"><span data-stu-id="950c3-121">List of custom header name and value pairs for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="950c3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="950c3-122">-DefaultProfile</span></span>
<span data-ttu-id="950c3-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="950c3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="950c3-124">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="950c3-124">-EndpointLocation</span></span>
<span data-ttu-id="950c3-125">Specifica la posizione dell'endpoint da usare nel metodo di routing del traffico delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="950c3-125">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="950c3-126">Questo parametro è applicabile solo agli endpoint del tipo ExternalEndpoints o NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="950c3-126">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="950c3-127">Devi specificare questo parametro quando viene usato il metodo di routing del traffico delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="950c3-127">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="950c3-128">Specificare un nome di area di Azure.</span><span class="sxs-lookup"><span data-stu-id="950c3-128">Specify an Azure region name.</span></span>
<span data-ttu-id="950c3-129">Per un elenco completo delle aree di Azure, vedere aree di Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="950c3-129">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="950c3-130">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="950c3-130">-EndpointName</span></span>
<span data-ttu-id="950c3-131">Specifica il nome dell'endpoint di gestione traffico che questo cmdlet aggiunge.</span><span class="sxs-lookup"><span data-stu-id="950c3-131">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

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

### <span data-ttu-id="950c3-132">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="950c3-132">-EndpointStatus</span></span>
<span data-ttu-id="950c3-133">Specifica lo stato dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="950c3-133">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="950c3-134">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="950c3-134">Valid values are:</span></span> 

- <span data-ttu-id="950c3-135">Abilitato</span><span class="sxs-lookup"><span data-stu-id="950c3-135">Enabled</span></span> 
- <span data-ttu-id="950c3-136">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="950c3-136">Disabled</span></span> 

<span data-ttu-id="950c3-137">Se lo stato è abilitato, l'endpoint viene esaminato per l'integrità dell'endpoint ed è incluso nel metodo di routing del traffico.</span><span class="sxs-lookup"><span data-stu-id="950c3-137">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="950c3-138">-Geomapping</span><span class="sxs-lookup"><span data-stu-id="950c3-138">-GeoMapping</span></span>
<span data-ttu-id="950c3-139">L'elenco delle aree geografiche mappate a questo endpoint quando si usa il metodo di routing del traffico "geografico".</span><span class="sxs-lookup"><span data-stu-id="950c3-139">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="950c3-140">Consultare la documentazione di Traffic Manager per un [elenco completo dei valori accettati](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span><span class="sxs-lookup"><span data-stu-id="950c3-140">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>

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

### <span data-ttu-id="950c3-141">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="950c3-141">-MinChildEndpoints</span></span>
<span data-ttu-id="950c3-142">Il numero minimo di endpoint che deve essere disponibile nel profilo figlio affinché l'endpoint annidato nel profilo padre venga considerato disponibile.</span><span class="sxs-lookup"><span data-stu-id="950c3-142">The minimum number of endpoints that must be available in the child profile in order for the Nested Endpoint in the parent profile to be considered available.</span></span>
<span data-ttu-id="950c3-143">Applicabile solo all'endpoint di tipo "NestedEndpoints".</span><span class="sxs-lookup"><span data-stu-id="950c3-143">Only applicable to endpoint of type 'NestedEndpoints'.</span></span>

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

### <span data-ttu-id="950c3-144">-Priorità</span><span class="sxs-lookup"><span data-stu-id="950c3-144">-Priority</span></span>
<span data-ttu-id="950c3-145">Specifica la priorità assegnata da Traffic Manager all'endpoint.</span><span class="sxs-lookup"><span data-stu-id="950c3-145">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="950c3-146">Questo parametro viene usato solo se il profilo di Traffic Manager è configurato con il metodo di routing prioritario.</span><span class="sxs-lookup"><span data-stu-id="950c3-146">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="950c3-147">I valori validi sono numeri interi compresi tra 1 e 1000.</span><span class="sxs-lookup"><span data-stu-id="950c3-147">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="950c3-148">I valori più bassi rappresentano la priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="950c3-148">Lower values represent higher priority.</span></span>

<span data-ttu-id="950c3-149">Se si specifica una priorità, è necessario specificare le priorità per tutti gli endpoint nel profilo e non ci sono due endpoint che condividono lo stesso valore di priorità.</span><span class="sxs-lookup"><span data-stu-id="950c3-149">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="950c3-150">Se non specifichi le priorità, Traffic Manager assegna i valori di priorità predefiniti agli endpoint, a partire da uno (1), nell'ordine in cui il profilo elenca gli endpoint.</span><span class="sxs-lookup"><span data-stu-id="950c3-150">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="950c3-151">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="950c3-151">-SubnetMapping</span></span>
<span data-ttu-id="950c3-152">Elenco di intervalli di indirizzi o subnet mappati a questo endpoint quando si usa il metodo di routing del traffico di ˜ Subnetâ €™.</span><span class="sxs-lookup"><span data-stu-id="950c3-152">The list of address ranges or subnets mapped to this endpoint when using the â€˜Subnetâ€™ traffic routing method.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="950c3-153">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="950c3-153">-Target</span></span>
<span data-ttu-id="950c3-154">Specifica il nome DNS completo dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="950c3-154">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="950c3-155">Traffic Manager restituisce questo valore nelle risposte DNS quando indirizza il traffico all'endpoint.</span><span class="sxs-lookup"><span data-stu-id="950c3-155">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="950c3-156">Specifica questo parametro solo per il tipo di endpoint ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="950c3-156">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="950c3-157">Per altri tipi di endpoint, specificare invece il parametro *TargetResourceId* .</span><span class="sxs-lookup"><span data-stu-id="950c3-157">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="950c3-158">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="950c3-158">-TargetResourceId</span></span>
<span data-ttu-id="950c3-159">Specifica l'ID risorsa della destinazione.</span><span class="sxs-lookup"><span data-stu-id="950c3-159">Specifies resource ID of the target.</span></span>
<span data-ttu-id="950c3-160">Specifica questo parametro solo per i tipi di endpoint AzureEndpoints e NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="950c3-160">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="950c3-161">Per il tipo di endpoint ExternalEndpoints, specificare invece il parametro di *destinazione* .</span><span class="sxs-lookup"><span data-stu-id="950c3-161">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="950c3-162">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="950c3-162">-TrafficManagerProfile</span></span>
<span data-ttu-id="950c3-163">Specifica un oggetto **TrafficManagerProfile** locale.</span><span class="sxs-lookup"><span data-stu-id="950c3-163">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="950c3-164">Questo cmdlet modifica questo oggetto locale.</span><span class="sxs-lookup"><span data-stu-id="950c3-164">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="950c3-165">Per ottenere un oggetto **TrafficManagerProfile** , usa il cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="950c3-165">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="950c3-166">-Digitare</span><span class="sxs-lookup"><span data-stu-id="950c3-166">-Type</span></span>
<span data-ttu-id="950c3-167">Specifica il tipo di endpoint che questo cmdlet aggiunge al profilo di Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="950c3-167">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="950c3-168">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="950c3-168">Valid values are:</span></span> 

- <span data-ttu-id="950c3-169">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="950c3-169">AzureEndpoints</span></span>
- <span data-ttu-id="950c3-170">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="950c3-170">ExternalEndpoints</span></span>
- <span data-ttu-id="950c3-171">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="950c3-171">NestedEndpoints</span></span>

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

### <span data-ttu-id="950c3-172">-Peso</span><span class="sxs-lookup"><span data-stu-id="950c3-172">-Weight</span></span>
<span data-ttu-id="950c3-173">Specifica il peso assegnato da Traffic Manager all'endpoint.</span><span class="sxs-lookup"><span data-stu-id="950c3-173">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="950c3-174">I valori validi sono numeri interi compresi tra 1 e 1000.</span><span class="sxs-lookup"><span data-stu-id="950c3-174">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="950c3-175">Il valore predefinito è uno (1).</span><span class="sxs-lookup"><span data-stu-id="950c3-175">The default value is one (1).</span></span>
<span data-ttu-id="950c3-176">Questo parametro viene usato solo se il profilo di Traffic Manager è configurato con il metodo di routing ponderato.</span><span class="sxs-lookup"><span data-stu-id="950c3-176">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="950c3-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="950c3-177">CommonParameters</span></span>
<span data-ttu-id="950c3-178">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="950c3-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="950c3-179">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="950c3-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="950c3-180">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="950c3-180">INPUTS</span></span>

### <span data-ttu-id="950c3-181">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="950c3-181">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="950c3-182">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="950c3-182">OUTPUTS</span></span>

### <span data-ttu-id="950c3-183">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="950c3-183">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="950c3-184">Note</span><span class="sxs-lookup"><span data-stu-id="950c3-184">NOTES</span></span>

## <span data-ttu-id="950c3-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="950c3-185">RELATED LINKS</span></span>

[<span data-ttu-id="950c3-186">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="950c3-186">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="950c3-187">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="950c3-187">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="950c3-188">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="950c3-188">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="950c3-189">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="950c3-189">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

