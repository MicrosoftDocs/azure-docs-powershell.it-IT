---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
ms.openlocfilehash: 76888e38487d54c3c7f2796cb49d660872fc5c96
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022708"
---
# <span data-ttu-id="1cbfd-101">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1cbfd-101">New-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="1cbfd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1cbfd-102">SYNOPSIS</span></span>
<span data-ttu-id="1cbfd-103">Crea un circuito di route di Azure Express.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-103">Creates an Azure express route circuit.</span></span>

## <span data-ttu-id="1cbfd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1cbfd-104">SYNTAX</span></span>

### <span data-ttu-id="1cbfd-105">ServiceProvider (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1cbfd-105">ServiceProvider (Default)</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String> -BandwidthInMbps <Int32>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cbfd-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="1cbfd-106">ExpressRoutePort</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ExpressRoutePort <PSExpressRoutePort> -BandwidthInGbps <Double>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cbfd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1cbfd-107">DESCRIPTION</span></span>
<span data-ttu-id="1cbfd-108">Il cmdlet **New-AzExpressRouteCircuit** crea un circuito di route di Azure Express.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-108">The **New-AzExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="1cbfd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1cbfd-109">EXAMPLES</span></span>

### <span data-ttu-id="1cbfd-110">Esempio 1: creare un nuovo circuito di ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="1cbfd-110">Example 1: Create a new ExpressRoute circuit</span></span>
```
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ServiceProviderName='Equinix'
    PeeringLocation='Silicon Valley'
    BandwidthInMbps=200
}
New-AzExpressRouteCircuit @parameters
```

### <span data-ttu-id="1cbfd-111">Esempio 2: creare un nuovo circuito di ExpressRoute in ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="1cbfd-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
```
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ExpressRoutePort=$PSExpressRoutePort
    BandwidthInGbps=10.0
}
New-AzExpressRouteCircuit @parameters
```

## <span data-ttu-id="1cbfd-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1cbfd-112">PARAMETERS</span></span>

