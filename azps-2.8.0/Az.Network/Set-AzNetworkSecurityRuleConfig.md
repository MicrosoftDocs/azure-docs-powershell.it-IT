---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 4293f044a270a43f12c7b4d74a410a324d0284dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852570"
---
# <span data-ttu-id="e7f9a-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e7f9a-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="e7f9a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e7f9a-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f9a-103">Aggiorna una configurazione della regola di sicurezza di rete per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="e7f9a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e7f9a-104">SYNTAX</span></span>

### <span data-ttu-id="e7f9a-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e7f9a-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7f9a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e7f9a-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7f9a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7f9a-107">DESCRIPTION</span></span>
<span data-ttu-id="e7f9a-108">Il cmdlet **set-AzNetworkSecurityRuleConfig** aggiorna una configurazione della regola di sicurezza di rete per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="e7f9a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e7f9a-109">EXAMPLES</span></span>

### <span data-ttu-id="e7f9a-110">Esempio 1: modificare la configurazione di Access in una regola di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="e7f9a-110">Example 1: Change the access configuration in a network security rule</span></span>
```
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="e7f9a-111">Il primo comando ottiene il gruppo di sicurezza di rete denominato NSG-FrontEnd e lo archivia nella variabile $nsg.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="e7f9a-112">Il secondo comando usa l'operatore pipeline per passare il gruppo di sicurezza in $nsg a Get-AzNetworkSecurityRuleConfig, che ottiene la configurazione della regola di sicurezza denominata RDP-Rule.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="e7f9a-113">Il terzo comando modifica la configurazione di Access di RDP-Rule in Deny.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

## <span data-ttu-id="e7f9a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e7f9a-114">PARAMETERS</span></span>

### <span data-ttu-id="e7f9a-115">-Access</span><span class="sxs-lookup"><span data-stu-id="e7f9a-115">-Access</span></span>
<span data-ttu-id="e7f9a-116">Specifica se il traffico di rete è consentito o negato.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-116">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="e7f9a-117">I valori accettabili per questo parametro sono: Allow e Deny.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f9a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f9a-118">-DefaultProfile</span></span>
<span data-ttu-id="e7f9a-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7f9a-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7f9a-120">-Description</span></span>
<span data-ttu-id="e7f9a-121">Specifica una descrizione per una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-121">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="e7f9a-122">La dimensione massima è di 140 caratteri.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-122">The maximum size is 140 characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f9a-123">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e7f9a-123">-DestinationAddressPrefix</span></span>
<span data-ttu-id="e7f9a-124">Specifica un prefisso per l'indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-124">Specifies a destination address prefix.</span></span>
<span data-ttu-id="e7f9a-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e7f9a-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e7f9a-126">Un indirizzo CIDR (classe Interdomain Routing)</span><span class="sxs-lookup"><span data-stu-id="e7f9a-126">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="e7f9a-127">Un intervallo di indirizzi IP di destinazione</span><span class="sxs-lookup"><span data-stu-id="e7f9a-127">A destination IP address range</span></span> 
- <span data-ttu-id="e7f9a-128">Un carattere jolly (\*) in modo che corrisponda a qualsiasi indirizzo IP, è possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-128">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="e7f9a-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e7f9a-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="e7f9a-130">Gruppo di sicurezza dell'applicazione impostato come destinazione per la regola.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="e7f9a-131">Non può essere usato con il parametro "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="e7f9a-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f9a-132">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="e7f9a-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="e7f9a-133">Gruppo di sicurezza dell'applicazione impostato come destinazione per la regola.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="e7f9a-134">Non può essere usato con il parametro "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="e7f9a-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f9a-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="e7f9a-135">-DestinationPortRange</span></span>
<span data-ttu-id="e7f9a-136">Specifica una porta o un intervallo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="e7f9a-137">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e7f9a-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e7f9a-138">Un numero intero</span><span class="sxs-lookup"><span data-stu-id="e7f9a-138">An integer</span></span> 
- <span data-ttu-id="e7f9a-139">Un intervallo di numeri interi compresi tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="e7f9a-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="e7f9a-140">Carattere jolly (\*) che corrisponde a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="e7f9a-140">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="e7f9a-141">-Direzione</span><span class="sxs-lookup"><span data-stu-id="e7f9a-141">-Direction</span></span>
<span data-ttu-id="e7f9a-142">Specifica se una regola viene valutata per il traffico in entrata o in uscita.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-142">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="e7f9a-143">I valori accettabili per questo parametro sono: in ingresso e in uscita.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f9a-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="e7f9a-144">-Name</span></span>
<span data-ttu-id="e7f9a-145">Specifica il nome della configurazione della regola di sicurezza della rete impostata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-145">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f9a-146">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e7f9a-146">-NetworkSecurityGroup</span></span>
<span data-ttu-id="e7f9a-147">Specifica l'oggetto **NetworkSecurityGroup** che contiene la configurazione della regola di sicurezza della rete da impostare.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-147">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7f9a-148">-Priorità</span><span class="sxs-lookup"><span data-stu-id="e7f9a-148">-Priority</span></span>
<span data-ttu-id="e7f9a-149">Specifica la priorità di una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-149">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="e7f9a-150">I valori accettabili per questo parametro sono: un numero intero compreso tra 100 e 4096.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-150">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="e7f9a-151">Il numero di priorità deve essere univoco per ogni regola della raccolta.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-151">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="e7f9a-152">Minore è il numero di priorità, maggiore è la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-152">The lower the priority number, the higher the priority of the rule.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f9a-153">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="e7f9a-153">-Protocol</span></span>
<span data-ttu-id="e7f9a-154">Specifica il protocollo di rete a cui si applica una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-154">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="e7f9a-155">I valori accettabili per questo parametro sono:--TCP</span><span class="sxs-lookup"><span data-stu-id="e7f9a-155">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="e7f9a-156">UDP</span><span class="sxs-lookup"><span data-stu-id="e7f9a-156">Udp</span></span>
- <span data-ttu-id="e7f9a-157">Carattere jolly (\*) in modo che corrisponda a entrambi</span><span class="sxs-lookup"><span data-stu-id="e7f9a-157">A wildcard character (\*) to match both</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Tcp, Udp, *

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f9a-158">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e7f9a-158">-SourceAddressPrefix</span></span>
<span data-ttu-id="e7f9a-159">Specifica un prefisso per l'indirizzo di origine.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-159">Specifies a source address prefix.</span></span>
<span data-ttu-id="e7f9a-160">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e7f9a-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e7f9a-161">UN CIDR</span><span class="sxs-lookup"><span data-stu-id="e7f9a-161">A CIDR</span></span>
- <span data-ttu-id="e7f9a-162">Un intervallo IP di origine</span><span class="sxs-lookup"><span data-stu-id="e7f9a-162">A source IP range</span></span>
- <span data-ttu-id="e7f9a-163">Un carattere jolly (\*) in modo che corrisponda a qualsiasi indirizzo IP è anche possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-163">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="e7f9a-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e7f9a-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="e7f9a-165">Gruppo di sicurezza dell'applicazione impostato come origine per la regola.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="e7f9a-166">Non può essere usato con il parametro "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="e7f9a-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f9a-167">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="e7f9a-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="e7f9a-168">Gruppo di sicurezza dell'applicazione impostato come origine per la regola.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="e7f9a-169">Non può essere usato con il parametro "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="e7f9a-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f9a-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="e7f9a-170">-SourcePortRange</span></span>
<span data-ttu-id="e7f9a-171">Specifica la porta o l'intervallo di origine.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-171">Specifies the source port or range.</span></span>
<span data-ttu-id="e7f9a-172">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e7f9a-172">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e7f9a-173">Un numero intero</span><span class="sxs-lookup"><span data-stu-id="e7f9a-173">An integer</span></span>
- <span data-ttu-id="e7f9a-174">Un intervallo di numeri interi compresi tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="e7f9a-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="e7f9a-175">Carattere jolly (\*) che corrisponde a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="e7f9a-175">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="e7f9a-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f9a-176">CommonParameters</span></span>
<span data-ttu-id="e7f9a-177">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7f9a-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f9a-178">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7f9a-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f9a-179">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e7f9a-179">INPUTS</span></span>

### <span data-ttu-id="e7f9a-180">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e7f9a-180">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="e7f9a-181">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e7f9a-181">OUTPUTS</span></span>

### <span data-ttu-id="e7f9a-182">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e7f9a-182">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="e7f9a-183">Note</span><span class="sxs-lookup"><span data-stu-id="e7f9a-183">NOTES</span></span>

## <span data-ttu-id="e7f9a-184">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e7f9a-184">RELATED LINKS</span></span>

[<span data-ttu-id="e7f9a-185">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e7f9a-185">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e7f9a-186">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e7f9a-186">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e7f9a-187">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e7f9a-187">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="e7f9a-188">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e7f9a-188">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


