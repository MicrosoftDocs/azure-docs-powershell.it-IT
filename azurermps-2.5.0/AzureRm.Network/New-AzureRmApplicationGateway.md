---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 73b72c6585fb4c7487b43dc99b3494cdc99bf7a3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866268"
---
# <span data-ttu-id="f2f2f-101">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f2f2f-101">New-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="f2f2f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2f2f-102">SYNOPSIS</span></span>
<span data-ttu-id="f2f2f-103">Crea un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-103">Creates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2f2f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2f2f-104">SYNTAX</span></span>

```
New-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]>
 [-SslCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-FrontendIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration]>]
 -FrontendPorts <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort]>
 [-Probes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]>]
 -BackendAddressPools <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>
 -BackendHttpSettingsCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings]>
 -HttpListeners <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener]>
 [-UrlPathMaps <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]>]
 -RequestRoutingRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule]>
 [-RedirectConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2f2f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2f2f-105">DESCRIPTION</span></span>
<span data-ttu-id="f2f2f-106">Il cmdlet **New-AzureRmApplicationGateway** crea un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-106">The **New-AzureRmApplicationGateway** cmdlet creates an Azure application gateway.</span></span>

<span data-ttu-id="f2f2f-107">Un gateway applicazione richiede le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f2f2f-107">An application gateway requires the following:</span></span>

- <span data-ttu-id="f2f2f-108">Un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-108">A resource group.</span></span>
- <span data-ttu-id="f2f2f-109">Una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-109">A virtual network.</span></span>
- <span data-ttu-id="f2f2f-110">Un pool di server back-end contenente gli indirizzi IP dei server back-end.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="f2f2f-111">Impostazioni del pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-111">Back-end server pool settings.</span></span> <span data-ttu-id="f2f2f-112">Ogni pool include impostazioni come la porta, il protocollo e l'affinità basata su cookie, che vengono applicati a tutti i server all'interno del pool.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="f2f2f-113">Indirizzi IP front-end, ovvero gli indirizzi IP aperti nel gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="f2f2f-114">Un indirizzo IP front-end può essere un indirizzo IP pubblico o un indirizzo IP interno.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="f2f2f-115">Porte front-end, che sono le porte pubbliche aperte nel gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="f2f2f-116">Il traffico che colpisce queste porte viene reindirizzato ai server back-end.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="f2f2f-117">Regola di routing delle richieste che associa il listener e il pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="f2f2f-118">La regola definisce il pool di server back-end a cui il traffico deve essere indirizzato quando colpisce un determinato listener.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>

<span data-ttu-id="f2f2f-119">Un listener ha una porta front-end, un indirizzo IP front-end, un protocollo (HTTP o HTTPS) e un nome di certificato SSL (Secure Sockets Layer) (se si configura SSL Offload).</span><span class="sxs-lookup"><span data-stu-id="f2f2f-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="f2f2f-120">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2f2f-120">EXAMPLES</span></span>

### <span data-ttu-id="f2f2f-121">Esempio 1: creare un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="f2f2f-121">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzureRmResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzureRmApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzureRmApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzureRmApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="f2f2f-122">L'esempio seguente crea un gateway dell'applicazione creando prima di tutto un gruppo di risorse e una rete virtuale, nonché le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f2f2f-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>

- <span data-ttu-id="f2f2f-123">Un pool di server back-end</span><span class="sxs-lookup"><span data-stu-id="f2f2f-123">A back-end server pool</span></span>
- <span data-ttu-id="f2f2f-124">Impostazioni del pool di server back-end</span><span class="sxs-lookup"><span data-stu-id="f2f2f-124">Back-end server pool settings</span></span>
- <span data-ttu-id="f2f2f-125">Porte front-end</span><span class="sxs-lookup"><span data-stu-id="f2f2f-125">Front-end ports</span></span>
- <span data-ttu-id="f2f2f-126">Indirizzi IP front-end</span><span class="sxs-lookup"><span data-stu-id="f2f2f-126">Front-end IP addresses</span></span>
- <span data-ttu-id="f2f2f-127">Regola di routing delle richieste</span><span class="sxs-lookup"><span data-stu-id="f2f2f-127">A request routing rule</span></span>

<span data-ttu-id="f2f2f-128">Questi quattro comandi creano una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-128">These four commands create a virtual network.</span></span>
<span data-ttu-id="f2f2f-129">Il primo comando crea una configurazione di subnet.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-129">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="f2f2f-130">Il secondo comando crea una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-130">The second command creates a virtual network.</span></span>
<span data-ttu-id="f2f2f-131">Il terzo comando verifica la configurazione della subnet e il quarto comando verifica che la rete virtuale venga creata correttamente.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-131">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>

<span data-ttu-id="f2f2f-132">I comandi seguenti creano il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-132">The following commands create the application gateway.</span></span>
<span data-ttu-id="f2f2f-133">Il primo comando crea una configurazione IP denominata GatewayIp01 per la subnet creata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-133">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="f2f2f-134">Il secondo comando crea un pool di server back-end denominato Pool01 con un elenco di indirizzi IP di back-end e archivia il pool nella variabile $Pool.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-134">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="f2f2f-135">Il terzo comando crea le impostazioni per il pool di server back-end e archivia le impostazioni nella variabile $PoolSetting.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-135">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="f2f2f-136">Il comando Forth crea una porta front-end sulla porta 80, la chiama FrontEndPort01 e archivia la porta nella variabile $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-136">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="f2f2f-137">Il quinto comando crea un indirizzo IP pubblico usando New-AzureRmPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-137">The fifth command creates a public IP address by using New-AzureRmPublicIpAddress.</span></span>
<span data-ttu-id="f2f2f-138">Il sesto comando crea una configurazione IP front-end usando $PublicIp, la chiama FrontEndPortConfig01 e la memorizza nella variabile $FrontEndIpConfig.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-138">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="f2f2f-139">Il settimo comando crea un listener usando il $FrontEndPort $FrontEndIpConfig creato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-139">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="f2f2f-140">L'ottavo comando crea una regola per il listener.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-140">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="f2f2f-141">Il nono comando imposta l'USK.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-141">The ninth command sets the SKU.</span></span>
<span data-ttu-id="f2f2f-142">Il decimo comando crea il gateway usando gli oggetti impostati dai comandi precedenti.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-142">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="f2f2f-143">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2f2f-143">PARAMETERS</span></span>

### <span data-ttu-id="f2f2f-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2f2f-144">-AsJob</span></span>
<span data-ttu-id="f2f2f-145">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f2f2f-145">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2f2f-146">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="f2f2f-146">-AuthenticationCertificates</span></span>
<span data-ttu-id="f2f2f-147">Specifica i certificati di autenticazione per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-147">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2f-148">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="f2f2f-148">-BackendAddressPools</span></span>
<span data-ttu-id="f2f2f-149">Specifica l'elenco dei pool di indirizzi back-end per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-149">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2f-150">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="f2f2f-150">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="f2f2f-151">Specifica l'elenco delle impostazioni HTTP di back-end per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-151">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2f-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2f2f-152">-DefaultProfile</span></span>
<span data-ttu-id="f2f2f-153">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2f2f-154">-Force</span><span class="sxs-lookup"><span data-stu-id="f2f2f-154">-Force</span></span>
<span data-ttu-id="f2f2f-155">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-155">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f2f2f-156">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="f2f2f-156">-FrontendIPConfigurations</span></span>
<span data-ttu-id="f2f2f-157">Specifica un elenco di configurazioni IP front-end per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-157">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2f-158">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="f2f2f-158">-FrontendPorts</span></span>
<span data-ttu-id="f2f2f-159">Specifica un elenco di porte front-end per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-159">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2f-160">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="f2f2f-160">-GatewayIPConfigurations</span></span>
<span data-ttu-id="f2f2f-161">Specifica un elenco di configurazioni IP per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-161">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2f-162">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="f2f2f-162">-HttpListeners</span></span>
<span data-ttu-id="f2f2f-163">Specifica un elenco di listener HTTP per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-163">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2f-164">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f2f2f-164">-Location</span></span>
<span data-ttu-id="f2f2f-165">Specifica l'area geografica in cui creare il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-165">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="f2f2f-166">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2f2f-166">-Name</span></span>
<span data-ttu-id="f2f2f-167">Specifica il nome del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-167">Specifies the name of application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2f-168">-Sonde</span><span class="sxs-lookup"><span data-stu-id="f2f2f-168">-Probes</span></span>
<span data-ttu-id="f2f2f-169">Specifica le sonde per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-169">Specifies probes for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2f-170">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="f2f2f-170">-RedirectConfigurations</span></span>
<span data-ttu-id="f2f2f-171">Elenco della configurazione di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="f2f2f-171">The list of redirect configuration</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2f-172">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="f2f2f-172">-RequestRoutingRules</span></span>
<span data-ttu-id="f2f2f-173">Specifica un elenco di regole di routing delle richieste per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-173">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2f-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2f2f-174">-ResourceGroupName</span></span>
<span data-ttu-id="f2f2f-175">Specifica il nome del gruppo di risorse in cui creare il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-175">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="f2f2f-176">-SKU</span><span class="sxs-lookup"><span data-stu-id="f2f2f-176">-Sku</span></span>
<span data-ttu-id="f2f2f-177">Specifica l'unità di conservazione delle scorte (SKU) del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-177">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySku
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2f-178">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="f2f2f-178">-SslCertificates</span></span>
<span data-ttu-id="f2f2f-179">Specifica l'elenco dei certificati SSL (Secure Sockets Layer) per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-179">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2f-180">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="f2f2f-180">-SslPolicy</span></span>
<span data-ttu-id="f2f2f-181">Specifica un criterio SSL per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-181">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2f-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="f2f2f-182">-Tag</span></span>
<span data-ttu-id="f2f2f-183">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f2f2f-184">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="f2f2f-184">For example:</span></span>

<span data-ttu-id="f2f2f-185">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f2f2f-185">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f2f2f-186">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="f2f2f-186">-UrlPathMaps</span></span>
<span data-ttu-id="f2f2f-187">Specifica le mappe Path URL per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-187">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2f-188">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f2f2f-188">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="f2f2f-189">Specifica una configurazione WAF (Web Application Firewall).</span><span class="sxs-lookup"><span data-stu-id="f2f2f-189">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="f2f2f-190">Puoi usare il cmdlet Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration per ottenere un WAF.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-190">You can use the Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f2f-191">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f2f2f-191">-Confirm</span></span>
<span data-ttu-id="f2f2f-192">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2f2f-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2f2f-193">-WhatIf</span></span>
<span data-ttu-id="f2f2f-194">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2f2f-195">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2f2f-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2f2f-196">CommonParameters</span></span>
<span data-ttu-id="f2f2f-197">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2f2f-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2f2f-198">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2f2f-198">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2f2f-199">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2f2f-199">INPUTS</span></span>

## <span data-ttu-id="f2f2f-200">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2f2f-200">OUTPUTS</span></span>

### <span data-ttu-id="f2f2f-201">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f2f2f-201">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f2f2f-202">Note</span><span class="sxs-lookup"><span data-stu-id="f2f2f-202">NOTES</span></span>

## <span data-ttu-id="f2f2f-203">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2f2f-203">RELATED LINKS</span></span>

[<span data-ttu-id="f2f2f-204">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f2f2f-204">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f2f2f-205">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f2f2f-205">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="f2f2f-206">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="f2f2f-206">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="f2f2f-207">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f2f2f-207">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f2f2f-208">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f2f2f-208">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="f2f2f-209">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f2f2f-209">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="f2f2f-210">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="f2f2f-210">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="f2f2f-211">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f2f2f-211">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="f2f2f-212">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f2f2f-212">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="f2f2f-213">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="f2f2f-213">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)
