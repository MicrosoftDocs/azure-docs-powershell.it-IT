---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
ms.openlocfilehash: 38995222182d120cd2067429d0f78798a9ebaaf8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018610"
---
# <span data-ttu-id="38d00-101">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="38d00-101">Set-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="38d00-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38d00-102">SYNOPSIS</span></span>
<span data-ttu-id="38d00-103">Aggiorna un tocco di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="38d00-103">Updates a virtual network tap.</span></span>

## <span data-ttu-id="38d00-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38d00-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38d00-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38d00-105">DESCRIPTION</span></span>
<span data-ttu-id="38d00-106">Il cmdlet **set-AzVirtualNetworkTap** aggiorna un tocco di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="38d00-106">The **Set-AzVirtualNetworkTap** cmdlet updates a virtual network tap.</span></span>

## <span data-ttu-id="38d00-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38d00-107">EXAMPLES</span></span>

### <span data-ttu-id="38d00-108">Esempio 1: configurare un tocco di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="38d00-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="38d00-109">Il comando Aggiorna il IpConfiguration di destinazione e aggiorna il tocco di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="38d00-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="38d00-110">Se sono presenti configurazioni tap che la fanno riferimento, tutto il traffico di origine non inizierà a essere speculare alla nuova configurazione IP di destinazione post-aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="38d00-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="38d00-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38d00-111">PARAMETERS</span></span>

### <span data-ttu-id="38d00-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38d00-112">-AsJob</span></span>
<span data-ttu-id="38d00-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="38d00-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38d00-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d00-114">-DefaultProfile</span></span>
<span data-ttu-id="38d00-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38d00-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38d00-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="38d00-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="38d00-117">Toccare rete virtuale</span><span class="sxs-lookup"><span data-stu-id="38d00-117">The virtual network tap</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38d00-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="38d00-118">-Confirm</span></span>
<span data-ttu-id="38d00-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38d00-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d00-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38d00-120">-WhatIf</span></span>
<span data-ttu-id="38d00-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38d00-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38d00-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38d00-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38d00-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d00-123">CommonParameters</span></span>
<span data-ttu-id="38d00-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38d00-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d00-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38d00-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d00-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38d00-126">INPUTS</span></span>

### <span data-ttu-id="38d00-127">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="38d00-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="38d00-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38d00-128">OUTPUTS</span></span>

### <span data-ttu-id="38d00-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="38d00-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="38d00-130">Note</span><span class="sxs-lookup"><span data-stu-id="38d00-130">NOTES</span></span>

## <span data-ttu-id="38d00-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38d00-131">RELATED LINKS</span></span>

[<span data-ttu-id="38d00-132">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="38d00-132">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="38d00-133">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="38d00-133">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="38d00-134">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="38d00-134">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)
