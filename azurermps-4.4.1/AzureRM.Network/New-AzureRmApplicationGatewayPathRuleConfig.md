---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: bcb712e7bfe0cd619d63378cad89402828eb6d36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520496"
---
# <span data-ttu-id="bd10f-101">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bd10f-101">New-AzureRmApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="bd10f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bd10f-102">SYNOPSIS</span></span>
<span data-ttu-id="bd10f-103">Crea una regola di percorso del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="bd10f-103">Creates an application gateway path rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd10f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd10f-104">SYNTAX</span></span>

### <span data-ttu-id="bd10f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bd10f-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd10f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bd10f-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd10f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd10f-107">DESCRIPTION</span></span>
<span data-ttu-id="bd10f-108">Il cmdlet **New-AzureRmApplicationGatewayPathRuleConfig** crea una regola di percorso del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bd10f-108">The **New-AzureRmApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="bd10f-109">Le regole create da questo cmdlet possono essere aggiunte a una raccolta di impostazioni di configurazione della mappa percorso URL e quindi assegnate a un gateway.</span><span class="sxs-lookup"><span data-stu-id="bd10f-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>

<span data-ttu-id="bd10f-110">Le impostazioni di configurazione della mappa percorso vengono usate in bilanciamento del carico del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="bd10f-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="bd10f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd10f-111">EXAMPLES</span></span>

### <span data-ttu-id="bd10f-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bd10f-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzureRmApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzureRmApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="bd10f-113">Questi comandi creano una nuova regola di percorso del gateway applicazione e quindi usano il cmdlet **Add-AzureRmApplicationGatewayUrlPathMapConfig** per assegnare la regola a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bd10f-113">These commands create a new application gateway path rule and then use the **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="bd10f-114">A questo scopo, il primo comando crea un riferimento a un oggetto al gateway ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="bd10f-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="bd10f-115">Questo riferimento oggetto è archiviato in una variabile denominata $Gateway.</span><span class="sxs-lookup"><span data-stu-id="bd10f-115">This object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="bd10f-116">I due comandi successivi creano un pool di indirizzi back-end e un oggetto impostazioni HTTP back-end; questi oggetti (archiviati nelle variabili $AddressPool e $HttpSettings) sono necessari per creare un oggetto regola di percorso.</span><span class="sxs-lookup"><span data-stu-id="bd10f-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>

<span data-ttu-id="bd10f-117">Il quarto comando crea l'oggetto della regola di percorso e viene archiviato in una variabile denominata $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="bd10f-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>

<span data-ttu-id="bd10f-118">Il quinto comando USA **Add-AzureRmApplicationGatewayUrlPathMapConfig** per aggiungere le impostazioni di configurazione e la nuova regola di percorso contenuta in tali impostazioni in ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="bd10f-118">The fifth command uses **Add-AzureRmApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="bd10f-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bd10f-119">PARAMETERS</span></span>

### <span data-ttu-id="bd10f-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bd10f-120">-BackendAddressPool</span></span>
<span data-ttu-id="bd10f-121">Specifica un riferimento a un oggetto a una raccolta di impostazioni del pool di indirizzi di backend da aggiungere alle impostazioni di configurazione delle regole del percorso gateway.</span><span class="sxs-lookup"><span data-stu-id="bd10f-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="bd10f-122">Puoi creare questo riferimento di oggetto usando il cmdlet New-AzureRmApplicationGatewayBackendAddressPool e la sintassi simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="bd10f-122">You can create this object reference by using the New-AzureRmApplicationGatewayBackendAddressPool cmdlet and syntax similar to this:</span></span>

`$AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`

<span data-ttu-id="bd10f-123">Il comando precedente aggiunge due indirizzi IP (192.16.1.1 e 192.168.1.2) al pool di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="bd10f-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="bd10f-124">Tieni presente che l'indirizzo IP è racchiuso tra virgolette e separato tramite virgole.</span><span class="sxs-lookup"><span data-stu-id="bd10f-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>

