---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 6f0a18211ae7c9d2fe8ffcb9c653de9952691e94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519898"
---
# <span data-ttu-id="a609a-101">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a609a-101">New-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="a609a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a609a-102">SYNOPSIS</span></span>
<span data-ttu-id="a609a-103">Crea un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a609a-103">Creates a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a609a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a609a-104">SYNTAX</span></span>

### <span data-ttu-id="a609a-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a609a-105">Default (Default)</span></span>
```
New-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a609a-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a609a-106">RadiusServerConfiguration</span></span>
```
New-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a609a-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a609a-107">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGateway
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a609a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a609a-108">DESCRIPTION</span></span>
<span data-ttu-id="a609a-109">Il gateway di rete virtuale è l'oggetto che rappresenta il gateway in Azure.</span><span class="sxs-lookup"><span data-stu-id="a609a-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="a609a-110">Il cmdlet **New-AzureRmVirtualNetworkGateway** crea l'oggetto del gateway in Azure in base al nome, al nome del gruppo di risorse, alla posizione e alla configurazione IP, oltre al tipo di gateway e alla rete VPN, ovvero il tipo di VPN.</span><span class="sxs-lookup"><span data-stu-id="a609a-110">The **New-AzureRmVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="a609a-111">È anche possibile assegnare un nome alla SKU gateway.</span><span class="sxs-lookup"><span data-stu-id="a609a-111">You can also name the Gateway SKU.</span></span>

<span data-ttu-id="a609a-112">Se questo gateway viene usato per le connessioni Point-to-site, sarà necessario includere anche il pool di indirizzi del client VPN da cui assegnare gli indirizzi ai client di connessione e il certificato radice del client VPN usato per autenticare i client VPN che si connettono al gateway.</span><span class="sxs-lookup"><span data-stu-id="a609a-112">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>

<span data-ttu-id="a609a-113">Puoi anche scegliere di includere altre caratteristiche come BGP e Active-Active.</span><span class="sxs-lookup"><span data-stu-id="a609a-113">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="a609a-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a609a-114">EXAMPLES</span></span>

### <span data-ttu-id="a609a-115">1: creare un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a609a-115">1: Create a Virtual Network Gateway</span></span>
```
New-AzureRmResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzureRMVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzureRMPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzureRmVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzureRMVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzureRmVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic"
```

<span data-ttu-id="a609a-116">Quanto sopra creerà un gruppo di risorse, richiederà un indirizzo IP pubblico, creerà una rete virtuale e una subnet e creerà un gateway di rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="a609a-116">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="a609a-117">Il gateway verrà chiamato "myNGW" nel gruppo di risorse "VNET-gateway" nella posizione "UK West" con le configurazioni IP create in precedenza salvate nella variabile "ngwIPConfig", il tipo di gateway "VPN", il tipo di VPN "RouteBased" e l'USK "Basic".</span><span class="sxs-lookup"><span data-stu-id="a609a-117">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="a609a-118">2: creare un gateway di rete virtuale con configurazione RADIUS esterna</span><span class="sxs-lookup"><span data-stu-id="a609a-118">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```
New-AzureRmResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzureRMVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzureRMPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzureRmVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzureRMVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzureRmVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="a609a-119">Quanto sopra creerà un gruppo di risorse, richiederà un indirizzo IP pubblico, creerà una rete virtuale e una subnet e creerà un gateway di rete virtuale in Azure.</span><span class="sxs-lookup"><span data-stu-id="a609a-119">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="a609a-120">Il gateway verrà chiamato "myNGW" nel gruppo di risorse "VNET-gateway" nella posizione "UK West" con le configurazioni IP create in precedenza salvate nella variabile "ngwIPConfig", il tipo di gateway "VPN", il tipo di VPN "RouteBased" e l'USK "Basic".</span><span class="sxs-lookup"><span data-stu-id="a609a-120">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="a609a-121">Aggiunge anche un server RADIUS esterno con l'indirizzo "TestRadiusServer"</span><span class="sxs-lookup"><span data-stu-id="a609a-121">It also adds an external radius server with address "TestRadiusServer"</span></span>

## <span data-ttu-id="a609a-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a609a-122">PARAMETERS</span></span>

