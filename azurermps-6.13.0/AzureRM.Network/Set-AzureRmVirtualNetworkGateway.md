---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 1884dd461c0433c4f6a68bf906f56653ca960e27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518620"
---
# <span data-ttu-id="bc784-101">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bc784-101">Set-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="bc784-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bc784-102">SYNOPSIS</span></span>
<span data-ttu-id="bc784-103">Aggiorna un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="bc784-103">Updates a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc784-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc784-104">SYNTAX</span></span>

### <span data-ttu-id="bc784-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bc784-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-VpnClientIpsecPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc784-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc784-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-VpnClientIpsecPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc784-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc784-107">DESCRIPTION</span></span>
<span data-ttu-id="bc784-108">Il cmdlet **set-AzureRmVirtualNetworkGateway** aggiorna un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="bc784-108">The **Set-AzureRmVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="bc784-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc784-109">EXAMPLES</span></span>

### <span data-ttu-id="bc784-110">Esempio 1: impostare lo stato dell'obiettivo come gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="bc784-110">Example 1: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="bc784-111">Il primo comando ottiene un gateway di rete virtuale denominato Gateway01 che appartiene al gruppo di risorse ResourceGroup001 e lo archivia nella variabile denominata $Gateway il secondo comando imposta lo stato obiettivo per il gateway di rete virtuale archiviato in $Gateway variabile.</span><span class="sxs-lookup"><span data-stu-id="bc784-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="bc784-112">Il comando imposta anche l'ASN su 1337.</span><span class="sxs-lookup"><span data-stu-id="bc784-112">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="bc784-113">Esempio 2: impostare lo stato dell'obiettivo come gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="bc784-113">Example 2: Set the goal state a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzureRmVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="bc784-114">Il primo comando ottiene un gateway di rete virtuale denominato Gateway01 che appartiene al gruppo di risorse ResourceGroup001 e lo archivia nella variabile denominata $Gateway il secondo comando crea l'oggetto criteri IPSec VPN in base ai parametri IPSec specificati.</span><span class="sxs-lookup"><span data-stu-id="bc784-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="bc784-115">Il terzo comando imposta lo stato obiettivo per il gateway di rete virtuale archiviato in $Gateway variabile.</span><span class="sxs-lookup"><span data-stu-id="bc784-115">The third command sets the goal state for the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="bc784-116">Il comando imposta anche il criterio IPSec VPN personalizzato specificato nell'oggetto $vpnclientipsecpolicy sul gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="bc784-116">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

## <span data-ttu-id="bc784-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bc784-117">PARAMETERS</span></span>

### <span data-ttu-id="bc784-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc784-118">-AsJob</span></span>
<span data-ttu-id="bc784-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="bc784-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc784-120">-ASN</span><span class="sxs-lookup"><span data-stu-id="bc784-120">-Asn</span></span>
<span data-ttu-id="bc784-121">Specifica il codice ASN (Virtual Network Gateway Autonomous System Number) usato per configurare sessioni BGP (Border Gateway Protocol) all'interno di tunnel IPsec.</span><span class="sxs-lookup"><span data-stu-id="bc784-121">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="bc784-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc784-122">-DefaultProfile</span></span>
<span data-ttu-id="bc784-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bc784-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc784-124">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="bc784-124">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="bc784-125">Disabilita la funzionalità Active-Active.</span><span class="sxs-lookup"><span data-stu-id="bc784-125">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="bc784-126">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="bc784-126">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="bc784-127">Abilita la funzionalità Active-Active.</span><span class="sxs-lookup"><span data-stu-id="bc784-127">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="bc784-128">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="bc784-128">-GatewayDefaultSite</span></span>
<span data-ttu-id="bc784-129">Specifica il sito predefinito da usare per il tunneling forzato.</span><span class="sxs-lookup"><span data-stu-id="bc784-129">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="bc784-130">Se si specifica un sito predefinito, tutto il traffico Internet proveniente dalla rete privata virtuale (VPN) del gateway viene instradato al sito.</span><span class="sxs-lookup"><span data-stu-id="bc784-130">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="bc784-131">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="bc784-131">-GatewaySku</span></span>
<span data-ttu-id="bc784-132">Specifica l'unità di conservazione delle scorte (SKU) del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="bc784-132">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="bc784-133">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="bc784-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bc784-134">Base</span><span class="sxs-lookup"><span data-stu-id="bc784-134">Basic</span></span>
- <span data-ttu-id="bc784-135">Standard</span><span class="sxs-lookup"><span data-stu-id="bc784-135">Standard</span></span>
- <span data-ttu-id="bc784-136">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="bc784-136">HighPerformance</span></span>
- <span data-ttu-id="bc784-137">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="bc784-137">VpnGw1</span></span>
- <span data-ttu-id="bc784-138">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="bc784-138">VpnGw2</span></span>
- <span data-ttu-id="bc784-139">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="bc784-139">VpnGw3</span></span>
- <span data-ttu-id="bc784-140">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="bc784-140">VpnGw1AZ</span></span>
- <span data-ttu-id="bc784-141">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="bc784-141">VpnGw2AZ</span></span>
- <span data-ttu-id="bc784-142">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="bc784-142">VpnGw3AZ</span></span>
- <span data-ttu-id="bc784-143">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="bc784-143">ErGw1AZ</span></span>
- <span data-ttu-id="bc784-144">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="bc784-144">ErGw2AZ</span></span>
- <span data-ttu-id="bc784-145">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="bc784-145">ErGw3AZ</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc784-146">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="bc784-146">-PeerWeight</span></span>
<span data-ttu-id="bc784-147">Specifica il peso aggiunto alle route acquisite su BGP da questo gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="bc784-147">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="bc784-148">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="bc784-148">-RadiusServerAddress</span></span>
<span data-ttu-id="bc784-149">Indirizzo del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="bc784-149">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="bc784-150">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="bc784-150">-RadiusServerSecret</span></span>
<span data-ttu-id="bc784-151">Segreto del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="bc784-151">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="bc784-152">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bc784-152">-VirtualNetworkGateway</span></span>
<span data-ttu-id="bc784-153">Specifica l'oggetto gateway di rete virtuale a cui basare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="bc784-153">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="bc784-154">Puoi usare il cmdlet Get-AzureRmVirtualNetworkGateway per ottenere l'oggetto gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="bc784-154">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="bc784-155">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="bc784-155">-VpnClientAddressPool</span></span>
<span data-ttu-id="bc784-156">Specifica lo spazio degli indirizzi usato da questo cmdlet per allocare gli indirizzi IP del client VPN.</span><span class="sxs-lookup"><span data-stu-id="bc784-156">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="bc784-157">Questa operazione non deve sovrapporsi a una rete virtuale o a intervalli locali.</span><span class="sxs-lookup"><span data-stu-id="bc784-157">This should not overlap with virtual network or on-premise ranges.</span></span>

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

