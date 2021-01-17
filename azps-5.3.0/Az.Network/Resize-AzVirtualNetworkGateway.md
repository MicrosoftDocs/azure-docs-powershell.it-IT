---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: dd48af6a0f20cafea5911adb629a83323faa94a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488912"
---
# <span data-ttu-id="ba8bc-101">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ba8bc-101">Resize-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="ba8bc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ba8bc-102">SYNOPSIS</span></span>
<span data-ttu-id="ba8bc-103">Ridimensiona un gateway di rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="ba8bc-103">Resizes an existing virtual network gateway.</span></span>

## <span data-ttu-id="ba8bc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba8bc-104">SYNTAX</span></span>

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba8bc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba8bc-105">DESCRIPTION</span></span>
<span data-ttu-id="ba8bc-106">Il cmdlet **Resize-AzVirtualNetworkGateway** consente di modificare l'unità di stoccaggio (SKU) per un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ba8bc-106">The **Resize-AzVirtualNetworkGateway** cmdlet enables you to change the stock-keeping unit (SKU) for a virtual network gateway.</span></span>
<span data-ttu-id="ba8bc-107">Gli SKU determinano le funzionalità di un gateway, inclusi elementi come la velocità effettiva e il numero massimo di tunnel IP consentiti.</span><span class="sxs-lookup"><span data-stu-id="ba8bc-107">SKUs determine the capabilities of a gateway, including such things as throughput and the maximum number of IP tunnels that are allowed.</span></span>
<span data-ttu-id="ba8bc-108">Azure supporta le SKU di base, standard, ad alte prestazioni, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ, in alcuni casi indicati come SKU di piccole, medie e grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="ba8bc-108">Azure supports Basic, Standard, High-Performance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ SKUs (sometimes referred to as Small, Medium, and Large SKUs).</span></span>
<span data-ttu-id="ba8bc-109">Per informazioni dettagliate sulle funzionalità di ogni tipo di SKU, vedere https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .</span><span class="sxs-lookup"><span data-stu-id="ba8bc-109">For detailed information about the capabilities of each SKU type, see https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/.</span></span>
<span data-ttu-id="ba8bc-110">Tieni presente che le SKU si differenziano per i prezzi e le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ba8bc-110">Keep in mind that SKUs differ in pricing as well as capabilities.</span></span>
<span data-ttu-id="ba8bc-111">Per altre informazioni, vedere https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .</span><span class="sxs-lookup"><span data-stu-id="ba8bc-111">For more information, see https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/.</span></span>

## <span data-ttu-id="ba8bc-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba8bc-112">EXAMPLES</span></span>

### <span data-ttu-id="ba8bc-113">Esempio 1: modificare le dimensioni di un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="ba8bc-113">Example 1: Change the size of a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

<span data-ttu-id="ba8bc-114">Questo esempio modifica le dimensioni di un gateway di rete virtuale denominato ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="ba8bc-114">This example changes the size of a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="ba8bc-115">Il primo comando crea un riferimento all'oggetto a ContosoVirtualGateway; Questo riferimento oggetto è archiviato in una variabile denominata $Gateway.</span><span class="sxs-lookup"><span data-stu-id="ba8bc-115">The first command creates an object reference to ContosoVirtualGateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="ba8bc-116">Il secondo comando usa quindi il cmdlet **Resize-AzVirtualNetworkGateway** per impostare la proprietà *GatewaySku* su Basic.</span><span class="sxs-lookup"><span data-stu-id="ba8bc-116">The second command then uses the **Resize-AzVirtualNetworkGateway** cmdlet to set the *GatewaySku* property to Basic.</span></span>

## <span data-ttu-id="ba8bc-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ba8bc-117">PARAMETERS</span></span>

