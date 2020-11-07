---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: bc59e5b317588317ae9dc428db76c924847895da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687558"
---
# <span data-ttu-id="92405-101">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="92405-101">New-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="92405-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="92405-102">SYNOPSIS</span></span>
<span data-ttu-id="92405-103">Crea un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="92405-103">Creates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92405-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92405-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-MaxReturn <Int64>]
 [-Tag <Hashtable>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-ExpectedStatusCodeRange <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92405-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92405-105">DESCRIPTION</span></span>
<span data-ttu-id="92405-106">Il cmdlet **New-AzureRmTrafficManagerProfile** crea un profilo di gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="92405-106">The **New-AzureRmTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="92405-107">Specificare il parametro *Name* e le impostazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="92405-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="92405-108">Questo cmdlet restituisce un oggetto local che rappresenta il nuovo profilo.</span><span class="sxs-lookup"><span data-stu-id="92405-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="92405-109">Questo cmdlet non configura gli endpoint di gestione del traffico.</span><span class="sxs-lookup"><span data-stu-id="92405-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="92405-110">Puoi aggiornare l'oggetto profilo locale usando il cmdlet Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="92405-110">You can update the local profile object by using the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="92405-111">Quindi carica le modifiche a Traffic Manager usando il cmdlet Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="92405-111">Then upload changes to Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="92405-112">In alternativa, è possibile aggiungere endpoint usando il cmdlet New-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="92405-112">Alternatively, you can add endpoints by using the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="92405-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92405-113">EXAMPLES</span></span>

### <span data-ttu-id="92405-114">Esempio 1: creare un profilo</span><span class="sxs-lookup"><span data-stu-id="92405-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="92405-115">Questo comando crea un profilo di gestione traffico di Azure denominato ContosoProfile nel gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="92405-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="92405-116">Il nome di dominio completo DNS è contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="92405-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="92405-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="92405-117">PARAMETERS</span></span>

### <span data-ttu-id="92405-118">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="92405-118">-CustomHeader</span></span>
<span data-ttu-id="92405-119">Elenco delle coppie nome intestazione personalizzate e valore per le richieste di probe.</span><span class="sxs-lookup"><span data-stu-id="92405-119">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="92405-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92405-120">-DefaultProfile</span></span>
<span data-ttu-id="92405-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="92405-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92405-122">-ExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="92405-122">-ExpectedStatusCodeRange</span></span>
<span data-ttu-id="92405-123">Elenco degli intervalli di codice di stato HTTP previsti per le richieste di probe.</span><span class="sxs-lookup"><span data-stu-id="92405-123">List of expected HTTP status code ranges for probe requests.</span></span>

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

### <span data-ttu-id="92405-124">-MaxReturn</span><span class="sxs-lookup"><span data-stu-id="92405-124">-MaxReturn</span></span>
<span data-ttu-id="92405-125">Numero massimo di risposte restituite per i profili con un metodo di routing multivalore.</span><span class="sxs-lookup"><span data-stu-id="92405-125">The maximum number of answers returned for profiles with a MultiValue routing method.</span></span>

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

### <span data-ttu-id="92405-126">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="92405-126">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="92405-127">Intervallo (in secondi) in cui Traffic Manager verificherà l'integrità di ogni endpoint in questo profilo.</span><span class="sxs-lookup"><span data-stu-id="92405-127">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="92405-128">Il valore predefinito è 30.</span><span class="sxs-lookup"><span data-stu-id="92405-128">The default is 30.</span></span>

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

### <span data-ttu-id="92405-129">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="92405-129">-MonitorPath</span></span>
<span data-ttu-id="92405-130">Specifica il percorso usato per monitorare l'integrità dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="92405-130">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="92405-131">Specificare un valore relativo al nome di dominio dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="92405-131">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="92405-132">Questo valore deve iniziare con una barra (/).</span><span class="sxs-lookup"><span data-stu-id="92405-132">This value must begin with a slash (/).</span></span>

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

### <span data-ttu-id="92405-133">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="92405-133">-MonitorPort</span></span>
<span data-ttu-id="92405-134">Specifica la porta TCP usata per monitorare l'integrità dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="92405-134">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="92405-135">I valori validi sono numeri interi compresi tra 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="92405-135">Valid values are integers from 1 through 65535.</span></span>

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

### <span data-ttu-id="92405-136">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="92405-136">-MonitorProtocol</span></span>
<span data-ttu-id="92405-137">Specifica il protocollo da usare per monitorare l'integrità degli endpoint.</span><span class="sxs-lookup"><span data-stu-id="92405-137">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="92405-138">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="92405-138">Valid values are:</span></span>

- <span data-ttu-id="92405-139">HTTP</span><span class="sxs-lookup"><span data-stu-id="92405-139">HTTP</span></span>
- <span data-ttu-id="92405-140">HTTPS</span><span class="sxs-lookup"><span data-stu-id="92405-140">HTTPS</span></span>

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

### <span data-ttu-id="92405-141">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="92405-141">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="92405-142">L'ora (in secondi) che Traffic Manager consente agli endpoint in questo profilo di rispondere al controllo dell'integrità.</span><span class="sxs-lookup"><span data-stu-id="92405-142">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="92405-143">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="92405-143">The default is 10.</span></span>

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

### <span data-ttu-id="92405-144">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="92405-144">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="92405-145">Numero di controlli di integrità consecutivi non riusciti che il gestore del traffico tollera prima di dichiarare un endpoint in questo profilo degradato dopo il successivo controllo dell'integrità consecutivo non riuscito.</span><span class="sxs-lookup"><span data-stu-id="92405-145">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="92405-146">Il valore predefinito è 3.</span><span class="sxs-lookup"><span data-stu-id="92405-146">The default is 3.</span></span>

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

### <span data-ttu-id="92405-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="92405-147">-Name</span></span>
<span data-ttu-id="92405-148">Specifica un nome per il profilo di Traffic Manager creato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92405-148">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="92405-149">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="92405-149">-ProfileStatus</span></span>
<span data-ttu-id="92405-150">Specifica lo stato del profilo.</span><span class="sxs-lookup"><span data-stu-id="92405-150">Specifies the status of the profile.</span></span>
<span data-ttu-id="92405-151">I valori validi sono: Enabled e disabled.</span><span class="sxs-lookup"><span data-stu-id="92405-151">Valid values are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="92405-152">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="92405-152">-RelativeDnsName</span></span>
<span data-ttu-id="92405-153">Specifica il nome DNS relativo fornito dal profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="92405-153">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="92405-154">Traffic Manager combina questo valore e il nome di dominio DNS usato da Azure Traffic Manager per creare il nome di dominio completo (FQDN) del profilo.</span><span class="sxs-lookup"><span data-stu-id="92405-154">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="92405-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92405-155">-ResourceGroupName</span></span>
<span data-ttu-id="92405-156">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="92405-156">Specifies the name of a resource group.</span></span>
<span data-ttu-id="92405-157">Questo cmdlet crea un profilo di gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="92405-157">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="92405-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="92405-158">-Tag</span></span>
<span data-ttu-id="92405-159">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="92405-159">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="92405-160">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="92405-160">For example:</span></span>

<span data-ttu-id="92405-161">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="92405-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="92405-162">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="92405-162">-TrafficRoutingMethod</span></span>
<span data-ttu-id="92405-163">Specifica il metodo di routing del traffico.</span><span class="sxs-lookup"><span data-stu-id="92405-163">Specifies the traffic routing method.</span></span>
<span data-ttu-id="92405-164">Questo metodo determina quale gestore del traffico di endpoint restituisce in risposta alle query DNS in arrivo.</span><span class="sxs-lookup"><span data-stu-id="92405-164">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="92405-165">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="92405-165">Valid values are:</span></span>

- <span data-ttu-id="92405-166">Prestazioni</span><span class="sxs-lookup"><span data-stu-id="92405-166">Performance</span></span>
- <span data-ttu-id="92405-167">Ponderata</span><span class="sxs-lookup"><span data-stu-id="92405-167">Weighted</span></span>
- <span data-ttu-id="92405-168">Priorità</span><span class="sxs-lookup"><span data-stu-id="92405-168">Priority</span></span>
- <span data-ttu-id="92405-169">Geographic</span><span class="sxs-lookup"><span data-stu-id="92405-169">Geographic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Performance, Weighted, Priority, Geographic

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92405-170">-TTL</span><span class="sxs-lookup"><span data-stu-id="92405-170">-Ttl</span></span>
<span data-ttu-id="92405-171">Specifica il valore time to Live (TTL) DNS.</span><span class="sxs-lookup"><span data-stu-id="92405-171">Specifies the DNS Time to Live (TTL) value.</span></span>

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

### <span data-ttu-id="92405-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92405-172">CommonParameters</span></span>
<span data-ttu-id="92405-173">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92405-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92405-174">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92405-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92405-175">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="92405-175">INPUTS</span></span>

### <span data-ttu-id="92405-176">Nessuno</span><span class="sxs-lookup"><span data-stu-id="92405-176">None</span></span>
<span data-ttu-id="92405-177">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="92405-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="92405-178">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92405-178">OUTPUTS</span></span>

### <span data-ttu-id="92405-179">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="92405-179">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="92405-180">Questo cmdlet restituisce un nuovo oggetto TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="92405-180">This cmdlet returns a new TrafficManagerProfile object.</span></span>

## <span data-ttu-id="92405-181">Note</span><span class="sxs-lookup"><span data-stu-id="92405-181">NOTES</span></span>

## <span data-ttu-id="92405-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92405-182">RELATED LINKS</span></span>

[<span data-ttu-id="92405-183">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="92405-183">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="92405-184">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="92405-184">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="92405-185">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="92405-185">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="92405-186">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="92405-186">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="92405-187">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="92405-187">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="92405-188">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="92405-188">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


