---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: a7c38a264860ad4a8458dbdb3555980279a33ff0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192819"
---
# <span data-ttu-id="64c57-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="64c57-101">New-AzFirewall</span></span>

## <span data-ttu-id="64c57-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64c57-102">SYNOPSIS</span></span>
<span data-ttu-id="64c57-103">Crea un nuovo firewall in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="64c57-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="64c57-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64c57-104">SYNTAX</span></span>

### <span data-ttu-id="64c57-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="64c57-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsProxyNotRequiredForNetworkRule] [-DnsServer <String[]>] [-AllowActiveFTP] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-HubIPAddresses <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64c57-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="64c57-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsProxyNotRequiredForNetworkRule] [-DnsServer <String[]>] [-AllowActiveFTP] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-HubIPAddresses <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64c57-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="64c57-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsProxyNotRequiredForNetworkRule] [-DnsServer <String[]>] [-AllowActiveFTP] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-HubIPAddresses <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="64c57-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64c57-108">DESCRIPTION</span></span>
<span data-ttu-id="64c57-109">Il cmdlet **New-AzFirewall** crea un firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="64c57-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="64c57-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64c57-110">EXAMPLES</span></span>

### <span data-ttu-id="64c57-111">Esempio 1: creare un firewall collegato a una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="64c57-111">Example 1: Create a Firewall attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="64c57-112">Questo esempio crea un firewall collegato alla rete virtuale "VNET" nello stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="64c57-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="64c57-113">Dato che non sono state specificate regole, il firewall bloccherà tutto il traffico (comportamento predefinito).</span><span class="sxs-lookup"><span data-stu-id="64c57-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="64c57-114">Le minacce Intel verranno eseguite anche in modalità predefinita-avviso-il che significa che il traffico illecito verrà registrato, ma non negato.</span><span class="sxs-lookup"><span data-stu-id="64c57-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="64c57-115">Esempio 2: creare un firewall che consente tutto il traffico HTTPS</span><span class="sxs-lookup"><span data-stu-id="64c57-115">Example 2: Create a Firewall which allows all HTTPS traffic</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="64c57-116">Questo esempio crea un firewall che consente tutto il traffico HTTPS sulla porta 443.</span><span class="sxs-lookup"><span data-stu-id="64c57-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="64c57-117">Threat Intel verrà eseguito in modalità predefinita-avviso-il che significa che il traffico illecito verrà registrato, ma non negato.</span><span class="sxs-lookup"><span data-stu-id="64c57-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="64c57-118">Esempio 3: DNAT-reindirizza il traffico destinato a 10.1.2.3:80 a 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="64c57-118">Example 3: DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```powershell
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="64c57-119">Questo esempio ha creato un firewall che ha tradotto l'indirizzo IP di destinazione e la porta di tutti i pacchetti destinati a 10.1.2.3:80 a 10.2.3.4:8080 Threat Intel è disattivata in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="64c57-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="64c57-120">Esempio 4: creare un firewall senza regole e con Intel Threat in modalità avviso</span><span class="sxs-lookup"><span data-stu-id="64c57-120">Example 4: Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="64c57-121">Questo esempio crea un firewall che blocca tutto il traffico (comportamento predefinito) ed è in uso in modalità avviso.</span><span class="sxs-lookup"><span data-stu-id="64c57-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="64c57-122">Questo significa che i registri di avviso vengono emessi per il traffico illecito prima di applicare le altre regole (in questo caso solo la regola predefinita-Deny All)</span><span class="sxs-lookup"><span data-stu-id="64c57-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="64c57-123">Esempio 5: creare un firewall che consente tutto il traffico HTTP sulla porta 8080, ma blocca i domini malevoli identificati da Intel Threat</span><span class="sxs-lookup"><span data-stu-id="64c57-123">Example 5: Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="64c57-124">Questo esempio crea un firewall che consente tutto il traffico HTTP sulla porta 8080, a meno che non sia considerato dannoso da Intel Threat.</span><span class="sxs-lookup"><span data-stu-id="64c57-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="64c57-125">Quando l'utente viene eseguito in modalità di negazione, diversamente da Alert, il traffico considerato malevolo da Intel Threat non è solo registrato, ma anche bloccato.</span><span class="sxs-lookup"><span data-stu-id="64c57-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="64c57-126">Esempio 6: creare un firewall senza regole e con le aree di disponibilità</span><span class="sxs-lookup"><span data-stu-id="64c57-126">Example 6: Create a Firewall with no rules and with availability zones</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="64c57-127">Questo esempio crea un firewall con tutte le aree di disponibilità disponibili.</span><span class="sxs-lookup"><span data-stu-id="64c57-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="64c57-128">Esempio 7: creare un firewall con due o più indirizzi IP pubblici</span><span class="sxs-lookup"><span data-stu-id="64c57-128">Example 7: Create a Firewall with two or more Public IP Addresses</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="64c57-129">Questo esempio crea un firewall collegato alla rete virtuale "VNET" con due indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="64c57-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="64c57-130">Esempio 8: creare un firewall che consente il traffico di MSSQL per database SQL specifico</span><span class="sxs-lookup"><span data-stu-id="64c57-130">Example 8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="64c57-131">Questo esempio crea un firewall che consente il traffico di MSSQL sulla porta standard 1433 per il database SQL sql1.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="64c57-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

