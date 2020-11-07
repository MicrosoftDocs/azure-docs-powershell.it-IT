---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 8b88ee761ab9ee136777fb29e7726a2f72110553
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688210"
---
# <span data-ttu-id="51a5d-101">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="51a5d-101">New-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="51a5d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="51a5d-102">SYNOPSIS</span></span>
<span data-ttu-id="51a5d-103">Crea un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="51a5d-103">Creates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51a5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51a5d-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51a5d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51a5d-105">DESCRIPTION</span></span>
<span data-ttu-id="51a5d-106">Il cmdlet **New-AzureRmTrafficManagerProfile** crea un profilo di gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="51a5d-106">The **New-AzureRmTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="51a5d-107">Specificare il parametro *Name* e le impostazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="51a5d-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="51a5d-108">Questo cmdlet restituisce un oggetto local che rappresenta il nuovo profilo.</span><span class="sxs-lookup"><span data-stu-id="51a5d-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="51a5d-109">Questo cmdlet non configura gli endpoint di gestione del traffico.</span><span class="sxs-lookup"><span data-stu-id="51a5d-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="51a5d-110">Puoi aggiornare l'oggetto profilo locale usando il cmdlet Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="51a5d-110">You can update the local profile object by using the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="51a5d-111">Quindi carica le modifiche a Traffic Manager usando il cmdlet Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="51a5d-111">Then upload changes to Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="51a5d-112">In alternativa, è possibile aggiungere endpoint usando il cmdlet New-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="51a5d-112">Alternatively, you can add endpoints by using the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="51a5d-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51a5d-113">EXAMPLES</span></span>

### <span data-ttu-id="51a5d-114">Esempio 1: creare un profilo</span><span class="sxs-lookup"><span data-stu-id="51a5d-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="51a5d-115">Questo comando crea un profilo di gestione traffico di Azure denominato ContosoProfile nel gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="51a5d-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="51a5d-116">Il nome di dominio completo DNS è contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="51a5d-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="51a5d-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="51a5d-117">PARAMETERS</span></span>

### <span data-ttu-id="51a5d-118">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="51a5d-118">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="51a5d-119">Intervallo (in secondi) in cui Traffic Manager verificherà l'integrità di ogni endpoint in questo profilo.</span><span class="sxs-lookup"><span data-stu-id="51a5d-119">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="51a5d-120">Il valore predefinito è 30.</span><span class="sxs-lookup"><span data-stu-id="51a5d-120">The default is 30.</span></span>

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

### <span data-ttu-id="51a5d-121">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="51a5d-121">-MonitorPath</span></span>
<span data-ttu-id="51a5d-122">Specifica il percorso usato per monitorare l'integrità dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="51a5d-122">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="51a5d-123">Specificare un valore relativo al nome di dominio dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="51a5d-123">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="51a5d-124">Questo valore deve iniziare con una barra (/).</span><span class="sxs-lookup"><span data-stu-id="51a5d-124">This value must begin with a slash (/).</span></span>

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

### <span data-ttu-id="51a5d-125">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="51a5d-125">-MonitorPort</span></span>
<span data-ttu-id="51a5d-126">Specifica la porta TCP usata per monitorare l'integrità dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="51a5d-126">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="51a5d-127">I valori validi sono numeri interi compresi tra 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="51a5d-127">Valid values are integers from 1 through 65535.</span></span>

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

### <span data-ttu-id="51a5d-128">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="51a5d-128">-MonitorProtocol</span></span>
<span data-ttu-id="51a5d-129">Specifica il protocollo da usare per monitorare l'integrità degli endpoint.</span><span class="sxs-lookup"><span data-stu-id="51a5d-129">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="51a5d-130">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="51a5d-130">Valid values are:</span></span>

- <span data-ttu-id="51a5d-131">HTTP</span><span class="sxs-lookup"><span data-stu-id="51a5d-131">HTTP</span></span>
- <span data-ttu-id="51a5d-132">HTTPS</span><span class="sxs-lookup"><span data-stu-id="51a5d-132">HTTPS</span></span>

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

### <span data-ttu-id="51a5d-133">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="51a5d-133">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="51a5d-134">L'ora (in secondi) che Traffic Manager consente agli endpoint in questo profilo di rispondere al controllo dell'integrità.</span><span class="sxs-lookup"><span data-stu-id="51a5d-134">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="51a5d-135">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="51a5d-135">The default is 10.</span></span>

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

