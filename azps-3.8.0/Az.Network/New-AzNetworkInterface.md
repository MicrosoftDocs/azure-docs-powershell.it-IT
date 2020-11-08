---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: feefe02c5056556d360a54819ea429cd39b84b62
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020094"
---
# <span data-ttu-id="24a0c-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="24a0c-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="24a0c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24a0c-102">SYNOPSIS</span></span>
<span data-ttu-id="24a0c-103">Crea un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="24a0c-103">Creates a network interface.</span></span>

## <span data-ttu-id="24a0c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24a0c-104">SYNTAX</span></span>

### <span data-ttu-id="24a0c-105">SetByIpConfigurationResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="24a0c-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24a0c-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="24a0c-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24a0c-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="24a0c-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24a0c-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="24a0c-108">SetByResource</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 [-PublicIpAddress <PSPublicIpAddress>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>] [-EnableIPForwarding]
 [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24a0c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24a0c-109">DESCRIPTION</span></span>
<span data-ttu-id="24a0c-110">Il cmdlet **New-AzNetworkInterface** crea un'interfaccia di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="24a0c-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="24a0c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24a0c-111">EXAMPLES</span></span>

### <span data-ttu-id="24a0c-112">Esempio 1: creare un'interfaccia di rete di Azure</span><span class="sxs-lookup"><span data-stu-id="24a0c-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="24a0c-113">Questo comando crea un'interfaccia di rete denominata NetworkInterface001 con un indirizzo IP privato assegnato in modo dinamico da Subnet1 nella rete virtuale denominata VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="24a0c-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="24a0c-114">Il comando assegna anche due server DNS all'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="24a0c-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="24a0c-115">La risorsa figlio IPConfiguration verrà creata automaticamente usando il nome IPConfiguration1.</span><span class="sxs-lookup"><span data-stu-id="24a0c-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="24a0c-116">Esempio 2: creare un'interfaccia di rete di Azure usando un oggetto di configurazione IP</span><span class="sxs-lookup"><span data-stu-id="24a0c-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "VirtualNetwork1" -ResourceGroupName "ResourceGroup1" 
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId $Subnet.Subnets[0].Id
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="24a0c-117">Questo esempio crea una nuova interfaccia di rete usando un oggetto di configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="24a0c-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="24a0c-118">L'oggetto di configurazione IP specifica un indirizzo IPv4 privato statico.</span><span class="sxs-lookup"><span data-stu-id="24a0c-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="24a0c-119">Il primo comando Recupera una rete virtuale specificata esistente usata per assegnare la subnet nel secondo comando.</span><span class="sxs-lookup"><span data-stu-id="24a0c-119">The first command retrieves an existing specified virtual network used to assign the subnet in the second command.</span></span>
<span data-ttu-id="24a0c-120">Il secondo comando crea una configurazione IP di interfaccia di rete denominata IPConfig1 e archivia la configurazione nella variabile denominata $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="24a0c-120">The second command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="24a0c-121">Il terzo comando crea un'interfaccia di rete denominata NetworkInterface1 che usa la configurazione IP dell'interfaccia di rete archiviata nella variabile denominata $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="24a0c-121">The third command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="24a0c-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24a0c-122">PARAMETERS</span></span>

### <span data-ttu-id="24a0c-123">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="24a0c-123">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="24a0c-124">Specifica un oggetto **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="24a0c-124">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a0c-125">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="24a0c-125">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="24a0c-126">Specifica l'ID di un oggetto **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="24a0c-126">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a0c-127">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="24a0c-127">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="24a0c-128">Specifica una raccolta di riferimenti ai gruppi di sicurezza delle applicazioni a cui deve appartenere la configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="24a0c-128">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a0c-129">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="24a0c-129">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="24a0c-130">Specifica una raccolta di riferimenti ai gruppi di sicurezza delle applicazioni a cui deve appartenere la configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="24a0c-130">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a0c-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24a0c-131">-AsJob</span></span>
<span data-ttu-id="24a0c-132">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="24a0c-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24a0c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24a0c-133">-DefaultProfile</span></span>
<span data-ttu-id="24a0c-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24a0c-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24a0c-135">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="24a0c-135">-DnsServer</span></span>
<span data-ttu-id="24a0c-136">Specifica il server DNS per l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="24a0c-136">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="24a0c-137">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="24a0c-137">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="24a0c-138">Consente la creazione di reti accelerate.</span><span class="sxs-lookup"><span data-stu-id="24a0c-138">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="24a0c-139">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="24a0c-139">-EnableIPForwarding</span></span>
<span data-ttu-id="24a0c-140">Indica che questo cmdlet Abilita l'inoltro IP per l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="24a0c-140">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="24a0c-141">L'inoltro IP consente a una macchina virtuale di ricevere il traffico indirizzato ad altre destinazioni.</span><span class="sxs-lookup"><span data-stu-id="24a0c-141">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="24a0c-142">-Force</span><span class="sxs-lookup"><span data-stu-id="24a0c-142">-Force</span></span>
<span data-ttu-id="24a0c-143">Impone la creazione dell'interfaccia di rete anche se esiste già un'interfaccia di rete con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="24a0c-143">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="24a0c-144">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="24a0c-144">-InternalDnsNameLabel</span></span>
<span data-ttu-id="24a0c-145">Specifica l'etichetta del nome DNS interno per la nuova interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="24a0c-145">Specifies the internal DNS name label for the new network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a0c-146">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="24a0c-146">-IpConfiguration</span></span>
<span data-ttu-id="24a0c-147">Specifica la configurazione IP utilizzata da questo cmdlet per l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="24a0c-147">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]
Parameter Sets: SetByIpConfigurationResource, SetByIpConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a0c-148">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="24a0c-148">-IpConfigurationName</span></span>
<span data-ttu-id="24a0c-149">Specifica il nome di una configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="24a0c-149">Specifies the name of an IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a0c-150">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="24a0c-150">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="24a0c-151">Specifica un oggetto **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="24a0c-151">Specifies a **BackendAddressPool** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a0c-152">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="24a0c-152">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="24a0c-153">Specifica l'ID di un oggetto **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="24a0c-153">Specifies the ID of a **BackendAddressPool** object.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a0c-154">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="24a0c-154">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="24a0c-155">Specifica una configurazione della regola NAT in ingresso per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="24a0c-155">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a0c-156">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="24a0c-156">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="24a0c-157">Specifica l'ID di una configurazione della regola NAT in ingresso per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="24a0c-157">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a0c-158">-Posizione</span><span class="sxs-lookup"><span data-stu-id="24a0c-158">-Location</span></span>
<span data-ttu-id="24a0c-159">Specifica l'area geografica di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="24a0c-159">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="24a0c-160">-Nome</span><span class="sxs-lookup"><span data-stu-id="24a0c-160">-Name</span></span>
<span data-ttu-id="24a0c-161">Specifica il nome dell'interfaccia di rete da creare.</span><span class="sxs-lookup"><span data-stu-id="24a0c-161">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="24a0c-162">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="24a0c-162">-NetworkSecurityGroup</span></span>
<span data-ttu-id="24a0c-163">Specifica un oggetto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="24a0c-163">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: SetByIpConfigurationResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a0c-164">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="24a0c-164">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="24a0c-165">Specifica l'ID di un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="24a0c-165">Specifies the ID of a network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIpConfigurationResourceId, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a0c-166">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="24a0c-166">-PrivateIpAddress</span></span>
<span data-ttu-id="24a0c-167">Specifica un indirizzo IP IPv4 statico da assegnare all'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="24a0c-167">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a0c-168">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="24a0c-168">-PublicIpAddress</span></span>
<span data-ttu-id="24a0c-169">Specifica un oggetto **PublicIPAddress** da assegnare a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="24a0c-169">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a0c-170">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="24a0c-170">-PublicIpAddressId</span></span>
<span data-ttu-id="24a0c-171">Specifica l'ID di un oggetto **PublicIPAddress** da assegnare a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="24a0c-171">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a0c-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24a0c-172">-ResourceGroupName</span></span>
<span data-ttu-id="24a0c-173">Specifica il nome di un gruppo di risorse a cui appartiene l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="24a0c-173">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="24a0c-174">-Subnet</span><span class="sxs-lookup"><span data-stu-id="24a0c-174">-Subnet</span></span>
<span data-ttu-id="24a0c-175">Specifica un oggetto **subnet** .</span><span class="sxs-lookup"><span data-stu-id="24a0c-175">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="24a0c-176">Questo cmdlet crea un'interfaccia di rete per la subnet specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="24a0c-176">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a0c-177">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="24a0c-177">-SubnetId</span></span>
<span data-ttu-id="24a0c-178">Specifica l'ID della subnet per cui creare un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="24a0c-178">Specifies the ID of the subnet for which to create a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24a0c-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="24a0c-179">-Tag</span></span>
<span data-ttu-id="24a0c-180">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="24a0c-180">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="24a0c-181">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="24a0c-181">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="24a0c-182">-Confermare</span><span class="sxs-lookup"><span data-stu-id="24a0c-182">-Confirm</span></span>
<span data-ttu-id="24a0c-183">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24a0c-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24a0c-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24a0c-184">-WhatIf</span></span>
<span data-ttu-id="24a0c-185">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24a0c-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24a0c-186">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24a0c-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24a0c-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a0c-187">CommonParameters</span></span>
<span data-ttu-id="24a0c-188">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24a0c-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a0c-189">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24a0c-189">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a0c-190">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24a0c-190">INPUTS</span></span>

