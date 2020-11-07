---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: 63f7dc9fd60e8ef4de77790f2fb66b8143c72b8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854425"
---
# <span data-ttu-id="db98a-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="db98a-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="db98a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db98a-102">SYNOPSIS</span></span>
<span data-ttu-id="db98a-103">Crea un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="db98a-103">Creates a network interface.</span></span>

## <span data-ttu-id="db98a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db98a-104">SYNTAX</span></span>

### <span data-ttu-id="db98a-105">SetByIpConfigurationResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="db98a-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db98a-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="db98a-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db98a-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="db98a-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db98a-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="db98a-108">SetByResource</span></span>
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

## <span data-ttu-id="db98a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db98a-109">DESCRIPTION</span></span>
<span data-ttu-id="db98a-110">Il cmdlet **New-AzNetworkInterface** crea un'interfaccia di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="db98a-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="db98a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db98a-111">EXAMPLES</span></span>

### <span data-ttu-id="db98a-112">Esempio 1: creare un'interfaccia di rete di Azure</span><span class="sxs-lookup"><span data-stu-id="db98a-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="db98a-113">Questo comando crea un'interfaccia di rete denominata NetworkInterface001 con un indirizzo IP privato assegnato in modo dinamico da Subnet1 nella rete virtuale denominata VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="db98a-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="db98a-114">Il comando assegna anche due server DNS all'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="db98a-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="db98a-115">La risorsa figlio IPConfiguration verrà creata automaticamente usando il nome IPConfiguration1.</span><span class="sxs-lookup"><span data-stu-id="db98a-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="db98a-116">Esempio 2: creare un'interfaccia di rete di Azure usando un oggetto di configurazione IP</span><span class="sxs-lookup"><span data-stu-id="db98a-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1"
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="db98a-117">Questo esempio crea una nuova interfaccia di rete usando un oggetto di configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="db98a-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="db98a-118">L'oggetto di configurazione IP specifica un indirizzo IPv4 privato statico.</span><span class="sxs-lookup"><span data-stu-id="db98a-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="db98a-119">Il primo comando crea una configurazione IP di interfaccia di rete denominata IPConfig1 e archivia la configurazione nella variabile denominata $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="db98a-119">The first command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="db98a-120">Il secondo comando crea un'interfaccia di rete denominata NetworkInterface1 che usa la configurazione IP dell'interfaccia di rete archiviata nella variabile denominata $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="db98a-120">The second command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="db98a-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db98a-121">PARAMETERS</span></span>