### <span data-ttu-id="51a5d-136">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="51a5d-136">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="51a5d-137">Numero di controlli di integrità consecutivi non riusciti che il gestore del traffico tollera prima di dichiarare un endpoint in questo profilo degradato dopo il successivo controllo dell'integrità consecutivo non riuscito.</span><span class="sxs-lookup"><span data-stu-id="51a5d-137">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="51a5d-138">Il valore predefinito è 3.</span><span class="sxs-lookup"><span data-stu-id="51a5d-138">The default is 3.</span></span>

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

### <span data-ttu-id="51a5d-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="51a5d-139">-Name</span></span>
<span data-ttu-id="51a5d-140">Specifica un nome per il profilo di Traffic Manager creato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51a5d-140">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="51a5d-141">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="51a5d-141">-ProfileStatus</span></span>
<span data-ttu-id="51a5d-142">Specifica lo stato del profilo.</span><span class="sxs-lookup"><span data-stu-id="51a5d-142">Specifies the status of the profile.</span></span>
<span data-ttu-id="51a5d-143">I valori validi sono: Enabled e disabled.</span><span class="sxs-lookup"><span data-stu-id="51a5d-143">Valid values are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="51a5d-144">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="51a5d-144">-RelativeDnsName</span></span>
<span data-ttu-id="51a5d-145">Specifica il nome DNS relativo fornito dal profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="51a5d-145">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="51a5d-146">Traffic Manager combina questo valore e il nome di dominio DNS usato da Azure Traffic Manager per creare il nome di dominio completo (FQDN) del profilo.</span><span class="sxs-lookup"><span data-stu-id="51a5d-146">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="51a5d-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51a5d-147">-ResourceGroupName</span></span>
<span data-ttu-id="51a5d-148">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="51a5d-148">Specifies the name of a resource group.</span></span>
<span data-ttu-id="51a5d-149">Questo cmdlet crea un profilo di gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="51a5d-149">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="51a5d-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="51a5d-150">-Tag</span></span>
<span data-ttu-id="51a5d-151">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="51a5d-151">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="51a5d-152">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="51a5d-152">For example:</span></span>

<span data-ttu-id="51a5d-153">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="51a5d-153">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="51a5d-154">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="51a5d-154">-TrafficRoutingMethod</span></span>
<span data-ttu-id="51a5d-155">Specifica il metodo di routing del traffico.</span><span class="sxs-lookup"><span data-stu-id="51a5d-155">Specifies the traffic routing method.</span></span>
<span data-ttu-id="51a5d-156">Questo metodo determina quale gestore del traffico di endpoint restituisce in risposta alle query DNS in arrivo.</span><span class="sxs-lookup"><span data-stu-id="51a5d-156">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="51a5d-157">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="51a5d-157">Valid values are:</span></span>

- <span data-ttu-id="51a5d-158">Prestazioni</span><span class="sxs-lookup"><span data-stu-id="51a5d-158">Performance</span></span>
- <span data-ttu-id="51a5d-159">Ponderata</span><span class="sxs-lookup"><span data-stu-id="51a5d-159">Weighted</span></span>
- <span data-ttu-id="51a5d-160">Priorità</span><span class="sxs-lookup"><span data-stu-id="51a5d-160">Priority</span></span>

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

### <span data-ttu-id="51a5d-161">-TTL</span><span class="sxs-lookup"><span data-stu-id="51a5d-161">-Ttl</span></span>
<span data-ttu-id="51a5d-162">Specifica il valore time to Live (TTL) DNS.</span><span class="sxs-lookup"><span data-stu-id="51a5d-162">Specifies the DNS Time to Live (TTL) value.</span></span>

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

### <span data-ttu-id="51a5d-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51a5d-163">-DefaultProfile</span></span>
<span data-ttu-id="51a5d-164">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="51a5d-164">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51a5d-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51a5d-165">CommonParameters</span></span>
<span data-ttu-id="51a5d-166">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51a5d-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51a5d-167">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51a5d-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51a5d-168">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="51a5d-168">INPUTS</span></span>

## <span data-ttu-id="51a5d-169">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51a5d-169">OUTPUTS</span></span>

### <span data-ttu-id="51a5d-170">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="51a5d-170">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="51a5d-171">Questo cmdlet restituisce un nuovo oggetto TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="51a5d-171">This cmdlet returns a new TrafficManagerProfile object.</span></span>

## <span data-ttu-id="51a5d-172">Note</span><span class="sxs-lookup"><span data-stu-id="51a5d-172">NOTES</span></span>

## <span data-ttu-id="51a5d-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51a5d-173">RELATED LINKS</span></span>

[<span data-ttu-id="51a5d-174">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="51a5d-174">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="51a5d-175">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="51a5d-175">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="51a5d-176">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="51a5d-176">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="51a5d-177">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="51a5d-177">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="51a5d-178">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="51a5d-178">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="51a5d-179">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="51a5d-179">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


