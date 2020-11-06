---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EDB94194-650C-4892-8DDC-E67D435522DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: dd47e858132dbe77556d82ce234d41bc2c990f6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516211"
---
# <span data-ttu-id="4491f-101">Remove-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4491f-101">Remove-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="4491f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4491f-102">SYNOPSIS</span></span>
<span data-ttu-id="4491f-103">Rimuove un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4491f-103">Removes an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4491f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4491f-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4491f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4491f-105">DESCRIPTION</span></span>
<span data-ttu-id="4491f-106">Il cmdlet **Remove-AzureRmExpressRouteCircuit** rimuove un circuito ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4491f-106">The **Remove-AzureRmExpressRouteCircuit** cmdlet removes an ExpressRoute circuit.</span></span>

## <span data-ttu-id="4491f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4491f-107">EXAMPLES</span></span>

### <span data-ttu-id="4491f-108">Esempio 1: eliminare un circuito ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="4491f-108">Example 1: Delete an ExpressRoute circuit</span></span>
```
Remove-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
```

### <span data-ttu-id="4491f-109">Esempio 2: eliminare un circuito ExpressRoute con la pipeline</span><span class="sxs-lookup"><span data-stu-id="4491f-109">Example 2: Delete an ExpressRoute circuit using the pipeline</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="4491f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4491f-110">PARAMETERS</span></span>

### <span data-ttu-id="4491f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="4491f-111">-Force</span></span>
<span data-ttu-id="4491f-112">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4491f-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4491f-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4491f-113">-Name</span></span>
<span data-ttu-id="4491f-114">Il nome del circuito di ExpressRoute da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="4491f-114">The name of the ExpressRoute circuit to be removed.</span></span>

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

### <span data-ttu-id="4491f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4491f-115">-PassThru</span></span>
<span data-ttu-id="4491f-116">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="4491f-116">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="4491f-117">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="4491f-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4491f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4491f-118">-ResourceGroupName</span></span>
<span data-ttu-id="4491f-119">Specifica il nome del gruppo di risorse a cui appartiene il circuito di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="4491f-119">Specifies the name of the resource group that this ExpressRoute circuit belongs to.</span></span>

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

### <span data-ttu-id="4491f-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4491f-120">-Confirm</span></span>
<span data-ttu-id="4491f-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4491f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4491f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4491f-122">-WhatIf</span></span>
<span data-ttu-id="4491f-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4491f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4491f-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4491f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4491f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4491f-125">-DefaultProfile</span></span>
<span data-ttu-id="4491f-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4491f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4491f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4491f-127">CommonParameters</span></span>
<span data-ttu-id="4491f-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4491f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4491f-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4491f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4491f-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4491f-130">INPUTS</span></span>

## <span data-ttu-id="4491f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4491f-131">OUTPUTS</span></span>

## <span data-ttu-id="4491f-132">Note</span><span class="sxs-lookup"><span data-stu-id="4491f-132">NOTES</span></span>

## <span data-ttu-id="4491f-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4491f-133">RELATED LINKS</span></span>

[<span data-ttu-id="4491f-134">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4491f-134">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="4491f-135">Move-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4491f-135">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="4491f-136">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4491f-136">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="4491f-137">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4491f-137">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
