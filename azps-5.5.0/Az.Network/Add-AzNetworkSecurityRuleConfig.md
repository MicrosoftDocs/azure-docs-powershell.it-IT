---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9160A21D-0F83-415B-830B-F35C8B863E90
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: a69f0d4056eb49f078c1e64342a1b4b2a8dae9ad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192023"
---
# <span data-ttu-id="b7289-101">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b7289-101">Add-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="b7289-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7289-102">SYNOPSIS</span></span>
<span data-ttu-id="b7289-103">Aggiunge una configurazione della regola di sicurezza di rete a un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="b7289-103">Adds a network security rule configuration to a network security group.</span></span>

## <span data-ttu-id="b7289-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7289-104">SYNTAX</span></span>

### <span data-ttu-id="b7289-105">SetByResource (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b7289-105">SetByResource (Default)</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7289-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b7289-106">SetByResourceId</span></span>
```
Add-AzNetworkSecurityRuleConfig -Name <String> -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-Description <String>] [-Protocol <String>] [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>]
 [-SourceAddressPrefix <String[]>] [-DestinationAddressPrefix <String[]>]
 [-SourceApplicationSecurityGroupId <String[]>] [-DestinationApplicationSecurityGroupId <String[]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7289-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b7289-107">DESCRIPTION</span></span>
<span data-ttu-id="b7289-108">Il cmdlet **Add-AzNetworkSecurityRuleConfig aggiunge** una configurazione della regola di sicurezza di rete a un gruppo di sicurezza di rete di Azure.</span><span class="sxs-lookup"><span data-stu-id="b7289-108">The **Add-AzNetworkSecurityRuleConfig** cmdlet adds a network security rule configuration to an Azure network security group.</span></span>

## <span data-ttu-id="b7289-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7289-109">EXAMPLES</span></span>

### <span data-ttu-id="b7289-110">1: Aggiunta di un gruppo di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="b7289-110">1: Adding a network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 | 
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access 
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet 
    -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389 | 
    Set-AzNetworkSecurityGroup
```

<span data-ttu-id="b7289-111">Il primo comando recupera un gruppo di sicurezza di rete Azure denominato "nsg1" dal gruppo di risorse "rg1".</span><span class="sxs-lookup"><span data-stu-id="b7289-111">The first command retrieves an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="b7289-112">Il secondo comando aggiunge una regola di sicurezza di rete denominata "rdp-rule" che consente il traffico Da Internet sulla porta 3389 all'oggetto gruppo di sicurezza di rete recuperato.</span><span class="sxs-lookup"><span data-stu-id="b7289-112">The second command adds a network security rule named "rdp-rule" that allows traffic from internet on port 3389 to the retrieved network security group object.</span></span> <span data-ttu-id="b7289-113">Mantiene il gruppo di sicurezza di rete Azure modificato.</span><span class="sxs-lookup"><span data-stu-id="b7289-113">Persists the modified Azure network security group.</span></span>

### <span data-ttu-id="b7289-114">2: Aggiunta di una nuova regola di sicurezza con i gruppi di sicurezza delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="b7289-114">2: Adding a new security rule with application security groups</span></span>
```
$srcAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name srcAsg -Location "West US"
$destAsg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name destAsg -Location "West US"

Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 |
Add-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access
    Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceApplicationSecurityGroup
    $srcAsg -SourcePortRange * -DestinationApplicationSecurityGroup $destAsg -DestinationPortRange 3389 |
Set-AzNetworkSecurityGroup
```

<span data-ttu-id="b7289-115">Prima di tutto, vengono creati due nuovi gruppi di sicurezza delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="b7289-115">First, we create two new application security groups.</span></span> <span data-ttu-id="b7289-116">Recupera quindi un gruppo di sicurezza di rete Azure denominato "nsg1" dal gruppo di risorse "rg1".</span><span class="sxs-lookup"><span data-stu-id="b7289-116">Then, we retrieve an Azure network security group named "nsg1" from resource group "rg1".</span></span> <span data-ttu-id="b7289-117">e aggiunge una regola di sicurezza di rete denominata "rdp-rule".</span><span class="sxs-lookup"><span data-stu-id="b7289-117">and add a network security rule named "rdp-rule" to it.</span></span> <span data-ttu-id="b7289-118">La regola consente il traffico da tutte le configurazioni IP nel gruppo di sicurezza dell'applicazione "srcAsg" a tutte le configurazioni IP in "destAsg" sulla porta 3389.</span><span class="sxs-lookup"><span data-stu-id="b7289-118">The rule allows traffic from all the IP configurations in the application security group "srcAsg" to all the IP configurations in "destAsg" on port 3389.</span></span> <span data-ttu-id="b7289-119">Dopo aver aggiunto la regola, il gruppo di sicurezza di rete Azure modificato viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="b7289-119">After adding the rule, we persist the modified Azure network security group.</span></span>

