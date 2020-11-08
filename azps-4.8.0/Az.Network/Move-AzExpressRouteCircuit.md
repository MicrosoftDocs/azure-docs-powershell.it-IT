---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/move-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
ms.openlocfilehash: 2c5219e4a829ac9786b69a41afaa7362783f26b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192361"
---
# <span data-ttu-id="565a0-101">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="565a0-101">Move-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="565a0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="565a0-102">SYNOPSIS</span></span>
<span data-ttu-id="565a0-103">Sposta un circuito ExpressRoute dal modello di distribuzione classico al modello di distribuzione di Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="565a0-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

## <span data-ttu-id="565a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="565a0-104">SYNTAX</span></span>

```
Move-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> -ServiceKey <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="565a0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="565a0-105">DESCRIPTION</span></span>
<span data-ttu-id="565a0-106">Il cmdlet **Move-AzExpressRouteCircuit** sposta un circuito ExpressRoute dal modello di distribuzione classico al modello di distribuzione di Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="565a0-106">The **Move-AzExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="565a0-107">Dopo lo sviluppo, il circuito di ExpressRoute si comporta come qualsiasi altro circuito di ExpressRoute creato nel modello di distribuzione di Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="565a0-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="565a0-108">I collegamenti a circuiti, le reti virtuali e i gateway VPN non vengono spostati in questa operazione.</span><span class="sxs-lookup"><span data-stu-id="565a0-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="565a0-109">Queste risorse devono essere riconfigurate dopo lo sposta.</span><span class="sxs-lookup"><span data-stu-id="565a0-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="565a0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="565a0-110">EXAMPLES</span></span>

### <span data-ttu-id="565a0-111">Esempio 1: trasferire un circuito di ExpressRoute nel modello di distribuzione di gestione risorse</span><span class="sxs-lookup"><span data-stu-id="565a0-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="565a0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="565a0-112">PARAMETERS</span></span>

### <span data-ttu-id="565a0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="565a0-113">-AsJob</span></span>
<span data-ttu-id="565a0-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="565a0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="565a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="565a0-115">-DefaultProfile</span></span>
<span data-ttu-id="565a0-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="565a0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="565a0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="565a0-117">-Force</span></span>
<span data-ttu-id="565a0-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="565a0-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="565a0-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="565a0-119">-Location</span></span>
<span data-ttu-id="565a0-120">Nome della posizione di Azure in cui si trova il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="565a0-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="565a0-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="565a0-121">-Name</span></span>
<span data-ttu-id="565a0-122">Il nome del circuito di ExpressRoute da spostare.</span><span class="sxs-lookup"><span data-stu-id="565a0-122">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="565a0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="565a0-123">-ResourceGroupName</span></span>
<span data-ttu-id="565a0-124">Nome del gruppo di risorse che conterrà il circuito ExpressRoute spostato.</span><span class="sxs-lookup"><span data-stu-id="565a0-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="565a0-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="565a0-125">-ServiceKey</span></span>
<span data-ttu-id="565a0-126">Il codice di servizio usato dal circuito di ExpressRoute nel modello di distribuzione classico.</span><span class="sxs-lookup"><span data-stu-id="565a0-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="565a0-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="565a0-127">-Tag</span></span>
<span data-ttu-id="565a0-128">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="565a0-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="565a0-129">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="565a0-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="565a0-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="565a0-130">-Confirm</span></span>
<span data-ttu-id="565a0-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="565a0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="565a0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="565a0-132">-WhatIf</span></span>
<span data-ttu-id="565a0-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="565a0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="565a0-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="565a0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="565a0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="565a0-135">CommonParameters</span></span>
<span data-ttu-id="565a0-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="565a0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="565a0-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="565a0-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="565a0-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="565a0-138">INPUTS</span></span>

### <span data-ttu-id="565a0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="565a0-139">System.String</span></span>

### <span data-ttu-id="565a0-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="565a0-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="565a0-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="565a0-141">OUTPUTS</span></span>

### <span data-ttu-id="565a0-142">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="565a0-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="565a0-143">Note</span><span class="sxs-lookup"><span data-stu-id="565a0-143">NOTES</span></span>

## <span data-ttu-id="565a0-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="565a0-144">RELATED LINKS</span></span>

[<span data-ttu-id="565a0-145">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="565a0-145">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="565a0-146">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="565a0-146">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="565a0-147">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="565a0-147">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="565a0-148">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="565a0-148">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)