---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: adef9e3a2ba0d1e67ee8cb2ec9bdd14d9833f5d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189655"
---
# <span data-ttu-id="55120-101">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="55120-101">New-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="55120-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55120-102">SYNOPSIS</span></span>
<span data-ttu-id="55120-103">Crea una configurazione delle regole di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="55120-103">Creates a network security rule configuration.</span></span>

## <span data-ttu-id="55120-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55120-104">SYNTAX</span></span>

### <span data-ttu-id="55120-105">SetByResource (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="55120-105">SetByResource (Default)</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55120-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="55120-106">SetByResourceId</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroupId <String[]>]
 [-DestinationApplicationSecurityGroupId <String[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55120-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="55120-107">DESCRIPTION</span></span>
<span data-ttu-id="55120-108">Il cmdlet **New-AzNetworkSecurityRuleConfig crea** una configurazione della regola di sicurezza di rete di Azure per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="55120-108">The **New-AzNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="55120-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55120-109">EXAMPLES</span></span>

### <span data-ttu-id="55120-110">Esempio 1: Creare una regola di sicurezza di rete per consentire RdP</span><span class="sxs-lookup"><span data-stu-id="55120-110">Example 1: Create a network security rule to allow RDP</span></span>
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="55120-111">Questo comando crea una regola di sicurezza che consente l'accesso da Internet alla porta 3389</span><span class="sxs-lookup"><span data-stu-id="55120-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="55120-112">Esempio 2: Creare una regola di sicurezza di rete che consente l'accesso HTTP</span><span class="sxs-lookup"><span data-stu-id="55120-112">Example 2: Create a network security rule that allows HTTP</span></span>
```powershell
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="55120-113">Questo comando crea una regola di sicurezza che consente l'accesso da Internet alla porta 80</span><span class="sxs-lookup"><span data-stu-id="55120-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="55120-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55120-114">PARAMETERS</span></span>

### <span data-ttu-id="55120-115">-Access</span><span class="sxs-lookup"><span data-stu-id="55120-115">-Access</span></span>
<span data-ttu-id="55120-116">Specifica se il traffico di rete è consentito o negato.</span><span class="sxs-lookup"><span data-stu-id="55120-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="55120-117">I valori accettabili per questo parametro sono: Allow e Deny.</span><span class="sxs-lookup"><span data-stu-id="55120-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="55120-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55120-118">-DefaultProfile</span></span>
<span data-ttu-id="55120-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="55120-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55120-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="55120-120">-Description</span></span>
<span data-ttu-id="55120-121">Specifica una descrizione della configurazione della regola di sicurezza di rete da creare.</span><span class="sxs-lookup"><span data-stu-id="55120-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="55120-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="55120-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="55120-123">Specifica un prefisso di indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="55120-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="55120-124">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="55120-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="55120-125">Indirizzo Classless Interdomain Routing (CIDR)</span><span class="sxs-lookup"><span data-stu-id="55120-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="55120-126">Un intervallo di indirizzi IP di destinazione</span><span class="sxs-lookup"><span data-stu-id="55120-126">A destination IP address range</span></span> 
- <span data-ttu-id="55120-127">Un carattere jolly (\*) per corrispondere a qualsiasi indirizzo IP È possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="55120-127">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="55120-128">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="55120-128">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="55120-129">Gruppo di sicurezza dell'applicazione impostato come destinazione della regola.</span><span class="sxs-lookup"><span data-stu-id="55120-129">The application security group set as destination for the rule.</span></span> <span data-ttu-id="55120-130">Non può essere usato con il parametro 'DestinationAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="55120-130">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="55120-131">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="55120-131">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="55120-132">Gruppo di sicurezza dell'applicazione impostato come destinazione della regola.</span><span class="sxs-lookup"><span data-stu-id="55120-132">The application security group set as destination for the rule.</span></span> <span data-ttu-id="55120-133">Non può essere usato con il parametro 'DestinationAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="55120-133">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="55120-134">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="55120-134">-DestinationPortRange</span></span>
<span data-ttu-id="55120-135">Specifica una porta o un intervallo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="55120-135">Specifies a destination port or range.</span></span>
<span data-ttu-id="55120-136">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="55120-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="55120-137">Un numero intero</span><span class="sxs-lookup"><span data-stu-id="55120-137">An integer</span></span>
- <span data-ttu-id="55120-138">Intervallo di interi compreso tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="55120-138">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="55120-139">Un carattere jolly (\*) che corrisponda a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="55120-139">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="55120-140">-Direction</span><span class="sxs-lookup"><span data-stu-id="55120-140">-Direction</span></span>
<span data-ttu-id="55120-141">Specifica se una regola viene valutata sul traffico in arrivo o in uscita.</span><span class="sxs-lookup"><span data-stu-id="55120-141">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="55120-142">I valori accettabili per questo parametro sono: in ingresso e in uscita.</span><span class="sxs-lookup"><span data-stu-id="55120-142">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="55120-143">-Name</span><span class="sxs-lookup"><span data-stu-id="55120-143">-Name</span></span>
<span data-ttu-id="55120-144">Specifica il nome della configurazione della regola di sicurezza di rete creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55120-144">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="55120-145">-Priority</span><span class="sxs-lookup"><span data-stu-id="55120-145">-Priority</span></span>
<span data-ttu-id="55120-146">Specifica la priorità di una configurazione delle regole.</span><span class="sxs-lookup"><span data-stu-id="55120-146">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="55120-147">I valori accettabili per questo parametro sono: un numero intero compreso tra 100 e 4096.</span><span class="sxs-lookup"><span data-stu-id="55120-147">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="55120-148">Il numero di priorità deve essere univoco per ogni regola della raccolta.</span><span class="sxs-lookup"><span data-stu-id="55120-148">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="55120-149">Più basso è il numero di priorità, più alta sarà la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="55120-149">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="55120-150">-Protocol</span><span class="sxs-lookup"><span data-stu-id="55120-150">-Protocol</span></span>
<span data-ttu-id="55120-151">Specifica il protocollo di rete a cui si applica una nuova configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="55120-151">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="55120-152">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="55120-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="55120-153">Tcp</span><span class="sxs-lookup"><span data-stu-id="55120-153">Tcp</span></span>
- <span data-ttu-id="55120-154">Udp</span><span class="sxs-lookup"><span data-stu-id="55120-154">Udp</span></span>
- <span data-ttu-id="55120-155">caratteri jolly (\*) per trovare le corrispondenze con entrambe.</span><span class="sxs-lookup"><span data-stu-id="55120-155">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="55120-156">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="55120-156">-SourceAddressPrefix</span></span>
<span data-ttu-id="55120-157">Specifica un prefisso dell'indirizzo di origine.</span><span class="sxs-lookup"><span data-stu-id="55120-157">Specifies a source address prefix.</span></span>
<span data-ttu-id="55120-158">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="55120-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="55120-159">UN CIDR</span><span class="sxs-lookup"><span data-stu-id="55120-159">A CIDR</span></span>
- <span data-ttu-id="55120-160">Un intervallo IP di origine</span><span class="sxs-lookup"><span data-stu-id="55120-160">A source IP range</span></span>
- <span data-ttu-id="55120-161">Un carattere jolly (\*) che corrisponda a qualsiasi indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="55120-161">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="55120-162">È anche possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="55120-162">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="55120-163">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="55120-163">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="55120-164">Gruppo di sicurezza dell'applicazione impostato come origine della regola.</span><span class="sxs-lookup"><span data-stu-id="55120-164">The application security group set as source for the rule.</span></span> <span data-ttu-id="55120-165">Non può essere usato con il parametro 'SourceAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="55120-165">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="55120-166">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="55120-166">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="55120-167">Gruppo di sicurezza dell'applicazione impostato come origine della regola.</span><span class="sxs-lookup"><span data-stu-id="55120-167">The application security group set as source for the rule.</span></span> <span data-ttu-id="55120-168">Non può essere usato con il parametro 'SourceAddressPrefix'.</span><span class="sxs-lookup"><span data-stu-id="55120-168">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="55120-169">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="55120-169">-SourcePortRange</span></span>
<span data-ttu-id="55120-170">Specifica la porta o l'intervallo di origine.</span><span class="sxs-lookup"><span data-stu-id="55120-170">Specifies the source port or range.</span></span>
<span data-ttu-id="55120-171">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="55120-171">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="55120-172">Un numero intero</span><span class="sxs-lookup"><span data-stu-id="55120-172">An integer</span></span>
- <span data-ttu-id="55120-173">Intervallo di interi compreso tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="55120-173">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="55120-174">Un carattere jolly (\*) che corrisponda a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="55120-174">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="55120-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55120-175">CommonParameters</span></span>
<span data-ttu-id="55120-176">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55120-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55120-177">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55120-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55120-178">INPUT</span><span class="sxs-lookup"><span data-stu-id="55120-178">INPUTS</span></span>

### <span data-ttu-id="55120-179">Nessuno</span><span class="sxs-lookup"><span data-stu-id="55120-179">None</span></span>

## <span data-ttu-id="55120-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55120-180">OUTPUTS</span></span>

### <span data-ttu-id="55120-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="55120-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="55120-182">NOTE</span><span class="sxs-lookup"><span data-stu-id="55120-182">NOTES</span></span>

## <span data-ttu-id="55120-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55120-183">RELATED LINKS</span></span>

[<span data-ttu-id="55120-184">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="55120-184">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="55120-185">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="55120-185">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="55120-186">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="55120-186">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="55120-187">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="55120-187">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


