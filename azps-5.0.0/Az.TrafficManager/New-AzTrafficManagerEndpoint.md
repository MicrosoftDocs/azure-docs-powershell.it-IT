---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9a32176afba8f4182ee1300e9b38936e9f35746c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199775"
---
# <span data-ttu-id="78d01-101">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="78d01-101">New-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="78d01-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="78d01-102">SYNOPSIS</span></span>
<span data-ttu-id="78d01-103">Crea un endpoint in un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="78d01-103">Creates an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="78d01-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78d01-104">SYNTAX</span></span>

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78d01-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78d01-105">DESCRIPTION</span></span>
<span data-ttu-id="78d01-106">Il cmdlet **New-AzTrafficManagerEndpoint** crea un endpoint in un profilo di gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="78d01-106">The **New-AzTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="78d01-107">Questo cmdlet consente di eseguire il commit di ogni nuovo endpoint nel servizio gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="78d01-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="78d01-108">Per aggiungere più endpoint a un oggetto profilo di gestione traffico locale e eseguire il commit delle modifiche in una singola operazione, usare il cmdlet Add-AzTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="78d01-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="78d01-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78d01-109">EXAMPLES</span></span>

### <span data-ttu-id="78d01-110">Esempio 1: creare un endpoint esterno per un profilo</span><span class="sxs-lookup"><span data-stu-id="78d01-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="78d01-111">Questo comando crea un endpoint esterno denominato Contoso nel profilo denominato ContosoProfile nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="78d01-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="78d01-112">Esempio 2: creare un endpoint Azure per un profilo</span><span class="sxs-lookup"><span data-stu-id="78d01-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="78d01-113">Questo comando crea un endpoint Azure denominato Contoso nel profilo denominato ContosoProfile nel gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="78d01-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="78d01-114">L'endpoint di Azure punta a Azure Web App il cui ID di gestione delle risorse di Azure viene assegnato dal percorso URI in *TargetResourceId*.</span><span class="sxs-lookup"><span data-stu-id="78d01-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="78d01-115">Il comando non specifica il parametro *EndpointLocation* perché la risorsa dell'app Web fornisce la posizione.</span><span class="sxs-lookup"><span data-stu-id="78d01-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="78d01-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="78d01-116">PARAMETERS</span></span>

### <span data-ttu-id="78d01-117">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="78d01-117">-CustomHeader</span></span>
<span data-ttu-id="78d01-118">Elenco delle coppie nome intestazione personalizzate e valore per le richieste di probe.</span><span class="sxs-lookup"><span data-stu-id="78d01-118">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="78d01-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78d01-119">-DefaultProfile</span></span>
<span data-ttu-id="78d01-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="78d01-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78d01-121">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="78d01-121">-EndpointLocation</span></span>
<span data-ttu-id="78d01-122">Specifica la posizione dell'endpoint da usare nel metodo di routing del traffico delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="78d01-122">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="78d01-123">Questo parametro è applicabile solo agli endpoint del tipo ExternalEndpoints o NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="78d01-123">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="78d01-124">Devi specificare questo parametro quando viene usato il metodo di routing del traffico delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="78d01-124">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="78d01-125">Specificare un nome di area di Azure.</span><span class="sxs-lookup"><span data-stu-id="78d01-125">Specify an Azure region name.</span></span>
<span data-ttu-id="78d01-126">Per un elenco completo delle aree di Azure, vedere aree di Azure http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="78d01-126">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="78d01-127">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="78d01-127">-EndpointStatus</span></span>
<span data-ttu-id="78d01-128">Specifica lo stato dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="78d01-128">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="78d01-129">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="78d01-129">Valid values are:</span></span> 

- <span data-ttu-id="78d01-130">Abilitato</span><span class="sxs-lookup"><span data-stu-id="78d01-130">Enabled</span></span> 
- <span data-ttu-id="78d01-131">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="78d01-131">Disabled</span></span> 

<span data-ttu-id="78d01-132">Se lo stato è abilitato, l'endpoint viene esaminato per l'integrità dell'endpoint ed è incluso nel metodo di routing del traffico.</span><span class="sxs-lookup"><span data-stu-id="78d01-132">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="78d01-133">-Geomapping</span><span class="sxs-lookup"><span data-stu-id="78d01-133">-GeoMapping</span></span>
<span data-ttu-id="78d01-134">L'elenco delle aree geografiche mappate a questo endpoint quando si usa il metodo di routing del traffico "geografico".</span><span class="sxs-lookup"><span data-stu-id="78d01-134">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="78d01-135">Consultare la documentazione di Traffic Manager per un elenco completo dei valori accettati.</span><span class="sxs-lookup"><span data-stu-id="78d01-135">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>

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

### <span data-ttu-id="78d01-136">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="78d01-136">-MinChildEndpoints</span></span>
<span data-ttu-id="78d01-137">Specificare un nome di area di Azure.</span><span class="sxs-lookup"><span data-stu-id="78d01-137">Specify an Azure region name.</span></span>
<span data-ttu-id="78d01-138">Per un elenco completo delle aree di Azure, vedere aree di Azure http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="78d01-138">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="78d01-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="78d01-139">-Name</span></span>
<span data-ttu-id="78d01-140">Specifica il nome dell'endpoint di gestione traffico creato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78d01-140">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="78d01-141">-Priorità</span><span class="sxs-lookup"><span data-stu-id="78d01-141">-Priority</span></span>
<span data-ttu-id="78d01-142">Specifica la priorità assegnata da Traffic Manager all'endpoint.</span><span class="sxs-lookup"><span data-stu-id="78d01-142">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="78d01-143">Questo parametro viene usato solo se il profilo di Traffic Manager è configurato con il metodo di routing prioritario.</span><span class="sxs-lookup"><span data-stu-id="78d01-143">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="78d01-144">I valori validi sono numeri interi compresi tra 1 e 1000.</span><span class="sxs-lookup"><span data-stu-id="78d01-144">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="78d01-145">I valori più bassi rappresentano la priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="78d01-145">Lower values represent higher priority.</span></span>

