---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 4b58561783fac3d0c068ec61821c9669a97e1542
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518639"
---
# <span data-ttu-id="8c7f6-101">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8c7f6-101">Get-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="8c7f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8c7f6-102">SYNOPSIS</span></span>
<span data-ttu-id="8c7f6-103">Ottiene il peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8c7f6-103">Gets the virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c7f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c7f6-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c7f6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c7f6-105">DESCRIPTION</span></span>
<span data-ttu-id="8c7f6-106">Il cmdlet **Get-AzureRmVirtualNetworkPeering** ottiene il peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8c7f6-106">The **Get-AzureRmVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="8c7f6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c7f6-107">EXAMPLES</span></span>

### <span data-ttu-id="8c7f6-108">Esempio 1: ottenere un peering tra due reti virtuali</span><span class="sxs-lookup"><span data-stu-id="8c7f6-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="8c7f6-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8c7f6-109">PARAMETERS</span></span>

### <span data-ttu-id="8c7f6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c7f6-110">-DefaultProfile</span></span>
<span data-ttu-id="8c7f6-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8c7f6-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c7f6-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c7f6-112">-Name</span></span>
<span data-ttu-id="8c7f6-113">Specifica il nome peer della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8c7f6-113">Specifies the virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7f6-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c7f6-114">-ResourceGroupName</span></span>
<span data-ttu-id="8c7f6-115">Specifica il nome del gruppo di risorse a cui appartiene il peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8c7f6-115">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="8c7f6-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="8c7f6-116">-VirtualNetworkName</span></span>
<span data-ttu-id="8c7f6-117">Specifica il nome di rete virtuale ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c7f6-117">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8c7f6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c7f6-118">CommonParameters</span></span>
<span data-ttu-id="8c7f6-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c7f6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c7f6-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c7f6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c7f6-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8c7f6-121">INPUTS</span></span>

### <span data-ttu-id="8c7f6-122">System. String</span><span class="sxs-lookup"><span data-stu-id="8c7f6-122">System.String</span></span>

## <span data-ttu-id="8c7f6-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c7f6-123">OUTPUTS</span></span>

### <span data-ttu-id="8c7f6-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8c7f6-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="8c7f6-125">Note</span><span class="sxs-lookup"><span data-stu-id="8c7f6-125">NOTES</span></span>

## <span data-ttu-id="8c7f6-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c7f6-126">RELATED LINKS</span></span>

[<span data-ttu-id="8c7f6-127">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8c7f6-127">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="8c7f6-128">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8c7f6-128">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="8c7f6-129">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8c7f6-129">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


