---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
ms.openlocfilehash: 479b89296ae52221f714992791ed73cd14bf2fe0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184518"
---
# <span data-ttu-id="435e2-101">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="435e2-101">New-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="435e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="435e2-102">SYNOPSIS</span></span>
<span data-ttu-id="435e2-103">Crea un circuito Express Route di Azure.</span><span class="sxs-lookup"><span data-stu-id="435e2-103">Creates an Azure express route circuit.</span></span>

## <span data-ttu-id="435e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="435e2-104">SYNTAX</span></span>

### <span data-ttu-id="435e2-105">ServiceProvider (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="435e2-105">ServiceProvider (Default)</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String> -BandwidthInMbps <Int32>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="435e2-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="435e2-106">ExpressRoutePort</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ExpressRoutePort <PSExpressRoutePort> -BandwidthInGbps <Double>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="435e2-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="435e2-107">DESCRIPTION</span></span>
<span data-ttu-id="435e2-108">Il cmdlet **New-AzExpressRouteCircuit crea** un circuito Azure Express Route.</span><span class="sxs-lookup"><span data-stu-id="435e2-108">The **New-AzExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="435e2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="435e2-109">EXAMPLES</span></span>

### <span data-ttu-id="435e2-110">Esempio 1: Creare un nuovo circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="435e2-110">Example 1: Create a new ExpressRoute circuit</span></span>
```powershell
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

### <span data-ttu-id="435e2-111">Esempio 2: Creare un nuovo circuito ExpressRoute su ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="435e2-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
```powershell
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

## <span data-ttu-id="435e2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="435e2-112">PARAMETERS</span></span>

### <span data-ttu-id="435e2-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="435e2-113">-AllowClassicOperations</span></span>
<span data-ttu-id="435e2-114">L'uso di questo parametro consente di usare i cmdlet classici di Azure PowerShell per gestire il circuito.</span><span class="sxs-lookup"><span data-stu-id="435e2-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="435e2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="435e2-115">-AsJob</span></span>
<span data-ttu-id="435e2-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="435e2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="435e2-117">-Authorization</span><span class="sxs-lookup"><span data-stu-id="435e2-117">-Authorization</span></span>
<span data-ttu-id="435e2-118">Elenco di autorizzazioni del circuito.</span><span class="sxs-lookup"><span data-stu-id="435e2-118">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="435e2-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="435e2-119">-BandwidthInGbps</span></span>
<span data-ttu-id="435e2-120">Larghezza di banda del circuito durante il provisioning del circuito in una risorsa ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="435e2-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="435e2-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="435e2-121">-BandwidthInMbps</span></span>
<span data-ttu-id="435e2-122">Larghezza di banda del circuito.</span><span class="sxs-lookup"><span data-stu-id="435e2-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="435e2-123">Deve essere un valore supportato dal provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="435e2-123">This must be a value that is supported by the service provider.</span></span>

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

### <span data-ttu-id="435e2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="435e2-124">-DefaultProfile</span></span>
<span data-ttu-id="435e2-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="435e2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="435e2-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="435e2-126">-ExpressRoutePort</span></span>
<span data-ttu-id="435e2-127">Riferimento alla risorsa ExpressRoutePort durante il provisioning del circuito in una risorsa ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="435e2-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="435e2-128">-Force</span><span class="sxs-lookup"><span data-stu-id="435e2-128">-Force</span></span>
<span data-ttu-id="435e2-129">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="435e2-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="435e2-130">-Location</span><span class="sxs-lookup"><span data-stu-id="435e2-130">-Location</span></span>
<span data-ttu-id="435e2-131">Posizione del circuito.</span><span class="sxs-lookup"><span data-stu-id="435e2-131">The location of the circuit.</span></span>

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

### <span data-ttu-id="435e2-132">-Name</span><span class="sxs-lookup"><span data-stu-id="435e2-132">-Name</span></span>
<span data-ttu-id="435e2-133">Nome del circuito ExpressRoute da creare.</span><span class="sxs-lookup"><span data-stu-id="435e2-133">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="435e2-134">-Peering</span><span class="sxs-lookup"><span data-stu-id="435e2-134">-Peering</span></span>
<span data-ttu-id="435e2-135">Configurazioni peer di elenco.</span><span class="sxs-lookup"><span data-stu-id="435e2-135">A list peer configurations.</span></span>

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

