---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 5648fe6049a7686d5f3930de6ea780598e2c0b06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970062"
---
# <span data-ttu-id="e1ad1-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="e1ad1-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="e1ad1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1ad1-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ad1-103">Ottiene il peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="e1ad1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1ad1-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1ad1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e1ad1-105">DESCRIPTION</span></span>
<span data-ttu-id="e1ad1-106">Il **cmdlet Get-AzVirtualNetworkEndoing** ottiene il peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="e1ad1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1ad1-107">EXAMPLES</span></span>

### <span data-ttu-id="e1ad1-108">Esempio 1: Ottenere un peering tra due reti virtuali</span><span class="sxs-lookup"><span data-stu-id="e1ad1-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

### <span data-ttu-id="e1ad1-109">Esempio 2: Ottenere tutti i peering in una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="e1ad1-109">Example 2: Get all peerings in virtual network</span></span>
```
# Get all virtual network peerings located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1To*" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="e1ad1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1ad1-110">PARAMETERS</span></span>

### <span data-ttu-id="e1ad1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ad1-111">-DefaultProfile</span></span>
<span data-ttu-id="e1ad1-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1ad1-113">-Name</span><span class="sxs-lookup"><span data-stu-id="e1ad1-113">-Name</span></span>
<span data-ttu-id="e1ad1-114">Specifica il nome del peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-114">Specifies the virtual network peering name.</span></span>

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

### <span data-ttu-id="e1ad1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1ad1-115">-ResourceGroupName</span></span>
<span data-ttu-id="e1ad1-116">Specifica il nome del gruppo di risorse a cui appartiene il peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-116">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="e1ad1-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e1ad1-117">-VirtualNetworkName</span></span>
<span data-ttu-id="e1ad1-118">Specifica il nome della rete virtuale che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-118">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e1ad1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ad1-119">CommonParameters</span></span>
<span data-ttu-id="e1ad1-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ad1-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e1ad1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ad1-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="e1ad1-122">INPUTS</span></span>

### <span data-ttu-id="e1ad1-123">System.String</span><span class="sxs-lookup"><span data-stu-id="e1ad1-123">System.String</span></span>

## <span data-ttu-id="e1ad1-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1ad1-124">OUTPUTS</span></span>

### <span data-ttu-id="e1ad1-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkIng</span><span class="sxs-lookup"><span data-stu-id="e1ad1-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="e1ad1-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="e1ad1-126">NOTES</span></span>

## <span data-ttu-id="e1ad1-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1ad1-127">RELATED LINKS</span></span>

[<span data-ttu-id="e1ad1-128">Add-AzVirtualNetwork Collegaing</span><span class="sxs-lookup"><span data-stu-id="e1ad1-128">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="e1ad1-129">Remove-AzVirtualNetwork Collegaing</span><span class="sxs-lookup"><span data-stu-id="e1ad1-129">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="e1ad1-130">Set-AzVirtualNetwork Collegaing</span><span class="sxs-lookup"><span data-stu-id="e1ad1-130">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
