---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EFFFF43-501E-4955-A4EE-2C09B8863B30
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 12967d69e1886b6446db906e5822fd10bbad0037
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003277"
---
# <span data-ttu-id="7290a-101">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7290a-101">Set-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="7290a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7290a-102">SYNOPSIS</span></span>
<span data-ttu-id="7290a-103">Aggiorna la configurazione di una regola di sicurezza di rete per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="7290a-103">Updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="7290a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7290a-104">SYNTAX</span></span>

### <span data-ttu-id="7290a-105">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="7290a-105">SetByResource (Default)</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7290a-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7290a-106">SetByResourceId</span></span>
```
Set-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7290a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7290a-107">DESCRIPTION</span></span>
<span data-ttu-id="7290a-108">Il cmdlet **Set-AzNetworkSecurityRuleConfig aggiorna** la configurazione di una regola di sicurezza di rete per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="7290a-108">The **Set-AzNetworkSecurityRuleConfig** cmdlet updates a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="7290a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7290a-109">EXAMPLES</span></span>

### <span data-ttu-id="7290a-110">Esempio 1: Modificare la configurazione di accesso in una regola di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="7290a-110">Example 1: Change the access configuration in a network security rule</span></span>
```powershell
PS C:\>$nsg = Get-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
PS C:\> $nsg | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
PS C:\> Set-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg -Access "Deny"
```

<span data-ttu-id="7290a-111">Il primo comando ottiene il gruppo di sicurezza di rete denominato NSG-FrontEnd e quindi lo archivia nella variabile $nsg.</span><span class="sxs-lookup"><span data-stu-id="7290a-111">The first command gets the network security group named NSG-FrontEnd, and then stores it in the variable $nsg.</span></span>
<span data-ttu-id="7290a-112">Il secondo comando usa l'operatore della pipeline per passare il gruppo di sicurezza in $nsg a Get-AzNetworkSecurityRuleConfig, che ottiene la configurazione della regola di sicurezza denominata rdp-rule.</span><span class="sxs-lookup"><span data-stu-id="7290a-112">The second command uses the pipeline operator to pass the security group in $nsg to Get-AzNetworkSecurityRuleConfig, which gets the security rule configuration named rdp-rule.</span></span>
<span data-ttu-id="7290a-113">Il terzo comando modifica la configurazione di accesso di rdp-rule in Nega.</span><span class="sxs-lookup"><span data-stu-id="7290a-113">The third command changes the access configuration of rdp-rule to Deny.</span></span> <span data-ttu-id="7290a-114">Questa operazione, tuttavia, sovrascrive la regola e imposta solo i parametri passati alla Set-AzNetworkSecurityRuleConfig funzione.</span><span class="sxs-lookup"><span data-stu-id="7290a-114">However, this overwrites the rule and only sets the parameters that are passed to the Set-AzNetworkSecurityRuleConfig function.</span></span>   <span data-ttu-id="7290a-115">NOTA: non è possibile modificare un singolo attributo</span><span class="sxs-lookup"><span data-stu-id="7290a-115">NOTE: There is no way to change a single attribute</span></span>

### <span data-ttu-id="7290a-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7290a-116">Example 2</span></span>

<span data-ttu-id="7290a-117">Aggiorna la configurazione di una regola di sicurezza di rete per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="7290a-117">Updates a network security rule configuration for a network security group.</span></span> <span data-ttu-id="7290a-118">(autogenerati)</span><span class="sxs-lookup"><span data-stu-id="7290a-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNetworkSecurityRuleConfig -Access Allow -DestinationAddressPrefix * -DestinationPortRange 3389 -Direction Inbound -Name 'rdp-rule' -NetworkSecurityGroup <PSNetworkSecurityGroup> -Priority 1 -Protocol Tcp -SourceAddressPrefix 'Internet' -SourcePortRange *
```

## <span data-ttu-id="7290a-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7290a-119">PARAMETERS</span></span>

