---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 1ab3d82b494d5598081ea229a7ae50d486b8ca20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189519"
---
# <span data-ttu-id="70c83-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="70c83-101">Set-AzFirewall</span></span>

## <span data-ttu-id="70c83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70c83-102">SYNOPSIS</span></span>
<span data-ttu-id="70c83-103">Salva un firewall modificato.</span><span class="sxs-lookup"><span data-stu-id="70c83-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="70c83-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="70c83-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70c83-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="70c83-105">DESCRIPTION</span></span>
<span data-ttu-id="70c83-106">Il cmdlet **Set-AzFirewall** aggiorna un firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="70c83-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="70c83-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="70c83-107">EXAMPLES</span></span>

### <span data-ttu-id="70c83-108">1: priorità di aggiornamento di una raccolta di regole dell'applicazione firewall</span><span class="sxs-lookup"><span data-stu-id="70c83-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="70c83-109">Questo esempio aggiorna la priorità di una raccolta di regole esistente di un firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="70c83-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="70c83-110">Presupponendo che "AzureFirewall" del firewall azure nel gruppo di risorse "rg" contenga una raccolta di regole dell'applicazione denominata "ruleCollectionName", i comandi precedenti cambieranno la priorità di quella raccolta di regole e aggiorneranno il firewall di Azure in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="70c83-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="70c83-111">Senza il Set-AzFirewall comando, tutte le operazioni eseguite sull'oggetto $azFw locale non si riflettono sul server.</span><span class="sxs-lookup"><span data-stu-id="70c83-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="70c83-112">2: Creare un firewall di Azure e impostare una raccolta di regole dell'applicazione in un secondo momento</span><span class="sxs-lookup"><span data-stu-id="70c83-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="70c83-113">In questo esempio viene creato prima un firewall senza raccolte di regole dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="70c83-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="70c83-114">Al termine della creazione di una regola dell'applicazione e di una raccolta di regole dell'applicazione, l'oggetto Firewall viene modificato in memoria, senza influire sulla configurazione reale nel cloud.</span><span class="sxs-lookup"><span data-stu-id="70c83-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="70c83-115">Perché le modifiche si riflettano nel cloud, Set-AzFirewall essere chiamato.</span><span class="sxs-lookup"><span data-stu-id="70c83-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="70c83-116">3: Aggiornare la modalità di funzionamento di Threat Intel di Azure Firewall</span><span class="sxs-lookup"><span data-stu-id="70c83-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="70c83-117">Questo esempio aggiorna la modalità di operazione Threat Intel di Azure Firewall "AzureFirewall" nel gruppo di risorse "rg".</span><span class="sxs-lookup"><span data-stu-id="70c83-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="70c83-118">Senza il Set-AzFirewall comando, tutte le operazioni eseguite sull'oggetto $azFw locale non si riflettono sul server.</span><span class="sxs-lookup"><span data-stu-id="70c83-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="70c83-119">4: Deassegnare e allocare il firewall</span><span class="sxs-lookup"><span data-stu-id="70c83-119">4: Deallocate and allocate the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="70c83-120">Questo esempio recupera un firewall, deassegna il firewall e lo salva.</span><span class="sxs-lookup"><span data-stu-id="70c83-120">This example retrieves a Firewall, deallocates the firewall, and saves it.</span></span> <span data-ttu-id="70c83-121">Il comando Deassegna rimuove il servizio in esecuzione, mantenendo però la configurazione del firewall.</span><span class="sxs-lookup"><span data-stu-id="70c83-121">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="70c83-122">Perché le modifiche si riflettano nel cloud, Set-AzFirewall essere chiamato.</span><span class="sxs-lookup"><span data-stu-id="70c83-122">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>
<span data-ttu-id="70c83-123">Se l'utente vuole avviare di nuovo il servizio, il metodo Allocate deve essere chiamato nel firewall.</span><span class="sxs-lookup"><span data-stu-id="70c83-123">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="70c83-124">La nuova rete virtuale e l'INDIRIZZO IP pubblico devono essere nello stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="70c83-124">The new VNet and Public IP must be in the same resource group as the Firewall.</span></span> <span data-ttu-id="70c83-125">Anche in questo caso, per riflettere le modifiche nel cloud, Set-AzFirewall essere chiamato.</span><span class="sxs-lookup"><span data-stu-id="70c83-125">Again, for changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="70c83-126">5: Eseguire l'assegnazione con un indirizzo IP pubblico di gestione per scenari di tunneling forzato</span><span class="sxs-lookup"><span data-stu-id="70c83-126">5: Allocate with a management public IP address for forced tunneling scenarios</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="70c83-127">Questo esempio alloca il firewall con un indirizzo IP pubblico di gestione e una subnet per scenari di tunneling forzato.</span><span class="sxs-lookup"><span data-stu-id="70c83-127">This example allocates the firewall with a management public IP address and subnet for forced tunneling scenarios.</span></span> <span data-ttu-id="70c83-128">La rete VNet deve contenere una subnet denominata "AzureFirewallManagementSubnet".</span><span class="sxs-lookup"><span data-stu-id="70c83-128">The VNet must contain a subnet called "AzureFirewallManagementSubnet".</span></span>

