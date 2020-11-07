---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 963dc6391ef5f500b26068e2a407eacd64ce6c16
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862758"
---
# <span data-ttu-id="88efd-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="88efd-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="88efd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="88efd-102">SYNOPSIS</span></span>
<span data-ttu-id="88efd-103">Imposta lo stato obiettivo per una configurazione della regola di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="88efd-103">Sets the goal state for a network security rule configuration.</span></span>

## <span data-ttu-id="88efd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88efd-104">SYNTAX</span></span>

### <span data-ttu-id="88efd-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="88efd-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
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

### <span data-ttu-id="88efd-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="88efd-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88efd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88efd-107">DESCRIPTION</span></span>
<span data-ttu-id="88efd-108">Il cmdlet **set-AzNetworkSecurityRuleConfig** imposta lo stato obiettivo per una configurazione della regola di sicurezza di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="88efd-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet sets the goal state for an Azure network security rule configuration.</span></span>

## <span data-ttu-id="88efd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88efd-109">EXAMPLES</span></span>

### <span data-ttu-id="88efd-110">Esempio 1: modificare la configurazione di Access in una regola di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="88efd-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="88efd-111">Il primo comando ottiene il gruppo di sicurezza di rete denominato NSG-FrontEnd e lo archivia nella variabile $nsg.</span><span class="sxs-lookup"><span data-stu-id="88efd-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>

<span data-ttu-id="88efd-112">Il secondo comando usa l'operatore pipeline per passare il gruppo di sicurezza in $nsg a Get-AzNetworkSecurityRuleConfig, che ottiene la configurazione della regola di sicurezza denominata RDP-Rule.</span><span class="sxs-lookup"><span data-stu-id="88efd-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>

<span data-ttu-id="88efd-113">Il terzo comando modifica la configurazione di Access di RDP-Rule in Deny.</span><span class="sxs-lookup"><span data-stu-id="88efd-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="88efd-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="88efd-114">PARAMETERS</span></span>

### <span data-ttu-id="88efd-115">-Access</span><span class="sxs-lookup"><span data-stu-id="88efd-115">-Access</span></span>
<span data-ttu-id="88efd-116">Specifica se il traffico di rete è consentito o negato.</span><span class="sxs-lookup"><span data-stu-id="88efd-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="88efd-117">I valori accettabili per questo parametro sono: Allow e Deny.</span><span class="sxs-lookup"><span data-stu-id="88efd-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="88efd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88efd-118">-DefaultProfile</span></span>
<span data-ttu-id="88efd-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="88efd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88efd-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="88efd-120">-Description</span></span>
<span data-ttu-id="88efd-121">Specifica una descrizione per una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="88efd-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="88efd-122">La dimensione massima è di 140 caratteri.</span><span class="sxs-lookup"><span data-stu-id="88efd-122">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="88efd-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="88efd-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="88efd-124">Specifica un prefisso per l'indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="88efd-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="88efd-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="88efd-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="88efd-126">Un indirizzo CIDR (classe Interdomain Routing)</span><span class="sxs-lookup"><span data-stu-id="88efd-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="88efd-127">Un intervallo di indirizzi IP di destinazione</span><span class="sxs-lookup"><span data-stu-id="88efd-127">A destination IP address range</span></span> 
- <span data-ttu-id="88efd-128">Carattere jolly (\*) che corrisponde a qualsiasi indirizzo IP</span><span class="sxs-lookup"><span data-stu-id="88efd-128">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="88efd-129">È possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="88efd-129">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="88efd-130">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="88efd-130">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="88efd-131">Gruppo di sicurezza dell'applicazione impostato come destinazione per la regola.</span><span class="sxs-lookup"><span data-stu-id="88efd-131">The application security group set as destination for the rule.</span></span> <span data-ttu-id="88efd-132">Non può essere usato con il parametro "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="88efd-132">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="88efd-133">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="88efd-133">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="88efd-134">Gruppo di sicurezza dell'applicazione impostato come destinazione per la regola.</span><span class="sxs-lookup"><span data-stu-id="88efd-134">The application security group set as destination for the rule.</span></span> <span data-ttu-id="88efd-135">Non può essere usato con il parametro "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="88efd-135">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="88efd-136">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="88efd-136">-DestinationPortRange</span></span>
<span data-ttu-id="88efd-137">Specifica una porta o un intervallo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="88efd-137">Specifies a destination port or range.</span></span>
<span data-ttu-id="88efd-138">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="88efd-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="88efd-139">Un numero intero</span><span class="sxs-lookup"><span data-stu-id="88efd-139">An integer</span></span> 
- <span data-ttu-id="88efd-140">Un intervallo di numeri interi compresi tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="88efd-140">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="88efd-141">Carattere jolly (\*) che corrisponde a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="88efd-141">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="88efd-142">-Direzione</span><span class="sxs-lookup"><span data-stu-id="88efd-142">-Direction</span></span>
<span data-ttu-id="88efd-143">Specifica se una regola viene valutata per il traffico in entrata o in uscita.</span><span class="sxs-lookup"><span data-stu-id="88efd-143">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="88efd-144">I valori accettabili per questo parametro sono: in ingresso e in uscita.</span><span class="sxs-lookup"><span data-stu-id="88efd-144">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="88efd-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="88efd-145">-Name</span></span>
<span data-ttu-id="88efd-146">Specifica il nome della configurazione della regola di sicurezza della rete impostata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88efd-146">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="88efd-147">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="88efd-147">-NetworkSecurityGroup</span></span>
<span data-ttu-id="88efd-148">Specifica l'oggetto **NetworkSecurityGroup** che contiene la configurazione della regola di sicurezza della rete da impostare.</span><span class="sxs-lookup"><span data-stu-id="88efd-148">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="88efd-149">-Priorità</span><span class="sxs-lookup"><span data-stu-id="88efd-149">-Priority</span></span>
<span data-ttu-id="88efd-150">Specifica la priorità di una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="88efd-150">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="88efd-151">I valori accettabili per questo parametro sono: un numero intero compreso tra 100 e 4096.</span><span class="sxs-lookup"><span data-stu-id="88efd-151">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>

