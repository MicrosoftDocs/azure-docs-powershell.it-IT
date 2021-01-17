---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 42f92e7f90e5349c116f8a6ed948ed7a29a35ad2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486568"
---
# <span data-ttu-id="cef8f-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cef8f-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="cef8f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cef8f-102">SYNOPSIS</span></span>
<span data-ttu-id="cef8f-103">Aggiorna una configurazione della regola di sicurezza di rete per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="cef8f-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="cef8f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cef8f-104">SYNTAX</span></span>

### <span data-ttu-id="cef8f-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cef8f-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cef8f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cef8f-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cef8f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cef8f-107">DESCRIPTION</span></span>
<span data-ttu-id="cef8f-108">Il cmdlet **set-AzNetworkSecurityRuleConfig** aggiorna una configurazione della regola di sicurezza di rete per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="cef8f-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="cef8f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cef8f-109">EXAMPLES</span></span>

### <span data-ttu-id="cef8f-110">Esempio 1: modificare la configurazione di Access in una regola di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="cef8f-110">Example 1: Change the access configuration in a network security rule</span></span>
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="cef8f-111">Il primo comando ottiene il gruppo di sicurezza di rete denominato NSG-FrontEnd e lo archivia nella variabile $nsg.</span><span class="sxs-lookup"><span data-stu-id="cef8f-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="cef8f-112">Il secondo comando usa l'operatore pipeline per passare il gruppo di sicurezza in $nsg a Get-AzNetworkSecurityRuleConfig, che ottiene la configurazione della regola di sicurezza denominata RDP-Rule.</span><span class="sxs-lookup"><span data-stu-id="cef8f-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="cef8f-113">Il terzo comando modifica la configurazione di Access di RDP-Rule in Deny.</span><span class="sxs-lookup"><span data-stu-id="cef8f-113">The third command changes the access configuration of rdp-rule to Deny.</span></span>

### <span data-ttu-id="cef8f-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cef8f-114">Example 2</span></span>

<span data-ttu-id="cef8f-115">Aggiorna una configurazione della regola di sicurezza di rete per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="cef8f-115">Updates a network security rule configuration for a network security group.</span></span> <span data-ttu-id="cef8f-116">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="cef8f-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## <span data-ttu-id="cef8f-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cef8f-117">PARAMETERS</span></span>

