---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 633FB5C9-BEB3-42A3-AF4F-A54CC3F9E0F7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworksecurityruleconfig
schema: 2.0.0
ms.openlocfilehash: 34397a467cb25a6b93963f8944096975663ccf5a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866483"
---
# <span data-ttu-id="035dc-101">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="035dc-101">New-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="035dc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="035dc-102">SYNOPSIS</span></span>
<span data-ttu-id="035dc-103">Crea una configurazione della regola di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="035dc-103">Creates a network security rule configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="035dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="035dc-104">SYNTAX</span></span>

### <span data-ttu-id="035dc-105">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="035dc-105">SetByResource (Default)</span></span>
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

### <span data-ttu-id="035dc-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="035dc-106">SetByResourceId</span></span>
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

## <span data-ttu-id="035dc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="035dc-107">DESCRIPTION</span></span>
<span data-ttu-id="035dc-108">Il cmdlet **New-AzureRmNetworkSecurityRuleConfig** crea una configurazione della regola di sicurezza di rete Azure per un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="035dc-108">The **New-AzureRmNetworkSecurityRuleConfig** cmdlet creates an Azure network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="035dc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="035dc-109">EXAMPLES</span></span>

### <span data-ttu-id="035dc-110">1: creare una regola di sicurezza della rete per consentire RDP</span><span class="sxs-lookup"><span data-stu-id="035dc-110">1: Create a network security rule to allow RDP</span></span>
```
$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
```

<span data-ttu-id="035dc-111">Questo comando crea una regola di sicurezza che consente l'accesso da Internet alla porta 3389</span><span class="sxs-lookup"><span data-stu-id="035dc-111">This command creates a security rule allowing access from the Internet to port 3389</span></span>

### <span data-ttu-id="035dc-112">2: creare una regola di sicurezza di rete che consente l'HTTP</span><span class="sxs-lookup"><span data-stu-id="035dc-112">2: Create a network security rule that allows HTTP</span></span>
```
$rule2 = New-AzureRmNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" 
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix 
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80
```

<span data-ttu-id="035dc-113">Questo comando crea una regola di sicurezza che consente l'accesso da Internet alla porta 80</span><span class="sxs-lookup"><span data-stu-id="035dc-113">This command creates a security rule allowing access from the Internet to port 80</span></span>

## <span data-ttu-id="035dc-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="035dc-114">PARAMETERS</span></span>

### <span data-ttu-id="035dc-115">-Access</span><span class="sxs-lookup"><span data-stu-id="035dc-115">-Access</span></span>
<span data-ttu-id="035dc-116">Specifica se il traffico di rete è consentito o negato.</span><span class="sxs-lookup"><span data-stu-id="035dc-116">Specifies whether network traffic is allowed or denied.</span></span>
<span data-ttu-id="035dc-117">I valori accettabili per questo parametro sono: Allow e Deny.</span><span class="sxs-lookup"><span data-stu-id="035dc-117">The acceptable values for this parameter are: Allow and Deny.</span></span>

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

### <span data-ttu-id="035dc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="035dc-118">-DefaultProfile</span></span>
<span data-ttu-id="035dc-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="035dc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="035dc-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="035dc-120">-Description</span></span>
<span data-ttu-id="035dc-121">Specifica una descrizione della configurazione della regola di sicurezza della rete da creare.</span><span class="sxs-lookup"><span data-stu-id="035dc-121">Specifies a description of the network security rule configuration to create.</span></span>

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

### <span data-ttu-id="035dc-122">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="035dc-122">-DestinationAddressPrefix</span></span>
<span data-ttu-id="035dc-123">Specifica un prefisso per l'indirizzo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="035dc-123">Specifies a destination address prefix.</span></span>
<span data-ttu-id="035dc-124">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="035dc-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="035dc-125">Un indirizzo CIDR (classe Interdomain Routing)</span><span class="sxs-lookup"><span data-stu-id="035dc-125">A Classless Interdomain Routing (CIDR) address</span></span> 
- <span data-ttu-id="035dc-126">Un intervallo di indirizzi IP di destinazione</span><span class="sxs-lookup"><span data-stu-id="035dc-126">A destination IP address range</span></span> 
- <span data-ttu-id="035dc-127">Carattere jolly (\*) che corrisponde a qualsiasi indirizzo IP</span><span class="sxs-lookup"><span data-stu-id="035dc-127">A wildcard character (\*) to match any IP address</span></span>

