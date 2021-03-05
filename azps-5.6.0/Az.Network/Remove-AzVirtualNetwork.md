---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
ms.openlocfilehash: 18d73d317b1bf2056fdefdfbc112c56bc4ebdfec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006046"
---
# <span data-ttu-id="171df-101">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="171df-101">Remove-AzVirtualNetwork</span></span>

## <span data-ttu-id="171df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="171df-102">SYNOPSIS</span></span>
<span data-ttu-id="171df-103">Rimuove una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="171df-103">Removes a virtual network.</span></span>

## <span data-ttu-id="171df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="171df-104">SYNTAX</span></span>

```
Remove-AzVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="171df-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="171df-105">DESCRIPTION</span></span>
<span data-ttu-id="171df-106">Il cmdlet **Remove-AzVirtualNetwork** rimuove una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="171df-106">The **Remove-AzVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="171df-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="171df-107">EXAMPLES</span></span>

### <span data-ttu-id="171df-108">1: Creare ed eliminare una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="171df-108">1: Create and delete a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
    
Remove-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="171df-109">Questo esempio crea una rete virtuale in un gruppo di risorse e quindi la elimina immediatamente.</span><span class="sxs-lookup"><span data-stu-id="171df-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="171df-110">Per eliminare la richiesta quando si elimina la rete virtuale, usare il contrassegno -Force.</span><span class="sxs-lookup"><span data-stu-id="171df-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="171df-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="171df-111">PARAMETERS</span></span>

### <span data-ttu-id="171df-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="171df-112">-AsJob</span></span>
<span data-ttu-id="171df-113">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="171df-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="171df-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="171df-114">-DefaultProfile</span></span>
<span data-ttu-id="171df-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="171df-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="171df-116">-Force</span><span class="sxs-lookup"><span data-stu-id="171df-116">-Force</span></span>
<span data-ttu-id="171df-117">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="171df-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="171df-118">-Name</span><span class="sxs-lookup"><span data-stu-id="171df-118">-Name</span></span>
<span data-ttu-id="171df-119">Specifica il nome della rete virtuale rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="171df-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="171df-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="171df-120">-PassThru</span></span>
<span data-ttu-id="171df-121">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="171df-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="171df-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="171df-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="171df-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="171df-123">-ResourceGroupName</span></span>
<span data-ttu-id="171df-124">Specifica il nome del gruppo di risorse che contiene la rete virtuale rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="171df-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="171df-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="171df-125">-Confirm</span></span>
<span data-ttu-id="171df-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="171df-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="171df-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="171df-127">-WhatIf</span></span>
<span data-ttu-id="171df-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="171df-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="171df-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="171df-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="171df-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="171df-130">CommonParameters</span></span>
<span data-ttu-id="171df-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="171df-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="171df-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="171df-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="171df-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="171df-133">INPUTS</span></span>

### <span data-ttu-id="171df-134">System.String</span><span class="sxs-lookup"><span data-stu-id="171df-134">System.String</span></span>

## <span data-ttu-id="171df-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="171df-135">OUTPUTS</span></span>

### <span data-ttu-id="171df-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="171df-136">System.Boolean</span></span>

## <span data-ttu-id="171df-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="171df-137">NOTES</span></span>

## <span data-ttu-id="171df-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="171df-138">RELATED LINKS</span></span>

[<span data-ttu-id="171df-139">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="171df-139">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="171df-140">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="171df-140">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="171df-141">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="171df-141">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


