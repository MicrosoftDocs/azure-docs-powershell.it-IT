---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 4a5c59f6cc561bdd5f12462aab1e4cd634e70fc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514684"
---
# <span data-ttu-id="258be-101">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="258be-101">New-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="258be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="258be-102">SYNOPSIS</span></span>
<span data-ttu-id="258be-103">Crea un circuito di route di Azure Express.</span><span class="sxs-lookup"><span data-stu-id="258be-103">Creates an Azure express route circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="258be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="258be-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String>
 -BandwidthInMbps <Int32>
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="258be-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="258be-105">DESCRIPTION</span></span>
<span data-ttu-id="258be-106">Il cmdlet **New-AzureRmExpressRouteCircuit** crea un circuito di route di Azure Express.</span><span class="sxs-lookup"><span data-stu-id="258be-106">The **New-AzureRmExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="258be-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="258be-107">EXAMPLES</span></span>

### <span data-ttu-id="258be-108">Esempio 1: creare un nuovo circuito di ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="258be-108">Example 1: Create a new ExpressRoute circuit</span></span>
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
New-AzureRmExpressRouteCircuit @parameters
```

## <span data-ttu-id="258be-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="258be-109">PARAMETERS</span></span>

### <span data-ttu-id="258be-110">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="258be-110">-AllowClassicOperations</span></span>
<span data-ttu-id="258be-111">L'uso di questo parametro consente di usare i cmdlet di PowerShell di Azure classici per gestire il circuito.</span><span class="sxs-lookup"><span data-stu-id="258be-111">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="258be-112">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="258be-112">-Authorization</span></span>
<span data-ttu-id="258be-113">Un elenco di autorizzazioni Circuit.</span><span class="sxs-lookup"><span data-stu-id="258be-113">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="258be-114">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="258be-114">-BandwidthInMbps</span></span>
<span data-ttu-id="258be-115">La larghezza di banda del circuito.</span><span class="sxs-lookup"><span data-stu-id="258be-115">The bandwidth of the circuit.</span></span> <span data-ttu-id="258be-116">Deve essere un valore supportato dal provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="258be-116">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="258be-117">-Force</span><span class="sxs-lookup"><span data-stu-id="258be-117">-Force</span></span>
<span data-ttu-id="258be-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="258be-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="258be-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="258be-119">-Location</span></span>
<span data-ttu-id="258be-120">Posizione del circuito.</span><span class="sxs-lookup"><span data-stu-id="258be-120">The location of the circuit.</span></span>

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

### <span data-ttu-id="258be-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="258be-121">-Name</span></span>
<span data-ttu-id="258be-122">Nome del circuito di ExpressRoute da creare.</span><span class="sxs-lookup"><span data-stu-id="258be-122">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="258be-123">-Peering</span><span class="sxs-lookup"><span data-stu-id="258be-123">-Peering</span></span>
<span data-ttu-id="258be-124">Configurazioni peer elenco.</span><span class="sxs-lookup"><span data-stu-id="258be-124">A list peer configurations.</span></span>

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

### <span data-ttu-id="258be-125">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="258be-125">-PeeringLocation</span></span>
<span data-ttu-id="258be-126">Nome della posizione di peering supportata dal provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="258be-126">The name of the peering location supported by the service provider.</span></span>

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

### <span data-ttu-id="258be-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="258be-127">-ResourceGroupName</span></span>
<span data-ttu-id="258be-128">Gruppo di risorse che conterrà il circuito.</span><span class="sxs-lookup"><span data-stu-id="258be-128">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="258be-129">-ServiceProvidername</span><span class="sxs-lookup"><span data-stu-id="258be-129">-ServiceProviderName</span></span>
<span data-ttu-id="258be-130">Nome del provider di servizi Circuit.</span><span class="sxs-lookup"><span data-stu-id="258be-130">The name of the circuit service provider.</span></span> <span data-ttu-id="258be-131">Deve corrispondere a un nome elencato dal cmdlet Get-AzureRmExpressRouteServiceProvider.</span><span class="sxs-lookup"><span data-stu-id="258be-131">This must match a name listed by the Get-AzureRmExpressRouteServiceProvider cmdlet.</span></span>

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

### <span data-ttu-id="258be-132">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="258be-132">-SkuFamily</span></span>
<span data-ttu-id="258be-133">La famiglia SKU determina il tipo di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="258be-133">SKU family determines the billing type.</span></span> <span data-ttu-id="258be-134">I valori possibili per questo parametro sono: `MeteredData` o `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="258be-134">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="258be-135">Tieni presente che puoi cambiare il tipo di fatturazione da MeteredData a UnlimitedData, ma non puoi cambiare il tipo da UnlimitedData a MeteredData.</span><span class="sxs-lookup"><span data-stu-id="258be-135">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="258be-136">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="258be-136">-SkuTier</span></span>
<span data-ttu-id="258be-137">Livello di servizio per il circuito.</span><span class="sxs-lookup"><span data-stu-id="258be-137">The tier of service for the circuit.</span></span> <span data-ttu-id="258be-138">I valori possibili per questo parametro sono: `Standard` o `Premium` .</span><span class="sxs-lookup"><span data-stu-id="258be-138">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="258be-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="258be-139">-Tag</span></span>
<span data-ttu-id="258be-140">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="258be-140">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="258be-141">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="258be-141">For example:</span></span>

<span data-ttu-id="258be-142">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="258be-142">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="258be-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="258be-143">-Confirm</span></span>
<span data-ttu-id="258be-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="258be-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="258be-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="258be-145">-WhatIf</span></span>
<span data-ttu-id="258be-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="258be-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="258be-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="258be-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="258be-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="258be-148">-DefaultProfile</span></span>
<span data-ttu-id="258be-149">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="258be-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="258be-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="258be-150">CommonParameters</span></span>
<span data-ttu-id="258be-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="258be-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="258be-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="258be-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="258be-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="258be-153">INPUTS</span></span>

## <span data-ttu-id="258be-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="258be-154">OUTPUTS</span></span>

### <span data-ttu-id="258be-155">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="258be-155">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="258be-156">Note</span><span class="sxs-lookup"><span data-stu-id="258be-156">NOTES</span></span>

## <span data-ttu-id="258be-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="258be-157">RELATED LINKS</span></span>

[<span data-ttu-id="258be-158">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="258be-158">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="258be-159">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="258be-159">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="258be-160">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="258be-160">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="258be-161">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="258be-161">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