### <span data-ttu-id="7290a-120">-Access</span><span class="sxs-lookup"><span data-stu-id="7290a-120">-Access</span></span>
<span data-ttu-id="7290a-121">Specifica se il traffico di rete è consentito o negato.</span><span class="sxs-lookup"><span data-stu-id="7290a-121">Specifies whether network traffic is allowed or denied.</span></span> <span data-ttu-id="7290a-122">I valori accettabili per questo parametro sono: Allow e Deny.</span><span class="sxs-lookup"><span data-stu-id="7290a-122">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="7290a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7290a-123">-DefaultProfile</span></span>
<span data-ttu-id="7290a-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7290a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7290a-125">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="7290a-125">-Description</span></span>
<span data-ttu-id="7290a-126">Specifica una descrizione per la configurazione di una regola.</span><span class="sxs-lookup"><span data-stu-id="7290a-126">Specifies a description for a rule configuration.</span></span>
<span data-ttu-id="7290a-127">La dimensione massima è 140 caratteri.</span><span class="sxs-lookup"><span data-stu-id="7290a-127">The maximum size is 140 characters.</span></span>

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

### <span data-ttu-id="7290a-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7290a-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="7290a-129">Specifica un prefisso di indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7290a-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="7290a-130">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="7290a-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7290a-131">Indirizzo Classless Interdomain Routing (CIDR)</span><span class="sxs-lookup"><span data-stu-id="7290a-131">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="7290a-132">Un intervallo di indirizzi IP di destinazione</span><span class="sxs-lookup"><span data-stu-id="7290a-132">A destination IP address range</span></span> 
- <span data-ttu-id="7290a-133">Un carattere jolly (\*) che corrisponda a qualsiasi indirizzo IP È possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="7290a-133">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="7290a-134">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7290a-134">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="7290a-135">Gruppo di sicurezza dell'applicazione impostato come destinazione della regola.</span><span class="sxs-lookup"><span data-stu-id="7290a-135">The application security group set as destination for the rule.</span></span> <span data-ttu-id="7290a-136">Non può essere usato con il parametro 'DestinationAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="7290a-136">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="7290a-137">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="7290a-137">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="7290a-138">Gruppo di sicurezza dell'applicazione impostato come destinazione della regola.</span><span class="sxs-lookup"><span data-stu-id="7290a-138">The application security group set as destination for the rule.</span></span> <span data-ttu-id="7290a-139">Non può essere usato con il parametro 'DestinationAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="7290a-139">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="7290a-140">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="7290a-140">-DestinationPortRange</span></span>
<span data-ttu-id="7290a-141">Specifica una porta o un intervallo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7290a-141">Specifies a destination port or range.</span></span>
<span data-ttu-id="7290a-142">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="7290a-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7290a-143">Un numero intero</span><span class="sxs-lookup"><span data-stu-id="7290a-143">An integer</span></span> 
- <span data-ttu-id="7290a-144">Intervallo di interi compreso tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="7290a-144">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="7290a-145">Un carattere jolly (\*) che corrisponda a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="7290a-145">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="7290a-146">-Direction</span><span class="sxs-lookup"><span data-stu-id="7290a-146">-Direction</span></span>
<span data-ttu-id="7290a-147">Specifica se una regola viene valutata per il traffico in arrivo o in uscita.</span><span class="sxs-lookup"><span data-stu-id="7290a-147">Specifies whether a rule is evaluated for incoming or outgoing traffic.</span></span>
<span data-ttu-id="7290a-148">I valori accettabili per questo parametro sono: in ingresso e in uscita.</span><span class="sxs-lookup"><span data-stu-id="7290a-148">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="7290a-149">-Name</span><span class="sxs-lookup"><span data-stu-id="7290a-149">-Name</span></span>
<span data-ttu-id="7290a-150">Specifica il nome della configurazione della regola di sicurezza di rete impostata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7290a-150">Specifies the name of the network security rule configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="7290a-151">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7290a-151">-NetworkSecurityGroup</span></span>
<span data-ttu-id="7290a-152">Specifica **l'oggetto NetworkSecurityGroup** che contiene la configurazione della regola di sicurezza di rete da impostare.</span><span class="sxs-lookup"><span data-stu-id="7290a-152">Specifies the **NetworkSecurityGroup** object that contains the network security rule configuration to set.</span></span>

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

