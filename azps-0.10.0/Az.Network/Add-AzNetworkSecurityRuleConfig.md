---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: b2b1667a9326a9c25d78639e397146c0dd85dc5f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860954"
---
# <span data-ttu-id="df256-101">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="df256-101">Add-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="df256-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="df256-102">SYNOPSIS</span></span>
<span data-ttu-id="df256-103">Aggiunge una configurazione della regola di sicurezza di rete a un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="df256-103">Adds a network security rule configuration to a network security group.</span></span>

## <span data-ttu-id="df256-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df256-104">SYNTAX</span></span>

### <span data-ttu-id="df256-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="df256-105">SetByResource (Default)</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="df256-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="df256-106">SetByResourceId</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df256-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df256-107">DESCRIPTION</span></span>
<span data-ttu-id="df256-108">Il cmdlet **Add-AzNetworkSecurityRuleConfig** aggiunge una configurazione della regola di sicurezza di rete a un gruppo di sicurezza di rete di Azure.</span><span class="sxs-lookup"><span data-stu-id="df256-108">The **Add-AzNetworkSecurityRuleConfig** cmdlet adds a network security rule configuration to an Azure network security group.</span></span>

## <span data-ttu-id="df256-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df256-109">EXAMPLES</span></span>

### <span data-ttu-id="df256-110">1: aggiunta di un gruppo di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="df256-110">1: Adding a network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

<span data-ttu-id="df256-111">Il primo comando Recupera un gruppo di sicurezza di rete di Azure denominato "nsg1" dal gruppo di risorse "RG1".</span><span class="sxs-lookup"><span data-stu-id="df256-111">The first command retrieves an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="df256-112">Il secondo comando aggiunge una regola di sicurezza di rete denominata "RDP-Rule" che consente il traffico da Internet sulla porta 3389 all'oggetto del gruppo di sicurezza di rete recuperato.</span><span class="sxs-lookup"><span data-stu-id="df256-112">The second command adds a network security rule named "rdp-rule" that allows traffic from internet on port 3389 to the retrieved network security group object.</span></span> <span data-ttu-id="df256-113">Rende persistente il gruppo di sicurezza di rete di Azure modificato.</span><span class="sxs-lookup"><span data-stu-id="df256-113">Persists the modified Azure network security group.</span></span>

### <span data-ttu-id="df256-114">1: aggiunta di una nuova regola di sicurezza con i gruppi di sicurezza delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="df256-114">1: Adding a new security rule with application security groups</span></span>
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

<span data-ttu-id="df256-115">Prima di tutto, creiamo due nuovi gruppi di sicurezza delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="df256-115">First, we create two new application security groups.</span></span> <span data-ttu-id="df256-116">Recuperiamo quindi un gruppo di sicurezza di rete di Azure denominato "nsg1" dal gruppo di risorse "RG1".</span><span class="sxs-lookup"><span data-stu-id="df256-116">Then, we retrieve an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="df256-117">e Aggiungi una regola di sicurezza di rete denominata "RDP-Rule".</span><span class="sxs-lookup"><span data-stu-id="df256-117">and add a network security rule named "rdp-rule" to it.</span></span> <span data-ttu-id="df256-118">La regola consente il traffico da tutte le configurazioni IP nel gruppo di sicurezza dell'applicazione "srcAsg" a tutte le configurazioni IP in "destAsg" sulla porta 3389.</span><span class="sxs-lookup"><span data-stu-id="df256-118">The rule allows traffic from all the IP configurations in the application security group "srcAsg" to all the IP configurations in "destAsg" on port 3389.</span></span> <span data-ttu-id="df256-119">Dopo aver aggiunto la regola, il gruppo di sicurezza di Azure Network modificato viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="df256-119">After adding the rule, we persist the modified Azure network security group.</span></span>

## <span data-ttu-id="df256-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="df256-120">PARAMETERS</span></span>

