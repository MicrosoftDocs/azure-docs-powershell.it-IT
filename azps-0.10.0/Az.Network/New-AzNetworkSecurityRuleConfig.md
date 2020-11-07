---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 17e73f28595a0b99c8209634a6dee6838fa4599d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860462"
---
# <span data-ttu-id="a1c39-101">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1c39-101">New-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="a1c39-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1c39-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c39-103">Crea una configurazione della regola di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="a1c39-103">Creates a network security rule configuration.</span></span>

## <span data-ttu-id="a1c39-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1c39-104">SYNTAX</span></span>

### <span data-ttu-id="a1c39-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a1c39-105">SetByResource (Default)</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1c39-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a1c39-106">SetByResourceId</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1c39-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1c39-107">DESCRIPTION</span></span>
<span data-ttu-id="a1c39-108">Il cmdlet **New-AzNetworkSecurityRuleConfig** crea una configurazione della regola di sicurezza di rete Azure per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="a1c39-108">The **New-AzNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="a1c39-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1c39-109">EXAMPLES</span></span>

### <span data-ttu-id="a1c39-110">1: creare una regola di sicurezza della rete per consentire RDP</span><span class="sxs-lookup"><span data-stu-id="a1c39-110">1: Create a network security rule to allow RDP</span></span>
```
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="a1c39-111">Questo comando crea una regola di sicurezza che consente l'accesso da Internet alla porta 3389</span><span class="sxs-lookup"><span data-stu-id="a1c39-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="a1c39-112">2: creare una regola di sicurezza di rete che consente l'HTTP</span><span class="sxs-lookup"><span data-stu-id="a1c39-112">2: Create a network security rule that allows HTTP</span></span>
```
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="a1c39-113">Questo comando crea una regola di sicurezza che consente l'accesso da Internet alla porta 80</span><span class="sxs-lookup"><span data-stu-id="a1c39-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="a1c39-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1c39-114">PARAMETERS</span></span>

### <span data-ttu-id="a1c39-115">-Access</span><span class="sxs-lookup"><span data-stu-id="a1c39-115">-Access</span></span>
<span data-ttu-id="a1c39-116">Specifica se il traffico di rete è consentito o negato.</span><span class="sxs-lookup"><span data-stu-id="a1c39-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="a1c39-117">I valori accettabili per questo parametro sono: Allow e Deny.</span><span class="sxs-lookup"><span data-stu-id="a1c39-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="a1c39-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1c39-118">-DefaultProfile</span></span>
<span data-ttu-id="a1c39-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1c39-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1c39-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1c39-120">-Description</span></span>
<span data-ttu-id="a1c39-121">Specifica una descrizione della configurazione della regola di sicurezza della rete da creare.</span><span class="sxs-lookup"><span data-stu-id="a1c39-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="a1c39-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a1c39-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="a1c39-123">Specifica un prefisso per l'indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a1c39-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="a1c39-124">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a1c39-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a1c39-125">Un indirizzo CIDR (classe Interdomain Routing)</span><span class="sxs-lookup"><span data-stu-id="a1c39-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="a1c39-126">Un intervallo di indirizzi IP di destinazione</span><span class="sxs-lookup"><span data-stu-id="a1c39-126">A destination IP address range</span></span> 
- <span data-ttu-id="a1c39-127">Carattere jolly (\*) che corrisponde a qualsiasi indirizzo IP</span><span class="sxs-lookup"><span data-stu-id="a1c39-127">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="a1c39-128">È possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="a1c39-128">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="a1c39-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a1c39-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="a1c39-130">Gruppo di sicurezza dell'applicazione impostato come destinazione per la regola.</span><span class="sxs-lookup"><span data-stu-id="a1c39-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="a1c39-131">Non può essere usato con il parametro "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="a1c39-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="a1c39-132">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a1c39-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="a1c39-133">Gruppo di sicurezza dell'applicazione impostato come destinazione per la regola.</span><span class="sxs-lookup"><span data-stu-id="a1c39-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="a1c39-134">Non può essere usato con il parametro "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="a1c39-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="a1c39-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="a1c39-135">-DestinationPortRange</span></span>
<span data-ttu-id="a1c39-136">Specifica una porta o un intervallo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a1c39-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="a1c39-137">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a1c39-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a1c39-138">Un numero intero</span><span class="sxs-lookup"><span data-stu-id="a1c39-138">An integer</span></span>
- <span data-ttu-id="a1c39-139">Un intervallo di numeri interi compresi tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="a1c39-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="a1c39-140">Carattere jolly (\*) che corrisponde a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="a1c39-140">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="a1c39-141">-Direzione</span><span class="sxs-lookup"><span data-stu-id="a1c39-141">-Direction</span></span>
<span data-ttu-id="a1c39-142">Specifica se una regola viene valutata nel traffico in entrata o in uscita.</span><span class="sxs-lookup"><span data-stu-id="a1c39-142">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="a1c39-143">I valori accettabili per questo parametro sono: in ingresso e in uscita.</span><span class="sxs-lookup"><span data-stu-id="a1c39-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="a1c39-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1c39-144">-Name</span></span>
<span data-ttu-id="a1c39-145">Specifica il nome della configurazione della regola di sicurezza della rete creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1c39-145">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a1c39-146">-Priorità</span><span class="sxs-lookup"><span data-stu-id="a1c39-146">-Priority</span></span>
<span data-ttu-id="a1c39-147">Specifica la priorità di una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="a1c39-147">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="a1c39-148">I valori accettabili per questo parametro sono: un numero intero compreso tra 100 e 4096.</span><span class="sxs-lookup"><span data-stu-id="a1c39-148">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>

