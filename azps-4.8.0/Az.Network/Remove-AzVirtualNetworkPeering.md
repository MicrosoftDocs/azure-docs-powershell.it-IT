---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 38530b5e4034286d623c82b841064760fe2e49e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190941"
---
# <span data-ttu-id="91aec-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="91aec-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="91aec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="91aec-102">SYNOPSIS</span></span>
<span data-ttu-id="91aec-103">Rimuove un peering di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="91aec-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="91aec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91aec-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91aec-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91aec-105">DESCRIPTION</span></span>
<span data-ttu-id="91aec-106">Rimuove un peering di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="91aec-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="91aec-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91aec-107">EXAMPLES</span></span>

### <span data-ttu-id="91aec-108">Esempio 1: rimuovere un peering di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="91aec-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="91aec-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="91aec-109">PARAMETERS</span></span>

### <span data-ttu-id="91aec-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91aec-110">-AsJob</span></span>
<span data-ttu-id="91aec-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="91aec-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91aec-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91aec-112">-DefaultProfile</span></span>
<span data-ttu-id="91aec-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91aec-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91aec-114">-Force</span><span class="sxs-lookup"><span data-stu-id="91aec-114">-Force</span></span>
<span data-ttu-id="91aec-115">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="91aec-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="91aec-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="91aec-116">-Name</span></span>
<span data-ttu-id="91aec-117">Nome peer di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="91aec-117">The virtual network peering name.</span></span>

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

### <span data-ttu-id="91aec-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91aec-118">-PassThru</span></span>
<span data-ttu-id="91aec-119">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="91aec-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="91aec-120">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="91aec-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="91aec-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91aec-121">-ResourceGroupName</span></span>
<span data-ttu-id="91aec-122">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="91aec-122">The resource group name</span></span>

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

### <span data-ttu-id="91aec-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="91aec-123">-VirtualNetworkName</span></span>
<span data-ttu-id="91aec-124">Nome della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="91aec-124">The virtual network name.</span></span>

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

### <span data-ttu-id="91aec-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="91aec-125">-Confirm</span></span>
<span data-ttu-id="91aec-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91aec-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91aec-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91aec-127">-WhatIf</span></span>
<span data-ttu-id="91aec-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91aec-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91aec-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91aec-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91aec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91aec-130">CommonParameters</span></span>
<span data-ttu-id="91aec-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91aec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91aec-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91aec-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91aec-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="91aec-133">INPUTS</span></span>

### <span data-ttu-id="91aec-134">System. String</span><span class="sxs-lookup"><span data-stu-id="91aec-134">System.String</span></span>

## <span data-ttu-id="91aec-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91aec-135">OUTPUTS</span></span>

### <span data-ttu-id="91aec-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="91aec-136">System.Boolean</span></span>

## <span data-ttu-id="91aec-137">Note</span><span class="sxs-lookup"><span data-stu-id="91aec-137">NOTES</span></span>

## <span data-ttu-id="91aec-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91aec-138">RELATED LINKS</span></span>

[<span data-ttu-id="91aec-139">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="91aec-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="91aec-140">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="91aec-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="91aec-141">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="91aec-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
