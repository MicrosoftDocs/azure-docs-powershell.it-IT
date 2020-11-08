---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: 23d0b2eacb5e4053cbed2c08101e225d861311de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200350"
---
# <span data-ttu-id="f77cb-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f77cb-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="f77cb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f77cb-102">SYNOPSIS</span></span>
<span data-ttu-id="f77cb-103">Crea un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="f77cb-103">Creates a network interface.</span></span>

## <span data-ttu-id="f77cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f77cb-104">SYNTAX</span></span>

### <span data-ttu-id="f77cb-105">SetByIpConfigurationResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f77cb-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f77cb-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="f77cb-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f77cb-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f77cb-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f77cb-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f77cb-108">SetByResource</span></span>
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

## <span data-ttu-id="f77cb-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f77cb-109">DESCRIPTION</span></span>
<span data-ttu-id="f77cb-110">Il cmdlet **New-AzNetworkInterface** crea un'interfaccia di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="f77cb-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="f77cb-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f77cb-111">EXAMPLES</span></span>

### <span data-ttu-id="f77cb-112">Esempio 1: creare un'interfaccia di rete di Azure</span><span class="sxs-lookup"><span data-stu-id="f77cb-112">Example 1: Create an Azure network interface</span></span>
```powershell
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="f77cb-113">Questo comando crea un'interfaccia di rete denominata NetworkInterface001 con un indirizzo IP privato assegnato in modo dinamico da Subnet1 nella rete virtuale denominata VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="f77cb-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="f77cb-114">Il comando assegna anche due server DNS all'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="f77cb-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="f77cb-115">La risorsa figlio IPConfiguration verrà creata automaticamente usando il nome IPConfiguration1.</span><span class="sxs-lookup"><span data-stu-id="f77cb-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="f77cb-116">Esempio 2: creare un'interfaccia di rete di Azure usando un oggetto di configurazione IP</span><span class="sxs-lookup"><span data-stu-id="f77cb-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```powershell
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "VirtualNetwork1" -ResourceGroupName "ResourceGroup1" 
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId $Subnet.Subnets[0].Id
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="f77cb-117">Questo esempio crea una nuova interfaccia di rete usando un oggetto di configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="f77cb-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="f77cb-118">L'oggetto di configurazione IP specifica un indirizzo IPv4 privato statico.</span><span class="sxs-lookup"><span data-stu-id="f77cb-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="f77cb-119">Il primo comando Recupera una rete virtuale specificata esistente usata per assegnare la subnet nel secondo comando.</span><span class="sxs-lookup"><span data-stu-id="f77cb-119">The first command retrieves an existing specified virtual network used to assign the subnet in the second command.</span></span>
<span data-ttu-id="f77cb-120">Il secondo comando crea una configurazione IP di interfaccia di rete denominata IPConfig1 e archivia la configurazione nella variabile denominata $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="f77cb-120">The second command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="f77cb-121">Il terzo comando crea un'interfaccia di rete denominata NetworkInterface1 che usa la configurazione IP dell'interfaccia di rete archiviata nella variabile denominata $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="f77cb-121">The third command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

### <span data-ttu-id="f77cb-122">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="f77cb-122">Example 3</span></span>

