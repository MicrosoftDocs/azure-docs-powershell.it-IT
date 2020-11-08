---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 0e8a4eeaad1f033377ab11d7361d71c8a63a9dc2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192059"
---
# <span data-ttu-id="03007-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="03007-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="03007-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="03007-102">SYNOPSIS</span></span>
<span data-ttu-id="03007-103">Rimuove una configurazione della connessione a un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="03007-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="03007-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03007-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03007-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03007-105">DESCRIPTION</span></span>
<span data-ttu-id="03007-106">Il cmdlet **Remove-AzExpressRouteCircuitConnectionConfig** rimuove una configurazione di connessione circuitale ExpressRoute associata a un circuito di Route Express specifico.</span><span class="sxs-lookup"><span data-stu-id="03007-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="03007-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03007-107">EXAMPLES</span></span>

### <span data-ttu-id="03007-108">Esempio 1: rimuovere una configurazione della connessione Circuit da un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="03007-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="03007-109">Esempio 2: rimuovere una configurazione di connessione circuitale tramite piping da un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="03007-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

### <span data-ttu-id="03007-110">Esempio 3: rimuovere una configurazione della connessione Circuit da un circuito ExpressRoute per una famiglia di indirizzi specifica</span><span class="sxs-lookup"><span data-stu-id="03007-110">Example 3: Remove a circuit connection configuration from an ExpressRoute circuit for a specific address family</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -AddressPrefixType IPv4
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="03007-111">Esempio 4: rimuovere una configurazione di connessione circuitale tramite piping da un circuito ExpressRoute per una famiglia di indirizzi specifica</span><span class="sxs-lookup"><span data-stu-id="03007-111">Example 4: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit for a specific address family</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -AddressPrefixType IPv6|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="03007-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="03007-112">PARAMETERS</span></span>

### <span data-ttu-id="03007-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03007-113">-DefaultProfile</span></span>
<span data-ttu-id="03007-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="03007-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03007-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="03007-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="03007-116">Il circuito ExpressRoute che contiene la configurazione peer da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="03007-116">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="03007-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="03007-117">-Name</span></span>
<span data-ttu-id="03007-118">Nome della configurazione della connessione circuitale da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="03007-118">The name of the circuit connection configuration to be removed.</span></span>

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
### <span data-ttu-id="03007-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="03007-119">-AddressPrefixType</span></span>
<span data-ttu-id="03007-120">Specifica la famiglia di indirizzi che deve essere rimossa dalla configurazione</span><span class="sxs-lookup"><span data-stu-id="03007-120">Specifies the address family that needs to be removed from the config</span></span> 

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

### <span data-ttu-id="03007-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="03007-121">-Confirm</span></span>
<span data-ttu-id="03007-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03007-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03007-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03007-123">-WhatIf</span></span>
<span data-ttu-id="03007-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03007-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03007-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03007-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03007-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03007-126">CommonParameters</span></span>
<span data-ttu-id="03007-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03007-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03007-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03007-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03007-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="03007-129">INPUTS</span></span>

### <span data-ttu-id="03007-130">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="03007-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="03007-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03007-131">OUTPUTS</span></span>

### <span data-ttu-id="03007-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="03007-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="03007-133">Note</span><span class="sxs-lookup"><span data-stu-id="03007-133">NOTES</span></span>

## <span data-ttu-id="03007-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03007-134">RELATED LINKS</span></span>

[<span data-ttu-id="03007-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="03007-135">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="03007-136">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="03007-136">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="03007-137">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="03007-137">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="03007-138">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="03007-138">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="03007-139">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="03007-139">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="03007-140">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="03007-140">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="03007-141">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="03007-141">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)