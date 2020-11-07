---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 657a03dbf69df1fe11cf0ceff1c5f594cabc9b41
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860481"
---
# <span data-ttu-id="c23ba-101">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c23ba-101">New-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="c23ba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c23ba-102">SYNOPSIS</span></span>
<span data-ttu-id="c23ba-103">Crea una configurazione di regola per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c23ba-103">Creates a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="c23ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c23ba-104">SYNTAX</span></span>

### <span data-ttu-id="c23ba-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c23ba-105">SetByResourceId</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c23ba-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c23ba-106">SetByResource</span></span>
```
New-AzLoadBalancerRuleConfig -Name <String> [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c23ba-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c23ba-107">DESCRIPTION</span></span>
<span data-ttu-id="c23ba-108">Il cmdlet **New-AzLoadBalancerRuleConfig** crea una configurazione di regola per un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="c23ba-108">The **New-AzLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="c23ba-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c23ba-109">EXAMPLES</span></span>

### <span data-ttu-id="c23ba-110">1: creazione di una configurazione di regola per un bilanciamento del carico di Azure</span><span class="sxs-lookup"><span data-stu-id="c23ba-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
```
PS C:\>  $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" 
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzLoadBalancerFrontendIpConfig -Name MyFrontEnd 
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port 
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration 
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp 
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP 
    -LoadDistribution SourceIP
```

<span data-ttu-id="c23ba-111">I primi tre comandi configurano un IP pubblico, un front-end e una sonda per la configurazione della regola nel comando avanti.</span><span class="sxs-lookup"><span data-stu-id="c23ba-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="c23ba-112">Il comando avanti crea una nuova regola denominata MyLBrule con determinate specifiche.</span><span class="sxs-lookup"><span data-stu-id="c23ba-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="c23ba-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c23ba-113">PARAMETERS</span></span>

### <span data-ttu-id="c23ba-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c23ba-114">-BackendAddressPool</span></span>
<span data-ttu-id="c23ba-115">Specifica un oggetto **BackendAddressPool** da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c23ba-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23ba-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c23ba-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="c23ba-117">Specifica l'ID di un oggetto **BackendAddressPool** da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c23ba-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23ba-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="c23ba-118">-BackendPort</span></span>
<span data-ttu-id="c23ba-119">Specifica la porta backend per il traffico che corrisponde alla configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c23ba-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c23ba-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c23ba-120">-DefaultProfile</span></span>
<span data-ttu-id="c23ba-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c23ba-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c23ba-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="c23ba-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="c23ba-123">Configura SNAT per le VM nel pool back-end per usare l'indirizzo publicIP specificato nel frontend della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c23ba-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23ba-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="c23ba-124">-EnableFloatingIP</span></span>
<span data-ttu-id="c23ba-125">Indica che questo cmdlet Abilita un indirizzo IP mobile per una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="c23ba-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23ba-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c23ba-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="c23ba-127">Specifica un elenco di indirizzi IP front-end da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c23ba-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23ba-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c23ba-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="c23ba-129">Specifica l'ID per una configurazione di indirizzi IP front-end.</span><span class="sxs-lookup"><span data-stu-id="c23ba-129">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23ba-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="c23ba-130">-FrontendPort</span></span>
<span data-ttu-id="c23ba-131">Specifica la porta front-end corrispondente alla configurazione di una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c23ba-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="c23ba-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c23ba-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c23ba-133">Specifica il periodo di tempo, in minuti, in cui lo stato delle conversazioni viene mantenuto in un punto di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c23ba-133">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="c23ba-134">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="c23ba-134">-LoadDistribution</span></span>
<span data-ttu-id="c23ba-135">Specifica una distribuzione del carico.</span><span class="sxs-lookup"><span data-stu-id="c23ba-135">Specifies a load distribution.</span></span>
<span data-ttu-id="c23ba-136">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c23ba-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c23ba-137">Predefinita</span><span class="sxs-lookup"><span data-stu-id="c23ba-137">Default</span></span>
- <span data-ttu-id="c23ba-138">SourceIP</span><span class="sxs-lookup"><span data-stu-id="c23ba-138">SourceIP</span></span>
- <span data-ttu-id="c23ba-139">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="c23ba-139">SourceIPProtocol</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Default, SourceIP, SourceIPProtocol

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23ba-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="c23ba-140">-Name</span></span>
<span data-ttu-id="c23ba-141">Specifica il nome della regola di bilanciamento del carico creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c23ba-141">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c23ba-142">-Probe</span><span class="sxs-lookup"><span data-stu-id="c23ba-142">-Probe</span></span>
<span data-ttu-id="c23ba-143">Specifica una sonda da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c23ba-143">Specifies a probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSProbe
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23ba-144">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="c23ba-144">-ProbeId</span></span>
<span data-ttu-id="c23ba-145">Specifica l'ID del Probe da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c23ba-145">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23ba-146">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="c23ba-146">-Protocol</span></span>
<span data-ttu-id="c23ba-147">Specifica il protocollo corrispondente alla configurazione di una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c23ba-147">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="c23ba-148">I valori accettabili per questo parametro sono: TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="c23ba-148">The acceptable values for this parameter are: Tcp or Udp.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c23ba-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c23ba-149">CommonParameters</span></span>
<span data-ttu-id="c23ba-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c23ba-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c23ba-151">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c23ba-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c23ba-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c23ba-152">INPUTS</span></span>

## <span data-ttu-id="c23ba-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c23ba-153">OUTPUTS</span></span>

### <span data-ttu-id="c23ba-154">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="c23ba-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="c23ba-155">Note</span><span class="sxs-lookup"><span data-stu-id="c23ba-155">NOTES</span></span>

## <span data-ttu-id="c23ba-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c23ba-156">RELATED LINKS</span></span>

[<span data-ttu-id="c23ba-157">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c23ba-157">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="c23ba-158">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c23ba-158">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="c23ba-159">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c23ba-159">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="c23ba-160">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c23ba-160">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


