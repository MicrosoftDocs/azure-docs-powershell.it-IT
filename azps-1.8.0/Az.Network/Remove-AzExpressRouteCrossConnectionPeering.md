---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: b991b26d8d6fc7a7cfd33ab051619b7192ae0aec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678133"
---
# <span data-ttu-id="e1a15-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="e1a15-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="e1a15-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e1a15-102">SYNOPSIS</span></span>
<span data-ttu-id="e1a15-103">Rimuove una configurazione di peering di ExpressRoute Cross Connection.</span><span class="sxs-lookup"><span data-stu-id="e1a15-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="e1a15-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1a15-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1a15-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1a15-105">DESCRIPTION</span></span>
<span data-ttu-id="e1a15-106">Il cmdlet **Remove-AzExpressRouteCrossConnectionPeering** rimuove una configurazione di peering di ExpressRoute Cross Connection.</span><span class="sxs-lookup"><span data-stu-id="e1a15-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="e1a15-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1a15-107">EXAMPLES</span></span>

### <span data-ttu-id="e1a15-108">Esempio 1: rimuovere una configurazione peer da una connessione ExpressRoute incrociata</span><span class="sxs-lookup"><span data-stu-id="e1a15-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="e1a15-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e1a15-109">PARAMETERS</span></span>

### <span data-ttu-id="e1a15-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1a15-110">-DefaultProfile</span></span>
<span data-ttu-id="e1a15-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1a15-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1a15-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="e1a15-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="e1a15-113">La connessione ExpressRoute Cross contenente la configurazione peer da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e1a15-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="e1a15-114">-Force</span><span class="sxs-lookup"><span data-stu-id="e1a15-114">-Force</span></span>
<span data-ttu-id="e1a15-115">Non chiedere conferma se si vuole usare una risorsa per un sovrarito</span><span class="sxs-lookup"><span data-stu-id="e1a15-115">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="e1a15-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="e1a15-116">-Name</span></span>
<span data-ttu-id="e1a15-117">Nome della configurazione peer da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e1a15-117">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="e1a15-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="e1a15-118">-PeerAddressType</span></span>
<span data-ttu-id="e1a15-119">Famiglia di indirizzi del peering</span><span class="sxs-lookup"><span data-stu-id="e1a15-119">The Address family of the peering</span></span>

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

### <span data-ttu-id="e1a15-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e1a15-120">-Confirm</span></span>
<span data-ttu-id="e1a15-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1a15-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1a15-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1a15-122">-WhatIf</span></span>
<span data-ttu-id="e1a15-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1a15-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1a15-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1a15-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1a15-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1a15-125">CommonParameters</span></span>
<span data-ttu-id="e1a15-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1a15-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1a15-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1a15-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1a15-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e1a15-128">INPUTS</span></span>

### <span data-ttu-id="e1a15-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="e1a15-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="e1a15-130">Il parametro ' ExpressRouteCrossConnection ' accetta il valore di tipo ' PSExpressRouteCrossConnection ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="e1a15-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="e1a15-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1a15-131">OUTPUTS</span></span>

### <span data-ttu-id="e1a15-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="e1a15-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="e1a15-133">Note</span><span class="sxs-lookup"><span data-stu-id="e1a15-133">NOTES</span></span>

## <span data-ttu-id="e1a15-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1a15-134">RELATED LINKS</span></span>

[<span data-ttu-id="e1a15-135">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="e1a15-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="e1a15-136">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="e1a15-136">Get-AzExpressRouteCrossConnectionPeering</span></span>](New-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="e1a15-137">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="e1a15-137">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="e1a15-138">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="e1a15-138">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
