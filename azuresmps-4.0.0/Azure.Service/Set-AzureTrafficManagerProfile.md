---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 700AC44E-4FD5-4516-80F3-B8C9E4DF6ABC
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37397b4e0ce9f1d9878860eb5e7a431e58a20a9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023752"
---
# <span data-ttu-id="bdc30-101">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bdc30-101">Set-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="bdc30-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bdc30-102">SYNOPSIS</span></span>
<span data-ttu-id="bdc30-103">Aggiorna le proprietà di un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="bdc30-103">Updates the properties of a Traffic Manager profile.</span></span>

## <span data-ttu-id="bdc30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bdc30-104">SYNTAX</span></span>

```
Set-AzureTrafficManagerProfile [-Name <String>] [-LoadBalancingMethod <String>] [-MonitorPort <Int32>]
 [-MonitorProtocol <String>] [-MonitorRelativePath <String>] [-Ttl <Int32>]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bdc30-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bdc30-105">DESCRIPTION</span></span>
<span data-ttu-id="bdc30-106">Il cmdlet **set-AzureTrafficManagerProfile** aggiorna le proprietà di un profilo di gestione traffico di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bdc30-106">The **Set-AzureTrafficManagerProfile** cmdlet updates the properties of a Microsoft Azure Traffic Manager profile.</span></span>

<span data-ttu-id="bdc30-107">Per i profili per cui è stato impostato il valore *LoadBalancingMethod* su "failover", è possibile determinare l'ordine di failover degli endpoint aggiunti al profilo con il cmdlet Add-AzureTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="bdc30-107">For profiles for which you have set the *LoadBalancingMethod* value to "Failover", you can determine the failover order of the endpoints you have added to your profile with the Add-AzureTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="bdc30-108">Per altre informazioni, vedere l'esempio 3 seguente.</span><span class="sxs-lookup"><span data-stu-id="bdc30-108">For more information, see Example 3 below.</span></span>

## <span data-ttu-id="bdc30-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bdc30-109">EXAMPLES</span></span>

### <span data-ttu-id="bdc30-110">Esempio 1: impostare il TTL per un profilo di gestione traffico</span><span class="sxs-lookup"><span data-stu-id="bdc30-110">Example 1: Set the TTL for a Traffic Manager profile</span></span>
```
PS C:\>Set-AzureTrafficManagerProfile -TrafficManagerProfile $MyTrafficManagerProfile -Ttl 60
```

<span data-ttu-id="bdc30-111">Questo comando imposta il TTL su 60 secondi per l'oggetto MyTrafficManagerProfile del profilo di Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="bdc30-111">This command sets the TTL to 60 seconds for the Traffic Manager profile object MyTrafficManagerProfile.</span></span>

### <span data-ttu-id="bdc30-112">Esempio 2: impostare diversi valori per un profilo</span><span class="sxs-lookup"><span data-stu-id="bdc30-112">Example 2: Set several values for a profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Set-AzureTrafficManagerProfile -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

<span data-ttu-id="bdc30-113">Questo comando ottiene un profilo di gestione traffico denominato profilo tramite il cmdlet **Get-AzureTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="bdc30-113">This command gets a Traffic Manager profile named MyProfile by using the **Get-AzureTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="bdc30-114">Il profilo usa il metodo di bilanciamento del carico RoundRobin, un TTL di 30 secondi, il protocollo HTTP monitor, la porta del monitor e il percorso relativo di un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="bdc30-114">The profile uses the RoundRobin load balancing method, a TTL of 30 seconds,  the monitor protocol HTTP, the monitor port, and the relative path for a Traffic Manager profile.</span></span>

### <span data-ttu-id="bdc30-115">Esempio 3: riordinare gli endpoint nell'ordine di failover desiderato</span><span class="sxs-lookup"><span data-stu-id="bdc30-115">Example 3: Reorder endpoints to desired failover order</span></span>
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

<span data-ttu-id="bdc30-116">In questo esempio vengono riordinati gli endpoint aggiunti a my profile all'ordine di failover desiderato.</span><span class="sxs-lookup"><span data-stu-id="bdc30-116">This example reorders the endpoints added to MyProfile to the desired failover order.</span></span>

<span data-ttu-id="bdc30-117">Il primo comando ottiene l'oggetto profilo Traffic Manager denominato profilo e archivia l'oggetto nella variabile $Profile.</span><span class="sxs-lookup"><span data-stu-id="bdc30-117">The first command gets the Traffic Manager profile object named MyProfile and stores the object in the $Profile variable.</span></span>

<span data-ttu-id="bdc30-118">Il secondo comando Riordina gli endpoint dalla matrice Endpoints all'ordine in cui deve essere eseguito il failover.</span><span class="sxs-lookup"><span data-stu-id="bdc30-118">The second command re-orders the endpoints from  the endpoints array to the order in which failover should occur.</span></span>

<span data-ttu-id="bdc30-119">L'ultimo comando Aggiorna il profilo di Traffic Manager archiviato in $Profile con il nuovo ordine di endpoint.</span><span class="sxs-lookup"><span data-stu-id="bdc30-119">The last command updates the Traffic Manager profile stored in $Profile with the new endpoint order.</span></span>

## <span data-ttu-id="bdc30-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bdc30-120">PARAMETERS</span></span>

### <span data-ttu-id="bdc30-121">-LoadBalancingMethod</span><span class="sxs-lookup"><span data-stu-id="bdc30-121">-LoadBalancingMethod</span></span>
<span data-ttu-id="bdc30-122">Specifica il metodo di bilanciamento del carico da usare per distribuire la connessione.</span><span class="sxs-lookup"><span data-stu-id="bdc30-122">Specifies the load balancing method to use to distribute the connection.</span></span>
<span data-ttu-id="bdc30-123">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="bdc30-123">Valid values are:</span></span> 

- <span data-ttu-id="bdc30-124">Prestazioni</span><span class="sxs-lookup"><span data-stu-id="bdc30-124">Performance</span></span>
- <span data-ttu-id="bdc30-125">Failover</span><span class="sxs-lookup"><span data-stu-id="bdc30-125">Failover</span></span>
- <span data-ttu-id="bdc30-126">RoundRobin</span><span class="sxs-lookup"><span data-stu-id="bdc30-126">RoundRobin</span></span>

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

### <span data-ttu-id="bdc30-127">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="bdc30-127">-MonitorPort</span></span>
<span data-ttu-id="bdc30-128">Specifica la porta utilizzata per monitorare l'integrità dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="bdc30-128">Specifies the port used to monitor endpoint health.</span></span>
<span data-ttu-id="bdc30-129">I valori validi sono valori interi maggiori di 0 e minore o uguale a 65.535.</span><span class="sxs-lookup"><span data-stu-id="bdc30-129">Valid values are integer values greater than 0 and less than or equal to 65,535.</span></span>

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

### <span data-ttu-id="bdc30-130">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="bdc30-130">-MonitorProtocol</span></span>
<span data-ttu-id="bdc30-131">Specifica il protocollo da usare per monitorare l'integrità degli endpoint.</span><span class="sxs-lookup"><span data-stu-id="bdc30-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="bdc30-132">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="bdc30-132">Valid values are:</span></span> 

- <span data-ttu-id="bdc30-133">Http</span><span class="sxs-lookup"><span data-stu-id="bdc30-133">Http</span></span>
- <span data-ttu-id="bdc30-134">Https</span><span class="sxs-lookup"><span data-stu-id="bdc30-134">Https</span></span>

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

### <span data-ttu-id="bdc30-135">-MonitorRelativePath</span><span class="sxs-lookup"><span data-stu-id="bdc30-135">-MonitorRelativePath</span></span>
<span data-ttu-id="bdc30-136">Specifica il percorso relativo al nome di dominio dell'endpoint da sondare per lo stato di integrità.</span><span class="sxs-lookup"><span data-stu-id="bdc30-136">Specifies the path relative to the endpoint domain name to probe for health state.</span></span>
<span data-ttu-id="bdc30-137">Il percorso deve soddisfare le restrizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="bdc30-137">The path must meet the following restrictions:</span></span> 

- <span data-ttu-id="bdc30-138">Il percorso deve essere compreso tra 1 e 1000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="bdc30-138">The path must be from 1 through 1000 characters.</span></span>
- <span data-ttu-id="bdc30-139">Deve iniziare con una barra di avanzamento/.</span><span class="sxs-lookup"><span data-stu-id="bdc30-139">It must start with a forward slash, /.</span></span>
- <span data-ttu-id="bdc30-140">Non deve contenere elementi XML \<\> .</span><span class="sxs-lookup"><span data-stu-id="bdc30-140">It must contain no XML elements, \<\>.</span></span>
- <span data-ttu-id="bdc30-141">Non deve contenere barre doppie,//.</span><span class="sxs-lookup"><span data-stu-id="bdc30-141">It must contain no double slashes, //.</span></span>
- <span data-ttu-id="bdc30-142">Non deve contenere caratteri di escape HTML non validi.</span><span class="sxs-lookup"><span data-stu-id="bdc30-142">It must contain no invalid HTML escape characters.</span></span>
<span data-ttu-id="bdc30-143">Ad esempio,% XY.</span><span class="sxs-lookup"><span data-stu-id="bdc30-143">For example, %XY.</span></span>

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

### <span data-ttu-id="bdc30-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="bdc30-144">-Name</span></span>
<span data-ttu-id="bdc30-145">Specifica il nome del profilo di Traffic Manager da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="bdc30-145">Specifies the name of the Traffic Manager profile to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdc30-146">-Profile</span><span class="sxs-lookup"><span data-stu-id="bdc30-146">-Profile</span></span>
<span data-ttu-id="bdc30-147">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdc30-147">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="bdc30-148">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="bdc30-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bdc30-149">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bdc30-149">-TrafficManagerProfile</span></span>
<span data-ttu-id="bdc30-150">Specifica l'oggetto profilo Traffic Manager usato per impostare il profilo.</span><span class="sxs-lookup"><span data-stu-id="bdc30-150">Specifies the Traffic Manager profile object you use to set the profile.</span></span>

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdc30-151">-TTL</span><span class="sxs-lookup"><span data-stu-id="bdc30-151">-Ttl</span></span>
<span data-ttu-id="bdc30-152">Specifica il TTL (time-to-Live) DNS che informa i resolver DNS locali della durata della cache delle voci DNS.</span><span class="sxs-lookup"><span data-stu-id="bdc30-152">Specifies the DNS Time-to-Live (TTL) that informs the Local DNS resolvers how long to cache DNS entries.</span></span>
<span data-ttu-id="bdc30-153">I valori validi sono un numero intero compreso tra 30 e 999.999.</span><span class="sxs-lookup"><span data-stu-id="bdc30-153">Valid values are an integer from 30 through 999,999.</span></span>

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

### <span data-ttu-id="bdc30-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdc30-154">CommonParameters</span></span>
<span data-ttu-id="bdc30-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdc30-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdc30-156">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdc30-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdc30-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bdc30-157">INPUTS</span></span>

## <span data-ttu-id="bdc30-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bdc30-158">OUTPUTS</span></span>

### <span data-ttu-id="bdc30-159">Microsoft. WindowsAzure. Commands. Utilities. TrafficManager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="bdc30-159">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="bdc30-160">Questo cmdlet genera un oggetto profilo di Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="bdc30-160">This cmdlet generates a Traffic Manager profile object.</span></span>

## <span data-ttu-id="bdc30-161">Note</span><span class="sxs-lookup"><span data-stu-id="bdc30-161">NOTES</span></span>

## <span data-ttu-id="bdc30-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bdc30-162">RELATED LINKS</span></span>

[<span data-ttu-id="bdc30-163">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bdc30-163">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="bdc30-164">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bdc30-164">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="bdc30-165">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bdc30-165">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="bdc30-166">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bdc30-166">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="bdc30-167">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bdc30-167">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)


