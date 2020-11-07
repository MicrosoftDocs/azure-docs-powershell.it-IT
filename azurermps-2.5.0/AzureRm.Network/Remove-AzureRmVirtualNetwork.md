---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: 89f0be5dbb0ba6b4e24e76be1eb75c375f0ebcd5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866043"
---
# <span data-ttu-id="0c664-101">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0c664-101">Remove-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="0c664-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c664-102">SYNOPSIS</span></span>
<span data-ttu-id="0c664-103">Rimuove una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="0c664-103">Removes a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c664-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c664-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c664-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c664-105">DESCRIPTION</span></span>
<span data-ttu-id="0c664-106">Il cmdlet **Remove-AzureRmVirtualNetwork** rimuove una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="0c664-106">The **Remove-AzureRmVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="0c664-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c664-107">EXAMPLES</span></span>

### <span data-ttu-id="0c664-108">1: creare ed eliminare una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="0c664-108">1: Create and delete a virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
    
Remove-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="0c664-109">Questo esempio crea una rete virtuale in un gruppo di risorse e quindi la Elimina immediatamente.</span><span class="sxs-lookup"><span data-stu-id="0c664-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="0c664-110">Per eliminare la richiesta quando si elimina la rete virtuale, usare il contrassegno-forza.</span><span class="sxs-lookup"><span data-stu-id="0c664-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="0c664-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c664-111">PARAMETERS</span></span>

### <span data-ttu-id="0c664-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c664-112">-AsJob</span></span>
<span data-ttu-id="0c664-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0c664-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c664-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c664-114">-DefaultProfile</span></span>
<span data-ttu-id="0c664-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c664-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c664-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0c664-116">-Force</span></span>
<span data-ttu-id="0c664-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0c664-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0c664-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c664-118">-Name</span></span>
<span data-ttu-id="0c664-119">Specifica il nome della rete virtuale rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c664-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0c664-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c664-120">-PassThru</span></span>
<span data-ttu-id="0c664-121">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="0c664-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0c664-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="0c664-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0c664-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c664-123">-ResourceGroupName</span></span>
<span data-ttu-id="0c664-124">Specifica il nome del gruppo di risorse che contiene la rete virtuale rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c664-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0c664-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0c664-125">-Confirm</span></span>
<span data-ttu-id="0c664-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c664-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c664-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c664-127">-WhatIf</span></span>
<span data-ttu-id="0c664-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c664-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c664-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c664-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c664-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c664-130">CommonParameters</span></span>
<span data-ttu-id="0c664-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c664-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c664-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c664-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c664-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c664-133">INPUTS</span></span>

## <span data-ttu-id="0c664-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c664-134">OUTPUTS</span></span>

## <span data-ttu-id="0c664-135">Note</span><span class="sxs-lookup"><span data-stu-id="0c664-135">NOTES</span></span>

## <span data-ttu-id="0c664-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c664-136">RELATED LINKS</span></span>

[<span data-ttu-id="0c664-137">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0c664-137">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="0c664-138">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0c664-138">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="0c664-139">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0c664-139">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