### <span data-ttu-id="1cbfd-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="1cbfd-113">-AllowClassicOperations</span></span>
<span data-ttu-id="1cbfd-114">L'uso di questo parametro consente di usare i cmdlet di PowerShell di Azure classici per gestire il circuito.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cbfd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1cbfd-115">-AsJob</span></span>
<span data-ttu-id="1cbfd-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1cbfd-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cbfd-117">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="1cbfd-117">-Authorization</span></span>
<span data-ttu-id="1cbfd-118">Un elenco di autorizzazioni Circuit.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-118">A list of circuit authorizations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cbfd-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="1cbfd-119">-BandwidthInGbps</span></span>
<span data-ttu-id="1cbfd-120">La larghezza di banda del circuito quando viene effettuato il provisioning del circuito in una risorsa ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: System.Double
Parameter Sets: ExpressRoutePort
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cbfd-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="1cbfd-121">-BandwidthInMbps</span></span>
<span data-ttu-id="1cbfd-122">La larghezza di banda del circuito.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="1cbfd-123">Deve essere un valore supportato dal provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-123">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cbfd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cbfd-124">-DefaultProfile</span></span>
<span data-ttu-id="1cbfd-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cbfd-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="1cbfd-126">-ExpressRoutePort</span></span>
<span data-ttu-id="1cbfd-127">Il riferimento alla risorsa ExpressRoutePort quando viene effettuato il provisioning del circuito in una risorsa ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: ExpressRoutePort
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1cbfd-128">-Force</span><span class="sxs-lookup"><span data-stu-id="1cbfd-128">-Force</span></span>
<span data-ttu-id="1cbfd-129">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-129">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cbfd-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1cbfd-130">-Location</span></span>
<span data-ttu-id="1cbfd-131">Posizione del circuito.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-131">The location of the circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cbfd-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="1cbfd-132">-Name</span></span>
<span data-ttu-id="1cbfd-133">Nome del circuito di ExpressRoute da creare.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-133">The name of the ExpressRoute circuit being created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cbfd-134">-Peering</span><span class="sxs-lookup"><span data-stu-id="1cbfd-134">-Peering</span></span>
<span data-ttu-id="1cbfd-135">Configurazioni peer elenco.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-135">A list peer configurations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPeering[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cbfd-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="1cbfd-136">-PeeringLocation</span></span>
<span data-ttu-id="1cbfd-137">Nome della posizione di peering supportata dal provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-137">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cbfd-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cbfd-138">-ResourceGroupName</span></span>
<span data-ttu-id="1cbfd-139">Gruppo di risorse che conterrà il circuito.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-139">The resource group that will contain the circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cbfd-140">-ServiceProvidername</span><span class="sxs-lookup"><span data-stu-id="1cbfd-140">-ServiceProviderName</span></span>
<span data-ttu-id="1cbfd-141">Nome del provider di servizi Circuit.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-141">The name of the circuit service provider.</span></span> <span data-ttu-id="1cbfd-142">Deve corrispondere a un nome elencato dal cmdlet Get-AzExpressRouteServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-142">This must match a name listed by the Get-AzExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cbfd-143">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="1cbfd-143">-SkuFamily</span></span>
<span data-ttu-id="1cbfd-144">La famiglia SKU determina il tipo di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-144">SKU family determines the billing type.</span></span> <span data-ttu-id="1cbfd-145">I valori possibili per questo parametro sono: `MeteredData` o `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="1cbfd-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="1cbfd-146">Tieni presente che puoi cambiare il tipo di fatturazione da MeteredData a UnlimitedData, ma non puoi cambiare il tipo da UnlimitedData a MeteredData.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MeteredData, UnlimitedData

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cbfd-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="1cbfd-147">-SkuTier</span></span>
<span data-ttu-id="1cbfd-148">Livello di servizio per il circuito.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-148">The tier of service for the circuit.</span></span> <span data-ttu-id="1cbfd-149">I valori possibili per questo parametro sono `Standard` : `Premium` o `Local` .</span><span class="sxs-lookup"><span data-stu-id="1cbfd-149">Possible values for this parameter are: `Standard`, `Premium` or `Local`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium, Local

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cbfd-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="1cbfd-150">-Tag</span></span>
<span data-ttu-id="1cbfd-151">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1cbfd-152">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="1cbfd-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cbfd-153">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1cbfd-153">-Confirm</span></span>
<span data-ttu-id="1cbfd-154">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cbfd-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cbfd-155">-WhatIf</span></span>
<span data-ttu-id="1cbfd-156">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cbfd-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cbfd-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cbfd-158">CommonParameters</span></span>
<span data-ttu-id="1cbfd-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cbfd-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cbfd-160">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cbfd-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cbfd-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1cbfd-161">INPUTS</span></span>

### <span data-ttu-id="1cbfd-162">System. String</span><span class="sxs-lookup"><span data-stu-id="1cbfd-162">System.String</span></span>

### <span data-ttu-id="1cbfd-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1cbfd-163">System.Int32</span></span>

### <span data-ttu-id="1cbfd-164">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="1cbfd-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="1cbfd-165">System. Double</span><span class="sxs-lookup"><span data-stu-id="1cbfd-165">System.Double</span></span>

### <span data-ttu-id="1cbfd-166">Microsoft. Azure. Commands. Network. Models. PSPeering []</span><span class="sxs-lookup"><span data-stu-id="1cbfd-166">Microsoft.Azure.Commands.Network.Models.PSPeering[]</span></span>

### <span data-ttu-id="1cbfd-167">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization []</span><span class="sxs-lookup"><span data-stu-id="1cbfd-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span></span>

### <span data-ttu-id="1cbfd-168">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1cbfd-168">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1cbfd-169">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1cbfd-169">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1cbfd-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1cbfd-170">OUTPUTS</span></span>

### <span data-ttu-id="1cbfd-171">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1cbfd-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="1cbfd-172">Note</span><span class="sxs-lookup"><span data-stu-id="1cbfd-172">NOTES</span></span>

## <span data-ttu-id="1cbfd-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1cbfd-173">RELATED LINKS</span></span>

[<span data-ttu-id="1cbfd-174">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1cbfd-174">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="1cbfd-175">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1cbfd-175">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="1cbfd-176">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1cbfd-176">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="1cbfd-177">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1cbfd-177">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
