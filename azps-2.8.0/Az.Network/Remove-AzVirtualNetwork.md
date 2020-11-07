---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
ms.openlocfilehash: 37dfce09dfcfc2dac3e561abc5957245d844763a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852717"
---
# <span data-ttu-id="dff33-101">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dff33-101">Remove-AzVirtualNetwork</span></span>

## <span data-ttu-id="dff33-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dff33-102">SYNOPSIS</span></span>
<span data-ttu-id="dff33-103">Rimuove una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="dff33-103">Removes a virtual network.</span></span>

## <span data-ttu-id="dff33-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dff33-104">SYNTAX</span></span>

```
Remove-AzVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dff33-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dff33-105">DESCRIPTION</span></span>
<span data-ttu-id="dff33-106">Il cmdlet **Remove-AzVirtualNetwork** rimuove una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="dff33-106">The **Remove-AzVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="dff33-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dff33-107">EXAMPLES</span></span>

### <span data-ttu-id="dff33-108">1: creare ed eliminare una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="dff33-108">1: Create and delete a virtual network</span></span>
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

<span data-ttu-id="dff33-109">Questo esempio crea una rete virtuale in un gruppo di risorse e quindi la Elimina immediatamente.</span><span class="sxs-lookup"><span data-stu-id="dff33-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="dff33-110">Per eliminare la richiesta quando si elimina la rete virtuale, usare il contrassegno-forza.</span><span class="sxs-lookup"><span data-stu-id="dff33-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="dff33-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dff33-111">PARAMETERS</span></span>

### <span data-ttu-id="dff33-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dff33-112">-AsJob</span></span>
<span data-ttu-id="dff33-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="dff33-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dff33-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dff33-114">-DefaultProfile</span></span>
<span data-ttu-id="dff33-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dff33-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dff33-116">-Force</span><span class="sxs-lookup"><span data-stu-id="dff33-116">-Force</span></span>
<span data-ttu-id="dff33-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="dff33-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dff33-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="dff33-118">-Name</span></span>
<span data-ttu-id="dff33-119">Specifica il nome della rete virtuale rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dff33-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dff33-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dff33-120">-PassThru</span></span>
<span data-ttu-id="dff33-121">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="dff33-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dff33-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="dff33-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dff33-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dff33-123">-ResourceGroupName</span></span>
<span data-ttu-id="dff33-124">Specifica il nome del gruppo di risorse che contiene la rete virtuale rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dff33-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dff33-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dff33-125">-Confirm</span></span>
<span data-ttu-id="dff33-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dff33-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dff33-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dff33-127">-WhatIf</span></span>
<span data-ttu-id="dff33-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dff33-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dff33-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dff33-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dff33-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dff33-130">CommonParameters</span></span>
<span data-ttu-id="dff33-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dff33-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dff33-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dff33-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dff33-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dff33-133">INPUTS</span></span>

### <span data-ttu-id="dff33-134">System. String</span><span class="sxs-lookup"><span data-stu-id="dff33-134">System.String</span></span>

## <span data-ttu-id="dff33-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dff33-135">OUTPUTS</span></span>

### <span data-ttu-id="dff33-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dff33-136">System.Boolean</span></span>

## <span data-ttu-id="dff33-137">Note</span><span class="sxs-lookup"><span data-stu-id="dff33-137">NOTES</span></span>

## <span data-ttu-id="dff33-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dff33-138">RELATED LINKS</span></span>

[<span data-ttu-id="dff33-139">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dff33-139">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="dff33-140">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dff33-140">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="dff33-141">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dff33-141">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


