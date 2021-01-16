---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 4309550557480211560e108489b14850672ee1f8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366841"
---
# <span data-ttu-id="c71de-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="c71de-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="c71de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c71de-102">SYNOPSIS</span></span>
<span data-ttu-id="c71de-103">Rimuove una configurazione di peering di ExpressRoute Cross Connection.</span><span class="sxs-lookup"><span data-stu-id="c71de-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="c71de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c71de-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c71de-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c71de-105">DESCRIPTION</span></span>
<span data-ttu-id="c71de-106">Il cmdlet **Remove-AzExpressRouteCrossConnectionPeering** rimuove una configurazione di peering di ExpressRoute Cross Connection.</span><span class="sxs-lookup"><span data-stu-id="c71de-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="c71de-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c71de-107">EXAMPLES</span></span>

### <span data-ttu-id="c71de-108">Esempio 1: rimuovere una configurazione peer da una connessione ExpressRoute incrociata</span><span class="sxs-lookup"><span data-stu-id="c71de-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="c71de-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c71de-109">PARAMETERS</span></span>

### <span data-ttu-id="c71de-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c71de-110">-DefaultProfile</span></span>
<span data-ttu-id="c71de-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c71de-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c71de-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c71de-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="c71de-113">La connessione ExpressRoute Cross contenente la configurazione peer da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c71de-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="c71de-114">-Force</span><span class="sxs-lookup"><span data-stu-id="c71de-114">-Force</span></span>
<span data-ttu-id="c71de-115">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="c71de-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c71de-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="c71de-116">-Name</span></span>
<span data-ttu-id="c71de-117">Nome della configurazione peer da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c71de-117">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="c71de-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="c71de-118">-PeerAddressType</span></span>
<span data-ttu-id="c71de-119">Famiglia di indirizzi del peering</span><span class="sxs-lookup"><span data-stu-id="c71de-119">The Address family of the peering</span></span>

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

### <span data-ttu-id="c71de-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c71de-120">-Confirm</span></span>
<span data-ttu-id="c71de-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c71de-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c71de-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c71de-122">-WhatIf</span></span>
<span data-ttu-id="c71de-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c71de-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c71de-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c71de-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c71de-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c71de-125">CommonParameters</span></span>
<span data-ttu-id="c71de-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c71de-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c71de-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c71de-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c71de-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c71de-128">INPUTS</span></span>

### <span data-ttu-id="c71de-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c71de-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="c71de-130">Il parametro ' ExpressRouteCrossConnection ' accetta il valore di tipo ' PSExpressRouteCrossConnection ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c71de-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="c71de-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c71de-131">OUTPUTS</span></span>

### <span data-ttu-id="c71de-132">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c71de-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="c71de-133">Note</span><span class="sxs-lookup"><span data-stu-id="c71de-133">NOTES</span></span>

## <span data-ttu-id="c71de-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c71de-134">RELATED LINKS</span></span>

[<span data-ttu-id="c71de-135">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="c71de-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="c71de-136">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="c71de-136">Get-AzExpressRouteCrossConnectionPeering</span></span>](./Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="c71de-137">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c71de-137">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="c71de-138">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c71de-138">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
