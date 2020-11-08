---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 36ba29104fbc9e87ae2776504dc48bed8a5b9ffa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019289"
---
# <span data-ttu-id="7603b-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7603b-101">Set-AzFirewall</span></span>

## <span data-ttu-id="7603b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7603b-102">SYNOPSIS</span></span>
<span data-ttu-id="7603b-103">Salva un firewall modificato.</span><span class="sxs-lookup"><span data-stu-id="7603b-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="7603b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7603b-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7603b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7603b-105">DESCRIPTION</span></span>
<span data-ttu-id="7603b-106">Il cmdlet **set-AzFirewall** aggiorna un firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="7603b-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="7603b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7603b-107">EXAMPLES</span></span>

### <span data-ttu-id="7603b-108">1: priorità di aggiornamento di una raccolta di regole applicazione firewall</span><span class="sxs-lookup"><span data-stu-id="7603b-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="7603b-109">Questo esempio aggiorna la priorità di una raccolta di regole esistente di un firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="7603b-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="7603b-110">Supponendo che il firewall di Azure "AzureFirewall" nel gruppo di risorse "RG" contenga una raccolta di regole dell'applicazione denominata "ruleCollectionName", i comandi descritti sopra cambieranno la priorità della raccolta di regole e aggiorneranno il firewall di Azure in seguito.</span><span class="sxs-lookup"><span data-stu-id="7603b-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="7603b-111">Senza il comando Set-AzFirewall, tutte le operazioni eseguite sull'oggetto $azFw locale non vengono riflesse nel server.</span><span class="sxs-lookup"><span data-stu-id="7603b-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="7603b-112">2: creare un firewall di Azure e impostare una raccolta regole applicazione in un secondo momento</span><span class="sxs-lookup"><span data-stu-id="7603b-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="7603b-113">In questo esempio, un firewall viene creato per primo senza insiemi di regole applicative.</span><span class="sxs-lookup"><span data-stu-id="7603b-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="7603b-114">In seguito vengono create una regola dell'applicazione e una raccolta regole applicazione, quindi l'oggetto firewall viene modificato in memoria, senza influire sulla configurazione reale nel cloud.</span><span class="sxs-lookup"><span data-stu-id="7603b-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="7603b-115">Per il riflesso delle modifiche nel cloud, Set-AzFirewall deve essere chiamato.</span><span class="sxs-lookup"><span data-stu-id="7603b-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="7603b-116">3: aggiornare la modalità di funzionamento di Intel Threat di Azure firewall</span><span class="sxs-lookup"><span data-stu-id="7603b-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="7603b-117">Questo esempio aggiorna la modalità di funzionamento della minaccia Intel di Azure firewall "AzureFirewall" nel gruppo di risorse "RG".</span><span class="sxs-lookup"><span data-stu-id="7603b-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="7603b-118">Senza il comando Set-AzFirewall, tutte le operazioni eseguite sull'oggetto $azFw locale non vengono riflesse nel server.</span><span class="sxs-lookup"><span data-stu-id="7603b-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="7603b-119">4: deallocare e allocare il firewall</span><span class="sxs-lookup"><span data-stu-id="7603b-119">4: Deallocate and allocate the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="7603b-120">Questo esempio recupera un firewall, rilascia il firewall e lo salva.</span><span class="sxs-lookup"><span data-stu-id="7603b-120">This example retrieves a Firewall, deallocates the firewall, and saves it.</span></span> <span data-ttu-id="7603b-121">Il comando deallocate rimuove il servizio in corso mantenendo la configurazione del firewall.</span><span class="sxs-lookup"><span data-stu-id="7603b-121">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="7603b-122">Per il riflesso delle modifiche nel cloud, Set-AzFirewall deve essere chiamato.</span><span class="sxs-lookup"><span data-stu-id="7603b-122">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>
<span data-ttu-id="7603b-123">Se l'utente vuole riavviare il servizio, il metodo allocate deve essere chiamato sul firewall.</span><span class="sxs-lookup"><span data-stu-id="7603b-123">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="7603b-124">Il nuovo VNet e l'IP pubblico devono essere nello stesso gruppo di risorse del firewall.</span><span class="sxs-lookup"><span data-stu-id="7603b-124">The new VNet and Public IP must be in the same resource group as the Firewall.</span></span> <span data-ttu-id="7603b-125">Anche in questo caso, per le modifiche da rispecchiare nel cloud, Set-AzFirewall deve essere chiamato.</span><span class="sxs-lookup"><span data-stu-id="7603b-125">Again, for changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="7603b-126">5: allocare con un indirizzo IP pubblico di gestione per gli scenari di tunneling forzato</span><span class="sxs-lookup"><span data-stu-id="7603b-126">5: Allocate with a management public IP address for forced tunneling scenarios</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
<span data-ttu-id="7603b-127">In questo esempio viene allocato il firewall con un indirizzo IP pubblico di gestione e una subnet per scenari di tunneling forzati.</span><span class="sxs-lookup"><span data-stu-id="7603b-127">This example allocates the firewall with a management public IP address and subnet for forced tunneling scenarios.</span></span> <span data-ttu-id="7603b-128">VNet deve contenere una subnet denominata "AzureFirewallManagementSubnet".</span><span class="sxs-lookup"><span data-stu-id="7603b-128">The VNet must contain a subnet called "AzureFirewallManagementSubnet".</span></span>

