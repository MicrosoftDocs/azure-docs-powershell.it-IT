---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1BA472FB-E684-486C-8066-42C9215DBDEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83d1afcae66af7e4548b1dbd4031392969f4d267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029519"
---
# <span data-ttu-id="393a8-101">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="393a8-101">Set-AzureEndpoint</span></span>

## <span data-ttu-id="393a8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="393a8-102">SYNOPSIS</span></span>
<span data-ttu-id="393a8-103">Modifica un endpoint assegnato a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="393a8-103">Modifies an endpoint assigned to a virtual machine.</span></span>

## <span data-ttu-id="393a8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="393a8-104">SYNTAX</span></span>

```
Set-AzureEndpoint [-Name] <String> [[-Protocol] <String>] [[-LocalPort] <Int32>] [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="393a8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="393a8-105">DESCRIPTION</span></span>
<span data-ttu-id="393a8-106">Il cmdlet **set-AzureEndpoint** modifica un endpoint assegnato a una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="393a8-106">The **Set-AzureEndpoint** cmdlet modifies an endpoint assigned to an Azure virtual machine.</span></span>
<span data-ttu-id="393a8-107">È possibile specificare le modifiche apportate a un endpoint che non viene caricato in modo equilibrato.</span><span class="sxs-lookup"><span data-stu-id="393a8-107">You can specify changes to an endpoint that is not load balanced.</span></span>

## <span data-ttu-id="393a8-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="393a8-108">EXAMPLES</span></span>

### <span data-ttu-id="393a8-109">Esempio 1: modificare un endpoint per l'ascolto in una porta</span><span class="sxs-lookup"><span data-stu-id="393a8-109">Example 1: Modify an endpoint to listen on a port</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Set-AzureEndpoint -Name "Web" -PublicPort 443 -LocalPort 443 -Protocol tcp | Update-AzureVM
```

<span data-ttu-id="393a8-110">Questo comando Recupera la configurazione di una macchina virtuale denominata VirtualMachine01 usando il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="393a8-110">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="393a8-111">Il comando lo passa al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="393a8-111">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="393a8-112">Questo cmdlet modifica l'endpoint denominato Web per l'ascolto sulla porta 443.</span><span class="sxs-lookup"><span data-stu-id="393a8-112">This cmdlet modifies the endpoint named Web to listen on port 443.</span></span>
<span data-ttu-id="393a8-113">Il comando passa l'oggetto macchina virtuale al cmdlet **Update-AzureVM** , che implementa le modifiche.</span><span class="sxs-lookup"><span data-stu-id="393a8-113">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="393a8-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="393a8-114">PARAMETERS</span></span>

### <span data-ttu-id="393a8-115">-ACL</span><span class="sxs-lookup"><span data-stu-id="393a8-115">-ACL</span></span>
<span data-ttu-id="393a8-116">Specifica un oggetto di configurazione dell'elenco di controllo di accesso (ACL) che questo cmdlet si applica all'endpoint.</span><span class="sxs-lookup"><span data-stu-id="393a8-116">Specifies an access control list (ACL) configuration object that this cmdlet applies to the endpoint.</span></span>

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

### <span data-ttu-id="393a8-117">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="393a8-117">-DirectServerReturn</span></span>
<span data-ttu-id="393a8-118">Specifica se questo cmdlet Abilita il ritorno diretto del server.</span><span class="sxs-lookup"><span data-stu-id="393a8-118">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="393a8-119">Specificare $True da abilitare o $False da disabilitare.</span><span class="sxs-lookup"><span data-stu-id="393a8-119">Specify $True to enable, or $False to disable.</span></span>

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

### <span data-ttu-id="393a8-120">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="393a8-120">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="393a8-121">Specifica il periodo di timeout inattività TCP, in minuti, per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="393a8-121">Specifies the TCP idle time-out period, in minutes, for the endpoint.</span></span>

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

### <span data-ttu-id="393a8-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="393a8-122">-InformationAction</span></span>
<span data-ttu-id="393a8-123">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="393a8-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="393a8-124">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="393a8-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="393a8-125">Continuare</span><span class="sxs-lookup"><span data-stu-id="393a8-125">Continue</span></span>
- <span data-ttu-id="393a8-126">Ignora</span><span class="sxs-lookup"><span data-stu-id="393a8-126">Ignore</span></span>
- <span data-ttu-id="393a8-127">Informarsi</span><span class="sxs-lookup"><span data-stu-id="393a8-127">Inquire</span></span>
- <span data-ttu-id="393a8-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="393a8-128">SilentlyContinue</span></span>
- <span data-ttu-id="393a8-129">Stop</span><span class="sxs-lookup"><span data-stu-id="393a8-129">Stop</span></span>
- <span data-ttu-id="393a8-130">Sospensione</span><span class="sxs-lookup"><span data-stu-id="393a8-130">Suspend</span></span>

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

### <span data-ttu-id="393a8-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="393a8-131">-InformationVariable</span></span>
<span data-ttu-id="393a8-132">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="393a8-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="393a8-133">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="393a8-133">-InternalLoadBalancerName</span></span>
<span data-ttu-id="393a8-134">Specifica il nome del bilanciamento del carico interno.</span><span class="sxs-lookup"><span data-stu-id="393a8-134">Specifies the name of the internal load balancer.</span></span>

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