<span data-ttu-id="035dc-128">È possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="035dc-128">You can use tags such as VirtualNetwork, AzureLoadBalancer, and Internet.</span></span>

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

### <span data-ttu-id="035dc-129">-DestinationApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="035dc-129">-DestinationApplicationSecurityGroup</span></span>
<span data-ttu-id="035dc-130">Gruppo di sicurezza dell'applicazione impostato come destinazione per la regola.</span><span class="sxs-lookup"><span data-stu-id="035dc-130">The application security group set as destination for the rule.</span></span> <span data-ttu-id="035dc-131">Non può essere usato con il parametro "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="035dc-131">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="035dc-132">-DestinationApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="035dc-132">-DestinationApplicationSecurityGroupId</span></span>
<span data-ttu-id="035dc-133">Gruppo di sicurezza dell'applicazione impostato come destinazione per la regola.</span><span class="sxs-lookup"><span data-stu-id="035dc-133">The application security group set as destination for the rule.</span></span> <span data-ttu-id="035dc-134">Non può essere usato con il parametro "DestinationAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="035dc-134">It cannot be used with 'DestinationAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="035dc-135">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="035dc-135">-DestinationPortRange</span></span>
<span data-ttu-id="035dc-136">Specifica una porta o un intervallo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="035dc-136">Specifies a destination port or range.</span></span>
<span data-ttu-id="035dc-137">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="035dc-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="035dc-138">Un numero intero</span><span class="sxs-lookup"><span data-stu-id="035dc-138">An integer</span></span>
- <span data-ttu-id="035dc-139">Un intervallo di numeri interi compresi tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="035dc-139">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="035dc-140">Carattere jolly (\*) che corrisponde a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="035dc-140">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="035dc-141">-Direzione</span><span class="sxs-lookup"><span data-stu-id="035dc-141">-Direction</span></span>
<span data-ttu-id="035dc-142">Specifica se una regola viene valutata nel traffico in entrata o in uscita.</span><span class="sxs-lookup"><span data-stu-id="035dc-142">Specifies whether a rule is evaluated on incoming or outgoing traffic.</span></span>
<span data-ttu-id="035dc-143">I valori accettabili per questo parametro sono: in ingresso e in uscita.</span><span class="sxs-lookup"><span data-stu-id="035dc-143">The acceptable values for this parameter are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="035dc-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="035dc-144">-Name</span></span>
<span data-ttu-id="035dc-145">Specifica il nome della configurazione della regola di sicurezza della rete creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="035dc-145">Specifies the name of the network security rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="035dc-146">-Priorità</span><span class="sxs-lookup"><span data-stu-id="035dc-146">-Priority</span></span>
<span data-ttu-id="035dc-147">Specifica la priorità di una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="035dc-147">Specifies the priority of a rule configuration.</span></span>
<span data-ttu-id="035dc-148">I valori accettabili per questo parametro sono: un numero intero compreso tra 100 e 4096.</span><span class="sxs-lookup"><span data-stu-id="035dc-148">The acceptable values for this parameter are: An integer between 100 and 4096.</span></span>

<span data-ttu-id="035dc-149">Il numero di priorità deve essere univoco per ogni regola della raccolta.</span><span class="sxs-lookup"><span data-stu-id="035dc-149">The priority number must be unique for each rule in the collection.</span></span>
<span data-ttu-id="035dc-150">Minore è il numero di priorità, maggiore è la priorità della regola.</span><span class="sxs-lookup"><span data-stu-id="035dc-150">The lower the priority number, the higher the priority of the rule.</span></span>

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

### <span data-ttu-id="035dc-151">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="035dc-151">-Protocol</span></span>
<span data-ttu-id="035dc-152">Specifica il protocollo di rete a cui si applica una nuova configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="035dc-152">Specifies the network protocol that a new rule configuration applies to.</span></span>
<span data-ttu-id="035dc-153">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="035dc-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="035dc-154">TCP</span><span class="sxs-lookup"><span data-stu-id="035dc-154">Tcp</span></span>
- <span data-ttu-id="035dc-155">UDP</span><span class="sxs-lookup"><span data-stu-id="035dc-155">Udp</span></span>
- <span data-ttu-id="035dc-156">carattere jolly (\*) in modo che corrisponda a entrambi.</span><span class="sxs-lookup"><span data-stu-id="035dc-156">wildcard character (\*) to match both.</span></span>

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

