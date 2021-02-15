---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 0cc6441d77806c28450d50d5f83a7588da1d1d46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193703"
---
# <span data-ttu-id="f75d2-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f75d2-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="f75d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f75d2-102">SYNOPSIS</span></span>
<span data-ttu-id="f75d2-103">Ottiene il peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="f75d2-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="f75d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f75d2-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f75d2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f75d2-105">DESCRIPTION</span></span>
<span data-ttu-id="f75d2-106">Il **cmdlet Get-AzVirtualNetworkIng ottiene** il peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="f75d2-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="f75d2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f75d2-107">EXAMPLES</span></span>

### <span data-ttu-id="f75d2-108">Esempio 1: Ottenere un peering tra due reti virtuali</span><span class="sxs-lookup"><span data-stu-id="f75d2-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

### <span data-ttu-id="f75d2-109">Esempio 2: Ottenere tutti i peering in una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="f75d2-109">Example 2: Get all peerings in virtual network</span></span>
```
# Get all virtual network peerings located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1To*" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="f75d2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f75d2-110">PARAMETERS</span></span>

### <span data-ttu-id="f75d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f75d2-111">-DefaultProfile</span></span>
<span data-ttu-id="f75d2-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f75d2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f75d2-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f75d2-113">-Name</span></span>
<span data-ttu-id="f75d2-114">Specifica il nome del peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="f75d2-114">Specifies the virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f75d2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f75d2-115">-ResourceGroupName</span></span>
<span data-ttu-id="f75d2-116">Specifica il nome del gruppo di risorse a cui appartiene il peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="f75d2-116">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="f75d2-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f75d2-117">-VirtualNetworkName</span></span>
<span data-ttu-id="f75d2-118">Specifica il nome della rete virtuale che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f75d2-118">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f75d2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f75d2-119">CommonParameters</span></span>
<span data-ttu-id="f75d2-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f75d2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f75d2-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f75d2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f75d2-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="f75d2-122">INPUTS</span></span>

### <span data-ttu-id="f75d2-123">System.String</span><span class="sxs-lookup"><span data-stu-id="f75d2-123">System.String</span></span>

## <span data-ttu-id="f75d2-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f75d2-124">OUTPUTS</span></span>

### <span data-ttu-id="f75d2-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkCollectioning</span><span class="sxs-lookup"><span data-stu-id="f75d2-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="f75d2-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="f75d2-126">NOTES</span></span>

## <span data-ttu-id="f75d2-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f75d2-127">RELATED LINKS</span></span>

[<span data-ttu-id="f75d2-128">Add-AzVirtualNetworkConvertering</span><span class="sxs-lookup"><span data-stu-id="f75d2-128">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="f75d2-129">Remove-AzVirtualNetwork Collegaing</span><span class="sxs-lookup"><span data-stu-id="f75d2-129">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="f75d2-130">Set-AzVirtualNetwork Collegaing</span><span class="sxs-lookup"><span data-stu-id="f75d2-130">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