<span data-ttu-id="78d01-146">Se si specifica una priorità, è necessario specificare le priorità per tutti gli endpoint nel profilo e non ci sono due endpoint che condividono lo stesso valore di priorità.</span><span class="sxs-lookup"><span data-stu-id="78d01-146">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="78d01-147">Se non specifichi le priorità, Traffic Manager assegna i valori di priorità predefiniti agli endpoint, a partire da uno (1), nell'ordine in cui il profilo elenca gli endpoint.</span><span class="sxs-lookup"><span data-stu-id="78d01-147">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="78d01-148">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="78d01-148">-ProfileName</span></span>
<span data-ttu-id="78d01-149">Specifica il nome di un profilo di gestione traffico a cui questo cmdlet aggiunge un endpoint.</span><span class="sxs-lookup"><span data-stu-id="78d01-149">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="78d01-150">Per ottenere un profilo, usare i cmdlet New-AzTrafficManagerProfile o Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="78d01-150">To obtain a profile, use the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="78d01-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78d01-151">-ResourceGroupName</span></span>
<span data-ttu-id="78d01-152">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="78d01-152">Specifies the name of a resource group.</span></span>
<span data-ttu-id="78d01-153">Questo cmdlet crea un endpoint di gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="78d01-153">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="78d01-154">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="78d01-154">-SubnetMapping</span></span>
<span data-ttu-id="78d01-155">Elenco di intervalli di indirizzi o subnet mappati a questo endpoint quando si usa il metodo di routing del traffico "subnet".</span><span class="sxs-lookup"><span data-stu-id="78d01-155">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

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

### <span data-ttu-id="78d01-156">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="78d01-156">-Target</span></span>
<span data-ttu-id="78d01-157">Specifica il nome DNS completo dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="78d01-157">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="78d01-158">Traffic Manager restituisce questo valore nelle risposte DNS quando indirizza il traffico all'endpoint.</span><span class="sxs-lookup"><span data-stu-id="78d01-158">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="78d01-159">Specifica questo parametro solo per il tipo di endpoint ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="78d01-159">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="78d01-160">Per altri tipi di endpoint, specificare invece il parametro *TargetResourceId* .</span><span class="sxs-lookup"><span data-stu-id="78d01-160">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="78d01-161">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="78d01-161">-TargetResourceId</span></span>
<span data-ttu-id="78d01-162">Specifica l'ID risorsa della destinazione.</span><span class="sxs-lookup"><span data-stu-id="78d01-162">Specifies resource ID of the target.</span></span>
<span data-ttu-id="78d01-163">Specifica questo parametro solo per i tipi di endpoint AzureEndpoints e NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="78d01-163">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="78d01-164">Per il tipo di endpoint ExternalEndpoints, specificare invece il parametro di *destinazione* .</span><span class="sxs-lookup"><span data-stu-id="78d01-164">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="78d01-165">-Digitare</span><span class="sxs-lookup"><span data-stu-id="78d01-165">-Type</span></span>
<span data-ttu-id="78d01-166">Specifica il tipo di endpoint che questo cmdlet aggiunge al profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="78d01-166">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="78d01-167">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="78d01-167">Valid values are:</span></span> 

- <span data-ttu-id="78d01-168">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="78d01-168">AzureEndpoints</span></span>
- <span data-ttu-id="78d01-169">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="78d01-169">ExternalEndpoints</span></span>
- <span data-ttu-id="78d01-170">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="78d01-170">NestedEndpoints</span></span>

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

### <span data-ttu-id="78d01-171">-Peso</span><span class="sxs-lookup"><span data-stu-id="78d01-171">-Weight</span></span>
<span data-ttu-id="78d01-172">Specifica il peso assegnato da Traffic Manager all'endpoint.</span><span class="sxs-lookup"><span data-stu-id="78d01-172">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="78d01-173">I valori validi sono numeri interi compresi tra 1 e 1000.</span><span class="sxs-lookup"><span data-stu-id="78d01-173">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="78d01-174">Il valore predefinito è uno (1).</span><span class="sxs-lookup"><span data-stu-id="78d01-174">The default value is one (1).</span></span>
<span data-ttu-id="78d01-175">Questo parametro viene usato solo se il profilo di Traffic Manager è configurato con il metodo di routing ponderato.</span><span class="sxs-lookup"><span data-stu-id="78d01-175">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="78d01-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78d01-176">CommonParameters</span></span>
<span data-ttu-id="78d01-177">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78d01-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78d01-178">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78d01-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78d01-179">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="78d01-179">INPUTS</span></span>

### <span data-ttu-id="78d01-180">Nessuno</span><span class="sxs-lookup"><span data-stu-id="78d01-180">None</span></span>

## <span data-ttu-id="78d01-181">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78d01-181">OUTPUTS</span></span>

### <span data-ttu-id="78d01-182">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="78d01-182">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="78d01-183">Note</span><span class="sxs-lookup"><span data-stu-id="78d01-183">NOTES</span></span>

## <span data-ttu-id="78d01-184">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78d01-184">RELATED LINKS</span></span>

[<span data-ttu-id="78d01-185">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="78d01-185">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="78d01-186">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="78d01-186">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="78d01-187">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="78d01-187">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="78d01-188">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="78d01-188">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="78d01-189">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="78d01-189">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="78d01-190">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="78d01-190">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="78d01-191">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="78d01-191">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


