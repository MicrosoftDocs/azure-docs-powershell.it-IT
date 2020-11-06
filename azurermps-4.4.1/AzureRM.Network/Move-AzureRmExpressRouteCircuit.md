---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Move-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: e4d167f98f837434018e04da91a31973acb45c8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519115"
---
# <span data-ttu-id="d325d-101">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d325d-101">Move-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="d325d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d325d-102">SYNOPSIS</span></span>
<span data-ttu-id="d325d-103">Sposta un circuito ExpressRoute dal modello di distribuzione classico al modello di distribuzione di Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="d325d-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d325d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d325d-104">SYNTAX</span></span>

```
Move-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 -ServiceKey <String> [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d325d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d325d-105">DESCRIPTION</span></span>
<span data-ttu-id="d325d-106">Il cmdlet **Move-AzureRmExpressRouteCircuit** sposta un circuito ExpressRoute dal modello di distribuzione classico al modello di distribuzione di Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="d325d-106">The **Move-AzureRmExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="d325d-107">Dopo lo sviluppo, il circuito di ExpressRoute si comporta come qualsiasi altro circuito di ExpressRoute creato nel modello di distribuzione di Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="d325d-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="d325d-108">I collegamenti a circuiti, le reti virtuali e i gateway VPN non vengono spostati in questa operazione.</span><span class="sxs-lookup"><span data-stu-id="d325d-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="d325d-109">Queste risorse devono essere riconfigurate dopo lo sposta.</span><span class="sxs-lookup"><span data-stu-id="d325d-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="d325d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d325d-110">EXAMPLES</span></span>

### <span data-ttu-id="d325d-111">Esempio 1: trasferire un circuito di ExpressRoute nel modello di distribuzione di gestione risorse</span><span class="sxs-lookup"><span data-stu-id="d325d-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="d325d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d325d-112">PARAMETERS</span></span>

### <span data-ttu-id="d325d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d325d-113">-Force</span></span>
<span data-ttu-id="d325d-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d325d-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d325d-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d325d-115">-Location</span></span>
<span data-ttu-id="d325d-116">Nome della posizione di Azure in cui si trova il circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="d325d-116">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="d325d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d325d-117">-Name</span></span>
<span data-ttu-id="d325d-118">Il nome del circuito di ExpressRoute da spostare.</span><span class="sxs-lookup"><span data-stu-id="d325d-118">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="d325d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d325d-119">-ResourceGroupName</span></span>
<span data-ttu-id="d325d-120">Nome del gruppo di risorse che conterrà il circuito ExpressRoute spostato.</span><span class="sxs-lookup"><span data-stu-id="d325d-120">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="d325d-121">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="d325d-121">-ServiceKey</span></span>
<span data-ttu-id="d325d-122">Il codice di servizio usato dal circuito di ExpressRoute nel modello di distribuzione classico.</span><span class="sxs-lookup"><span data-stu-id="d325d-122">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="d325d-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="d325d-123">-Tag</span></span>
<span data-ttu-id="d325d-124">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d325d-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d325d-125">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="d325d-125">For example:</span></span>

<span data-ttu-id="d325d-126">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d325d-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d325d-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d325d-127">-Confirm</span></span>
<span data-ttu-id="d325d-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d325d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d325d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d325d-129">-WhatIf</span></span>
<span data-ttu-id="d325d-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d325d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d325d-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d325d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d325d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d325d-132">-DefaultProfile</span></span>
<span data-ttu-id="d325d-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d325d-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d325d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d325d-134">CommonParameters</span></span>
<span data-ttu-id="d325d-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d325d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d325d-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d325d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d325d-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d325d-137">INPUTS</span></span>

## <span data-ttu-id="d325d-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d325d-138">OUTPUTS</span></span>

### <span data-ttu-id="d325d-139">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d325d-139">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="d325d-140">Note</span><span class="sxs-lookup"><span data-stu-id="d325d-140">NOTES</span></span>

## <span data-ttu-id="d325d-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d325d-141">RELATED LINKS</span></span>

[<span data-ttu-id="d325d-142">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d325d-142">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d325d-143">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d325d-143">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d325d-144">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d325d-144">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d325d-145">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d325d-145">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
