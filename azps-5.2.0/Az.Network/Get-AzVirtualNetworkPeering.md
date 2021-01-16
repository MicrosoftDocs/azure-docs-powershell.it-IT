---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkPeering.md
ms.openlocfilehash: 0cc6441d77806c28450d50d5f83a7588da1d1d46
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358497"
---
# <span data-ttu-id="a94cc-101">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a94cc-101">Get-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="a94cc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a94cc-102">SYNOPSIS</span></span>
<span data-ttu-id="a94cc-103">Ottiene il peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a94cc-103">Gets the virtual network peering.</span></span>

## <span data-ttu-id="a94cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a94cc-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a94cc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a94cc-105">DESCRIPTION</span></span>
<span data-ttu-id="a94cc-106">Il cmdlet **Get-AzVirtualNetworkPeering** ottiene il peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a94cc-106">The **Get-AzVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="a94cc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a94cc-107">EXAMPLES</span></span>

### <span data-ttu-id="a94cc-108">Esempio 1: ottenere un peering tra due reti virtuali</span><span class="sxs-lookup"><span data-stu-id="a94cc-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

### <span data-ttu-id="a94cc-109">Esempio 2: ottenere tutti i peer in una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a94cc-109">Example 2: Get all peerings in virtual network</span></span>
```
# Get all virtual network peerings located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzVirtualNetworkPeering -Name "myVnet1To*" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="a94cc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a94cc-110">PARAMETERS</span></span>

### <span data-ttu-id="a94cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a94cc-111">-DefaultProfile</span></span>
<span data-ttu-id="a94cc-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a94cc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a94cc-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a94cc-113">-Name</span></span>
<span data-ttu-id="a94cc-114">Specifica il nome peer della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a94cc-114">Specifies the virtual network peering name.</span></span>

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

### <span data-ttu-id="a94cc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a94cc-115">-ResourceGroupName</span></span>
<span data-ttu-id="a94cc-116">Specifica il nome del gruppo di risorse a cui appartiene il peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a94cc-116">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="a94cc-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a94cc-117">-VirtualNetworkName</span></span>
<span data-ttu-id="a94cc-118">Specifica il nome di rete virtuale ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a94cc-118">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a94cc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a94cc-119">CommonParameters</span></span>
<span data-ttu-id="a94cc-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a94cc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a94cc-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a94cc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a94cc-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a94cc-122">INPUTS</span></span>

### <span data-ttu-id="a94cc-123">System. String</span><span class="sxs-lookup"><span data-stu-id="a94cc-123">System.String</span></span>

## <span data-ttu-id="a94cc-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a94cc-124">OUTPUTS</span></span>

### <span data-ttu-id="a94cc-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a94cc-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="a94cc-126">Note</span><span class="sxs-lookup"><span data-stu-id="a94cc-126">NOTES</span></span>

## <span data-ttu-id="a94cc-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a94cc-127">RELATED LINKS</span></span>

[<span data-ttu-id="a94cc-128">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a94cc-128">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="a94cc-129">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a94cc-129">Remove-AzVirtualNetworkPeering</span></span>](./Remove-AzVirtualNetworkPeering.md)

[<span data-ttu-id="a94cc-130">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a94cc-130">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
