---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 3b4014b56a36228fe53221430ffe79a43118f8fe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864162"
---
# <span data-ttu-id="d836b-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d836b-101">New-AzFirewall</span></span>

## <span data-ttu-id="d836b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d836b-102">SYNOPSIS</span></span>
<span data-ttu-id="d836b-103">Crea un nuovo firewall in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d836b-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="d836b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d836b-104">SYNTAX</span></span>

### <span data-ttu-id="d836b-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d836b-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-FirewallPolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d836b-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="d836b-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-FirewallPolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d836b-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="d836b-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]> [-ManagementPublicIpAddress <PSPublicIpAddress>]
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallThreatIntelWhitelist>] [-PrivateRange <String[]>] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-Zone <String[]>] [-Sku <String>] [-VirtualHubId <String>] [-FirewallPolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d836b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d836b-108">DESCRIPTION</span></span>
<span data-ttu-id="d836b-109">Il cmdlet **New-AzFirewall** crea un firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="d836b-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="d836b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d836b-110">EXAMPLES</span></span>

### <span data-ttu-id="d836b-111">1: creare un firewall collegato a una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="d836b-111">1:  Create a Firewall attached to a virtual network</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="d836b-112">Questo esempio crea un firewall collegato alla rete virtuale "VNET" nello stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="d836b-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="d836b-113">Dato che non sono state specificate regole, il firewall bloccherà tutto il traffico (comportamento predefinito).</span><span class="sxs-lookup"><span data-stu-id="d836b-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="d836b-114">Le minacce Intel verranno eseguite anche in modalità predefinita-avviso-il che significa che il traffico illecito verrà registrato, ma non negato.</span><span class="sxs-lookup"><span data-stu-id="d836b-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="d836b-115">2: creare un firewall che consente tutto il traffico HTTPS</span><span class="sxs-lookup"><span data-stu-id="d836b-115">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="d836b-116">Questo esempio crea un firewall che consente tutto il traffico HTTPS sulla porta 443.</span><span class="sxs-lookup"><span data-stu-id="d836b-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="d836b-117">Threat Intel verrà eseguito in modalità predefinita-avviso-il che significa che il traffico illecito verrà registrato, ma non negato.</span><span class="sxs-lookup"><span data-stu-id="d836b-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="d836b-118">3: DNAT-reindirizza il traffico destinato a 10.1.2.3:80 a 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="d836b-118">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="d836b-119">Questo esempio ha creato un firewall che ha tradotto l'indirizzo IP di destinazione e la porta di tutti i pacchetti destinati a 10.1.2.3:80 a 10.2.3.4:8080 Threat Intel è disattivata in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="d836b-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="d836b-120">4: creare un firewall senza regole e con le minacce Intel in modalità avviso</span><span class="sxs-lookup"><span data-stu-id="d836b-120">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="d836b-121">Questo esempio crea un firewall che blocca tutto il traffico (comportamento predefinito) ed è in uso in modalità avviso.</span><span class="sxs-lookup"><span data-stu-id="d836b-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="d836b-122">Questo significa che i registri di avviso vengono emessi per il traffico illecito prima di applicare le altre regole (in questo caso solo la regola predefinita-Deny All)</span><span class="sxs-lookup"><span data-stu-id="d836b-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="d836b-123">5: creare un firewall che consente tutto il traffico HTTP sulla porta 8080, ma blocca i domini malevoli identificati da Intel Threat</span><span class="sxs-lookup"><span data-stu-id="d836b-123">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="d836b-124">Questo esempio crea un firewall che consente tutto il traffico HTTP sulla porta 8080, a meno che non sia considerato dannoso da Intel Threat.</span><span class="sxs-lookup"><span data-stu-id="d836b-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="d836b-125">Quando l'utente viene eseguito in modalità di negazione, diversamente da Alert, il traffico considerato malevolo da Intel Threat non è solo registrato, ma anche bloccato.</span><span class="sxs-lookup"><span data-stu-id="d836b-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="d836b-126">6: creare un firewall senza regole e con le aree di disponibilità</span><span class="sxs-lookup"><span data-stu-id="d836b-126">6:  Create a Firewall with no rules and with availability zones</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="d836b-127">Questo esempio crea un firewall con tutte le aree di disponibilità disponibili.</span><span class="sxs-lookup"><span data-stu-id="d836b-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="d836b-128">7: creare un firewall con due o più indirizzi IP pubblici</span><span class="sxs-lookup"><span data-stu-id="d836b-128">7: Create a Firewall with two or more Public IP Addresses</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="d836b-129">Questo esempio crea un firewall collegato alla rete virtuale "VNET" con due indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="d836b-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="d836b-130">8: creare un firewall che consente il traffico di MSSQL per database SQL specifico</span><span class="sxs-lookup"><span data-stu-id="d836b-130">8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="d836b-131">Questo esempio crea un firewall che consente il traffico di MSSQL sulla porta standard 1433 per il database SQL sql1.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="d836b-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

### <span data-ttu-id="d836b-132">9: creare un firewall collegato a un hub virtuale</span><span class="sxs-lookup"><span data-stu-id="d836b-132">9:  Create a Firewall attached to a virtual hub</span></span>
```
$rgName = "resourceGroupName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
$fpId = $fp.Id
$vHub = Get-AzVirtualHub -Name "hub"
$vHubId = $vHub.Id

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -Sku AZFW_Hub -VirtualHubId $vHubId -FirewallPolicyId -$fpId
```

<span data-ttu-id="d836b-133">Questo esempio crea un firewall allegato all'hub virtuale "vHub".</span><span class="sxs-lookup"><span data-stu-id="d836b-133">This example creates a Firewall attached to virtual hub "vHub".</span></span> <span data-ttu-id="d836b-134">Un criterio firewall $fp verrà allegato al firewall.</span><span class="sxs-lookup"><span data-stu-id="d836b-134">A firewall policy $fp will be attached to the firewall.</span></span> <span data-ttu-id="d836b-135">Questo firewall consente/nega il traffico in base alle regole menzionate nel $fp criteri firewall.</span><span class="sxs-lookup"><span data-stu-id="d836b-135">This firewall allows/denies the traffic based on the rules mentioned in the firewall policy $fp.</span></span> <span data-ttu-id="d836b-136">L'hub virtuale e il firewall devono trovarsi nelle stesse aree geografiche.</span><span class="sxs-lookup"><span data-stu-id="d836b-136">The virtual hub and the firewall should be in the same regions.</span></span>

### <span data-ttu-id="d836b-137">10: creare un firewall con la configurazione whitelist di Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="d836b-137">10: Create a Firewall with threat intelligence whitelist setup</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$tiWhitelist = New-AzFirewallThreatIntelWhitelist -FQDN @("www.microsoft.com") -IpAddresses @("8.8.8.8")
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelWhitelist $tiWhitelist
```

<span data-ttu-id="d836b-138">Questo esempio crea un firewall che whitelist "www.microsoft.com" e "8.8.8.8" da Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="d836b-138">This example creates a Firewall that whitelist "www.microsoft.com" and "8.8.8.8" from threat intelligence</span></span>

### <span data-ttu-id="d836b-139">11: creare un firewall con configurazione di intervalli privati personalizzata</span><span class="sxs-lookup"><span data-stu-id="d836b-139">11: Create a Firewall with customized private range setup</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -PrivateRange @("99.99.99.0/24", "66.66.0.0/16")
```

<span data-ttu-id="d836b-140">Questo esempio crea un firewall che tratta "99.99.99.0/24" e "66.66.0.0/16" come intervalli IP privati e non SNAT il traffico a tali indirizzi</span><span class="sxs-lookup"><span data-stu-id="d836b-140">This example creates a Firewall that treats "99.99.99.0/24" and "66.66.0.0/16" as private ip ranges and won't snat traffic to those addresses</span></span>

### <span data-ttu-id="d836b-141">12: creare un firewall con una subnet di gestione e un indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="d836b-141">12:  Create a Firewall with a management subnet and Public IP address</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "managementPublicIpName"

New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ManagementPublicIpAddress $mgmtPip
```

<span data-ttu-id="d836b-142">Questo esempio crea un firewall collegato alla rete virtuale "VNET" nello stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="d836b-142">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="d836b-143">Dato che non sono state specificate regole, il firewall bloccherà tutto il traffico (comportamento predefinito).</span><span class="sxs-lookup"><span data-stu-id="d836b-143">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="d836b-144">Le minacce Intel verranno eseguite anche in modalità predefinita-avviso-il che significa che il traffico illecito verrà registrato, ma non negato.</span><span class="sxs-lookup"><span data-stu-id="d836b-144">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

<span data-ttu-id="d836b-145">Per supportare scenari di "tunneling forzato", questo firewall utilizzerà la subnet "AzureFirewallManagementSubnet" e l'indirizzo IP pubblico di gestione per il traffico di gestione</span><span class="sxs-lookup"><span data-stu-id="d836b-145">To support "forced tunneling" scenarios, this firewall will use the subnet "AzureFirewallManagementSubnet" and the management public IP address for its management traffic</span></span>

### <span data-ttu-id="d836b-146">13: creare un firewall con criteri firewall collegati a una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="d836b-146">13:  Create a Firewall with Firewall Policy attached to a virtual network</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
$fp = Get-AzFirewallPolicy -ResourceGroupName $rgName -Name "fp"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -FirewallPolicyId $fp
```

<span data-ttu-id="d836b-147">Questo esempio crea un firewall collegato alla rete virtuale "VNET" nello stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="d836b-147">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="d836b-148">Le regole e le minacce di intelligence che verranno applicate al firewall verranno ricavate dal criterio firewall</span><span class="sxs-lookup"><span data-stu-id="d836b-148">The rules and threat intelligence that will be applied to the firewall will be taken from the firewall policy</span></span>

## <span data-ttu-id="d836b-149">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d836b-149">PARAMETERS</span></span>

### <span data-ttu-id="d836b-150">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d836b-150">-ApplicationRuleCollection</span></span>
<span data-ttu-id="d836b-151">Specifica le raccolte di regole dell'applicazione per il nuovo firewall.</span><span class="sxs-lookup"><span data-stu-id="d836b-151">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="d836b-152">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d836b-152">-AsJob</span></span>
<span data-ttu-id="d836b-153">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d836b-153">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d836b-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d836b-154">-DefaultProfile</span></span>
<span data-ttu-id="d836b-155">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d836b-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d836b-156">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="d836b-156">-FirewallPolicyId</span></span>
<span data-ttu-id="d836b-157">Criteri firewall allegati al firewall</span><span class="sxs-lookup"><span data-stu-id="d836b-157">The firewall policy attached to the firewall</span></span>

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

### <span data-ttu-id="d836b-158">-Force</span><span class="sxs-lookup"><span data-stu-id="d836b-158">-Force</span></span>
<span data-ttu-id="d836b-159">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d836b-159">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d836b-160">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d836b-160">-Location</span></span>
<span data-ttu-id="d836b-161">Specifica l'area geografica per il firewall.</span><span class="sxs-lookup"><span data-stu-id="d836b-161">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="d836b-162">-ManagementPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d836b-162">-ManagementPublicIpAddress</span></span>
<span data-ttu-id="d836b-163">Uno o più indirizzi IP pubblici da usare per il traffico di gestione.</span><span class="sxs-lookup"><span data-stu-id="d836b-163">One or more Public IP Addresses to use for management traffic.</span></span> <span data-ttu-id="d836b-164">Gli indirizzi IP pubblici devono usare SKU standard e devono appartenere allo stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="d836b-164">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="d836b-165">-Nome</span><span class="sxs-lookup"><span data-stu-id="d836b-165">-Name</span></span>
<span data-ttu-id="d836b-166">Specifica il nome del firewall di Azure creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d836b-166">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="d836b-167">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d836b-167">-NatRuleCollection</span></span>
<span data-ttu-id="d836b-168">Elenco di AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="d836b-168">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="d836b-169">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d836b-169">-NetworkRuleCollection</span></span>
<span data-ttu-id="d836b-170">Elenco di AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="d836b-170">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="d836b-171">-PrivateRange</span><span class="sxs-lookup"><span data-stu-id="d836b-171">-PrivateRange</span></span>
<span data-ttu-id="d836b-172">Gli intervalli IP privati a cui il traffico non verrà SNAT'ed</span><span class="sxs-lookup"><span data-stu-id="d836b-172">The private IP ranges to which traffic won't be SNAT'ed</span></span>

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

### <span data-ttu-id="d836b-173">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d836b-173">-PublicIpAddress</span></span>
<span data-ttu-id="d836b-174">Uno o più indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="d836b-174">One or more Public IP Addresses.</span></span> <span data-ttu-id="d836b-175">Gli indirizzi IP pubblici devono usare SKU standard e devono appartenere allo stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="d836b-175">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="d836b-176">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="d836b-176">-PublicIpName</span></span>
<span data-ttu-id="d836b-177">Nome IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="d836b-177">Public Ip Name.</span></span> <span data-ttu-id="d836b-178">L'IP pubblico deve usare SKU standard e deve appartenere allo stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="d836b-178">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="d836b-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d836b-179">-ResourceGroupName</span></span>
<span data-ttu-id="d836b-180">Specifica il nome di un gruppo di risorse che contiene il firewall.</span><span class="sxs-lookup"><span data-stu-id="d836b-180">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="d836b-181">-SKU</span><span class="sxs-lookup"><span data-stu-id="d836b-181">-Sku</span></span>
<span data-ttu-id="d836b-182">Tipo di SKU per il firewall</span><span class="sxs-lookup"><span data-stu-id="d836b-182">The sku type for firewall</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AZFW_Hub, AZFW_VNet

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d836b-183">-Tag</span><span class="sxs-lookup"><span data-stu-id="d836b-183">-Tag</span></span>
<span data-ttu-id="d836b-184">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d836b-184">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d836b-185">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="d836b-185">For example:</span></span>

<span data-ttu-id="d836b-186">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d836b-186">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d836b-187">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="d836b-187">-ThreatIntelMode</span></span>
<span data-ttu-id="d836b-188">Specifica la modalità operativa per Threat Intelligence.</span><span class="sxs-lookup"><span data-stu-id="d836b-188">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="d836b-189">La modalità predefinita è Alert, non disattivata.</span><span class="sxs-lookup"><span data-stu-id="d836b-189">Default mode is Alert, not Off.</span></span>

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

### <span data-ttu-id="d836b-190">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="d836b-190">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="d836b-191">Whitelist per Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="d836b-191">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="d836b-192">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="d836b-192">-VirtualHubId</span></span>
<span data-ttu-id="d836b-193">Hub virtuale a cui è associato un firewall</span><span class="sxs-lookup"><span data-stu-id="d836b-193">The virtual hub that a firewall is attached to</span></span>

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

### <span data-ttu-id="d836b-194">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d836b-194">-VirtualNetwork</span></span>
<span data-ttu-id="d836b-195">Rete virtuale</span><span class="sxs-lookup"><span data-stu-id="d836b-195">Virtual Network</span></span>

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

### <span data-ttu-id="d836b-196">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d836b-196">-VirtualNetworkName</span></span>
<span data-ttu-id="d836b-197">Specifica il nome della rete virtuale per cui verrà distribuito il firewall.</span><span class="sxs-lookup"><span data-stu-id="d836b-197">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="d836b-198">La rete virtuale e il firewall devono appartenere allo stesso gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d836b-198">Virtual network and Firewall must belong to the same resource group.</span></span>

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

### <span data-ttu-id="d836b-199">-Zona</span><span class="sxs-lookup"><span data-stu-id="d836b-199">-Zone</span></span>
<span data-ttu-id="d836b-200">Elenco delle aree di disponibilità che denotano da dove deve provenire il firewall.</span><span class="sxs-lookup"><span data-stu-id="d836b-200">A list of availability zones denoting where the firewall needs to come from.</span></span>

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

### <span data-ttu-id="d836b-201">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d836b-201">-Confirm</span></span>
<span data-ttu-id="d836b-202">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d836b-202">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d836b-203">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d836b-203">-WhatIf</span></span>
<span data-ttu-id="d836b-204">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d836b-204">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d836b-205">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d836b-205">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d836b-206">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d836b-206">CommonParameters</span></span>
<span data-ttu-id="d836b-207">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d836b-207">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d836b-208">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d836b-208">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d836b-209">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d836b-209">INPUTS</span></span>

### <span data-ttu-id="d836b-210">System. String</span><span class="sxs-lookup"><span data-stu-id="d836b-210">System.String</span></span>

### <span data-ttu-id="d836b-211">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d836b-211">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="d836b-212">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress []</span><span class="sxs-lookup"><span data-stu-id="d836b-212">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="d836b-213">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d836b-213">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="d836b-214">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="d836b-214">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="d836b-215">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="d836b-215">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="d836b-216">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="d836b-216">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="d836b-217">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d836b-217">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d836b-218">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d836b-218">OUTPUTS</span></span>

### <span data-ttu-id="d836b-219">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="d836b-219">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="d836b-220">Note</span><span class="sxs-lookup"><span data-stu-id="d836b-220">NOTES</span></span>

## <span data-ttu-id="d836b-221">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d836b-221">RELATED LINKS</span></span>

[<span data-ttu-id="d836b-222">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d836b-222">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="d836b-223">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d836b-223">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="d836b-224">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d836b-224">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="d836b-225">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d836b-225">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="d836b-226">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d836b-226">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="d836b-227">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="d836b-227">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
