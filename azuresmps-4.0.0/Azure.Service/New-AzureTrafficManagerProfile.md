---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 2287E103-442D-47FB-8279-0AE5936412C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6a12f0e74964e096577b5a4fec0a46fd41d7872
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029664"
---
# <span data-ttu-id="c9db6-101">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c9db6-101">New-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="c9db6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9db6-102">SYNOPSIS</span></span>
<span data-ttu-id="c9db6-103">Crea un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="c9db6-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="c9db6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9db6-104">SYNTAX</span></span>

```
New-AzureTrafficManagerProfile -Name <String> -DomainName <String> -LoadBalancingMethod <String>
 -MonitorPort <Int32> -MonitorProtocol <String> -MonitorRelativePath <String> -Ttl <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c9db6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9db6-105">DESCRIPTION</span></span>
<span data-ttu-id="c9db6-106">Il cmdlet **New-AzureTrafficManagerProfile** crea un profilo di Microsoft Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="c9db6-106">The **New-AzureTrafficManagerProfile** cmdlet creates a Microsoft Azure Traffic Manager profile.</span></span>

<span data-ttu-id="c9db6-107">Dopo aver creato un profilo in cui si imposta il valore *LoadBalancingMethod* su "failover", è possibile determinare l'ordine di failover degli endpoint aggiunti al profilo con il cmdlet Add-AzureTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="c9db6-107">After you create a profile where you set the *LoadBalancingMethod* value to "Failover", you can determine the failover order of the endpoints you add to your profile with the Add-AzureTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="c9db6-108">Per altre informazioni, vedere l'esempio 2 seguente.</span><span class="sxs-lookup"><span data-stu-id="c9db6-108">For more information, see Example 2 below.</span></span>

## <span data-ttu-id="c9db6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9db6-109">EXAMPLES</span></span>

### <span data-ttu-id="c9db6-110">Esempio 1: creare un profilo di Traffic Manager</span><span class="sxs-lookup"><span data-stu-id="c9db6-110">Example 1: Create a Traffic Manager profile</span></span>
```
PS C:\>New-AzureTrafficManagerProfile -Name "MyProfile" -DomainName "My.profile.trafficmanager.net" -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

<span data-ttu-id="c9db6-111">Questo comando crea un profilo di gestione traffico denominato profilo nel dominio di gestione traffico specificato con un metodo di bilanciamento del carico rotondo Robin, un TTL di 30 secondi, il protocollo di monitoraggio HTTP, la porta di monitoraggio 80 e il percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="c9db6-111">This command creates a Traffic Manager profile named MyProfile in the specified Traffic Manager domain with a Round Robin load balancing method, a TTL of 30 seconds, HTTP monitoring protocol, monitoring port 80, and with the specified path.</span></span>

### <span data-ttu-id="c9db6-112">Esempio 2: riordinare gli endpoint nell'ordine di failover desiderato</span><span class="sxs-lookup"><span data-stu-id="c9db6-112">Example 2: Reorder endpoints to desired failover order</span></span>
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

<span data-ttu-id="c9db6-113">In questo esempio vengono riordinati gli endpoint aggiunti a my profile all'ordine di failover desiderato.</span><span class="sxs-lookup"><span data-stu-id="c9db6-113">This example reorders the endpoints added to MyProfile to the desired failover order.</span></span>

<span data-ttu-id="c9db6-114">Il primo comando ottiene l'oggetto profilo Traffic Manager denominato profilo e archivia l'oggetto nella variabile $Profile.</span><span class="sxs-lookup"><span data-stu-id="c9db6-114">The first command gets the Traffic Manager profile object named MyProfile and stores the object in the $Profile variable.</span></span>

<span data-ttu-id="c9db6-115">Il secondo comando Riordina gli endpoint dalla matrice Endpoints all'ordine in cui deve essere eseguito il failover.</span><span class="sxs-lookup"><span data-stu-id="c9db6-115">The second command re-orders the endpoints from  the endpoints array to the order in which failover should occur.</span></span>

<span data-ttu-id="c9db6-116">L'ultimo comando Aggiorna il profilo di Traffic Manager archiviato in $Profile con il nuovo ordine di endpoint.</span><span class="sxs-lookup"><span data-stu-id="c9db6-116">The last command updates the Traffic Manager profile stored in $Profile with the new endpoint order.</span></span>

## <span data-ttu-id="c9db6-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9db6-117">PARAMETERS</span></span>

### <span data-ttu-id="c9db6-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="c9db6-118">-DomainName</span></span>
<span data-ttu-id="c9db6-119">Specifica il nome di dominio del profilo di Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="c9db6-119">Specifies the domain name of the Traffic Manager profile.</span></span>
<span data-ttu-id="c9db6-120">Deve essere un sottodominio di trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="c9db6-120">This must be a subdomain of trafficmanager.net.</span></span>

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

### <span data-ttu-id="c9db6-121">-LoadBalancingMethod</span><span class="sxs-lookup"><span data-stu-id="c9db6-121">-LoadBalancingMethod</span></span>
<span data-ttu-id="c9db6-122">Specifica il metodo di bilanciamento del carico da usare per distribuire la connessione.</span><span class="sxs-lookup"><span data-stu-id="c9db6-122">Specifies the load balancing method to use to distribute the connection.</span></span>
<span data-ttu-id="c9db6-123">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="c9db6-123">Valid values are:</span></span> 

