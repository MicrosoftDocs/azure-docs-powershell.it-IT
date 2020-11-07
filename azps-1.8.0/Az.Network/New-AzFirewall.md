---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A3D60CF1-2E66-4EE5-9C68-932DD8DF80BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewall.md
ms.openlocfilehash: 48e8fc8685073a0fad742152191fe68c368fbb3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678303"
---
# <span data-ttu-id="1d2bc-101">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1d2bc-101">New-AzFirewall</span></span>

## <span data-ttu-id="1d2bc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1d2bc-102">SYNOPSIS</span></span>
<span data-ttu-id="1d2bc-103">Crea un nuovo firewall in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-103">Creates a new Firewall in a resource group.</span></span>

## <span data-ttu-id="1d2bc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d2bc-104">SYNTAX</span></span>

### <span data-ttu-id="1d2bc-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1d2bc-105">Default (Default)</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String>
 [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d2bc-106">IpConfigurationParameterValues</span><span class="sxs-lookup"><span data-stu-id="1d2bc-106">IpConfigurationParameterValues</span></span>
```
New-AzFirewall -Name <String> -ResourceGroupName <String> -Location <String> -VirtualNetworkName <String>
 -PublicIpName <String> [-ApplicationRuleCollection <PSAzureFirewallApplicationRuleCollection[]>]
 [-NatRuleCollection <PSAzureFirewallNatRuleCollection[]>]
 [-NetworkRuleCollection <PSAzureFirewallNetworkRuleCollection[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d2bc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d2bc-107">DESCRIPTION</span></span>
<span data-ttu-id="1d2bc-108">Il cmdlet **New-AzFirewall** crea un firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-108">The **New-AzFirewall** cmdlet creates an Azure Firewall.</span></span>

## <span data-ttu-id="1d2bc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d2bc-109">EXAMPLES</span></span>

### <span data-ttu-id="1d2bc-110">1: creare un firewall collegato a una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="1d2bc-110">1:  Create a Firewall attached to a virtual network</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name"
```

<span data-ttu-id="1d2bc-111">Questo esempio crea un firewall collegato alla rete virtuale "VNET" nello stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-111">This example creates a Firewall attached to virtual network "vnet" in the same resource group as the firewall.</span></span>
<span data-ttu-id="1d2bc-112">Dato che non sono state specificate regole, il firewall bloccherà tutto il traffico (comportamento predefinito).</span><span class="sxs-lookup"><span data-stu-id="1d2bc-112">Since no rules were specified, the firewall will block all traffic (default behavior).</span></span>
<span data-ttu-id="1d2bc-113">Le minacce Intel verranno eseguite anche in modalità predefinita-avviso-il che significa che il traffico illecito verrà registrato, ma non negato.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-113">Threat Intel will also run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="1d2bc-114">2: creare un firewall che consente tutto il traffico HTTPS</span><span class="sxs-lookup"><span data-stu-id="1d2bc-114">2:  Create a Firewall which allows all HTTPS traffic</span></span>
```
$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "https:443" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection
```

<span data-ttu-id="1d2bc-115">Questo esempio crea un firewall che consente tutto il traffico HTTPS sulla porta 443.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-115">This example creates a Firewall which allows all HTTPS traffic on port 443.</span></span>
<span data-ttu-id="1d2bc-116">Threat Intel verrà eseguito in modalità predefinita-avviso-il che significa che il traffico illecito verrà registrato, ma non negato.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-116">Threat Intel will run in default mode - Alert - which means malicious traffic will be logged, but not denied.</span></span>

### <span data-ttu-id="1d2bc-117">3: DNAT-reindirizza il traffico destinato a 10.1.2.3:80 a 10.2.3.4:8080</span><span class="sxs-lookup"><span data-stu-id="1d2bc-117">3:  DNAT - redirect traffic destined to 10.1.2.3:80 to 10.2.3.4:8080</span></span>
```
$rule = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.2.3.4" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "NatRuleCollection" -Priority 1000 -Rule $rule
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -NatRuleCollection $ruleCollection -ThreatIntelMode Off
```

<span data-ttu-id="1d2bc-118">Questo esempio ha creato un firewall che ha tradotto l'indirizzo IP di destinazione e la porta di tutti i pacchetti destinati a 10.1.2.3:80 a 10.2.3.4:8080 Threat Intel è disattivata in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-118">This example created a Firewall which translated the destination IP and port of all packets destined to 10.1.2.3:80 to 10.2.3.4:8080 Threat Intel is turned off in this example.</span></span>

### <span data-ttu-id="1d2bc-119">4: creare un firewall senza regole e con le minacce Intel in modalità avviso</span><span class="sxs-lookup"><span data-stu-id="1d2bc-119">4:  Create a Firewall with no rules and with Threat Intel in Alert mode</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ThreatIntelMode Alert
```

<span data-ttu-id="1d2bc-120">Questo esempio crea un firewall che blocca tutto il traffico (comportamento predefinito) ed è in uso in modalità avviso.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-120">This example creates a Firewall which blocks all traffic (default behavior) and has Threat Intel running in Alert mode.</span></span>
<span data-ttu-id="1d2bc-121">Questo significa che i registri di avviso vengono emessi per il traffico illecito prima di applicare le altre regole (in questo caso solo la regola predefinita-Deny All)</span><span class="sxs-lookup"><span data-stu-id="1d2bc-121">This means alerting logs are emitted for malicious traffic before applying the other rules (in this case just the default rule - Deny All)</span></span>

### <span data-ttu-id="1d2bc-122">5: creare un firewall che consente tutto il traffico HTTP sulla porta 8080, ma blocca i domini malevoli identificati da Intel Threat</span><span class="sxs-lookup"><span data-stu-id="1d2bc-122">5:  Create a Firewall which allows all HTTP traffic on port 8080, but blocks malicious domains identified by Threat Intel</span></span>
```
$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:8080" -TargetFqdn "*" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
New-AzFirewall -Name "azFw" -ResourceGroupName "rg" -Location centralus -VirtualNetworkName "vnet" -PublicIpName "pip-name" -ApplicationRuleCollection $ruleCollection -ThreatIntelMode Deny
```

<span data-ttu-id="1d2bc-123">Questo esempio crea un firewall che consente tutto il traffico HTTP sulla porta 8080, a meno che non sia considerato dannoso da Intel Threat.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-123">This example creates a Firewall which allows all HTTP traffic on port 8080 unless it is considered malicious by Threat Intel.</span></span>
<span data-ttu-id="1d2bc-124">Quando l'utente viene eseguito in modalità di negazione, diversamente da Alert, il traffico considerato malevolo da Intel Threat non è solo registrato, ma anche bloccato.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-124">When running in Deny mode, unlike Alert, traffic considered malicious by Threat Intel is not just logged, but also blocked.</span></span>

## <span data-ttu-id="1d2bc-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1d2bc-125">PARAMETERS</span></span>

### <span data-ttu-id="1d2bc-126">-ApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1d2bc-126">-ApplicationRuleCollection</span></span>
<span data-ttu-id="1d2bc-127">Specifica le raccolte di regole dell'applicazione per il nuovo firewall.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-127">Specifies the collections of application rules for the new Firewall.</span></span>

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

### <span data-ttu-id="1d2bc-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d2bc-128">-AsJob</span></span>
<span data-ttu-id="1d2bc-129">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1d2bc-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d2bc-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d2bc-130">-DefaultProfile</span></span>
<span data-ttu-id="1d2bc-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d2bc-132">-Force</span><span class="sxs-lookup"><span data-stu-id="1d2bc-132">-Force</span></span>
<span data-ttu-id="1d2bc-133">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1d2bc-134">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1d2bc-134">-Location</span></span>
<span data-ttu-id="1d2bc-135">Specifica l'area geografica per il firewall.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-135">Specifies the region for the Firewall.</span></span>

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

### <span data-ttu-id="1d2bc-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="1d2bc-136">-Name</span></span>
<span data-ttu-id="1d2bc-137">Specifica il nome del firewall di Azure creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-137">Specifies the name of the Azure Firewall that this cmdlet creates.</span></span>

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

### <span data-ttu-id="1d2bc-138">-NatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1d2bc-138">-NatRuleCollection</span></span>
<span data-ttu-id="1d2bc-139">Elenco di AzureFirewallNatRuleCollections</span><span class="sxs-lookup"><span data-stu-id="1d2bc-139">The list of AzureFirewallNatRuleCollections</span></span>

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

### <span data-ttu-id="1d2bc-140">-NetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1d2bc-140">-NetworkRuleCollection</span></span>
<span data-ttu-id="1d2bc-141">Elenco di AzureFirewallNetworkRuleCollections</span><span class="sxs-lookup"><span data-stu-id="1d2bc-141">The list of AzureFirewallNetworkRuleCollections</span></span>

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

### <span data-ttu-id="1d2bc-142">-PublicIpName</span><span class="sxs-lookup"><span data-stu-id="1d2bc-142">-PublicIpName</span></span>
<span data-ttu-id="1d2bc-143">Nome IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-143">Public Ip Name.</span></span> <span data-ttu-id="1d2bc-144">L'IP pubblico deve usare SKU standard e deve appartenere allo stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-144">The Public IP must use Standard SKU and must belong to the same resource group as the Firewall.</span></span>

```yaml
Type: System.String
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d2bc-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d2bc-145">-ResourceGroupName</span></span>
<span data-ttu-id="1d2bc-146">Specifica il nome di un gruppo di risorse che contiene il firewall.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-146">Specifies the name of a resource group to contain the Firewall.</span></span>

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

### <span data-ttu-id="1d2bc-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="1d2bc-147">-Tag</span></span>
<span data-ttu-id="1d2bc-148">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1d2bc-149">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="1d2bc-149">For example:</span></span>

<span data-ttu-id="1d2bc-150">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="1d2bc-150">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1d2bc-151">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="1d2bc-151">-ThreatIntelMode</span></span>
<span data-ttu-id="1d2bc-152">Specifica la modalità operativa per Threat Intelligence.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-152">Specifies the operation mode for Threat Intelligence.</span></span> <span data-ttu-id="1d2bc-153">La modalità predefinita è Alert, non disattivata.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-153">Default mode is Alert, not Off.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Alert
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d2bc-154">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="1d2bc-154">-VirtualNetworkName</span></span>
<span data-ttu-id="1d2bc-155">Specifica il nome della rete virtuale per cui verrà distribuito il firewall.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-155">Specifies the name of the virtual network for which the Firewall will be deployed.</span></span> <span data-ttu-id="1d2bc-156">La rete virtuale e il firewall devono appartenere allo stesso gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-156">Virtual network and Firewall must belong to the same resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: IpConfigurationParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d2bc-157">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1d2bc-157">-Confirm</span></span>
<span data-ttu-id="1d2bc-158">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d2bc-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d2bc-159">-WhatIf</span></span>
<span data-ttu-id="1d2bc-160">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d2bc-161">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d2bc-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d2bc-162">CommonParameters</span></span>
<span data-ttu-id="1d2bc-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d2bc-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d2bc-164">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d2bc-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d2bc-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1d2bc-165">INPUTS</span></span>

### <span data-ttu-id="1d2bc-166">System. String</span><span class="sxs-lookup"><span data-stu-id="1d2bc-166">System.String</span></span>

### <span data-ttu-id="1d2bc-167">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallApplicationRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="1d2bc-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection[]</span></span>

### <span data-ttu-id="1d2bc-168">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNatRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="1d2bc-168">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection[]</span></span>

### <span data-ttu-id="1d2bc-169">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRuleCollection []</span><span class="sxs-lookup"><span data-stu-id="1d2bc-169">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection[]</span></span>

### <span data-ttu-id="1d2bc-170">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1d2bc-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1d2bc-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d2bc-171">OUTPUTS</span></span>

### <span data-ttu-id="1d2bc-172">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="1d2bc-172">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="1d2bc-173">Note</span><span class="sxs-lookup"><span data-stu-id="1d2bc-173">NOTES</span></span>

## <span data-ttu-id="1d2bc-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d2bc-174">RELATED LINKS</span></span>

[<span data-ttu-id="1d2bc-175">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1d2bc-175">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="1d2bc-176">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1d2bc-176">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)

[<span data-ttu-id="1d2bc-177">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="1d2bc-177">Set-AzFirewall</span></span>](./Set-AzFirewall.md)

[<span data-ttu-id="1d2bc-178">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1d2bc-178">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="1d2bc-179">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1d2bc-179">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="1d2bc-180">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1d2bc-180">New-AzFirewallNetworkRuleCollection</span></span>](./New-AzFirewallNetworkRuleCollection.md)
