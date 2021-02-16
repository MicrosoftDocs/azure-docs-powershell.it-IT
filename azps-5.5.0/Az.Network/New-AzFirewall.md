---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 031c926d25fe55a9572fe12922ccee26b6371a2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179711"
---
# <span data-ttu-id="c38a3-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c38a3-101">New-AzFirewall</span></span>

## <span data-ttu-id="c38a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c38a3-102">SYNOPSIS</span></span>
<span data-ttu-id="c38a3-103">Crea un nuovo firewall in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c38a3-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="c38a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c38a3-104">SYNTAX</span></span>

### <span data-ttu-id="c38a3-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c38a3-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c38a3-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="c38a3-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c38a3-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="c38a3-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-EnableDnsProxy]
 [-DnsServer <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob] [-Zone <String[]>] [-SkuName <String>]
 [-SkuTier <String>] [-VirtualHubId <String>] [-HubIPAddress <PSAzureFirewallHubIpAddresses>]
 [-FirewallPolicyId <String>] [-AllowActiveFTP] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c38a3-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c38a3-108">DESCRIPTION</span></span>
<span data-ttu-id="c38a3-109">Il cmdlet **New-AzFirewall** crea un firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="c38a3-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="c38a3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c38a3-110">EXAMPLES</span></span>

### <span data-ttu-id="c38a3-111">Esempio 1: Creare un firewall collegato a una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="c38a3-111">Example 1: Create a Firewall attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="c38a3-112">Questo esempio crea un firewall collegato alla rete virtuale "vnet" nello stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="c38a3-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="c38a3-113">Poiché non sono state specificate regole, il firewall blocca tutto il traffico (comportamento predefinito).</span><span class="sxs-lookup"><span data-stu-id="c38a3-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="c38a3-114">Threat Intel verrà eseguito anche in modalità predefinita- Avviso, il che significa che verrà registrato traffico dannoso, ma non negato.</span><span class="sxs-lookup"><span data-stu-id="c38a3-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="c38a3-115">Esempio 2: Creare un firewall che consente tutto il traffico HTTPS</span><span class="sxs-lookup"><span data-stu-id="c38a3-115">Example 2: Create a Firewall which allows all HTTPS traffic</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="c38a3-116">Questo esempio crea un firewall che consente tutto il traffico HTTPS sulla porta 443.</span><span class="sxs-lookup"><span data-stu-id="c38a3-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="c38a3-117">Threat Intel verrà eseguito in modalità predefinita - Avviso: questo significa che verrà registrato traffico dannoso, ma non negato.</span><span class="sxs-lookup"><span data-stu-id="c38a3-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="c38a3-118">Esempio 3: REPLICAT - reindirizzamento del traffico destinato a 10.1.2.3:80 a 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="c38a3-118">Example 3: DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```powershell
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="c38a3-119">In questo esempio è stato creato un firewall che ha convertito l'IP di destinazione e la porta di tutti i pacchetti destinati a una versione da 10.1.2.3:80 a 10.2.3.4:8080 threat Intel disattivata.</span><span class="sxs-lookup"><span data-stu-id="c38a3-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="c38a3-120">Esempio 4: Creare un firewall senza regole e con Threat Intel in modalità avviso</span><span class="sxs-lookup"><span data-stu-id="c38a3-120">Example 4: Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="c38a3-121">Questo esempio crea un firewall che blocca tutto il traffico (comportamento predefinito) e ha Threat Intel in esecuzione in modalità avviso.</span><span class="sxs-lookup"><span data-stu-id="c38a3-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="c38a3-122">Questo significa che i log di avviso vengono emessi per traffico dannoso prima di applicare le altre regole (in questo caso solo la regola predefinita - Nega tutto)</span><span class="sxs-lookup"><span data-stu-id="c38a3-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="c38a3-123">Esempio 5: Creare un firewall che consente tutto il traffico HTTP sulla porta 8080, ma blocca i domini dannosi identificati da Threat Intel</span><span class="sxs-lookup"><span data-stu-id="c38a3-123">Example 5: Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="c38a3-124">Questo esempio crea un firewall che consente tutto il traffico HTTP sulla porta 8080 a meno che non sia considerato dannoso da Threat Intel.</span><span class="sxs-lookup"><span data-stu-id="c38a3-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="c38a3-125">A differenza degli avvisi, quando l'esecuzione è in esecuzione in modalità Nega, il traffico considerato dannoso da Threat Intel non viene solo registrato, ma anche bloccato.</span><span class="sxs-lookup"><span data-stu-id="c38a3-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="c38a3-126">Esempio 6: Creare un firewall senza regole e con aree di disponibilità</span><span class="sxs-lookup"><span data-stu-id="c38a3-126">Example 6: Create a Firewall with no rules and with availability zones</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="c38a3-127">Questo esempio crea un firewall con tutte le aree di disponibilità disponibili.</span><span class="sxs-lookup"><span data-stu-id="c38a3-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="c38a3-128">Esempio 7: Creare un firewall con due o più indirizzi IP pubblici</span><span class="sxs-lookup"><span data-stu-id="c38a3-128">Example 7: Create a Firewall with two or more Public IP Addresses</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -SkuName "AZFW_VNet" -SkuTier "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -SkuName "AZFW_VNet" -SkuTier "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="c38a3-129">Questo esempio crea un firewall collegato a una rete virtuale "vnet" con due indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="c38a3-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="c38a3-130">Esempio 8: Creare un firewall che consente il traffico MSSQL a un database SQL specifico</span><span class="sxs-lookup"><span data-stu-id="c38a3-130">Example 8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="c38a3-131">Questo esempio crea un firewall che consente il traffico MSSQL sulla porta standard 1433 per SQL di database sql1.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="c38a3-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