### <span data-ttu-id="24a0c-191">System. String</span><span class="sxs-lookup"><span data-stu-id="24a0c-191">System.String</span></span>

### <span data-ttu-id="24a0c-192">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="24a0c-192">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="24a0c-193">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="24a0c-193">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="24a0c-194">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="24a0c-194">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="24a0c-195">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="24a0c-195">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="24a0c-196">System. String []</span><span class="sxs-lookup"><span data-stu-id="24a0c-196">System.String[]</span></span>

### <span data-ttu-id="24a0c-197">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="24a0c-197">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="24a0c-198">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="24a0c-198">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="24a0c-199">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="24a0c-199">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="24a0c-200">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="24a0c-200">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="24a0c-201">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="24a0c-201">System.Collections.Hashtable</span></span>

## <span data-ttu-id="24a0c-202">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24a0c-202">OUTPUTS</span></span>

### <span data-ttu-id="24a0c-203">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="24a0c-203">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="24a0c-204">Note</span><span class="sxs-lookup"><span data-stu-id="24a0c-204">NOTES</span></span>

## <span data-ttu-id="24a0c-205">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24a0c-205">RELATED LINKS</span></span>

[<span data-ttu-id="24a0c-206">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="24a0c-206">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="24a0c-207">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="24a0c-207">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="24a0c-208">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="24a0c-208">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