### <span data-ttu-id="df256-121">-Access</span><span class="sxs-lookup"><span data-stu-id="df256-121">-Access</span></span>
<span data-ttu-id="df256-122">Specifica se il traffico di rete è consentito o negato.</span><span class="sxs-lookup"><span data-stu-id="df256-122">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="df256-123">I valori accettabili per questo parametro sono: Allow e Deny.</span><span class="sxs-lookup"><span data-stu-id="df256-123">The acceptable values for this parameter are: Allow and Deny.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df256-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df256-124">-DefaultProfile</span></span>
<span data-ttu-id="df256-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="df256-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df256-126">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="df256-126">-Description</span></span>
<span data-ttu-id="df256-127">Specifica una descrizione di una configurazione della regola di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="df256-127">Specifies a description of a network security rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df256-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="df256-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="df256-129">Specifica un prefisso per l'indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="df256-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="df256-130">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="df256-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="df256-131">Un indirizzo CIDR (classe Interdomain Routing)</span><span class="sxs-lookup"><span data-stu-id="df256-131">A Classless Interdomain Routing (CIDR) address</span></span>
- <span data-ttu-id="df256-132">Un intervallo di indirizzi IP di destinazione</span><span class="sxs-lookup"><span data-stu-id="df256-132">A destination IP address range</span></span>
- <span data-ttu-id="df256-133">Carattere jolly (\*) che corrisponde a qualsiasi indirizzo IP</span><span class="sxs-lookup"><span data-stu-id="df256-133">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="df256-134">È possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="df256-134">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df256-135">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="df256-135">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="df256-136">Gruppo di sicurezza dell'applicazione impostato come destinazione per la regola.</span><span class="sxs-lookup"><span data-stu-id="df256-136">The application security group set as destination for the rule.</span></span> <span data-ttu-id="df256-137">Non può essere usato con il parametro "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="df256-137">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df256-138">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="df256-138">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="df256-139">Gruppo di sicurezza dell'applicazione impostato come destinazione per la regola.</span><span class="sxs-lookup"><span data-stu-id="df256-139">The application security group set as destination for the rule.</span></span> <span data-ttu-id="df256-140">Non può essere usato con il parametro "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="df256-140">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df256-141">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="df256-141">-DestinationPortRange</span></span>
<span data-ttu-id="df256-142">Specifica una porta o un intervallo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="df256-142">Specifies a destination port or range.</span></span>
<span data-ttu-id="df256-143">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="df256-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="df256-144">Un numero intero</span><span class="sxs-lookup"><span data-stu-id="df256-144">An integer</span></span>
- <span data-ttu-id="df256-145">Un intervallo di numeri interi compresi tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="df256-145">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="df256-146">Carattere jolly (\*) che corrisponde a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="df256-146">A wildcard character (\*) to match any port</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df256-147">-Direzione</span><span class="sxs-lookup"><span data-stu-id="df256-147">-Direction</span></span>
<span data-ttu-id="df256-148">Specifica se una regola viene valutata nel traffico in entrata o in uscita.</span><span class="sxs-lookup"><span data-stu-id="df256-148">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="df256-149">I valori accettabili per questo parametro sono: in ingresso e in uscita.</span><span class="sxs-lookup"><span data-stu-id="df256-149">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df256-150">-Nome</span><span class="sxs-lookup"><span data-stu-id="df256-150">-Name</span></span>
<span data-ttu-id="df256-151">Specifica il nome di una configurazione della regola di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="df256-151">Specifies the name of a network security rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df256-152">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="df256-152">-NetworkSecurityGroup</span></span>
<span data-ttu-id="df256-153">Specifica un oggetto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="df256-153">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="df256-154">Questo cmdlet aggiunge una configurazione della regola di sicurezza di rete all'oggetto specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="df256-154">This cmdlet adds a network security rule configuration to the object that this parameter specifies.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df256-155">-Priorità</span><span class="sxs-lookup"><span data-stu-id="df256-155">-Priority</span></span>
<span data-ttu-id="df256-156">Specifica la priorità di una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="df256-156">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="df256-157">I valori accettabili per questo parametro sono: un numero intero compreso tra 100 e 4096.</span><span class="sxs-lookup"><span data-stu-id="df256-157">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>

