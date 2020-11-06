---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 3ea8e43710d9e195218cc1b96a2656af2a7e2adf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511068"
---
# <span data-ttu-id="16005-101">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="16005-101">Remove-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="16005-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="16005-102">SYNOPSIS</span></span>
<span data-ttu-id="16005-103">Rimuove un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="16005-103">Removes an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16005-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16005-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16005-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16005-105">DESCRIPTION</span></span>
<span data-ttu-id="16005-106">Il cmdlet **Remove-AzureRmExpressRouteCircuit** rimuove un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="16005-106">The **Remove-AzureRmExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="16005-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16005-107">EXAMPLES</span></span>

### <span data-ttu-id="16005-108">Esempio 1: eliminare un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="16005-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="16005-109">Esempio 2: eliminare un circuito ExpressRoute con la pipeline</span><span class="sxs-lookup"><span data-stu-id="16005-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="16005-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="16005-110">PARAMETERS</span></span>

### <span data-ttu-id="16005-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16005-111">-AsJob</span></span>
<span data-ttu-id="16005-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="16005-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16005-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16005-113">-DefaultProfile</span></span>
<span data-ttu-id="16005-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16005-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16005-115">-Force</span><span class="sxs-lookup"><span data-stu-id="16005-115">-Force</span></span>
<span data-ttu-id="16005-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="16005-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="16005-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="16005-117">-Name</span></span>
<span data-ttu-id="16005-118">Il nome del circuito di ExpressRoute da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="16005-118">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="16005-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16005-119">-PassThru</span></span>
<span data-ttu-id="16005-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="16005-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="16005-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="16005-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="16005-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16005-122">-ResourceGroupName</span></span>
<span data-ttu-id="16005-123">Specifica il nome del gruppo di risorse a cui appartiene il circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="16005-123">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="16005-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="16005-124">-Confirm</span></span>
<span data-ttu-id="16005-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16005-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16005-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16005-126">-WhatIf</span></span>
<span data-ttu-id="16005-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16005-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16005-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16005-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16005-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16005-129">CommonParameters</span></span>
<span data-ttu-id="16005-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16005-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16005-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16005-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16005-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="16005-132">INPUTS</span></span>

### <span data-ttu-id="16005-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="16005-133">None</span></span>
<span data-ttu-id="16005-134">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="16005-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="16005-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16005-135">OUTPUTS</span></span>

## <span data-ttu-id="16005-136">Note</span><span class="sxs-lookup"><span data-stu-id="16005-136">NOTES</span></span>

## <span data-ttu-id="16005-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16005-137">RELATED LINKS</span></span>

[<span data-ttu-id="16005-138">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="16005-138">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="16005-139">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="16005-139">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="16005-140">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="16005-140">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="16005-141">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="16005-141">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
