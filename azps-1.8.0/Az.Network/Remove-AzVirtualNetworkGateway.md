---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: 7815755d9ec5fffe973e0ecb044409f945ee5faa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678066"
---
# <span data-ttu-id="ed7ec-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed7ec-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="ed7ec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed7ec-102">SYNOPSIS</span></span>
<span data-ttu-id="ed7ec-103">Elimina un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="ed7ec-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="ed7ec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed7ec-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed7ec-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed7ec-105">DESCRIPTION</span></span>
<span data-ttu-id="ed7ec-106">Il gateway di rete virtuale è l'oggetto che rappresenta il gateway in Azure.</span><span class="sxs-lookup"><span data-stu-id="ed7ec-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="ed7ec-107">Il cmdlet **Get-AzVirtualNetworkGateway** restituisce l'oggetto del gateway in Azure in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ed7ec-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="ed7ec-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed7ec-108">EXAMPLES</span></span>

### <span data-ttu-id="ed7ec-109">1: eliminare un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="ed7ec-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="ed7ec-110">Elimina l'oggetto del gateway di rete virtuale con il nome "gateway" nel gruppo di risorse "myRG" Nota: per prima cosa è necessario eliminare tutte le connessioni al gateway di rete virtuale usando il cmdlet **Remove-AzVirtualNetworkGatewayConnection** .</span><span class="sxs-lookup"><span data-stu-id="ed7ec-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG" Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="ed7ec-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed7ec-111">PARAMETERS</span></span>

### <span data-ttu-id="ed7ec-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed7ec-112">-AsJob</span></span>
<span data-ttu-id="ed7ec-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ed7ec-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed7ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed7ec-114">-DefaultProfile</span></span>
<span data-ttu-id="ed7ec-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed7ec-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed7ec-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ed7ec-116">-Force</span></span>
<span data-ttu-id="ed7ec-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ed7ec-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ed7ec-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed7ec-118">-Name</span></span>
<span data-ttu-id="ed7ec-119">Specifica il nome del gateway di rete virtuale rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed7ec-119">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ed7ec-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed7ec-120">-PassThru</span></span>
<span data-ttu-id="ed7ec-121">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="ed7ec-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ed7ec-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="ed7ec-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ed7ec-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed7ec-123">-ResourceGroupName</span></span>
<span data-ttu-id="ed7ec-124">Specifica il nome del gruppo di risorse che contiene il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ed7ec-124">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="ed7ec-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ed7ec-125">-Confirm</span></span>
<span data-ttu-id="ed7ec-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed7ec-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed7ec-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed7ec-127">-WhatIf</span></span>
<span data-ttu-id="ed7ec-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed7ec-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed7ec-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed7ec-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed7ec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed7ec-130">CommonParameters</span></span>
<span data-ttu-id="ed7ec-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed7ec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed7ec-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed7ec-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed7ec-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed7ec-133">INPUTS</span></span>

### <span data-ttu-id="ed7ec-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ed7ec-134">System.String</span></span>

## <span data-ttu-id="ed7ec-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed7ec-135">OUTPUTS</span></span>

### <span data-ttu-id="ed7ec-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ed7ec-136">System.Boolean</span></span>

## <span data-ttu-id="ed7ec-137">Note</span><span class="sxs-lookup"><span data-stu-id="ed7ec-137">NOTES</span></span>

## <span data-ttu-id="ed7ec-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed7ec-138">RELATED LINKS</span></span>

[<span data-ttu-id="ed7ec-139">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed7ec-139">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ed7ec-140">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed7ec-140">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ed7ec-141">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed7ec-141">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ed7ec-142">Ridimensionare-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed7ec-142">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ed7ec-143">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ed7ec-143">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
