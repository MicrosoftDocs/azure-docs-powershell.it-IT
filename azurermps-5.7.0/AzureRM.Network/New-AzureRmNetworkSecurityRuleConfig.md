---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: 14af257cf6c5d5e547f81b76fd82a910580b3790
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516688"
---
# <span data-ttu-id="b8c75-101">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b8c75-101">New-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="b8c75-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b8c75-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c75-103">Crea una configurazione della regola di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="b8c75-103">Creates a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8c75-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b8c75-104">SYNTAX</span></span>

### <span data-ttu-id="b8c75-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b8c75-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DestinationApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-Access <String>] [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8c75-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b8c75-106">SetByResourceId</span></span>
```
New-AzureRmNetworkSecurityRuleConfig -Name <String> [-Description <String>] [-Protocol <String>]
 [-SourcePortRange <System.Collections.Generic.List`1[System.String]>]
 [-DestinationPortRange <System.Collections.Generic.List`1[System.String]>]
 [-SourceAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-DestinationAddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-SourceApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DestinationApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-Access <String>]
 [-Priority <Int32>] [-Direction <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8c75-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8c75-107">DESCRIPTION</span></span>
<span data-ttu-id="b8c75-108">Il cmdlet **New-AzureRmNetworkSecurityRuleConfig** crea una configurazione della regola di sicurezza di rete Azure per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="b8c75-108">The **New-AzureRmNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="b8c75-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b8c75-109">EXAMPLES</span></span>

### <span data-ttu-id="b8c75-110">1: creare una regola di sicurezza della rete per consentire RDP</span><span class="sxs-lookup"><span data-stu-id="b8c75-110">1: Create a network security rule to allow RDP</span></span>
```
$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="b8c75-111">Questo comando crea una regola di sicurezza che consente l'accesso da Internet alla porta 3389</span><span class="sxs-lookup"><span data-stu-id="b8c75-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="b8c75-112">2: creare una regola di sicurezza di rete che consente l'HTTP</span><span class="sxs-lookup"><span data-stu-id="b8c75-112">2: Create a network security rule that allows HTTP</span></span>
```
$rule2 = New-AzureRmNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="b8c75-113">Questo comando crea una regola di sicurezza che consente l'accesso da Internet alla porta 80</span><span class="sxs-lookup"><span data-stu-id="b8c75-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="b8c75-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b8c75-114">PARAMETERS</span></span>

### <span data-ttu-id="b8c75-115">-Access</span><span class="sxs-lookup"><span data-stu-id="b8c75-115">-Access</span></span>
<span data-ttu-id="b8c75-116">Specifica se il traffico di rete è consentito o negato.</span><span class="sxs-lookup"><span data-stu-id="b8c75-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="b8c75-117">I valori accettabili per questo parametro sono: Allow e Deny.</span><span class="sxs-lookup"><span data-stu-id="b8c75-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="b8c75-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c75-118">-DefaultProfile</span></span>
<span data-ttu-id="b8c75-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b8c75-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8c75-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8c75-120">-Description</span></span>
<span data-ttu-id="b8c75-121">Specifica una descrizione della configurazione della regola di sicurezza della rete da creare.</span><span class="sxs-lookup"><span data-stu-id="b8c75-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="b8c75-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b8c75-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="b8c75-123">Specifica un prefisso per l'indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b8c75-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="b8c75-124">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b8c75-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b8c75-125">Un indirizzo CIDR (classe Interdomain Routing)</span><span class="sxs-lookup"><span data-stu-id="b8c75-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="b8c75-126">Un intervallo di indirizzi IP di destinazione</span><span class="sxs-lookup"><span data-stu-id="b8c75-126">A destination IP address range</span></span> 
- <span data-ttu-id="b8c75-127">Carattere jolly (\*) che corrisponde a qualsiasi indirizzo IP</span><span class="sxs-lookup"><span data-stu-id="b8c75-127">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="b8c75-128">È possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="b8c75-128">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="b8c75-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b8c75-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="b8c75-130">Gruppo di sicurezza dell'applicazione impostato come destinazione per la regola.</span><span class="sxs-lookup"><span data-stu-id="b8c75-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="b8c75-131">Non può essere usato con il parametro "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="b8c75-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="b8c75-132">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="b8c75-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="b8c75-133">Gruppo di sicurezza dell'applicazione impostato come destinazione per la regola.</span><span class="sxs-lookup"><span data-stu-id="b8c75-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="b8c75-134">Non può essere usato con il parametro "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="b8c75-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="b8c75-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="b8c75-135">-DestinationPortRange</span></span>
<span data-ttu-id="b8c75-136">Specifica una porta o un intervallo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b8c75-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="b8c75-137">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b8c75-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b8c75-138">Un numero intero</span><span class="sxs-lookup"><span data-stu-id="b8c75-138">An integer</span></span>
- <span data-ttu-id="b8c75-139">Un intervallo di numeri interi compresi tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="b8c75-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="b8c75-140">Carattere jolly (\*) che corrisponde a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="b8c75-140">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="b8c75-141">-Direzione</span><span class="sxs-lookup"><span data-stu-id="b8c75-141">-Direction</span></span>
<span data-ttu-id="b8c75-142">Specifica se una regola viene valutata nel traffico in entrata o in uscita.</span><span class="sxs-lookup"><span data-stu-id="b8c75-142">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="b8c75-143">I valori accettabili per questo parametro sono: in ingresso e in uscita.</span><span class="sxs-lookup"><span data-stu-id="b8c75-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="b8c75-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8c75-144">-Name</span></span>
<span data-ttu-id="b8c75-145">Specifica il nome della configurazione della regola di sicurezza della rete creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8c75-145">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b8c75-146">-Priorità</span><span class="sxs-lookup"><span data-stu-id="b8c75-146">-Priority</span></span>
<span data-ttu-id="b8c75-147">Specifica la priorità di una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="b8c75-147">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="b8c75-148">I valori accettabili per questo parametro sono: un numero intero compreso tra 100 e 4096.</span><span class="sxs-lookup"><span data-stu-id="b8c75-148">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>

<span data-ttu-id="b8c75-149">Il numero di priorità deve essere univoco per ogni regola della raccolta.</span><span class="sxs-lookup"><span data-stu-id="b8c75-149">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="b8c75-150">Minore è il numero di priorità, maggiore è la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="b8c75-150">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="b8c75-151">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="b8c75-151">-Protocol</span></span>
<span data-ttu-id="b8c75-152">Specifica il protocollo di rete a cui si applica una nuova configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="b8c75-152">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="b8c75-153">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b8c75-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b8c75-154">TCP</span><span class="sxs-lookup"><span data-stu-id="b8c75-154">Tcp</span></span>
- <span data-ttu-id="b8c75-155">UDP</span><span class="sxs-lookup"><span data-stu-id="b8c75-155">Udp</span></span>
- <span data-ttu-id="b8c75-156">carattere jolly (\*) in modo che corrisponda a entrambi.</span><span class="sxs-lookup"><span data-stu-id="b8c75-156">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="b8c75-157">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b8c75-157">-SourceAddressPrefix</span></span>
<span data-ttu-id="b8c75-158">Specifica un prefisso per l'indirizzo di origine.</span><span class="sxs-lookup"><span data-stu-id="b8c75-158">Specifies a source address prefix.</span></span>
<span data-ttu-id="b8c75-159">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b8c75-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b8c75-160">UN CIDR</span><span class="sxs-lookup"><span data-stu-id="b8c75-160">A CIDR</span></span>
- <span data-ttu-id="b8c75-161">Un intervallo IP di origine</span><span class="sxs-lookup"><span data-stu-id="b8c75-161">A source IP range</span></span>
- <span data-ttu-id="b8c75-162">Un carattere jolly (\*) per corrispondere a qualsiasi indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="b8c75-162">A wildcard character (\*) to match any IP address.</span></span>

<span data-ttu-id="b8c75-163">È anche possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="b8c75-163">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="b8c75-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b8c75-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="b8c75-165">Gruppo di sicurezza dell'applicazione impostato come origine per la regola.</span><span class="sxs-lookup"><span data-stu-id="b8c75-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="b8c75-166">Non può essere usato con il parametro "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="b8c75-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="b8c75-167">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="b8c75-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="b8c75-168">Gruppo di sicurezza dell'applicazione impostato come origine per la regola.</span><span class="sxs-lookup"><span data-stu-id="b8c75-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="b8c75-169">Non può essere usato con il parametro "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="b8c75-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="b8c75-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="b8c75-170">-SourcePortRange</span></span>
<span data-ttu-id="b8c75-171">Specifica la porta o l'intervallo di origine.</span><span class="sxs-lookup"><span data-stu-id="b8c75-171">Specifies the source port or range.</span></span>
<span data-ttu-id="b8c75-172">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b8c75-172">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b8c75-173">Un numero intero</span><span class="sxs-lookup"><span data-stu-id="b8c75-173">An integer</span></span>
- <span data-ttu-id="b8c75-174">Un intervallo di numeri interi compresi tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="b8c75-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="b8c75-175">Carattere jolly (\*) che corrisponde a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="b8c75-175">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="b8c75-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c75-176">CommonParameters</span></span>
<span data-ttu-id="b8c75-177">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8c75-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c75-178">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8c75-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c75-179">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b8c75-179">INPUTS</span></span>

### <span data-ttu-id="b8c75-180">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b8c75-180">None</span></span>
<span data-ttu-id="b8c75-181">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b8c75-181">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b8c75-182">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b8c75-182">OUTPUTS</span></span>

### <span data-ttu-id="b8c75-183">Microsoft. Azure. Commands. Network. Models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="b8c75-183">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="b8c75-184">Note</span><span class="sxs-lookup"><span data-stu-id="b8c75-184">NOTES</span></span>

## <span data-ttu-id="b8c75-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b8c75-185">RELATED LINKS</span></span>

[<span data-ttu-id="b8c75-186">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b8c75-186">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b8c75-187">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b8c75-187">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b8c75-188">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b8c75-188">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b8c75-189">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b8c75-189">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


