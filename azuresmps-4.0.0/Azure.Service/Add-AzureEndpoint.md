---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D767F017-6545-4BC6-927E-E7A99A08D5D2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b3122795f2af33a28206936b7b28322ad171b19
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023691"
---
# <span data-ttu-id="6df61-101">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="6df61-101">Add-AzureEndpoint</span></span>

## <span data-ttu-id="6df61-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6df61-102">SYNOPSIS</span></span>
<span data-ttu-id="6df61-103">Aggiunge un endpoint a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6df61-103">Adds an endpoint to a virtual machine.</span></span>

## <span data-ttu-id="6df61-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6df61-104">SYNTAX</span></span>

### <span data-ttu-id="6df61-105">NoLB (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6df61-105">NoLB (Default)</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6df61-106">LBNoProbe</span><span class="sxs-lookup"><span data-stu-id="6df61-106">LBNoProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> [-NoProbe]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6df61-107">LBDefaultProbe</span><span class="sxs-lookup"><span data-stu-id="6df61-107">LBDefaultProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> [-DefaultProbe]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6df61-108">LBCustomProbe</span><span class="sxs-lookup"><span data-stu-id="6df61-108">LBCustomProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> -ProbePort <Int32>
 -ProbeProtocol <String> [-ProbePath <String>] [-ProbeIntervalInSeconds <Int32>]
 [-ProbeTimeoutInSeconds <Int32>] [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadBalancerDistribution <String>] [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6df61-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6df61-109">DESCRIPTION</span></span>
<span data-ttu-id="6df61-110">Il cmdlet **Add-AzureEndpoint** aggiunge un endpoint a un oggetto macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="6df61-110">The **Add-AzureEndpoint** cmdlet adds an endpoint to an Azure virtual machine object.</span></span>

## <span data-ttu-id="6df61-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6df61-111">EXAMPLES</span></span>

### <span data-ttu-id="6df61-112">Esempio 1: aggiungere un endpoint</span><span class="sxs-lookup"><span data-stu-id="6df61-112">Example 1: Add an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 | Update-AzureVM
```

<span data-ttu-id="6df61-113">Questo comando Recupera la configurazione di una macchina virtuale denominata VirtualMachine01 usando il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="6df61-113">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="6df61-114">Il comando lo passa al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="6df61-114">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6df61-115">Questo cmdlet aggiunge un endpoint denominato Httpin.</span><span class="sxs-lookup"><span data-stu-id="6df61-115">This cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="6df61-116">L'endpoint ha una porta pubblica 80 e la porta locale 8080.</span><span class="sxs-lookup"><span data-stu-id="6df61-116">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="6df61-117">Il comando passa l'oggetto macchina virtuale al cmdlet **Update-AzureVM** , che implementa le modifiche.</span><span class="sxs-lookup"><span data-stu-id="6df61-117">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

### <span data-ttu-id="6df61-118">Esempio 2: aggiungere un endpoint appartenente a un gruppo di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="6df61-118">Example 2: Add an endpoint that belongs to a load balanced group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "LoadBalancedService" -Name "VirtualMachine12" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 -LBSetName "WebFarm" -ProbePort 80 -ProbeProtocol "http" -ProbePath '/' | Update-AzureVM
```

<span data-ttu-id="6df61-119">Questo comando Recupera la configurazione di una macchina virtuale denominata VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="6df61-119">This command retrieves the configuration of a virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="6df61-120">Il cmdlet corrente aggiunge un endpoint denominato Httpin.</span><span class="sxs-lookup"><span data-stu-id="6df61-120">The current cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="6df61-121">L'endpoint ha una porta pubblica 80 e la porta locale 8080.</span><span class="sxs-lookup"><span data-stu-id="6df61-121">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="6df61-122">L'endpoint appartiene al gruppo di bilanciamento del carico condiviso denominato webfarm.</span><span class="sxs-lookup"><span data-stu-id="6df61-122">The endpoint belongs to the shared load balanced group named WebFarm.</span></span>
<span data-ttu-id="6df61-123">Una sonda HTTP sulla porta 80 con un percorso di "/" monitora la disponibilità dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="6df61-123">An HTTP probe on port 80 with a path of '/' monitors the availability of the endpoint.</span></span>
<span data-ttu-id="6df61-124">Il comando implementa le modifiche.</span><span class="sxs-lookup"><span data-stu-id="6df61-124">The command implements your changes.</span></span>

### <span data-ttu-id="6df61-125">Esempio 3: associare un IP virtuale a un endpoint</span><span class="sxs-lookup"><span data-stu-id="6df61-125">Example 3: Associate a virtual IP to an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine25" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -LocalPort 8080 -PublicPort 80 -VirtualIPName "ContosoVip11" | Update-AzureVM
```

<span data-ttu-id="6df61-126">Questo comando Recupera la configurazione di una macchina virtuale denominata VirtualMachine25.</span><span class="sxs-lookup"><span data-stu-id="6df61-126">This command retrieves the configuration of a virtual machine named VirtualMachine25.</span></span>
<span data-ttu-id="6df61-127">Il cmdlet corrente aggiunge un endpoint denominato Httpin.</span><span class="sxs-lookup"><span data-stu-id="6df61-127">The current cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="6df61-128">L'endpoint ha una porta pubblica 80 e la porta locale 8080.</span><span class="sxs-lookup"><span data-stu-id="6df61-128">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="6df61-129">Questo comando associa un IP virtuale all'endpoint.</span><span class="sxs-lookup"><span data-stu-id="6df61-129">This command associates a virtual IP to the endpoint.</span></span>
<span data-ttu-id="6df61-130">Il comando implementa le modifiche.</span><span class="sxs-lookup"><span data-stu-id="6df61-130">The command implements your changes.</span></span>

## <span data-ttu-id="6df61-131">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6df61-131">PARAMETERS</span></span>

### <span data-ttu-id="6df61-132">-ACL</span><span class="sxs-lookup"><span data-stu-id="6df61-132">-ACL</span></span>
<span data-ttu-id="6df61-133">Specifica un oggetto di configurazione dell'elenco di controllo di accesso (ACL) per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="6df61-133">Specifies an access control list (ACL) configuration object for the endpoint.</span></span>

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

### <span data-ttu-id="6df61-134">-DefaultProbe</span><span class="sxs-lookup"><span data-stu-id="6df61-134">-DefaultProbe</span></span>
<span data-ttu-id="6df61-135">Indica che questo cmdlet usa l'impostazione di probe predefinita.</span><span class="sxs-lookup"><span data-stu-id="6df61-135">Indicates that this cmdlet uses the default probe setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LBDefaultProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df61-136">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="6df61-136">-DirectServerReturn</span></span>
<span data-ttu-id="6df61-137">Specifica se questo cmdlet Abilita il ritorno diretto del server.</span><span class="sxs-lookup"><span data-stu-id="6df61-137">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="6df61-138">Specificare $True da abilitare o $False da disabilitare.</span><span class="sxs-lookup"><span data-stu-id="6df61-138">Specify $True to enable, or $False to disable.</span></span>

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

### <span data-ttu-id="6df61-139">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="6df61-139">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="6df61-140">Specifica il periodo di timeout inattività TCP, in minuti, per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="6df61-140">Specifies the TCP idle time-out period, in minutes, for the endpoint.</span></span>

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

### <span data-ttu-id="6df61-141">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6df61-141">-InformationAction</span></span>
<span data-ttu-id="6df61-142">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="6df61-142">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6df61-143">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6df61-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6df61-144">Continuare</span><span class="sxs-lookup"><span data-stu-id="6df61-144">Continue</span></span>
- <span data-ttu-id="6df61-145">Ignora</span><span class="sxs-lookup"><span data-stu-id="6df61-145">Ignore</span></span>
- <span data-ttu-id="6df61-146">Informarsi</span><span class="sxs-lookup"><span data-stu-id="6df61-146">Inquire</span></span>
- <span data-ttu-id="6df61-147">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6df61-147">SilentlyContinue</span></span>
- <span data-ttu-id="6df61-148">Stop</span><span class="sxs-lookup"><span data-stu-id="6df61-148">Stop</span></span>
- <span data-ttu-id="6df61-149">Sospensione</span><span class="sxs-lookup"><span data-stu-id="6df61-149">Suspend</span></span>

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

### <span data-ttu-id="6df61-150">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6df61-150">-InformationVariable</span></span>
<span data-ttu-id="6df61-151">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="6df61-151">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6df61-152">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="6df61-152">-InternalLoadBalancerName</span></span>
<span data-ttu-id="6df61-153">Specifica il nome del bilanciamento del carico interno.</span><span class="sxs-lookup"><span data-stu-id="6df61-153">Specifies the name of the internal load balancer.</span></span>

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

### <span data-ttu-id="6df61-154">-LBSetName</span><span class="sxs-lookup"><span data-stu-id="6df61-154">-LBSetName</span></span>
<span data-ttu-id="6df61-155">Specifica il nome del set di bilanciamento del carico per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="6df61-155">Specifies the name of the load balancer set for the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: LBNoProbe, LBDefaultProbe, LBCustomProbe
Aliases: LoadBalancedEndpointSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df61-156">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="6df61-156">-LoadBalancerDistribution</span></span>
<span data-ttu-id="6df61-157">Specifica l'algoritmo di distribuzione del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="6df61-157">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="6df61-158">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="6df61-158">Valid values are:</span></span> 

- <span data-ttu-id="6df61-159">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="6df61-159">sourceIP.</span></span>
<span data-ttu-id="6df61-160">Due affinità della tupla: IP di origine, IP di destinazione</span><span class="sxs-lookup"><span data-stu-id="6df61-160">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="6df61-161">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="6df61-161">sourceIPProtocol.</span></span>
<span data-ttu-id="6df61-162">Tre affinità della tupla: IP di origine, IP di destinazione, protocollo</span><span class="sxs-lookup"><span data-stu-id="6df61-162">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="6df61-163">nessuno.</span><span class="sxs-lookup"><span data-stu-id="6df61-163">none.</span></span>
<span data-ttu-id="6df61-164">Cinque affinità di tupla: IP di origine, porta di origine, IP di destinazione, porta di destinazione, protocollo</span><span class="sxs-lookup"><span data-stu-id="6df61-164">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="6df61-165">Il valore predefinito è None.</span><span class="sxs-lookup"><span data-stu-id="6df61-165">The default value is none.</span></span>

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

### <span data-ttu-id="6df61-166">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="6df61-166">-LocalPort</span></span>
<span data-ttu-id="6df61-167">Specifica la porta locale, privata, utilizzata dall'endpoint.</span><span class="sxs-lookup"><span data-stu-id="6df61-167">Specifies the local, private, port that this endpoint uses.</span></span>
<span data-ttu-id="6df61-168">Le applicazioni all'interno della macchina virtuale ascoltano la porta per le richieste di input del servizio per questo endpoint.</span><span class="sxs-lookup"><span data-stu-id="6df61-168">Applications within the virtual machine listen on this port for service input requests for this endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df61-169">-Nome</span><span class="sxs-lookup"><span data-stu-id="6df61-169">-Name</span></span>
<span data-ttu-id="6df61-170">Specifica un nome per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="6df61-170">Specifies a name for the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df61-171">-Noprobe</span><span class="sxs-lookup"><span data-stu-id="6df61-171">-NoProbe</span></span>
<span data-ttu-id="6df61-172">Indica che questo cmdlet usa l'impostazione No Probe.</span><span class="sxs-lookup"><span data-stu-id="6df61-172">Indicates that this cmdlet uses the no probe setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LBNoProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df61-173">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="6df61-173">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="6df61-174">Specifica l'intervallo di polling Probe, in secondi, per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="6df61-174">Specifies the probe polling interval, in seconds, for the endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df61-175">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="6df61-175">-ProbePath</span></span>
<span data-ttu-id="6df61-176">Specifica il percorso relativo del probe HTTP.</span><span class="sxs-lookup"><span data-stu-id="6df61-176">Specifies the relative path to the HTTP probe.</span></span>

```yaml
Type: String
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df61-177">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="6df61-177">-ProbePort</span></span>
<span data-ttu-id="6df61-178">Specifica la porta utilizzata dall'endpoint.</span><span class="sxs-lookup"><span data-stu-id="6df61-178">Specifies the port that the endpoint uses.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df61-179">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="6df61-179">-ProbeProtocol</span></span>
<span data-ttu-id="6df61-180">Specifica il protocollo della porta.</span><span class="sxs-lookup"><span data-stu-id="6df61-180">Specifies the port protocol.</span></span>
<span data-ttu-id="6df61-181">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="6df61-181">Valid values are:</span></span> 

- <span data-ttu-id="6df61-182">TCP</span><span class="sxs-lookup"><span data-stu-id="6df61-182">tcp</span></span> 
- <span data-ttu-id="6df61-183">http</span><span class="sxs-lookup"><span data-stu-id="6df61-183">http</span></span>

```yaml
Type: String
Parameter Sets: LBCustomProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df61-184">-ProbeTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="6df61-184">-ProbeTimeoutInSeconds</span></span>
<span data-ttu-id="6df61-185">Specifica il periodo di timeout del polling probe in secondi.</span><span class="sxs-lookup"><span data-stu-id="6df61-185">Specifies the probe polling time-out period in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df61-186">-Profile</span><span class="sxs-lookup"><span data-stu-id="6df61-186">-Profile</span></span>
<span data-ttu-id="6df61-187">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6df61-187">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6df61-188">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="6df61-188">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6df61-189">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="6df61-189">-Protocol</span></span>
<span data-ttu-id="6df61-190">Specifica il protocollo dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="6df61-190">Specifies the protocol of the endpoint.</span></span>
<span data-ttu-id="6df61-191">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="6df61-191">Valid values are:</span></span> 

- <span data-ttu-id="6df61-192">TCP</span><span class="sxs-lookup"><span data-stu-id="6df61-192">tcp</span></span> 
- <span data-ttu-id="6df61-193">UDP</span><span class="sxs-lookup"><span data-stu-id="6df61-193">udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df61-194">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="6df61-194">-PublicPort</span></span>
<span data-ttu-id="6df61-195">Specifica la porta pubblica utilizzata dall'endpoint.</span><span class="sxs-lookup"><span data-stu-id="6df61-195">Specifies the public port that the endpoint uses.</span></span>
<span data-ttu-id="6df61-196">Se non specifichi un valore, Azure assegna una porta disponibile.</span><span class="sxs-lookup"><span data-stu-id="6df61-196">If you do not specify a value, Azure assigns an available port.</span></span>

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

### <span data-ttu-id="6df61-197">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="6df61-197">-VirtualIPName</span></span>
<span data-ttu-id="6df61-198">Specifica il nome di un indirizzo IP virtuale che Azure associa all'endpoint.</span><span class="sxs-lookup"><span data-stu-id="6df61-198">Specifies the name of a virtual IP address that Azure associates to the endpoint.</span></span>
<span data-ttu-id="6df61-199">Il servizio può avere più IP virtuali.</span><span class="sxs-lookup"><span data-stu-id="6df61-199">Your service can have multiple virtual IPs.</span></span>
<span data-ttu-id="6df61-200">Per creare indirizzi IP virtuali, usare il cmdlet **Add-AzureVirtualIP** .</span><span class="sxs-lookup"><span data-stu-id="6df61-200">To create virtual IPs, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="6df61-201">-VM</span><span class="sxs-lookup"><span data-stu-id="6df61-201">-VM</span></span>
<span data-ttu-id="6df61-202">Specifica la macchina virtuale a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="6df61-202">Specifies the virtual machine to which the endpoint belongs.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6df61-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6df61-203">CommonParameters</span></span>
<span data-ttu-id="6df61-204">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6df61-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6df61-205">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6df61-205">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6df61-206">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6df61-206">INPUTS</span></span>

## <span data-ttu-id="6df61-207">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6df61-207">OUTPUTS</span></span>

### <span data-ttu-id="6df61-208">System. Object</span><span class="sxs-lookup"><span data-stu-id="6df61-208">System.Object</span></span>

## <span data-ttu-id="6df61-209">Note</span><span class="sxs-lookup"><span data-stu-id="6df61-209">NOTES</span></span>

## <span data-ttu-id="6df61-210">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6df61-210">RELATED LINKS</span></span>

[<span data-ttu-id="6df61-211">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="6df61-211">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="6df61-212">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="6df61-212">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="6df61-213">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="6df61-213">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="6df61-214">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="6df61-214">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="6df61-215">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="6df61-215">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="6df61-216">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="6df61-216">Update-AzureVM</span></span>](./Update-AzureVM.md)