<span data-ttu-id="df256-158">Il numero di priorità deve essere univoco per ogni regola della raccolta.</span><span class="sxs-lookup"><span data-stu-id="df256-158">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="df256-159">Minore è il numero di priorità, maggiore è la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="df256-159">The lower the priority number, the higher the priority of the rule.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df256-160">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="df256-160">-Protocol</span></span>
<span data-ttu-id="df256-161">Specifica il protocollo di rete a cui si applica una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="df256-161">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="df256-162">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="df256-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="df256-163">TCP</span><span class="sxs-lookup"><span data-stu-id="df256-163">Tcp</span></span>
- <span data-ttu-id="df256-164">UDP</span><span class="sxs-lookup"><span data-stu-id="df256-164">Udp</span></span>
- <span data-ttu-id="df256-165">Carattere jolly (\*) in modo che corrisponda a entrambi</span><span class="sxs-lookup"><span data-stu-id="df256-165">Wildcard character (\*) to match both</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df256-166">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="df256-166">-SourceAddressPrefix</span></span>
<span data-ttu-id="df256-167">Specifica un prefisso per l'indirizzo di origine.</span><span class="sxs-lookup"><span data-stu-id="df256-167">Specifies a source address prefix.</span></span>
<span data-ttu-id="df256-168">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="df256-168">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="df256-169">UN CIDR</span><span class="sxs-lookup"><span data-stu-id="df256-169">A CIDR</span></span>
- <span data-ttu-id="df256-170">Un intervallo IP di origine</span><span class="sxs-lookup"><span data-stu-id="df256-170">A source IP range</span></span>
- <span data-ttu-id="df256-171">Un carattere jolly (\*) per corrispondere a qualsiasi indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="df256-171">A wildcard character (\*) to match any IP address.</span></span>

<span data-ttu-id="df256-172">È anche possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="df256-172">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df256-173">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="df256-173">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="df256-174">Gruppo di sicurezza dell'applicazione impostato come origine per la regola.</span><span class="sxs-lookup"><span data-stu-id="df256-174">The application security group set as source for the rule.</span></span> <span data-ttu-id="df256-175">Non può essere usato con il parametro "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="df256-175">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df256-176">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="df256-176">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="df256-177">Gruppo di sicurezza dell'applicazione impostato come origine per la regola.</span><span class="sxs-lookup"><span data-stu-id="df256-177">The application security group set as source for the rule.</span></span> <span data-ttu-id="df256-178">Non può essere usato con il parametro "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="df256-178">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df256-179">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="df256-179">-SourcePortRange</span></span>
<span data-ttu-id="df256-180">Specifica una porta o un intervallo di origine.</span><span class="sxs-lookup"><span data-stu-id="df256-180">Specifies a source port or range.</span></span>
<span data-ttu-id="df256-181">Questo valore è espresso come numero intero, come intervallo compreso tra 0 e 65535 o come carattere jolly (\*) in modo che corrisponda a qualsiasi porta di origine.</span><span class="sxs-lookup"><span data-stu-id="df256-181">This value is expressed as an integer, as a range between 0 and 65535, or as a wildcard character (\*) to match any source port.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df256-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df256-182">CommonParameters</span></span>
<span data-ttu-id="df256-183">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df256-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df256-184">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df256-184">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df256-185">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="df256-185">INPUTS</span></span>

### <span data-ttu-id="df256-186">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="df256-186">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="df256-187">Il parametro ' NetworkSecurityGroup ' accetta il valore di tipo ' PSNetworkSecurityGroup ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="df256-187">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="df256-188">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df256-188">OUTPUTS</span></span>

### <span data-ttu-id="df256-189">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="df256-189">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="df256-190">Note</span><span class="sxs-lookup"><span data-stu-id="df256-190">NOTES</span></span>

## <span data-ttu-id="df256-191">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df256-191">RELATED LINKS</span></span>

[<span data-ttu-id="df256-192">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="df256-192">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="df256-193">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="df256-193">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="df256-194">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="df256-194">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="df256-195">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="df256-195">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