### <span data-ttu-id="c38a3-132">Esempio 9: Creare un firewall collegato a un hub virtuale</span><span class="sxs-lookup"><span data-stu-id="c38a3-132">Example 9: Create a Firewall attached to a virtual hub</span></span>
```powershell
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -SkuName AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

<span data-ttu-id="c38a3-133">Questo esempio crea un firewall collegato all'hub virtuale "vHub".</span><span class="sxs-lookup"><span data-stu-id="c38a3-133">This example creates a Firewall attached to virtual hub "vHub".</span></span> <span data-ttu-id="c38a3-134">Un $fp firewall verrà collegato al firewall.</span><span class="sxs-lookup"><span data-stu-id="c38a3-134">A firewall policy $fp will be attached to the firewall.</span></span> <span data-ttu-id="c38a3-135">Questo firewall consente/impedisce il traffico in base alle regole citate nel criterio del firewall $fp.</span><span class="sxs-lookup"><span data-stu-id="c38a3-135">This firewall allows/denies the traffic based on the rules mentioned in the firewall policy $fp.</span></span> <span data-ttu-id="c38a3-136">L'hub virtuale e il firewall devono essere nelle stesse aree geografiche.</span><span class="sxs-lookup"><span data-stu-id="c38a3-136">The virtual hub and the firewall should be in the same regions.</span></span>

### <span data-ttu-id="c38a3-137">Esempio 10: Creare un firewall con configurazione dell'elenco degli indirizzi vuoti di Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="c38a3-137">Example 10: Create a Firewall with threat intelligence whitelist setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

<span data-ttu-id="c38a3-138">Questo esempio crea un firewall che contiene gli elenchi dei firewall "www.microsoft.com" e "8.8.8.8" da Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="c38a3-138">This example creates a Firewall that whitelist "www.microsoft.com" and "8.8.8.8" from threat intelligence</span></span>

### <span data-ttu-id="c38a3-139">Esempio 11: Creare un firewall con la configurazione di intervalli privati personalizzati</span><span class="sxs-lookup"><span data-stu-id="c38a3-139">Example 11: Create a Firewall with customized private range setup</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

<span data-ttu-id="c38a3-140">Questo esempio crea un firewall che considera "99.99.99.0/24" e "66.66.0.0/16" come intervalli IP privati e non snat il traffico verso tali indirizzi.</span><span class="sxs-lookup"><span data-stu-id="c38a3-140">This example creates a Firewall that treats "99.99.99.0/24" and "66.66.0.0/16" as private ip ranges and won't snat traffic to those addresses</span></span>

### <span data-ttu-id="c38a3-141">Esempio 12: Creare un firewall con una subnet di gestione e un indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="c38a3-141">Example 12: Create a Firewall with a management subnet and Public IP address</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

<span data-ttu-id="c38a3-142">Questo esempio crea un firewall collegato alla rete virtuale "vnet" nello stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="c38a3-142">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="c38a3-143">Poiché non sono state specificate regole, il firewall blocca tutto il traffico (comportamento predefinito).</span><span class="sxs-lookup"><span data-stu-id="c38a3-143">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="c38a3-144">Threat Intel verrà eseguito anche in modalità predefinita- Avviso, il che significa che verrà registrato traffico dannoso, ma non negato.</span><span class="sxs-lookup"><span data-stu-id="c38a3-144">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

<span data-ttu-id="c38a3-145">Per supportare scenari di "tunneling forzato", questo firewall userà la subnet "AzureFirewallManagementSubnet" e l'indirizzo IP pubblico di gestione per il traffico di gestione</span><span class="sxs-lookup"><span data-stu-id="c38a3-145">To support "forced tunneling" scenarios, this firewall will use the subnet "AzureFirewallManagementSubnet" and the management public IP address for its management traffic</span></span>

### <span data-ttu-id="c38a3-146">Esempio 13: Creare un firewall con criteri firewall collegati a una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="c38a3-146">Example 13: Create a Firewall with Firewall Policy attached to a virtual network</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

<span data-ttu-id="c38a3-147">Questo esempio crea un firewall collegato alla rete virtuale "vnet" nello stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="c38a3-147">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="c38a3-148">Le regole e le informazioni sulle minacce che verranno applicate al firewall verranno prese dai criteri del firewall</span><span class="sxs-lookup"><span data-stu-id="c38a3-148">The rules and threat intelligence that will be applied to the firewall will be taken from the firewall policy</span></span>

### <span data-ttu-id="c38a3-149">Esempio 14: Creare un firewall con proxy DNS e server DNS</span><span class="sxs-lookup"><span data-stu-id="c38a3-149">Example 14: Create a Firewall with DNS Proxy and DNS Servers</span></span>
```powershell
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -DnsServer @("10.10.10.1", "20.20.20.2")
```

<span data-ttu-id="c38a3-150">Questo esempio crea un firewall collegato alla rete virtuale "vnet" nello stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="c38a3-150">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="c38a3-151">Il proxy DNS è abilitato per questo firewall e vengono forniti 2 server DNS.</span><span class="sxs-lookup"><span data-stu-id="c38a3-151">DNS Proxy is enabled for this firewall and 2 DNS Servers are provided.</span></span> <span data-ttu-id="c38a3-152">È impostata anche l'opzione Richiedi regole proxy DNS per la rete, quindi se sono presenti regole di rete con FQDN, verrà usato anche il proxy DNS.</span><span class="sxs-lookup"><span data-stu-id="c38a3-152">Also Require DNS Proxy for Network rules is set so if there are any Network rules with FQDNs then DNS proxy will be used for them too.</span></span>

### <span data-ttu-id="c38a3-153">Esempio 15: Creare un firewall con più IP.</span><span class="sxs-lookup"><span data-stu-id="c38a3-153">Example 15: Create a Firewall with multiple IPs.</span></span> <span data-ttu-id="c38a3-154">Il firewall può essere associato all'hub virtuale</span><span class="sxs-lookup"><span data-stu-id="c38a3-154">The Firewall can be associated with the Virtual Hub</span></span>
```powershell
$rgName = "resourceGroupName"
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id
$fwpips = New-AzFirewallHubPublicIpAddress -Count 2
$hubIpAddresses = New-AzFirewallHubIpAddress -PublicIPs $fwpips
$fw=New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location westus -SkuName AZFW_Hub -HubIPAddresses $hubIpAddresses -VirtualHubId $vHubId
```

<span data-ttu-id="c38a3-155">Questo esempio crea un firewall collegato all'hub virtuale "hub" nello stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="c38a3-155">This example creates a Firewall attached to virtual hub "hub" in the same resource group as the firewall.</span></span>
<span data-ttu-id="c38a3-156">Al firewall verranno assegnati due IP pubblici creati in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="c38a3-156">The Firewall will be assigned 2 public IPs that are created implicitly.</span></span>

### <span data-ttu-id="c38a3-157">16: Creare un firewall con Consenti FTP attivo.</span><span class="sxs-lookup"><span data-stu-id="c38a3-157">16:  Create a Firewall with Allow Active FTP.</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -AllowActiveFTP
```

