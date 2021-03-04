---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/powershell/module/az.network/move-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
ms.openlocfilehash: 6964767438fac6a1afd8da4333560f49cfe1bb44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952205"
---
# <span data-ttu-id="6eaad-101">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6eaad-101">Move-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="6eaad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6eaad-102">SYNOPSIS</span></span>
<span data-ttu-id="6eaad-103">Sposta un circuito ExpressRoute dal modello di distribuzione classica al modello di distribuzione di Gestione risorse.</span><span class="sxs-lookup"><span data-stu-id="6eaad-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

## <span data-ttu-id="6eaad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6eaad-104">SYNTAX</span></span>

```
Move-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> -ServiceKey <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6eaad-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6eaad-105">DESCRIPTION</span></span>
<span data-ttu-id="6eaad-106">Il cmdlet **Move-AzExpressRouteCircuit** sposta un circuito ExpressRoute dal modello di distribuzione classico al modello di distribuzione di Gestione risorse.</span><span class="sxs-lookup"><span data-stu-id="6eaad-106">The **Move-AzExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="6eaad-107">Dopo lo spostamento, il circuito ExpressRoute si comporta e funziona come qualsiasi altro circuito ExpressRoute creato nel modello di distribuzione di Gestione risorse.</span><span class="sxs-lookup"><span data-stu-id="6eaad-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="6eaad-108">I collegamenti di circuito, le reti virtuali e i gateway VPN non vengono spostati attraverso questa operazione.</span><span class="sxs-lookup"><span data-stu-id="6eaad-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="6eaad-109">Queste risorse devono essere riconfigurate dopo lo spostamento.</span><span class="sxs-lookup"><span data-stu-id="6eaad-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="6eaad-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6eaad-110">EXAMPLES</span></span>

### <span data-ttu-id="6eaad-111">Esempio 1: Spostare un circuito ExpressRoute nel modello di distribuzione di Gestione risorse</span><span class="sxs-lookup"><span data-stu-id="6eaad-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="6eaad-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6eaad-112">PARAMETERS</span></span>

### <span data-ttu-id="6eaad-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6eaad-113">-AsJob</span></span>
<span data-ttu-id="6eaad-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6eaad-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6eaad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eaad-115">-DefaultProfile</span></span>
<span data-ttu-id="6eaad-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6eaad-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6eaad-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6eaad-117">-Force</span></span>
<span data-ttu-id="6eaad-118">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="6eaad-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6eaad-119">-Location</span><span class="sxs-lookup"><span data-stu-id="6eaad-119">-Location</span></span>
<span data-ttu-id="6eaad-120">Nome della posizione di Azure in cui si trova il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="6eaad-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="6eaad-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6eaad-121">-Name</span></span>
<span data-ttu-id="6eaad-122">Nome del circuito ExpressRoute da spostare.</span><span class="sxs-lookup"><span data-stu-id="6eaad-122">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="6eaad-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eaad-123">-ResourceGroupName</span></span>
<span data-ttu-id="6eaad-124">Nome del gruppo di risorse che conterrà il circuito ExpressRoute da spostare.</span><span class="sxs-lookup"><span data-stu-id="6eaad-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="6eaad-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="6eaad-125">-ServiceKey</span></span>
<span data-ttu-id="6eaad-126">Chiave di servizio usata dal circuito ExpressRoute nel modello di distribuzione classica.</span><span class="sxs-lookup"><span data-stu-id="6eaad-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="6eaad-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="6eaad-127">-Tag</span></span>
<span data-ttu-id="6eaad-128">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6eaad-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6eaad-129">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="6eaad-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6eaad-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6eaad-130">-Confirm</span></span>
<span data-ttu-id="6eaad-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6eaad-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eaad-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eaad-132">-WhatIf</span></span>
<span data-ttu-id="6eaad-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6eaad-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6eaad-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6eaad-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eaad-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eaad-135">CommonParameters</span></span>
<span data-ttu-id="6eaad-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eaad-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eaad-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eaad-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eaad-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="6eaad-138">INPUTS</span></span>

### <span data-ttu-id="6eaad-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6eaad-139">System.String</span></span>

### <span data-ttu-id="6eaad-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="6eaad-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6eaad-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6eaad-141">OUTPUTS</span></span>

### <span data-ttu-id="6eaad-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6eaad-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="6eaad-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="6eaad-143">NOTES</span></span>

## <span data-ttu-id="6eaad-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6eaad-144">RELATED LINKS</span></span>

[<span data-ttu-id="6eaad-145">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6eaad-145">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="6eaad-146">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6eaad-146">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="6eaad-147">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6eaad-147">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="6eaad-148">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6eaad-148">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
