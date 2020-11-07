---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/move-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: bd4d51c03d26a1fb99b04c8b5245850512c2c940
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866267"
---
# <span data-ttu-id="efada-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="efada-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="efada-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="efada-102">SYNOPSIS</span></span>
<span data-ttu-id="efada-103">Sposta un circuito ExpressRoute dal modello di distribuzione classico al modello di distribuzione di Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="efada-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efada-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="efada-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efada-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="efada-105">DESCRIPTION</span></span>
<span data-ttu-id="efada-106">Il cmdlet **Move-AzureRmExpressRouteCircuit** sposta un circuito ExpressRoute dal modello di distribuzione classico al modello di distribuzione di Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="efada-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="efada-107">Dopo lo sviluppo, il circuito di ExpressRoute si comporta come qualsiasi altro circuito di ExpressRoute creato nel modello di distribuzione di Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="efada-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="efada-108">I collegamenti a circuiti, le reti virtuali e i gateway VPN non vengono spostati in questa operazione.</span><span class="sxs-lookup"><span data-stu-id="efada-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="efada-109">Queste risorse devono essere riconfigurate dopo lo sposta.</span><span class="sxs-lookup"><span data-stu-id="efada-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="efada-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="efada-110">EXAMPLES</span></span>

### <span data-ttu-id="efada-111">Esempio 1: trasferire un circuito di ExpressRoute nel modello di distribuzione di gestione risorse</span><span class="sxs-lookup"><span data-stu-id="efada-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="efada-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="efada-112">PARAMETERS</span></span>

### <span data-ttu-id="efada-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="efada-113">-AsJob</span></span>
<span data-ttu-id="efada-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="efada-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="efada-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efada-115">-DefaultProfile</span></span>
<span data-ttu-id="efada-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="efada-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efada-117">-Force</span><span class="sxs-lookup"><span data-stu-id="efada-117">-Force</span></span>
<span data-ttu-id="efada-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="efada-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="efada-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="efada-119">-Location</span></span>
<span data-ttu-id="efada-120">Nome della posizione di Azure in cui si trova il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="efada-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="efada-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="efada-121">-Name</span></span>
<span data-ttu-id="efada-122">Il nome del circuito di ExpressRoute da spostare.</span><span class="sxs-lookup"><span data-stu-id="efada-122">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="efada-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efada-123">-ResourceGroupName</span></span>
<span data-ttu-id="efada-124">Nome del gruppo di risorse che conterrà il circuito ExpressRoute spostato.</span><span class="sxs-lookup"><span data-stu-id="efada-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="efada-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="efada-125">-ServiceKey</span></span>
<span data-ttu-id="efada-126">Il codice di servizio usato dal circuito di ExpressRoute nel modello di distribuzione classico.</span><span class="sxs-lookup"><span data-stu-id="efada-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="efada-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="efada-127">-Tag</span></span>
<span data-ttu-id="efada-128">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="efada-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="efada-129">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="efada-129">For example:</span></span>

<span data-ttu-id="efada-130">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="efada-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="efada-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="efada-131">-Confirm</span></span>
<span data-ttu-id="efada-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efada-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efada-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efada-133">-WhatIf</span></span>
<span data-ttu-id="efada-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="efada-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efada-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="efada-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efada-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efada-136">CommonParameters</span></span>
<span data-ttu-id="efada-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efada-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efada-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efada-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efada-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="efada-139">INPUTS</span></span>

## <span data-ttu-id="efada-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="efada-140">OUTPUTS</span></span>

### <span data-ttu-id="efada-141">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="efada-141">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="efada-142">Note</span><span class="sxs-lookup"><span data-stu-id="efada-142">NOTES</span></span>

## <span data-ttu-id="efada-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="efada-143">RELATED LINKS</span></span>

[<span data-ttu-id="efada-144">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="efada-144">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="efada-145">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="efada-145">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="efada-146">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="efada-146">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="efada-147">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="efada-147">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