<span data-ttu-id="88efd-152">Il numero di priorità deve essere univoco per ogni regola della raccolta.</span><span class="sxs-lookup"><span data-stu-id="88efd-152">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="88efd-153">Minore è il numero di priorità, maggiore è la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="88efd-153">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="88efd-154">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="88efd-154">-Protocol</span></span>
<span data-ttu-id="88efd-155">Specifica il protocollo di rete a cui si applica una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="88efd-155">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="88efd-156">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="88efd-156">The acceptable values for this parameter are:</span></span>

 <span data-ttu-id="88efd-157">--TCP</span><span class="sxs-lookup"><span data-stu-id="88efd-157">--Tcp</span></span>
- <span data-ttu-id="88efd-158">UDP</span><span class="sxs-lookup"><span data-stu-id="88efd-158">Udp</span></span>
- <span data-ttu-id="88efd-159">Carattere jolly (\*) in modo che corrisponda a entrambi</span><span class="sxs-lookup"><span data-stu-id="88efd-159">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="88efd-160">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="88efd-160">-SourceAddressPrefix</span></span>
<span data-ttu-id="88efd-161">Specifica un prefisso per l'indirizzo di origine.</span><span class="sxs-lookup"><span data-stu-id="88efd-161">Specifies a source address prefix.</span></span>
<span data-ttu-id="88efd-162">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="88efd-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="88efd-163">UN CIDR</span><span class="sxs-lookup"><span data-stu-id="88efd-163">A CIDR</span></span>
- <span data-ttu-id="88efd-164">Un intervallo IP di origine</span><span class="sxs-lookup"><span data-stu-id="88efd-164">A source IP range</span></span>
- <span data-ttu-id="88efd-165">Carattere jolly (\*) che corrisponde a qualsiasi indirizzo IP</span><span class="sxs-lookup"><span data-stu-id="88efd-165">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="88efd-166">È anche possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="88efd-166">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="88efd-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="88efd-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="88efd-168">Gruppo di sicurezza dell'applicazione impostato come origine per la regola.</span><span class="sxs-lookup"><span data-stu-id="88efd-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="88efd-169">Non può essere usato con il parametro "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="88efd-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="88efd-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="88efd-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="88efd-171">Gruppo di sicurezza dell'applicazione impostato come origine per la regola.</span><span class="sxs-lookup"><span data-stu-id="88efd-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="88efd-172">Non può essere usato con il parametro "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="88efd-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="88efd-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="88efd-173">-SourcePortRange</span></span>
<span data-ttu-id="88efd-174">Specifica la porta o l'intervallo di origine.</span><span class="sxs-lookup"><span data-stu-id="88efd-174">Specifies the source port or range.</span></span>
<span data-ttu-id="88efd-175">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="88efd-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="88efd-176">Un numero intero</span><span class="sxs-lookup"><span data-stu-id="88efd-176">An integer</span></span>
- <span data-ttu-id="88efd-177">Un intervallo di numeri interi compresi tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="88efd-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="88efd-178">Carattere jolly (\*) che corrisponde a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="88efd-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="88efd-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88efd-179">CommonParameters</span></span>
<span data-ttu-id="88efd-180">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88efd-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88efd-181">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88efd-181">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88efd-182">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="88efd-182">INPUTS</span></span>

### <span data-ttu-id="88efd-183">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="88efd-183">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="88efd-184">Il parametro ' NetworkSecurityGroup ' accetta il valore di tipo ' PSNetworkSecurityGroup ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="88efd-184">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="88efd-185">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88efd-185">OUTPUTS</span></span>

### <span data-ttu-id="88efd-186">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="88efd-186">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="88efd-187">Note</span><span class="sxs-lookup"><span data-stu-id="88efd-187">NOTES</span></span>

## <span data-ttu-id="88efd-188">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88efd-188">RELATED LINKS</span></span>

[<span data-ttu-id="88efd-189">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="88efd-189">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="88efd-190">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="88efd-190">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="88efd-191">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="88efd-191">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="88efd-192">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="88efd-192">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


