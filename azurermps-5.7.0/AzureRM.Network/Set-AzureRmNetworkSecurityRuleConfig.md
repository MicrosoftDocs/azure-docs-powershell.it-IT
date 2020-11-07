---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: c1febd5d39e99ef52e940c590fcd43c24b19affd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520685"
---
# <span data-ttu-id="9190b-101">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9190b-101">Set-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="9190b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9190b-102">SYNOPSIS</span></span>
<span data-ttu-id="9190b-103">Imposta lo stato obiettivo per una configurazione della regola di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="9190b-103">Sets the goal state for a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9190b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9190b-104">SYNTAX</span></span>

### <span data-ttu-id="9190b-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9190b-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
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

### <span data-ttu-id="9190b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9190b-106">SetByResourceId</span></span>
```
Set-AzureRmNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9190b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9190b-107">DESCRIPTION</span></span>
<span data-ttu-id="9190b-108">Il cmdlet **set-AzureRmNetworkSecurityRuleConfig** imposta lo stato obiettivo per una configurazione della regola di sicurezza di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="9190b-108">The **Set-AzureRmNetworkSecurityRuleConfig** cmdlet sets the goal state for an Azure network security rule configuration.</span></span>

## <span data-ttu-id="9190b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9190b-109">EXAMPLES</span></span>

### <span data-ttu-id="9190b-110">Esempio 1: modificare la configurazione di Access in una regola di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="9190b-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="9190b-111">Il primo comando ottiene il gruppo di sicurezza di rete denominato NSG-FrontEnd e lo archivia nella variabile $nsg.</span><span class="sxs-lookup"><span data-stu-id="9190b-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>

<span data-ttu-id="9190b-112">Il secondo comando usa l'operatore pipeline per passare il gruppo di sicurezza in $nsg a Get-AzureRmNetworkSecurityRuleConfig, che ottiene la configurazione della regola di sicurezza denominata RDP-Rule.</span><span class="sxs-lookup"><span data-stu-id="9190b-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzureRmNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>

<span data-ttu-id="9190b-113">Il terzo comando modifica la configurazione di Access di RDP-Rule in Deny.</span><span class="sxs-lookup"><span data-stu-id="9190b-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="9190b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9190b-114">PARAMETERS</span></span>

### <span data-ttu-id="9190b-115">-Access</span><span class="sxs-lookup"><span data-stu-id="9190b-115">-Access</span></span>
<span data-ttu-id="9190b-116">Specifica se il traffico di rete è consentito o negato.</span><span class="sxs-lookup"><span data-stu-id="9190b-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="9190b-117">I valori accettabili per questo parametro sono: Allow e Deny.</span><span class="sxs-lookup"><span data-stu-id="9190b-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="9190b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9190b-118">-DefaultProfile</span></span>
<span data-ttu-id="9190b-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9190b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9190b-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="9190b-120">-Description</span></span>
<span data-ttu-id="9190b-121">Specifica una descrizione per una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="9190b-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="9190b-122">La dimensione massima è di 140 caratteri.</span><span class="sxs-lookup"><span data-stu-id="9190b-122">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="9190b-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9190b-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="9190b-124">Specifica un prefisso per l'indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9190b-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="9190b-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9190b-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9190b-126">Un indirizzo CIDR (classe Interdomain Routing)</span><span class="sxs-lookup"><span data-stu-id="9190b-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="9190b-127">Un intervallo di indirizzi IP di destinazione</span><span class="sxs-lookup"><span data-stu-id="9190b-127">A destination IP address range</span></span> 
- <span data-ttu-id="9190b-128">Carattere jolly (\*) che corrisponde a qualsiasi indirizzo IP</span><span class="sxs-lookup"><span data-stu-id="9190b-128">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="9190b-129">È possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="9190b-129">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="9190b-130">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9190b-130">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="9190b-131">Gruppo di sicurezza dell'applicazione impostato come destinazione per la regola.</span><span class="sxs-lookup"><span data-stu-id="9190b-131">The application security group set as destination for the rule.</span></span> <span data-ttu-id="9190b-132">Non può essere usato con il parametro "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="9190b-132">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="9190b-133">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="9190b-133">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="9190b-134">Gruppo di sicurezza dell'applicazione impostato come destinazione per la regola.</span><span class="sxs-lookup"><span data-stu-id="9190b-134">The application security group set as destination for the rule.</span></span> <span data-ttu-id="9190b-135">Non può essere usato con il parametro "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="9190b-135">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="9190b-136">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="9190b-136">-DestinationPortRange</span></span>
<span data-ttu-id="9190b-137">Specifica una porta o un intervallo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9190b-137">Specifies a destination port or range.</span></span>
<span data-ttu-id="9190b-138">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9190b-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9190b-139">Un numero intero</span><span class="sxs-lookup"><span data-stu-id="9190b-139">An integer</span></span> 
- <span data-ttu-id="9190b-140">Un intervallo di numeri interi compresi tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="9190b-140">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="9190b-141">Carattere jolly (\*) che corrisponde a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="9190b-141">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="9190b-142">-Direzione</span><span class="sxs-lookup"><span data-stu-id="9190b-142">-Direction</span></span>
<span data-ttu-id="9190b-143">Specifica se una regola viene valutata per il traffico in entrata o in uscita.</span><span class="sxs-lookup"><span data-stu-id="9190b-143">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="9190b-144">I valori accettabili per questo parametro sono: in ingresso e in uscita.</span><span class="sxs-lookup"><span data-stu-id="9190b-144">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="9190b-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="9190b-145">-Name</span></span>
<span data-ttu-id="9190b-146">Specifica il nome della configurazione della regola di sicurezza della rete impostata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9190b-146">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="9190b-147">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9190b-147">-NetworkSecurityGroup</span></span>
<span data-ttu-id="9190b-148">Specifica l'oggetto **NetworkSecurityGroup** che contiene la configurazione della regola di sicurezza della rete da impostare.</span><span class="sxs-lookup"><span data-stu-id="9190b-148">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="9190b-149">-Priorità</span><span class="sxs-lookup"><span data-stu-id="9190b-149">-Priority</span></span>
<span data-ttu-id="9190b-150">Specifica la priorità di una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="9190b-150">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="9190b-151">I valori accettabili per questo parametro sono: un numero intero compreso tra 100 e 4096.</span><span class="sxs-lookup"><span data-stu-id="9190b-151">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>

<span data-ttu-id="9190b-152">Il numero di priorità deve essere univoco per ogni regola della raccolta.</span><span class="sxs-lookup"><span data-stu-id="9190b-152">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="9190b-153">Minore è il numero di priorità, maggiore è la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="9190b-153">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="9190b-154">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="9190b-154">-Protocol</span></span>
<span data-ttu-id="9190b-155">Specifica il protocollo di rete a cui si applica una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="9190b-155">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="9190b-156">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9190b-156">The acceptable values for this parameter are:</span></span>

 <span data-ttu-id="9190b-157">--TCP</span><span class="sxs-lookup"><span data-stu-id="9190b-157">--Tcp</span></span>
- <span data-ttu-id="9190b-158">UDP</span><span class="sxs-lookup"><span data-stu-id="9190b-158">Udp</span></span>
- <span data-ttu-id="9190b-159">Carattere jolly (\*) in modo che corrisponda a entrambi</span><span class="sxs-lookup"><span data-stu-id="9190b-159">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="9190b-160">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="9190b-160">-SourceAddressPrefix</span></span>
<span data-ttu-id="9190b-161">Specifica un prefisso per l'indirizzo di origine.</span><span class="sxs-lookup"><span data-stu-id="9190b-161">Specifies a source address prefix.</span></span>
<span data-ttu-id="9190b-162">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9190b-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9190b-163">UN CIDR</span><span class="sxs-lookup"><span data-stu-id="9190b-163">A CIDR</span></span>
- <span data-ttu-id="9190b-164">Un intervallo IP di origine</span><span class="sxs-lookup"><span data-stu-id="9190b-164">A source IP range</span></span>
- <span data-ttu-id="9190b-165">Carattere jolly (\*) che corrisponde a qualsiasi indirizzo IP</span><span class="sxs-lookup"><span data-stu-id="9190b-165">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="9190b-166">È anche possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="9190b-166">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="9190b-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9190b-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="9190b-168">Gruppo di sicurezza dell'applicazione impostato come origine per la regola.</span><span class="sxs-lookup"><span data-stu-id="9190b-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="9190b-169">Non può essere usato con il parametro "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="9190b-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="9190b-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="9190b-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="9190b-171">Gruppo di sicurezza dell'applicazione impostato come origine per la regola.</span><span class="sxs-lookup"><span data-stu-id="9190b-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="9190b-172">Non può essere usato con il parametro "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="9190b-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="9190b-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="9190b-173">-SourcePortRange</span></span>
<span data-ttu-id="9190b-174">Specifica la porta o l'intervallo di origine.</span><span class="sxs-lookup"><span data-stu-id="9190b-174">Specifies the source port or range.</span></span>
<span data-ttu-id="9190b-175">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9190b-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9190b-176">Un numero intero</span><span class="sxs-lookup"><span data-stu-id="9190b-176">An integer</span></span>
- <span data-ttu-id="9190b-177">Un intervallo di numeri interi compresi tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="9190b-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="9190b-178">Carattere jolly (\*) che corrisponde a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="9190b-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="9190b-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9190b-179">CommonParameters</span></span>
<span data-ttu-id="9190b-180">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9190b-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9190b-181">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9190b-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9190b-182">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9190b-182">INPUTS</span></span>

### <span data-ttu-id="9190b-183">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9190b-183">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="9190b-184">Il parametro ' NetworkSecurityGroup ' accetta il valore di tipo ' PSNetworkSecurityGroup ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="9190b-184">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="9190b-185">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9190b-185">OUTPUTS</span></span>

### <span data-ttu-id="9190b-186">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9190b-186">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="9190b-187">Note</span><span class="sxs-lookup"><span data-stu-id="9190b-187">NOTES</span></span>

## <span data-ttu-id="9190b-188">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9190b-188">RELATED LINKS</span></span>

[<span data-ttu-id="9190b-189">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9190b-189">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9190b-190">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9190b-190">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9190b-191">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9190b-191">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9190b-192">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9190b-192">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