<span data-ttu-id="bd10f-125">La variabile risultante, $AddressPool, può quindi essere usata come valore di parametro per il parametro *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="bd10f-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>

<span data-ttu-id="bd10f-126">Il pool di indirizzi di backend rappresenta gli indirizzi IP nei server back-end.</span><span class="sxs-lookup"><span data-stu-id="bd10f-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="bd10f-127">Questi indirizzi IP dovrebbero appartenere alla subnet della rete virtuale o devono essere indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="bd10f-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="bd10f-128">Se si usa questo parametro, non è possibile usare il parametro *DefaultBackendAddressPoolId* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="bd10f-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd10f-129">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="bd10f-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="bd10f-130">Specifica l'ID di un pool di indirizzi di backend esistente che può essere aggiunto alle impostazioni di configurazione della regola del percorso gateway.</span><span class="sxs-lookup"><span data-stu-id="bd10f-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="bd10f-131">Gli ID del pool di indirizzi possono essere restituiti tramite il cmdlet Get-AzureRmApplicationGatewayBackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="bd10f-131">Address pool IDs can be returned by using the Get-AzureRmApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="bd10f-132">Dopo aver ottenuto l'ID, puoi usare il parametro *DefaultBackendAddressPoolId* invece del parametro *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="bd10f-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="bd10f-133">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="bd10f-133">For instance:</span></span>

<span data-ttu-id="bd10f-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span><span class="sxs-lookup"><span data-stu-id="bd10f-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span></span>

<span data-ttu-id="bd10f-135">Il pool di indirizzi di backend rappresenta gli indirizzi IP nei server back-end.</span><span class="sxs-lookup"><span data-stu-id="bd10f-135">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="bd10f-136">Questi indirizzi IP dovrebbero appartenere alla subnet della rete virtuale o devono essere indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="bd10f-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd10f-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="bd10f-137">-BackendHttpSettings</span></span>
<span data-ttu-id="bd10f-138">Specifica un riferimento a un oggetto a una raccolta di impostazioni HTTP di backend da aggiungere alle impostazioni di configurazione della regola del percorso del gateway.</span><span class="sxs-lookup"><span data-stu-id="bd10f-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="bd10f-139">Puoi creare questo riferimento di oggetto usando il cmdlet New-AzureRmApplicationGatewayBackendHttpSettings e la sintassi simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="bd10f-139">You can create this object reference by using the New-AzureRmApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this:</span></span>

<span data-ttu-id="bd10f-140">$HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings-nome "ContosoHttpSetings"-porta 80-protocollo "http"-CookieBasedAffinity "disabilitato"</span><span class="sxs-lookup"><span data-stu-id="bd10f-140">$HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"</span></span>

<span data-ttu-id="bd10f-141">La variabile risultante, $HttpSettings, può quindi essere usata come valore di parametro per il parametro *DefaultBackendAddressPool* :</span><span class="sxs-lookup"><span data-stu-id="bd10f-141">The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter:</span></span>

<span data-ttu-id="bd10f-142">-DefaultBackendHttpSettings $HttpSettings</span><span class="sxs-lookup"><span data-stu-id="bd10f-142">-DefaultBackendHttpSettings $HttpSettings</span></span>

