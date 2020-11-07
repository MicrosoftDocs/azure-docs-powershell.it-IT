---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: e9a93b66f62f6a42ba400dd84b6890cdf9f81cec
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865749"
---
# <span data-ttu-id="c420d-101">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c420d-101">Remove-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="c420d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c420d-102">SYNOPSIS</span></span>
<span data-ttu-id="c420d-103">Rimuove un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c420d-103">Removes an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c420d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c420d-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c420d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c420d-105">DESCRIPTION</span></span>
<span data-ttu-id="c420d-106">Il cmdlet **Remove-AzureRmExpressRouteCircuit** rimuove un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c420d-106">The **Remove-AzureRmExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="c420d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c420d-107">EXAMPLES</span></span>

### <span data-ttu-id="c420d-108">Esempio 1: eliminare un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="c420d-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="c420d-109">Esempio 2: eliminare un circuito ExpressRoute con la pipeline</span><span class="sxs-lookup"><span data-stu-id="c420d-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="c420d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c420d-110">PARAMETERS</span></span>

### <span data-ttu-id="c420d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c420d-111">-AsJob</span></span>
<span data-ttu-id="c420d-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c420d-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c420d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c420d-113">-DefaultProfile</span></span>
<span data-ttu-id="c420d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c420d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c420d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c420d-115">-Force</span></span>
<span data-ttu-id="c420d-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c420d-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c420d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c420d-117">-Name</span></span>
<span data-ttu-id="c420d-118">Il nome del circuito di ExpressRoute da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c420d-118">The name of the ExpressRoute circuit to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c420d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c420d-119">-PassThru</span></span>
<span data-ttu-id="c420d-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="c420d-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="c420d-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="c420d-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c420d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c420d-122">-ResourceGroupName</span></span>
<span data-ttu-id="c420d-123">Specifica il nome del gruppo di risorse a cui appartiene il circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="c420d-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c420d-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c420d-124">-Confirm</span></span>
<span data-ttu-id="c420d-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c420d-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c420d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c420d-126">-WhatIf</span></span>
<span data-ttu-id="c420d-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c420d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c420d-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c420d-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c420d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c420d-129">CommonParameters</span></span>
<span data-ttu-id="c420d-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c420d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c420d-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c420d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c420d-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c420d-132">INPUTS</span></span>

## <span data-ttu-id="c420d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c420d-133">OUTPUTS</span></span>

## <span data-ttu-id="c420d-134">Note</span><span class="sxs-lookup"><span data-stu-id="c420d-134">NOTES</span></span>

## <span data-ttu-id="c420d-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c420d-135">RELATED LINKS</span></span>

[<span data-ttu-id="c420d-136">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c420d-136">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="c420d-137">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c420d-137">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="c420d-138">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c420d-138">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="c420d-139">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="c420d-139">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
