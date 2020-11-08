---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
ms.openlocfilehash: c5e1f69e8a11f09e4f7b838c5e489c8a240d40e6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189980"
---
# <span data-ttu-id="524c7-101">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="524c7-101">New-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="524c7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="524c7-102">SYNOPSIS</span></span>
<span data-ttu-id="524c7-103">Crea un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="524c7-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="524c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="524c7-104">SYNTAX</span></span>

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

## <span data-ttu-id="524c7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="524c7-105">DESCRIPTION</span></span>
<span data-ttu-id="524c7-106">Il cmdlet **New-AzTrafficManagerProfile** crea un profilo di gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="524c7-106">The **New-AzTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="524c7-107">Specificare il parametro *Name* e le impostazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="524c7-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="524c7-108">Questo cmdlet restituisce un oggetto local che rappresenta il nuovo profilo.</span><span class="sxs-lookup"><span data-stu-id="524c7-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="524c7-109">Questo cmdlet non configura gli endpoint di gestione del traffico.</span><span class="sxs-lookup"><span data-stu-id="524c7-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="524c7-110">Puoi aggiornare l'oggetto profilo locale usando il cmdlet Add-AzTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="524c7-110">You can update the local profile object by using the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="524c7-111">Quindi carica le modifiche a Traffic Manager usando il cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="524c7-111">Then upload changes to Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="524c7-112">In alternativa, è possibile aggiungere endpoint usando il cmdlet New-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="524c7-112">Alternatively, you can add endpoints by using the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="524c7-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="524c7-113">EXAMPLES</span></span>

### <span data-ttu-id="524c7-114">Esempio 1: creare un profilo</span><span class="sxs-lookup"><span data-stu-id="524c7-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="524c7-115">Questo comando crea un profilo di gestione traffico di Azure denominato ContosoProfile nel gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="524c7-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="524c7-116">Il nome di dominio completo DNS è contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="524c7-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="524c7-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="524c7-117">PARAMETERS</span></span>

### <span data-ttu-id="524c7-118">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="524c7-118">-CustomHeader</span></span>
<span data-ttu-id="524c7-119">Elenco delle coppie nome intestazione personalizzate e valore per le richieste di probe.</span><span class="sxs-lookup"><span data-stu-id="524c7-119">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="524c7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="524c7-120">-DefaultProfile</span></span>
<span data-ttu-id="524c7-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="524c7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="524c7-122">-ExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="524c7-122">-ExpectedStatusCodeRange</span></span>
<span data-ttu-id="524c7-123">Elenco degli intervalli di codice di stato HTTP previsti per le richieste di probe.</span><span class="sxs-lookup"><span data-stu-id="524c7-123">List of expected HTTP status code ranges for probe requests.</span></span>

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

### <span data-ttu-id="524c7-124">-MaxReturn</span><span class="sxs-lookup"><span data-stu-id="524c7-124">-MaxReturn</span></span>
<span data-ttu-id="524c7-125">Numero massimo di risposte restituite per i profili con un metodo di routing multivalore.</span><span class="sxs-lookup"><span data-stu-id="524c7-125">The maximum number of answers returned for profiles with a MultiValue routing method.</span></span>

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

### <span data-ttu-id="524c7-126">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="524c7-126">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="524c7-127">Intervallo (in secondi) in cui Traffic Manager verificherà l'integrità di ogni endpoint in questo profilo.</span><span class="sxs-lookup"><span data-stu-id="524c7-127">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="524c7-128">Il valore predefinito è 30.</span><span class="sxs-lookup"><span data-stu-id="524c7-128">The default is 30.</span></span>

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

### <span data-ttu-id="524c7-129">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="524c7-129">-MonitorPath</span></span>
<span data-ttu-id="524c7-130">Specifica il percorso usato per monitorare l'integrità dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="524c7-130">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="524c7-131">Specificare un valore relativo al nome di dominio dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="524c7-131">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="524c7-132">Questo valore deve iniziare con una barra (/).</span><span class="sxs-lookup"><span data-stu-id="524c7-132">This value must begin with a slash (/).</span></span>

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

### <span data-ttu-id="524c7-133">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="524c7-133">-MonitorPort</span></span>
<span data-ttu-id="524c7-134">Specifica la porta TCP usata per monitorare l'integrità dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="524c7-134">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="524c7-135">I valori validi sono numeri interi compresi tra 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="524c7-135">Valid values are integers from 1 through 65535.</span></span>

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

### <span data-ttu-id="524c7-136">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="524c7-136">-MonitorProtocol</span></span>
<span data-ttu-id="524c7-137">Specifica il protocollo da usare per monitorare l'integrità degli endpoint.</span><span class="sxs-lookup"><span data-stu-id="524c7-137">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="524c7-138">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="524c7-138">Valid values are:</span></span>

- <span data-ttu-id="524c7-139">HTTP</span><span class="sxs-lookup"><span data-stu-id="524c7-139">HTTP</span></span>
- <span data-ttu-id="524c7-140">HTTPS</span><span class="sxs-lookup"><span data-stu-id="524c7-140">HTTPS</span></span>

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

