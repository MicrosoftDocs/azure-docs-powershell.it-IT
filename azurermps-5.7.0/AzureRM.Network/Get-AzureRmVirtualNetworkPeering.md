---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 463DDBA8-0F93-483D-A4B6-3B055968CDE8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 0c68886906957204ee0885a00bfc07740fb6ac65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686094"
---
# <span data-ttu-id="39d40-101">Get-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="39d40-101">Get-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="39d40-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39d40-102">SYNOPSIS</span></span>
<span data-ttu-id="39d40-103">Ottiene il peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="39d40-103">Gets the virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39d40-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39d40-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39d40-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39d40-105">DESCRIPTION</span></span>
<span data-ttu-id="39d40-106">Il cmdlet **Get-AzureRmVirtualNetworkPeering** ottiene il peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="39d40-106">The **Get-AzureRmVirtualNetworkPeering** cmdlet gets the virtual network peering.</span></span>

## <span data-ttu-id="39d40-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39d40-107">EXAMPLES</span></span>

### <span data-ttu-id="39d40-108">Esempio 1: ottenere un peering tra due reti virtuali</span><span class="sxs-lookup"><span data-stu-id="39d40-108">Example 1: Get a peering between two virtual networks</span></span>
```
# Get virtual network peering named myVnet1TomyVnet2 located in myVirtualNetwork in the resource group named myResourceGroup.

Get-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetwork "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="39d40-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39d40-109">PARAMETERS</span></span>

### <span data-ttu-id="39d40-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39d40-110">-DefaultProfile</span></span>
<span data-ttu-id="39d40-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39d40-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39d40-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="39d40-112">-Name</span></span>
<span data-ttu-id="39d40-113">Specifica il nome peer della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="39d40-113">Specifies the virtual network peering name.</span></span>

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

### <span data-ttu-id="39d40-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39d40-114">-ResourceGroupName</span></span>
<span data-ttu-id="39d40-115">Specifica il nome del gruppo di risorse a cui appartiene il peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="39d40-115">Specifies the resource group name that the virtual network peering belongs to.</span></span>

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

### <span data-ttu-id="39d40-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="39d40-116">-VirtualNetworkName</span></span>
<span data-ttu-id="39d40-117">Specifica il nome di rete virtuale ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39d40-117">Specifies the virtual network name that this cmdlet gets.</span></span>

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

### <span data-ttu-id="39d40-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39d40-118">CommonParameters</span></span>
<span data-ttu-id="39d40-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39d40-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39d40-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39d40-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39d40-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39d40-121">INPUTS</span></span>

### <span data-ttu-id="39d40-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="39d40-122">None</span></span>
<span data-ttu-id="39d40-123">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="39d40-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="39d40-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39d40-124">OUTPUTS</span></span>

### <span data-ttu-id="39d40-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="39d40-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkPeering</span></span>

## <span data-ttu-id="39d40-126">Note</span><span class="sxs-lookup"><span data-stu-id="39d40-126">NOTES</span></span>

## <span data-ttu-id="39d40-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39d40-127">RELATED LINKS</span></span>

[<span data-ttu-id="39d40-128">Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="39d40-128">Add-AzureRmVirtualNetworkPeering</span></span>](./Add-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="39d40-129">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="39d40-129">Remove-AzureRmVirtualNetworkPeering</span></span>](./Remove-AzureRmVirtualNetworkPeering.md)

[<span data-ttu-id="39d40-130">Set-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="39d40-130">Set-AzureRmVirtualNetworkPeering</span></span>](./Set-AzureRmVirtualNetworkPeering.md)


