---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FD84D530-491B-4075-A6B4-2E1C46AD92D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerruleconfig
schema: 2.0.0
ms.openlocfilehash: f3e256def28dff292efc5ba4278dc4f56b3ec721
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867014"
---
# <span data-ttu-id="210ef-101">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="210ef-101">New-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="210ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="210ef-102">SYNOPSIS</span></span>
<span data-ttu-id="210ef-103">Crea una configurazione di regola per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="210ef-103">Creates a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="210ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="210ef-104">SYNTAX</span></span>

### <span data-ttu-id="210ef-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="210ef-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-BackendAddressPoolId <String>] [-ProbeId <String>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="210ef-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="210ef-106">SetByResource</span></span>
```
New-AzureRmLoadBalancerRuleConfig -Name <String> [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-BackendAddressPool <PSBackendAddressPool>] [-Probe <PSProbe>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-LoadDistribution <String>] [-EnableFloatingIP]
 [-DisableOutboundSNAT] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="210ef-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="210ef-107">DESCRIPTION</span></span>
<span data-ttu-id="210ef-108">Il cmdlet **New-AzureRmLoadBalancerRuleConfig** crea una configurazione di regola per un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="210ef-108">The **New-AzureRmLoadBalancerRuleConfig** cmdlet creates a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="210ef-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="210ef-109">EXAMPLES</span></span>

### <span data-ttu-id="210ef-110">1: creazione di una configurazione di regola per un bilanciamento del carico di Azure</span><span class="sxs-lookup"><span data-stu-id="210ef-110">1: Creating a rule configuration for an Azure Load Balancer</span></span>
```
PS C:\>  $publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" 
    -name MyPublicIP -location 'West US' -AllocationMethod Dynamic
PS C:\>  $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name MyFrontEnd 
    -PublicIpAddress $publicip
PS C:\>  $probe = New-AzureRmLoadBalancerProbeConfig -Name MyProbe -Protocol http -Port 
    80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath healthcheck.aspx
PS C:\> New-AzureRmLoadBalancerRuleConfig -Name "MyLBrule" -FrontendIPConfiguration 
    $frontend -BackendAddressPool $backendAddressPool -Probe $probe -Protocol Tcp 
    -FrontendPort 80 -BackendPort 80 -IdleTimeoutInMinutes 15 -EnableFloatingIP 
    -LoadDistribution SourceIP
