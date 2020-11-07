---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/move-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Move-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Move-AzExpressRouteCircuit.md
ms.openlocfilehash: ffa10dca752adaeebbdd6fbf92a6a16b094a3085
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860598"
---
# <span data-ttu-id="64777-101">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="64777-101">Move-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="64777-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64777-102">SYNOPSIS</span></span>
<span data-ttu-id="64777-103">Sposta un circuito ExpressRoute dal modello di distribuzione classico al modello di distribuzione di Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="64777-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

## <span data-ttu-id="64777-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64777-104">SYNTAX</span></span>

```
Move-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64777-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64777-105">DESCRIPTION</span></span>
<span data-ttu-id="64777-106">Il cmdlet **Move-AzExpressRouteCircuit** sposta un circuito ExpressRoute dal modello di distribuzione classico al modello di distribuzione di Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="64777-106">The **Move-AzExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="64777-107">Dopo lo sviluppo, il circuito di ExpressRoute si comporta come qualsiasi altro circuito di ExpressRoute creato nel modello di distribuzione di Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="64777-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="64777-108">I collegamenti a circuiti, le reti virtuali e i gateway VPN non vengono spostati in questa operazione.</span><span class="sxs-lookup"><span data-stu-id="64777-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="64777-109">Queste risorse devono essere riconfigurate dopo lo sposta.</span><span class="sxs-lookup"><span data-stu-id="64777-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="64777-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64777-110">EXAMPLES</span></span>

### <span data-ttu-id="64777-111">Esempio 1: trasferire un circuito di ExpressRoute nel modello di distribuzione di gestione risorse</span><span class="sxs-lookup"><span data-stu-id="64777-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="64777-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64777-112">PARAMETERS</span></span>

### <span data-ttu-id="64777-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64777-113">-AsJob</span></span>
<span data-ttu-id="64777-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="64777-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64777-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64777-115">-DefaultProfile</span></span>
<span data-ttu-id="64777-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64777-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64777-117">-Force</span><span class="sxs-lookup"><span data-stu-id="64777-117">-Force</span></span>
<span data-ttu-id="64777-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="64777-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="64777-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="64777-119">-Location</span></span>
<span data-ttu-id="64777-120">Nome della posizione di Azure in cui si trova il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="64777-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="64777-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="64777-121">-Name</span></span>
<span data-ttu-id="64777-122">Il nome del circuito di ExpressRoute da spostare.</span><span class="sxs-lookup"><span data-stu-id="64777-122">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="64777-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64777-123">-ResourceGroupName</span></span>
<span data-ttu-id="64777-124">Nome del gruppo di risorse che conterrà il circuito ExpressRoute spostato.</span><span class="sxs-lookup"><span data-stu-id="64777-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="64777-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="64777-125">-ServiceKey</span></span>
<span data-ttu-id="64777-126">Il codice di servizio usato dal circuito di ExpressRoute nel modello di distribuzione classico.</span><span class="sxs-lookup"><span data-stu-id="64777-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="64777-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="64777-127">-Tag</span></span>
<span data-ttu-id="64777-128">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="64777-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="64777-129">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="64777-129">For example:</span></span>

<span data-ttu-id="64777-130">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="64777-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="64777-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="64777-131">-Confirm</span></span>
<span data-ttu-id="64777-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64777-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64777-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64777-133">-WhatIf</span></span>
<span data-ttu-id="64777-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64777-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64777-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64777-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64777-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64777-136">CommonParameters</span></span>
<span data-ttu-id="64777-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64777-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64777-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64777-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64777-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64777-139">INPUTS</span></span>

## <span data-ttu-id="64777-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64777-140">OUTPUTS</span></span>

### <span data-ttu-id="64777-141">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="64777-141">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="64777-142">Note</span><span class="sxs-lookup"><span data-stu-id="64777-142">NOTES</span></span>

## <span data-ttu-id="64777-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64777-143">RELATED LINKS</span></span>

[<span data-ttu-id="64777-144">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="64777-144">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="64777-145">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="64777-145">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="64777-146">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="64777-146">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="64777-147">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="64777-147">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
