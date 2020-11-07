---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5C309071-A2ED-464C-9197-0A77859C8FBB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGateway.md
ms.openlocfilehash: 6576cedfa49d2ba2215d72b7f31ea85288f5cbda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677920"
---
# <span data-ttu-id="1fb94-101">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1fb94-101">Set-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="1fb94-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1fb94-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb94-103">Aggiorna un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="1fb94-103">Updates a virtual network gateway.</span></span>

## <span data-ttu-id="1fb94-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1fb94-104">SYNTAX</span></span>

### <span data-ttu-id="1fb94-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1fb94-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fb94-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fb94-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-EnableActiveActiveFeature] [-DisableActiveActiveFeature]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fb94-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1fb94-107">DESCRIPTION</span></span>
<span data-ttu-id="1fb94-108">Il cmdlet **set-AzVirtualNetworkGateway** aggiorna un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="1fb94-108">The **Set-AzVirtualNetworkGateway** cmdlet updates a virtual network gateway.</span></span>

## <span data-ttu-id="1fb94-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1fb94-109">EXAMPLES</span></span>

### <span data-ttu-id="1fb94-110">Esempio 1: aggiornare l'ASN di un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="1fb94-110">Example 1: Update a virtual network gateway's ASN</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -Asn 1337
```

<span data-ttu-id="1fb94-111">Il primo comando ottiene un gateway di rete virtuale denominato Gateway01 che appartiene al gruppo di risorse ResourceGroup001 e lo archivia nella variabile denominata $Gateway il secondo comando Aggiorna il gateway di rete virtuale archiviato in $Gateway variabile.</span><span class="sxs-lookup"><span data-stu-id="1fb94-111">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="1fb94-112">Il comando imposta anche l'ASN su 1337.</span><span class="sxs-lookup"><span data-stu-id="1fb94-112">The command also sets the ASN to 1337.</span></span>

### <span data-ttu-id="1fb94-113">Esempio 2: aggiungere criteri IPsec a un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="1fb94-113">Example 2: Add IPsec policy to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -ResourceGroupName "ResourceGroup001" -Name "Gateway001"
PS C:\> $vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86472 -SADataSizeKilobytes 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
PS C:\> $gateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="1fb94-114">Il primo comando ottiene un gateway di rete virtuale denominato Gateway01 che appartiene al gruppo di risorse ResourceGroup001 e lo archivia nella variabile denominata $Gateway il secondo comando crea l'oggetto criteri IPSec VPN in base ai parametri IPSec specificati.</span><span class="sxs-lookup"><span data-stu-id="1fb94-114">The first command gets a virtual network gateway named Gateway01 that belongs to resource group ResourceGroup001 and stores it to the variable named $Gateway The second command creates the Vpn ipsec policy object as per specified ipsec parameters.</span></span>
<span data-ttu-id="1fb94-115">Il terzo comando Aggiorna il gateway di rete virtuale archiviato in $Gateway variabile.</span><span class="sxs-lookup"><span data-stu-id="1fb94-115">The third command updates the virtual network gateway stored in variable $Gateway.</span></span>
<span data-ttu-id="1fb94-116">Il comando imposta anche il criterio IPSec VPN personalizzato specificato nell'oggetto $vpnclientipsecpolicy sul gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="1fb94-116">The command also sets the custom vpn ipsec policy specified in the $vpnclientipsecpolicy object on Virtual network gateway.</span></span>

## <span data-ttu-id="1fb94-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1fb94-117">PARAMETERS</span></span>

### <span data-ttu-id="1fb94-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fb94-118">-AsJob</span></span>
<span data-ttu-id="1fb94-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1fb94-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1fb94-120">-ASN</span><span class="sxs-lookup"><span data-stu-id="1fb94-120">-Asn</span></span>
<span data-ttu-id="1fb94-121">Specifica il codice ASN (Virtual Network Gateway Autonomous System Number) usato per configurare sessioni BGP (Border Gateway Protocol) all'interno di tunnel IPsec.</span><span class="sxs-lookup"><span data-stu-id="1fb94-121">Specifies the virtual network gateway Autonomous System Number (ASN) that is used to set up Border Gateway Protocol (BGP) sessions inside IPsec tunnels.</span></span>

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

### <span data-ttu-id="1fb94-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb94-122">-DefaultProfile</span></span>
<span data-ttu-id="1fb94-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1fb94-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fb94-124">-DisableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="1fb94-124">-DisableActiveActiveFeature</span></span>
<span data-ttu-id="1fb94-125">Disabilita la funzionalità Active-Active.</span><span class="sxs-lookup"><span data-stu-id="1fb94-125">Disables the active-active feature.</span></span>

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

### <span data-ttu-id="1fb94-126">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="1fb94-126">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="1fb94-127">Abilita la funzionalità Active-Active.</span><span class="sxs-lookup"><span data-stu-id="1fb94-127">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="1fb94-128">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="1fb94-128">-GatewayDefaultSite</span></span>
<span data-ttu-id="1fb94-129">Specifica il sito predefinito da usare per il tunneling forzato.</span><span class="sxs-lookup"><span data-stu-id="1fb94-129">Specifies the default site to use for force tunneling.</span></span>
<span data-ttu-id="1fb94-130">Se si specifica un sito predefinito, tutto il traffico Internet proveniente dalla rete privata virtuale (VPN) del gateway viene instradato al sito.</span><span class="sxs-lookup"><span data-stu-id="1fb94-130">If a default site is specified, all internet traffic from the gateway's Virtual Private Network (VPN) is routed to that site.</span></span>

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

### <span data-ttu-id="1fb94-131">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="1fb94-131">-GatewaySku</span></span>
<span data-ttu-id="1fb94-132">Specifica l'unità di conservazione delle scorte (SKU) del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="1fb94-132">Specifies the stock keeping unit (SKU) of the virtual network gateway.</span></span>
<span data-ttu-id="1fb94-133">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1fb94-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1fb94-134">Base</span><span class="sxs-lookup"><span data-stu-id="1fb94-134">Basic</span></span>
- <span data-ttu-id="1fb94-135">Standard</span><span class="sxs-lookup"><span data-stu-id="1fb94-135">Standard</span></span>
- <span data-ttu-id="1fb94-136">HighPerformance</span><span class="sxs-lookup"><span data-stu-id="1fb94-136">HighPerformance</span></span>
- <span data-ttu-id="1fb94-137">VpnGw1</span><span class="sxs-lookup"><span data-stu-id="1fb94-137">VpnGw1</span></span>
- <span data-ttu-id="1fb94-138">VpnGw2</span><span class="sxs-lookup"><span data-stu-id="1fb94-138">VpnGw2</span></span>
- <span data-ttu-id="1fb94-139">VpnGw3</span><span class="sxs-lookup"><span data-stu-id="1fb94-139">VpnGw3</span></span>
- <span data-ttu-id="1fb94-140">VpnGw1AZ</span><span class="sxs-lookup"><span data-stu-id="1fb94-140">VpnGw1AZ</span></span>
- <span data-ttu-id="1fb94-141">VpnGw2AZ</span><span class="sxs-lookup"><span data-stu-id="1fb94-141">VpnGw2AZ</span></span>
- <span data-ttu-id="1fb94-142">VpnGw3AZ</span><span class="sxs-lookup"><span data-stu-id="1fb94-142">VpnGw3AZ</span></span>
- <span data-ttu-id="1fb94-143">ErGw1AZ</span><span class="sxs-lookup"><span data-stu-id="1fb94-143">ErGw1AZ</span></span>
- <span data-ttu-id="1fb94-144">ErGw2AZ</span><span class="sxs-lookup"><span data-stu-id="1fb94-144">ErGw2AZ</span></span>
- <span data-ttu-id="1fb94-145">ErGw3AZ</span><span class="sxs-lookup"><span data-stu-id="1fb94-145">ErGw3AZ</span></span>

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

### <span data-ttu-id="1fb94-146">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="1fb94-146">-PeerWeight</span></span>
<span data-ttu-id="1fb94-147">Specifica il peso aggiunto alle route acquisite su BGP da questo gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="1fb94-147">Specifies the weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="1fb94-148">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="1fb94-148">-RadiusServerAddress</span></span>
<span data-ttu-id="1fb94-149">Indirizzo del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="1fb94-149">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="1fb94-150">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="1fb94-150">-RadiusServerSecret</span></span>
<span data-ttu-id="1fb94-151">Segreto del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="1fb94-151">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="1fb94-152">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1fb94-152">-VirtualNetworkGateway</span></span>
<span data-ttu-id="1fb94-153">Specifica l'oggetto gateway di rete virtuale a cui basare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="1fb94-153">Specifies the virtual network gateway object to base modifications off of.</span></span>
<span data-ttu-id="1fb94-154">Puoi usare il cmdlet Get-AzVirtualNetworkGateway per ottenere l'oggetto gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="1fb94-154">You can use the Get-AzVirtualNetworkGateway cmdlet to get the virtual network gateway object.</span></span>

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

### <span data-ttu-id="1fb94-155">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="1fb94-155">-VpnClientAddressPool</span></span>
<span data-ttu-id="1fb94-156">Specifica lo spazio degli indirizzi usato da questo cmdlet per allocare gli indirizzi IP del client VPN.</span><span class="sxs-lookup"><span data-stu-id="1fb94-156">Specifies the address space that this cmdlet uses to allocate VPN client IP addresses from.</span></span>
<span data-ttu-id="1fb94-157">Questa operazione non deve sovrapporsi a una rete virtuale o a intervalli locali.</span><span class="sxs-lookup"><span data-stu-id="1fb94-157">This should not overlap with virtual network or on-premise ranges.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fb94-158">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="1fb94-158">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="1fb94-159">Elenco dei criteri IPSec per i protocolli di tunneling client VPN di P2S.</span><span class="sxs-lookup"><span data-stu-id="1fb94-159">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fb94-160">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="1fb94-160">-VpnClientProtocol</span></span>
<span data-ttu-id="1fb94-161">Elenco dei protocolli di tunneling client VPN di P2S</span><span class="sxs-lookup"><span data-stu-id="1fb94-161">A list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fb94-162">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="1fb94-162">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="1fb94-163">Specifica un elenco di certificati client VPN revocati.</span><span class="sxs-lookup"><span data-stu-id="1fb94-163">Specifies a list of revoked VPN client certificates.</span></span>
<span data-ttu-id="1fb94-164">Viene rimosso un client VPN che presenta un certificato che corrisponde a uno di questi.</span><span class="sxs-lookup"><span data-stu-id="1fb94-164">A VPN client presenting a certificate that matches one of these is removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fb94-165">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="1fb94-165">-VpnClientRootCertificates</span></span>
<span data-ttu-id="1fb94-166">Specifica un elenco di certificati radice client VPN da usare per l'autenticazione del client VPN.</span><span class="sxs-lookup"><span data-stu-id="1fb94-166">Specifies a list of VPN client root certificates to use for VPN client authentication.</span></span>
<span data-ttu-id="1fb94-167">La connessione dei client VPN deve presentare i certificati generati da uno di questi certificati radice.</span><span class="sxs-lookup"><span data-stu-id="1fb94-167">Connecting VPN clients must present certificates generated from one of these root certificates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fb94-168">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1fb94-168">-Confirm</span></span>
<span data-ttu-id="1fb94-169">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fb94-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fb94-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fb94-170">-WhatIf</span></span>
<span data-ttu-id="1fb94-171">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1fb94-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1fb94-172">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1fb94-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fb94-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb94-173">CommonParameters</span></span>
<span data-ttu-id="1fb94-174">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fb94-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fb94-175">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fb94-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb94-176">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1fb94-176">INPUTS</span></span>

### <span data-ttu-id="1fb94-177">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1fb94-177">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="1fb94-178">System. String</span><span class="sxs-lookup"><span data-stu-id="1fb94-178">System.String</span></span>

### <span data-ttu-id="1fb94-179">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1fb94-179">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="1fb94-180">System. String []</span><span class="sxs-lookup"><span data-stu-id="1fb94-180">System.String[]</span></span>

### <span data-ttu-id="1fb94-181">Microsoft. Azure. Commands. Network. Models. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="1fb94-181">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="1fb94-182">Microsoft. Azure. Commands. Network. Models. PSVpnClientRevokedCertificate []</span><span class="sxs-lookup"><span data-stu-id="1fb94-182">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="1fb94-183">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="1fb94-183">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="1fb94-184">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="1fb94-184">System.UInt32</span></span>

### <span data-ttu-id="1fb94-185">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1fb94-185">System.Int32</span></span>

### <span data-ttu-id="1fb94-186">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="1fb94-186">System.Security.SecureString</span></span>

## <span data-ttu-id="1fb94-187">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1fb94-187">OUTPUTS</span></span>

### <span data-ttu-id="1fb94-188">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1fb94-188">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="1fb94-189">Note</span><span class="sxs-lookup"><span data-stu-id="1fb94-189">NOTES</span></span>
* <span data-ttu-id="1fb94-190">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="1fb94-190">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="1fb94-191">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1fb94-191">RELATED LINKS</span></span>

[<span data-ttu-id="1fb94-192">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1fb94-192">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1fb94-193">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1fb94-193">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1fb94-194">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1fb94-194">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1fb94-195">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1fb94-195">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1fb94-196">Ridimensionare-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1fb94-196">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)