## <span data-ttu-id="b7289-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7289-120">PARAMETERS</span></span>

### <span data-ttu-id="b7289-121">-Access</span><span class="sxs-lookup"><span data-stu-id="b7289-121">-Access</span></span>
<span data-ttu-id="b7289-122">Specifica se il traffico di rete è consentito o negato.</span><span class="sxs-lookup"><span data-stu-id="b7289-122">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="b7289-123">I valori accettabili per questo parametro sono: Allow e Deny.</span><span class="sxs-lookup"><span data-stu-id="b7289-123">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="b7289-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7289-124">-DefaultProfile</span></span>
<span data-ttu-id="b7289-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7289-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7289-126">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7289-126">-Description</span></span>
<span data-ttu-id="b7289-127">Specifica una descrizione della configurazione di una regola di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="b7289-127">Specifies a description of a network security rule configuration.</span></span>

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

### <span data-ttu-id="b7289-128">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b7289-128">-DestinationAddressPrefix</span></span>
<span data-ttu-id="b7289-129">Specifica un prefisso di indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b7289-129">Specifies a destination address prefix.</span></span>
<span data-ttu-id="b7289-130">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="b7289-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7289-131">Indirizzo Classless Interdomain Routing (CIDR)</span><span class="sxs-lookup"><span data-stu-id="b7289-131">A Classless Interdomain Routing (CIDR) address</span></span>
- <span data-ttu-id="b7289-132">Un intervallo di indirizzi IP di destinazione</span><span class="sxs-lookup"><span data-stu-id="b7289-132">A destination IP address range</span></span>
- <span data-ttu-id="b7289-133">Un carattere jolly (\*) per corrispondere a qualsiasi indirizzo IP È possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="b7289-133">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="b7289-134">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b7289-134">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="b7289-135">Gruppo di sicurezza dell'applicazione impostato come destinazione della regola.</span><span class="sxs-lookup"><span data-stu-id="b7289-135">The application security group set as destination for the rule.</span></span> <span data-ttu-id="b7289-136">Non può essere usato con il parametro 'DestinationAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="b7289-136">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="b7289-137">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="b7289-137">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="b7289-138">Gruppo di sicurezza dell'applicazione impostato come destinazione della regola.</span><span class="sxs-lookup"><span data-stu-id="b7289-138">The application security group set as destination for the rule.</span></span> <span data-ttu-id="b7289-139">Non può essere usato con il parametro 'DestinationAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="b7289-139">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="b7289-140">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="b7289-140">-DestinationPortRange</span></span>
<span data-ttu-id="b7289-141">Specifica una porta o un intervallo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b7289-141">Specifies a destination port or range.</span></span>
<span data-ttu-id="b7289-142">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="b7289-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7289-143">Un numero intero</span><span class="sxs-lookup"><span data-stu-id="b7289-143">An integer</span></span>
- <span data-ttu-id="b7289-144">Intervallo di interi compreso tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="b7289-144">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="b7289-145">Un carattere jolly (\*) che corrisponda a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="b7289-145">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="b7289-146">-Direction</span><span class="sxs-lookup"><span data-stu-id="b7289-146">-Direction</span></span>
<span data-ttu-id="b7289-147">Specifica se una regola viene valutata sul traffico in arrivo o in uscita.</span><span class="sxs-lookup"><span data-stu-id="b7289-147">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="b7289-148">I valori accettabili per questo parametro sono: in ingresso e in uscita.</span><span class="sxs-lookup"><span data-stu-id="b7289-148">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="b7289-149">-Name</span><span class="sxs-lookup"><span data-stu-id="b7289-149">-Name</span></span>
<span data-ttu-id="b7289-150">Specifica il nome di una configurazione della regola di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="b7289-150">Specifies the name of a network security rule configuration.</span></span>

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

