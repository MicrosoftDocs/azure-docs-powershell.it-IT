---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 896324e8d08cae69f24c195de9b44b325985c2c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514043"
---
# <span data-ttu-id="6a922-101">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6a922-101">New-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="6a922-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a922-102">SYNOPSIS</span></span>
<span data-ttu-id="6a922-103">Crea un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="6a922-103">Creates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a922-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a922-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a922-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a922-105">DESCRIPTION</span></span>
<span data-ttu-id="6a922-106">Il cmdlet **New-AzureRmTrafficManagerProfile** crea un profilo di gestione traffico di Azure.</span><span class="sxs-lookup"><span data-stu-id="6a922-106">The **New-AzureRmTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="6a922-107">Specificare il parametro *Name* e le impostazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="6a922-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="6a922-108">Questo cmdlet restituisce un oggetto local che rappresenta il nuovo profilo.</span><span class="sxs-lookup"><span data-stu-id="6a922-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="6a922-109">Questo cmdlet non configura gli endpoint di gestione del traffico.</span><span class="sxs-lookup"><span data-stu-id="6a922-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="6a922-110">Puoi aggiornare l'oggetto profilo locale usando il cmdlet Add-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="6a922-110">You can update the local profile object by using the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="6a922-111">Quindi carica le modifiche a Traffic Manager usando il cmdlet Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="6a922-111">Then upload changes to Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="6a922-112">In alternativa, è possibile aggiungere endpoint usando il cmdlet New-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6a922-112">Alternatively, you can add endpoints by using the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="6a922-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a922-113">EXAMPLES</span></span>

### <span data-ttu-id="6a922-114">Esempio 1: creare un profilo</span><span class="sxs-lookup"><span data-stu-id="6a922-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="6a922-115">Questo comando crea un profilo di gestione traffico di Azure denominato ContosoProfile nel gruppo di risorse ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="6a922-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="6a922-116">Il nome di dominio completo DNS è contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="6a922-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="6a922-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a922-117">PARAMETERS</span></span>

### <span data-ttu-id="6a922-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a922-118">-DefaultProfile</span></span>
<span data-ttu-id="6a922-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a922-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a922-120">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="6a922-120">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="6a922-121">Intervallo (in secondi) in cui Traffic Manager verificherà l'integrità di ogni endpoint in questo profilo.</span><span class="sxs-lookup"><span data-stu-id="6a922-121">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="6a922-122">Il valore predefinito è 30.</span><span class="sxs-lookup"><span data-stu-id="6a922-122">The default is 30.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: IntervalInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a922-123">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="6a922-123">-MonitorPath</span></span>
<span data-ttu-id="6a922-124">Specifica il percorso usato per monitorare l'integrità dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="6a922-124">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="6a922-125">Specificare un valore relativo al nome di dominio dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="6a922-125">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="6a922-126">Questo valore deve iniziare con una barra (/).</span><span class="sxs-lookup"><span data-stu-id="6a922-126">This value must begin with a slash (/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PathForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a922-127">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="6a922-127">-MonitorPort</span></span>
<span data-ttu-id="6a922-128">Specifica la porta TCP usata per monitorare l'integrità dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="6a922-128">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="6a922-129">I valori validi sono numeri interi compresi tra 1 e 65535.</span><span class="sxs-lookup"><span data-stu-id="6a922-129">Valid values are integers from 1 through 65535.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: PortForMonitor

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a922-130">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="6a922-130">-MonitorProtocol</span></span>
<span data-ttu-id="6a922-131">Specifica il protocollo da usare per monitorare l'integrità degli endpoint.</span><span class="sxs-lookup"><span data-stu-id="6a922-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="6a922-132">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="6a922-132">Valid values are:</span></span>

