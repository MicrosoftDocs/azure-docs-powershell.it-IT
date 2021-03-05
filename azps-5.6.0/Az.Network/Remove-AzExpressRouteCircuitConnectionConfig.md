---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 0fdcf052f366572f0fe90a47452d65972caf573c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996406"
---
# <span data-ttu-id="8746f-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8746f-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="8746f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8746f-102">SYNOPSIS</span></span>
<span data-ttu-id="8746f-103">Rimuove una configurazione di connessione del circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="8746f-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="8746f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8746f-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8746f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8746f-105">DESCRIPTION</span></span>
<span data-ttu-id="8746f-106">Il cmdlet **Remove-AzExpressRouteCircuitConnectionConfig** rimuove una configurazione di connessione al circuito ExpressRoute associata a un determinato circuito Express Route.</span><span class="sxs-lookup"><span data-stu-id="8746f-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="8746f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8746f-107">EXAMPLES</span></span>

### <span data-ttu-id="8746f-108">Esempio 1: Rimuovere una configurazione di connessione a un circuito da un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="8746f-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="8746f-109">Esempio 2: Rimuovere una configurazione di connessione a un circuito tramite Piping da un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="8746f-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

### <span data-ttu-id="8746f-110">Esempio 3: Rimuovere una configurazione di connessione a un circuito ExpressRoute per una famiglia di indirizzi specifica</span><span class="sxs-lookup"><span data-stu-id="8746f-110">Example 3: Remove a circuit connection configuration from an ExpressRoute circuit for a specific address family</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -AddressPrefixType IPv4
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="8746f-111">Esempio 4: Rimuovere la configurazione di una connessione a un circuito tramite Piping da un circuito ExpressRoute per una famiglia di indirizzi specifica</span><span class="sxs-lookup"><span data-stu-id="8746f-111">Example 4: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit for a specific address family</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -AddressPrefixType IPv6|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="8746f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8746f-112">PARAMETERS</span></span>

### <span data-ttu-id="8746f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8746f-113">-DefaultProfile</span></span>
<span data-ttu-id="8746f-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8746f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8746f-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8746f-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="8746f-116">Circuito ExpressRoute contenente la configurazione di peering da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8746f-116">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="8746f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8746f-117">-Name</span></span>
<span data-ttu-id="8746f-118">Nome della configurazione della connessione al circuito da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8746f-118">The name of the circuit connection configuration to be removed.</span></span>

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
### <span data-ttu-id="8746f-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="8746f-119">-AddressPrefixType</span></span>
<span data-ttu-id="8746f-120">Specifica la famiglia di indirizzi che deve essere rimossa dalla configurazione</span><span class="sxs-lookup"><span data-stu-id="8746f-120">Specifies the address family that needs to be removed from the config</span></span> 

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

### <span data-ttu-id="8746f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8746f-121">-Confirm</span></span>
<span data-ttu-id="8746f-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8746f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8746f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8746f-123">-WhatIf</span></span>
<span data-ttu-id="8746f-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8746f-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8746f-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8746f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8746f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8746f-126">CommonParameters</span></span>
<span data-ttu-id="8746f-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8746f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8746f-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8746f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8746f-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="8746f-129">INPUTS</span></span>

### <span data-ttu-id="8746f-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8746f-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="8746f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8746f-131">OUTPUTS</span></span>

### <span data-ttu-id="8746f-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8746f-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="8746f-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="8746f-133">NOTES</span></span>

## <span data-ttu-id="8746f-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8746f-134">RELATED LINKS</span></span>

[<span data-ttu-id="8746f-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8746f-135">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="8746f-136">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8746f-136">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="8746f-137">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8746f-137">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="8746f-138">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8746f-138">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="8746f-139">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8746f-139">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="8746f-140">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8746f-140">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="8746f-141">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8746f-141">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)