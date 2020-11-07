---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterface.md
ms.openlocfilehash: 75e16da63a5348b47a5b67042a2fb1e2078206c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687145"
---
# <span data-ttu-id="84d92-101">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="84d92-101">New-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="84d92-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84d92-102">SYNOPSIS</span></span>
<span data-ttu-id="84d92-103">Crea un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="84d92-103">Creates a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84d92-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84d92-104">SYNTAX</span></span>

### <span data-ttu-id="84d92-105">SetByIpConfigurationResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="84d92-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84d92-106">SetByIpConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="84d92-106">SetByIpConfigurationResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-NetworkSecurityGroupId <String>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84d92-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="84d92-107">SetByResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84d92-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="84d92-108">SetByResource</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 [-PublicIpAddress <PSPublicIpAddress>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84d92-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84d92-109">DESCRIPTION</span></span>
<span data-ttu-id="84d92-110">Il cmdlet **New-AzureRmNetworkInterface** crea un'interfaccia di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="84d92-110">The **New-AzureRmNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="84d92-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84d92-111">EXAMPLES</span></span>

### <span data-ttu-id="84d92-112">Esempio 1: creare un'interfaccia di rete di Azure</span><span class="sxs-lookup"><span data-stu-id="84d92-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="84d92-113">Questo comando crea un'interfaccia di rete denominata NetworkInterface001 con un indirizzo IP privato assegnato in modo dinamico da Subnet1 nella rete virtuale denominata VirtualNetwork1.</span><span class="sxs-lookup"><span data-stu-id="84d92-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="84d92-114">Il comando assegna anche due server DNS all'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="84d92-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="84d92-115">La risorsa figlio IPConfiguration verrà creata automaticamente usando il nome IPConfiguration1.</span><span class="sxs-lookup"><span data-stu-id="84d92-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="84d92-116">Esempio 2: creare un'interfaccia di rete di Azure usando un oggetto di configurazione IP</span><span class="sxs-lookup"><span data-stu-id="84d92-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$IPconfig = New-AzureRmNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1"
PS C:\> New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="84d92-117">Questo esempio crea una nuova interfaccia di rete usando un oggetto di configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="84d92-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="84d92-118">L'oggetto di configurazione IP specifica un indirizzo IPv4 privato statico.</span><span class="sxs-lookup"><span data-stu-id="84d92-118">The IP configuration object specifies a static private IPv4 address.</span></span>

<span data-ttu-id="84d92-119">Il primo comando crea una configurazione IP di interfaccia di rete denominata IPConfig1 e archivia la configurazione nella variabile denominata $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="84d92-119">The first command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>

<span data-ttu-id="84d92-120">Il secondo comando crea un'interfaccia di rete denominata NetworkInterface1 che usa la configurazione IP dell'interfaccia di rete archiviata nella variabile denominata $IPconfig.</span><span class="sxs-lookup"><span data-stu-id="84d92-120">The second command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="84d92-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84d92-121">PARAMETERS</span></span>

