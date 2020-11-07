---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: bf69b628224baa74014d75b4c687a15d830d13c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852785"
---
# <span data-ttu-id="26076-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="26076-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="26076-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26076-102">SYNOPSIS</span></span>
<span data-ttu-id="26076-103">Rimuove una configurazione della connessione a un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="26076-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="26076-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26076-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26076-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26076-105">DESCRIPTION</span></span>
<span data-ttu-id="26076-106">Il cmdlet **Remove-AzExpressRouteCircuitConnectionConfig** rimuove una configurazione di connessione circuitale ExpressRoute associata a un circuito di Route Express specifico.</span><span class="sxs-lookup"><span data-stu-id="26076-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="26076-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26076-107">EXAMPLES</span></span>

### <span data-ttu-id="26076-108">Esempio 1: rimuovere una configurazione della connessione Circuit da un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="26076-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="26076-109">Esempio 2: rimuovere una configurazione di connessione circuitale tramite piping da un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="26076-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="26076-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26076-110">PARAMETERS</span></span>

### <span data-ttu-id="26076-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26076-111">-DefaultProfile</span></span>
<span data-ttu-id="26076-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26076-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26076-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="26076-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="26076-114">Il circuito ExpressRoute che contiene la configurazione peer da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="26076-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="26076-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="26076-115">-Name</span></span>
<span data-ttu-id="26076-116">Nome della configurazione della connessione circuitale da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="26076-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="26076-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="26076-117">-Confirm</span></span>
<span data-ttu-id="26076-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26076-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26076-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26076-119">-WhatIf</span></span>
<span data-ttu-id="26076-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26076-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26076-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26076-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26076-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26076-122">CommonParameters</span></span>
<span data-ttu-id="26076-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26076-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26076-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26076-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26076-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26076-125">INPUTS</span></span>

### <span data-ttu-id="26076-126">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="26076-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="26076-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26076-127">OUTPUTS</span></span>

### <span data-ttu-id="26076-128">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="26076-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="26076-129">Note</span><span class="sxs-lookup"><span data-stu-id="26076-129">NOTES</span></span>

## <span data-ttu-id="26076-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26076-130">RELATED LINKS</span></span>

[<span data-ttu-id="26076-131">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="26076-131">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="26076-132">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="26076-132">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="26076-133">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="26076-133">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="26076-134">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="26076-134">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="26076-135">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="26076-135">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="26076-136">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="26076-136">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="26076-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="26076-137">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)