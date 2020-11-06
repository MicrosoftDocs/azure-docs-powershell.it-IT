---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 41c94d0dd8401399f360af89f1744cc10e900e1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516191"
---
# <span data-ttu-id="8c168-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8c168-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="8c168-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8c168-102">SYNOPSIS</span></span>
<span data-ttu-id="8c168-103">Aggiorna un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8c168-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c168-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c168-104">SYNTAX</span></span>

### <span data-ttu-id="8c168-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8c168-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c168-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c168-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c168-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c168-107">DESCRIPTION</span></span>
<span data-ttu-id="8c168-108">Il cmdlet **set-AzureRmVirtualNetworkGateway** aggiorna un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8c168-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="8c168-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c168-109">EXAMPLES</span></span>

### <span data-ttu-id="8c168-110">Esempio 1: impostare lo stato dell'obiettivo come gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="8c168-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="8c168-111">Il primo comando ottiene un gateway di rete virtuale denominato Gateway01 che appartiene al gruppo di risorse ResourceGroup001 e lo archivia nella variabile denominata $Gateway</span><span class="sxs-lookup"><span data-stu-id="8c168-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway</span></span>

<span data-ttu-id="8c168-112">Il secondo comando imposta lo stato obiettivo per il gateway di rete virtuale archiviato in $Gateway variabile.</span><span class="sxs-lookup"><span data-stu-id="8c168-112">The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="8c168-113">Il comando imposta anche l'ASN su 1337.</span><span class="sxs-lookup"><span data-stu-id="8c168-113">The command also sets the ASN to 1337.</span></span>

## <span data-ttu-id="8c168-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8c168-114">PARAMETERS</span></span>

### <span data-ttu-id="8c168-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="8c168-115">-Asn</span></span>
<span data-ttu-id="8c168-116">Specifica il codice ASN (Virtual Network Gateway Autonomous System Number) usato per configurare sessioni BGP (Border Gateway Protocol) all'interno di tunnel IPsec.</span><span class="sxs-lookup"><span data-stu-id="8c168-116">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c168-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c168-117">-DefaultProfile</span></span>
<span data-ttu-id="8c168-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8c168-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="8c168-119">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="8c168-119">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="8c168-120">Disabilita la funzionalità Active-Active.</span><span class="sxs-lookup"><span data-stu-id="8c168-120">Disables the active-active feature.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c168-121">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="8c168-121">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="8c168-122">Abilita la funzionalità Active-Active.</span><span class="sxs-lookup"><span data-stu-id="8c168-122">Enables the active-active feature.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c168-123">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="8c168-123">-GatewayDefaultSite</span></span>
<span data-ttu-id="8c168-124">Specifica il sito predefinito da usare per il tunneling forzato.</span><span class="sxs-lookup"><span data-stu-id="8c168-124">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="8c168-125">Se si specifica un sito predefinito, tutto il traffico Internet proveniente dalla rete privata virtuale (VPN) del gateway viene instradato al sito.</span><span class="sxs-lookup"><span data-stu-id="8c168-125">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c168-126">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="8c168-126">-GatewaySku</span></span>
<span data-ttu-id="8c168-127">Specifica l'unità di conservazione delle scorte (SKU) del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8c168-127">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="8c168-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8c168-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8c168-129">Base</span><span class="sxs-lookup"><span data-stu-id="8c168-129">Basic</span></span>
- <span data-ttu-id="8c168-130">Standard</span><span class="sxs-lookup"><span data-stu-id="8c168-130">Standard</span></span>
- <span data-ttu-id="8c168-131">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="8c168-131">HighPerformance</span></span>
- <span data-ttu-id="8c168-132">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="8c168-132">VpnGw1</span></span>
- <span data-ttu-id="8c168-133">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="8c168-133">VpnGw2</span></span>
- <span data-ttu-id="8c168-134">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="8c168-134">VpnGw3</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c168-135">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="8c168-135">-PeerWeight</span></span>
<span data-ttu-id="8c168-136">Specifica il peso aggiunto alle route acquisite su BGP da questo gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="8c168-136">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c168-137">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="8c168-137">-RadiusServerAddress</span></span>
<span data-ttu-id="8c168-138">Indirizzo del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="8c168-138">P2S External Radius server address.</span></span>
```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c168-139">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="8c168-139">-RadiusServerSecret</span></span>
<span data-ttu-id="8c168-140">Segreto del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="8c168-140">P2S External Radius server secret.</span></span>
```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c168-141">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8c168-141">-VirtualNetworkGateway</span></span>
<span data-ttu-id="8c168-142">Specifica l'oggetto gateway di rete virtuale a cui basare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="8c168-142">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="8c168-143">Puoi usare il cmdlet Get-AzureRmVirtualNetworkGateway per ottenere l'oggetto gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8c168-143">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="8c168-144">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="8c168-144">-VpnClientAddressPool</span></span>
<span data-ttu-id="8c168-145">Specifica lo spazio degli indirizzi usato da questo cmdlet per allocare gli indirizzi IP del client VPN.</span><span class="sxs-lookup"><span data-stu-id="8c168-145">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="8c168-146">Questa operazione non deve sovrapporsi a una rete virtuale o a intervalli locali.</span><span class="sxs-lookup"><span data-stu-id="8c168-146">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="8c168-147">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="8c168-147">-VpnClientProtocol</span></span>
<span data-ttu-id="8c168-148">Elenco dei protocolli di tunneling client VPN di P2S</span><span class="sxs-lookup"><span data-stu-id="8c168-148">A list of P2S VPN client tunneling protocols</span></span>
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

### <span data-ttu-id="8c168-149">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="8c168-149">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="8c168-150">Specifica un elenco di certificati client VPN revocati.</span><span class="sxs-lookup"><span data-stu-id="8c168-150">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="8c168-151">Viene rimosso un client VPN che presenta un certificato che corrisponde a uno di questi.</span><span class="sxs-lookup"><span data-stu-id="8c168-151">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="8c168-152">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="8c168-152">-VpnClientRootCertificates</span></span>
<span data-ttu-id="8c168-153">Specifica un elenco di certificati radice client VPN da usare per l'autenticazione del client VPN.</span><span class="sxs-lookup"><span data-stu-id="8c168-153">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="8c168-154">La connessione dei client VPN deve presentare i certificati generati da uno di questi certificati radice.</span><span class="sxs-lookup"><span data-stu-id="8c168-154">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="8c168-155">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8c168-155">-Confirm</span></span>
<span data-ttu-id="8c168-156">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c168-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c168-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c168-157">-WhatIf</span></span>
<span data-ttu-id="8c168-158">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8c168-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c168-159">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8c168-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c168-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c168-160">CommonParameters</span></span>
<span data-ttu-id="8c168-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c168-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c168-162">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c168-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c168-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8c168-163">INPUTS</span></span>

### <span data-ttu-id="8c168-164">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8c168-164">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="8c168-165">Il parametro ' VirtualNetworkGateway ' accetta il valore di tipo ' PSVirtualNetworkGateway ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="8c168-165">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="8c168-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c168-166">OUTPUTS</span></span>

### <span data-ttu-id="8c168-167">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8c168-167">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="8c168-168">Note</span><span class="sxs-lookup"><span data-stu-id="8c168-168">NOTES</span></span>
* <span data-ttu-id="8c168-169">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="8c168-169">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8c168-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c168-170">RELATED LINKS</span></span>

[<span data-ttu-id="8c168-171">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8c168-171">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="8c168-172">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8c168-172">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="8c168-173">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8c168-173">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="8c168-174">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8c168-174">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="8c168-175">Ridimensionare-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8c168-175">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


