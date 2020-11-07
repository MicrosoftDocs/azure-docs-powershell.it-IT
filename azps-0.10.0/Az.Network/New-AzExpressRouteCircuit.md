---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzExpressRouteCircuit.md
ms.openlocfilehash: d03b52c477686f3aa724057771285eaf9d522a56
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860517"
---
# <span data-ttu-id="e5638-101">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e5638-101">New-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="e5638-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e5638-102">SYNOPSIS</span></span>
<span data-ttu-id="e5638-103">Crea un circuito di route di Azure Express.</span><span class="sxs-lookup"><span data-stu-id="e5638-103">Creates an Azure express route circuit.</span></span>

## <span data-ttu-id="e5638-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5638-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String>
 -BandwidthInMbps <Int32>
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5638-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5638-105">DESCRIPTION</span></span>
<span data-ttu-id="e5638-106">Il cmdlet **New-AzExpressRouteCircuit** crea un circuito di route di Azure Express.</span><span class="sxs-lookup"><span data-stu-id="e5638-106">The **New-AzExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="e5638-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5638-107">EXAMPLES</span></span>

### <span data-ttu-id="e5638-108">Esempio 1: creare un nuovo circuito di ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="e5638-108">Example 1: Create a new ExpressRoute circuit</span></span>
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

## <span data-ttu-id="e5638-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e5638-109">PARAMETERS</span></span>

### <span data-ttu-id="e5638-110">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="e5638-110">-AllowClassicOperations</span></span>
<span data-ttu-id="e5638-111">L'uso di questo parametro consente di usare i cmdlet di PowerShell di Azure classici per gestire il circuito.</span><span class="sxs-lookup"><span data-stu-id="e5638-111">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5638-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5638-112">-AsJob</span></span>
<span data-ttu-id="e5638-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e5638-113">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5638-114">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="e5638-114">-Authorization</span></span>
<span data-ttu-id="e5638-115">Un elenco di autorizzazioni Circuit.</span><span class="sxs-lookup"><span data-stu-id="e5638-115">A list of circuit authorizations.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5638-116">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="e5638-116">-BandwidthInMbps</span></span>
<span data-ttu-id="e5638-117">La larghezza di banda del circuito.</span><span class="sxs-lookup"><span data-stu-id="e5638-117">The bandwidth of the circuit.</span></span> <span data-ttu-id="e5638-118">Deve essere un valore supportato dal provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="e5638-118">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5638-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5638-119">-DefaultProfile</span></span>
<span data-ttu-id="e5638-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e5638-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5638-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e5638-121">-Force</span></span>
<span data-ttu-id="e5638-122">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e5638-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5638-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e5638-123">-Location</span></span>
<span data-ttu-id="e5638-124">Posizione del circuito.</span><span class="sxs-lookup"><span data-stu-id="e5638-124">The location of the circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5638-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5638-125">-Name</span></span>
<span data-ttu-id="e5638-126">Nome del circuito di ExpressRoute da creare.</span><span class="sxs-lookup"><span data-stu-id="e5638-126">The name of the ExpressRoute circuit being created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5638-127">-Peering</span><span class="sxs-lookup"><span data-stu-id="e5638-127">-Peering</span></span>
<span data-ttu-id="e5638-128">Configurazioni peer elenco.</span><span class="sxs-lookup"><span data-stu-id="e5638-128">A list peer configurations.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5638-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="e5638-129">-PeeringLocation</span></span>
<span data-ttu-id="e5638-130">Nome della posizione di peering supportata dal provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="e5638-130">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5638-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5638-131">-ResourceGroupName</span></span>
<span data-ttu-id="e5638-132">Gruppo di risorse che conterrà il circuito.</span><span class="sxs-lookup"><span data-stu-id="e5638-132">The resource group that will contain the circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5638-133">-ServiceProvidername</span><span class="sxs-lookup"><span data-stu-id="e5638-133">-ServiceProviderName</span></span>
<span data-ttu-id="e5638-134">Nome del provider di servizi Circuit.</span><span class="sxs-lookup"><span data-stu-id="e5638-134">The name of the circuit service provider.</span></span> <span data-ttu-id="e5638-135">Deve corrispondere a un nome elencato dal cmdlet Get-AzExpressRouteServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="e5638-135">This must match a name listed by the Get-AzExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5638-136">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="e5638-136">-SkuFamily</span></span>
<span data-ttu-id="e5638-137">La famiglia SKU determina il tipo di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="e5638-137">SKU family determines the billing type.</span></span> <span data-ttu-id="e5638-138">I valori possibili per questo parametro sono: `MeteredData` o `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="e5638-138">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="e5638-139">Tieni presente che puoi cambiare il tipo di fatturazione da MeteredData a UnlimitedData, ma non puoi cambiare il tipo da UnlimitedData a MeteredData.</span><span class="sxs-lookup"><span data-stu-id="e5638-139">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: MeteredData, UnlimitedData

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5638-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="e5638-140">-SkuTier</span></span>
<span data-ttu-id="e5638-141">Livello di servizio per il circuito.</span><span class="sxs-lookup"><span data-stu-id="e5638-141">The tier of service for the circuit.</span></span> <span data-ttu-id="e5638-142">I valori possibili per questo parametro sono: `Standard` o `Premium` .</span><span class="sxs-lookup"><span data-stu-id="e5638-142">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5638-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="e5638-143">-Tag</span></span>
<span data-ttu-id="e5638-144">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e5638-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e5638-145">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="e5638-145">For example:</span></span>

<span data-ttu-id="e5638-146">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e5638-146">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5638-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e5638-147">-Confirm</span></span>
<span data-ttu-id="e5638-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5638-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5638-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5638-149">-WhatIf</span></span>
<span data-ttu-id="e5638-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5638-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5638-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5638-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5638-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5638-152">CommonParameters</span></span>
<span data-ttu-id="e5638-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5638-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5638-154">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5638-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5638-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e5638-155">INPUTS</span></span>

## <span data-ttu-id="e5638-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5638-156">OUTPUTS</span></span>

### <span data-ttu-id="e5638-157">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e5638-157">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="e5638-158">Note</span><span class="sxs-lookup"><span data-stu-id="e5638-158">NOTES</span></span>

## <span data-ttu-id="e5638-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5638-159">RELATED LINKS</span></span>

[<span data-ttu-id="e5638-160">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e5638-160">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="e5638-161">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e5638-161">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="e5638-162">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e5638-162">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="e5638-163">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="e5638-163">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