### <span data-ttu-id="64c57-132">Esempio 9: creare un firewall collegato a un hub virtuale</span><span class="sxs-lookup"><span data-stu-id="64c57-132">Example 9: Create a Firewall attached to a virtual hub</span></span>
```powershell
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -Sku AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

<span data-ttu-id="64c57-133">Questo esempio crea un firewall allegato all'hub virtuale "vHub".</span><span class="sxs-lookup"><span data-stu-id="64c57-133">This example creates a Firewall attached to virtual hub "vHub".</span></span> <span data-ttu-id="64c57-134">Un criterio firewall $fp verrà allegato al firewall.</span><span class="sxs-lookup"><span data-stu-id="64c57-134">A firewall policy $fp will be attached to the firewall.</span></span> <span data-ttu-id="64c57-135">Questo firewall consente/nega il traffico in base alle regole menzionate nel $fp criteri firewall.</span><span class="sxs-lookup"><span data-stu-id="64c57-135">This firewall allows/denies the traffic based on the rules mentioned in the firewall policy $fp.</span></span> <span data-ttu-id="64c57-136">L'hub virtuale e il firewall devono trovarsi nelle stesse aree geografiche.</span><span class="sxs-lookup"><span data-stu-id="64c57-136">The virtual hub and the firewall should be in the same regions.</span></span>

### <span data-ttu-id="64c57-137">Esempio 10: creare un firewall con la configurazione whitelist di Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="64c57-137">Example 10: Create a Firewall with threat intelligence whitelist setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

<span data-ttu-id="64c57-138">Questo esempio crea un firewall che whitelist "www.microsoft.com" e "8.8.8.8" da Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="64c57-138">This example creates a Firewall that whitelist "www.microsoft.com" and "8.8.8.8" from threat intelligence</span></span>

### <span data-ttu-id="64c57-139">Esempio 11: creare un firewall con l'installazione di intervalli privati personalizzati</span><span class="sxs-lookup"><span data-stu-id="64c57-139">Example 11: Create a Firewall with customized private range setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

<span data-ttu-id="64c57-140">Questo esempio crea un firewall che tratta "99.99.99.0/24" e "66.66.0.0/16" come intervalli IP privati e non SNAT il traffico a tali indirizzi</span><span class="sxs-lookup"><span data-stu-id="64c57-140">This example creates a Firewall that treats "99.99.99.0/24" and "66.66.0.0/16" as private ip ranges and won't snat traffic to those addresses</span></span>

### <span data-ttu-id="64c57-141">Esempio 12: creare un firewall con una subnet di gestione e un indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="64c57-141">Example 12: Create a Firewall with a management subnet and Public IP address</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

<span data-ttu-id="64c57-142">Questo esempio crea un firewall collegato alla rete virtuale "VNET" nello stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="64c57-142">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="64c57-143">Dato che non sono state specificate regole, il firewall bloccherà tutto il traffico (comportamento predefinito).</span><span class="sxs-lookup"><span data-stu-id="64c57-143">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="64c57-144">Le minacce Intel verranno eseguite anche in modalità predefinita-avviso-il che significa che il traffico illecito verrà registrato, ma non negato.</span><span class="sxs-lookup"><span data-stu-id="64c57-144">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

<span data-ttu-id="64c57-145">Per supportare scenari di "tunneling forzato", questo firewall utilizzerà la subnet "AzureFirewallManagementSubnet" e l'indirizzo IP pubblico di gestione per il traffico di gestione</span><span class="sxs-lookup"><span data-stu-id="64c57-145">To support "forced tunneling" scenarios, this firewall will use the subnet "AzureFirewallManagementSubnet" and the management public IP address for its management traffic</span></span>

### <span data-ttu-id="64c57-146">Esempio 13: creare un firewall con criteri firewall collegati a una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="64c57-146">Example 13: Create a Firewall with Firewall Policy attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

<span data-ttu-id="64c57-147">Questo esempio crea un firewall collegato alla rete virtuale "VNET" nello stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="64c57-147">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="64c57-148">Le regole e le minacce di intelligence che verranno applicate al firewall verranno ricavate dal criterio firewall</span><span class="sxs-lookup"><span data-stu-id="64c57-148">The rules and threat intelligence that will be applied to the firewall will be taken from the firewall policy</span></span>

### <span data-ttu-id="64c57-149">Esempio 14: creare un firewall con proxy DNS e server DNS</span><span class="sxs-lookup"><span data-stu-id="64c57-149">Example 14: Create a Firewall with DNS Proxy and DNS Servers</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -DnsServer @("10.10.10.1", "20.20.20.2")
```

