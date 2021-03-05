---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: 94730c362ae9854179525212971dda5c2ad1feae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996433"
---
# <span data-ttu-id="2f8f8-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2f8f8-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="2f8f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f8f8-102">SYNOPSIS</span></span>
<span data-ttu-id="2f8f8-103">Rimuove un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2f8f8-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="2f8f8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2f8f8-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f8f8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2f8f8-105">DESCRIPTION</span></span>
<span data-ttu-id="2f8f8-106">Il cmdlet **Remove-AzExpressRouteCircuit** rimuove un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2f8f8-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="2f8f8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2f8f8-107">EXAMPLES</span></span>

### <span data-ttu-id="2f8f8-108">Esempio 1: Eliminare un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="2f8f8-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="2f8f8-109">Esempio 2: Eliminare un circuito ExpressRoute usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="2f8f8-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="2f8f8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f8f8-110">PARAMETERS</span></span>

### <span data-ttu-id="2f8f8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f8f8-111">-AsJob</span></span>
<span data-ttu-id="2f8f8-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2f8f8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f8f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f8f8-113">-DefaultProfile</span></span>
<span data-ttu-id="2f8f8-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2f8f8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f8f8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2f8f8-115">-Force</span></span>
<span data-ttu-id="2f8f8-116">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="2f8f8-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2f8f8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2f8f8-117">-Name</span></span>
<span data-ttu-id="2f8f8-118">Nome del circuito ExpressRoute da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="2f8f8-118">The name of the ExpressRoute circuit to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f8f8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f8f8-119">-PassThru</span></span>
<span data-ttu-id="2f8f8-120">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="2f8f8-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="2f8f8-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="2f8f8-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2f8f8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f8f8-122">-ResourceGroupName</span></span>
<span data-ttu-id="2f8f8-123">Specifica il nome del gruppo di risorse a cui appartiene questo circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2f8f8-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f8f8-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f8f8-124">-Confirm</span></span>
<span data-ttu-id="2f8f8-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f8f8-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f8f8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f8f8-126">-WhatIf</span></span>
<span data-ttu-id="2f8f8-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2f8f8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f8f8-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2f8f8-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f8f8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f8f8-129">CommonParameters</span></span>
<span data-ttu-id="2f8f8-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f8f8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f8f8-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f8f8-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f8f8-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="2f8f8-132">INPUTS</span></span>

### <span data-ttu-id="2f8f8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="2f8f8-133">System.String</span></span>

## <span data-ttu-id="2f8f8-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2f8f8-134">OUTPUTS</span></span>

### <span data-ttu-id="2f8f8-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2f8f8-135">System.Boolean</span></span>

## <span data-ttu-id="2f8f8-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="2f8f8-136">NOTES</span></span>

## <span data-ttu-id="2f8f8-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2f8f8-137">RELATED LINKS</span></span>

[<span data-ttu-id="2f8f8-138">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2f8f8-138">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="2f8f8-139">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2f8f8-139">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="2f8f8-140">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2f8f8-140">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="2f8f8-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2f8f8-141">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
