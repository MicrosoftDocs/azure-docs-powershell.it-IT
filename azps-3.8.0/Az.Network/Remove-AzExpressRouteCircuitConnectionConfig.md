---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: b01e0ecb48a5a4c27fc79448ca0e4d71e820d292
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022026"
---
# <span data-ttu-id="b7bab-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b7bab-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="b7bab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7bab-102">SYNOPSIS</span></span>
<span data-ttu-id="b7bab-103">Rimuove una configurazione della connessione a un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="b7bab-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="b7bab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7bab-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7bab-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7bab-105">DESCRIPTION</span></span>
<span data-ttu-id="b7bab-106">Il cmdlet **Remove-AzExpressRouteCircuitConnectionConfig** rimuove una configurazione di connessione circuitale ExpressRoute associata a un circuito di Route Express specifico.</span><span class="sxs-lookup"><span data-stu-id="b7bab-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="b7bab-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7bab-107">EXAMPLES</span></span>

### <span data-ttu-id="b7bab-108">Esempio 1: rimuovere una configurazione della connessione Circuit da un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="b7bab-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="b7bab-109">Esempio 2: rimuovere una configurazione di connessione circuitale tramite piping da un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="b7bab-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="b7bab-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7bab-110">PARAMETERS</span></span>

### <span data-ttu-id="b7bab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7bab-111">-DefaultProfile</span></span>
<span data-ttu-id="b7bab-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7bab-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7bab-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b7bab-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="b7bab-114">Il circuito ExpressRoute che contiene la configurazione peer da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b7bab-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="b7bab-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7bab-115">-Name</span></span>
<span data-ttu-id="b7bab-116">Nome della configurazione della connessione circuitale da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b7bab-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="b7bab-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b7bab-117">-Confirm</span></span>
<span data-ttu-id="b7bab-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7bab-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7bab-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7bab-119">-WhatIf</span></span>
<span data-ttu-id="b7bab-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7bab-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7bab-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7bab-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7bab-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7bab-122">CommonParameters</span></span>
<span data-ttu-id="b7bab-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7bab-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7bab-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7bab-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7bab-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7bab-125">INPUTS</span></span>

### <span data-ttu-id="b7bab-126">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b7bab-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b7bab-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7bab-127">OUTPUTS</span></span>

### <span data-ttu-id="b7bab-128">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b7bab-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b7bab-129">Note</span><span class="sxs-lookup"><span data-stu-id="b7bab-129">NOTES</span></span>

## <span data-ttu-id="b7bab-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7bab-130">RELATED LINKS</span></span>

[<span data-ttu-id="b7bab-131">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b7bab-131">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="b7bab-132">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b7bab-132">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="b7bab-133">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b7bab-133">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="b7bab-134">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b7bab-134">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="b7bab-135">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b7bab-135">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="b7bab-136">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b7bab-136">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="b7bab-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b7bab-137">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)