### <span data-ttu-id="524c7-141">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="524c7-141">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="524c7-142">L'ora (in secondi) che Traffic Manager consente agli endpoint in questo profilo di rispondere al controllo dell'integrità.</span><span class="sxs-lookup"><span data-stu-id="524c7-142">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="524c7-143">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="524c7-143">The default is 10.</span></span>

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

### <span data-ttu-id="524c7-144">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="524c7-144">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="524c7-145">Numero di controlli di integrità consecutivi non riusciti che il gestore del traffico tollera prima di dichiarare un endpoint in questo profilo degradato dopo il successivo controllo dell'integrità consecutivo non riuscito.</span><span class="sxs-lookup"><span data-stu-id="524c7-145">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="524c7-146">Il valore predefinito è 3.</span><span class="sxs-lookup"><span data-stu-id="524c7-146">The default is 3.</span></span>

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

### <span data-ttu-id="524c7-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="524c7-147">-Name</span></span>
<span data-ttu-id="524c7-148">Specifica un nome per il profilo di Traffic Manager creato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="524c7-148">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="524c7-149">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="524c7-149">-ProfileStatus</span></span>
<span data-ttu-id="524c7-150">Specifica lo stato del profilo.</span><span class="sxs-lookup"><span data-stu-id="524c7-150">Specifies the status of the profile.</span></span>
<span data-ttu-id="524c7-151">I valori validi sono: Enabled e disabled.</span><span class="sxs-lookup"><span data-stu-id="524c7-151">Valid values are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="524c7-152">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="524c7-152">-RelativeDnsName</span></span>
<span data-ttu-id="524c7-153">Specifica il nome DNS relativo fornito dal profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="524c7-153">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="524c7-154">Traffic Manager combina questo valore e il nome di dominio DNS usato da Azure Traffic Manager per creare il nome di dominio completo (FQDN) del profilo.</span><span class="sxs-lookup"><span data-stu-id="524c7-154">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="524c7-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="524c7-155">-ResourceGroupName</span></span>
<span data-ttu-id="524c7-156">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="524c7-156">Specifies the name of a resource group.</span></span>
<span data-ttu-id="524c7-157">Questo cmdlet crea un profilo di gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="524c7-157">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="524c7-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="524c7-158">-Tag</span></span>
<span data-ttu-id="524c7-159">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="524c7-159">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="524c7-160">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="524c7-160">For example:</span></span>

<span data-ttu-id="524c7-161">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="524c7-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="524c7-162">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="524c7-162">-TrafficRoutingMethod</span></span>
<span data-ttu-id="524c7-163">Specifica il metodo di routing del traffico.</span><span class="sxs-lookup"><span data-stu-id="524c7-163">Specifies the traffic routing method.</span></span>
<span data-ttu-id="524c7-164">Questo metodo determina quale gestore del traffico di endpoint restituisce in risposta alle query DNS in arrivo.</span><span class="sxs-lookup"><span data-stu-id="524c7-164">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="524c7-165">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="524c7-165">Valid values are:</span></span>

- <span data-ttu-id="524c7-166">Prestazioni</span><span class="sxs-lookup"><span data-stu-id="524c7-166">Performance</span></span>
- <span data-ttu-id="524c7-167">Ponderata</span><span class="sxs-lookup"><span data-stu-id="524c7-167">Weighted</span></span>
- <span data-ttu-id="524c7-168">Priorità</span><span class="sxs-lookup"><span data-stu-id="524c7-168">Priority</span></span>
- <span data-ttu-id="524c7-169">Geographic</span><span class="sxs-lookup"><span data-stu-id="524c7-169">Geographic</span></span>

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

### <span data-ttu-id="524c7-170">-TTL</span><span class="sxs-lookup"><span data-stu-id="524c7-170">-Ttl</span></span>
<span data-ttu-id="524c7-171">Specifica il valore time to Live (TTL) DNS.</span><span class="sxs-lookup"><span data-stu-id="524c7-171">Specifies the DNS Time to Live (TTL) value.</span></span>

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

### <span data-ttu-id="524c7-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="524c7-172">CommonParameters</span></span>
<span data-ttu-id="524c7-173">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="524c7-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="524c7-174">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="524c7-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="524c7-175">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="524c7-175">INPUTS</span></span>

### <span data-ttu-id="524c7-176">Nessuno</span><span class="sxs-lookup"><span data-stu-id="524c7-176">None</span></span>

## <span data-ttu-id="524c7-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="524c7-177">OUTPUTS</span></span>

### <span data-ttu-id="524c7-178">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="524c7-178">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="524c7-179">Note</span><span class="sxs-lookup"><span data-stu-id="524c7-179">NOTES</span></span>

## <span data-ttu-id="524c7-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="524c7-180">RELATED LINKS</span></span>

[<span data-ttu-id="524c7-181">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="524c7-181">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="524c7-182">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="524c7-182">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="524c7-183">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="524c7-183">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="524c7-184">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="524c7-184">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="524c7-185">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="524c7-185">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="524c7-186">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="524c7-186">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