### <span data-ttu-id="bc784-158">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="bc784-158">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="bc784-159">Elenco dei criteri IPSec per i protocolli di tunneling client VPN di P2S.</span><span class="sxs-lookup"><span data-stu-id="bc784-159">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc784-160">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="bc784-160">-VpnClientProtocol</span></span>
<span data-ttu-id="bc784-161">Elenco dei protocolli di tunneling client VPN di P2S</span><span class="sxs-lookup"><span data-stu-id="bc784-161">A list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc784-162">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="bc784-162">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="bc784-163">Specifica un elenco di certificati client VPN revocati.</span><span class="sxs-lookup"><span data-stu-id="bc784-163">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="bc784-164">Viene rimosso un client VPN che presenta un certificato che corrisponde a uno di questi.</span><span class="sxs-lookup"><span data-stu-id="bc784-164">A VPN client presenting a certificate that matches one of these is removed.</span></span>

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

### <span data-ttu-id="bc784-165">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="bc784-165">-VpnClientRootCertificates</span></span>
<span data-ttu-id="bc784-166">Specifica un elenco di certificati radice client VPN da usare per l'autenticazione del client VPN.</span><span class="sxs-lookup"><span data-stu-id="bc784-166">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="bc784-167">La connessione dei client VPN deve presentare i certificati generati da uno di questi certificati radice.</span><span class="sxs-lookup"><span data-stu-id="bc784-167">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

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

### <span data-ttu-id="bc784-168">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bc784-168">-Confirm</span></span>
<span data-ttu-id="bc784-169">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc784-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc784-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc784-170">-WhatIf</span></span>
<span data-ttu-id="bc784-171">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc784-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc784-172">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bc784-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc784-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc784-173">CommonParameters</span></span>
<span data-ttu-id="bc784-174">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc784-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc784-175">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc784-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc784-176">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bc784-176">INPUTS</span></span>

### <span data-ttu-id="bc784-177">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bc784-177">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="bc784-178">Parametri: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bc784-178">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="bc784-179">System. String</span><span class="sxs-lookup"><span data-stu-id="bc784-179">System.String</span></span>

### <span data-ttu-id="bc784-180">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bc784-180">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="bc784-181">System. Collections. Generic. list ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="bc784-181">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="bc784-182">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bc784-182">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="bc784-183">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bc784-183">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="bc784-184">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bc784-184">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="bc784-185">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="bc784-185">System.UInt32</span></span>

### <span data-ttu-id="bc784-186">System. Int32</span><span class="sxs-lookup"><span data-stu-id="bc784-186">System.Int32</span></span>

### <span data-ttu-id="bc784-187">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="bc784-187">System.Security.SecureString</span></span>

## <span data-ttu-id="bc784-188">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc784-188">OUTPUTS</span></span>

### <span data-ttu-id="bc784-189">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bc784-189">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="bc784-190">Note</span><span class="sxs-lookup"><span data-stu-id="bc784-190">NOTES</span></span>
* <span data-ttu-id="bc784-191">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="bc784-191">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bc784-192">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc784-192">RELATED LINKS</span></span>

[<span data-ttu-id="bc784-193">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bc784-193">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="bc784-194">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bc784-194">New-AzureRmVirtualNetworkGateway</span></span>](./New-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="bc784-195">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bc784-195">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="bc784-196">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bc784-196">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="bc784-197">Ridimensionare-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bc784-197">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


