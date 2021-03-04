---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
ms.openlocfilehash: 22d2396e4471e2321ff9e532d4361909baa67163
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952014"
---
# <span data-ttu-id="4232f-101">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="4232f-101">Set-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="4232f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4232f-102">SYNOPSIS</span></span>
<span data-ttu-id="4232f-103">Aggiorna un tocco di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="4232f-103">Updates a virtual network tap.</span></span>

## <span data-ttu-id="4232f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4232f-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4232f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4232f-105">DESCRIPTION</span></span>
<span data-ttu-id="4232f-106">Il cmdlet **Set-AzVirtualNetworkTap** aggiorna un tocco di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="4232f-106">The **Set-AzVirtualNetworkTap** cmdlet updates a virtual network tap.</span></span>

## <span data-ttu-id="4232f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4232f-107">EXAMPLES</span></span>

### <span data-ttu-id="4232f-108">Esempio 1: Configurare un tocco di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="4232f-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="4232f-109">Il comando aggiorna destination IpConfiguration e aggiorna il tocco della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="4232f-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="4232f-110">Se ci sono configurazioni di tocco che fanno riferimento ad essa, tutto il traffico di origine non verrà speculare al nuovo ip di destinazione dopo l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="4232f-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="4232f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4232f-111">PARAMETERS</span></span>

### <span data-ttu-id="4232f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4232f-112">-AsJob</span></span>
<span data-ttu-id="4232f-113">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4232f-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4232f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4232f-114">-DefaultProfile</span></span>
<span data-ttu-id="4232f-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4232f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4232f-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="4232f-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="4232f-117">Il tocco della rete virtuale</span><span class="sxs-lookup"><span data-stu-id="4232f-117">The virtual network tap</span></span>

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

### <span data-ttu-id="4232f-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4232f-118">-Confirm</span></span>
<span data-ttu-id="4232f-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4232f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4232f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4232f-120">-WhatIf</span></span>
<span data-ttu-id="4232f-121">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4232f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4232f-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4232f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4232f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4232f-123">CommonParameters</span></span>
<span data-ttu-id="4232f-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4232f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4232f-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4232f-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4232f-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="4232f-126">INPUTS</span></span>

### <span data-ttu-id="4232f-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="4232f-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="4232f-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4232f-128">OUTPUTS</span></span>

### <span data-ttu-id="4232f-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="4232f-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="4232f-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="4232f-130">NOTES</span></span>

## <span data-ttu-id="4232f-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4232f-131">RELATED LINKS</span></span>

[<span data-ttu-id="4232f-132">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="4232f-132">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="4232f-133">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="4232f-133">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="4232f-134">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="4232f-134">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)