<span data-ttu-id="64c57-150">Questo esempio crea un firewall collegato alla rete virtuale "VNET" nello stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="64c57-150">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="64c57-151">Proxy DNS è abilitato per questo firewall e sono disponibili 2 server DNS.</span><span class="sxs-lookup"><span data-stu-id="64c57-151">DNS Proxy is enabled for this firewall and 2 DNS Servers are provided.</span></span> <span data-ttu-id="64c57-152">Richiede inoltre che il proxy DNS per le regole di rete sia impostato, quindi se esistono regole di rete con FQDN, verrà usato anche il proxy DNS.</span><span class="sxs-lookup"><span data-stu-id="64c57-152">Also Require DNS Proxy for Network rules is set so if there are any Network rules with FQDNs then DNS proxy will be used for them too.</span></span>

### <span data-ttu-id="64c57-153">Esempio 15: creare un firewall con più IPs.</span><span class="sxs-lookup"><span data-stu-id="64c57-153">Example 15: Create a Firewall with multiple IPs.</span></span> <span data-ttu-id="64c57-154">Il firewall può essere associato all'hub virtuale</span><span class="sxs-lookup"><span data-stu-id="64c57-154">The Firewall can be associated with the Virtual Hub</span></span>
```powershell
$rgName = "resourceGroupName"
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id
$fwpips = New-AzFirewallHubPublicIpAddress -Count 2
$hubIpAddresses = New-AzFirewallHubIpAddress -PublicIPs $fwpips
$fw=New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location westus -Sku AZFW_Hub -HubIPAddresses $hubIpAddresses -VirtualHubId $vHubId
```

<span data-ttu-id="64c57-155">Questo esempio crea un firewall collegato all'hub virtuale "hub" nello stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="64c57-155">This example creates a Firewall attached to virtual hub "hub" in the same resource group as the firewall.</span></span>
<span data-ttu-id="64c57-156">Al firewall verranno assegnati due indirizzi IP pubblici creati in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="64c57-156">The Firewall will be assigned 2 public IPs that are created implicitly.</span></span>

