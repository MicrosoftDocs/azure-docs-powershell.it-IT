---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/resize-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Resize-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 92de7fae42a0cf065518cfa8125c76ceb64f8f47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687889"
---
# <span data-ttu-id="950d4-101">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="950d4-101">Resize-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="950d4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="950d4-102">SYNOPSIS</span></span>
<span data-ttu-id="950d4-103">Ridimensiona un gateway di rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="950d4-103">Resizes an existing virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="950d4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="950d4-104">SYNTAX</span></span>

```
Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="950d4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="950d4-105">DESCRIPTION</span></span>
<span data-ttu-id="950d4-106">Il cmdlet **Resize-AzureRmVirtualNetworkGateway** consente di modificare l'unità di stoccaggio (SKU) per un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="950d4-106">The **Resize-AzureRmVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="950d4-107">Gli SKU determinano le funzionalità di un gateway, inclusi elementi come la velocità effettiva e il numero massimo di tunnel IP consentiti.</span><span class="sxs-lookup"><span data-stu-id="950d4-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="950d4-108">Azure supporta SKU di base, standard, ad alte prestazioni, VpnGw1, VpnGw2 e VpnGw3 (a volte denominate SKU di piccole, medie e grandi dimensioni).</span><span class="sxs-lookup"><span data-stu-id="950d4-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2 and VpnGw3 SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="950d4-109">Per informazioni dettagliate sulle funzionalità di ogni tipo di SKU, vedere https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="950d4-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>

<span data-ttu-id="950d4-110">Tieni presente che le SKU si differenziano per i prezzi e le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="950d4-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="950d4-111">Per altre informazioni, vedere https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="950d4-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="950d4-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="950d4-112">EXAMPLES</span></span>

### <span data-ttu-id="950d4-113">Esempio 1: modificare le dimensioni di un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="950d4-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="950d4-114">Questo esempio modifica le dimensioni di un gateway di rete virtuale denominato ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="950d4-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="950d4-115">Il primo comando crea un riferimento all'oggetto a ContosoVirtualGateway; Questo riferimento oggetto è archiviato in una variabile denominata $Gateway.</span><span class="sxs-lookup"><span data-stu-id="950d4-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="950d4-116">Il secondo comando usa quindi il cmdlet **Resize-AzureRmVirtualNetworkGateway** per impostare la proprietà *GatewaySku* su Basic.</span><span class="sxs-lookup"><span data-stu-id="950d4-116">The second command then uses the **Resize-AzureRmVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="950d4-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="950d4-117">PARAMETERS</span></span>

### <span data-ttu-id="950d4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="950d4-118">-DefaultProfile</span></span>
<span data-ttu-id="950d4-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="950d4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="950d4-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="950d4-120">-GatewaySku</span></span>
<span data-ttu-id="950d4-121">Specifica il nuovo tipo di SKU gateway.</span><span class="sxs-lookup"><span data-stu-id="950d4-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="950d4-122">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="950d4-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="950d4-123">Base</span><span class="sxs-lookup"><span data-stu-id="950d4-123">Basic</span></span>
- <span data-ttu-id="950d4-124">Standard</span><span class="sxs-lookup"><span data-stu-id="950d4-124">Standard</span></span>
- <span data-ttu-id="950d4-125">Prestazioni elevate</span><span class="sxs-lookup"><span data-stu-id="950d4-125">High Performance</span></span>
- <span data-ttu-id="950d4-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="950d4-126">VpnGw1</span></span>
- <span data-ttu-id="950d4-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="950d4-127">VpnGw2</span></span>
- <span data-ttu-id="950d4-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="950d4-128">VpnGw3</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="950d4-129">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="950d4-129">-VirtualNetworkGateway</span></span>
<span data-ttu-id="950d4-130">Specifica un riferimento a un oggetto al gateway di rete virtuale da ridimensionare.</span><span class="sxs-lookup"><span data-stu-id="950d4-130">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="950d4-131">Puoi creare questo riferimento di oggetto usando la Get-AzureRmVirtualNetworkGateway e specificando il nome del gateway.</span><span class="sxs-lookup"><span data-stu-id="950d4-131">You can create this object reference by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="950d4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="950d4-132">CommonParameters</span></span>
<span data-ttu-id="950d4-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="950d4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="950d4-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="950d4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="950d4-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="950d4-135">INPUTS</span></span>

###  
<span data-ttu-id="950d4-136">Questo cmdlet accetta le istanze pipeline dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="950d4-136">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="950d4-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="950d4-137">OUTPUTS</span></span>

###  
<span data-ttu-id="950d4-138">Questo cmdlet modifica le istanze esistenti dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="950d4-138">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="950d4-139">Note</span><span class="sxs-lookup"><span data-stu-id="950d4-139">NOTES</span></span>
<span data-ttu-id="950d4-140">Non è possibile eseguire il ridimensionamento dagli SKU Basic/standard/HighPerformance alle nuove SKU VpnGw1/VpnGw2/VpnGw3.</span><span class="sxs-lookup"><span data-stu-id="950d4-140">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="950d4-141">Vedere https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways per istruzioni.</span><span class="sxs-lookup"><span data-stu-id="950d4-141">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="950d4-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="950d4-142">RELATED LINKS</span></span>

[<span data-ttu-id="950d4-143">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="950d4-143">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="950d4-144">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="950d4-144">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="950d4-145">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="950d4-145">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