### <span data-ttu-id="7290a-153">-Priority</span><span class="sxs-lookup"><span data-stu-id="7290a-153">-Priority</span></span>
<span data-ttu-id="7290a-154">Specifica la priorità di una configurazione delle regole.</span><span class="sxs-lookup"><span data-stu-id="7290a-154">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="7290a-155">I valori accettabili per questo parametro sono:un numero intero compreso tra 100 e 4096.</span><span class="sxs-lookup"><span data-stu-id="7290a-155">The acceptable values for this parameter are:An integer between 100 and 4096.</span></span>
<span data-ttu-id="7290a-156">Il numero di priorità deve essere univoco per ogni regola della raccolta.</span><span class="sxs-lookup"><span data-stu-id="7290a-156">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="7290a-157">Più basso è il numero di priorità, più alta sarà la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="7290a-157">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="7290a-158">-Protocol</span><span class="sxs-lookup"><span data-stu-id="7290a-158">-Protocol</span></span>
<span data-ttu-id="7290a-159">Specifica il protocollo di rete a cui si applica una configurazione delle regole.</span><span class="sxs-lookup"><span data-stu-id="7290a-159">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="7290a-160">I valori accettabili per questo parametro sono: --Tcp</span><span class="sxs-lookup"><span data-stu-id="7290a-160">The acceptable values for this parameter are: --Tcp</span></span>
- <span data-ttu-id="7290a-161">Udp</span><span class="sxs-lookup"><span data-stu-id="7290a-161">Udp</span></span>
- <span data-ttu-id="7290a-162">Un carattere jolly (\*) che corrisponda a entrambi</span><span class="sxs-lookup"><span data-stu-id="7290a-162">A wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="7290a-163">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7290a-163">-SourceAddressPrefix</span></span>
<span data-ttu-id="7290a-164">Specifica un prefisso dell'indirizzo di origine.</span><span class="sxs-lookup"><span data-stu-id="7290a-164">Specifies a source address prefix.</span></span>
<span data-ttu-id="7290a-165">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="7290a-165">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7290a-166">UN CIDR</span><span class="sxs-lookup"><span data-stu-id="7290a-166">A CIDR</span></span>
- <span data-ttu-id="7290a-167">Un intervallo IP di origine</span><span class="sxs-lookup"><span data-stu-id="7290a-167">A source IP range</span></span>
- <span data-ttu-id="7290a-168">Un carattere jolly (\*) che corrisponda a qualsiasi indirizzo IP È anche possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="7290a-168">A wildcard character (\*) to match any IP address You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="7290a-169">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7290a-169">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="7290a-170">Gruppo di sicurezza dell'applicazione impostato come origine della regola.</span><span class="sxs-lookup"><span data-stu-id="7290a-170">The application security group set as source for the rule.</span></span> <span data-ttu-id="7290a-171">Non può essere usato con il parametro 'SourceAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="7290a-171">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="7290a-172">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="7290a-172">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="7290a-173">Gruppo di sicurezza dell'applicazione impostato come origine della regola.</span><span class="sxs-lookup"><span data-stu-id="7290a-173">The application security group set as source for the rule.</span></span> <span data-ttu-id="7290a-174">Non può essere usato con il parametro 'SourceAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="7290a-174">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="7290a-175">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="7290a-175">-SourcePortRange</span></span>
<span data-ttu-id="7290a-176">Specifica la porta o l'intervallo di origine.</span><span class="sxs-lookup"><span data-stu-id="7290a-176">Specifies the source port or range.</span></span>
<span data-ttu-id="7290a-177">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="7290a-177">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7290a-178">Un numero intero</span><span class="sxs-lookup"><span data-stu-id="7290a-178">An integer</span></span>
- <span data-ttu-id="7290a-179">Intervallo di interi compreso tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="7290a-179">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="7290a-180">Un carattere jolly (\*) che corrisponda a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="7290a-180">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="7290a-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7290a-181">CommonParameters</span></span>
<span data-ttu-id="7290a-182">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7290a-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7290a-183">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7290a-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7290a-184">INPUT</span><span class="sxs-lookup"><span data-stu-id="7290a-184">INPUTS</span></span>

### <span data-ttu-id="7290a-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7290a-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="7290a-186">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7290a-186">OUTPUTS</span></span>

### <span data-ttu-id="7290a-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7290a-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="7290a-188">NOTE</span><span class="sxs-lookup"><span data-stu-id="7290a-188">NOTES</span></span>

## <span data-ttu-id="7290a-189">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7290a-189">RELATED LINKS</span></span>

[<span data-ttu-id="7290a-190">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7290a-190">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7290a-191">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7290a-191">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7290a-192">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7290a-192">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7290a-193">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7290a-193">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)


