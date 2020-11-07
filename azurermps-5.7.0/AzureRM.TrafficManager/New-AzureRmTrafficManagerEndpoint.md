---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 6117bbae035653762d99096eb8735885c0554d0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686663"
---
# <span data-ttu-id="ec727-101">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ec727-101">New-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="ec727-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ec727-102">SYNOPSIS</span></span>
<span data-ttu-id="ec727-103">Crea un endpoint in un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="ec727-103">Creates an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec727-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec727-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec727-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec727-105">DESCRIPTION</span></span>
<span data-ttu-id="ec727-106">Il cmdlet **New-AzureRmTrafficManagerEndpoint** crea un endpoint in un profilo di gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="ec727-106">The **New-AzureRmTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="ec727-107">Questo cmdlet consente di eseguire il commit di ogni nuovo endpoint nel servizio gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="ec727-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="ec727-108">Per aggiungere più endpoint a un oggetto profilo di gestione traffico locale e eseguire il commit delle modifiche in una singola operazione, usare il cmdlet Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="ec727-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="ec727-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec727-109">EXAMPLES</span></span>

### <span data-ttu-id="ec727-110">Esempio 1: creare un endpoint esterno per un profilo</span><span class="sxs-lookup"><span data-stu-id="ec727-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="ec727-111">Questo comando crea un endpoint esterno denominato Contoso nel profilo denominato ContosoProfile nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ec727-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="ec727-112">Esempio 2: creare un endpoint Azure per un profilo</span><span class="sxs-lookup"><span data-stu-id="ec727-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="ec727-113">Questo comando crea un endpoint Azure denominato Contoso nel profilo denominato ContosoProfile nel gruppo di risorse ResouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ec727-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="ec727-114">L'endpoint di Azure punta a Azure Web App il cui ID di gestione delle risorse di Azure viene assegnato dal percorso URI in *TargetResourceId*.</span><span class="sxs-lookup"><span data-stu-id="ec727-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="ec727-115">Il comando non specifica il parametro *EndpointLocation* perché la risorsa dell'app Web fornisce la posizione.</span><span class="sxs-lookup"><span data-stu-id="ec727-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="ec727-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec727-116">PARAMETERS</span></span>

### <span data-ttu-id="ec727-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec727-117">-DefaultProfile</span></span>
<span data-ttu-id="ec727-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ec727-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec727-119">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="ec727-119">-EndpointLocation</span></span>
<span data-ttu-id="ec727-120">Specifica la posizione dell'endpoint da usare nel metodo di routing del traffico delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="ec727-120">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="ec727-121">Questo parametro è applicabile solo agli endpoint del tipo ExternalEndpoints o NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="ec727-121">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="ec727-122">Devi specificare questo parametro quando viene usato il metodo di routing del traffico delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="ec727-122">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="ec727-123">Specificare un nome di area di Azure.</span><span class="sxs-lookup"><span data-stu-id="ec727-123">Specify an Azure region name.</span></span>
<span data-ttu-id="ec727-124">Per un elenco completo delle aree di Azure, vedere aree di Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="ec727-124">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="ec727-125">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="ec727-125">-EndpointStatus</span></span>
<span data-ttu-id="ec727-126">Specifica lo stato dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="ec727-126">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="ec727-127">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="ec727-127">Valid values are:</span></span> 

- <span data-ttu-id="ec727-128">Abilitato</span><span class="sxs-lookup"><span data-stu-id="ec727-128">Enabled</span></span> 
- <span data-ttu-id="ec727-129">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="ec727-129">Disabled</span></span> 

<span data-ttu-id="ec727-130">Se lo stato è abilitato, l'endpoint viene esaminato per l'integrità dell'endpoint ed è incluso nel metodo di routing del traffico.</span><span class="sxs-lookup"><span data-stu-id="ec727-130">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec727-131">-Geomapping</span><span class="sxs-lookup"><span data-stu-id="ec727-131">-GeoMapping</span></span>
<span data-ttu-id="ec727-132">L'elenco delle aree geografiche mappate a questo endpoint quando si usa il metodo di routing del traffico "geografico".</span><span class="sxs-lookup"><span data-stu-id="ec727-132">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="ec727-133">Consultare la documentazione di Traffic Manager per un elenco completo dei valori accettati.</span><span class="sxs-lookup"><span data-stu-id="ec727-133">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>
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

### <span data-ttu-id="ec727-134">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="ec727-134">-MinChildEndpoints</span></span>
<span data-ttu-id="ec727-135">Specificare un nome di area di Azure.</span><span class="sxs-lookup"><span data-stu-id="ec727-135">Specify an Azure region name.</span></span>
<span data-ttu-id="ec727-136">Per un elenco completo delle aree di Azure, vedere aree di Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="ec727-136">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec727-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="ec727-137">-Name</span></span>
<span data-ttu-id="ec727-138">Specifica il nome dell'endpoint di gestione traffico creato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec727-138">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ec727-139">-Priorità</span><span class="sxs-lookup"><span data-stu-id="ec727-139">-Priority</span></span>
<span data-ttu-id="ec727-140">Specifica la priorità assegnata da Traffic Manager all'endpoint.</span><span class="sxs-lookup"><span data-stu-id="ec727-140">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="ec727-141">Questo parametro viene usato solo se il profilo di Traffic Manager è configurato con il metodo di routing prioritario.</span><span class="sxs-lookup"><span data-stu-id="ec727-141">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="ec727-142">I valori validi sono numeri interi compresi tra 1 e 1000.</span><span class="sxs-lookup"><span data-stu-id="ec727-142">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="ec727-143">I valori più bassi rappresentano la priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="ec727-143">Lower values represent higher priority.</span></span>

