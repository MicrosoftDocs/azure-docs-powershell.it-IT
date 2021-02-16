---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: d2508b233bc67cb49d0a1c525f7e43ccf07242b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179638"
---
# <span data-ttu-id="cfa9b-101">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfa9b-101">New-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="cfa9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfa9b-102">SYNOPSIS</span></span>
<span data-ttu-id="cfa9b-103">Crea una configurazione della regola NAT in ingresso per una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="cfa9b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cfa9b-104">SYNTAX</span></span>

### <span data-ttu-id="cfa9b-105">SetByResource (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cfa9b-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfa9b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cfa9b-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cfa9b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cfa9b-107">DESCRIPTION</span></span>
<span data-ttu-id="cfa9b-108">Il cmdlet **New-AzLoadBalancerInboundNatRuleConfig** crea una configurazione della regola NAT (Network Address Translation) in ingresso per una bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-108">The **New-AzLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="cfa9b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cfa9b-109">EXAMPLES</span></span>

### <span data-ttu-id="cfa9b-110">Esempio 1: Creare una configurazione di regola NAT in ingresso per una bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="cfa9b-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="cfa9b-111">Il primo comando crea un indirizzo IP pubblico denominato MyPublicIP nel gruppo di risorse denominato MyResourceGroup e quindi lo archivia nella $publicip variabile.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="cfa9b-112">Il secondo comando crea una configurazione IP front-end denominata FrontendIpConfig01 usando l'indirizzo IP pubblico in $publicip e quindi la archivia nella variabile $frontend>.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="cfa9b-113">Il terzo comando crea una configurazione della regola NAT in ingresso denominata MyInboundNatRule usando l'oggetto front-end in $frontend.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="cfa9b-114">Il protocollo TCP viene specificato e la porta front-end è 3389, come in questo caso la porta back-end.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="cfa9b-115">I *parametri FrontendIpConfiguration,* *Protocol,* *FrontendPort* e *BackendPort* sono tutti necessari per creare una configurazione della regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-115">The *FrontendIpConfiguration*, *Protocol*, *FrontendPort*, and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="cfa9b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cfa9b-116">PARAMETERS</span></span>

### <span data-ttu-id="cfa9b-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="cfa9b-117">-BackendPort</span></span>
<span data-ttu-id="cfa9b-118">Specifica la porta back-end per il traffico corrispondente a questa configurazione della regola.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa9b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfa9b-119">-DefaultProfile</span></span>
<span data-ttu-id="cfa9b-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfa9b-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="cfa9b-121">-EnableFloatingIP</span></span>
<span data-ttu-id="cfa9b-122">Indica che questo cmdlet abilita un indirizzo IP mobile per la configurazione di una regola.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfa9b-123">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="cfa9b-123">-EnableTcpReset</span></span>
<span data-ttu-id="cfa9b-124">Ricevere la reimpostazione TCP bidirezionale in un timeout di inattività del flusso TCP o un'interruzione della connessione imprevista.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-124">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="cfa9b-125">Questo elemento viene usato solo quando il protocollo è impostato su TCP.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-125">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfa9b-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfa9b-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="cfa9b-127">Specifica un elenco di indirizzi IP front-end da associare a una configurazione di regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa9b-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="cfa9b-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="cfa9b-129">Specifica l'ID per una configurazione dell'indirizzo IP front-end.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-129">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa9b-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="cfa9b-130">-FrontendPort</span></span>
<span data-ttu-id="cfa9b-131">Specifica la porta front-end a cui corrisponde una configurazione di regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa9b-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="cfa9b-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="cfa9b-133">Specifica l'intervallo di tempo, in minuti, per il quale lo stato delle conversazioni viene gestito in una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa9b-134">-Name</span><span class="sxs-lookup"><span data-stu-id="cfa9b-134">-Name</span></span>
<span data-ttu-id="cfa9b-135">Specifica il nome della configurazione della regola creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-135">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="cfa9b-136">-Protocol</span><span class="sxs-lookup"><span data-stu-id="cfa9b-136">-Protocol</span></span>
<span data-ttu-id="cfa9b-137">Specifica un protocollo.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-137">Specifies a protocol.</span></span>
<span data-ttu-id="cfa9b-138">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="cfa9b-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cfa9b-139">Tcp</span><span class="sxs-lookup"><span data-stu-id="cfa9b-139">Tcp</span></span>
- <span data-ttu-id="cfa9b-140">Udp</span><span class="sxs-lookup"><span data-stu-id="cfa9b-140">Udp</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa9b-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cfa9b-141">-Confirm</span></span>
<span data-ttu-id="cfa9b-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfa9b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfa9b-143">-WhatIf</span></span>
<span data-ttu-id="cfa9b-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cfa9b-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfa9b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfa9b-146">CommonParameters</span></span>
<span data-ttu-id="cfa9b-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfa9b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfa9b-148">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfa9b-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfa9b-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="cfa9b-149">INPUTS</span></span>

### <span data-ttu-id="cfa9b-150">System.String</span><span class="sxs-lookup"><span data-stu-id="cfa9b-150">System.String</span></span>

### <span data-ttu-id="cfa9b-151">System.Int32</span><span class="sxs-lookup"><span data-stu-id="cfa9b-151">System.Int32</span></span>

### <span data-ttu-id="cfa9b-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfa9b-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="cfa9b-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cfa9b-153">OUTPUTS</span></span>

### <span data-ttu-id="cfa9b-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="cfa9b-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="cfa9b-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="cfa9b-155">NOTES</span></span>

## <span data-ttu-id="cfa9b-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cfa9b-156">RELATED LINKS</span></span>

[<span data-ttu-id="cfa9b-157">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfa9b-157">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="cfa9b-158">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfa9b-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="cfa9b-159">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cfa9b-159">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="cfa9b-160">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="cfa9b-160">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="cfa9b-161">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfa9b-161">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="cfa9b-162">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfa9b-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


