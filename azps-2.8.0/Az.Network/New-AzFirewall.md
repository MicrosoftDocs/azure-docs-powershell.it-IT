---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 8d8d3ce0a236acb511eac715385b53c821f1dceb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852986"
---
# <span data-ttu-id="07843-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="07843-101">New-AzFirewall</span></span>

## <span data-ttu-id="07843-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07843-102">SYNOPSIS</span></span>
<span data-ttu-id="07843-103">Crea un nuovo firewall in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="07843-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="07843-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07843-104">SYNTAX</span></span>

### <span data-ttu-id="07843-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="07843-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Zone <String[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07843-106">OldIpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="07843-106">OldIpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Zone <String[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07843-107">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="07843-107">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetwork <PSVirtualNetwork>
 -PublicIpAddress <PSPublicIpAddress[]>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-ThreatIntelMode <String>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07843-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07843-108">DESCRIPTION</span></span>
<span data-ttu-id="07843-109">Il cmdlet **New-AzFirewall** crea un firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="07843-109">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="07843-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07843-110">EXAMPLES</span></span>

### <span data-ttu-id="07843-111">1: creare un firewall collegato a una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="07843-111">1:  Create a Firewall attached to a virtual network</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip
```

<span data-ttu-id="07843-112">Questo esempio crea un firewall collegato alla rete virtuale "VNET" nello stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="07843-112">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="07843-113">Dato che non sono state specificate regole, il firewall bloccherà tutto il traffico (comportamento predefinito).</span><span class="sxs-lookup"><span data-stu-id="07843-113">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="07843-114">Le minacce Intel verranno eseguite anche in modalità predefinita-avviso-il che significa che il traffico illecito verrà registrato, ma non negato.</span><span class="sxs-lookup"><span data-stu-id="07843-114">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="07843-115">2: creare un firewall che consente tutto il traffico HTTPS</span><span class="sxs-lookup"><span data-stu-id="07843-115">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="07843-116">Questo esempio crea un firewall che consente tutto il traffico HTTPS sulla porta 443.</span><span class="sxs-lookup"><span data-stu-id="07843-116">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="07843-117">Threat Intel verrà eseguito in modalità predefinita-avviso-il che significa che il traffico illecito verrà registrato, ma non negato.</span><span class="sxs-lookup"><span data-stu-id="07843-117">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="07843-118">3: DNAT-reindirizza il traffico destinato a 10.1.2.3:80 a 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="07843-118">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="07843-119">Questo esempio ha creato un firewall che ha tradotto l'indirizzo IP di destinazione e la porta di tutti i pacchetti destinati a 10.1.2.3:80 a 10.2.3.4:8080 Threat Intel è disattivata in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="07843-119">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="07843-120">4: creare un firewall senza regole e con le minacce Intel in modalità avviso</span><span class="sxs-lookup"><span data-stu-id="07843-120">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ThreatIntelMode Alert
```

<span data-ttu-id="07843-121">Questo esempio crea un firewall che blocca tutto il traffico (comportamento predefinito) ed è in uso in modalità avviso.</span><span class="sxs-lookup"><span data-stu-id="07843-121">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="07843-122">Questo significa che i registri di avviso vengono emessi per il traffico illecito prima di applicare le altre regole (in questo caso solo la regola predefinita-Deny All)</span><span class="sxs-lookup"><span data-stu-id="07843-122">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="07843-123">5: creare un firewall che consente tutto il traffico HTTP sulla porta 8080, ma blocca i domini malevoli identificati da Intel Threat</span><span class="sxs-lookup"><span data-stu-id="07843-123">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="07843-124">Questo esempio crea un firewall che consente tutto il traffico HTTP sulla porta 8080, a meno che non sia considerato dannoso da Intel Threat.</span><span class="sxs-lookup"><span data-stu-id="07843-124">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="07843-125">Quando l'utente viene eseguito in modalità di negazione, diversamente da Alert, il traffico considerato malevolo da Intel Threat non è solo registrato, ma anche bloccato.</span><span class="sxs-lookup"><span data-stu-id="07843-125">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

