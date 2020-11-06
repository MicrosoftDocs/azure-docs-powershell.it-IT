---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 7eaadd8c80fff6491983a3e1d9c750227eba43cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508508"
---
# <span data-ttu-id="f78b8-101">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f78b8-101">New-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="f78b8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f78b8-102">SYNOPSIS</span></span>
<span data-ttu-id="f78b8-103">Crea un endpoint in un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="f78b8-103">Creates an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f78b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f78b8-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f78b8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f78b8-105">DESCRIPTION</span></span>
<span data-ttu-id="f78b8-106">Il cmdlet **New-AzureRmTrafficManagerEndpoint** crea un endpoint in un profilo di gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="f78b8-106">The **New-AzureRmTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="f78b8-107">Questo cmdlet consente di eseguire il commit di ogni nuovo endpoint nel servizio gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="f78b8-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="f78b8-108">Per aggiungere più endpoint a un oggetto profilo di gestione traffico locale e eseguire il commit delle modifiche in una singola operazione, usare il cmdlet Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="f78b8-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="f78b8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f78b8-109">EXAMPLES</span></span>

### <span data-ttu-id="f78b8-110">Esempio 1: creare un endpoint esterno per un profilo</span><span class="sxs-lookup"><span data-stu-id="f78b8-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="f78b8-111">Questo comando crea un endpoint esterno denominato Contoso nel profilo denominato ContosoProfile nel gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f78b8-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="f78b8-112">Esempio 2: creare un endpoint Azure per un profilo</span><span class="sxs-lookup"><span data-stu-id="f78b8-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="f78b8-113">Questo comando crea un endpoint Azure denominato Contoso nel profilo denominato ContosoProfile nel gruppo di risorse ResouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f78b8-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="f78b8-114">L'endpoint di Azure punta a Azure Web App il cui ID di gestione delle risorse di Azure viene assegnato dal percorso URI in *TargetResourceId*.</span><span class="sxs-lookup"><span data-stu-id="f78b8-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="f78b8-115">Il comando non specifica il parametro *EndpointLocation* perché la risorsa dell'app Web fornisce la posizione.</span><span class="sxs-lookup"><span data-stu-id="f78b8-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="f78b8-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f78b8-116">PARAMETERS</span></span>

### <span data-ttu-id="f78b8-117">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="f78b8-117">-EndpointLocation</span></span>
<span data-ttu-id="f78b8-118">Specifica la posizione dell'endpoint da usare nel metodo di routing del traffico delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="f78b8-118">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="f78b8-119">Questo parametro è applicabile solo agli endpoint del tipo ExternalEndpoints o NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="f78b8-119">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="f78b8-120">Devi specificare questo parametro quando viene usato il metodo di routing del traffico delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="f78b8-120">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="f78b8-121">Specificare un nome di area di Azure.</span><span class="sxs-lookup"><span data-stu-id="f78b8-121">Specify an Azure region name.</span></span>
<span data-ttu-id="f78b8-122">Per un elenco completo delle aree di Azure, vedere aree di Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="f78b8-122">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="f78b8-123">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="f78b8-123">-EndpointStatus</span></span>
<span data-ttu-id="f78b8-124">Specifica lo stato dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="f78b8-124">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="f78b8-125">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="f78b8-125">Valid values are:</span></span> 

- <span data-ttu-id="f78b8-126">Abilitato</span><span class="sxs-lookup"><span data-stu-id="f78b8-126">Enabled</span></span> 
- <span data-ttu-id="f78b8-127">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="f78b8-127">Disabled</span></span> 

<span data-ttu-id="f78b8-128">Se lo stato è abilitato, l'endpoint viene esaminato per l'integrità dell'endpoint ed è incluso nel metodo di routing del traffico.</span><span class="sxs-lookup"><span data-stu-id="f78b8-128">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="f78b8-129">-Geomapping</span><span class="sxs-lookup"><span data-stu-id="f78b8-129">-GeoMapping</span></span>
<span data-ttu-id="f78b8-130">L'elenco delle aree geografiche mappate a questo endpoint quando si usa il metodo di routing del traffico "geografico".</span><span class="sxs-lookup"><span data-stu-id="f78b8-130">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="f78b8-131">Consultare la documentazione di Traffic Manager per un elenco completo dei valori accettati.</span><span class="sxs-lookup"><span data-stu-id="f78b8-131">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>
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

### <span data-ttu-id="f78b8-132">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="f78b8-132">-MinChildEndpoints</span></span>
<span data-ttu-id="f78b8-133">Specificare un nome di area di Azure.</span><span class="sxs-lookup"><span data-stu-id="f78b8-133">Specify an Azure region name.</span></span>
<span data-ttu-id="f78b8-134">Per un elenco completo delle aree di Azure, vedere aree di Azure https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="f78b8-134">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="f78b8-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="f78b8-135">-Name</span></span>
<span data-ttu-id="f78b8-136">Specifica il nome dell'endpoint di gestione traffico creato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f78b8-136">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f78b8-137">-Priorità</span><span class="sxs-lookup"><span data-stu-id="f78b8-137">-Priority</span></span>
<span data-ttu-id="f78b8-138">Specifica la priorità assegnata da Traffic Manager all'endpoint.</span><span class="sxs-lookup"><span data-stu-id="f78b8-138">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="f78b8-139">Questo parametro viene usato solo se il profilo di Traffic Manager è configurato con il metodo di routing prioritario.</span><span class="sxs-lookup"><span data-stu-id="f78b8-139">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="f78b8-140">I valori validi sono numeri interi compresi tra 1 e 1000.</span><span class="sxs-lookup"><span data-stu-id="f78b8-140">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="f78b8-141">I valori più bassi rappresentano la priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="f78b8-141">Lower values represent higher priority.</span></span>

