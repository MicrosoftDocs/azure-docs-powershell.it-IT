---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 42f92e7f90e5349c116f8a6ed948ed7a29a35ad2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200198"
---
# <span data-ttu-id="c4536-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4536-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="c4536-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c4536-102">SYNOPSIS</span></span>
<span data-ttu-id="c4536-103">Aggiorna una configurazione della regola di sicurezza di rete per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="c4536-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="c4536-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4536-104">SYNTAX</span></span>

### <span data-ttu-id="c4536-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c4536-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4536-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c4536-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4536-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4536-107">DESCRIPTION</span></span>
<span data-ttu-id="c4536-108">Il cmdlet **set-AzNetworkSecurityRuleConfig** aggiorna una configurazione della regola di sicurezza di rete per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="c4536-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="c4536-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4536-109">EXAMPLES</span></span>

### <span data-ttu-id="c4536-110">Esempio 1: modificare la configurazione di Access in una regola di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="c4536-110">Example 1: Change the access configuration in a network security rule</span></span>
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="c4536-111">Il primo comando ottiene il gruppo di sicurezza di rete denominato NSG-FrontEnd e lo archivia nella variabile $nsg.</span><span class="sxs-lookup"><span data-stu-id="c4536-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="c4536-112">Il secondo comando usa l'operatore pipeline per passare il gruppo di sicurezza in $nsg a Get-AzNetworkSecurityRuleConfig, che ottiene la configurazione della regola di sicurezza denominata RDP-Rule.</span><span class="sxs-lookup"><span data-stu-id="c4536-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="c4536-113">Il terzo comando modifica la configurazione di Access di RDP-Rule in Deny.</span><span class="sxs-lookup"><span data-stu-id="c4536-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

### <span data-ttu-id="c4536-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c4536-114">Example 2</span></span>

<span data-ttu-id="c4536-115">Aggiorna una configurazione della regola di sicurezza di rete per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="c4536-115">Updates a network security rule configuration for a network security group.</span></span> <span data-ttu-id="c4536-116">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="c4536-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## <span data-ttu-id="c4536-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c4536-117">PARAMETERS</span></span>