### <span data-ttu-id="07843-126">6: creare un firewall senza regole e con le aree di disponibilità</span><span class="sxs-lookup"><span data-stu-id="07843-126">6:  Create a Firewall with no rules and with availability zones</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetworkName $vnet.Name -PublicIpName $pip.Name -Zone 1,2,3
```

<span data-ttu-id="07843-127">Questo esempio crea un firewall con tutte le aree di disponibilità disponibili.</span><span class="sxs-lookup"><span data-stu-id="07843-127">This example creates a Firewall with all available availability zones.</span></span>

### <span data-ttu-id="07843-128">7: creare un firewall con due o più indirizzi IP pubblici</span><span class="sxs-lookup"><span data-stu-id="07843-128">7: Create a Firewall with two or more Public IP Addresses</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -Name "vnet" -ResourceGroupName $rgName
$pip1 = New-AzPublicIpAddress -Name "AzFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$pip2 = New-AzPublicIpAddress -Name "AzFwPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress @($pip1, $pip2)
```

<span data-ttu-id="07843-129">Questo esempio crea un firewall collegato alla rete virtuale "VNET" con due indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="07843-129">This example creates a Firewall attached to virtual network "vnet" with two public IP addresses.</span></span>

### <span data-ttu-id="07843-130">8: creare un firewall che consente il traffico di MSSQL per database SQL specifico</span><span class="sxs-lookup"><span data-stu-id="07843-130">8: Create a Firewall which allows MSSQL traffic to specific SQL database</span></span>
```
$rgName = "resourceGroupName"
$vnet = Get-AzVirtualNetwork -ResourceGroupName $rgName -Name "vnet"
$pip = Get-AzPublicIpAddress -ResourceGroupName $rgName -Name "publicIpName"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "mssql:1433" -TargetFqdn "sql1.database.windows.net"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName $rgName -Location centralus -VirtualNetwork $vnet -PublicIpAddress $pip -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="07843-131">Questo esempio crea un firewall che consente il traffico di MSSQL sulla porta standard 1433 per il database SQL sql1.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="07843-131">This example creates a Firewall which allows MSSQL traffic on standard port 1433 to SQL database sql1.database.windows.net.</span></span>

## <span data-ttu-id="07843-132">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07843-132">PARAMETERS</span></span>

### <span data-ttu-id="07843-133">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="07843-133">-ApplicationRuleCollection</span></span>
<span data-ttu-id="07843-134">Specifica le raccolte di regole dell'applicazione per il nuovo firewall.</span><span class="sxs-lookup"><span data-stu-id="07843-134">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="07843-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07843-135">-AsJob</span></span>
<span data-ttu-id="07843-136">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="07843-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07843-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07843-137">-DefaultProfile</span></span>
<span data-ttu-id="07843-138">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07843-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07843-139">-Force</span><span class="sxs-lookup"><span data-stu-id="07843-139">-Force</span></span>
<span data-ttu-id="07843-140">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="07843-140">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="07843-141">-Posizione</span><span class="sxs-lookup"><span data-stu-id="07843-141">-Location</span></span>
<span data-ttu-id="07843-142">Specifica l'area geografica per il firewall.</span><span class="sxs-lookup"><span data-stu-id="07843-142">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="07843-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="07843-143">-Name</span></span>
<span data-ttu-id="07843-144">Specifica il nome del firewall di Azure creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07843-144">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="07843-145">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="07843-145">-NatRuleCollection</span></span>
<span data-ttu-id="07843-146">Elenco di AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="07843-146">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="07843-147">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="07843-147">-NetworkRuleCollection</span></span>
<span data-ttu-id="07843-148">Elenco di AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="07843-148">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="07843-149">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="07843-149">-PublicIpAddress</span></span>
<span data-ttu-id="07843-150">Uno o più indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="07843-150">One or more Public IP Addresses.</span></span> <span data-ttu-id="07843-151">Gli indirizzi IP pubblici devono usare SKU standard e devono appartenere allo stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="07843-151">The Public IP addresses must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="07843-152">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="07843-152">-PublicIpName</span></span>
<span data-ttu-id="07843-153">Nome IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="07843-153">Public Ip Name.</span></span> <span data-ttu-id="07843-154">L'IP pubblico deve usare SKU standard e deve appartenere allo stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="07843-154">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

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

### <span data-ttu-id="07843-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07843-155">-ResourceGroupName</span></span>
<span data-ttu-id="07843-156">Specifica il nome di un gruppo di risorse che contiene il firewall.</span><span class="sxs-lookup"><span data-stu-id="07843-156">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="07843-157">-Zona</span><span class="sxs-lookup"><span data-stu-id="07843-157">-Zone</span></span>
<span data-ttu-id="07843-158">Elenco delle aree di disponibilità che denotano da dove deve provenire il firewall.</span><span class="sxs-lookup"><span data-stu-id="07843-158">A list of availability zones denoting where the firewall needs to come from.</span></span>

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

### <span data-ttu-id="07843-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="07843-159">-Tag</span></span>
<span data-ttu-id="07843-160">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="07843-160">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="07843-161">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="07843-161">For example:</span></span>

<span data-ttu-id="07843-162">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="07843-162">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="07843-163">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="07843-163">-ThreatIntelMode</span></span>
<span data-ttu-id="07843-164">Specifica la modalità operativa per Threat Intelligence.</span><span class="sxs-lookup"><span data-stu-id="07843-164">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="07843-165">La modalità predefinita è Alert, non disattivata.</span><span class="sxs-lookup"><span data-stu-id="07843-165">Default mode is Alert, not Off.</span></span>

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

### <span data-ttu-id="07843-166">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="07843-166">-VirtualNetwork</span></span>
<span data-ttu-id="07843-167">Rete virtuale</span><span class="sxs-lookup"><span data-stu-id="07843-167">Virtual Network</span></span>

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

### <span data-ttu-id="07843-168">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="07843-168">-VirtualNetworkName</span></span>
<span data-ttu-id="07843-169">Specifica il nome della rete virtuale per cui verrà distribuito il firewall.</span><span class="sxs-lookup"><span data-stu-id="07843-169">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="07843-170">La rete virtuale e il firewall devono appartenere allo stesso gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="07843-170">Virtual network and Firewall must belong to the same resource group.</span></span>

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

### <span data-ttu-id="07843-171">-Confermare</span><span class="sxs-lookup"><span data-stu-id="07843-171">-Confirm</span></span>
<span data-ttu-id="07843-172">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07843-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07843-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07843-173">-WhatIf</span></span>
<span data-ttu-id="07843-174">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07843-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07843-175">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07843-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07843-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07843-176">CommonParameters</span></span>
<span data-ttu-id="07843-177">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07843-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07843-178">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07843-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07843-179">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07843-179">INPUTS</span></span>

### <span data-ttu-id="07843-180">System. String</span><span class="sxs-lookup"><span data-stu-id="07843-180">System.String</span></span>

### <span data-ttu-id="07843-181">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="07843-181">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="07843-182">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress []</span><span class="sxs-lookup"><span data-stu-id="07843-182">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress[]</span></span>

### <span data-ttu-id="07843-183">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="07843-183">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="07843-184">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="07843-184">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="07843-185">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="07843-185">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="07843-186">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="07843-186">System.Collections.Hashtable</span></span>

## <span data-ttu-id="07843-187">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07843-187">OUTPUTS</span></span>

### <span data-ttu-id="07843-188">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="07843-188">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="07843-189">Note</span><span class="sxs-lookup"><span data-stu-id="07843-189">NOTES</span></span>

## <span data-ttu-id="07843-190">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07843-190">RELATED LINKS</span></span>

[<span data-ttu-id="07843-191">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="07843-191">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="07843-192">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="07843-192">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="07843-193">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="07843-193">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="07843-194">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="07843-194">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="07843-195">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="07843-195">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="07843-196">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="07843-196">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
