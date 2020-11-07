---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkpeering
schema: 2.0.0
ms.openlocfilehash: b5e3cf083f003a643639635c61ca8e3f13e16eaf
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866274"
---
# <span data-ttu-id="d3a45-101">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="d3a45-101">Get-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="d3a45-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3a45-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a45-103">Ottiene il peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d3a45-103">Gets the virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3a45-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3a45-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3a45-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3a45-105">DESCRIPTION</span></span>
<span data-ttu-id="d3a45-106">Il cmdlet **Get-AzureRmVirtualNetworkPeering** ottiene il peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d3a45-106">The **Get-AzureRmVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="d3a45-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3a45-107">EXAMPLES</span></span>

### <span data-ttu-id="d3a45-108">Esempio 1: ottenere un peering tra due reti virtuali</span><span class="sxs-lookup"><span data-stu-id="d3a45-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="d3a45-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3a45-109">PARAMETERS</span></span>

### <span data-ttu-id="d3a45-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a45-110">-DefaultProfile</span></span>
<span data-ttu-id="d3a45-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3a45-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3a45-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3a45-112">-Name</span></span>
<span data-ttu-id="d3a45-113">Specifica il nome peer della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d3a45-113">Specifies the virtual network peering name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3a45-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3a45-114">-ResourceGroupName</span></span>
<span data-ttu-id="d3a45-115">Specifica il nome del gruppo di risorse a cui appartiene il peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d3a45-115">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="d3a45-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d3a45-116">-VirtualNetworkName</span></span>
<span data-ttu-id="d3a45-117">Specifica il nome di rete virtuale ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3a45-117">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d3a45-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a45-118">CommonParameters</span></span>
<span data-ttu-id="d3a45-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3a45-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a45-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3a45-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a45-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3a45-121">INPUTS</span></span>

## <span data-ttu-id="d3a45-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3a45-122">OUTPUTS</span></span>

### <span data-ttu-id="d3a45-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="d3a45-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="d3a45-124">Note</span><span class="sxs-lookup"><span data-stu-id="d3a45-124">NOTES</span></span>

## <span data-ttu-id="d3a45-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3a45-125">RELATED LINKS</span></span>

[<span data-ttu-id="d3a45-126">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="d3a45-126">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="d3a45-127">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="d3a45-127">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="d3a45-128">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="d3a45-128">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