### <span data-ttu-id="db98a-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="db98a-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="db98a-123">Specifica un oggetto **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="db98a-123">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="db98a-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="db98a-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="db98a-125">Specifica l'ID di un oggetto **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="db98a-125">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="db98a-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="db98a-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="db98a-127">Specifica una raccolta di riferimenti ai gruppi di sicurezza delle applicazioni a cui deve appartenere la configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="db98a-127">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="db98a-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="db98a-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="db98a-129">Specifica una raccolta di riferimenti ai gruppi di sicurezza delle applicazioni a cui deve appartenere la configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="db98a-129">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="db98a-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db98a-130">-AsJob</span></span>
<span data-ttu-id="db98a-131">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="db98a-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db98a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db98a-132">-DefaultProfile</span></span>
<span data-ttu-id="db98a-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db98a-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db98a-134">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="db98a-134">-DnsServer</span></span>
<span data-ttu-id="db98a-135">Specifica il server DNS per l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="db98a-135">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="db98a-136">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="db98a-136">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="db98a-137">Consente la creazione di reti accelerate.</span><span class="sxs-lookup"><span data-stu-id="db98a-137">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="db98a-138">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="db98a-138">-EnableIPForwarding</span></span>
<span data-ttu-id="db98a-139">Indica che questo cmdlet Abilita l'inoltro IP per l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="db98a-139">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="db98a-140">L'inoltro IP consente a una macchina virtuale di ricevere il traffico indirizzato ad altre destinazioni.</span><span class="sxs-lookup"><span data-stu-id="db98a-140">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="db98a-141">-Force</span><span class="sxs-lookup"><span data-stu-id="db98a-141">-Force</span></span>
<span data-ttu-id="db98a-142">Impone la creazione dell'interfaccia di rete anche se esiste già un'interfaccia di rete con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="db98a-142">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="db98a-143">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="db98a-143">-InternalDnsNameLabel</span></span>
<span data-ttu-id="db98a-144">Specifica l'etichetta del nome DNS interno per la nuova interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="db98a-144">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="db98a-145">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="db98a-145">-IpConfiguration</span></span>
<span data-ttu-id="db98a-146">Specifica la configurazione IP utilizzata da questo cmdlet per l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="db98a-146">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="db98a-147">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="db98a-147">-IpConfigurationName</span></span>
<span data-ttu-id="db98a-148">Specifica il nome di una configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="db98a-148">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="db98a-149">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="db98a-149">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="db98a-150">Specifica un oggetto **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="db98a-150">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="db98a-151">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="db98a-151">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="db98a-152">Specifica l'ID di un oggetto **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="db98a-152">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="db98a-153">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="db98a-153">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="db98a-154">Specifica una configurazione della regola NAT in ingresso per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="db98a-154">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="db98a-155">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="db98a-155">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="db98a-156">Specifica l'ID di una configurazione della regola NAT in ingresso per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="db98a-156">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="db98a-157">-Posizione</span><span class="sxs-lookup"><span data-stu-id="db98a-157">-Location</span></span>
<span data-ttu-id="db98a-158">Specifica l'area geografica di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="db98a-158">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="db98a-159">-Nome</span><span class="sxs-lookup"><span data-stu-id="db98a-159">-Name</span></span>
<span data-ttu-id="db98a-160">Specifica il nome dell'interfaccia di rete da creare.</span><span class="sxs-lookup"><span data-stu-id="db98a-160">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="db98a-161">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="db98a-161">-NetworkSecurityGroup</span></span>
<span data-ttu-id="db98a-162">Specifica un oggetto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="db98a-162">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="db98a-163">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="db98a-163">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="db98a-164">Specifica l'ID di un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="db98a-164">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="db98a-165">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="db98a-165">-PrivateIpAddress</span></span>
<span data-ttu-id="db98a-166">Specifica un indirizzo IP IPv4 statico da assegnare all'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="db98a-166">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="db98a-167">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="db98a-167">-PublicIpAddress</span></span>
<span data-ttu-id="db98a-168">Specifica un oggetto **PublicIPAddress** da assegnare a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="db98a-168">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="db98a-169">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="db98a-169">-PublicIpAddressId</span></span>
<span data-ttu-id="db98a-170">Specifica l'ID di un oggetto **PublicIPAddress** da assegnare a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="db98a-170">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="db98a-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db98a-171">-ResourceGroupName</span></span>
<span data-ttu-id="db98a-172">Specifica il nome di un gruppo di risorse a cui appartiene l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="db98a-172">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="db98a-173">-Subnet</span><span class="sxs-lookup"><span data-stu-id="db98a-173">-Subnet</span></span>
<span data-ttu-id="db98a-174">Specifica un oggetto **subnet** .</span><span class="sxs-lookup"><span data-stu-id="db98a-174">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="db98a-175">Questo cmdlet crea un'interfaccia di rete per la subnet specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="db98a-175">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="db98a-176">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="db98a-176">-SubnetId</span></span>
<span data-ttu-id="db98a-177">Specifica l'ID della subnet per cui creare un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="db98a-177">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="db98a-178">-Tag</span><span class="sxs-lookup"><span data-stu-id="db98a-178">-Tag</span></span>
<span data-ttu-id="db98a-179">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="db98a-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="db98a-180">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="db98a-180">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="db98a-181">-Confermare</span><span class="sxs-lookup"><span data-stu-id="db98a-181">-Confirm</span></span>
<span data-ttu-id="db98a-182">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db98a-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db98a-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db98a-183">-WhatIf</span></span>
<span data-ttu-id="db98a-184">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db98a-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db98a-185">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db98a-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db98a-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db98a-186">CommonParameters</span></span>
<span data-ttu-id="db98a-187">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db98a-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db98a-188">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db98a-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db98a-189">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db98a-189">INPUTS</span></span>

### <span data-ttu-id="db98a-190">System. String</span><span class="sxs-lookup"><span data-stu-id="db98a-190">System.String</span></span>

### <span data-ttu-id="db98a-191">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="db98a-191">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="db98a-192">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="db98a-192">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="db98a-193">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="db98a-193">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="db98a-194">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="db98a-194">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="db98a-195">System. String []</span><span class="sxs-lookup"><span data-stu-id="db98a-195">System.String[]</span></span>

### <span data-ttu-id="db98a-196">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="db98a-196">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="db98a-197">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="db98a-197">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="db98a-198">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="db98a-198">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="db98a-199">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="db98a-199">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="db98a-200">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="db98a-200">System.Collections.Hashtable</span></span>

## <span data-ttu-id="db98a-201">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db98a-201">OUTPUTS</span></span>

### <span data-ttu-id="db98a-202">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="db98a-202">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="db98a-203">Note</span><span class="sxs-lookup"><span data-stu-id="db98a-203">NOTES</span></span>

## <span data-ttu-id="db98a-204">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db98a-204">RELATED LINKS</span></span>

[<span data-ttu-id="db98a-205">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="db98a-205">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="db98a-206">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="db98a-206">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="db98a-207">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="db98a-207">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