<span data-ttu-id="c38a3-158">In questo esempio viene creato un firewall con il flag FTP attivo consentito.</span><span class="sxs-lookup"><span data-stu-id="c38a3-158">This example creates a Firewall with allow active FTP flag.</span></span>

## <span data-ttu-id="c38a3-159">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c38a3-159">PARAMETERS</span></span>

### <span data-ttu-id="c38a3-160">-AllowActiveFTP</span><span class="sxs-lookup"><span data-stu-id="c38a3-160">-AllowActiveFTP</span></span>
<span data-ttu-id="c38a3-161">Consente FTP attivo nel firewall.</span><span class="sxs-lookup"><span data-stu-id="c38a3-161">Allows Active FTP on the Firewall.</span></span> <span data-ttu-id="c38a3-162">Per impostazione predefinita, questa opzione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="c38a3-162">By default it is disabled.</span></span>


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

### <span data-ttu-id="c38a3-163">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c38a3-163">-ApplicationRuleCollection</span></span>
<span data-ttu-id="c38a3-164">Specifica le raccolte di regole dell'applicazione per il nuovo firewall.</span><span class="sxs-lookup"><span data-stu-id="c38a3-164">Specifies the collections of application rules for the new Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c38a3-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c38a3-165">-AsJob</span></span>
<span data-ttu-id="c38a3-166">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c38a3-166">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c38a3-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c38a3-167">-DefaultProfile</span></span>
<span data-ttu-id="c38a3-168">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c38a3-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c38a3-169">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="c38a3-169">-DnsServer</span></span>
<span data-ttu-id="c38a3-170">L'elenco dei server DNS da usare per la risoluzione DNS,</span><span class="sxs-lookup"><span data-stu-id="c38a3-170">The list of DNS Servers to be used for DNS resolution,</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38a3-171">-EnableDnsProxy</span><span class="sxs-lookup"><span data-stu-id="c38a3-171">-EnableDnsProxy</span></span>
<span data-ttu-id="c38a3-172">Abilitare il proxy DNS.</span><span class="sxs-lookup"><span data-stu-id="c38a3-172">Enable DNS Proxy.</span></span> <span data-ttu-id="c38a3-173">Per impostazione predefinita, questa opzione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="c38a3-173">By default it is disabled.</span></span>


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

