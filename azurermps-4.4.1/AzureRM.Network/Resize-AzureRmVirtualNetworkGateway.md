---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 9f7b85ed3c8f7c1c64ec89f8575975dde81fed7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688609"
---
# <span data-ttu-id="5c5ff-101">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5c5ff-101">Resize-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="5c5ff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5c5ff-102">SYNOPSIS</span></span>
<span data-ttu-id="5c5ff-103">Ridimensiona un gateway di rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="5c5ff-103">Resizes an existing virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c5ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c5ff-104">SYNTAX</span></span>

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c5ff-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c5ff-105">DESCRIPTION</span></span>
<span data-ttu-id="5c5ff-106">Il cmdlet **Resize-AzureRmVirtualNetworkGateway** consente di modificare l'unità di stoccaggio (SKU) per un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="5c5ff-106">The **Resize-AzureRmVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="5c5ff-107">Gli SKU determinano le funzionalità di un gateway, inclusi elementi come la velocità effettiva e il numero massimo di tunnel IP consentiti.</span><span class="sxs-lookup"><span data-stu-id="5c5ff-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="5c5ff-108">Azure supporta SKU di base, standard, ad alte prestazioni, VpnGw1, VpnGw2 e VpnGw3 (a volte denominate SKU di piccole, medie e grandi dimensioni).</span><span class="sxs-lookup"><span data-stu-id="5c5ff-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2 and VpnGw3 SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="5c5ff-109">Per informazioni dettagliate sulle funzionalità di ogni tipo di SKU, vedere https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="5c5ff-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>

<span data-ttu-id="5c5ff-110">Tieni presente che le SKU si differenziano per i prezzi e le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="5c5ff-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="5c5ff-111">Per altre informazioni, vedere https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="5c5ff-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="5c5ff-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c5ff-112">EXAMPLES</span></span>

### <span data-ttu-id="5c5ff-113">Esempio 1: modificare le dimensioni di un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="5c5ff-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="5c5ff-114">Questo esempio modifica le dimensioni di un gateway di rete virtuale denominato ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="5c5ff-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="5c5ff-115">Il primo comando crea un riferimento all'oggetto a ContosoVirtualGateway; Questo riferimento oggetto è archiviato in una variabile denominata $Gateway.</span><span class="sxs-lookup"><span data-stu-id="5c5ff-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="5c5ff-116">Il secondo comando usa quindi il cmdlet **Resize-AzureRmVirtualNetworkGateway** per impostare la proprietà *GatewaySku* su Basic.</span><span class="sxs-lookup"><span data-stu-id="5c5ff-116">The second command then uses the **Resize-AzureRmVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="5c5ff-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5c5ff-117">PARAMETERS</span></span>

### <span data-ttu-id="5c5ff-118">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="5c5ff-118">-GatewaySku</span></span>
<span data-ttu-id="5c5ff-119">Specifica il nuovo tipo di SKU gateway.</span><span class="sxs-lookup"><span data-stu-id="5c5ff-119">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="5c5ff-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5c5ff-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5c5ff-121">Base</span><span class="sxs-lookup"><span data-stu-id="5c5ff-121">Basic</span></span>
- <span data-ttu-id="5c5ff-122">Standard</span><span class="sxs-lookup"><span data-stu-id="5c5ff-122">Standard</span></span>
- <span data-ttu-id="5c5ff-123">Prestazioni elevate</span><span class="sxs-lookup"><span data-stu-id="5c5ff-123">High Performance</span></span>
- <span data-ttu-id="5c5ff-124">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="5c5ff-124">VpnGw1</span></span>
- <span data-ttu-id="5c5ff-125">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="5c5ff-125">VpnGw2</span></span>
- <span data-ttu-id="5c5ff-126">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="5c5ff-126">VpnGw3</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c5ff-127">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5c5ff-127">-VirtualNetworkGateway</span></span>
<span data-ttu-id="5c5ff-128">Specifica un riferimento a un oggetto al gateway di rete virtuale da ridimensionare.</span><span class="sxs-lookup"><span data-stu-id="5c5ff-128">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="5c5ff-129">Puoi creare questo riferimento di oggetto usando la Get-AzureRmVirtualNetworkGateway e specificando il nome del gateway.</span><span class="sxs-lookup"><span data-stu-id="5c5ff-129">You can create this object reference by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c5ff-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c5ff-130">-DefaultProfile</span></span>
<span data-ttu-id="5c5ff-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5c5ff-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c5ff-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c5ff-132">CommonParameters</span></span>
<span data-ttu-id="5c5ff-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c5ff-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c5ff-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c5ff-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c5ff-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5c5ff-135">INPUTS</span></span>

###  
<span data-ttu-id="5c5ff-136">Questo cmdlet accetta le istanze pipeline dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="5c5ff-136">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="5c5ff-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c5ff-137">OUTPUTS</span></span>

###  
<span data-ttu-id="5c5ff-138">Questo cmdlet modifica le istanze esistenti dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="5c5ff-138">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="5c5ff-139">Note</span><span class="sxs-lookup"><span data-stu-id="5c5ff-139">NOTES</span></span>
<span data-ttu-id="5c5ff-140">Non è possibile eseguire il ridimensionamento dagli SKU Basic/standard/HighPerformance alle nuove SKU VpnGw1/VpnGw2/VpnGw3.</span><span class="sxs-lookup"><span data-stu-id="5c5ff-140">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="5c5ff-141">Vedere https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways per istruzioni.</span><span class="sxs-lookup"><span data-stu-id="5c5ff-141">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="5c5ff-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c5ff-142">RELATED LINKS</span></span>

[<span data-ttu-id="5c5ff-143">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="5c5ff-143">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="5c5ff-144">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5c5ff-144">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="5c5ff-145">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="5c5ff-145">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