### <span data-ttu-id="a609a-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a609a-123">-AsJob</span></span>
<span data-ttu-id="a609a-124">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a609a-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a609a-125">-ASN</span><span class="sxs-lookup"><span data-stu-id="a609a-125">-Asn</span></span>
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

### <span data-ttu-id="a609a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a609a-126">-DefaultProfile</span></span>
<span data-ttu-id="a609a-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a609a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="a609a-128">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="a609a-128">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="a609a-129">Abilita la funzionalità Active-Active.</span><span class="sxs-lookup"><span data-stu-id="a609a-129">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="a609a-130">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="a609a-130">-EnableBgp</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a609a-131">-Force</span><span class="sxs-lookup"><span data-stu-id="a609a-131">-Force</span></span>
<span data-ttu-id="a609a-132">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a609a-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a609a-133">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="a609a-133">-GatewayDefaultSite</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a609a-134">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="a609a-134">-GatewaySku</span></span>
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

### <span data-ttu-id="a609a-135">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="a609a-135">-GatewayType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Vpn, ExpressRoute

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a609a-136">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="a609a-136">-IpConfigurations</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a609a-137">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a609a-137">-Location</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a609a-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="a609a-138">-Name</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a609a-139">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="a609a-139">-PeerWeight</span></span>
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

### <span data-ttu-id="a609a-140">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="a609a-140">-RadiusServerAddress</span></span>
<span data-ttu-id="a609a-141">Indirizzo del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="a609a-141">P2S External Radius server address.</span></span>
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

### <span data-ttu-id="a609a-142">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="a609a-142">-RadiusServerSecret</span></span>
<span data-ttu-id="a609a-143">Segreto del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="a609a-143">P2S External Radius server secret.</span></span>
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

### <span data-ttu-id="a609a-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a609a-144">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a609a-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="a609a-145">-Tag</span></span>
<span data-ttu-id="a609a-146">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a609a-146">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a609a-147">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="a609a-147">For example:</span></span>

<span data-ttu-id="a609a-148">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a609a-148">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a609a-149">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="a609a-149">-VpnClientAddressPool</span></span>
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

### <span data-ttu-id="a609a-150">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="a609a-150">-VpnClientProtocol</span></span>
<span data-ttu-id="a609a-151">Elenco dei protocolli di tunneling client VPN di P2S</span><span class="sxs-lookup"><span data-stu-id="a609a-151">The list of P2S VPN client tunneling protocols</span></span>
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

### <span data-ttu-id="a609a-152">-VpnClientRevokedCertificates</span><span class="sxs-lookup"><span data-stu-id="a609a-152">-VpnClientRevokedCertificates</span></span>
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

### <span data-ttu-id="a609a-153">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="a609a-153">-VpnClientRootCertificates</span></span>
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

### <span data-ttu-id="a609a-154">-VpnType</span><span class="sxs-lookup"><span data-stu-id="a609a-154">-VpnType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PolicyBased, RouteBased

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a609a-155">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a609a-155">-Confirm</span></span>
<span data-ttu-id="a609a-156">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a609a-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a609a-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a609a-157">-WhatIf</span></span>
<span data-ttu-id="a609a-158">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a609a-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a609a-159">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a609a-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a609a-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a609a-160">CommonParameters</span></span>
<span data-ttu-id="a609a-161">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a609a-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a609a-162">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a609a-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a609a-163">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a609a-163">INPUTS</span></span>

### <span data-ttu-id="a609a-164">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a609a-164">None</span></span>
<span data-ttu-id="a609a-165">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a609a-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a609a-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a609a-166">OUTPUTS</span></span>

### <span data-ttu-id="a609a-167">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a609a-167">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="a609a-168">Note</span><span class="sxs-lookup"><span data-stu-id="a609a-168">NOTES</span></span>

## <span data-ttu-id="a609a-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a609a-169">RELATED LINKS</span></span>

[<span data-ttu-id="a609a-170">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a609a-170">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="a609a-171">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a609a-171">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="a609a-172">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a609a-172">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="a609a-173">Ridimensionare-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a609a-173">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="a609a-174">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a609a-174">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)
