---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 9ef4d8f2638fdb853fa83b896bb51f95d1ef119e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326981"
---
# <span data-ttu-id="c5552-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c5552-101">Set-AzFirewall</span></span>

## <span data-ttu-id="c5552-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c5552-102">SYNOPSIS</span></span>
<span data-ttu-id="c5552-103">Salva un firewall modificato.</span><span class="sxs-lookup"><span data-stu-id="c5552-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="c5552-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5552-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5552-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5552-105">DESCRIPTION</span></span>
<span data-ttu-id="c5552-106">Il cmdlet **set-AzFirewall** aggiorna un firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="c5552-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="c5552-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5552-107">EXAMPLES</span></span>

### <span data-ttu-id="c5552-108">1: priorità di aggiornamento di una raccolta di regole applicazione firewall</span><span class="sxs-lookup"><span data-stu-id="c5552-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="c5552-109">Questo esempio aggiorna la priorità di una raccolta di regole esistente di un firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="c5552-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="c5552-110">Supponendo che il firewall di Azure "AzureFirewall" nel gruppo di risorse "RG" contenga una raccolta di regole dell'applicazione denominata "ruleCollectionName", i comandi descritti sopra cambieranno la priorità della raccolta di regole e aggiorneranno il firewall di Azure in seguito.</span><span class="sxs-lookup"><span data-stu-id="c5552-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="c5552-111">Senza il comando Set-AzFirewall, tutte le operazioni eseguite sull'oggetto $azFw locale non vengono riflesse nel server.</span><span class="sxs-lookup"><span data-stu-id="c5552-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="c5552-112">2: creare un firewall di Azure e impostare una raccolta regole applicazione in un secondo momento</span><span class="sxs-lookup"><span data-stu-id="c5552-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="c5552-113">In questo esempio, un firewall viene creato per primo senza insiemi di regole applicative.</span><span class="sxs-lookup"><span data-stu-id="c5552-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="c5552-114">In seguito vengono create una regola dell'applicazione e una raccolta regole applicazione, quindi l'oggetto firewall viene modificato in memoria, senza influire sulla configurazione reale nel cloud.</span><span class="sxs-lookup"><span data-stu-id="c5552-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="c5552-115">Per il riflesso delle modifiche nel cloud, Set-AzFirewall deve essere chiamato.</span><span class="sxs-lookup"><span data-stu-id="c5552-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="c5552-116">3: aggiornare la modalità di funzionamento di Intel Threat di Azure firewall</span><span class="sxs-lookup"><span data-stu-id="c5552-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="c5552-117">Questo esempio aggiorna la modalità di funzionamento della minaccia Intel di Azure firewall "AzureFirewall" nel gruppo di risorse "RG".</span><span class="sxs-lookup"><span data-stu-id="c5552-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="c5552-118">Senza il comando Set-AzFirewall, tutte le operazioni eseguite sull'oggetto $azFw locale non vengono riflesse nel server.</span><span class="sxs-lookup"><span data-stu-id="c5552-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="c5552-119">4: deallocare e allocare il firewall</span><span class="sxs-lookup"><span data-stu-id="c5552-119">4: Deallocate and allocate the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="c5552-120">Questo esempio recupera un firewall, rilascia il firewall e lo salva.</span><span class="sxs-lookup"><span data-stu-id="c5552-120">This example retrieves a Firewall, deallocates the firewall, and saves it.</span></span> <span data-ttu-id="c5552-121">Il comando deallocate rimuove il servizio in corso mantenendo la configurazione del firewall.</span><span class="sxs-lookup"><span data-stu-id="c5552-121">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="c5552-122">Per il riflesso delle modifiche nel cloud, Set-AzFirewall deve essere chiamato.</span><span class="sxs-lookup"><span data-stu-id="c5552-122">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>
<span data-ttu-id="c5552-123">Se l'utente vuole riavviare il servizio, il metodo allocate deve essere chiamato sul firewall.</span><span class="sxs-lookup"><span data-stu-id="c5552-123">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="c5552-124">Il nuovo VNet e l'IP pubblico devono essere nello stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="c5552-124">The new VNet and Public IP must be in the same resource group as the Firewall.</span></span> <span data-ttu-id="c5552-125">Anche in questo caso, per le modifiche da rispecchiare nel cloud, Set-AzFirewall deve essere chiamato.</span><span class="sxs-lookup"><span data-stu-id="c5552-125">Again, for changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="c5552-126">5: allocare con un indirizzo IP pubblico di gestione per gli scenari di tunneling forzato</span><span class="sxs-lookup"><span data-stu-id="c5552-126">5: Allocate with a management public IP address for forced tunneling scenarios</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="c5552-127">In questo esempio viene allocato il firewall con un indirizzo IP pubblico di gestione e una subnet per scenari di tunneling forzati.</span><span class="sxs-lookup"><span data-stu-id="c5552-127">This example allocates the firewall with a management public IP address and subnet for forced tunneling scenarios.</span></span> <span data-ttu-id="c5552-128">VNet deve contenere una subnet denominata "AzureFirewallManagementSubnet".</span><span class="sxs-lookup"><span data-stu-id="c5552-128">The VNet must contain a subnet called "AzureFirewallManagementSubnet".</span></span>

