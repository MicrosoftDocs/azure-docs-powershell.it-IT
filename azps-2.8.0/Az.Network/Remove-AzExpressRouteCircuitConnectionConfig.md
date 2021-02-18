---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: c596dffcef97dfbb1cabbc5ca2c2455a7768c25f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409937"
---
# <span data-ttu-id="285d6-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="285d6-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="285d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="285d6-102">SYNOPSIS</span></span>
<span data-ttu-id="285d6-103">Rimuove una configurazione di connessione del circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="285d6-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="285d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="285d6-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="285d6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="285d6-105">DESCRIPTION</span></span>
<span data-ttu-id="285d6-106">Il cmdlet **Remove-AzExpressRouteCircuitConnectionConfig** rimuove una configurazione di connessione al circuito ExpressRoute associata a un determinato circuito Express Route.</span><span class="sxs-lookup"><span data-stu-id="285d6-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="285d6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="285d6-107">EXAMPLES</span></span>

### <span data-ttu-id="285d6-108">Esempio 1: Rimuovere una configurazione di connessione a un circuito da un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="285d6-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="285d6-109">Esempio 2: Rimuovere una configurazione di connessione a un circuito tramite Piping da un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="285d6-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="285d6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="285d6-110">PARAMETERS</span></span>

### <span data-ttu-id="285d6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="285d6-111">-DefaultProfile</span></span>
<span data-ttu-id="285d6-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="285d6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="285d6-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="285d6-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="285d6-114">Circuito ExpressRoute contenente la configurazione di peering da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="285d6-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="285d6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="285d6-115">-Name</span></span>
<span data-ttu-id="285d6-116">Nome della configurazione della connessione al circuito da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="285d6-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="285d6-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="285d6-117">-Confirm</span></span>
<span data-ttu-id="285d6-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="285d6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="285d6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="285d6-119">-WhatIf</span></span>
<span data-ttu-id="285d6-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="285d6-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="285d6-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="285d6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="285d6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="285d6-122">CommonParameters</span></span>
<span data-ttu-id="285d6-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="285d6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="285d6-124">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="285d6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="285d6-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="285d6-125">INPUTS</span></span>

### <span data-ttu-id="285d6-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="285d6-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="285d6-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="285d6-127">OUTPUTS</span></span>

### <span data-ttu-id="285d6-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="285d6-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="285d6-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="285d6-129">NOTES</span></span>

## <span data-ttu-id="285d6-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="285d6-130">RELATED LINKS</span></span>

[<span data-ttu-id="285d6-131">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="285d6-131">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="285d6-132">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="285d6-132">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="285d6-133">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="285d6-133">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)





[<span data-ttu-id="285d6-134">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="285d6-134">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="285d6-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="285d6-135">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