<span data-ttu-id="f77cb-123">Crea un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="f77cb-123">Creates a network interface.</span></span> <span data-ttu-id="f77cb-124">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="f77cb-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzNetworkInterface -Location 'West US' -Name 'NetworkInterface1' -PrivateIpAddress '10.0.1.10' -ResourceGroupName 'ResourceGroup1' -SubnetId '/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1'
```

## <span data-ttu-id="f77cb-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f77cb-125">PARAMETERS</span></span>

### <span data-ttu-id="f77cb-126">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f77cb-126">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="f77cb-127">Specifica un oggetto **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="f77cb-127">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="f77cb-128">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f77cb-128">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="f77cb-129">Specifica l'ID di un oggetto **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="f77cb-129">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="f77cb-130">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f77cb-130">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="f77cb-131">Specifica una raccolta di riferimenti ai gruppi di sicurezza delle applicazioni a cui deve appartenere la configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="f77cb-131">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="f77cb-132">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="f77cb-132">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="f77cb-133">Specifica una raccolta di riferimenti ai gruppi di sicurezza delle applicazioni a cui deve appartenere la configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="f77cb-133">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="f77cb-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f77cb-134">-AsJob</span></span>
<span data-ttu-id="f77cb-135">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f77cb-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f77cb-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f77cb-136">-DefaultProfile</span></span>
<span data-ttu-id="f77cb-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f77cb-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f77cb-138">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="f77cb-138">-DnsServer</span></span>
<span data-ttu-id="f77cb-139">Specifica il server DNS per l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="f77cb-139">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="f77cb-140">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="f77cb-140">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="f77cb-141">Consente la creazione di reti accelerate.</span><span class="sxs-lookup"><span data-stu-id="f77cb-141">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="f77cb-142">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="f77cb-142">-EnableIPForwarding</span></span>
<span data-ttu-id="f77cb-143">Indica che questo cmdlet Abilita l'inoltro IP per l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="f77cb-143">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="f77cb-144">L'inoltro IP consente a una macchina virtuale di ricevere il traffico indirizzato ad altre destinazioni.</span><span class="sxs-lookup"><span data-stu-id="f77cb-144">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="f77cb-145">-Force</span><span class="sxs-lookup"><span data-stu-id="f77cb-145">-Force</span></span>
<span data-ttu-id="f77cb-146">Impone la creazione dell'interfaccia di rete anche se esiste già un'interfaccia di rete con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="f77cb-146">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="f77cb-147">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="f77cb-147">-InternalDnsNameLabel</span></span>
<span data-ttu-id="f77cb-148">Specifica l'etichetta del nome DNS interno per la nuova interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="f77cb-148">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="f77cb-149">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f77cb-149">-IpConfiguration</span></span>
<span data-ttu-id="f77cb-150">Specifica la configurazione IP utilizzata da questo cmdlet per l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="f77cb-150">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="f77cb-151">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f77cb-151">-IpConfigurationName</span></span>
<span data-ttu-id="f77cb-152">Specifica il nome di una configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="f77cb-152">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="f77cb-153">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f77cb-153">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="f77cb-154">Specifica un oggetto **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="f77cb-154">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="f77cb-155">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="f77cb-155">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="f77cb-156">Specifica l'ID di un oggetto **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="f77cb-156">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="f77cb-157">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="f77cb-157">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="f77cb-158">Specifica una configurazione della regola NAT in ingresso per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f77cb-158">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="f77cb-159">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="f77cb-159">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="f77cb-160">Specifica l'ID di una configurazione della regola NAT in ingresso per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f77cb-160">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="f77cb-161">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f77cb-161">-Location</span></span>
<span data-ttu-id="f77cb-162">Specifica l'area geografica di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="f77cb-162">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="f77cb-163">-Nome</span><span class="sxs-lookup"><span data-stu-id="f77cb-163">-Name</span></span>
<span data-ttu-id="f77cb-164">Specifica il nome dell'interfaccia di rete da creare.</span><span class="sxs-lookup"><span data-stu-id="f77cb-164">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="f77cb-165">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f77cb-165">-NetworkSecurityGroup</span></span>
<span data-ttu-id="f77cb-166">Specifica un oggetto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="f77cb-166">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="f77cb-167">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="f77cb-167">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="f77cb-168">Specifica l'ID di un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="f77cb-168">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="f77cb-169">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="f77cb-169">-PrivateIpAddress</span></span>
<span data-ttu-id="f77cb-170">Specifica un indirizzo IP IPv4 statico da assegnare all'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="f77cb-170">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="f77cb-171">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f77cb-171">-PublicIpAddress</span></span>
<span data-ttu-id="f77cb-172">Specifica un oggetto **PublicIPAddress** da assegnare a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="f77cb-172">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="f77cb-173">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="f77cb-173">-PublicIpAddressId</span></span>
<span data-ttu-id="f77cb-174">Specifica l'ID di un oggetto **PublicIPAddress** da assegnare a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="f77cb-174">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="f77cb-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f77cb-175">-ResourceGroupName</span></span>
<span data-ttu-id="f77cb-176">Specifica il nome di un gruppo di risorse a cui appartiene l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="f77cb-176">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="f77cb-177">-Subnet</span><span class="sxs-lookup"><span data-stu-id="f77cb-177">-Subnet</span></span>
<span data-ttu-id="f77cb-178">Specifica un oggetto **subnet** .</span><span class="sxs-lookup"><span data-stu-id="f77cb-178">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="f77cb-179">Questo cmdlet crea un'interfaccia di rete per la subnet specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="f77cb-179">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="f77cb-180">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f77cb-180">-SubnetId</span></span>
<span data-ttu-id="f77cb-181">Specifica l'ID della subnet per cui creare un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="f77cb-181">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="f77cb-182">-Tag</span><span class="sxs-lookup"><span data-stu-id="f77cb-182">-Tag</span></span>
<span data-ttu-id="f77cb-183">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f77cb-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f77cb-184">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f77cb-184">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f77cb-185">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f77cb-185">-Confirm</span></span>
<span data-ttu-id="f77cb-186">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f77cb-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f77cb-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f77cb-187">-WhatIf</span></span>
<span data-ttu-id="f77cb-188">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f77cb-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f77cb-189">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f77cb-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f77cb-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f77cb-190">CommonParameters</span></span>
<span data-ttu-id="f77cb-191">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f77cb-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f77cb-192">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f77cb-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f77cb-193">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f77cb-193">INPUTS</span></span>

### <span data-ttu-id="f77cb-194">System. String</span><span class="sxs-lookup"><span data-stu-id="f77cb-194">System.String</span></span>

### <span data-ttu-id="f77cb-195">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="f77cb-195">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="f77cb-196">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="f77cb-196">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="f77cb-197">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f77cb-197">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="f77cb-198">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f77cb-198">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="f77cb-199">System. String []</span><span class="sxs-lookup"><span data-stu-id="f77cb-199">System.String[]</span></span>

### <span data-ttu-id="f77cb-200">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="f77cb-200">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="f77cb-201">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="f77cb-201">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="f77cb-202">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="f77cb-202">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="f77cb-203">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="f77cb-203">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="f77cb-204">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f77cb-204">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f77cb-205">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f77cb-205">OUTPUTS</span></span>

### <span data-ttu-id="f77cb-206">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f77cb-206">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="f77cb-207">Note</span><span class="sxs-lookup"><span data-stu-id="f77cb-207">NOTES</span></span>

## <span data-ttu-id="f77cb-208">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f77cb-208">RELATED LINKS</span></span>

[<span data-ttu-id="f77cb-209">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f77cb-209">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="f77cb-210">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f77cb-210">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="f77cb-211">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f77cb-211">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