<span data-ttu-id="f78b8-142">Se si specifica una priorità, è necessario specificare le priorità per tutti gli endpoint nel profilo e non ci sono due endpoint che condividono lo stesso valore di priorità.</span><span class="sxs-lookup"><span data-stu-id="f78b8-142">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="f78b8-143">Se non specifichi le priorità, Traffic Manager assegna i valori di priorità predefiniti agli endpoint, a partire da uno (1), nell'ordine in cui il profilo elenca gli endpoint.</span><span class="sxs-lookup"><span data-stu-id="f78b8-143">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="f78b8-144">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="f78b8-144">-ProfileName</span></span>
<span data-ttu-id="f78b8-145">Specifica il nome di un profilo di gestione traffico a cui questo cmdlet aggiunge un endpoint.</span><span class="sxs-lookup"><span data-stu-id="f78b8-145">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="f78b8-146">Per ottenere un profilo, usare i cmdlet New-AzureRmTrafficManagerProfile o Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f78b8-146">To obtain a profile, use the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="f78b8-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f78b8-147">-ResourceGroupName</span></span>
<span data-ttu-id="f78b8-148">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f78b8-148">Specifies the name of a resource group.</span></span>
<span data-ttu-id="f78b8-149">Questo cmdlet crea un endpoint di gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f78b8-149">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f78b8-150">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="f78b8-150">-Target</span></span>
<span data-ttu-id="f78b8-151">Specifica il nome DNS completo dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="f78b8-151">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="f78b8-152">Traffic Manager restituisce questo valore nelle risposte DNS quando indirizza il traffico all'endpoint.</span><span class="sxs-lookup"><span data-stu-id="f78b8-152">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="f78b8-153">Specifica questo parametro solo per il tipo di endpoint ExternalEndpoints.</span><span class="sxs-lookup"><span data-stu-id="f78b8-153">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="f78b8-154">Per altri tipi di endpoint, specificare invece il parametro *TargetResourceId* .</span><span class="sxs-lookup"><span data-stu-id="f78b8-154">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="f78b8-155">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f78b8-155">-TargetResourceId</span></span>
<span data-ttu-id="f78b8-156">Specifica l'ID risorsa della destinazione.</span><span class="sxs-lookup"><span data-stu-id="f78b8-156">Specifies resource ID of the target.</span></span>
<span data-ttu-id="f78b8-157">Specifica questo parametro solo per i tipi di endpoint AzureEndpoints e NestedEndpoints.</span><span class="sxs-lookup"><span data-stu-id="f78b8-157">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="f78b8-158">Per il tipo di endpoint ExternalEndpoints, specificare invece il parametro di *destinazione* .</span><span class="sxs-lookup"><span data-stu-id="f78b8-158">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="f78b8-159">-Digitare</span><span class="sxs-lookup"><span data-stu-id="f78b8-159">-Type</span></span>
<span data-ttu-id="f78b8-160">Specifica il tipo di endpoint che questo cmdlet aggiunge al profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="f78b8-160">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="f78b8-161">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="f78b8-161">Valid values are:</span></span> 

- <span data-ttu-id="f78b8-162">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="f78b8-162">AzureEndpoints</span></span>
- <span data-ttu-id="f78b8-163">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="f78b8-163">ExternalEndpoints</span></span>
- <span data-ttu-id="f78b8-164">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="f78b8-164">NestedEndpoints</span></span>

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

### <span data-ttu-id="f78b8-165">-Peso</span><span class="sxs-lookup"><span data-stu-id="f78b8-165">-Weight</span></span>
<span data-ttu-id="f78b8-166">Specifica il peso assegnato da Traffic Manager all'endpoint.</span><span class="sxs-lookup"><span data-stu-id="f78b8-166">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="f78b8-167">I valori validi sono numeri interi compresi tra 1 e 1000.</span><span class="sxs-lookup"><span data-stu-id="f78b8-167">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="f78b8-168">Il valore predefinito è uno (1).</span><span class="sxs-lookup"><span data-stu-id="f78b8-168">The default value is one (1).</span></span>
<span data-ttu-id="f78b8-169">Questo parametro viene usato solo se il profilo di Traffic Manager è configurato con il metodo di routing ponderato.</span><span class="sxs-lookup"><span data-stu-id="f78b8-169">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="f78b8-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f78b8-170">-DefaultProfile</span></span>
<span data-ttu-id="f78b8-171">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f78b8-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f78b8-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f78b8-172">CommonParameters</span></span>
<span data-ttu-id="f78b8-173">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f78b8-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f78b8-174">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f78b8-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f78b8-175">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f78b8-175">INPUTS</span></span>

## <span data-ttu-id="f78b8-176">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f78b8-176">OUTPUTS</span></span>

### <span data-ttu-id="f78b8-177">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f78b8-177">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="f78b8-178">Note</span><span class="sxs-lookup"><span data-stu-id="f78b8-178">NOTES</span></span>

## <span data-ttu-id="f78b8-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f78b8-179">RELATED LINKS</span></span>

[<span data-ttu-id="f78b8-180">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f78b8-180">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="f78b8-181">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f78b8-181">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="f78b8-182">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f78b8-182">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="f78b8-183">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f78b8-183">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="f78b8-184">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f78b8-184">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="f78b8-185">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f78b8-185">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="f78b8-186">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f78b8-186">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