### <span data-ttu-id="c4536-118">-Access</span><span class="sxs-lookup"><span data-stu-id="c4536-118">-Access</span></span>
<span data-ttu-id="c4536-119">Specifica se il traffico di rete è consentito o negato.</span><span class="sxs-lookup"><span data-stu-id="c4536-119">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="c4536-120">I valori accettabili per questo parametro sono: Allow e Deny.</span><span class="sxs-lookup"><span data-stu-id="c4536-120">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="c4536-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4536-121">-DefaultProfile</span></span>
<span data-ttu-id="c4536-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c4536-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4536-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4536-123">-Description</span></span>
<span data-ttu-id="c4536-124">Specifica una descrizione per una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="c4536-124">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="c4536-125">La dimensione massima è di 140 caratteri.</span><span class="sxs-lookup"><span data-stu-id="c4536-125">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="c4536-126">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c4536-126">-DestinationAddressPrefix</span></span>
<span data-ttu-id="c4536-127">Specifica un prefisso per l'indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c4536-127">Specifies a destination address prefix.</span></span>
<span data-ttu-id="c4536-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c4536-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c4536-129">Un indirizzo CIDR (classe Interdomain Routing)</span><span class="sxs-lookup"><span data-stu-id="c4536-129">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="c4536-130">Un intervallo di indirizzi IP di destinazione</span><span class="sxs-lookup"><span data-stu-id="c4536-130">A destination IP address range</span></span> 
- <span data-ttu-id="c4536-131">Un carattere jolly (\*) in modo che corrisponda a qualsiasi indirizzo IP, è possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="c4536-131">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="c4536-132">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c4536-132">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="c4536-133">Gruppo di sicurezza dell'applicazione impostato come destinazione per la regola.</span><span class="sxs-lookup"><span data-stu-id="c4536-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="c4536-134">Non può essere usato con il parametro "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="c4536-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="c4536-135">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="c4536-135">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="c4536-136">Gruppo di sicurezza dell'applicazione impostato come destinazione per la regola.</span><span class="sxs-lookup"><span data-stu-id="c4536-136">The application security group set as destination for the rule.</span></span> <span data-ttu-id="c4536-137">Non può essere usato con il parametro "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="c4536-137">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="c4536-138">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="c4536-138">-DestinationPortRange</span></span>
<span data-ttu-id="c4536-139">Specifica una porta o un intervallo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c4536-139">Specifies a destination port or range.</span></span>
<span data-ttu-id="c4536-140">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c4536-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c4536-141">Un numero intero</span><span class="sxs-lookup"><span data-stu-id="c4536-141">An integer</span></span> 
- <span data-ttu-id="c4536-142">Un intervallo di numeri interi compresi tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="c4536-142">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="c4536-143">Carattere jolly (\*) che corrisponde a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="c4536-143">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="c4536-144">-Direzione</span><span class="sxs-lookup"><span data-stu-id="c4536-144">-Direction</span></span>
<span data-ttu-id="c4536-145">Specifica se una regola viene valutata per il traffico in entrata o in uscita.</span><span class="sxs-lookup"><span data-stu-id="c4536-145">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="c4536-146">I valori accettabili per questo parametro sono: in ingresso e in uscita.</span><span class="sxs-lookup"><span data-stu-id="c4536-146">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="c4536-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="c4536-147">-Name</span></span>
<span data-ttu-id="c4536-148">Specifica il nome della configurazione della regola di sicurezza della rete impostata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4536-148">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="c4536-149">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c4536-149">-NetworkSecurityGroup</span></span>
<span data-ttu-id="c4536-150">Specifica l'oggetto **NetworkSecurityGroup** che contiene la configurazione della regola di sicurezza della rete da impostare.</span><span class="sxs-lookup"><span data-stu-id="c4536-150">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="c4536-151">-Priorità</span><span class="sxs-lookup"><span data-stu-id="c4536-151">-Priority</span></span>
<span data-ttu-id="c4536-152">Specifica la priorità di una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="c4536-152">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="c4536-153">I valori accettabili per questo parametro sono: un numero intero compreso tra 100 e 4096.</span><span class="sxs-lookup"><span data-stu-id="c4536-153">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="c4536-154">Il numero di priorità deve essere univoco per ogni regola della raccolta.</span><span class="sxs-lookup"><span data-stu-id="c4536-154">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="c4536-155">Minore è il numero di priorità, maggiore è la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="c4536-155">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="c4536-156">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="c4536-156">-Protocol</span></span>
<span data-ttu-id="c4536-157">Specifica il protocollo di rete a cui si applica una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="c4536-157">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="c4536-158">I valori accettabili per questo parametro sono:--TCP</span><span class="sxs-lookup"><span data-stu-id="c4536-158">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="c4536-159">UDP</span><span class="sxs-lookup"><span data-stu-id="c4536-159">Udp</span></span>
- <span data-ttu-id="c4536-160">Carattere jolly (\*) in modo che corrisponda a entrambi</span><span class="sxs-lookup"><span data-stu-id="c4536-160">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="c4536-161">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c4536-161">-SourceAddressPrefix</span></span>
<span data-ttu-id="c4536-162">Specifica un prefisso per l'indirizzo di origine.</span><span class="sxs-lookup"><span data-stu-id="c4536-162">Specifies a source address prefix.</span></span>
<span data-ttu-id="c4536-163">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c4536-163">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c4536-164">UN CIDR</span><span class="sxs-lookup"><span data-stu-id="c4536-164">A CIDR</span></span>
- <span data-ttu-id="c4536-165">Un intervallo IP di origine</span><span class="sxs-lookup"><span data-stu-id="c4536-165">A source IP range</span></span>
- <span data-ttu-id="c4536-166">Un carattere jolly (\*) in modo che corrisponda a qualsiasi indirizzo IP è anche possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="c4536-166">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="c4536-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c4536-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="c4536-168">Gruppo di sicurezza dell'applicazione impostato come origine per la regola.</span><span class="sxs-lookup"><span data-stu-id="c4536-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="c4536-169">Non può essere usato con il parametro "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="c4536-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="c4536-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="c4536-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="c4536-171">Gruppo di sicurezza dell'applicazione impostato come origine per la regola.</span><span class="sxs-lookup"><span data-stu-id="c4536-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="c4536-172">Non può essere usato con il parametro "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="c4536-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="c4536-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="c4536-173">-SourcePortRange</span></span>
<span data-ttu-id="c4536-174">Specifica la porta o l'intervallo di origine.</span><span class="sxs-lookup"><span data-stu-id="c4536-174">Specifies the source port or range.</span></span>
<span data-ttu-id="c4536-175">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c4536-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c4536-176">Un numero intero</span><span class="sxs-lookup"><span data-stu-id="c4536-176">An integer</span></span>
- <span data-ttu-id="c4536-177">Un intervallo di numeri interi compresi tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="c4536-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="c4536-178">Carattere jolly (\*) che corrisponde a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="c4536-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="c4536-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4536-179">CommonParameters</span></span>
<span data-ttu-id="c4536-180">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4536-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4536-181">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4536-181">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4536-182">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c4536-182">INPUTS</span></span>

### <span data-ttu-id="c4536-183">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c4536-183">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="c4536-184">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4536-184">OUTPUTS</span></span>

### <span data-ttu-id="c4536-185">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c4536-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="c4536-186">Note</span><span class="sxs-lookup"><span data-stu-id="c4536-186">NOTES</span></span>

## <span data-ttu-id="c4536-187">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4536-187">RELATED LINKS</span></span>

[<span data-ttu-id="c4536-188">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4536-188">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c4536-189">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4536-189">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c4536-190">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4536-190">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c4536-191">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4536-191">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