### <span data-ttu-id="7603b-129">6: aggiungere un indirizzo IP pubblico a un firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="7603b-129">6:  Add a Public IP address to an Azure Firewall</span></span>
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="7603b-130">In questo esempio l'indirizzo IP pubblico "azFwPublicIp1" come allegato al firewall.</span><span class="sxs-lookup"><span data-stu-id="7603b-130">In this example, the Public IP Address "azFwPublicIp1" as attached to the Firewall.</span></span>

### <span data-ttu-id="7603b-131">7: rimuovere un indirizzo IP pubblico da un firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="7603b-131">7:  Remove a Public IP address from an Azure Firewall</span></span>
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

<span data-ttu-id="7603b-132">In questo esempio l'indirizzo IP pubblico "azFwPublicIp1" è disconnesso dal firewall.</span><span class="sxs-lookup"><span data-stu-id="7603b-132">In this example, the Public IP Address "azFwPublicIp1" as detached from the Firewall.</span></span>

### <span data-ttu-id="7603b-133">8: modificare l'indirizzo IP pubblico di gestione in un firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="7603b-133">8:  Change the management public IP address on an Azure Firewall</span></span>
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

<span data-ttu-id="7603b-134">In questo esempio l'indirizzo IP pubblico di gestione del firewall verrà modificato in "AzFwMgmtPublicIp2"</span><span class="sxs-lookup"><span data-stu-id="7603b-134">In this example, the management public IP address of the firewall will be changed to "AzFwMgmtPublicIp2"</span></span>


## <span data-ttu-id="7603b-135">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7603b-135">PARAMETERS</span></span>

### <span data-ttu-id="7603b-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7603b-136">-AsJob</span></span>
<span data-ttu-id="7603b-137">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7603b-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7603b-138">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="7603b-138">-AzureFirewall</span></span>
<span data-ttu-id="7603b-139">AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="7603b-139">The AzureFirewall</span></span>

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

### <span data-ttu-id="7603b-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7603b-140">-DefaultProfile</span></span>
<span data-ttu-id="7603b-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7603b-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7603b-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7603b-142">-Confirm</span></span>
<span data-ttu-id="7603b-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7603b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7603b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7603b-144">-WhatIf</span></span>
<span data-ttu-id="7603b-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7603b-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7603b-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7603b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7603b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7603b-147">CommonParameters</span></span>
<span data-ttu-id="7603b-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7603b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7603b-149">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7603b-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7603b-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7603b-150">INPUTS</span></span>

### <span data-ttu-id="7603b-151">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="7603b-151">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="7603b-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7603b-152">OUTPUTS</span></span>

### <span data-ttu-id="7603b-153">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="7603b-153">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="7603b-154">Note</span><span class="sxs-lookup"><span data-stu-id="7603b-154">NOTES</span></span>

## <span data-ttu-id="7603b-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7603b-155">RELATED LINKS</span></span>

[<span data-ttu-id="7603b-156">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7603b-156">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="7603b-157">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7603b-157">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="7603b-158">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7603b-158">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
