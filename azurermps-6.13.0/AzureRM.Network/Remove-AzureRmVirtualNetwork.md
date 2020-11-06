---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
ms.openlocfilehash: b27ad6bfc08f6c6d9304cc78f888870a8a2dbad4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520911"
---
# <span data-ttu-id="2562a-101">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2562a-101">Remove-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="2562a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2562a-102">SYNOPSIS</span></span>
<span data-ttu-id="2562a-103">Rimuove una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="2562a-103">Removes a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2562a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2562a-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2562a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2562a-105">DESCRIPTION</span></span>
<span data-ttu-id="2562a-106">Il cmdlet **Remove-AzureRmVirtualNetwork** rimuove una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="2562a-106">The **Remove-AzureRmVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="2562a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2562a-107">EXAMPLES</span></span>

### <span data-ttu-id="2562a-108">1: creare ed eliminare una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="2562a-108">1: Create and delete a virtual network</span></span>
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

<span data-ttu-id="2562a-109">Questo esempio crea una rete virtuale in un gruppo di risorse e quindi la Elimina immediatamente.</span><span class="sxs-lookup"><span data-stu-id="2562a-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="2562a-110">Per eliminare la richiesta quando si elimina la rete virtuale, usare il contrassegno-forza.</span><span class="sxs-lookup"><span data-stu-id="2562a-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="2562a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2562a-111">PARAMETERS</span></span>

### <span data-ttu-id="2562a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2562a-112">-AsJob</span></span>
<span data-ttu-id="2562a-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2562a-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2562a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2562a-114">-DefaultProfile</span></span>
<span data-ttu-id="2562a-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2562a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2562a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2562a-116">-Force</span></span>
<span data-ttu-id="2562a-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2562a-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2562a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="2562a-118">-Name</span></span>
<span data-ttu-id="2562a-119">Specifica il nome della rete virtuale rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2562a-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2562a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2562a-120">-PassThru</span></span>
<span data-ttu-id="2562a-121">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="2562a-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2562a-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="2562a-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2562a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2562a-123">-ResourceGroupName</span></span>
<span data-ttu-id="2562a-124">Specifica il nome del gruppo di risorse che contiene la rete virtuale rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2562a-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2562a-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2562a-125">-Confirm</span></span>
<span data-ttu-id="2562a-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2562a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2562a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2562a-127">-WhatIf</span></span>
<span data-ttu-id="2562a-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2562a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2562a-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2562a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2562a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2562a-130">CommonParameters</span></span>
<span data-ttu-id="2562a-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2562a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2562a-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2562a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2562a-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2562a-133">INPUTS</span></span>

### <span data-ttu-id="2562a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2562a-134">System.String</span></span>

## <span data-ttu-id="2562a-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2562a-135">OUTPUTS</span></span>

### <span data-ttu-id="2562a-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2562a-136">System.Boolean</span></span>

## <span data-ttu-id="2562a-137">Note</span><span class="sxs-lookup"><span data-stu-id="2562a-137">NOTES</span></span>

## <span data-ttu-id="2562a-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2562a-138">RELATED LINKS</span></span>

[<span data-ttu-id="2562a-139">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2562a-139">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="2562a-140">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2562a-140">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="2562a-141">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2562a-141">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