- <span data-ttu-id="6a922-133">HTTP</span><span class="sxs-lookup"><span data-stu-id="6a922-133">HTTP</span></span>
- <span data-ttu-id="6a922-134">HTTPS</span><span class="sxs-lookup"><span data-stu-id="6a922-134">HTTPS</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ProtocolForMonitor
Accepted values: HTTP, HTTPS, TCP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a922-135">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="6a922-135">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="6a922-136">L'ora (in secondi) che Traffic Manager consente agli endpoint in questo profilo di rispondere al controllo dell'integrità.</span><span class="sxs-lookup"><span data-stu-id="6a922-136">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="6a922-137">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="6a922-137">The default is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: TimeoutInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a922-138">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="6a922-138">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="6a922-139">Numero di controlli di integrità consecutivi non riusciti che il gestore del traffico tollera prima di dichiarare un endpoint in questo profilo degradato dopo il successivo controllo dell'integrità consecutivo non riuscito.</span><span class="sxs-lookup"><span data-stu-id="6a922-139">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="6a922-140">Il valore predefinito è 3.</span><span class="sxs-lookup"><span data-stu-id="6a922-140">The default is 3.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ToleratedNumberOfFailuresForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a922-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a922-141">-Name</span></span>
<span data-ttu-id="6a922-142">Specifica un nome per il profilo di Traffic Manager creato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a922-142">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6a922-143">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="6a922-143">-ProfileStatus</span></span>
<span data-ttu-id="6a922-144">Specifica lo stato del profilo.</span><span class="sxs-lookup"><span data-stu-id="6a922-144">Specifies the status of the profile.</span></span>
<span data-ttu-id="6a922-145">I valori validi sono: Enabled e disabled.</span><span class="sxs-lookup"><span data-stu-id="6a922-145">Valid values are: Enabled and Disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a922-146">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="6a922-146">-RelativeDnsName</span></span>
<span data-ttu-id="6a922-147">Specifica il nome DNS relativo fornito dal profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="6a922-147">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="6a922-148">Traffic Manager combina questo valore e il nome di dominio DNS usato da Azure Traffic Manager per creare il nome di dominio completo (FQDN) del profilo.</span><span class="sxs-lookup"><span data-stu-id="6a922-148">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="6a922-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a922-149">-ResourceGroupName</span></span>
<span data-ttu-id="6a922-150">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6a922-150">Specifies the name of a resource group.</span></span>
<span data-ttu-id="6a922-151">Questo cmdlet crea un profilo di gestione traffico nel gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6a922-151">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6a922-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="6a922-152">-Tag</span></span>
<span data-ttu-id="6a922-153">Coppie chiave-valore nella forma di una tabella hash impostata come tag nel server.</span><span class="sxs-lookup"><span data-stu-id="6a922-153">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="6a922-154">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="6a922-154">For example:</span></span>

<span data-ttu-id="6a922-155">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="6a922-155">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a922-156">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="6a922-156">-TrafficRoutingMethod</span></span>
<span data-ttu-id="6a922-157">Specifica il metodo di routing del traffico.</span><span class="sxs-lookup"><span data-stu-id="6a922-157">Specifies the traffic routing method.</span></span>
<span data-ttu-id="6a922-158">Questo metodo determina quale gestore del traffico di endpoint restituisce in risposta alle query DNS in arrivo.</span><span class="sxs-lookup"><span data-stu-id="6a922-158">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="6a922-159">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="6a922-159">Valid values are:</span></span>

- <span data-ttu-id="6a922-160">Prestazioni</span><span class="sxs-lookup"><span data-stu-id="6a922-160">Performance</span></span>
- <span data-ttu-id="6a922-161">Ponderata</span><span class="sxs-lookup"><span data-stu-id="6a922-161">Weighted</span></span>
- <span data-ttu-id="6a922-162">Priorità</span><span class="sxs-lookup"><span data-stu-id="6a922-162">Priority</span></span>
- <span data-ttu-id="6a922-163">Geographic</span><span class="sxs-lookup"><span data-stu-id="6a922-163">Geographic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Performance, Weighted, Priority, Geographic

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a922-164">-TTL</span><span class="sxs-lookup"><span data-stu-id="6a922-164">-Ttl</span></span>
<span data-ttu-id="6a922-165">Specifica il valore time to Live (TTL) DNS.</span><span class="sxs-lookup"><span data-stu-id="6a922-165">Specifies the DNS Time to Live (TTL) value.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a922-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a922-166">CommonParameters</span></span>
<span data-ttu-id="6a922-167">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a922-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a922-168">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a922-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a922-169">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a922-169">INPUTS</span></span>

### <span data-ttu-id="6a922-170">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6a922-170">None</span></span>
<span data-ttu-id="6a922-171">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="6a922-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6a922-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a922-172">OUTPUTS</span></span>

### <span data-ttu-id="6a922-173">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6a922-173">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="6a922-174">Questo cmdlet restituisce un nuovo oggetto TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="6a922-174">This cmdlet returns a new TrafficManagerProfile object.</span></span>

## <span data-ttu-id="6a922-175">Note</span><span class="sxs-lookup"><span data-stu-id="6a922-175">NOTES</span></span>

## <span data-ttu-id="6a922-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a922-176">RELATED LINKS</span></span>

[<span data-ttu-id="6a922-177">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="6a922-177">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="6a922-178">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6a922-178">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="6a922-179">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6a922-179">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="6a922-180">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6a922-180">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="6a922-181">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6a922-181">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="6a922-182">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6a922-182">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


