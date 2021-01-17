---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: adef9e3a2ba0d1e67ee8cb2ec9bdd14d9833f5d7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340723"
---
# <span data-ttu-id="4047c-101">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4047c-101">New-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="4047c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4047c-102">SYNOPSIS</span></span>
<span data-ttu-id="4047c-103">Crea una configurazione della regola di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="4047c-103">Creates a network security rule configuration.</span></span>

## <span data-ttu-id="4047c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4047c-104">SYNTAX</span></span>

### <span data-ttu-id="4047c-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4047c-105">SetByResource (Default)</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroup <PSApplicationSecurityGroup[]>]
 [-DestinationApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4047c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4047c-106">SetByResourceId</span></span>
```
New-AzNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <String[]>] [-DestinationPortRange <String[]>] [-SourceAddressPrefix <String[]>]
 [-DestinationAddressPrefix <String[]>] [-SourceApplicationSecurityGroupId <String[]>]
 [-DestinationApplicationSecurityGroupId <String[]>] [-Access <String>] [-Priority <Int32>]
 [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4047c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4047c-107">DESCRIPTION</span></span>
<span data-ttu-id="4047c-108">Il cmdlet **New-AzNetworkSecurityRuleConfig** crea una configurazione della regola di sicurezza di rete Azure per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="4047c-108">The **New-AzNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="4047c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4047c-109">EXAMPLES</span></span>

### <span data-ttu-id="4047c-110">Esempio 1: creare una regola di sicurezza di rete per consentire RDP</span><span class="sxs-lookup"><span data-stu-id="4047c-110">Example 1: Create a network security rule to allow RDP</span></span>
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="4047c-111">Questo comando crea una regola di sicurezza che consente l'accesso da Internet alla porta 3389</span><span class="sxs-lookup"><span data-stu-id="4047c-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="4047c-112">Esempio 2: creare una regola di sicurezza di rete che consente l'HTTP</span><span class="sxs-lookup"><span data-stu-id="4047c-112">Example 2: Create a network security rule that allows HTTP</span></span>
```powershell
$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="4047c-113">Questo comando crea una regola di sicurezza che consente l'accesso da Internet alla porta 80</span><span class="sxs-lookup"><span data-stu-id="4047c-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="4047c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4047c-114">PARAMETERS</span></span>

### <span data-ttu-id="4047c-115">-Access</span><span class="sxs-lookup"><span data-stu-id="4047c-115">-Access</span></span>
<span data-ttu-id="4047c-116">Specifica se il traffico di rete è consentito o negato.</span><span class="sxs-lookup"><span data-stu-id="4047c-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="4047c-117">I valori accettabili per questo parametro sono: Allow e Deny.</span><span class="sxs-lookup"><span data-stu-id="4047c-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="4047c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4047c-118">-DefaultProfile</span></span>
<span data-ttu-id="4047c-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4047c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4047c-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="4047c-120">-Description</span></span>
<span data-ttu-id="4047c-121">Specifica una descrizione della configurazione della regola di sicurezza della rete da creare.</span><span class="sxs-lookup"><span data-stu-id="4047c-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="4047c-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4047c-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="4047c-123">Specifica un prefisso per l'indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4047c-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="4047c-124">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4047c-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4047c-125">Un indirizzo CIDR (classe Interdomain Routing)</span><span class="sxs-lookup"><span data-stu-id="4047c-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="4047c-126">Un intervallo di indirizzi IP di destinazione</span><span class="sxs-lookup"><span data-stu-id="4047c-126">A destination IP address range</span></span> 
- <span data-ttu-id="4047c-127">Un carattere jolly (\*) in modo che corrisponda a qualsiasi indirizzo IP, è possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="4047c-127">A wildcard character (\*) to match any IP address You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="4047c-128">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4047c-128">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="4047c-129">Gruppo di sicurezza dell'applicazione impostato come destinazione per la regola.</span><span class="sxs-lookup"><span data-stu-id="4047c-129">The application security group set as destination for the rule.</span></span> <span data-ttu-id="4047c-130">Non può essere usato con il parametro "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="4047c-130">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="4047c-131">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="4047c-131">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="4047c-132">Gruppo di sicurezza dell'applicazione impostato come destinazione per la regola.</span><span class="sxs-lookup"><span data-stu-id="4047c-132">The application security group set as destination for the rule.</span></span> <span data-ttu-id="4047c-133">Non può essere usato con il parametro "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="4047c-133">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="4047c-134">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="4047c-134">-DestinationPortRange</span></span>
<span data-ttu-id="4047c-135">Specifica una porta o un intervallo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4047c-135">Specifies a destination port or range.</span></span>
<span data-ttu-id="4047c-136">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4047c-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4047c-137">Un numero intero</span><span class="sxs-lookup"><span data-stu-id="4047c-137">An integer</span></span>
- <span data-ttu-id="4047c-138">Un intervallo di numeri interi compresi tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="4047c-138">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="4047c-139">Carattere jolly (\*) che corrisponde a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="4047c-139">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="4047c-140">-Direzione</span><span class="sxs-lookup"><span data-stu-id="4047c-140">-Direction</span></span>
<span data-ttu-id="4047c-141">Specifica se una regola viene valutata nel traffico in entrata o in uscita.</span><span class="sxs-lookup"><span data-stu-id="4047c-141">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="4047c-142">I valori accettabili per questo parametro sono: in ingresso e in uscita.</span><span class="sxs-lookup"><span data-stu-id="4047c-142">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="4047c-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="4047c-143">-Name</span></span>
<span data-ttu-id="4047c-144">Specifica il nome della configurazione della regola di sicurezza della rete creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4047c-144">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4047c-145">-Priorità</span><span class="sxs-lookup"><span data-stu-id="4047c-145">-Priority</span></span>
<span data-ttu-id="4047c-146">Specifica la priorità di una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="4047c-146">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="4047c-147">I valori accettabili per questo parametro sono: un numero intero compreso tra 100 e 4096.</span><span class="sxs-lookup"><span data-stu-id="4047c-147">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>
<span data-ttu-id="4047c-148">Il numero di priorità deve essere univoco per ogni regola della raccolta.</span><span class="sxs-lookup"><span data-stu-id="4047c-148">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="4047c-149">Minore è il numero di priorità, maggiore è la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="4047c-149">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="4047c-150">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="4047c-150">-Protocol</span></span>
<span data-ttu-id="4047c-151">Specifica il protocollo di rete a cui si applica una nuova configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="4047c-151">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="4047c-152">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4047c-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4047c-153">TCP</span><span class="sxs-lookup"><span data-stu-id="4047c-153">Tcp</span></span>
- <span data-ttu-id="4047c-154">UDP</span><span class="sxs-lookup"><span data-stu-id="4047c-154">Udp</span></span>
- <span data-ttu-id="4047c-155">carattere jolly (\*) in modo che corrisponda a entrambi.</span><span class="sxs-lookup"><span data-stu-id="4047c-155">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="4047c-156">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="4047c-156">-SourceAddressPrefix</span></span>
<span data-ttu-id="4047c-157">Specifica un prefisso per l'indirizzo di origine.</span><span class="sxs-lookup"><span data-stu-id="4047c-157">Specifies a source address prefix.</span></span>
<span data-ttu-id="4047c-158">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4047c-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4047c-159">UN CIDR</span><span class="sxs-lookup"><span data-stu-id="4047c-159">A CIDR</span></span>
- <span data-ttu-id="4047c-160">Un intervallo IP di origine</span><span class="sxs-lookup"><span data-stu-id="4047c-160">A source IP range</span></span>
- <span data-ttu-id="4047c-161">Un carattere jolly (\*) per corrispondere a qualsiasi indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="4047c-161">A wildcard character (\*) to match any IP address.</span></span>
<span data-ttu-id="4047c-162">È anche possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="4047c-162">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="4047c-163">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4047c-163">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="4047c-164">Gruppo di sicurezza dell'applicazione impostato come origine per la regola.</span><span class="sxs-lookup"><span data-stu-id="4047c-164">The application security group set as source for the rule.</span></span> <span data-ttu-id="4047c-165">Non può essere usato con il parametro "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="4047c-165">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="4047c-166">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="4047c-166">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="4047c-167">Gruppo di sicurezza dell'applicazione impostato come origine per la regola.</span><span class="sxs-lookup"><span data-stu-id="4047c-167">The application security group set as source for the rule.</span></span> <span data-ttu-id="4047c-168">Non può essere usato con il parametro "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="4047c-168">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="4047c-169">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="4047c-169">-SourcePortRange</span></span>
<span data-ttu-id="4047c-170">Specifica la porta o l'intervallo di origine.</span><span class="sxs-lookup"><span data-stu-id="4047c-170">Specifies the source port or range.</span></span>
<span data-ttu-id="4047c-171">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4047c-171">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4047c-172">Un numero intero</span><span class="sxs-lookup"><span data-stu-id="4047c-172">An integer</span></span>
- <span data-ttu-id="4047c-173">Un intervallo di numeri interi compresi tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="4047c-173">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="4047c-174">Carattere jolly (\*) che corrisponde a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="4047c-174">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="4047c-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4047c-175">CommonParameters</span></span>
<span data-ttu-id="4047c-176">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4047c-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4047c-177">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4047c-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4047c-178">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4047c-178">INPUTS</span></span>

### <span data-ttu-id="4047c-179">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4047c-179">None</span></span>

## <span data-ttu-id="4047c-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4047c-180">OUTPUTS</span></span>

### <span data-ttu-id="4047c-181">Microsoft. Azure. Commands. Network. Models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="4047c-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="4047c-182">Note</span><span class="sxs-lookup"><span data-stu-id="4047c-182">NOTES</span></span>

## <span data-ttu-id="4047c-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4047c-183">RELATED LINKS</span></span>

[<span data-ttu-id="4047c-184">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4047c-184">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4047c-185">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4047c-185">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4047c-186">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4047c-186">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4047c-187">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4047c-187">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


