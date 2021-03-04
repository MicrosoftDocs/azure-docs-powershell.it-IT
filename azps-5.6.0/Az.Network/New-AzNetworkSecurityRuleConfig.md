---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 45702774e44e4b3da0b90d37e86e478c52dcba17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953918"
---
# <span data-ttu-id="cfacc-101">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfacc-101">New-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="cfacc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfacc-102">SYNOPSIS</span></span>
<span data-ttu-id="cfacc-103">Crea una configurazione delle regole di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="cfacc-103">Creates a network security rule configuration.</span></span>

## <span data-ttu-id="cfacc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cfacc-104">SYNTAX</span></span>

### <span data-ttu-id="cfacc-105">SetByResource (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cfacc-105">SetByResource (Default)</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfacc-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cfacc-106">SetByResourceId</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroupId <String[]>]
 [-DestinationApplicationSecurityGroupId <String[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfacc-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cfacc-107">DESCRIPTION</span></span>
<span data-ttu-id="cfacc-108">Il cmdlet **New-AzNetworkSecurityRuleConfig crea** una configurazione della regola di sicurezza di rete di Azure per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="cfacc-108">The **New-AzNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="cfacc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cfacc-109">EXAMPLES</span></span>

### <span data-ttu-id="cfacc-110">Esempio 1: Creare una regola di sicurezza di rete per consentire RDP</span><span class="sxs-lookup"><span data-stu-id="cfacc-110">Example 1: Create a network security rule to allow RDP</span></span>
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="cfacc-111">Questo comando crea una regola di sicurezza che consente l'accesso da Internet alla porta 3389</span><span class="sxs-lookup"><span data-stu-id="cfacc-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="cfacc-112">Esempio 2: Creare una regola di sicurezza di rete che consenta di utilizzare HTTP</span><span class="sxs-lookup"><span data-stu-id="cfacc-112">Example 2: Create a network security rule that allows HTTP</span></span>
```powershell
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="cfacc-113">Questo comando crea una regola di sicurezza che consente l'accesso da Internet alla porta 80</span><span class="sxs-lookup"><span data-stu-id="cfacc-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="cfacc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cfacc-114">PARAMETERS</span></span>

### <span data-ttu-id="cfacc-115">-Access</span><span class="sxs-lookup"><span data-stu-id="cfacc-115">-Access</span></span>
<span data-ttu-id="cfacc-116">Specifica se il traffico di rete è consentito o negato.</span><span class="sxs-lookup"><span data-stu-id="cfacc-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="cfacc-117">I valori accettabili per questo parametro sono: Allow e Deny.</span><span class="sxs-lookup"><span data-stu-id="cfacc-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="cfacc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfacc-118">-DefaultProfile</span></span>
<span data-ttu-id="cfacc-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cfacc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfacc-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="cfacc-120">-Description</span></span>
<span data-ttu-id="cfacc-121">Specifica una descrizione della configurazione della regola di sicurezza di rete da creare.</span><span class="sxs-lookup"><span data-stu-id="cfacc-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="cfacc-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="cfacc-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="cfacc-123">Specifica un prefisso di indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cfacc-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="cfacc-124">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="cfacc-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cfacc-125">Indirizzo Classless Interdomain Routing (CIDR)</span><span class="sxs-lookup"><span data-stu-id="cfacc-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="cfacc-126">Un intervallo di indirizzi IP di destinazione</span><span class="sxs-lookup"><span data-stu-id="cfacc-126">A destination IP address range</span></span> 
- <span data-ttu-id="cfacc-127">Un carattere jolly (\*) che corrisponda a qualsiasi indirizzo IP È possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="cfacc-127">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="cfacc-128">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cfacc-128">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="cfacc-129">Gruppo di sicurezza dell'applicazione impostato come destinazione della regola.</span><span class="sxs-lookup"><span data-stu-id="cfacc-129">The application security group set as destination for the rule.</span></span> <span data-ttu-id="cfacc-130">Non può essere usato con il parametro 'DestinationAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="cfacc-130">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="cfacc-131">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="cfacc-131">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="cfacc-132">Gruppo di sicurezza dell'applicazione impostato come destinazione della regola.</span><span class="sxs-lookup"><span data-stu-id="cfacc-132">The application security group set as destination for the rule.</span></span> <span data-ttu-id="cfacc-133">Non può essere usato con il parametro 'DestinationAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="cfacc-133">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="cfacc-134">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="cfacc-134">-DestinationPortRange</span></span>
<span data-ttu-id="cfacc-135">Specifica una porta o un intervallo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cfacc-135">Specifies a destination port or range.</span></span>
<span data-ttu-id="cfacc-136">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="cfacc-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cfacc-137">Numero intero</span><span class="sxs-lookup"><span data-stu-id="cfacc-137">An integer</span></span>
- <span data-ttu-id="cfacc-138">Intervallo di interi compreso tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="cfacc-138">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="cfacc-139">Un carattere jolly (\*) che corrisponda a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="cfacc-139">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="cfacc-140">-Direction</span><span class="sxs-lookup"><span data-stu-id="cfacc-140">-Direction</span></span>
<span data-ttu-id="cfacc-141">Specifica se una regola viene valutata sul traffico in arrivo o in uscita.</span><span class="sxs-lookup"><span data-stu-id="cfacc-141">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="cfacc-142">I valori accettabili per questo parametro sono: in ingresso e in uscita.</span><span class="sxs-lookup"><span data-stu-id="cfacc-142">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="cfacc-143">-Name</span><span class="sxs-lookup"><span data-stu-id="cfacc-143">-Name</span></span>
<span data-ttu-id="cfacc-144">Specifica il nome della configurazione della regola di sicurezza di rete creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfacc-144">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="cfacc-145">-Priority</span><span class="sxs-lookup"><span data-stu-id="cfacc-145">-Priority</span></span>
<span data-ttu-id="cfacc-146">Specifica la priorità di una configurazione delle regole.</span><span class="sxs-lookup"><span data-stu-id="cfacc-146">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="cfacc-147">I valori accettabili per questo parametro sono: un numero intero compreso tra 100 e 4096.</span><span class="sxs-lookup"><span data-stu-id="cfacc-147">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="cfacc-148">Il numero di priorità deve essere univoco per ogni regola della raccolta.</span><span class="sxs-lookup"><span data-stu-id="cfacc-148">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="cfacc-149">Più basso è il numero di priorità, più alta sarà la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="cfacc-149">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="cfacc-150">-Protocol</span><span class="sxs-lookup"><span data-stu-id="cfacc-150">-Protocol</span></span>
<span data-ttu-id="cfacc-151">Specifica il protocollo di rete a cui si applica una nuova configurazione di regole.</span><span class="sxs-lookup"><span data-stu-id="cfacc-151">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="cfacc-152">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="cfacc-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cfacc-153">Tcp</span><span class="sxs-lookup"><span data-stu-id="cfacc-153">Tcp</span></span>
- <span data-ttu-id="cfacc-154">Udp</span><span class="sxs-lookup"><span data-stu-id="cfacc-154">Udp</span></span>
- <span data-ttu-id="cfacc-155">caratteri jolly (\*) per trovare le corrispondenze con entrambe.</span><span class="sxs-lookup"><span data-stu-id="cfacc-155">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="cfacc-156">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="cfacc-156">-SourceAddressPrefix</span></span>
<span data-ttu-id="cfacc-157">Specifica un prefisso dell'indirizzo di origine.</span><span class="sxs-lookup"><span data-stu-id="cfacc-157">Specifies a source address prefix.</span></span>
<span data-ttu-id="cfacc-158">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="cfacc-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cfacc-159">UN CIDR</span><span class="sxs-lookup"><span data-stu-id="cfacc-159">A CIDR</span></span>
- <span data-ttu-id="cfacc-160">Un intervallo IP di origine</span><span class="sxs-lookup"><span data-stu-id="cfacc-160">A source IP range</span></span>
- <span data-ttu-id="cfacc-161">Un carattere jolly (\*) che corrisponda a qualsiasi indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="cfacc-161">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="cfacc-162">È anche possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="cfacc-162">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="cfacc-163">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cfacc-163">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="cfacc-164">Gruppo di sicurezza dell'applicazione impostato come origine della regola.</span><span class="sxs-lookup"><span data-stu-id="cfacc-164">The application security group set as source for the rule.</span></span> <span data-ttu-id="cfacc-165">Non può essere usato con il parametro 'SourceAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="cfacc-165">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="cfacc-166">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="cfacc-166">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="cfacc-167">Gruppo di sicurezza dell'applicazione impostato come origine della regola.</span><span class="sxs-lookup"><span data-stu-id="cfacc-167">The application security group set as source for the rule.</span></span> <span data-ttu-id="cfacc-168">Non può essere usato con il parametro 'SourceAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="cfacc-168">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="cfacc-169">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="cfacc-169">-SourcePortRange</span></span>
<span data-ttu-id="cfacc-170">Specifica la porta o l'intervallo di origine.</span><span class="sxs-lookup"><span data-stu-id="cfacc-170">Specifies the source port or range.</span></span>
<span data-ttu-id="cfacc-171">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="cfacc-171">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cfacc-172">Numero intero</span><span class="sxs-lookup"><span data-stu-id="cfacc-172">An integer</span></span>
- <span data-ttu-id="cfacc-173">Intervallo di interi compreso tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="cfacc-173">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="cfacc-174">Un carattere jolly (\*) che corrisponda a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="cfacc-174">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="cfacc-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfacc-175">CommonParameters</span></span>
<span data-ttu-id="cfacc-176">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfacc-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfacc-177">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfacc-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfacc-178">INPUT</span><span class="sxs-lookup"><span data-stu-id="cfacc-178">INPUTS</span></span>

### <span data-ttu-id="cfacc-179">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cfacc-179">None</span></span>

## <span data-ttu-id="cfacc-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cfacc-180">OUTPUTS</span></span>

### <span data-ttu-id="cfacc-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="cfacc-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="cfacc-182">NOTE</span><span class="sxs-lookup"><span data-stu-id="cfacc-182">NOTES</span></span>

## <span data-ttu-id="cfacc-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cfacc-183">RELATED LINKS</span></span>

[<span data-ttu-id="cfacc-184">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfacc-184">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="cfacc-185">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfacc-185">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="cfacc-186">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfacc-186">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="cfacc-187">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfacc-187">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


