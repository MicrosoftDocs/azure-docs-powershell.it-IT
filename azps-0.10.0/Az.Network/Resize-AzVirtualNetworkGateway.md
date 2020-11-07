---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: bd42d7cec30b7d42dcb1cdb3657f6681bf2cb6b0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862877"
---
# <span data-ttu-id="620b7-101">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="620b7-101">Resize-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="620b7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="620b7-102">SYNOPSIS</span></span>
<span data-ttu-id="620b7-103">Ridimensiona un gateway di rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="620b7-103">Resizes an existing virtual network gateway.</span></span>

## <span data-ttu-id="620b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="620b7-104">SYNTAX</span></span>

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="620b7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="620b7-105">DESCRIPTION</span></span>
<span data-ttu-id="620b7-106">Il cmdlet **Resize-AzVirtualNetworkGateway** consente di modificare l'unità di stoccaggio (SKU) per un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="620b7-106">The **Resize-AzVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="620b7-107">Gli SKU determinano le funzionalità di un gateway, inclusi elementi come la velocità effettiva e il numero massimo di tunnel IP consentiti.</span><span class="sxs-lookup"><span data-stu-id="620b7-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="620b7-108">Azure supporta SKU di base, standard, ad alte prestazioni, VpnGw1, VpnGw2 e VpnGw3 (a volte denominate SKU di piccole, medie e grandi dimensioni).</span><span class="sxs-lookup"><span data-stu-id="620b7-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2 and VpnGw3 SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="620b7-109">Per informazioni dettagliate sulle funzionalità di ogni tipo di SKU, vedere https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="620b7-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>

<span data-ttu-id="620b7-110">Tieni presente che le SKU si differenziano per i prezzi e le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="620b7-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="620b7-111">Per altre informazioni, vedere https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="620b7-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="620b7-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="620b7-112">EXAMPLES</span></span>

### <span data-ttu-id="620b7-113">Esempio 1: modificare le dimensioni di un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="620b7-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="620b7-114">Questo esempio modifica le dimensioni di un gateway di rete virtuale denominato ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="620b7-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="620b7-115">Il primo comando crea un riferimento all'oggetto a ContosoVirtualGateway; Questo riferimento oggetto è archiviato in una variabile denominata $Gateway.</span><span class="sxs-lookup"><span data-stu-id="620b7-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="620b7-116">Il secondo comando usa quindi il cmdlet **Resize-AzVirtualNetworkGateway** per impostare la proprietà *GatewaySku* su Basic.</span><span class="sxs-lookup"><span data-stu-id="620b7-116">The second command then uses the **Resize-AzVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="620b7-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="620b7-117">PARAMETERS</span></span>

### <span data-ttu-id="620b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="620b7-118">-DefaultProfile</span></span>
<span data-ttu-id="620b7-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="620b7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="620b7-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="620b7-120">-GatewaySku</span></span>
<span data-ttu-id="620b7-121">Specifica il nuovo tipo di SKU gateway.</span><span class="sxs-lookup"><span data-stu-id="620b7-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="620b7-122">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="620b7-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="620b7-123">Base</span><span class="sxs-lookup"><span data-stu-id="620b7-123">Basic</span></span>
- <span data-ttu-id="620b7-124">Standard</span><span class="sxs-lookup"><span data-stu-id="620b7-124">Standard</span></span>
- <span data-ttu-id="620b7-125">Prestazioni elevate</span><span class="sxs-lookup"><span data-stu-id="620b7-125">High Performance</span></span>
- <span data-ttu-id="620b7-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="620b7-126">VpnGw1</span></span>
- <span data-ttu-id="620b7-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="620b7-127">VpnGw2</span></span>
- <span data-ttu-id="620b7-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="620b7-128">VpnGw3</span></span>

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

### <span data-ttu-id="620b7-129">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="620b7-129">-VirtualNetworkGateway</span></span>
<span data-ttu-id="620b7-130">Specifica un riferimento a un oggetto al gateway di rete virtuale da ridimensionare.</span><span class="sxs-lookup"><span data-stu-id="620b7-130">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="620b7-131">Puoi creare questo riferimento di oggetto usando la Get-AzVirtualNetworkGateway e specificando il nome del gateway.</span><span class="sxs-lookup"><span data-stu-id="620b7-131">You can create this object reference by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="620b7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="620b7-132">CommonParameters</span></span>
<span data-ttu-id="620b7-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="620b7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="620b7-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="620b7-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="620b7-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="620b7-135">INPUTS</span></span>

###  
<span data-ttu-id="620b7-136">Questo cmdlet accetta le istanze pipeline dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="620b7-136">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="620b7-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="620b7-137">OUTPUTS</span></span>

###  
<span data-ttu-id="620b7-138">Questo cmdlet modifica le istanze esistenti dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="620b7-138">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="620b7-139">Note</span><span class="sxs-lookup"><span data-stu-id="620b7-139">NOTES</span></span>
<span data-ttu-id="620b7-140">Non è possibile eseguire il ridimensionamento dagli SKU Basic/standard/HighPerformance alle nuove SKU VpnGw1/VpnGw2/VpnGw3.</span><span class="sxs-lookup"><span data-stu-id="620b7-140">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="620b7-141">Vedere https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways per istruzioni.</span><span class="sxs-lookup"><span data-stu-id="620b7-141">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="620b7-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="620b7-142">RELATED LINKS</span></span>

[<span data-ttu-id="620b7-143">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="620b7-143">Get-AzVpnClientPackage</span></span>](./Get-AzVpnClientPackage.md)

[<span data-ttu-id="620b7-144">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="620b7-144">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="620b7-145">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="620b7-145">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


