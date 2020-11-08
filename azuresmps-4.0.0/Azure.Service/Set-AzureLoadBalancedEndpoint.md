---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7259C717-250C-454A-B0DF-738B70747FF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 298633bbc95bfb13ae340dea242c6c04267d479e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023911"
---
# <span data-ttu-id="81b73-101">Set-AzureLoadBalancedEndpoint</span><span class="sxs-lookup"><span data-stu-id="81b73-101">Set-AzureLoadBalancedEndpoint</span></span>

## <span data-ttu-id="81b73-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="81b73-102">SYNOPSIS</span></span>
<span data-ttu-id="81b73-103">Modifica tutti gli endpoint in un set di bilanciamento del carico all'interno di un servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="81b73-103">Modifies all of the endpoints in a load balancer set within an Azure service.</span></span>

## <span data-ttu-id="81b73-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81b73-104">SYNTAX</span></span>

### <span data-ttu-id="81b73-105">DefaultProbe (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="81b73-105">DefaultProbe (Default)</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="81b73-106">TCPProbe</span><span class="sxs-lookup"><span data-stu-id="81b73-106">TCPProbe</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-ProbeProtocolTCP]
 [-ProbePort <Int32>] [-ProbeIntervalInSeconds <Int32>] [-ProbeTimeoutInSeconds <Int32>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="81b73-107">HTTPProbe</span><span class="sxs-lookup"><span data-stu-id="81b73-107">HTTPProbe</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-ProbeProtocolHTTP]
 -ProbePath <String> [-ProbePort <Int32>] [-ProbeIntervalInSeconds <Int32>] [-ProbeTimeoutInSeconds <Int32>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="81b73-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81b73-108">DESCRIPTION</span></span>
<span data-ttu-id="81b73-109">Il cmdlet **set-AzureLoadBalancedEndpoint** modifica tutti gli endpoint in un set di bilanciamento del carico in un servizio Azure.</span><span class="sxs-lookup"><span data-stu-id="81b73-109">The **Set-AzureLoadBalancedEndpoint** cmdlet modifies all of the endpoints in a load balancer set in an Azure service.</span></span>

## <span data-ttu-id="81b73-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81b73-110">EXAMPLES</span></span>

### <span data-ttu-id="81b73-111">Esempio 1: modificare gli endpoint in un set di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="81b73-111">Example 1: Modify the endpoints in a load balancer set</span></span>
```
PS C:\> Set-AzureLoadBalancedEndpoint -ServiceName "ContosoService" -LBSetName "LBSet01" -Protocol "TCP" -LocalPort 80 -ProbeProtocolTCP -ProbePort 8080
```

<span data-ttu-id="81b73-112">Questo comando modifica tutti gli endpoint nel set di bilanciamento del carico denominato LBSet01 per usare il protocollo TCP e la porta privata 80.</span><span class="sxs-lookup"><span data-stu-id="81b73-112">This command modifies all endpoints in the load balancer set named LBSet01 to use the TCP protocol and private port 80.</span></span>
<span data-ttu-id="81b73-113">Il comando imposta la sonda di bilanciamento del carico per usare il protocollo TCP sulla porta 8080.</span><span class="sxs-lookup"><span data-stu-id="81b73-113">The command sets the load balancer probe to use the TCP protocol on port 8080.</span></span>

### <span data-ttu-id="81b73-114">Esempio 2: specificare un IP virtuale diverso</span><span class="sxs-lookup"><span data-stu-id="81b73-114">Example 2: Specify a different virtual IP</span></span>
```
PS C:\> Set-AzureLoadBalancedEndpoint -ServiceName "ContosoService" -LBSetName "LBSet02" -VirtualIPName "Vip01"
```

<span data-ttu-id="81b73-115">Questo comando modifica il bilanciamento del carico con il nome del set di bilanciamento del carico per usare un IP virtuale denominato Vip01.</span><span class="sxs-lookup"><span data-stu-id="81b73-115">This command modifies the load balancer that has the load balancer set name to use a virtual IP named Vip01.</span></span>

## <span data-ttu-id="81b73-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="81b73-116">PARAMETERS</span></span>

### <span data-ttu-id="81b73-117">-ACL</span><span class="sxs-lookup"><span data-stu-id="81b73-117">-ACL</span></span>
<span data-ttu-id="81b73-118">Specifica un oggetto di configurazione dell'elenco di controllo di accesso (ACL) che questo cmdlet si applica agli endpoint.</span><span class="sxs-lookup"><span data-stu-id="81b73-118">Specifies an access control list (ACL) configuration object that this cmdlet applies to the endpoints.</span></span>

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b73-119">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="81b73-119">-DirectServerReturn</span></span>
<span data-ttu-id="81b73-120">Specifica se questo cmdlet Abilita il ritorno diretto del server.</span><span class="sxs-lookup"><span data-stu-id="81b73-120">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="81b73-121">Specificare $True da abilitare o $False da disabilitare.</span><span class="sxs-lookup"><span data-stu-id="81b73-121">Specify $True to enable, or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b73-122">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="81b73-122">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="81b73-123">Specifica il periodo di timeout inattività TCP, in minuti, per gli endpoint.</span><span class="sxs-lookup"><span data-stu-id="81b73-123">Specifies the TCP idle time-out period, in minutes, for the endpoints.</span></span>

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

### <span data-ttu-id="81b73-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="81b73-124">-InformationAction</span></span>
<span data-ttu-id="81b73-125">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="81b73-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="81b73-126">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="81b73-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="81b73-127">Continuare</span><span class="sxs-lookup"><span data-stu-id="81b73-127">Continue</span></span>
- <span data-ttu-id="81b73-128">Ignora</span><span class="sxs-lookup"><span data-stu-id="81b73-128">Ignore</span></span>
- <span data-ttu-id="81b73-129">Informarsi</span><span class="sxs-lookup"><span data-stu-id="81b73-129">Inquire</span></span>
- <span data-ttu-id="81b73-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="81b73-130">SilentlyContinue</span></span>
- <span data-ttu-id="81b73-131">Stop</span><span class="sxs-lookup"><span data-stu-id="81b73-131">Stop</span></span>
- <span data-ttu-id="81b73-132">Sospensione</span><span class="sxs-lookup"><span data-stu-id="81b73-132">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b73-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="81b73-133">-InformationVariable</span></span>
<span data-ttu-id="81b73-134">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="81b73-134">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b73-135">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="81b73-135">-InternalLoadBalancerName</span></span>
<span data-ttu-id="81b73-136">Specifica il nome del bilanciamento del carico interno che questo cmdlet include nella configurazione.</span><span class="sxs-lookup"><span data-stu-id="81b73-136">Specifies the name of the internal load balancer that this cmdlet includes in the configuration.</span></span>

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

### <span data-ttu-id="81b73-137">-LBSetName</span><span class="sxs-lookup"><span data-stu-id="81b73-137">-LBSetName</span></span>
<span data-ttu-id="81b73-138">Specifica il nome del set di bilanciamento del carico che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="81b73-138">Specifies the name of the load balancer set that this cmdlet updates.</span></span>

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

### <span data-ttu-id="81b73-139">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="81b73-139">-LoadBalancerDistribution</span></span>
<span data-ttu-id="81b73-140">Specifica l'algoritmo di distribuzione del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="81b73-140">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="81b73-141">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="81b73-141">Valid values are:</span></span> 

- <span data-ttu-id="81b73-142">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="81b73-142">sourceIP.</span></span>
<span data-ttu-id="81b73-143">Due affinità della tupla: IP di origine, IP di destinazione</span><span class="sxs-lookup"><span data-stu-id="81b73-143">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="81b73-144">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="81b73-144">sourceIPProtocol.</span></span>
<span data-ttu-id="81b73-145">Tre affinità della tupla: IP di origine, IP di destinazione, protocollo</span><span class="sxs-lookup"><span data-stu-id="81b73-145">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="81b73-146">nessuno.</span><span class="sxs-lookup"><span data-stu-id="81b73-146">none.</span></span>
<span data-ttu-id="81b73-147">Cinque affinità di tupla: IP di origine, porta di origine, IP di destinazione, porta di destinazione, protocollo</span><span class="sxs-lookup"><span data-stu-id="81b73-147">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="81b73-148">Il valore predefinito è None.</span><span class="sxs-lookup"><span data-stu-id="81b73-148">The default value is none.</span></span>

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

### <span data-ttu-id="81b73-149">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="81b73-149">-LocalPort</span></span>
<span data-ttu-id="81b73-150">Specifica la porta locale, privata, usata da questi endpoint.</span><span class="sxs-lookup"><span data-stu-id="81b73-150">Specifies the local, private, port that these endpoints use.</span></span>
<span data-ttu-id="81b73-151">Le applicazioni nella macchina virtuale ascoltano questa porta per le richieste di input del servizio per questo endpoint.</span><span class="sxs-lookup"><span data-stu-id="81b73-151">Applications in the virtual machine listen on this port for service input requests for this endpoint.</span></span>

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

### <span data-ttu-id="81b73-152">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="81b73-152">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="81b73-153">Specifica l'intervallo di polling Probe, in secondi, per gli endpoint.</span><span class="sxs-lookup"><span data-stu-id="81b73-153">Specifies the probe polling interval, in seconds, for the endpoints.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b73-154">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="81b73-154">-ProbePath</span></span>
<span data-ttu-id="81b73-155">Specifica il percorso relativo del probe HTTP.</span><span class="sxs-lookup"><span data-stu-id="81b73-155">Specifies the relative path of the HTTP Probe.</span></span>

```yaml
Type: String
Parameter Sets: HTTPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b73-156">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="81b73-156">-ProbePort</span></span>
<span data-ttu-id="81b73-157">Specifica la porta utilizzata dalla sonda di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="81b73-157">Specifies the port that the load balancer probe uses.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b73-158">-ProbeProtocolHTTP</span><span class="sxs-lookup"><span data-stu-id="81b73-158">-ProbeProtocolHTTP</span></span>
<span data-ttu-id="81b73-159">Specifica che gli endpoint di bilanciamento del carico usano un probe HTTP.</span><span class="sxs-lookup"><span data-stu-id="81b73-159">Specifies that the load balancer endpoints use an HTTP Probe.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: HTTPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b73-160">-ProbeProtocolTCP</span><span class="sxs-lookup"><span data-stu-id="81b73-160">-ProbeProtocolTCP</span></span>
<span data-ttu-id="81b73-161">Specifica che gli endpoint di bilanciamento del carico usano una sonda TCP.</span><span class="sxs-lookup"><span data-stu-id="81b73-161">Specifies that the load balancer endpoints use a TCP Probe.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: TCPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b73-162">-ProbeTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="81b73-162">-ProbeTimeoutInSeconds</span></span>
<span data-ttu-id="81b73-163">Specifica il timeout del polling delle sonde in pochi secondi.</span><span class="sxs-lookup"><span data-stu-id="81b73-163">Specifies the probe polling time-out in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b73-164">-Profile</span><span class="sxs-lookup"><span data-stu-id="81b73-164">-Profile</span></span>
<span data-ttu-id="81b73-165">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81b73-165">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="81b73-166">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="81b73-166">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81b73-167">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="81b73-167">-Protocol</span></span>
<span data-ttu-id="81b73-168">Specifica il protocollo degli endpoint.</span><span class="sxs-lookup"><span data-stu-id="81b73-168">Specifies the protocol of the endpoints.</span></span>
<span data-ttu-id="81b73-169">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="81b73-169">Valid values are:</span></span> 

- <span data-ttu-id="81b73-170">TCP</span><span class="sxs-lookup"><span data-stu-id="81b73-170">TCP</span></span> 
- <span data-ttu-id="81b73-171">UDP</span><span class="sxs-lookup"><span data-stu-id="81b73-171">UDP</span></span>

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

### <span data-ttu-id="81b73-172">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="81b73-172">-PublicPort</span></span>
<span data-ttu-id="81b73-173">Specifica la porta pubblica utilizzata dall'endpoint.</span><span class="sxs-lookup"><span data-stu-id="81b73-173">Specifies the public port that the endpoint uses.</span></span>
<span data-ttu-id="81b73-174">Se non specifichi un valore, Azure assegna una porta disponibile.</span><span class="sxs-lookup"><span data-stu-id="81b73-174">If you do not specify a value, Azure assigns an available port.</span></span>

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

### <span data-ttu-id="81b73-175">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="81b73-175">-ServiceName</span></span>
<span data-ttu-id="81b73-176">Specifica il nome del servizio Azure che contiene gli endpoint modificati da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81b73-176">Specifies the name of the Azure service that contains the endpoints that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81b73-177">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="81b73-177">-VirtualIPName</span></span>
<span data-ttu-id="81b73-178">Specifica il nome di un indirizzo IP virtuale che Azure associa agli endpoint.</span><span class="sxs-lookup"><span data-stu-id="81b73-178">Specifies the name of a virtual IP address that Azure associates to the endpoints.</span></span>
<span data-ttu-id="81b73-179">Per aggiungere indirizzi IP virtuali al servizio, usare il cmdlet **Add-AzureVirtualIP** .</span><span class="sxs-lookup"><span data-stu-id="81b73-179">To add virtual IPs to your service, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="81b73-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81b73-180">CommonParameters</span></span>
<span data-ttu-id="81b73-181">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81b73-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81b73-182">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81b73-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81b73-183">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="81b73-183">INPUTS</span></span>

## <span data-ttu-id="81b73-184">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81b73-184">OUTPUTS</span></span>

## <span data-ttu-id="81b73-185">Note</span><span class="sxs-lookup"><span data-stu-id="81b73-185">NOTES</span></span>

## <span data-ttu-id="81b73-186">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81b73-186">RELATED LINKS</span></span>

[<span data-ttu-id="81b73-187">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="81b73-187">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="81b73-188">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="81b73-188">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