### <span data-ttu-id="ba8bc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba8bc-118">-DefaultProfile</span></span>
<span data-ttu-id="ba8bc-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba8bc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba8bc-120">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="ba8bc-120">-GatewaySku</span></span>
<span data-ttu-id="ba8bc-121">Specifica il nuovo tipo di SKU gateway.</span><span class="sxs-lookup"><span data-stu-id="ba8bc-121">Specifies the new type of gateway SKU.</span></span>
<span data-ttu-id="ba8bc-122">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ba8bc-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ba8bc-123">Base</span><span class="sxs-lookup"><span data-stu-id="ba8bc-123">Basic</span></span>
- <span data-ttu-id="ba8bc-124">Standard</span><span class="sxs-lookup"><span data-stu-id="ba8bc-124">Standard</span></span>
- <span data-ttu-id="ba8bc-125">Prestazioni elevate</span><span class="sxs-lookup"><span data-stu-id="ba8bc-125">High Performance</span></span>
- <span data-ttu-id="ba8bc-126">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="ba8bc-126">VpnGw1</span></span>
- <span data-ttu-id="ba8bc-127">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="ba8bc-127">VpnGw2</span></span>
- <span data-ttu-id="ba8bc-128">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="ba8bc-128">VpnGw3</span></span>
- <span data-ttu-id="ba8bc-129">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="ba8bc-129">VpnGw1AZ</span></span> 
- <span data-ttu-id="ba8bc-130">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="ba8bc-130">VpnGw2AZ</span></span> 
- <span data-ttu-id="ba8bc-131">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="ba8bc-131">VpnGw3AZ</span></span> 
- <span data-ttu-id="ba8bc-132">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="ba8bc-132">ErGw1AZ</span></span> 
- <span data-ttu-id="ba8bc-133">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="ba8bc-133">ErGw2AZ</span></span> 
- <span data-ttu-id="ba8bc-134">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="ba8bc-134">ErGw3AZ</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba8bc-135">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ba8bc-135">-VirtualNetworkGateway</span></span>
<span data-ttu-id="ba8bc-136">Specifica un riferimento a un oggetto al gateway di rete virtuale da ridimensionare.</span><span class="sxs-lookup"><span data-stu-id="ba8bc-136">Specifies an object reference to the virtual network gateway to be resized.</span></span>
<span data-ttu-id="ba8bc-137">Puoi creare questo riferimento di oggetto usando la Get-AzVirtualNetworkGateway e specificando il nome del gateway.</span><span class="sxs-lookup"><span data-stu-id="ba8bc-137">You can create this object reference by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="ba8bc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba8bc-138">CommonParameters</span></span>
<span data-ttu-id="ba8bc-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba8bc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba8bc-140">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba8bc-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba8bc-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ba8bc-141">INPUTS</span></span>

### <span data-ttu-id="ba8bc-142">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ba8bc-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="ba8bc-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ba8bc-143">System.String</span></span>

## <span data-ttu-id="ba8bc-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba8bc-144">OUTPUTS</span></span>

### <span data-ttu-id="ba8bc-145">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ba8bc-145">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="ba8bc-146">Note</span><span class="sxs-lookup"><span data-stu-id="ba8bc-146">NOTES</span></span>
<span data-ttu-id="ba8bc-147">Non è possibile eseguire il ridimensionamento dagli SKU Basic/standard/HighPerformance alle nuove SKU VpnGw1/VpnGw2/VpnGw3.</span><span class="sxs-lookup"><span data-stu-id="ba8bc-147">You cannot resize from Basic/Standard/HighPerformance SKUs to the new VpnGw1/VpnGw2/VpnGw3 SKUs.</span></span> <span data-ttu-id="ba8bc-148">Il ridimensionamento ulteriore non è consentito da/a VpnGw1AZ/VpnGw2AZ/VpnGw3AZ o ErGw1AZ/ErGw2AZ/ErGw3AZ.</span><span class="sxs-lookup"><span data-stu-id="ba8bc-148">Further resize is not allowed from/to VpnGw1AZ/VpnGw2AZ/VpnGw3AZ or ErGw1AZ/ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="ba8bc-149">Il ridimensionamento è consentito solo all'interno della serie SKU, ad esempio VpnGw1AZ può essere ridimensionato in/da VpnGw2AZ/VpnGw3AZ e ErGw1AZ può essere ridimensionato in/da ErGw2AZ/ErGw3AZ.</span><span class="sxs-lookup"><span data-stu-id="ba8bc-149">Resize is allowed only within the SKU 'series' e.g VpnGw1AZ can be resized to/from VpnGw2AZ/VpnGw3AZ and ErGw1AZ can be resized to/from ErGw2AZ/ErGw3AZ.</span></span> <span data-ttu-id="ba8bc-150">Vedere https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways per istruzioni.</span><span class="sxs-lookup"><span data-stu-id="ba8bc-150">See https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngateways for instructions.</span></span>

## <span data-ttu-id="ba8bc-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba8bc-151">RELATED LINKS</span></span>

[<span data-ttu-id="ba8bc-152">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ba8bc-152">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ba8bc-153">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ba8bc-153">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ba8bc-154">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ba8bc-154">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ba8bc-155">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ba8bc-155">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ba8bc-156">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ba8bc-156">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ba8bc-157">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="ba8bc-157">Get-AzVpnClientPackage</span></span>](./Get-AzVpnClientPackage.md)

[<span data-ttu-id="ba8bc-158">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="ba8bc-158">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)