### <span data-ttu-id="c38a3-174">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="c38a3-174">-FirewallPolicyId</span></span>
<span data-ttu-id="c38a3-175">Criterio del firewall collegato al firewall</span><span class="sxs-lookup"><span data-stu-id="c38a3-175">The firewall policy attached to the firewall</span></span>

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

### <span data-ttu-id="c38a3-176">-Force</span><span class="sxs-lookup"><span data-stu-id="c38a3-176">-Force</span></span>
<span data-ttu-id="c38a3-177">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="c38a3-177">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c38a3-178">-HubIPAddress</span><span class="sxs-lookup"><span data-stu-id="c38a3-178">-HubIPAddress</span></span>
<span data-ttu-id="c38a3-179">Gli indirizzi IP del firewall collegato a un hub virtuale</span><span class="sxs-lookup"><span data-stu-id="c38a3-179">The ip addresses for the firewall attached to a virtual hub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38a3-180">-Location</span><span class="sxs-lookup"><span data-stu-id="c38a3-180">-Location</span></span>
<span data-ttu-id="c38a3-181">Specifica l'area geografica per il firewall.</span><span class="sxs-lookup"><span data-stu-id="c38a3-181">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="c38a3-182">-ManagementPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c38a3-182">-ManagementPublicIpAddress</span></span>
<span data-ttu-id="c38a3-183">Uno o più indirizzi IP pubblici da usare per il traffico di gestione.</span><span class="sxs-lookup"><span data-stu-id="c38a3-183">One or more Public IP Addresses to use for management traffic.</span></span> <span data-ttu-id="c38a3-184">Gli indirizzi IP pubblici devono usare SKU standard e devono appartenere allo stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="c38a3-184">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c38a3-185">-Name</span><span class="sxs-lookup"><span data-stu-id="c38a3-185">-Name</span></span>
<span data-ttu-id="c38a3-186">Specifica il nome del firewall di Azure creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c38a3-186">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c38a3-187">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c38a3-187">-NatRuleCollection</span></span>
<span data-ttu-id="c38a3-188">Elenco di AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="c38a3-188">The list of AzureFirewallNatRuleCollections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c38a3-189">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c38a3-189">-NetworkRuleCollection</span></span>
<span data-ttu-id="c38a3-190">Elenco di AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="c38a3-190">The list of AzureFirewallNetworkRuleCollections</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c38a3-191">-PrivateRange</span><span class="sxs-lookup"><span data-stu-id="c38a3-191">-PrivateRange</span></span>
<span data-ttu-id="c38a3-192">Gli intervalli di indirizzi IP privati a cui il traffico non sarà SNAT</span><span class="sxs-lookup"><span data-stu-id="c38a3-192">The private IP ranges to which traffic won't be SNAT'ed</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38a3-193">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c38a3-193">-PublicIpAddress</span></span>
<span data-ttu-id="c38a3-194">Uno o più indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="c38a3-194">One or more Public IP Addresses.</span></span> <span data-ttu-id="c38a3-195">Gli indirizzi IP pubblici devono usare SKU standard e devono appartenere allo stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="c38a3-195">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c38a3-196">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="c38a3-196">-PublicIpName</span></span>
<span data-ttu-id="c38a3-197">Nome IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="c38a3-197">Public Ip Name.</span></span> <span data-ttu-id="c38a3-198">L'IP pubblico deve usare SKU standard e deve appartenere allo stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="c38a3-198">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c38a3-199">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c38a3-199">-ResourceGroupName</span></span>
<span data-ttu-id="c38a3-200">Specifica il nome di un gruppo di risorse che deve contenere il firewall.</span><span class="sxs-lookup"><span data-stu-id="c38a3-200">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="c38a3-201">-SKUName</span><span class="sxs-lookup"><span data-stu-id="c38a3-201">-SkuName</span></span>
<span data-ttu-id="c38a3-202">Nome SKU del firewall</span><span class="sxs-lookup"><span data-stu-id="c38a3-202">The sku name for firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Sku
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c38a3-203">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="c38a3-203">-SkuTier</span></span>
<span data-ttu-id="c38a3-204">Livello SKU per il firewall</span><span class="sxs-lookup"><span data-stu-id="c38a3-204">The sku tier for firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c38a3-205">-Tag</span><span class="sxs-lookup"><span data-stu-id="c38a3-205">-Tag</span></span>
<span data-ttu-id="c38a3-206">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c38a3-206">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c38a3-207">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="c38a3-207">For example:</span></span>