### <span data-ttu-id="70c83-129">6: Aggiungere un indirizzo IP pubblico a un firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="70c83-129">6:  Add a Public IP address to an Azure Firewall</span></span>
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="70c83-130">In questo esempio l'indirizzo IP pubblico "azFwPublicIp1" associato al firewall.</span><span class="sxs-lookup"><span data-stu-id="70c83-130">In this example, the Public IP Address "azFwPublicIp1" as attached to the Firewall.</span></span>

### <span data-ttu-id="70c83-131">7: Rimuovere un indirizzo IP pubblico da un firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="70c83-131">7:  Remove a Public IP address from an Azure Firewall</span></span>
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="70c83-132">In questo esempio l'indirizzo IP pubblico "azFwPublicIp1" è scollegato dal firewall.</span><span class="sxs-lookup"><span data-stu-id="70c83-132">In this example, the Public IP Address "azFwPublicIp1" as detached from the Firewall.</span></span>

### <span data-ttu-id="70c83-133">8: Modificare l'indirizzo IP pubblico di gestione in un firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="70c83-133">8:  Change the management public IP address on an Azure Firewall</span></span>
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

<span data-ttu-id="70c83-134">In questo esempio l'indirizzo IP pubblico di gestione del firewall verrà modificato in "AzFwMgmtPublicIp2"</span><span class="sxs-lookup"><span data-stu-id="70c83-134">In this example, the management public IP address of the firewall will be changed to "AzFwMgmtPublicIp2"</span></span>

### <span data-ttu-id="70c83-135">9: Aggiungere la configurazione DNS a un firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="70c83-135">9:  Add DNS configuration to an Azure Firewall</span></span>
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

<span data-ttu-id="70c83-136">In questo esempio, la configurazione del server DNS e del proxy DNS è collegata al firewall.</span><span class="sxs-lookup"><span data-stu-id="70c83-136">In this example, DNS Proxy and DNS Server configuration is attached to the Firewall.</span></span>

### <span data-ttu-id="70c83-137">10: aggiornare la destinazione di una regola esistente in una raccolta di regole dell'applicazione firewall</span><span class="sxs-lookup"><span data-stu-id="70c83-137">10: Update destination of an existing rule within a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses = "10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="70c83-138">Questo esempio aggiorna la destinazione di una regola esistente in una raccolta di regole di un firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="70c83-138">This example updates the destination of an existing rule within a rule collection of an Azure Firewall.</span></span> <span data-ttu-id="70c83-139">In questo modo è possibile aggiornare automaticamente le regole quando gli indirizzi IP cambiano dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="70c83-139">This allows you to automatically update your rules when IP addresses change dynamically.</span></span>

### <span data-ttu-id="70c83-140">11: Consenti FTP attivo nel firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="70c83-140">11: Allow Active FTP on Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

<span data-ttu-id="70c83-141">In questo esempio, FTP attivo è consentito nel firewall.</span><span class="sxs-lookup"><span data-stu-id="70c83-141">In this example, Active FTP is allowed on the Firewall.</span></span>

## <span data-ttu-id="70c83-142">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70c83-142">PARAMETERS</span></span>

### <span data-ttu-id="70c83-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70c83-143">-AsJob</span></span>
<span data-ttu-id="70c83-144">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="70c83-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70c83-145">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="70c83-145">-AzureFirewall</span></span>
<span data-ttu-id="70c83-146">The AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="70c83-146">The AzureFirewall</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70c83-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70c83-147">-DefaultProfile</span></span>
<span data-ttu-id="70c83-148">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="70c83-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70c83-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70c83-149">-Confirm</span></span>
<span data-ttu-id="70c83-150">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70c83-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c83-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70c83-151">-WhatIf</span></span>
<span data-ttu-id="70c83-152">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70c83-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70c83-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="70c83-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c83-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70c83-154">CommonParameters</span></span>
<span data-ttu-id="70c83-155">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70c83-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70c83-156">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70c83-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70c83-157">INPUT</span><span class="sxs-lookup"><span data-stu-id="70c83-157">INPUTS</span></span>

### <span data-ttu-id="70c83-158">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="70c83-158">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="70c83-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="70c83-159">OUTPUTS</span></span>

### <span data-ttu-id="70c83-160">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="70c83-160">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="70c83-161">NOTE</span><span class="sxs-lookup"><span data-stu-id="70c83-161">NOTES</span></span>

## <span data-ttu-id="70c83-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="70c83-162">RELATED LINKS</span></span>

[<span data-ttu-id="70c83-163">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="70c83-163">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="70c83-164">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="70c83-164">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="70c83-165">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="70c83-165">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