```

<span data-ttu-id="210ef-111">I primi tre comandi configurano un IP pubblico, un front-end e una sonda per la configurazione della regola nel comando avanti.</span><span class="sxs-lookup"><span data-stu-id="210ef-111">The first three commands set up a public IP, a front end, and a probe for the rule configuration in the forth command.</span></span> <span data-ttu-id="210ef-112">Il comando avanti crea una nuova regola denominata MyLBrule con determinate specifiche.</span><span class="sxs-lookup"><span data-stu-id="210ef-112">The forth command creates a new rule called MyLBrule with certain specifications.</span></span>

## <span data-ttu-id="210ef-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="210ef-113">PARAMETERS</span></span>

### <span data-ttu-id="210ef-114">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="210ef-114">-BackendAddressPool</span></span>
<span data-ttu-id="210ef-115">Specifica un oggetto **BackendAddressPool** da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="210ef-115">Specifies a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="210ef-116">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="210ef-116">-BackendAddressPoolId</span></span>
<span data-ttu-id="210ef-117">Specifica l'ID di un oggetto **BackendAddressPool** da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="210ef-117">Specifies the ID of a **BackendAddressPool** object to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="210ef-118">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="210ef-118">-BackendPort</span></span>
<span data-ttu-id="210ef-119">Specifica la porta backend per il traffico che corrisponde alla configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="210ef-119">Specifies the backend port for traffic that is matched by this load balancer rule configuration.</span></span>

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

### <span data-ttu-id="210ef-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="210ef-120">-DefaultProfile</span></span>
<span data-ttu-id="210ef-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="210ef-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="210ef-122">-DisableOutboundSNAT</span><span class="sxs-lookup"><span data-stu-id="210ef-122">-DisableOutboundSNAT</span></span>
<span data-ttu-id="210ef-123">Configura SNAT per le VM nel pool back-end per usare l'indirizzo publicIP specificato nel frontend della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="210ef-123">Configures SNAT for the VMs in the backend pool to use the publicIP address specified in the frontend of the load balancing rule.</span></span>

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

### <span data-ttu-id="210ef-124">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="210ef-124">-EnableFloatingIP</span></span>
<span data-ttu-id="210ef-125">Indica che questo cmdlet Abilita un indirizzo IP mobile per una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="210ef-125">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="210ef-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="210ef-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="210ef-127">Specifica un elenco di indirizzi IP front-end da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="210ef-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="210ef-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="210ef-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="210ef-129">Specifica l'ID per una configurazione di indirizzi IP front-end.</span><span class="sxs-lookup"><span data-stu-id="210ef-129">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="210ef-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="210ef-130">-FrontendPort</span></span>
<span data-ttu-id="210ef-131">Specifica la porta front-end corrispondente alla configurazione di una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="210ef-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="210ef-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="210ef-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="210ef-133">Specifica il periodo di tempo, in minuti, in cui lo stato delle conversazioni viene mantenuto in un punto di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="210ef-133">Specifies the length of time, in minutes, that the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="210ef-134">-LoadDistribution</span><span class="sxs-lookup"><span data-stu-id="210ef-134">-LoadDistribution</span></span>
<span data-ttu-id="210ef-135">Specifica una distribuzione del carico.</span><span class="sxs-lookup"><span data-stu-id="210ef-135">Specifies a load distribution.</span></span>
<span data-ttu-id="210ef-136">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="210ef-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="210ef-137">Predefinita</span><span class="sxs-lookup"><span data-stu-id="210ef-137">Default</span></span>
- <span data-ttu-id="210ef-138">SourceIP</span><span class="sxs-lookup"><span data-stu-id="210ef-138">SourceIP</span></span>
- <span data-ttu-id="210ef-139">SourceIPProtocol</span><span class="sxs-lookup"><span data-stu-id="210ef-139">SourceIPProtocol</span></span>

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

### <span data-ttu-id="210ef-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="210ef-140">-Name</span></span>
<span data-ttu-id="210ef-141">Specifica il nome della regola di bilanciamento del carico creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="210ef-141">Specifies the name of the load balancing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="210ef-142">-Probe</span><span class="sxs-lookup"><span data-stu-id="210ef-142">-Probe</span></span>
<span data-ttu-id="210ef-143">Specifica una sonda da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="210ef-143">Specifies a probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="210ef-144">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="210ef-144">-ProbeId</span></span>
<span data-ttu-id="210ef-145">Specifica l'ID del Probe da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="210ef-145">Specifies the ID of the probe to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="210ef-146">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="210ef-146">-Protocol</span></span>
<span data-ttu-id="210ef-147">Specifica il protocollo corrispondente alla configurazione di una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="210ef-147">Specifies the protocol that is matched by a load balancer rule configuration.</span></span>
<span data-ttu-id="210ef-148">I valori accettabili per questo parametro sono: TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="210ef-148">The acceptable values for this parameter are: Tcp or Udp.</span></span>

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

### <span data-ttu-id="210ef-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="210ef-149">CommonParameters</span></span>
<span data-ttu-id="210ef-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="210ef-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="210ef-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="210ef-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="210ef-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="210ef-152">INPUTS</span></span>

## <span data-ttu-id="210ef-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="210ef-153">OUTPUTS</span></span>

### <span data-ttu-id="210ef-154">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="210ef-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="210ef-155">Note</span><span class="sxs-lookup"><span data-stu-id="210ef-155">NOTES</span></span>

## <span data-ttu-id="210ef-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="210ef-156">RELATED LINKS</span></span>

[<span data-ttu-id="210ef-157">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="210ef-157">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="210ef-158">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="210ef-158">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="210ef-159">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="210ef-159">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="210ef-160">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="210ef-160">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


