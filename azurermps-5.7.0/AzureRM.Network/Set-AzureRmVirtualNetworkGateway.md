---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 013da22d02f091d49e9780585bb8648c9c895ad7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512499"
---
# <span data-ttu-id="d1ec3-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d1ec3-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="d1ec3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1ec3-102">SYNOPSIS</span></span>
<span data-ttu-id="d1ec3-103">Aggiorna un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1ec3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1ec3-104">SYNTAX</span></span>

### <span data-ttu-id="d1ec3-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d1ec3-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1ec3-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1ec3-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1ec3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1ec3-107">DESCRIPTION</span></span>
<span data-ttu-id="d1ec3-108">Il cmdlet **set-AzureRmVirtualNetworkGateway** aggiorna un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="d1ec3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1ec3-109">EXAMPLES</span></span>

### <span data-ttu-id="d1ec3-110">Esempio 1: impostare lo stato dell'obiettivo come gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="d1ec3-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="d1ec3-111">Il primo comando ottiene un gateway di rete virtuale denominato Gateway01 che appartiene al gruppo di risorse ResourceGroup001 e lo archivia nella variabile denominata $Gateway</span><span class="sxs-lookup"><span data-stu-id="d1ec3-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway</span></span>

<span data-ttu-id="d1ec3-112">Il secondo comando imposta lo stato obiettivo per il gateway di rete virtuale archiviato in $Gateway variabile.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-112">The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="d1ec3-113">Il comando imposta anche l'ASN su 1337.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-113">The command also sets the ASN to 1337.</span></span>

## <span data-ttu-id="d1ec3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1ec3-114">PARAMETERS</span></span>

### <span data-ttu-id="d1ec3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1ec3-115">-AsJob</span></span>
<span data-ttu-id="d1ec3-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d1ec3-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1ec3-117">-ASN</span><span class="sxs-lookup"><span data-stu-id="d1ec3-117">-Asn</span></span>
<span data-ttu-id="d1ec3-118">Specifica il codice ASN (Virtual Network Gateway Autonomous System Number) usato per configurare sessioni BGP (Border Gateway Protocol) all'interno di tunnel IPsec.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-118">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ec3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1ec3-119">-DefaultProfile</span></span>
<span data-ttu-id="d1ec3-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="d1ec3-121">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="d1ec3-121">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="d1ec3-122">Disabilita la funzionalità Active-Active.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-122">Disables the active-active feature.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1ec3-123">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="d1ec3-123">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="d1ec3-124">Abilita la funzionalità Active-Active.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-124">Enables the active-active feature.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1ec3-125">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="d1ec3-125">-GatewayDefaultSite</span></span>
<span data-ttu-id="d1ec3-126">Specifica il sito predefinito da usare per il tunneling forzato.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-126">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="d1ec3-127">Se si specifica un sito predefinito, tutto il traffico Internet proveniente dalla rete privata virtuale (VPN) del gateway viene instradato al sito.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-127">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ec3-128">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="d1ec3-128">-GatewaySku</span></span>
<span data-ttu-id="d1ec3-129">Specifica l'unità di conservazione delle scorte (SKU) del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-129">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="d1ec3-130">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d1ec3-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d1ec3-131">Base</span><span class="sxs-lookup"><span data-stu-id="d1ec3-131">Basic</span></span>
- <span data-ttu-id="d1ec3-132">Standard</span><span class="sxs-lookup"><span data-stu-id="d1ec3-132">Standard</span></span>
- <span data-ttu-id="d1ec3-133">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="d1ec3-133">HighPerformance</span></span>
- <span data-ttu-id="d1ec3-134">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="d1ec3-134">VpnGw1</span></span>
- <span data-ttu-id="d1ec3-135">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="d1ec3-135">VpnGw2</span></span>
- <span data-ttu-id="d1ec3-136">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="d1ec3-136">VpnGw3</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ec3-137">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="d1ec3-137">-PeerWeight</span></span>
<span data-ttu-id="d1ec3-138">Specifica il peso aggiunto alle route acquisite su BGP da questo gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="d1ec3-138">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ec3-139">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="d1ec3-139">-RadiusServerAddress</span></span>
<span data-ttu-id="d1ec3-140">Indirizzo del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-140">P2S External Radius server address.</span></span>
```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ec3-141">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="d1ec3-141">-RadiusServerSecret</span></span>
<span data-ttu-id="d1ec3-142">Segreto del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-142">P2S External Radius server secret.</span></span>
```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ec3-143">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d1ec3-143">-VirtualNetworkGateway</span></span>
<span data-ttu-id="d1ec3-144">Specifica l'oggetto gateway di rete virtuale a cui basare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-144">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="d1ec3-145">Puoi usare il cmdlet Get-AzureRmVirtualNetworkGateway per ottenere l'oggetto gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-145">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="d1ec3-146">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="d1ec3-146">-VpnClientAddressPool</span></span>
<span data-ttu-id="d1ec3-147">Specifica lo spazio degli indirizzi usato da questo cmdlet per allocare gli indirizzi IP del client VPN.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-147">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="d1ec3-148">Questa operazione non deve sovrapporsi a una rete virtuale o a intervalli locali.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-148">This should not overlap with virtual network or on-premise ranges.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ec3-149">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="d1ec3-149">-VpnClientProtocol</span></span>
<span data-ttu-id="d1ec3-150">Elenco dei protocolli di tunneling client VPN di P2S</span><span class="sxs-lookup"><span data-stu-id="d1ec3-150">A list of P2S VPN client tunneling protocols</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 
Accepted values: SSTP, IkeV2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ec3-151">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="d1ec3-151">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="d1ec3-152">Specifica un elenco di certificati client VPN revocati.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-152">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="d1ec3-153">Viene rimosso un client VPN che presenta un certificato che corrisponde a uno di questi.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-153">A VPN client presenting a certificate that matches one of these is removed.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ec3-154">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="d1ec3-154">-VpnClientRootCertificates</span></span>
<span data-ttu-id="d1ec3-155">Specifica un elenco di certificati radice client VPN da usare per l'autenticazione del client VPN.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-155">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="d1ec3-156">La connessione dei client VPN deve presentare i certificati generati da uno di questi certificati radice.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-156">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1ec3-157">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d1ec3-157">-Confirm</span></span>
<span data-ttu-id="d1ec3-158">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1ec3-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1ec3-159">-WhatIf</span></span>
<span data-ttu-id="d1ec3-160">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1ec3-161">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-161">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1ec3-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1ec3-162">CommonParameters</span></span>
<span data-ttu-id="d1ec3-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1ec3-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1ec3-164">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1ec3-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1ec3-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1ec3-165">INPUTS</span></span>

### <span data-ttu-id="d1ec3-166">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d1ec3-166">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="d1ec3-167">Il parametro ' VirtualNetworkGateway ' accetta il valore di tipo ' PSVirtualNetworkGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="d1ec3-167">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="d1ec3-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1ec3-168">OUTPUTS</span></span>

### <span data-ttu-id="d1ec3-169">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d1ec3-169">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="d1ec3-170">Note</span><span class="sxs-lookup"><span data-stu-id="d1ec3-170">NOTES</span></span>
* <span data-ttu-id="d1ec3-171">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="d1ec3-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d1ec3-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1ec3-172">RELATED LINKS</span></span>

[<span data-ttu-id="d1ec3-173">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d1ec3-173">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="d1ec3-174">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d1ec3-174">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="d1ec3-175">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d1ec3-175">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="d1ec3-176">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d1ec3-176">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="d1ec3-177">Ridimensionare-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d1ec3-177">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


