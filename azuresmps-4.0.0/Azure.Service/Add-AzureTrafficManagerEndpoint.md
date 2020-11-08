---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: CF1FC482-812D-4BAD-BA3A-D88E614A5165
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79f212e83ece1def42c6d8de343a42e087f5181a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029838"
---
# <span data-ttu-id="1df11-101">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1df11-101">Add-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="1df11-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1df11-102">SYNOPSIS</span></span>
<span data-ttu-id="1df11-103">Aggiunge un endpoint a un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="1df11-103">Adds an endpoint to a Traffic Manager profile.</span></span>

## <span data-ttu-id="1df11-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1df11-104">SYNTAX</span></span>

```
Add-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] -Type <String> -Status <String>
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1df11-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1df11-105">DESCRIPTION</span></span>
<span data-ttu-id="1df11-106">Il cmdlet **Add-AzureTrafficManagerEndpoint** aggiunge un endpoint a un profilo di gestione traffico di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1df11-106">The **Add-AzureTrafficManagerEndpoint** cmdlet adds an endpoint to a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="1df11-107">Dopo aver aggiunto un endpoint, passa il risultato al cmdlet **set-AzureTrafficManagerProfile** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="1df11-107">After you add an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1df11-108">Questo cmdlet si connette a Azure per salvare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="1df11-108">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="1df11-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1df11-109">EXAMPLES</span></span>

### <span data-ttu-id="1df11-110">Esempio 1: aggiungere un endpoint a un profilo</span><span class="sxs-lookup"><span data-stu-id="1df11-110">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Add-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" -Status "Enabled" -Type "CloudService" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="1df11-111">Il primo comando usa il cmdlet **Get-AzureTrafficManagerProfile** per ottenere il profilo denominato ContosoProfile e lo archivia nella variabile $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="1df11-111">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="1df11-112">Il secondo comando aggiunge un endpoint al profilo di Traffic Manager archiviato in $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="1df11-112">The second command adds an endpoint to Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="1df11-113">L'endpoint ha il nome di dominio Contoso02App.couldapp.net.</span><span class="sxs-lookup"><span data-stu-id="1df11-113">The endpoint has the domain name Contoso02App.couldapp.net.</span></span>
<span data-ttu-id="1df11-114">Il comando specifica anche se è abilitato e il relativo tipo.</span><span class="sxs-lookup"><span data-stu-id="1df11-114">The command also specifies whether it is enabled and its type.</span></span>
<span data-ttu-id="1df11-115">Il comando passa l'oggetto profile al cmdlet **set-AzureTrafficManagerProfile** per connettersi a Azure per salvare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="1df11-115">The command passes the profile object to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

### <span data-ttu-id="1df11-116">Esempio 2: aggiungere un endpoint con una posizione e un peso specificati</span><span class="sxs-lookup"><span data-stu-id="1df11-116">Example 2: Add an endpoint that has a specified location and weight</span></span>
```
PS C:\>Add-AzureTrafficManagerEndpoint -TrafficManagerProfile ContosoTrafficManagerProfile -DomainName " Contoso02App.cloudapp.net" -Status Enabled -Type CloudService -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="1df11-117">Questo comando aggiunge un endpoint a un profilo di gestione traffico.</span><span class="sxs-lookup"><span data-stu-id="1df11-117">This command adds an endpoint to a Traffic Manager profile.</span></span>
<span data-ttu-id="1df11-118">L'endpoint ha il nome di dominio Contoso02App.couldapp.net.</span><span class="sxs-lookup"><span data-stu-id="1df11-118">The endpoint has the domain name Contoso02App.couldapp.net.</span></span>
<span data-ttu-id="1df11-119">Il comando specifica anche se è abilitato e il relativo tipo.</span><span class="sxs-lookup"><span data-stu-id="1df11-119">The command also specifies whether it is enabled and its type.</span></span>
<span data-ttu-id="1df11-120">Il comando specifica anche il peso e la posizione per l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="1df11-120">The command also specifies the weight and location for the endpoint.</span></span>
<span data-ttu-id="1df11-121">Il comando passa l'oggetto profile a **set-AzureTrafficManagerProfile** per connettersi ad Azure per salvare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="1df11-121">The command passes the profile object to **Set-AzureTrafficManagerProfile** to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="1df11-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1df11-122">PARAMETERS</span></span>

### <span data-ttu-id="1df11-123">-DomainName</span><span class="sxs-lookup"><span data-stu-id="1df11-123">-DomainName</span></span>
<span data-ttu-id="1df11-124">Specifica il nome di dominio dell'endpoint da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="1df11-124">Specifies the domain name of the endpoint to add.</span></span>

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

### <span data-ttu-id="1df11-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1df11-125">-Location</span></span>
<span data-ttu-id="1df11-126">Specifica la posizione dell'endpoint aggiunto dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1df11-126">Specifies the location of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="1df11-127">Deve essere una posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1df11-127">This must be an Azure location.</span></span>

<span data-ttu-id="1df11-128">Questo parametro deve contenere un valore per gli endpoint del tipo "any" o di tipo "TrafficManager" in un profilo con il metodo di bilanciamento del carico impostato su "performance".</span><span class="sxs-lookup"><span data-stu-id="1df11-128">This parameter must contain a value for endpoints of the type "Any" or of type "TrafficManager" in a profile that has the load balancing method set to "Performance".</span></span>
<span data-ttu-id="1df11-129">I valori possibili sono i nomi delle aree di Azure, come indicato in https://azure.microsoft.com/regions/ .</span><span class="sxs-lookup"><span data-stu-id="1df11-129">The possible values are the Azure region names, as listed at https://azure.microsoft.com/regions/.</span></span>

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