- <span data-ttu-id="c9db6-124">Prestazioni</span><span class="sxs-lookup"><span data-stu-id="c9db6-124">Performance</span></span>
- <span data-ttu-id="c9db6-125">Failover</span><span class="sxs-lookup"><span data-stu-id="c9db6-125">Failover</span></span>
- <span data-ttu-id="c9db6-126">RoundRobin</span><span class="sxs-lookup"><span data-stu-id="c9db6-126">RoundRobin</span></span>

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

### <span data-ttu-id="c9db6-127">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="c9db6-127">-MonitorPort</span></span>
<span data-ttu-id="c9db6-128">Specifica la porta utilizzata per monitorare l'integrità dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="c9db6-128">Specifies the port used to monitor endpoint health.</span></span>
<span data-ttu-id="c9db6-129">I valori validi sono valori interi maggiori di 0 e minore o uguale a 65.535.</span><span class="sxs-lookup"><span data-stu-id="c9db6-129">Valid values are integer values greater than 0 and less than or equal to 65,535.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9db6-130">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="c9db6-130">-MonitorProtocol</span></span>
<span data-ttu-id="c9db6-131">Specifica il protocollo da usare per monitorare l'integrità degli endpoint.</span><span class="sxs-lookup"><span data-stu-id="c9db6-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="c9db6-132">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="c9db6-132">Valid values are:</span></span> 

- <span data-ttu-id="c9db6-133">Http</span><span class="sxs-lookup"><span data-stu-id="c9db6-133">Http</span></span>

- <span data-ttu-id="c9db6-134">Https</span><span class="sxs-lookup"><span data-stu-id="c9db6-134">Https</span></span>

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

### <span data-ttu-id="c9db6-135">-MonitorRelativePath</span><span class="sxs-lookup"><span data-stu-id="c9db6-135">-MonitorRelativePath</span></span>
<span data-ttu-id="c9db6-136">Specifica il percorso relativo al nome di dominio dell'endpoint da sondare per lo stato di integrità.</span><span class="sxs-lookup"><span data-stu-id="c9db6-136">Specifies the path relative to the endpoint domain name to probe for health state.</span></span>
<span data-ttu-id="c9db6-137">Il percorso deve soddisfare le restrizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c9db6-137">The path must meet the following restrictions:</span></span> 

- <span data-ttu-id="c9db6-138">Il percorso deve essere compreso tra 1 e 1000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="c9db6-138">The path must be from 1 through 1000 characters.</span></span>

- <span data-ttu-id="c9db6-139">Deve iniziare con una barra di avanzamento/.</span><span class="sxs-lookup"><span data-stu-id="c9db6-139">It must start with a forward slash, /.</span></span>

- <span data-ttu-id="c9db6-140">Non deve contenere elementi XML \<\> .</span><span class="sxs-lookup"><span data-stu-id="c9db6-140">It must contain no XML elements, \<\>.</span></span>

- <span data-ttu-id="c9db6-141">Non deve contenere barre doppie,//.</span><span class="sxs-lookup"><span data-stu-id="c9db6-141">It must contain no double slashes, //.</span></span>

- <span data-ttu-id="c9db6-142">Non deve contenere caratteri di escape HTML non validi.</span><span class="sxs-lookup"><span data-stu-id="c9db6-142">It must contain no invalid HTML escape characters.</span></span>
<span data-ttu-id="c9db6-143">Ad esempio,% XY.</span><span class="sxs-lookup"><span data-stu-id="c9db6-143">For example, %XY.</span></span>

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

### <span data-ttu-id="c9db6-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9db6-144">-Name</span></span>
<span data-ttu-id="c9db6-145">Specifica il nome del profilo di Traffic Manager da creare.</span><span class="sxs-lookup"><span data-stu-id="c9db6-145">Specifies the name of the Traffic Manager profile to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9db6-146">-Profile</span><span class="sxs-lookup"><span data-stu-id="c9db6-146">-Profile</span></span>
<span data-ttu-id="c9db6-147">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9db6-147">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c9db6-148">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c9db6-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c9db6-149">-TTL</span><span class="sxs-lookup"><span data-stu-id="c9db6-149">-Ttl</span></span>
<span data-ttu-id="c9db6-150">Specifica il TTL (time-to-Live) DNS che informa i resolver DNS locali della durata della cache delle voci DNS.</span><span class="sxs-lookup"><span data-stu-id="c9db6-150">Specifies the DNS Time-to-Live (TTL) that informs the Local DNS resolvers how long to cache DNS entries.</span></span>
<span data-ttu-id="c9db6-151">I valori validi sono numeri interi compresi tra 30 e 999.999.</span><span class="sxs-lookup"><span data-stu-id="c9db6-151">Valid values are integers from 30 through 999,999.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9db6-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9db6-152">CommonParameters</span></span>
<span data-ttu-id="c9db6-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9db6-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9db6-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9db6-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9db6-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9db6-155">INPUTS</span></span>

## <span data-ttu-id="c9db6-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9db6-156">OUTPUTS</span></span>

### <span data-ttu-id="c9db6-157">Microsoft. WindowsAzure. Commands. Utilities. TrafficManager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="c9db6-157">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="c9db6-158">Questo cmdlet genera un oggetto profilo di Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="c9db6-158">This cmdlet generates a Traffic Manager profile object.</span></span>

## <span data-ttu-id="c9db6-159">Note</span><span class="sxs-lookup"><span data-stu-id="c9db6-159">NOTES</span></span>

## <span data-ttu-id="c9db6-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9db6-160">RELATED LINKS</span></span>

[<span data-ttu-id="c9db6-161">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c9db6-161">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="c9db6-162">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c9db6-162">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="c9db6-163">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c9db6-163">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="c9db6-164">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c9db6-164">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="c9db6-165">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c9db6-165">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