<span data-ttu-id="ec727-144">Se si specifica una priorità, è necessario specificare le priorità per tutti gli endpoint nel profilo e non ci sono due endpoint che condividono lo stesso valore di priorità.</span><span class="sxs-lookup"><span data-stu-id="ec727-144">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="ec727-145">Se non specifichi le priorità, Traffic Manager assegna i valori di priorità predefiniti agli endpoint, a partire da uno (1), nell'ordine in cui il profilo elenca gli endpoint.</span><span class="sxs-lookup"><span data-stu-id="ec727-145">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec727-146">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="ec727-146">-ProfileName</span></span>
<span data-ttu-id="ec727-147">Specifica il nome di un profilo di gestione traffico a cui questo cmdlet aggiunge un endpoint.</span><span class="sxs-lookup"><span data-stu-id="ec727-147">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="ec727-148">Per ottenere un profilo, usare i cmdlet New-AzureRmTrafficManagerProfile o Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="ec727-148">To obtain a profile, use the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="ec727-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec727-149">-ResourceGroupName</span></span>
<span data-ttu-id="ec727-150">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ec727-150">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ec727-151">Questo cmdlet crea un endpoint di gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="ec727-151">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ec727-152">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="ec727-152">-Target</span></span>
<span data-ttu-id="ec727-153">Specifica il nome DNS completo dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="ec727-153">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="ec727-154">Traffic Manager restituisce questo valore nelle risposte DNS quando indirizza il traffico all'endpoint.</span><span class="sxs-lookup"><span data-stu-id="ec727-154">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="ec727-155">Specifica questo parametro solo per il tipo di endpoint ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="ec727-155">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="ec727-156">Per altri tipi di endpoint, specificare invece il parametro *TargetResourceId* .</span><span class="sxs-lookup"><span data-stu-id="ec727-156">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="ec727-157">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="ec727-157">-TargetResourceId</span></span>
<span data-ttu-id="ec727-158">Specifica l'ID risorsa della destinazione.</span><span class="sxs-lookup"><span data-stu-id="ec727-158">Specifies resource ID of the target.</span></span>
<span data-ttu-id="ec727-159">Specifica questo parametro solo per i tipi di endpoint AzureEndpoints e NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="ec727-159">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="ec727-160">Per il tipo di endpoint ExternalEndpoints, specificare invece il parametro di *destinazione* .</span><span class="sxs-lookup"><span data-stu-id="ec727-160">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="ec727-161">-Digitare</span><span class="sxs-lookup"><span data-stu-id="ec727-161">-Type</span></span>
<span data-ttu-id="ec727-162">Specifica il tipo di endpoint che questo cmdlet aggiunge al profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="ec727-162">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="ec727-163">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="ec727-163">Valid values are:</span></span> 

- <span data-ttu-id="ec727-164">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="ec727-164">AzureEndpoints</span></span>
- <span data-ttu-id="ec727-165">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="ec727-165">ExternalEndpoints</span></span>
- <span data-ttu-id="ec727-166">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="ec727-166">NestedEndpoints</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec727-167">-Peso</span><span class="sxs-lookup"><span data-stu-id="ec727-167">-Weight</span></span>
<span data-ttu-id="ec727-168">Specifica il peso assegnato da Traffic Manager all'endpoint.</span><span class="sxs-lookup"><span data-stu-id="ec727-168">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="ec727-169">I valori validi sono numeri interi compresi tra 1 e 1000.</span><span class="sxs-lookup"><span data-stu-id="ec727-169">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="ec727-170">Il valore predefinito è uno (1).</span><span class="sxs-lookup"><span data-stu-id="ec727-170">The default value is one (1).</span></span>
<span data-ttu-id="ec727-171">Questo parametro viene usato solo se il profilo di Traffic Manager è configurato con il metodo di routing ponderato.</span><span class="sxs-lookup"><span data-stu-id="ec727-171">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec727-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec727-172">CommonParameters</span></span>
<span data-ttu-id="ec727-173">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec727-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec727-174">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec727-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec727-175">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ec727-175">INPUTS</span></span>

### <span data-ttu-id="ec727-176">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ec727-176">None</span></span>
<span data-ttu-id="ec727-177">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="ec727-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ec727-178">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec727-178">OUTPUTS</span></span>

### <span data-ttu-id="ec727-179">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ec727-179">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="ec727-180">Note</span><span class="sxs-lookup"><span data-stu-id="ec727-180">NOTES</span></span>

## <span data-ttu-id="ec727-181">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec727-181">RELATED LINKS</span></span>

[<span data-ttu-id="ec727-182">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ec727-182">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="ec727-183">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ec727-183">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="ec727-184">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ec727-184">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="ec727-185">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ec727-185">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="ec727-186">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ec727-186">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="ec727-187">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ec727-187">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="ec727-188">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ec727-188">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


