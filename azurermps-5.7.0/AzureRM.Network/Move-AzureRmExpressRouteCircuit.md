---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/move-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: d0fb9fb0c6fb27ff683fcbb2b3ae537d736189cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515568"
---
# <span data-ttu-id="8dd0d-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8dd0d-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="8dd0d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8dd0d-102">SYNOPSIS</span></span>
<span data-ttu-id="8dd0d-103">Sposta un circuito ExpressRoute dal modello di distribuzione classico al modello di distribuzione di Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="8dd0d-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8dd0d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8dd0d-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dd0d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8dd0d-105">DESCRIPTION</span></span>
<span data-ttu-id="8dd0d-106">Il cmdlet **Move-AzureRmExpressRouteCircuit** sposta un circuito ExpressRoute dal modello di distribuzione classico al modello di distribuzione di Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="8dd0d-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="8dd0d-107">Dopo lo sviluppo, il circuito di ExpressRoute si comporta come qualsiasi altro circuito di ExpressRoute creato nel modello di distribuzione di Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="8dd0d-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="8dd0d-108">I collegamenti a circuiti, le reti virtuali e i gateway VPN non vengono spostati in questa operazione.</span><span class="sxs-lookup"><span data-stu-id="8dd0d-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="8dd0d-109">Queste risorse devono essere riconfigurate dopo lo sposta.</span><span class="sxs-lookup"><span data-stu-id="8dd0d-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="8dd0d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8dd0d-110">EXAMPLES</span></span>

### <span data-ttu-id="8dd0d-111">Esempio 1: trasferire un circuito di ExpressRoute nel modello di distribuzione di gestione risorse</span><span class="sxs-lookup"><span data-stu-id="8dd0d-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="8dd0d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8dd0d-112">PARAMETERS</span></span>

### <span data-ttu-id="8dd0d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8dd0d-113">-AsJob</span></span>
<span data-ttu-id="8dd0d-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8dd0d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8dd0d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dd0d-115">-DefaultProfile</span></span>
<span data-ttu-id="8dd0d-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8dd0d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8dd0d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8dd0d-117">-Force</span></span>
<span data-ttu-id="8dd0d-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8dd0d-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8dd0d-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8dd0d-119">-Location</span></span>
<span data-ttu-id="8dd0d-120">Nome della posizione di Azure in cui si trova il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8dd0d-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="8dd0d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8dd0d-121">-Name</span></span>
<span data-ttu-id="8dd0d-122">Il nome del circuito di ExpressRoute da spostare.</span><span class="sxs-lookup"><span data-stu-id="8dd0d-122">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="8dd0d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dd0d-123">-ResourceGroupName</span></span>
<span data-ttu-id="8dd0d-124">Nome del gruppo di risorse che conterrà il circuito ExpressRoute spostato.</span><span class="sxs-lookup"><span data-stu-id="8dd0d-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="8dd0d-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="8dd0d-125">-ServiceKey</span></span>
<span data-ttu-id="8dd0d-126">Il codice di servizio usato dal circuito di ExpressRoute nel modello di distribuzione classico.</span><span class="sxs-lookup"><span data-stu-id="8dd0d-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="8dd0d-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="8dd0d-127">-Tag</span></span>
<span data-ttu-id="8dd0d-128">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8dd0d-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8dd0d-129">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="8dd0d-129">For example:</span></span>

<span data-ttu-id="8dd0d-130">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8dd0d-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8dd0d-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8dd0d-131">-Confirm</span></span>
<span data-ttu-id="8dd0d-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dd0d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dd0d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dd0d-133">-WhatIf</span></span>
<span data-ttu-id="8dd0d-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8dd0d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dd0d-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8dd0d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dd0d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dd0d-136">CommonParameters</span></span>
<span data-ttu-id="8dd0d-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dd0d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dd0d-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dd0d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dd0d-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8dd0d-139">INPUTS</span></span>

### <span data-ttu-id="8dd0d-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8dd0d-140">None</span></span>
<span data-ttu-id="8dd0d-141">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="8dd0d-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8dd0d-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8dd0d-142">OUTPUTS</span></span>

### <span data-ttu-id="8dd0d-143">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8dd0d-143">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="8dd0d-144">Note</span><span class="sxs-lookup"><span data-stu-id="8dd0d-144">NOTES</span></span>

## <span data-ttu-id="8dd0d-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8dd0d-145">RELATED LINKS</span></span>

[<span data-ttu-id="8dd0d-146">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8dd0d-146">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="8dd0d-147">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8dd0d-147">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="8dd0d-148">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8dd0d-148">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="8dd0d-149">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8dd0d-149">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