### <span data-ttu-id="84d92-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="84d92-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="84d92-123">Specifica un oggetto **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="84d92-123">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84d92-124">-ApplicationGatewayBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="84d92-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="84d92-125">Specifica l'ID di un oggetto **ApplicationGatewayBackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="84d92-125">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84d92-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="84d92-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="84d92-127">Specifica una raccolta di riferimenti ai gruppi di sicurezza delle applicazioni a cui deve appartenere la configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="84d92-127">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84d92-128">-ApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="84d92-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="84d92-129">Specifica una raccolta di riferimenti ai gruppi di sicurezza delle applicazioni a cui deve appartenere la configurazione IP dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="84d92-129">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84d92-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84d92-130">-DefaultProfile</span></span>
<span data-ttu-id="84d92-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84d92-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84d92-132">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="84d92-132">-DnsServer</span></span>
<span data-ttu-id="84d92-133">Specifica il server DNS per l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="84d92-133">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="84d92-134">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="84d92-134">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="84d92-135">Consente la creazione di reti accelerate.</span><span class="sxs-lookup"><span data-stu-id="84d92-135">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="84d92-136">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="84d92-136">-EnableIPForwarding</span></span>
<span data-ttu-id="84d92-137">Indica che questo cmdlet Abilita l'inoltro IP per l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="84d92-137">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="84d92-138">L'inoltro IP consente a una macchina virtuale di ricevere il traffico indirizzato ad altre destinazioni.</span><span class="sxs-lookup"><span data-stu-id="84d92-138">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="84d92-139">-Force</span><span class="sxs-lookup"><span data-stu-id="84d92-139">-Force</span></span>
<span data-ttu-id="84d92-140">Impone la creazione dell'interfaccia di rete anche se esiste già un'interfaccia di rete con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="84d92-140">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="84d92-141">-InternalDnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="84d92-141">-InternalDnsNameLabel</span></span>
<span data-ttu-id="84d92-142">Specifica l'etichetta del nome DNS interno per la nuova interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="84d92-142">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="84d92-143">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="84d92-143">-IpConfiguration</span></span>
<span data-ttu-id="84d92-144">Specifica la configurazione IP utilizzata da questo cmdlet per l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="84d92-144">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]
Parameter Sets: SetByIpConfigurationResource, SetByIpConfigurationResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84d92-145">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="84d92-145">-IpConfigurationName</span></span>
<span data-ttu-id="84d92-146">Specifica il nome di una configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="84d92-146">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="84d92-147">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="84d92-147">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="84d92-148">Specifica un oggetto **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="84d92-148">Specifies a **BackendAddressPool** object.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84d92-149">-LoadBalancerBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="84d92-149">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="84d92-150">Specifica l'ID di un oggetto **BackendAddressPool** .</span><span class="sxs-lookup"><span data-stu-id="84d92-150">Specifies the ID of a **BackendAddressPool** object.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84d92-151">-LoadBalancerInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="84d92-151">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="84d92-152">Specifica una configurazione della regola NAT in ingresso per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="84d92-152">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84d92-153">-LoadBalancerInboundNatRuleId</span><span class="sxs-lookup"><span data-stu-id="84d92-153">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="84d92-154">Specifica l'ID di una configurazione della regola NAT in ingresso per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="84d92-154">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84d92-155">-Posizione</span><span class="sxs-lookup"><span data-stu-id="84d92-155">-Location</span></span>
<span data-ttu-id="84d92-156">Specifica l'area geografica di un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="84d92-156">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="84d92-157">-Nome</span><span class="sxs-lookup"><span data-stu-id="84d92-157">-Name</span></span>
<span data-ttu-id="84d92-158">Specifica il nome dell'interfaccia di rete da creare.</span><span class="sxs-lookup"><span data-stu-id="84d92-158">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="84d92-159">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="84d92-159">-NetworkSecurityGroup</span></span>
<span data-ttu-id="84d92-160">Specifica un oggetto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="84d92-160">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="84d92-161">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="84d92-161">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="84d92-162">Specifica l'ID di un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="84d92-162">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="84d92-163">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="84d92-163">-PrivateIpAddress</span></span>
<span data-ttu-id="84d92-164">Specifica un indirizzo IP IPv4 statico da assegnare all'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="84d92-164">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="84d92-165">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="84d92-165">-PublicIpAddress</span></span>
<span data-ttu-id="84d92-166">Specifica un oggetto **PublicIPAddress** da assegnare a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="84d92-166">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="84d92-167">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="84d92-167">-PublicIpAddressId</span></span>
<span data-ttu-id="84d92-168">Specifica l'ID di un oggetto **PublicIPAddress** da assegnare a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="84d92-168">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="84d92-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84d92-169">-ResourceGroupName</span></span>
<span data-ttu-id="84d92-170">Specifica il nome di un gruppo di risorse a cui appartiene l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="84d92-170">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="84d92-171">-Subnet</span><span class="sxs-lookup"><span data-stu-id="84d92-171">-Subnet</span></span>
<span data-ttu-id="84d92-172">Specifica un oggetto **subnet** .</span><span class="sxs-lookup"><span data-stu-id="84d92-172">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="84d92-173">Questo cmdlet crea un'interfaccia di rete per la subnet specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="84d92-173">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="84d92-174">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="84d92-174">-SubnetId</span></span>
<span data-ttu-id="84d92-175">Specifica l'ID della subnet per cui creare un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="84d92-175">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="84d92-176">-Tag</span><span class="sxs-lookup"><span data-stu-id="84d92-176">-Tag</span></span>
<span data-ttu-id="84d92-177">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="84d92-177">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="84d92-178">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="84d92-178">For example:</span></span>

<span data-ttu-id="84d92-179">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="84d92-179">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="84d92-180">-Confermare</span><span class="sxs-lookup"><span data-stu-id="84d92-180">-Confirm</span></span>
<span data-ttu-id="84d92-181">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84d92-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84d92-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84d92-182">-WhatIf</span></span>
<span data-ttu-id="84d92-183">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84d92-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84d92-184">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84d92-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84d92-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84d92-185">CommonParameters</span></span>
<span data-ttu-id="84d92-186">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84d92-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84d92-187">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84d92-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84d92-188">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84d92-188">INPUTS</span></span>

## <span data-ttu-id="84d92-189">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84d92-189">OUTPUTS</span></span>

### <span data-ttu-id="84d92-190">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="84d92-190">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="84d92-191">Note</span><span class="sxs-lookup"><span data-stu-id="84d92-191">NOTES</span></span>

## <span data-ttu-id="84d92-192">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84d92-192">RELATED LINKS</span></span>

[<span data-ttu-id="84d92-193">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="84d92-193">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="84d92-194">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="84d92-194">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="84d92-195">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="84d92-195">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)