### <span data-ttu-id="64c57-157">16: creare un firewall con Consenti FTP attivo.</span><span class="sxs-lookup"><span data-stu-id="64c57-157">16:  Create a Firewall with Allow Active FTP.</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -AllowActiveFTP
```

<span data-ttu-id="64c57-158">Questo esempio crea un firewall con l'opzione Consenti FTP attivo.</span><span class="sxs-lookup"><span data-stu-id="64c57-158">This example creates a Firewall with allow active FTP flag.</span></span>

## <span data-ttu-id="64c57-159">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64c57-159">PARAMETERS</span></span>

### <span data-ttu-id="64c57-160">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="64c57-160">-ApplicationRuleCollection</span></span>
<span data-ttu-id="64c57-161">Specifica le raccolte di regole dell'applicazione per il nuovo firewall.</span><span class="sxs-lookup"><span data-stu-id="64c57-161">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: PSAzureFirewallApplicationRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64c57-162">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64c57-162">-AsJob</span></span>
<span data-ttu-id="64c57-163">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="64c57-163">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64c57-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64c57-164">-DefaultProfile</span></span>
<span data-ttu-id="64c57-165">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64c57-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c57-166">-DnsProxyNotRequiredForNetworkRule</span><span class="sxs-lookup"><span data-stu-id="64c57-166">-DnsProxyNotRequiredForNetworkRule</span></span>
<span data-ttu-id="64c57-167">Richiede la funzionalità proxy DNS per gli FQDN nelle regole di rete.</span><span class="sxs-lookup"><span data-stu-id="64c57-167">Requires DNS Proxy functionality for FQDNs within Network Rules.</span></span>

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

### <span data-ttu-id="64c57-168">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="64c57-168">-DnsServer</span></span>
<span data-ttu-id="64c57-169">L'elenco dei server DNS da usare per la risoluzione DNS,</span><span class="sxs-lookup"><span data-stu-id="64c57-169">The list of DNS Servers to be used for DNS resolution,</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c57-170">-EnableDnsProxy</span><span class="sxs-lookup"><span data-stu-id="64c57-170">-EnableDnsProxy</span></span>
<span data-ttu-id="64c57-171">Abilita proxy DNS.</span><span class="sxs-lookup"><span data-stu-id="64c57-171">Enable DNS Proxy.</span></span> <span data-ttu-id="64c57-172">Per impostazione predefinita, è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="64c57-172">By default it is disabled.</span></span>


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

### <span data-ttu-id="64c57-173">-AllowActiveFTP</span><span class="sxs-lookup"><span data-stu-id="64c57-173">-AllowActiveFTP</span></span>
<span data-ttu-id="64c57-174">Consente l'FTP attivo sul firewall.</span><span class="sxs-lookup"><span data-stu-id="64c57-174">Allows Active FTP on the Firewall.</span></span> <span data-ttu-id="64c57-175">Per impostazione predefinita, è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="64c57-175">By default it is disabled.</span></span>


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

### <span data-ttu-id="64c57-176">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="64c57-176">-FirewallPolicyId</span></span>
<span data-ttu-id="64c57-177">Criteri firewall allegati al firewall</span><span class="sxs-lookup"><span data-stu-id="64c57-177">The firewall policy attached to the firewall</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64c57-178">-Force</span><span class="sxs-lookup"><span data-stu-id="64c57-178">-Force</span></span>
<span data-ttu-id="64c57-179">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="64c57-179">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="64c57-180">-HubIPAddresses</span><span class="sxs-lookup"><span data-stu-id="64c57-180">-HubIPAddresses</span></span>
<span data-ttu-id="64c57-181">Indirizzi IP per il firewall allegato a un hub virtuale</span><span class="sxs-lookup"><span data-stu-id="64c57-181">The ip addresses for the firewall attached to a virtual hub</span></span>

```yaml
Type: PSAzureFirewallHubIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c57-182">-Posizione</span><span class="sxs-lookup"><span data-stu-id="64c57-182">-Location</span></span>
<span data-ttu-id="64c57-183">Specifica l'area geografica per il firewall.</span><span class="sxs-lookup"><span data-stu-id="64c57-183">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="64c57-184">-ManagementPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="64c57-184">-ManagementPublicIpAddress</span></span>
<span data-ttu-id="64c57-185">Uno o più indirizzi IP pubblici da usare per il traffico di gestione.</span><span class="sxs-lookup"><span data-stu-id="64c57-185">One or more Public IP Addresses to use for management traffic.</span></span> <span data-ttu-id="64c57-186">Gli indirizzi IP pubblici devono usare SKU standard e devono appartenere allo stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="64c57-186">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64c57-187">-Nome</span><span class="sxs-lookup"><span data-stu-id="64c57-187">-Name</span></span>
<span data-ttu-id="64c57-188">Specifica il nome del firewall di Azure creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64c57-188">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="64c57-189">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="64c57-189">-NatRuleCollection</span></span>
<span data-ttu-id="64c57-190">Elenco di AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="64c57-190">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: PSAzureFirewallNatRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64c57-191">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="64c57-191">-NetworkRuleCollection</span></span>
<span data-ttu-id="64c57-192">Elenco di AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="64c57-192">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: PSAzureFirewallNetworkRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64c57-193">-PrivateRange</span><span class="sxs-lookup"><span data-stu-id="64c57-193">-PrivateRange</span></span>
<span data-ttu-id="64c57-194">Gli intervalli IP privati a cui il traffico non verrà SNAT'ed</span><span class="sxs-lookup"><span data-stu-id="64c57-194">The private IP ranges to which traffic won't be SNAT'ed</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c57-195">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="64c57-195">-PublicIpAddress</span></span>
<span data-ttu-id="64c57-196">Uno o più indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="64c57-196">One or more Public IP Addresses.</span></span> <span data-ttu-id="64c57-197">Gli indirizzi IP pubblici devono usare SKU standard e devono appartenere allo stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="64c57-197">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: PSPublicIpAddress[]
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64c57-198">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="64c57-198">-PublicIpName</span></span>
<span data-ttu-id="64c57-199">Nome IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="64c57-199">Public Ip Name.</span></span> <span data-ttu-id="64c57-200">L'IP pubblico deve usare SKU standard e deve appartenere allo stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="64c57-200">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64c57-201">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64c57-201">-ResourceGroupName</span></span>
<span data-ttu-id="64c57-202">Specifica il nome di un gruppo di risorse che contiene il firewall.</span><span class="sxs-lookup"><span data-stu-id="64c57-202">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="64c57-203">-SKU</span><span class="sxs-lookup"><span data-stu-id="64c57-203">-Sku</span></span>
<span data-ttu-id="64c57-204">Tipo di SKU per il firewall</span><span class="sxs-lookup"><span data-stu-id="64c57-204">The sku type for firewall</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64c57-205">-Tag</span><span class="sxs-lookup"><span data-stu-id="64c57-205">-Tag</span></span>
<span data-ttu-id="64c57-206">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="64c57-206">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="64c57-207">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="64c57-207">For example:</span></span>