### <span data-ttu-id="1df11-130">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="1df11-130">-MinChildEndpoints</span></span>
<span data-ttu-id="1df11-131">Specifica il numero minimo di endpoint che il profilo annidato deve avere online affinché l'endpoint venga considerato online.</span><span class="sxs-lookup"><span data-stu-id="1df11-131">Specifies the minimum number of endpoints the nested profile must have online for this endpoint to be considered online.</span></span>

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

### <span data-ttu-id="1df11-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="1df11-132">-Profile</span></span>
<span data-ttu-id="1df11-133">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1df11-133">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="1df11-134">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="1df11-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1df11-135">-Stato</span><span class="sxs-lookup"><span data-stu-id="1df11-135">-Status</span></span>
<span data-ttu-id="1df11-136">Specifica lo stato dell'endpoint di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="1df11-136">Specifies the status of the monitoring endpoint.</span></span>
<span data-ttu-id="1df11-137">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="1df11-137">Valid values are:</span></span> 

- <span data-ttu-id="1df11-138">Abilitato</span><span class="sxs-lookup"><span data-stu-id="1df11-138">Enabled</span></span>
- <span data-ttu-id="1df11-139">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="1df11-139">Disabled</span></span>

<span data-ttu-id="1df11-140">Se specifichi un valore di Enabled, Traffic Manager monitora l'endpoint e il metodo di bilanciamento del carico lo considera quando Gestisci il traffico.</span><span class="sxs-lookup"><span data-stu-id="1df11-140">If you specify a value of Enabled, Traffic Manager monitors the endpoint and the load-balancing method considers it when managing traffic.</span></span>

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

### <span data-ttu-id="1df11-141">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1df11-141">-TrafficManagerProfile</span></span>
<span data-ttu-id="1df11-142">Specifica l'oggetto profilo Traffic Manager a cui aggiungere l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="1df11-142">Specifies the Traffic Manager profile object to which to add the endpoint.</span></span>

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

### <span data-ttu-id="1df11-143">-Digitare</span><span class="sxs-lookup"><span data-stu-id="1df11-143">-Type</span></span>
<span data-ttu-id="1df11-144">Specifica il tipo di endpoint.</span><span class="sxs-lookup"><span data-stu-id="1df11-144">Specifies the type of endpoint.</span></span>
<span data-ttu-id="1df11-145">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="1df11-145">Valid values are:</span></span> 

- <span data-ttu-id="1df11-146">CloudService</span><span class="sxs-lookup"><span data-stu-id="1df11-146">CloudService</span></span>
- <span data-ttu-id="1df11-147">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1df11-147">AzureWebsite</span></span>
- <span data-ttu-id="1df11-148">TrafficManager</span><span class="sxs-lookup"><span data-stu-id="1df11-148">TrafficManager</span></span>

- <span data-ttu-id="1df11-149">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="1df11-149">Any</span></span> 

<span data-ttu-id="1df11-150">Se sono presenti più endpoint AzureWebsite, gli endpoint devono trovarsi in diversi datacenter.</span><span class="sxs-lookup"><span data-stu-id="1df11-150">If there is more than one AzureWebsite endpoint, the endpoints must be in different datacenters.</span></span>

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

### <span data-ttu-id="1df11-151">-Peso</span><span class="sxs-lookup"><span data-stu-id="1df11-151">-Weight</span></span>
<span data-ttu-id="1df11-152">Specifica il peso dell'endpoint aggiunto dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1df11-152">Specifies the weight of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="1df11-153">L'intervallo di valori valido per questo parametro è 1.000 \[ \] .</span><span class="sxs-lookup"><span data-stu-id="1df11-153">The valid value range for this parameter is \[1,1000\].</span></span>

<span data-ttu-id="1df11-154">Questo parametro viene usato solo per i criteri di bilanciamento del carico di RoundRobin.</span><span class="sxs-lookup"><span data-stu-id="1df11-154">This parameter is only used for RoundRobin load balancing policies.</span></span>

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

### <span data-ttu-id="1df11-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1df11-155">CommonParameters</span></span>
<span data-ttu-id="1df11-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1df11-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1df11-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1df11-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1df11-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1df11-158">INPUTS</span></span>

## <span data-ttu-id="1df11-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1df11-159">OUTPUTS</span></span>

### <span data-ttu-id="1df11-160">Microsoft. WindowsAzure. Commands. Utilities. TrafficManager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="1df11-160">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="1df11-161">Questo cmdlet genera un oggetto profilo di Traffic Manager, che contiene informazioni sul profilo aggiornato.</span><span class="sxs-lookup"><span data-stu-id="1df11-161">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="1df11-162">Note</span><span class="sxs-lookup"><span data-stu-id="1df11-162">NOTES</span></span>

## <span data-ttu-id="1df11-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1df11-163">RELATED LINKS</span></span>

[<span data-ttu-id="1df11-164">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1df11-164">Remove-AzureTrafficManagerEndpoint</span></span>](./Remove-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="1df11-165">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1df11-165">Set-AzureTrafficManagerEndpoint</span></span>](./Set-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="1df11-166">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1df11-166">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="1df11-167">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1df11-167">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


