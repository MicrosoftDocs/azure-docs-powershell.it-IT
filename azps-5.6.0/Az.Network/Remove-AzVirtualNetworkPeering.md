---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: f47b1bcc571337de8a64c591383367568cf7d67e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993522"
---
# <span data-ttu-id="e969e-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e969e-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="e969e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e969e-102">SYNOPSIS</span></span>
<span data-ttu-id="e969e-103">Rimuove il peering di una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e969e-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="e969e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e969e-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e969e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e969e-105">DESCRIPTION</span></span>
<span data-ttu-id="e969e-106">Rimuove il peering di una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e969e-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="e969e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e969e-107">EXAMPLES</span></span>

### <span data-ttu-id="e969e-108">Esempio 1: Rimuovere il peering di una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="e969e-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="e969e-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e969e-109">PARAMETERS</span></span>

### <span data-ttu-id="e969e-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e969e-110">-AsJob</span></span>
<span data-ttu-id="e969e-111">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e969e-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e969e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e969e-112">-DefaultProfile</span></span>
<span data-ttu-id="e969e-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e969e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e969e-114">-Force</span><span class="sxs-lookup"><span data-stu-id="e969e-114">-Force</span></span>
<span data-ttu-id="e969e-115">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="e969e-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e969e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e969e-116">-Name</span></span>
<span data-ttu-id="e969e-117">Nome del peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e969e-117">The virtual network peering name.</span></span>

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

### <span data-ttu-id="e969e-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e969e-118">-PassThru</span></span>
<span data-ttu-id="e969e-119">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="e969e-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e969e-120">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="e969e-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e969e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e969e-121">-ResourceGroupName</span></span>
<span data-ttu-id="e969e-122">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e969e-122">The resource group name</span></span>

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

### <span data-ttu-id="e969e-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e969e-123">-VirtualNetworkName</span></span>
<span data-ttu-id="e969e-124">Nome della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e969e-124">The virtual network name.</span></span>

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

### <span data-ttu-id="e969e-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e969e-125">-Confirm</span></span>
<span data-ttu-id="e969e-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e969e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e969e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e969e-127">-WhatIf</span></span>
<span data-ttu-id="e969e-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e969e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e969e-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e969e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e969e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e969e-130">CommonParameters</span></span>
<span data-ttu-id="e969e-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e969e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e969e-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e969e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e969e-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="e969e-133">INPUTS</span></span>

### <span data-ttu-id="e969e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e969e-134">System.String</span></span>

## <span data-ttu-id="e969e-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e969e-135">OUTPUTS</span></span>

### <span data-ttu-id="e969e-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e969e-136">System.Boolean</span></span>

## <span data-ttu-id="e969e-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="e969e-137">NOTES</span></span>

## <span data-ttu-id="e969e-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e969e-138">RELATED LINKS</span></span>

[<span data-ttu-id="e969e-139">Add-AzVirtualNetwork Collegaing</span><span class="sxs-lookup"><span data-stu-id="e969e-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="e969e-140">Get-AzVirtualNetwork Collegaing</span><span class="sxs-lookup"><span data-stu-id="e969e-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="e969e-141">Set-AzVirtualNetwork Collegaing</span><span class="sxs-lookup"><span data-stu-id="e969e-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
