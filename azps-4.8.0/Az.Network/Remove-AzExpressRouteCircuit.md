---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuit.md
ms.openlocfilehash: bc77c5d133561984f388e378f13595b3a72af785
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192752"
---
# <span data-ttu-id="41583-101">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="41583-101">Remove-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="41583-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="41583-102">SYNOPSIS</span></span>
<span data-ttu-id="41583-103">Rimuove un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="41583-103">Removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="41583-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41583-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41583-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41583-105">DESCRIPTION</span></span>
<span data-ttu-id="41583-106">Il cmdlet **Remove-AzExpressRouteCircuit** rimuove un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="41583-106">The **Remove-AzExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="41583-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41583-107">EXAMPLES</span></span>

### <span data-ttu-id="41583-108">Esempio 1: eliminare un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="41583-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="41583-109">Esempio 2: eliminare un circuito ExpressRoute con la pipeline</span><span class="sxs-lookup"><span data-stu-id="41583-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzExpressRouteCircuit
```

## <span data-ttu-id="41583-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="41583-110">PARAMETERS</span></span>

### <span data-ttu-id="41583-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41583-111">-AsJob</span></span>
<span data-ttu-id="41583-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="41583-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41583-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41583-113">-DefaultProfile</span></span>
<span data-ttu-id="41583-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="41583-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41583-115">-Force</span><span class="sxs-lookup"><span data-stu-id="41583-115">-Force</span></span>
<span data-ttu-id="41583-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="41583-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="41583-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="41583-117">-Name</span></span>
<span data-ttu-id="41583-118">Il nome del circuito di ExpressRoute da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="41583-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="41583-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41583-119">-PassThru</span></span>
<span data-ttu-id="41583-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="41583-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="41583-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="41583-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="41583-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41583-122">-ResourceGroupName</span></span>
<span data-ttu-id="41583-123">Specifica il nome del gruppo di risorse a cui appartiene il circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="41583-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="41583-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="41583-124">-Confirm</span></span>
<span data-ttu-id="41583-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41583-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41583-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41583-126">-WhatIf</span></span>
<span data-ttu-id="41583-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41583-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41583-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41583-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41583-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41583-129">CommonParameters</span></span>
<span data-ttu-id="41583-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41583-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41583-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41583-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41583-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="41583-132">INPUTS</span></span>

### <span data-ttu-id="41583-133">System. String</span><span class="sxs-lookup"><span data-stu-id="41583-133">System.String</span></span>

## <span data-ttu-id="41583-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41583-134">OUTPUTS</span></span>

### <span data-ttu-id="41583-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="41583-135">System.Boolean</span></span>

## <span data-ttu-id="41583-136">Note</span><span class="sxs-lookup"><span data-stu-id="41583-136">NOTES</span></span>

## <span data-ttu-id="41583-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41583-137">RELATED LINKS</span></span>

[<span data-ttu-id="41583-138">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="41583-138">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="41583-139">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="41583-139">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="41583-140">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="41583-140">New-AzExpressRouteCircuit</span></span>](New-AzExpressRouteCircuit.md)

[<span data-ttu-id="41583-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="41583-141">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)