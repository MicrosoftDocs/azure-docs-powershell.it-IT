---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: 1d767677c547c2418ca19e3206f3ca5a25638de0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521322"
---
# <span data-ttu-id="bbedb-101">Set-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="bbedb-101">Set-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="bbedb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bbedb-102">SYNOPSIS</span></span>
<span data-ttu-id="bbedb-103">Imposta lo stato obiettivo per un tocco di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="bbedb-103">Sets the goal state for a virtual network tap.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbedb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bbedb-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbedb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bbedb-105">DESCRIPTION</span></span>
<span data-ttu-id="bbedb-106">**Set-AzureRmVirtualNetworkTap** imposta lo stato obiettivo per un tocco di rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="bbedb-106">The **Set-AzureRmVirtualNetworkTap** sets the goal state for an Azure virtual network tap.</span></span>

## <span data-ttu-id="bbedb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bbedb-107">EXAMPLES</span></span>

### <span data-ttu-id="bbedb-108">Esempio 1: configurare un tocco di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="bbedb-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzureRmVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzureRmVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="bbedb-109">Il comando Aggiorna il IpConfiguration di destinazione e aggiorna il tocco di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="bbedb-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="bbedb-110">Se sono presenti configurazioni tap che la fanno riferimento, tutto il traffico di origine non inizierà a essere speculare alla nuova configurazione IP di destinazione post-aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="bbedb-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="bbedb-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bbedb-111">PARAMETERS</span></span>

### <span data-ttu-id="bbedb-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bbedb-112">-AsJob</span></span>
<span data-ttu-id="bbedb-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="bbedb-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bbedb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbedb-114">-DefaultProfile</span></span>
<span data-ttu-id="bbedb-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bbedb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbedb-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="bbedb-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="bbedb-117">Toccare rete virtuale</span><span class="sxs-lookup"><span data-stu-id="bbedb-117">The virtual network tap</span></span>

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

### <span data-ttu-id="bbedb-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bbedb-118">-Confirm</span></span>
<span data-ttu-id="bbedb-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbedb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbedb-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbedb-120">-WhatIf</span></span>
<span data-ttu-id="bbedb-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbedb-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbedb-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbedb-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbedb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbedb-123">CommonParameters</span></span>
<span data-ttu-id="bbedb-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbedb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbedb-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbedb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbedb-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bbedb-126">INPUTS</span></span>

### <span data-ttu-id="bbedb-127">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="bbedb-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="bbedb-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bbedb-128">OUTPUTS</span></span>

### <span data-ttu-id="bbedb-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="bbedb-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="bbedb-130">Note</span><span class="sxs-lookup"><span data-stu-id="bbedb-130">NOTES</span></span>

## <span data-ttu-id="bbedb-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bbedb-131">RELATED LINKS</span></span>