<span data-ttu-id="c38a3-208">@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="c38a3-208">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c38a3-209">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="c38a3-209">-ThreatIntelMode</span></span>
<span data-ttu-id="c38a3-210">Specifica la modalità di operazione per Threat Intelligence.</span><span class="sxs-lookup"><span data-stu-id="c38a3-210">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="c38a3-211">La modalità predefinita è Avviso, non Disattivata.</span><span class="sxs-lookup"><span data-stu-id="c38a3-211">Default mode is Alert, not Off.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c38a3-212">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="c38a3-212">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="c38a3-213">Elenco degli indirizzi vuoti per Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="c38a3-213">The whitelist for Threat Intelligence</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38a3-214">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="c38a3-214">-VirtualHubId</span></span>
<span data-ttu-id="c38a3-215">Hub virtuale a cui è collegato un firewall</span><span class="sxs-lookup"><span data-stu-id="c38a3-215">The virtual hub that a firewall is attached to</span></span>

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

### <span data-ttu-id="c38a3-216">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c38a3-216">-VirtualNetwork</span></span>
<span data-ttu-id="c38a3-217">Rete virtuale</span><span class="sxs-lookup"><span data-stu-id="c38a3-217">Virtual Network</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c38a3-218">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="c38a3-218">-VirtualNetworkName</span></span>
<span data-ttu-id="c38a3-219">Specifica il nome della rete virtuale per cui verrà distribuito il firewall.</span><span class="sxs-lookup"><span data-stu-id="c38a3-219">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="c38a3-220">Rete virtuale e Firewall devono appartenere allo stesso gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c38a3-220">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: OldIpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c38a3-221">-Zone</span><span class="sxs-lookup"><span data-stu-id="c38a3-221">-Zone</span></span>
<span data-ttu-id="c38a3-222">Un elenco delle aree di disponibilità che denotono la posizione da cui deve provengono il firewall.</span><span class="sxs-lookup"><span data-stu-id="c38a3-222">A list of availability zones denoting where the firewall needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38a3-223">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c38a3-223">-Confirm</span></span>
<span data-ttu-id="c38a3-224">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c38a3-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c38a3-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c38a3-225">-WhatIf</span></span>
<span data-ttu-id="c38a3-226">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c38a3-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c38a3-227">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c38a3-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c38a3-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c38a3-228">CommonParameters</span></span>
<span data-ttu-id="c38a3-229">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c38a3-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c38a3-230">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c38a3-230">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c38a3-231">INPUT</span><span class="sxs-lookup"><span data-stu-id="c38a3-231">INPUTS</span></span>