### <span data-ttu-id="393a8-135">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="393a8-135">-LoadBalancerDistribution</span></span>
<span data-ttu-id="393a8-136">Specifica l'algoritmo di distribuzione del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="393a8-136">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="393a8-137">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="393a8-137">Valid values are:</span></span> 

- <span data-ttu-id="393a8-138">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="393a8-138">sourceIP.</span></span>
<span data-ttu-id="393a8-139">Due affinità della tupla: IP di origine, IP di destinazione</span><span class="sxs-lookup"><span data-stu-id="393a8-139">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="393a8-140">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="393a8-140">sourceIPProtocol.</span></span>
<span data-ttu-id="393a8-141">Tre affinità della tupla: IP di origine, IP di destinazione, protocollo</span><span class="sxs-lookup"><span data-stu-id="393a8-141">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="393a8-142">nessuno.</span><span class="sxs-lookup"><span data-stu-id="393a8-142">none.</span></span>
<span data-ttu-id="393a8-143">Cinque affinità di tupla: IP di origine, porta di origine, IP di destinazione, porta di destinazione, protocollo</span><span class="sxs-lookup"><span data-stu-id="393a8-143">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="393a8-144">Il valore predefinito è None.</span><span class="sxs-lookup"><span data-stu-id="393a8-144">The default value is none.</span></span>

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

### <span data-ttu-id="393a8-145">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="393a8-145">-LocalPort</span></span>
<span data-ttu-id="393a8-146">Specifica la porta locale, privata, utilizzata dall'endpoint.</span><span class="sxs-lookup"><span data-stu-id="393a8-146">Specifies the local, private, port that this endpoint uses.</span></span>
<span data-ttu-id="393a8-147">Le applicazioni all'interno della macchina virtuale ascoltano la porta per le richieste di input del servizio per questo endpoint.</span><span class="sxs-lookup"><span data-stu-id="393a8-147">Applications within the virtual machine listen on this port for service input requests for this endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="393a8-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="393a8-148">-Name</span></span>
<span data-ttu-id="393a8-149">Specifica il nome dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="393a8-149">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="393a8-150">-Profile</span><span class="sxs-lookup"><span data-stu-id="393a8-150">-Profile</span></span>
<span data-ttu-id="393a8-151">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="393a8-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="393a8-152">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="393a8-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="393a8-153">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="393a8-153">-Protocol</span></span>
<span data-ttu-id="393a8-154">Specifica il protocollo dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="393a8-154">Specifies the protocol of the endpoint.</span></span>
<span data-ttu-id="393a8-155">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="393a8-155">Valid values are:</span></span> 

- <span data-ttu-id="393a8-156">TCP</span><span class="sxs-lookup"><span data-stu-id="393a8-156">tcp</span></span> 
- <span data-ttu-id="393a8-157">UDP</span><span class="sxs-lookup"><span data-stu-id="393a8-157">udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="393a8-158">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="393a8-158">-PublicPort</span></span>
<span data-ttu-id="393a8-159">Specifica la porta pubblica utilizzata dall'endpoint.</span><span class="sxs-lookup"><span data-stu-id="393a8-159">Specifies the public port that the endpoint uses.</span></span>

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

### <span data-ttu-id="393a8-160">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="393a8-160">-VirtualIPName</span></span>
<span data-ttu-id="393a8-161">Specifica il nome di un indirizzo IP virtuale che Azure associa all'endpoint.</span><span class="sxs-lookup"><span data-stu-id="393a8-161">Specifies the name of a virtual IP address that Azure associates to the endpoint.</span></span>
<span data-ttu-id="393a8-162">Il servizio può avere più IP virtuali.</span><span class="sxs-lookup"><span data-stu-id="393a8-162">Your service can have multiple virtual IPs.</span></span>
<span data-ttu-id="393a8-163">Per creare indirizzi IP virtuali, usare il cmdlet **Add-AzureVirtualIP** .</span><span class="sxs-lookup"><span data-stu-id="393a8-163">To create virtual IPs, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="393a8-164">-VM</span><span class="sxs-lookup"><span data-stu-id="393a8-164">-VM</span></span>
<span data-ttu-id="393a8-165">Specifica la macchina virtuale a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="393a8-165">Specifies the virtual machine to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="393a8-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="393a8-166">CommonParameters</span></span>
<span data-ttu-id="393a8-167">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="393a8-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="393a8-168">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="393a8-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="393a8-169">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="393a8-169">INPUTS</span></span>

## <span data-ttu-id="393a8-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="393a8-170">OUTPUTS</span></span>

### <span data-ttu-id="393a8-171">System. Object</span><span class="sxs-lookup"><span data-stu-id="393a8-171">System.Object</span></span>

## <span data-ttu-id="393a8-172">Note</span><span class="sxs-lookup"><span data-stu-id="393a8-172">NOTES</span></span>

## <span data-ttu-id="393a8-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="393a8-173">RELATED LINKS</span></span>

[<span data-ttu-id="393a8-174">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="393a8-174">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="393a8-175">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="393a8-175">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="393a8-176">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="393a8-176">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="393a8-177">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="393a8-177">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="393a8-178">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="393a8-178">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="393a8-179">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="393a8-179">Update-AzureVM</span></span>](./Update-AzureVM.md)