<span data-ttu-id="a1c39-149">Il numero di priorità deve essere univoco per ogni regola della raccolta.</span><span class="sxs-lookup"><span data-stu-id="a1c39-149">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="a1c39-150">Minore è il numero di priorità, maggiore è la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="a1c39-150">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="a1c39-151">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="a1c39-151">-Protocol</span></span>
<span data-ttu-id="a1c39-152">Specifica il protocollo di rete a cui si applica una nuova configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="a1c39-152">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="a1c39-153">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a1c39-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a1c39-154">TCP</span><span class="sxs-lookup"><span data-stu-id="a1c39-154">Tcp</span></span>
- <span data-ttu-id="a1c39-155">UDP</span><span class="sxs-lookup"><span data-stu-id="a1c39-155">Udp</span></span>
- <span data-ttu-id="a1c39-156">carattere jolly (\*) in modo che corrisponda a entrambi.</span><span class="sxs-lookup"><span data-stu-id="a1c39-156">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="a1c39-157">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a1c39-157">-SourceAddressPrefix</span></span>
<span data-ttu-id="a1c39-158">Specifica un prefisso per l'indirizzo di origine.</span><span class="sxs-lookup"><span data-stu-id="a1c39-158">Specifies a source address prefix.</span></span>
<span data-ttu-id="a1c39-159">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a1c39-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a1c39-160">UN CIDR</span><span class="sxs-lookup"><span data-stu-id="a1c39-160">A CIDR</span></span>
- <span data-ttu-id="a1c39-161">Un intervallo IP di origine</span><span class="sxs-lookup"><span data-stu-id="a1c39-161">A source IP range</span></span>
- <span data-ttu-id="a1c39-162">Un carattere jolly (\*) per corrispondere a qualsiasi indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="a1c39-162">A wildcard character (\*) to match any IP address.</span></span>

<span data-ttu-id="a1c39-163">È anche possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="a1c39-163">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="a1c39-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a1c39-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="a1c39-165">Gruppo di sicurezza dell'applicazione impostato come origine per la regola.</span><span class="sxs-lookup"><span data-stu-id="a1c39-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="a1c39-166">Non può essere usato con il parametro "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="a1c39-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="a1c39-167">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a1c39-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="a1c39-168">Gruppo di sicurezza dell'applicazione impostato come origine per la regola.</span><span class="sxs-lookup"><span data-stu-id="a1c39-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="a1c39-169">Non può essere usato con il parametro "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="a1c39-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="a1c39-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="a1c39-170">-SourcePortRange</span></span>
<span data-ttu-id="a1c39-171">Specifica la porta o l'intervallo di origine.</span><span class="sxs-lookup"><span data-stu-id="a1c39-171">Specifies the source port or range.</span></span>
<span data-ttu-id="a1c39-172">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a1c39-172">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a1c39-173">Un numero intero</span><span class="sxs-lookup"><span data-stu-id="a1c39-173">An integer</span></span>
- <span data-ttu-id="a1c39-174">Un intervallo di numeri interi compresi tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="a1c39-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="a1c39-175">Carattere jolly (\*) che corrisponde a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="a1c39-175">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="a1c39-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c39-176">CommonParameters</span></span>
<span data-ttu-id="a1c39-177">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1c39-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c39-178">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1c39-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c39-179">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1c39-179">INPUTS</span></span>

## <span data-ttu-id="a1c39-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1c39-180">OUTPUTS</span></span>

### <span data-ttu-id="a1c39-181">Microsoft. Azure. Commands. Network. Models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="a1c39-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="a1c39-182">Note</span><span class="sxs-lookup"><span data-stu-id="a1c39-182">NOTES</span></span>

## <span data-ttu-id="a1c39-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1c39-183">RELATED LINKS</span></span>

[<span data-ttu-id="a1c39-184">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1c39-184">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a1c39-185">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1c39-185">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a1c39-186">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1c39-186">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a1c39-187">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a1c39-187">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


