---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
ms.openlocfilehash: b6a7854d3ddf3c3d444418e08717577a8a2ac172
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686563"
---
# <span data-ttu-id="b7c84-101">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7c84-101">New-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="b7c84-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7c84-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c84-103">Crea un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7c84-103">Creates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7c84-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7c84-104">SYNTAX</span></span>

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
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7c84-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7c84-105">DESCRIPTION</span></span>
<span data-ttu-id="b7c84-106">Il cmdlet **New-AzureRmApplicationGateway** crea un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="b7c84-106">The **New-AzureRmApplicationGateway** cmdlet creates an Azure application gateway.</span></span>

<span data-ttu-id="b7c84-107">Un gateway applicazione richiede le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b7c84-107">An application gateway requires the following:</span></span>

- <span data-ttu-id="b7c84-108">Un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b7c84-108">A resource group.</span></span>
- <span data-ttu-id="b7c84-109">Una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b7c84-109">A virtual network.</span></span>
- <span data-ttu-id="b7c84-110">Un pool di server back-end contenente gli indirizzi IP dei server back-end.</span><span class="sxs-lookup"><span data-stu-id="b7c84-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="b7c84-111">Impostazioni del pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="b7c84-111">Back-end server pool settings.</span></span> <span data-ttu-id="b7c84-112">Ogni pool include impostazioni come la porta, il protocollo e l'affinità basata su cookie, che vengono applicati a tutti i server all'interno del pool.</span><span class="sxs-lookup"><span data-stu-id="b7c84-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="b7c84-113">Indirizzi IP front-end, ovvero gli indirizzi IP aperti nel gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7c84-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="b7c84-114">Un indirizzo IP front-end può essere un indirizzo IP pubblico o un indirizzo IP interno.</span><span class="sxs-lookup"><span data-stu-id="b7c84-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="b7c84-115">Porte front-end, che sono le porte pubbliche aperte nel gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7c84-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="b7c84-116">Il traffico che colpisce queste porte viene reindirizzato ai server back-end.</span><span class="sxs-lookup"><span data-stu-id="b7c84-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="b7c84-117">Regola di routing delle richieste che associa il listener e il pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="b7c84-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="b7c84-118">La regola definisce il pool di server back-end a cui il traffico deve essere indirizzato quando colpisce un determinato listener.</span><span class="sxs-lookup"><span data-stu-id="b7c84-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>

<span data-ttu-id="b7c84-119">Un listener ha una porta front-end, un indirizzo IP front-end, un protocollo (HTTP o HTTPS) e un nome di certificato SSL (Secure Sockets Layer) (se si configura SSL Offload).</span><span class="sxs-lookup"><span data-stu-id="b7c84-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="b7c84-120">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7c84-120">EXAMPLES</span></span>