### <span data-ttu-id="435e2-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="435e2-136">-PeeringLocation</span></span>
<span data-ttu-id="435e2-137">Nome della posizione di peering supportata dal provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="435e2-137">The name of the peering location supported by the service provider.</span></span>

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

### <span data-ttu-id="435e2-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="435e2-138">-ResourceGroupName</span></span>
<span data-ttu-id="435e2-139">Gruppo di risorse che conterrà il circuito.</span><span class="sxs-lookup"><span data-stu-id="435e2-139">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="435e2-140">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="435e2-140">-ServiceProviderName</span></span>
<span data-ttu-id="435e2-141">Nome del provider di servizi di circuito.</span><span class="sxs-lookup"><span data-stu-id="435e2-141">The name of the circuit service provider.</span></span> <span data-ttu-id="435e2-142">Deve corrispondere a un nome elencato dal cmdlet Get-AzExpressRouteServiceProvider servizio.</span><span class="sxs-lookup"><span data-stu-id="435e2-142">This must match a name listed by the Get-AzExpressRouteServiceProvider cmdlet.</span></span>

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

### <span data-ttu-id="435e2-143">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="435e2-143">-SkuFamily</span></span>
<span data-ttu-id="435e2-144">La famiglia di SKU determina il tipo di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="435e2-144">SKU family determines the billing type.</span></span> <span data-ttu-id="435e2-145">I valori possibili per questo parametro sono: `MeteredData` o `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="435e2-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="435e2-146">Si noti che è possibile modificare il tipo di fatturazione da MeteredData a UnlimitedData, ma non da UnlimitedData a MeteredData.</span><span class="sxs-lookup"><span data-stu-id="435e2-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="435e2-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="435e2-147">-SkuTier</span></span>
<span data-ttu-id="435e2-148">Il livello di servizio per il circuito.</span><span class="sxs-lookup"><span data-stu-id="435e2-148">The tier of service for the circuit.</span></span> <span data-ttu-id="435e2-149">I valori possibili per questo parametro sono: `Standard` , `Premium` o `Local` .</span><span class="sxs-lookup"><span data-stu-id="435e2-149">Possible values for this parameter are: `Standard`, `Premium` or `Local`.</span></span>

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

### <span data-ttu-id="435e2-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="435e2-150">-Tag</span></span>
<span data-ttu-id="435e2-151">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="435e2-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="435e2-152">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="435e2-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="435e2-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="435e2-153">-Confirm</span></span>
<span data-ttu-id="435e2-154">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="435e2-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="435e2-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="435e2-155">-WhatIf</span></span>
<span data-ttu-id="435e2-156">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="435e2-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="435e2-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="435e2-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="435e2-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="435e2-158">CommonParameters</span></span>
<span data-ttu-id="435e2-159">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="435e2-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="435e2-160">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="435e2-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="435e2-161">INPUT</span><span class="sxs-lookup"><span data-stu-id="435e2-161">INPUTS</span></span>

### <span data-ttu-id="435e2-162">System.String</span><span class="sxs-lookup"><span data-stu-id="435e2-162">System.String</span></span>

### <span data-ttu-id="435e2-163">System.Int32</span><span class="sxs-lookup"><span data-stu-id="435e2-163">System.Int32</span></span>

### <span data-ttu-id="435e2-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="435e2-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="435e2-165">System.Double</span><span class="sxs-lookup"><span data-stu-id="435e2-165">System.Double</span></span>

### <span data-ttu-id="435e2-166">Microsoft.Azure.Commands.Network.Models.PS Pseudoing[]</span><span class="sxs-lookup"><span data-stu-id="435e2-166">Microsoft.Azure.Commands.Network.Models.PSPeering[]</span></span>

### <span data-ttu-id="435e2-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span><span class="sxs-lookup"><span data-stu-id="435e2-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span></span>

### <span data-ttu-id="435e2-168">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="435e2-168">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="435e2-169">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="435e2-169">System.Collections.Hashtable</span></span>

## <span data-ttu-id="435e2-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="435e2-170">OUTPUTS</span></span>

### <span data-ttu-id="435e2-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="435e2-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="435e2-172">NOTE</span><span class="sxs-lookup"><span data-stu-id="435e2-172">NOTES</span></span>

## <span data-ttu-id="435e2-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="435e2-173">RELATED LINKS</span></span>

[<span data-ttu-id="435e2-174">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="435e2-174">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="435e2-175">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="435e2-175">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="435e2-176">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="435e2-176">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="435e2-177">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="435e2-177">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
