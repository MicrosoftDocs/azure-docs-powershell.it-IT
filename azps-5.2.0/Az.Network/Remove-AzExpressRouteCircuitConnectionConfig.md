---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 0e8a4eeaad1f033377ab11d7361d71c8a63a9dc2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366883"
---
# <span data-ttu-id="9f6d3-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="9f6d3-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="9f6d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9f6d3-102">SYNOPSIS</span></span>
<span data-ttu-id="9f6d3-103">Rimuove una configurazione della connessione a un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="9f6d3-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="9f6d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f6d3-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f6d3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f6d3-105">DESCRIPTION</span></span>
<span data-ttu-id="9f6d3-106">Il cmdlet **Remove-AzExpressRouteCircuitConnectionConfig** rimuove una configurazione di connessione circuitale ExpressRoute associata a un circuito di Route Express specifico.</span><span class="sxs-lookup"><span data-stu-id="9f6d3-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="9f6d3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f6d3-107">EXAMPLES</span></span>

### <span data-ttu-id="9f6d3-108">Esempio 1: rimuovere una configurazione della connessione Circuit da un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="9f6d3-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="9f6d3-109">Esempio 2: rimuovere una configurazione di connessione circuitale tramite piping da un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="9f6d3-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

### <span data-ttu-id="9f6d3-110">Esempio 3: rimuovere una configurazione della connessione Circuit da un circuito ExpressRoute per una famiglia di indirizzi specifica</span><span class="sxs-lookup"><span data-stu-id="9f6d3-110">Example 3: Remove a circuit connection configuration from an ExpressRoute circuit for a specific address family</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -AddressPrefixType IPv4
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="9f6d3-111">Esempio 4: rimuovere una configurazione di connessione circuitale tramite piping da un circuito ExpressRoute per una famiglia di indirizzi specifica</span><span class="sxs-lookup"><span data-stu-id="9f6d3-111">Example 4: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit for a specific address family</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -AddressPrefixType IPv6|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="9f6d3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9f6d3-112">PARAMETERS</span></span>

### <span data-ttu-id="9f6d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f6d3-113">-DefaultProfile</span></span>
<span data-ttu-id="9f6d3-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9f6d3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f6d3-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9f6d3-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="9f6d3-116">Il circuito ExpressRoute che contiene la configurazione peer da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="9f6d3-116">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f6d3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f6d3-117">-Name</span></span>
<span data-ttu-id="9f6d3-118">Nome della configurazione della connessione circuitale da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="9f6d3-118">The name of the circuit connection configuration to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="9f6d3-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="9f6d3-119">-AddressPrefixType</span></span>
<span data-ttu-id="9f6d3-120">Specifica la famiglia di indirizzi che deve essere rimossa dalla configurazione</span><span class="sxs-lookup"><span data-stu-id="9f6d3-120">Specifies the address family that needs to be removed from the config</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: IPv4 
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f6d3-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9f6d3-121">-Confirm</span></span>
<span data-ttu-id="9f6d3-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f6d3-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f6d3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f6d3-123">-WhatIf</span></span>
<span data-ttu-id="9f6d3-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9f6d3-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9f6d3-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9f6d3-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f6d3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f6d3-126">CommonParameters</span></span>
<span data-ttu-id="9f6d3-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f6d3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f6d3-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f6d3-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f6d3-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9f6d3-129">INPUTS</span></span>

### <span data-ttu-id="9f6d3-130">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9f6d3-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="9f6d3-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f6d3-131">OUTPUTS</span></span>

### <span data-ttu-id="9f6d3-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9f6d3-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="9f6d3-133">Note</span><span class="sxs-lookup"><span data-stu-id="9f6d3-133">NOTES</span></span>

## <span data-ttu-id="9f6d3-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f6d3-134">RELATED LINKS</span></span>

[<span data-ttu-id="9f6d3-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9f6d3-135">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="9f6d3-136">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="9f6d3-136">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="9f6d3-137">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="9f6d3-137">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="9f6d3-138">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="9f6d3-138">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="9f6d3-139">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="9f6d3-139">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="9f6d3-140">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9f6d3-140">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="9f6d3-141">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9f6d3-141">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)