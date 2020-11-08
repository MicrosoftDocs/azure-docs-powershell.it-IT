---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: FAEA7859-7E58-4343-AD57-7EFC0D87432E
online version: ''
schema: 2.0.0
ms.openlocfilehash: d2886faacd3e9f7d02a008a056dc2145844f8b30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023392"
---
# <span data-ttu-id="e6bed-101">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6bed-101">Set-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="e6bed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6bed-102">SYNOPSIS</span></span>
<span data-ttu-id="e6bed-103">Aggiorna le proprietà di un endpoint in un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="e6bed-103">Updates the properties of an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="e6bed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6bed-104">SYNTAX</span></span>

```
Set-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] [-Type <String>] [-Status <String>]
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e6bed-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6bed-105">DESCRIPTION</span></span>
<span data-ttu-id="e6bed-106">Il cmdlet **set-AzureTrafficManagerEndpoint** aggiorna le proprietà di un endpoint in un profilo di gestione traffico di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e6bed-106">The **Set-AzureTrafficManagerEndpoint** cmdlet updates the properties of an endpoint in a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="e6bed-107">Se l'endpoint non esiste nel profilo corrente, questo cmdlet lo crea.</span><span class="sxs-lookup"><span data-stu-id="e6bed-107">If the endpoint does not exist in the current profile, this cmdlet creates it.</span></span>
<span data-ttu-id="e6bed-108">Dopo aver aggiunto un endpoint, passa il risultato al cmdlet **set-AzureTrafficManagerProfile** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="e6bed-108">After you add an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e6bed-109">Questo cmdlet si connette a Azure per salvare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="e6bed-109">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="e6bed-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6bed-110">EXAMPLES</span></span>

### <span data-ttu-id="e6bed-111">Esempio 1: aggiornare un endpoint per un profilo</span><span class="sxs-lookup"><span data-stu-id="e6bed-111">Example 1: Update an endpoint for a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Set-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "ContosoApp02.cloudapp.net" -Status "Enabled" -Type "CloudService" -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="e6bed-112">Il primo comando usa il cmdlet **Get-AzureTrafficManagerProfile** per ottenere il profilo denominato ContosoProfile e lo archivia nella variabile $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="e6bed-112">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="e6bed-113">Il secondo comando Aggiorna l'endpoint nel profilo di Traffic Manager archiviato in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="e6bed-113">The second command updates the endpoint in the Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="e6bed-114">L'endpoint ha il nome di dominio ContosoApp02.cloudapp.net.</span><span class="sxs-lookup"><span data-stu-id="e6bed-114">The endpoint has the domain name ContosoApp02.cloudapp.net.</span></span>
<span data-ttu-id="e6bed-115">Il comando specifica inoltre lo stato, il tipo, il peso e la posizione dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="e6bed-115">The command also specifies the status, type, weight, and location of the endpoint.</span></span>
<span data-ttu-id="e6bed-116">Il comando passa il profilo modificato al cmdlet **set-AzureTrafficManagerProfile** per connettersi a Azure per salvare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="e6bed-116">The command passes the modified profile to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="e6bed-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6bed-117">PARAMETERS</span></span>

### <span data-ttu-id="e6bed-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="e6bed-118">-DomainName</span></span>
<span data-ttu-id="e6bed-119">Specifica il nome di dominio dell'endpoint da modificare.</span><span class="sxs-lookup"><span data-stu-id="e6bed-119">Specifies the domain name of the endpoint to modify.</span></span>

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

### <span data-ttu-id="e6bed-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e6bed-120">-Location</span></span>
<span data-ttu-id="e6bed-121">Specifica la posizione dell'endpoint aggiunto dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6bed-121">Specifies the location of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="e6bed-122">Deve essere una posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e6bed-122">This must be an Azure location.</span></span>

<span data-ttu-id="e6bed-123">Questo parametro deve contenere un valore per gli endpoint del tipo "any" o di tipo "TrafficManager" in un profilo con il metodo di bilanciamento del carico impostato su "performance".</span><span class="sxs-lookup"><span data-stu-id="e6bed-123">This parameter must contain a value for endpoints of the type "Any" or of type "TrafficManager" in a profile that has the load balancing method set to "Performance".</span></span>
<span data-ttu-id="e6bed-124">I valori possibili sono i nomi delle aree di Azure, come indicato in  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/ .</span><span class="sxs-lookup"><span data-stu-id="e6bed-124">The possible values are the Azure region names, as listed at  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/.</span></span>

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

### <span data-ttu-id="e6bed-125">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="e6bed-125">-MinChildEndpoints</span></span>
<span data-ttu-id="e6bed-126">Specifica il numero minimo di endpoint che il profilo annidato deve avere online affinché l'endpoint venga considerato online.</span><span class="sxs-lookup"><span data-stu-id="e6bed-126">Specifies the minimum number of endpoints the nested profile must have online for this endpoint to be considered online.</span></span>

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

### <span data-ttu-id="e6bed-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="e6bed-127">-Profile</span></span>
<span data-ttu-id="e6bed-128">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6bed-128">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="e6bed-129">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="e6bed-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e6bed-130">-Stato</span><span class="sxs-lookup"><span data-stu-id="e6bed-130">-Status</span></span>
<span data-ttu-id="e6bed-131">Specifica lo stato dell'endpoint di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="e6bed-131">Specifies the status of the monitoring endpoint.</span></span>
<span data-ttu-id="e6bed-132">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="e6bed-132">Valid values are:</span></span> 

- <span data-ttu-id="e6bed-133">Abilitato</span><span class="sxs-lookup"><span data-stu-id="e6bed-133">Enabled</span></span>
- <span data-ttu-id="e6bed-134">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="e6bed-134">Disabled</span></span>

<span data-ttu-id="e6bed-135">Se specifichi un valore di Enabled, Traffic Manager monitora l'endpoint e il metodo di bilanciamento del carico lo considera quando Gestisci il traffico.</span><span class="sxs-lookup"><span data-stu-id="e6bed-135">If you specify a value of Enabled, Traffic Manager monitors the endpoint and the load-balancing method considers it when managing traffic.</span></span>

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

### <span data-ttu-id="e6bed-136">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e6bed-136">-TrafficManagerProfile</span></span>
<span data-ttu-id="e6bed-137">Specifica l'oggetto profilo Traffic Manager per cui modificare l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="e6bed-137">Specifies the Traffic Manager profile object for which to modify the endpoint.</span></span>

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

### <span data-ttu-id="e6bed-138">-Digitare</span><span class="sxs-lookup"><span data-stu-id="e6bed-138">-Type</span></span>
<span data-ttu-id="e6bed-139">Specifica il tipo di endpoint.</span><span class="sxs-lookup"><span data-stu-id="e6bed-139">Specifies the type of endpoint.</span></span>
<span data-ttu-id="e6bed-140">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="e6bed-140">Valid values are:</span></span> 

- <span data-ttu-id="e6bed-141">CloudService</span><span class="sxs-lookup"><span data-stu-id="e6bed-141">CloudService</span></span>
- <span data-ttu-id="e6bed-142">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e6bed-142">AzureWebsite</span></span>
- <span data-ttu-id="e6bed-143">TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e6bed-143">TrafficManager</span></span>

- <span data-ttu-id="e6bed-144">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="e6bed-144">Any</span></span> 

<span data-ttu-id="e6bed-145">Se sono presenti più endpoint AzureWebsite, gli endpoint devono trovarsi in diversi datacenter.</span><span class="sxs-lookup"><span data-stu-id="e6bed-145">If there is more than one AzureWebsite endpoint, the endpoints must be in different datacenters.</span></span>

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

### <span data-ttu-id="e6bed-146">-Peso</span><span class="sxs-lookup"><span data-stu-id="e6bed-146">-Weight</span></span>
<span data-ttu-id="e6bed-147">Specifica il peso dell'endpoint aggiunto dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6bed-147">Specifies the weight of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="e6bed-148">L'intervallo di valori valido per questo parametro è 1.000 \[ \] .</span><span class="sxs-lookup"><span data-stu-id="e6bed-148">The valid value range for this parameter is \[1,1000\].</span></span>

<span data-ttu-id="e6bed-149">Questo parametro viene usato solo per i criteri di bilanciamento del carico di RoundRobin.</span><span class="sxs-lookup"><span data-stu-id="e6bed-149">This parameter is only used for RoundRobin load balancing policies.</span></span>

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

### <span data-ttu-id="e6bed-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6bed-150">CommonParameters</span></span>
<span data-ttu-id="e6bed-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6bed-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6bed-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6bed-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6bed-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6bed-153">INPUTS</span></span>

## <span data-ttu-id="e6bed-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6bed-154">OUTPUTS</span></span>

### <span data-ttu-id="e6bed-155">Microsoft. WindowsAzure. Commands. Utilities. TrafficManager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="e6bed-155">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="e6bed-156">Questo cmdlet genera un oggetto profilo di Traffic Manager, che contiene informazioni sul profilo aggiornato.</span><span class="sxs-lookup"><span data-stu-id="e6bed-156">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="e6bed-157">Note</span><span class="sxs-lookup"><span data-stu-id="e6bed-157">NOTES</span></span>

## <span data-ttu-id="e6bed-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6bed-158">RELATED LINKS</span></span>

[<span data-ttu-id="e6bed-159">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6bed-159">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="e6bed-160">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6bed-160">Remove-AzureTrafficManagerEndpoint</span></span>](./Remove-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="e6bed-161">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e6bed-161">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="e6bed-162">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e6bed-162">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


