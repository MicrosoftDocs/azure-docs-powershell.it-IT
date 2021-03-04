---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/new-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
ms.openlocfilehash: a17f88a23399fda7f4775ca52fbe1d4aec35594d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950814"
---
# <span data-ttu-id="63728-101">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="63728-101">New-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="63728-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63728-102">SYNOPSIS</span></span>
<span data-ttu-id="63728-103">Crea un profilo di Gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="63728-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="63728-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63728-104">SYNTAX</span></span>

```
New-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-MaxReturn <Int64>]
 [-Tag <Hashtable>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-ExpectedStatusCodeRange <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63728-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="63728-105">DESCRIPTION</span></span>
<span data-ttu-id="63728-106">Il cmdlet **New-AzTrafficManagerProfile** crea un profilo di Gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="63728-106">The **New-AzTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="63728-107">Specificare il *parametro Name* e le impostazioni obbligatorie.</span><span class="sxs-lookup"><span data-stu-id="63728-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="63728-108">Questo cmdlet restituisce un oggetto locale che rappresenta il nuovo profilo.</span><span class="sxs-lookup"><span data-stu-id="63728-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="63728-109">Questo cmdlet non configura gli endpoint di Gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="63728-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="63728-110">È possibile aggiornare l'oggetto profilo locale usando il cmdlet Add-AzTrafficManagerEndpointConfig locale.</span><span class="sxs-lookup"><span data-stu-id="63728-110">You can update the local profile object by using the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="63728-111">Caricare quindi le modifiche in Gestione traffico usando Set-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63728-111">Then upload changes to Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="63728-112">In alternativa, è possibile aggiungere endpoint usando il cmdlet New-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="63728-112">Alternatively, you can add endpoints by using the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="63728-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63728-113">EXAMPLES</span></span>

### <span data-ttu-id="63728-114">Esempio 1: Creare un profilo</span><span class="sxs-lookup"><span data-stu-id="63728-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="63728-115">Questo comando crea un profilo di Gestione traffico di Azure denominato ContosoProfile nel gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="63728-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="63728-116">L'FQDN DNS è contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="63728-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="63728-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63728-117">PARAMETERS</span></span>

### <span data-ttu-id="63728-118">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="63728-118">-CustomHeader</span></span>
<span data-ttu-id="63728-119">Elenco di coppie di nomi di intestazione e valori personalizzati per le richieste di acquisto.</span><span class="sxs-lookup"><span data-stu-id="63728-119">List of custom header name and value pairs for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63728-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63728-120">-DefaultProfile</span></span>
<span data-ttu-id="63728-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="63728-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63728-122">-ExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="63728-122">-ExpectedStatusCodeRange</span></span>
<span data-ttu-id="63728-123">Elenco degli intervalli di codici di stato HTTP previsti per le richieste di risposta.</span><span class="sxs-lookup"><span data-stu-id="63728-123">List of expected HTTP status code ranges for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63728-124">-MaxReturn</span><span class="sxs-lookup"><span data-stu-id="63728-124">-MaxReturn</span></span>
<span data-ttu-id="63728-125">Numero massimo di risposte restituite per i profili con un metodo di routing MultiValue.</span><span class="sxs-lookup"><span data-stu-id="63728-125">The maximum number of answers returned for profiles with a MultiValue routing method.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63728-126">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="63728-126">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="63728-127">Intervallo (in secondi) in cui Gestione traffico controlla l'integrità di ogni endpoint in questo profilo.</span><span class="sxs-lookup"><span data-stu-id="63728-127">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="63728-128">L'impostazione predefinita è 30.</span><span class="sxs-lookup"><span data-stu-id="63728-128">The default is 30.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: IntervalInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63728-129">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="63728-129">-MonitorPath</span></span>
<span data-ttu-id="63728-130">Specifica il percorso usato per monitorare l'integrità dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="63728-130">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="63728-131">Specificare un valore relativo al nome di dominio dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="63728-131">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="63728-132">Questo valore deve iniziare con una barra (/).</span><span class="sxs-lookup"><span data-stu-id="63728-132">This value must begin with a slash (/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PathForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63728-133">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="63728-133">-MonitorPort</span></span>
<span data-ttu-id="63728-134">Specifica la porta TCP usata per monitorare l'integrità dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="63728-134">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="63728-135">I valori validi sono numeri interi da 1 a 65535.</span><span class="sxs-lookup"><span data-stu-id="63728-135">Valid values are integers from 1 through 65535.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: PortForMonitor

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63728-136">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="63728-136">-MonitorProtocol</span></span>
<span data-ttu-id="63728-137">Specifica il protocollo da usare per monitorare l'integrità dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="63728-137">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="63728-138">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="63728-138">Valid values are:</span></span>

- <span data-ttu-id="63728-139">HTTP</span><span class="sxs-lookup"><span data-stu-id="63728-139">HTTP</span></span>
- <span data-ttu-id="63728-140">HTTPS</span><span class="sxs-lookup"><span data-stu-id="63728-140">HTTPS</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProtocolForMonitor
Accepted values: HTTP, HTTPS, TCP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63728-141">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="63728-141">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="63728-142">Il tempo (in secondi) che Gestione traffico consente agli endpoint di questo profilo di rispondere alla verifica dell'integrità.</span><span class="sxs-lookup"><span data-stu-id="63728-142">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="63728-143">L'impostazione predefinita è 10.</span><span class="sxs-lookup"><span data-stu-id="63728-143">The default is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TimeoutInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63728-144">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="63728-144">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="63728-145">Numero di controlli di integrità consecutivi non riusciti che Gestione traffico convalida prima di dichiarare un endpoint in questo profilo Degradato dopo la successiva verifica dell'integrità non riuscita successiva.</span><span class="sxs-lookup"><span data-stu-id="63728-145">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="63728-146">L'impostazione predefinita è 3.</span><span class="sxs-lookup"><span data-stu-id="63728-146">The default is 3.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ToleratedNumberOfFailuresForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63728-147">-Name</span><span class="sxs-lookup"><span data-stu-id="63728-147">-Name</span></span>
<span data-ttu-id="63728-148">Specifica un nome per il profilo di Gestione traffico creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63728-148">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="63728-149">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="63728-149">-ProfileStatus</span></span>
<span data-ttu-id="63728-150">Specifica lo stato del profilo.</span><span class="sxs-lookup"><span data-stu-id="63728-150">Specifies the status of the profile.</span></span>
<span data-ttu-id="63728-151">I valori validi sono: Abilitato e Disabilitato.</span><span class="sxs-lookup"><span data-stu-id="63728-151">Valid values are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63728-152">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="63728-152">-RelativeDnsName</span></span>
<span data-ttu-id="63728-153">Specifica il nome DNS relativo fornito da questo profilo di Gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="63728-153">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="63728-154">Gestione traffico combina questo valore e il nome di dominio DNS utilizzato da Gestione traffico di Azure per formare il nome di dominio completo (FQDN) del profilo.</span><span class="sxs-lookup"><span data-stu-id="63728-154">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="63728-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63728-155">-ResourceGroupName</span></span>
<span data-ttu-id="63728-156">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="63728-156">Specifies the name of a resource group.</span></span>
<span data-ttu-id="63728-157">Questo cmdlet crea un profilo di Gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="63728-157">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="63728-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="63728-158">-Tag</span></span>
<span data-ttu-id="63728-159">Coppie chiave-valore sotto forma di tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="63728-159">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="63728-160">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="63728-160">For example:</span></span>

<span data-ttu-id="63728-161">@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="63728-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63728-162">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="63728-162">-TrafficRoutingMethod</span></span>
<span data-ttu-id="63728-163">Specifica il metodo di routing del traffico.</span><span class="sxs-lookup"><span data-stu-id="63728-163">Specifies the traffic routing method.</span></span>
<span data-ttu-id="63728-164">Questo metodo determina quale endpoint Gestore traffico restituisce in risposta alle query DNS in ingresso.</span><span class="sxs-lookup"><span data-stu-id="63728-164">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="63728-165">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="63728-165">Valid values are:</span></span>

- <span data-ttu-id="63728-166">Prestazioni</span><span class="sxs-lookup"><span data-stu-id="63728-166">Performance</span></span>
- <span data-ttu-id="63728-167">Ponderato</span><span class="sxs-lookup"><span data-stu-id="63728-167">Weighted</span></span>
- <span data-ttu-id="63728-168">Priorità</span><span class="sxs-lookup"><span data-stu-id="63728-168">Priority</span></span>
- <span data-ttu-id="63728-169">Geografico</span><span class="sxs-lookup"><span data-stu-id="63728-169">Geographic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Performance, Weighted, Priority, Geographic, Subnet, MultiValue

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63728-170">-Ttl</span><span class="sxs-lookup"><span data-stu-id="63728-170">-Ttl</span></span>
<span data-ttu-id="63728-171">Specifica il valore Dns Time to Live (TTL).</span><span class="sxs-lookup"><span data-stu-id="63728-171">Specifies the DNS Time to Live (TTL) value.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63728-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63728-172">CommonParameters</span></span>
<span data-ttu-id="63728-173">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63728-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63728-174">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63728-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63728-175">INPUT</span><span class="sxs-lookup"><span data-stu-id="63728-175">INPUTS</span></span>

### <span data-ttu-id="63728-176">Nessuno</span><span class="sxs-lookup"><span data-stu-id="63728-176">None</span></span>

## <span data-ttu-id="63728-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63728-177">OUTPUTS</span></span>

### <span data-ttu-id="63728-178">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="63728-178">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="63728-179">NOTE</span><span class="sxs-lookup"><span data-stu-id="63728-179">NOTES</span></span>

## <span data-ttu-id="63728-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63728-180">RELATED LINKS</span></span>

[<span data-ttu-id="63728-181">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="63728-181">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="63728-182">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="63728-182">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="63728-183">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="63728-183">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="63728-184">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="63728-184">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="63728-185">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="63728-185">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="63728-186">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="63728-186">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