### <span data-ttu-id="b7289-151">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b7289-151">-NetworkSecurityGroup</span></span>
<span data-ttu-id="b7289-152">Specifica un **oggetto NetworkSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="b7289-152">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="b7289-153">Questo cmdlet aggiunge all'oggetto specificato da questo parametro una configurazione della regola di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="b7289-153">This cmdlet adds a network security rule configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="b7289-154">-Priority</span><span class="sxs-lookup"><span data-stu-id="b7289-154">-Priority</span></span>
<span data-ttu-id="b7289-155">Specifica la priorità di una configurazione delle regole.</span><span class="sxs-lookup"><span data-stu-id="b7289-155">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="b7289-156">I valori accettabili per questo parametro sono: un numero intero compreso tra 100 e 4096.</span><span class="sxs-lookup"><span data-stu-id="b7289-156">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="b7289-157">Il numero di priorità deve essere univoco per ogni regola della raccolta.</span><span class="sxs-lookup"><span data-stu-id="b7289-157">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="b7289-158">Più basso è il numero di priorità, più alta sarà la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="b7289-158">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="b7289-159">-Protocol</span><span class="sxs-lookup"><span data-stu-id="b7289-159">-Protocol</span></span>
<span data-ttu-id="b7289-160">Specifica il protocollo di rete a cui si applica una configurazione di regole.</span><span class="sxs-lookup"><span data-stu-id="b7289-160">Specifies the network protocol that a rule configuration applies to.</span></span>
<span data-ttu-id="b7289-161">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="b7289-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7289-162">Tcp</span><span class="sxs-lookup"><span data-stu-id="b7289-162">Tcp</span></span>
- <span data-ttu-id="b7289-163">Udp</span><span class="sxs-lookup"><span data-stu-id="b7289-163">Udp</span></span>
- <span data-ttu-id="b7289-164">Carattere jolly (\*) per trovare le corrispondenze con entrambe le corrispondenze</span><span class="sxs-lookup"><span data-stu-id="b7289-164">Wildcard character (\*) to match both</span></span>

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

### <span data-ttu-id="b7289-165">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b7289-165">-SourceAddressPrefix</span></span>
<span data-ttu-id="b7289-166">Specifica un prefisso dell'indirizzo di origine.</span><span class="sxs-lookup"><span data-stu-id="b7289-166">Specifies a source address prefix.</span></span>
<span data-ttu-id="b7289-167">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="b7289-167">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7289-168">UN CIDR</span><span class="sxs-lookup"><span data-stu-id="b7289-168">A CIDR</span></span>
- <span data-ttu-id="b7289-169">Un intervallo IP di origine</span><span class="sxs-lookup"><span data-stu-id="b7289-169">A source IP range</span></span>
- <span data-ttu-id="b7289-170">Un carattere jolly (\*) che corrisponda a qualsiasi indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="b7289-170">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="b7289-171">È anche possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="b7289-171">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="b7289-172">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b7289-172">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="b7289-173">Gruppo di sicurezza dell'applicazione impostato come origine della regola.</span><span class="sxs-lookup"><span data-stu-id="b7289-173">The application security group set as source for the rule.</span></span> <span data-ttu-id="b7289-174">Non può essere usato con il parametro 'SourceAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="b7289-174">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="b7289-175">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="b7289-175">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="b7289-176">Gruppo di sicurezza dell'applicazione impostato come origine della regola.</span><span class="sxs-lookup"><span data-stu-id="b7289-176">The application security group set as source for the rule.</span></span> <span data-ttu-id="b7289-177">Non può essere usato con il parametro 'SourceAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="b7289-177">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="b7289-178">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="b7289-178">-SourcePortRange</span></span>
<span data-ttu-id="b7289-179">Specifica una porta o un intervallo di origine.</span><span class="sxs-lookup"><span data-stu-id="b7289-179">Specifies a source port or range.</span></span>
<span data-ttu-id="b7289-180">Questo valore viene espresso come numero intero, come intervallo compreso tra 0 e 65535 o come carattere jolly (\*) in modo che corrisponda a qualsiasi porta di origine.</span><span class="sxs-lookup"><span data-stu-id="b7289-180">This value is expressed as an integer, as a range between 0 and 65535, or as a wildcard character (\*) to match any source port.</span></span>

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

### <span data-ttu-id="b7289-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7289-181">CommonParameters</span></span>
<span data-ttu-id="b7289-182">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7289-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7289-183">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7289-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7289-184">INPUT</span><span class="sxs-lookup"><span data-stu-id="b7289-184">INPUTS</span></span>

### <span data-ttu-id="b7289-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b7289-185">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="b7289-186">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7289-186">OUTPUTS</span></span>

### <span data-ttu-id="b7289-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b7289-187">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="b7289-188">NOTE</span><span class="sxs-lookup"><span data-stu-id="b7289-188">NOTES</span></span>

## <span data-ttu-id="b7289-189">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7289-189">RELATED LINKS</span></span>

[<span data-ttu-id="b7289-190">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b7289-190">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b7289-191">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b7289-191">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b7289-192">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b7289-192">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b7289-193">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b7289-193">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