<span data-ttu-id="64c57-208">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="64c57-208">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="64c57-209">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="64c57-209">-ThreatIntelMode</span></span>
<span data-ttu-id="64c57-210">Specifica la modalità operativa per Threat Intelligence.</span><span class="sxs-lookup"><span data-stu-id="64c57-210">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="64c57-211">La modalità predefinita è Alert, non disattivata.</span><span class="sxs-lookup"><span data-stu-id="64c57-211">Default mode is Alert, not Off.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64c57-212">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="64c57-212">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="64c57-213">Whitelist per Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="64c57-213">The whitelist for Threat Intelligence</span></span>

```yaml
Type: PSAzureFirewallThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c57-214">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="64c57-214">-VirtualHubId</span></span>
<span data-ttu-id="64c57-215">Hub virtuale a cui è associato un firewall</span><span class="sxs-lookup"><span data-stu-id="64c57-215">The virtual hub that a firewall is attached to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64c57-216">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="64c57-216">-VirtualNetwork</span></span>
<span data-ttu-id="64c57-217">Rete virtuale</span><span class="sxs-lookup"><span data-stu-id="64c57-217">Virtual Network</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64c57-218">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="64c57-218">-VirtualNetworkName</span></span>
<span data-ttu-id="64c57-219">Specifica il nome della rete virtuale per cui verrà distribuito il firewall.</span><span class="sxs-lookup"><span data-stu-id="64c57-219">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="64c57-220">La rete virtuale e il firewall devono appartenere allo stesso gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="64c57-220">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64c57-221">-Zona</span><span class="sxs-lookup"><span data-stu-id="64c57-221">-Zone</span></span>
<span data-ttu-id="64c57-222">Elenco delle aree di disponibilità che denotano da dove deve provenire il firewall.</span><span class="sxs-lookup"><span data-stu-id="64c57-222">A list of availability zones denoting where the firewall needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c57-223">-Confermare</span><span class="sxs-lookup"><span data-stu-id="64c57-223">-Confirm</span></span>
<span data-ttu-id="64c57-224">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64c57-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64c57-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64c57-225">-WhatIf</span></span>
<span data-ttu-id="64c57-226">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64c57-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64c57-227">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="64c57-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64c57-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64c57-228">CommonParameters</span></span>
<span data-ttu-id="64c57-229">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64c57-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64c57-230">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64c57-230">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64c57-231">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64c57-231">INPUTS</span></span>

### <span data-ttu-id="64c57-232">System. String</span><span class="sxs-lookup"><span data-stu-id="64c57-232">System.String</span></span>

### <span data-ttu-id="64c57-233">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="64c57-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="64c57-234">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress []</span><span class="sxs-lookup"><span data-stu-id="64c57-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="64c57-235">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="64c57-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="64c57-236">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="64c57-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="64c57-237">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="64c57-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="64c57-238">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="64c57-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="64c57-239">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="64c57-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="64c57-240">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64c57-240">OUTPUTS</span></span>

### <span data-ttu-id="64c57-241">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="64c57-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="64c57-242">Note</span><span class="sxs-lookup"><span data-stu-id="64c57-242">NOTES</span></span>

## <span data-ttu-id="64c57-243">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64c57-243">RELATED LINKS</span></span>

[<span data-ttu-id="64c57-244">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="64c57-244">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="64c57-245">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="64c57-245">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="64c57-246">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="64c57-246">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="64c57-247">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="64c57-247">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="64c57-248">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="64c57-248">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="64c57-249">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="64c57-249">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