### <span data-ttu-id="035dc-157">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="035dc-157">-SourceAddressPrefix</span></span>
<span data-ttu-id="035dc-158">Specifica un prefisso per l'indirizzo di origine.</span><span class="sxs-lookup"><span data-stu-id="035dc-158">Specifies a source address prefix.</span></span>
<span data-ttu-id="035dc-159">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="035dc-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="035dc-160">UN CIDR</span><span class="sxs-lookup"><span data-stu-id="035dc-160">A CIDR</span></span>
- <span data-ttu-id="035dc-161">Un intervallo IP di origine</span><span class="sxs-lookup"><span data-stu-id="035dc-161">A source IP range</span></span>
- <span data-ttu-id="035dc-162">Un carattere jolly (\*) per corrispondere a qualsiasi indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="035dc-162">A wildcard character (\*) to match any IP address.</span></span>

<span data-ttu-id="035dc-163">È anche possibile usare tag come VirtualNetwork, AzureLoadBalancer e Internet.</span><span class="sxs-lookup"><span data-stu-id="035dc-163">You can also use tags such as VirtualNetwork, AzureLoadBalancer and Internet.</span></span>

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

### <span data-ttu-id="035dc-164">-SourceApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="035dc-164">-SourceApplicationSecurityGroup</span></span>
<span data-ttu-id="035dc-165">Gruppo di sicurezza dell'applicazione impostato come origine per la regola.</span><span class="sxs-lookup"><span data-stu-id="035dc-165">The application security group set as source for the rule.</span></span> <span data-ttu-id="035dc-166">Non può essere usato con il parametro "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="035dc-166">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="035dc-167">-SourceApplicationSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="035dc-167">-SourceApplicationSecurityGroupId</span></span>
<span data-ttu-id="035dc-168">Gruppo di sicurezza dell'applicazione impostato come origine per la regola.</span><span class="sxs-lookup"><span data-stu-id="035dc-168">The application security group set as source for the rule.</span></span> <span data-ttu-id="035dc-169">Non può essere usato con il parametro "SourceAddressPrefix".</span><span class="sxs-lookup"><span data-stu-id="035dc-169">It cannot be used with 'SourceAddressPrefix' parameter.</span></span>

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

### <span data-ttu-id="035dc-170">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="035dc-170">-SourcePortRange</span></span>
<span data-ttu-id="035dc-171">Specifica la porta o l'intervallo di origine.</span><span class="sxs-lookup"><span data-stu-id="035dc-171">Specifies the source port or range.</span></span>
<span data-ttu-id="035dc-172">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="035dc-172">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="035dc-173">Un numero intero</span><span class="sxs-lookup"><span data-stu-id="035dc-173">An integer</span></span>
- <span data-ttu-id="035dc-174">Un intervallo di numeri interi compresi tra 0 e 65535</span><span class="sxs-lookup"><span data-stu-id="035dc-174">A range of integers between 0 and 65535</span></span>
- <span data-ttu-id="035dc-175">Carattere jolly (\*) che corrisponde a qualsiasi porta</span><span class="sxs-lookup"><span data-stu-id="035dc-175">A wildcard character (\*) to match any port</span></span>

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

### <span data-ttu-id="035dc-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="035dc-176">CommonParameters</span></span>
<span data-ttu-id="035dc-177">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="035dc-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="035dc-178">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="035dc-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="035dc-179">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="035dc-179">INPUTS</span></span>

## <span data-ttu-id="035dc-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="035dc-180">OUTPUTS</span></span>

### <span data-ttu-id="035dc-181">Microsoft. Azure. Commands. Network. Models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="035dc-181">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="035dc-182">Note</span><span class="sxs-lookup"><span data-stu-id="035dc-182">NOTES</span></span>

## <span data-ttu-id="035dc-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="035dc-183">RELATED LINKS</span></span>

[<span data-ttu-id="035dc-184">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="035dc-184">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="035dc-185">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="035dc-185">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="035dc-186">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="035dc-186">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="035dc-187">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="035dc-187">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


