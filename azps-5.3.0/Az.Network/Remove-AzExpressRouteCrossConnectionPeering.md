---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 4309550557480211560e108489b14850672ee1f8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475896"
---
# <span data-ttu-id="6fdd1-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="6fdd1-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="6fdd1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6fdd1-102">SYNOPSIS</span></span>
<span data-ttu-id="6fdd1-103">Rimuove una configurazione di peering di ExpressRoute Cross Connection.</span><span class="sxs-lookup"><span data-stu-id="6fdd1-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="6fdd1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6fdd1-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fdd1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6fdd1-105">DESCRIPTION</span></span>
<span data-ttu-id="6fdd1-106">Il cmdlet **Remove-AzExpressRouteCrossConnectionPeering** rimuove una configurazione di peering di ExpressRoute Cross Connection.</span><span class="sxs-lookup"><span data-stu-id="6fdd1-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="6fdd1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6fdd1-107">EXAMPLES</span></span>

### <span data-ttu-id="6fdd1-108">Esempio 1: rimuovere una configurazione peer da una connessione ExpressRoute incrociata</span><span class="sxs-lookup"><span data-stu-id="6fdd1-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="6fdd1-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6fdd1-109">PARAMETERS</span></span>

### <span data-ttu-id="6fdd1-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fdd1-110">-DefaultProfile</span></span>
<span data-ttu-id="6fdd1-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6fdd1-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fdd1-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="6fdd1-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="6fdd1-113">La connessione ExpressRoute Cross contenente la configurazione peer da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6fdd1-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fdd1-114">-Force</span><span class="sxs-lookup"><span data-stu-id="6fdd1-114">-Force</span></span>
<span data-ttu-id="6fdd1-115">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="6fdd1-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="6fdd1-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="6fdd1-116">-Name</span></span>
<span data-ttu-id="6fdd1-117">Nome della configurazione peer da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6fdd1-117">The name of the peering configuration to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fdd1-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="6fdd1-118">-PeerAddressType</span></span>
<span data-ttu-id="6fdd1-119">Famiglia di indirizzi del peering</span><span class="sxs-lookup"><span data-stu-id="6fdd1-119">The Address family of the peering</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fdd1-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6fdd1-120">-Confirm</span></span>
<span data-ttu-id="6fdd1-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fdd1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fdd1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fdd1-122">-WhatIf</span></span>
<span data-ttu-id="6fdd1-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6fdd1-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6fdd1-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6fdd1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fdd1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fdd1-125">CommonParameters</span></span>
<span data-ttu-id="6fdd1-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fdd1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fdd1-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fdd1-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fdd1-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6fdd1-128">INPUTS</span></span>

### <span data-ttu-id="6fdd1-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="6fdd1-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="6fdd1-130">Il parametro ' ExpressRouteCrossConnection ' accetta il valore di tipo ' PSExpressRouteCrossConnection ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="6fdd1-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="6fdd1-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6fdd1-131">OUTPUTS</span></span>

### <span data-ttu-id="6fdd1-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="6fdd1-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="6fdd1-133">Note</span><span class="sxs-lookup"><span data-stu-id="6fdd1-133">NOTES</span></span>

## <span data-ttu-id="6fdd1-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6fdd1-134">RELATED LINKS</span></span>

[<span data-ttu-id="6fdd1-135">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="6fdd1-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="6fdd1-136">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="6fdd1-136">Get-AzExpressRouteCrossConnectionPeering</span></span>](./Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="6fdd1-137">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="6fdd1-137">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="6fdd1-138">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="6fdd1-138">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