### <span data-ttu-id="b7c84-121">Esempio 1: creare un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="b7c84-121">Example 1: Create an application gateway</span></span>
```
PS C:\>$ResourceGroup = New-AzureRmResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} PS C:\>$Subnet = New-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet PS C:\>$GatewayIPconfig = New-AzureRmApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name $PublicIpName -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzureRmApplicationGatewayHttpListener -Name $listenerName  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $ FrontEndPort
PS C:\> $Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzureRmApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="b7c84-122">L'esempio seguente crea un gateway dell'applicazione creando prima di tutto un gruppo di risorse e una rete virtuale, nonché le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b7c84-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>

- <span data-ttu-id="b7c84-123">Un pool di server back-end</span><span class="sxs-lookup"><span data-stu-id="b7c84-123">A back-end server pool</span></span>
- <span data-ttu-id="b7c84-124">Impostazioni del pool di server back-end</span><span class="sxs-lookup"><span data-stu-id="b7c84-124">Back-end server pool settings</span></span>
- <span data-ttu-id="b7c84-125">Porte front-end</span><span class="sxs-lookup"><span data-stu-id="b7c84-125">Front-end ports</span></span>
- <span data-ttu-id="b7c84-126">Indirizzi IP front-end</span><span class="sxs-lookup"><span data-stu-id="b7c84-126">Front-end IP addresses</span></span>
- <span data-ttu-id="b7c84-127">Regola di routing delle richieste</span><span class="sxs-lookup"><span data-stu-id="b7c84-127">A request routing rule</span></span>

<span data-ttu-id="b7c84-128">Questi quattro comandi creano una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b7c84-128">These four commands create a virtual network.</span></span>
<span data-ttu-id="b7c84-129">Il primo comando crea una configurazione di subnet.</span><span class="sxs-lookup"><span data-stu-id="b7c84-129">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="b7c84-130">Il secondo comando crea una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b7c84-130">The second command creates a virtual network.</span></span>
<span data-ttu-id="b7c84-131">Il terzo comando verifica la configurazione della subnet e il quarto comando verifica che la rete virtuale venga creata correttamente.</span><span class="sxs-lookup"><span data-stu-id="b7c84-131">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>

<span data-ttu-id="b7c84-132">I comandi seguenti creano il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7c84-132">The following commands create the application gateway.</span></span>
<span data-ttu-id="b7c84-133">Il primo comando crea una configurazione IP denominata GatewayIp01 per la subnet creata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="b7c84-133">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="b7c84-134">Il secondo comando crea un pool di server back-end denominato Pool01 con un elenco di indirizzi IP di back-end e archivia il pool nella variabile $Pool.</span><span class="sxs-lookup"><span data-stu-id="b7c84-134">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="b7c84-135">Il terzo comando crea le impostazioni per il pool di server back-end e archivia le impostazioni nella variabile $PoolSetting.</span><span class="sxs-lookup"><span data-stu-id="b7c84-135">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="b7c84-136">Il comando Forth crea una porta front-end sulla porta 80, la chiama FrontEndPort01 e archivia la porta nella variabile $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="b7c84-136">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="b7c84-137">Il quinto comando crea un indirizzo IP pubblico usando New-AzureRmPublicIpAddress.</span><span class="sxs-lookup"><span data-stu-id="b7c84-137">The fifth command creates a public IP address by using New-AzureRmPublicIpAddress.</span></span>
<span data-ttu-id="b7c84-138">Il sesto comando crea una configurazione IP front-end usando $PublicIp, la chiama FrontEndPortConfig01 e la memorizza nella variabile $FrontEndIpConfig.</span><span class="sxs-lookup"><span data-stu-id="b7c84-138">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="b7c84-139">Il settimo comando crea un listener usando il $FrontEndPort $FrontEndIpConfig creato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="b7c84-139">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="b7c84-140">L'ottavo comando crea una regola per il listener.</span><span class="sxs-lookup"><span data-stu-id="b7c84-140">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="b7c84-141">Il nono comando imposta l'USK.</span><span class="sxs-lookup"><span data-stu-id="b7c84-141">The ninth command sets the SKU.</span></span>
<span data-ttu-id="b7c84-142">Il decimo comando crea il gateway usando gli oggetti impostati dai comandi precedenti.</span><span class="sxs-lookup"><span data-stu-id="b7c84-142">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="b7c84-143">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7c84-143">PARAMETERS</span></span>

### <span data-ttu-id="b7c84-144">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="b7c84-144">-AuthenticationCertificates</span></span>
<span data-ttu-id="b7c84-145">Specifica i certificati di autenticazione per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7c84-145">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="b7c84-146">-BackendAddressPools</span><span class="sxs-lookup"><span data-stu-id="b7c84-146">-BackendAddressPools</span></span>
<span data-ttu-id="b7c84-147">Specifica l'elenco dei pool di indirizzi back-end per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7c84-147">Specifies the list of back-end address pools for the application gateway.</span></span>

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

### <span data-ttu-id="b7c84-148">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="b7c84-148">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="b7c84-149">Specifica l'elenco delle impostazioni HTTP di back-end per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7c84-149">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

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

### <span data-ttu-id="b7c84-150">-Force</span><span class="sxs-lookup"><span data-stu-id="b7c84-150">-Force</span></span>
<span data-ttu-id="b7c84-151">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b7c84-151">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b7c84-152">-FrontendIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="b7c84-152">-FrontendIPConfigurations</span></span>
<span data-ttu-id="b7c84-153">Specifica un elenco di configurazioni IP front-end per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7c84-153">Specifies a list of front-end IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="b7c84-154">-FrontendPorts</span><span class="sxs-lookup"><span data-stu-id="b7c84-154">-FrontendPorts</span></span>
<span data-ttu-id="b7c84-155">Specifica un elenco di porte front-end per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7c84-155">Specifies a list of front-end ports for the application gateway.</span></span>

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

### <span data-ttu-id="b7c84-156">-GatewayIPConfigurations</span><span class="sxs-lookup"><span data-stu-id="b7c84-156">-GatewayIPConfigurations</span></span>
<span data-ttu-id="b7c84-157">Specifica un elenco di configurazioni IP per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7c84-157">Specifies a list of IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="b7c84-158">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="b7c84-158">-HttpListeners</span></span>
<span data-ttu-id="b7c84-159">Specifica un elenco di listener HTTP per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7c84-159">Specifies a list of HTTP listeners for the application gateway.</span></span>

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

### <span data-ttu-id="b7c84-160">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b7c84-160">-Location</span></span>
<span data-ttu-id="b7c84-161">Specifica l'area geografica in cui creare il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7c84-161">Specifies the region in which to create the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c84-162">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7c84-162">-Name</span></span>
<span data-ttu-id="b7c84-163">Specifica il nome del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7c84-163">Specifies the name of application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c84-164">-Sonde</span><span class="sxs-lookup"><span data-stu-id="b7c84-164">-Probes</span></span>
<span data-ttu-id="b7c84-165">Specifica le sonde per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7c84-165">Specifies probes for the application gateway.</span></span>

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

### <span data-ttu-id="b7c84-166">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="b7c84-166">-RedirectConfigurations</span></span>
<span data-ttu-id="b7c84-167">Elenco della configurazione di Reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="b7c84-167">The list of redirect configuration</span></span>

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

### <span data-ttu-id="b7c84-168">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="b7c84-168">-RequestRoutingRules</span></span>
<span data-ttu-id="b7c84-169">Specifica un elenco di regole di routing delle richieste per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7c84-169">Specifies a list of request routing rules for the application gateway.</span></span>

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

### <span data-ttu-id="b7c84-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7c84-170">-ResourceGroupName</span></span>
<span data-ttu-id="b7c84-171">Specifica il nome del gruppo di risorse in cui creare il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7c84-171">Specifies the name of the resource group in which to create the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c84-172">-SKU</span><span class="sxs-lookup"><span data-stu-id="b7c84-172">-Sku</span></span>
<span data-ttu-id="b7c84-173">Specifica l'unità di conservazione delle scorte (SKU) del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7c84-173">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c84-174">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="b7c84-174">-SslCertificates</span></span>
<span data-ttu-id="b7c84-175">Specifica l'elenco dei certificati SSL (Secure Sockets Layer) per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7c84-175">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

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

### <span data-ttu-id="b7c84-176">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="b7c84-176">-SslPolicy</span></span>
<span data-ttu-id="b7c84-177">Specifica un criterio SSL per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7c84-177">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c84-178">-Tag</span><span class="sxs-lookup"><span data-stu-id="b7c84-178">-Tag</span></span>
<span data-ttu-id="b7c84-179">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b7c84-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b7c84-180">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="b7c84-180">For example:</span></span>

<span data-ttu-id="b7c84-181">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b7c84-181">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c84-182">-UrlPathMaps</span><span class="sxs-lookup"><span data-stu-id="b7c84-182">-UrlPathMaps</span></span>
<span data-ttu-id="b7c84-183">Specifica le mappe Path URL per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b7c84-183">Specifies URL path maps for the application gateway.</span></span>

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

### <span data-ttu-id="b7c84-184">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7c84-184">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="b7c84-185">Specifica una configurazione WAF (Web Application Firewall).</span><span class="sxs-lookup"><span data-stu-id="b7c84-185">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="b7c84-186">Puoi usare il cmdlet Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration per ottenere un WAF.</span><span class="sxs-lookup"><span data-stu-id="b7c84-186">You can use the Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c84-187">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b7c84-187">-Confirm</span></span>
<span data-ttu-id="b7c84-188">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7c84-188">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c84-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7c84-189">-WhatIf</span></span>
<span data-ttu-id="b7c84-190">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7c84-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7c84-191">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7c84-191">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c84-192">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7c84-192">-DefaultProfile</span></span>
<span data-ttu-id="b7c84-193">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7c84-193">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7c84-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c84-194">CommonParameters</span></span>
<span data-ttu-id="b7c84-195">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7c84-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7c84-196">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7c84-196">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c84-197">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7c84-197">INPUTS</span></span>

## <span data-ttu-id="b7c84-198">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7c84-198">OUTPUTS</span></span>

### <span data-ttu-id="b7c84-199">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b7c84-199">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b7c84-200">Note</span><span class="sxs-lookup"><span data-stu-id="b7c84-200">NOTES</span></span>

## <span data-ttu-id="b7c84-201">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7c84-201">RELATED LINKS</span></span>

[<span data-ttu-id="b7c84-202">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b7c84-202">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b7c84-203">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b7c84-203">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="b7c84-204">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="b7c84-204">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="b7c84-205">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="b7c84-205">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="b7c84-206">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b7c84-206">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="b7c84-207">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7c84-207">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b7c84-208">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b7c84-208">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="b7c84-209">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="b7c84-209">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="b7c84-210">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b7c84-210">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="b7c84-211">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b7c84-211">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)
