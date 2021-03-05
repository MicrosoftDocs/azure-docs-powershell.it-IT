---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 9769a5506f528eb03d5e6d5a26340b961786c363
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963997"
---
# <span data-ttu-id="651c6-101">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="651c6-101">Set-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="651c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="651c6-102">SYNOPSIS</span></span>
<span data-ttu-id="651c6-103">Modifica una connessione incrociata ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="651c6-103">Modifies an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="651c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="651c6-104">SYNTAX</span></span>

### <span data-ttu-id="651c6-105">ModifyByCircuitReference</span><span class="sxs-lookup"><span data-stu-id="651c6-105">ModifyByCircuitReference</span></span>
```
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="651c6-106">ModifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="651c6-106">ModifyByParameterValues</span></span>
```
Set-AzExpressRouteCrossConnection -ResourceGroupName <String> -Name <String>
 [-ServiceProviderProvisioningState <String>] [-ServiceProviderNotes <String>]
 [-Peerings <PSExpressRouteCrossConnectionPeering[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="651c6-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="651c6-107">DESCRIPTION</span></span>
<span data-ttu-id="651c6-108">Il cmdlet **Set-AzExpressRouteCrossConnection** salva la connessione incrociata ExpressRoute modificata ad Azure.</span><span class="sxs-lookup"><span data-stu-id="651c6-108">The **Set-AzExpressRouteCrossConnection** cmdlet saves the modified ExpressRoute cross connection to Azure.</span></span>

## <span data-ttu-id="651c6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="651c6-109">EXAMPLES</span></span>

### <span data-ttu-id="651c6-110">Esempio 1: Modificare lo stato di provisioning del provider di servizi di una connessione incrociata ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="651c6-110">Example 1: Change the Service Provider Provisioning State of an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$cc.ServiceProviderProvisioningState = 'Provisioned'
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="651c6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="651c6-111">PARAMETERS</span></span>

### <span data-ttu-id="651c6-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="651c6-112">-AsJob</span></span>
<span data-ttu-id="651c6-113">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="651c6-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="651c6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="651c6-114">-DefaultProfile</span></span>
<span data-ttu-id="651c6-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="651c6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="651c6-116">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="651c6-116">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="651c6-117">Specifica **l'oggetto ExpressRouteCrossConnection** modificato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="651c6-117">Specifies the **ExpressRouteCrossConnection** object that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: ModifyByCircuitReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="651c6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="651c6-118">-Force</span></span>
<span data-ttu-id="651c6-119">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="651c6-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="651c6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="651c6-120">-Name</span></span>
<span data-ttu-id="651c6-121">Nome della connessione incrociata Express Route.</span><span class="sxs-lookup"><span data-stu-id="651c6-121">The name of express route cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="651c6-122">-Peering</span><span class="sxs-lookup"><span data-stu-id="651c6-122">-Peerings</span></span>
<span data-ttu-id="651c6-123">Elenco di peering per la connessione incrociata</span><span class="sxs-lookup"><span data-stu-id="651c6-123">The list of peerings for the cross connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionPeering[]
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="651c6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="651c6-124">-ResourceGroupName</span></span>
<span data-ttu-id="651c6-125">The ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="651c6-125">The ExpressRouteCrossConnection</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="651c6-126">-ServiceProviderNotes</span><span class="sxs-lookup"><span data-stu-id="651c6-126">-ServiceProviderNotes</span></span>
<span data-ttu-id="651c6-127">Note del provider di servizi</span><span class="sxs-lookup"><span data-stu-id="651c6-127">The service provider notes</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="651c6-128">-ServiceProviderProvisioningState</span><span class="sxs-lookup"><span data-stu-id="651c6-128">-ServiceProviderProvisioningState</span></span>
<span data-ttu-id="651c6-129">Stato di provisioning del provider di servizi da impostare</span><span class="sxs-lookup"><span data-stu-id="651c6-129">The service provider provisioning state to be set</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="651c6-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="651c6-130">-Confirm</span></span>
<span data-ttu-id="651c6-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="651c6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="651c6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="651c6-132">-WhatIf</span></span>
<span data-ttu-id="651c6-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="651c6-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="651c6-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="651c6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="651c6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="651c6-135">CommonParameters</span></span>
<span data-ttu-id="651c6-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="651c6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="651c6-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="651c6-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="651c6-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="651c6-138">INPUTS</span></span>

### <span data-ttu-id="651c6-139">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="651c6-139">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="651c6-140">Il parametro 'ExpressRouteCrossConnection' accetta il valore di tipo 'PSExpressRouteCrossConnection' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="651c6-140">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="651c6-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="651c6-141">OUTPUTS</span></span>

### <span data-ttu-id="651c6-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="651c6-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="651c6-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="651c6-143">NOTES</span></span>

## <span data-ttu-id="651c6-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="651c6-144">RELATED LINKS</span></span>

[<span data-ttu-id="651c6-145">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="651c6-145">Get-AzExpressRouteCrossConnection</span></span>](./Get-AzExpressRouteCrossConnection.md)