### <span data-ttu-id="c5552-129">6: aggiungere un indirizzo IP pubblico a un firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="c5552-129">6:  Add a Public IP address to an Azure Firewall</span></span>
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="c5552-130">In questo esempio l'indirizzo IP pubblico "azFwPublicIp1" come allegato al firewall.</span><span class="sxs-lookup"><span data-stu-id="c5552-130">In this example, the Public IP Address "azFwPublicIp1" as attached to the Firewall.</span></span>

### <span data-ttu-id="c5552-131">7: rimuovere un indirizzo IP pubblico da un firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="c5552-131">7:  Remove a Public IP address from an Azure Firewall</span></span>
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="c5552-132">In questo esempio l'indirizzo IP pubblico "azFwPublicIp1" è disconnesso dal firewall.</span><span class="sxs-lookup"><span data-stu-id="c5552-132">In this example, the Public IP Address "azFwPublicIp1" as detached from the Firewall.</span></span>

### <span data-ttu-id="c5552-133">8: modificare l'indirizzo IP pubblico di gestione in un firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="c5552-133">8:  Change the management public IP address on an Azure Firewall</span></span>
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

<span data-ttu-id="c5552-134">In questo esempio l'indirizzo IP pubblico di gestione del firewall verrà modificato in "AzFwMgmtPublicIp2"</span><span class="sxs-lookup"><span data-stu-id="c5552-134">In this example, the management public IP address of the firewall will be changed to "AzFwMgmtPublicIp2"</span></span>

### <span data-ttu-id="c5552-135">9: aggiungere la configurazione DNS a un firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="c5552-135">9:  Add DNS configuration to an Azure Firewall</span></span>
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

<span data-ttu-id="c5552-136">In questo esempio, il proxy DNS e la configurazione del server DNS sono allegati al firewall.</span><span class="sxs-lookup"><span data-stu-id="c5552-136">In this example, DNS Proxy and DNS Server configuration is attached to the Firewall.</span></span>

### <span data-ttu-id="c5552-137">10: aggiornare la destinazione di una regola esistente all'interno di una raccolta di regole applicazione firewall</span><span class="sxs-lookup"><span data-stu-id="c5552-137">10: Update destination of an existing rule within a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses="10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="c5552-138">Questo esempio aggiorna la destinazione di una regola esistente all'interno di una raccolta di regole di un firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="c5552-138">This example updates the destination of an existing rule within a rule collection of an Azure Firewall.</span></span> <span data-ttu-id="c5552-139">In questo modo è possibile aggiornare automaticamente le regole quando gli indirizzi IP cambiano dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="c5552-139">This allows you to automatically update your rules when IP addresses change dynamically.</span></span>

### <span data-ttu-id="c5552-140">11: consentire l'FTP attivo in Azure firewall</span><span class="sxs-lookup"><span data-stu-id="c5552-140">11: Allow Active FTP on Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

<span data-ttu-id="c5552-141">In questo esempio, il protocollo FTP attivo è consentito nel firewall.</span><span class="sxs-lookup"><span data-stu-id="c5552-141">In this example, Active FTP is allowed on the Firewall.</span></span>

## <span data-ttu-id="c5552-142">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c5552-142">PARAMETERS</span></span>

### <span data-ttu-id="c5552-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5552-143">-AsJob</span></span>
<span data-ttu-id="c5552-144">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c5552-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c5552-145">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="c5552-145">-AzureFirewall</span></span>
<span data-ttu-id="c5552-146">AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="c5552-146">The AzureFirewall</span></span>

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

### <span data-ttu-id="c5552-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5552-147">-DefaultProfile</span></span>
<span data-ttu-id="c5552-148">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c5552-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5552-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c5552-149">-Confirm</span></span>
<span data-ttu-id="c5552-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5552-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5552-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5552-151">-WhatIf</span></span>
<span data-ttu-id="c5552-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5552-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c5552-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5552-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5552-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5552-154">CommonParameters</span></span>
<span data-ttu-id="c5552-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5552-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5552-156">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5552-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5552-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c5552-157">INPUTS</span></span>

### <span data-ttu-id="c5552-158">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="c5552-158">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="c5552-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5552-159">OUTPUTS</span></span>

### <span data-ttu-id="c5552-160">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="c5552-160">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="c5552-161">Note</span><span class="sxs-lookup"><span data-stu-id="c5552-161">NOTES</span></span>

## <span data-ttu-id="c5552-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5552-162">RELATED LINKS</span></span>

[<span data-ttu-id="c5552-163">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c5552-163">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="c5552-164">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c5552-164">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="c5552-165">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="c5552-165">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