### <span data-ttu-id="c38a3-232">System.String</span><span class="sxs-lookup"><span data-stu-id="c38a3-232">System.String</span></span>

### <span data-ttu-id="c38a3-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c38a3-233">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="c38a3-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span><span class="sxs-lookup"><span data-stu-id="c38a3-234">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="c38a3-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c38a3-235">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="c38a3-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span><span class="sxs-lookup"><span data-stu-id="c38a3-236">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="c38a3-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span><span class="sxs-lookup"><span data-stu-id="c38a3-237">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="c38a3-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span><span class="sxs-lookup"><span data-stu-id="c38a3-238">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="c38a3-239">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c38a3-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c38a3-240">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c38a3-240">OUTPUTS</span></span>

### <span data-ttu-id="c38a3-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="c38a3-241">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="c38a3-242">NOTE</span><span class="sxs-lookup"><span data-stu-id="c38a3-242">NOTES</span></span>

## <span data-ttu-id="c38a3-243">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c38a3-243">RELATED LINKS</span></span>

[<span data-ttu-id="c38a3-244">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c38a3-244">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="c38a3-245">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c38a3-245">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="c38a3-246">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c38a3-246">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="c38a3-247">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c38a3-247">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="c38a3-248">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c38a3-248">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="c38a3-249">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c38a3-249">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