### <span data-ttu-id="cef8f-118">-Access</span><span class="sxs-lookup"><span data-stu-id="cef8f-118">-Access</span></span>
<span data-ttu-id="cef8f-119">Specifica se il traffico di rete è consentito o negato.</span><span class="sxs-lookup"><span data-stu-id="cef8f-119">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="cef8f-120">I valori accettabili per questo parametro sono: Allow e Deny.</span><span class="sxs-lookup"><span data-stu-id="cef8f-120">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="cef8f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef8f-121">-DefaultProfile</span></span>
<span data-ttu-id="cef8f-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cef8f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cef8f-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="cef8f-123">-Description</span></span>
<span data-ttu-id="cef8f-124">Specifica una descrizione per una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="cef8f-124">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="cef8f-125">La dimensione massima è di 140 caratteri.</span><span class="sxs-lookup"><span data-stu-id="cef8f-125">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="cef8f-126">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="cef8f-126">-DestinationAddressPrefix</span></span>
<span data-ttu-id="cef8f-127">Specifica un prefisso per l'indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cef8f-127">Specifies a destination address prefix.</span></span>
<span data-ttu-id="cef8f-128">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="cef8f-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cef8f-129">Un indirizzo CIDR (classe Interdomain Routing)</span><span class="sxs-lookup"><span data-stu-id="cef8f-129">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="cef8f-130">Un intervallo di indirizzi IP di destinazione</span><span class="sxs-lookup"><span data-stu-id="cef8f-130">A destination IP address range</span></span> 
- <span data-ttu-id="cef8f-131">Un carattere jolly (\*) in modo che corrisponda a qualsiasi indirizzo IP, è possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="cef8f-131">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="cef8f-132">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cef8f-132">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="cef8f-133">Gruppo di sicurezza dell'applicazione impostato come destinazione per la regola.</span><span class="sxs-lookup"><span data-stu-id="cef8f-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="cef8f-134">Non può essere usato con il parametro "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="cef8f-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="cef8f-135">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="cef8f-135">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="cef8f-136">Gruppo di sicurezza dell'applicazione impostato come destinazione per la regola.</span><span class="sxs-lookup"><span data-stu-id="cef8f-136">The application security group set as destination for the rule.</span></span> <span data-ttu-id="cef8f-137">Non può essere usato con il parametro "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="cef8f-137">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="cef8f-138">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="cef8f-138">-DestinationPortRange</span></span>
<span data-ttu-id="cef8f-139">Specifica una porta o un intervallo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cef8f-139">Specifies a destination port or range.</span></span>
<span data-ttu-id="cef8f-140">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="cef8f-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cef8f-141">Un numero intero</span><span class="sxs-lookup"><span data-stu-id="cef8f-141">An integer</span></span> 
- <span data-ttu-id="cef8f-142">Un intervallo di numeri interi compresi tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="cef8f-142">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="cef8f-143">Carattere jolly (\*) che corrisponde a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="cef8f-143">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="cef8f-144">-Direzione</span><span class="sxs-lookup"><span data-stu-id="cef8f-144">-Direction</span></span>
<span data-ttu-id="cef8f-145">Specifica se una regola viene valutata per il traffico in entrata o in uscita.</span><span class="sxs-lookup"><span data-stu-id="cef8f-145">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="cef8f-146">I valori accettabili per questo parametro sono: in ingresso e in uscita.</span><span class="sxs-lookup"><span data-stu-id="cef8f-146">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="cef8f-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="cef8f-147">-Name</span></span>
<span data-ttu-id="cef8f-148">Specifica il nome della configurazione della regola di sicurezza della rete impostata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cef8f-148">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="cef8f-149">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cef8f-149">-NetworkSecurityGroup</span></span>
<span data-ttu-id="cef8f-150">Specifica l'oggetto **NetworkSecurityGroup** che contiene la configurazione della regola di sicurezza della rete da impostare.</span><span class="sxs-lookup"><span data-stu-id="cef8f-150">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="cef8f-151">-Priorità</span><span class="sxs-lookup"><span data-stu-id="cef8f-151">-Priority</span></span>
<span data-ttu-id="cef8f-152">Specifica la priorità di una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="cef8f-152">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="cef8f-153">I valori accettabili per questo parametro sono: un numero intero compreso tra 100 e 4096.</span><span class="sxs-lookup"><span data-stu-id="cef8f-153">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="cef8f-154">Il numero di priorità deve essere univoco per ogni regola della raccolta.</span><span class="sxs-lookup"><span data-stu-id="cef8f-154">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="cef8f-155">Minore è il numero di priorità, maggiore è la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="cef8f-155">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="cef8f-156">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="cef8f-156">-Protocol</span></span>
<span data-ttu-id="cef8f-157">Specifica il protocollo di rete a cui si applica una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="cef8f-157">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="cef8f-158">I valori accettabili per questo parametro sono:--TCP</span><span class="sxs-lookup"><span data-stu-id="cef8f-158">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="cef8f-159">UDP</span><span class="sxs-lookup"><span data-stu-id="cef8f-159">Udp</span></span>
- <span data-ttu-id="cef8f-160">Carattere jolly (\*) in modo che corrisponda a entrambi</span><span class="sxs-lookup"><span data-stu-id="cef8f-160">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="cef8f-161">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="cef8f-161">-SourceAddressPrefix</span></span>
<span data-ttu-id="cef8f-162">Specifica un prefisso per l'indirizzo di origine.</span><span class="sxs-lookup"><span data-stu-id="cef8f-162">Specifies a source address prefix.</span></span>
<span data-ttu-id="cef8f-163">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="cef8f-163">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cef8f-164">UN CIDR</span><span class="sxs-lookup"><span data-stu-id="cef8f-164">A CIDR</span></span>
- <span data-ttu-id="cef8f-165">Un intervallo IP di origine</span><span class="sxs-lookup"><span data-stu-id="cef8f-165">A source IP range</span></span>
- <span data-ttu-id="cef8f-166">Un carattere jolly (\*) in modo che corrisponda a qualsiasi indirizzo IP è anche possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="cef8f-166">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="cef8f-167">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cef8f-167">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="cef8f-168">Gruppo di sicurezza dell'applicazione impostato come origine per la regola.</span><span class="sxs-lookup"><span data-stu-id="cef8f-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="cef8f-169">Non può essere usato con il parametro "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="cef8f-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="cef8f-170">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="cef8f-170">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="cef8f-171">Gruppo di sicurezza dell'applicazione impostato come origine per la regola.</span><span class="sxs-lookup"><span data-stu-id="cef8f-171">The application security group set as source for the rule.</span></span> <span data-ttu-id="cef8f-172">Non può essere usato con il parametro "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="cef8f-172">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="cef8f-173">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="cef8f-173">-SourcePortRange</span></span>
<span data-ttu-id="cef8f-174">Specifica la porta o l'intervallo di origine.</span><span class="sxs-lookup"><span data-stu-id="cef8f-174">Specifies the source port or range.</span></span>
<span data-ttu-id="cef8f-175">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="cef8f-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cef8f-176">Un numero intero</span><span class="sxs-lookup"><span data-stu-id="cef8f-176">An integer</span></span>
- <span data-ttu-id="cef8f-177">Un intervallo di numeri interi compresi tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="cef8f-177">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="cef8f-178">Carattere jolly (\*) che corrisponde a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="cef8f-178">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="cef8f-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef8f-179">CommonParameters</span></span>
<span data-ttu-id="cef8f-180">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cef8f-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef8f-181">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cef8f-181">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef8f-182">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cef8f-182">INPUTS</span></span>

### <span data-ttu-id="cef8f-183">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cef8f-183">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="cef8f-184">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cef8f-184">OUTPUTS</span></span>

### <span data-ttu-id="cef8f-185">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cef8f-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="cef8f-186">Note</span><span class="sxs-lookup"><span data-stu-id="cef8f-186">NOTES</span></span>

## <span data-ttu-id="cef8f-187">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cef8f-187">RELATED LINKS</span></span>

[<span data-ttu-id="cef8f-188">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cef8f-188">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="cef8f-189">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cef8f-189">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="cef8f-190">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cef8f-190">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="cef8f-191">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cef8f-191">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