<span data-ttu-id="bd10f-143">Le impostazioni HTTP di backend configurano proprietà come la porta, il protocollo e l'affinità basata su cookie per un pool back-end.</span><span class="sxs-lookup"><span data-stu-id="bd10f-143">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="bd10f-144">Se si usa questo parametro, non è possibile usare il parametro *DefaultBackendHttpSettingsId* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="bd10f-144">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd10f-145">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="bd10f-145">-BackendHttpSettingsId</span></span>
<span data-ttu-id="bd10f-146">Specifica l'ID di una raccolta di impostazioni HTTP di backend esistente che può essere aggiunta alle impostazioni di configurazione della regola del percorso del gateway.</span><span class="sxs-lookup"><span data-stu-id="bd10f-146">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="bd10f-147">Gli ID delle impostazioni HTTP possono essere restituiti usando il cmdlet Get-AzureRmApplicationGatewayBackendHttpSettings.</span><span class="sxs-lookup"><span data-stu-id="bd10f-147">HTTP setting IDs can be returned by using the Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="bd10f-148">Dopo aver ottenuto l'ID, puoi usare il parametro *DefaultBackendHttpSettingsId* invece del parametro *DefaultBackendHttpSettings* .</span><span class="sxs-lookup"><span data-stu-id="bd10f-148">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="bd10f-149">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="bd10f-149">For instance:</span></span>

<span data-ttu-id="bd10f-150">-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span><span class="sxs-lookup"><span data-stu-id="bd10f-150">-DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span></span>

<span data-ttu-id="bd10f-151">Le impostazioni HTTP di backend configurano proprietà come la porta, il protocollo e l'affinità basata su cookie per un pool back-end.</span><span class="sxs-lookup"><span data-stu-id="bd10f-151">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="bd10f-152">Se si usa questo parametro, non è possibile usare il parametro *DefaultBackendHttpSettings* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="bd10f-152">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd10f-153">-Nome</span><span class="sxs-lookup"><span data-stu-id="bd10f-153">-Name</span></span>
<span data-ttu-id="bd10f-154">Specifica il nome della configurazione della regola di percorso creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd10f-154">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="bd10f-155">-Percorsi</span><span class="sxs-lookup"><span data-stu-id="bd10f-155">-Paths</span></span>
<span data-ttu-id="bd10f-156">Specifica una o più regole di percorso del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="bd10f-156">Specifies one or more application gateway path rules.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd10f-157">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd10f-157">-RedirectConfiguration</span></span>
<span data-ttu-id="bd10f-158">App gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd10f-158">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd10f-159">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="bd10f-159">-RedirectConfigurationId</span></span>
<span data-ttu-id="bd10f-160">ID dell'applicazione gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd10f-160">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd10f-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd10f-161">-DefaultProfile</span></span>
<span data-ttu-id="bd10f-162">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bd10f-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd10f-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd10f-163">CommonParameters</span></span>
<span data-ttu-id="bd10f-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd10f-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd10f-165">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd10f-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd10f-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bd10f-166">INPUTS</span></span>

###  
<span data-ttu-id="bd10f-167">**New-AzureRmApplicationGatewayPathRuleConfig** non accetta l'input da pipeline.</span><span class="sxs-lookup"><span data-stu-id="bd10f-167">**New-AzureRmApplicationGatewayPathRuleConfig** does not accept pipelined input.</span></span>

## <span data-ttu-id="bd10f-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd10f-168">OUTPUTS</span></span>

###  
<span data-ttu-id="bd10f-169">**New-AzureRmApplicationGatewayPathRuleConfig** crea nuove istanze dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPathRule** .</span><span class="sxs-lookup"><span data-stu-id="bd10f-169">**New-AzureRmApplicationGatewayPathRuleConfig** creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule** object.</span></span>

## <span data-ttu-id="bd10f-170">Note</span><span class="sxs-lookup"><span data-stu-id="bd10f-170">NOTES</span></span>

## <span data-ttu-id="bd10f-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd10f-171">RELATED LINKS</span></span>

[<span data-ttu-id="bd10f-172">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="bd10f-172">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="bd10f-173">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bd10f-173">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="bd10f-174">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="bd10f-174">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="bd10f-175">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bd10f-175">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="bd10f-176">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="bd10f-176">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="bd10f-177">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bd10f-177">New-AzureRmApplicationGatewayPathRuleConfig</span></span>](./New-AzureRmApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="bd10f-178">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="bd10f-178">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="bd10f-179">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="bd10f-179">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="bd10f-180">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="bd10f-180">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


