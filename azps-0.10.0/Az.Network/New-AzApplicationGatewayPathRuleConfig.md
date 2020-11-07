---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: b6722412717d0ef087c2540ff49d3d7a5b87913c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860562"
---
# <span data-ttu-id="64dc7-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64dc7-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="64dc7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="64dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="64dc7-103">Crea una regola di percorso del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="64dc7-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="64dc7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="64dc7-104">SYNTAX</span></span>

### <span data-ttu-id="64dc7-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="64dc7-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64dc7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="64dc7-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64dc7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64dc7-107">DESCRIPTION</span></span>
<span data-ttu-id="64dc7-108">Il cmdlet **New-AzApplicationGatewayPathRuleConfig** crea una regola di percorso del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="64dc7-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="64dc7-109">Le regole create da questo cmdlet possono essere aggiunte a una raccolta di impostazioni di configurazione della mappa percorso URL e quindi assegnate a un gateway.</span><span class="sxs-lookup"><span data-stu-id="64dc7-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>

<span data-ttu-id="64dc7-110">Le impostazioni di configurazione della mappa percorso vengono usate in bilanciamento del carico del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="64dc7-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="64dc7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="64dc7-111">EXAMPLES</span></span>

### <span data-ttu-id="64dc7-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="64dc7-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSetting -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="64dc7-113">Questi comandi creano una nuova regola di percorso del gateway applicazione e quindi usano il cmdlet **Add-AzApplicationGatewayUrlPathMapConfig** per assegnare la regola a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="64dc7-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="64dc7-114">A questo scopo, il primo comando crea un riferimento a un oggetto al gateway ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="64dc7-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="64dc7-115">Questo riferimento oggetto è archiviato in una variabile denominata $Gateway.</span><span class="sxs-lookup"><span data-stu-id="64dc7-115">This object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="64dc7-116">I due comandi successivi creano un pool di indirizzi back-end e un oggetto impostazioni HTTP back-end; questi oggetti (archiviati nelle variabili $AddressPool e $HttpSettings) sono necessari per creare un oggetto regola di percorso.</span><span class="sxs-lookup"><span data-stu-id="64dc7-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>

<span data-ttu-id="64dc7-117">Il quarto comando crea l'oggetto della regola di percorso e viene archiviato in una variabile denominata $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="64dc7-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>

<span data-ttu-id="64dc7-118">Il quinto comando USA **Add-AzApplicationGatewayUrlPathMapConfig** per aggiungere le impostazioni di configurazione e la nuova regola di percorso contenuta in tali impostazioni in ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="64dc7-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="64dc7-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="64dc7-119">PARAMETERS</span></span>

### <span data-ttu-id="64dc7-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="64dc7-120">-BackendAddressPool</span></span>
<span data-ttu-id="64dc7-121">Specifica un riferimento a un oggetto a una raccolta di impostazioni del pool di indirizzi di backend da aggiungere alle impostazioni di configurazione delle regole del percorso gateway.</span><span class="sxs-lookup"><span data-stu-id="64dc7-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="64dc7-122">Puoi creare questo riferimento di oggetto usando il cmdlet New-AzApplicationGatewayBackendAddressPool e la sintassi simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="64dc7-122">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this:</span></span>

`$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`

<span data-ttu-id="64dc7-123">Il comando precedente aggiunge due indirizzi IP (192.16.1.1 e 192.168.1.2) al pool di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="64dc7-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="64dc7-124">Tieni presente che l'indirizzo IP è racchiuso tra virgolette e separato tramite virgole.</span><span class="sxs-lookup"><span data-stu-id="64dc7-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>

<span data-ttu-id="64dc7-125">La variabile risultante, $AddressPool, può quindi essere usata come valore di parametro per il parametro *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="64dc7-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>

<span data-ttu-id="64dc7-126">Il pool di indirizzi di backend rappresenta gli indirizzi IP nei server back-end.</span><span class="sxs-lookup"><span data-stu-id="64dc7-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="64dc7-127">Questi indirizzi IP dovrebbero appartenere alla subnet della rete virtuale o devono essere indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="64dc7-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="64dc7-128">Se si usa questo parametro, non è possibile usare il parametro *DefaultBackendAddressPoolId* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="64dc7-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64dc7-129">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="64dc7-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="64dc7-130">Specifica l'ID di un pool di indirizzi di backend esistente che può essere aggiunto alle impostazioni di configurazione della regola del percorso gateway.</span><span class="sxs-lookup"><span data-stu-id="64dc7-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="64dc7-131">Gli ID del pool di indirizzi possono essere restituiti tramite il cmdlet Get-AzApplicationGatewayBackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="64dc7-131">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="64dc7-132">Dopo aver ottenuto l'ID, puoi usare il parametro *DefaultBackendAddressPoolId* invece del parametro *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="64dc7-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="64dc7-133">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="64dc7-133">For instance:</span></span>

<span data-ttu-id="64dc7-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span><span class="sxs-lookup"><span data-stu-id="64dc7-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span></span>

<span data-ttu-id="64dc7-135">Il pool di indirizzi di backend rappresenta gli indirizzi IP nei server back-end.</span><span class="sxs-lookup"><span data-stu-id="64dc7-135">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="64dc7-136">Questi indirizzi IP dovrebbero appartenere alla subnet della rete virtuale o devono essere indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="64dc7-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64dc7-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="64dc7-137">-BackendHttpSettings</span></span>
<span data-ttu-id="64dc7-138">Specifica un riferimento a un oggetto a una raccolta di impostazioni HTTP di backend da aggiungere alle impostazioni di configurazione della regola del percorso del gateway.</span><span class="sxs-lookup"><span data-stu-id="64dc7-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="64dc7-139">Puoi creare questo riferimento di oggetto usando il cmdlet New-AzApplicationGatewayBackendHttpSetting e la sintassi simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="64dc7-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSetting cmdlet and syntax similar to this:</span></span>

<span data-ttu-id="64dc7-140">$HttpSettings = New-AzApplicationGatewayBackendHttpSetting-nome "ContosoHttpSetings"-porta 80-protocollo "http"-CookieBasedAffinity "disabilitato"</span><span class="sxs-lookup"><span data-stu-id="64dc7-140">$HttpSettings = New-AzApplicationGatewayBackendHttpSetting -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"</span></span>

<span data-ttu-id="64dc7-141">La variabile risultante, $HttpSettings, può quindi essere usata come valore di parametro per il parametro *DefaultBackendAddressPool* :</span><span class="sxs-lookup"><span data-stu-id="64dc7-141">The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter:</span></span>

<span data-ttu-id="64dc7-142">-DefaultBackendHttpSettings $HttpSettings</span><span class="sxs-lookup"><span data-stu-id="64dc7-142">-DefaultBackendHttpSettings $HttpSettings</span></span>

<span data-ttu-id="64dc7-143">Le impostazioni HTTP di backend configurano proprietà come la porta, il protocollo e l'affinità basata su cookie per un pool back-end.</span><span class="sxs-lookup"><span data-stu-id="64dc7-143">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="64dc7-144">Se si usa questo parametro, non è possibile usare il parametro *DefaultBackendHttpSettingsId* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="64dc7-144">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64dc7-145">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="64dc7-145">-BackendHttpSettingsId</span></span>
<span data-ttu-id="64dc7-146">Specifica l'ID di una raccolta di impostazioni HTTP di backend esistente che può essere aggiunta alle impostazioni di configurazione della regola del percorso del gateway.</span><span class="sxs-lookup"><span data-stu-id="64dc7-146">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="64dc7-147">Gli ID delle impostazioni HTTP possono essere restituiti usando il cmdlet Get-AzApplicationGatewayBackendHttpSetting.</span><span class="sxs-lookup"><span data-stu-id="64dc7-147">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSetting cmdlet.</span></span>
<span data-ttu-id="64dc7-148">Dopo aver ottenuto l'ID, puoi usare il parametro *DefaultBackendHttpSettingsId* invece del parametro *DefaultBackendHttpSettings* .</span><span class="sxs-lookup"><span data-stu-id="64dc7-148">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="64dc7-149">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="64dc7-149">For instance:</span></span>

<span data-ttu-id="64dc7-150">-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span><span class="sxs-lookup"><span data-stu-id="64dc7-150">-DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span></span>

<span data-ttu-id="64dc7-151">Le impostazioni HTTP di backend configurano proprietà come la porta, il protocollo e l'affinità basata su cookie per un pool back-end.</span><span class="sxs-lookup"><span data-stu-id="64dc7-151">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="64dc7-152">Se si usa questo parametro, non è possibile usare il parametro *DefaultBackendHttpSettings* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="64dc7-152">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64dc7-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64dc7-153">-DefaultProfile</span></span>
<span data-ttu-id="64dc7-154">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="64dc7-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64dc7-155">-Nome</span><span class="sxs-lookup"><span data-stu-id="64dc7-155">-Name</span></span>
<span data-ttu-id="64dc7-156">Specifica il nome della configurazione della regola di percorso creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64dc7-156">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="64dc7-157">-Percorsi</span><span class="sxs-lookup"><span data-stu-id="64dc7-157">-Paths</span></span>
<span data-ttu-id="64dc7-158">Specifica una o più regole di percorso del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="64dc7-158">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="64dc7-159">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="64dc7-159">-RedirectConfiguration</span></span>
<span data-ttu-id="64dc7-160">App gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="64dc7-160">Application gateway RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64dc7-161">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="64dc7-161">-RedirectConfigurationId</span></span>
<span data-ttu-id="64dc7-162">ID dell'applicazione gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="64dc7-162">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64dc7-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64dc7-163">CommonParameters</span></span>
<span data-ttu-id="64dc7-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64dc7-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64dc7-165">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64dc7-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64dc7-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="64dc7-166">INPUTS</span></span>

###  
<span data-ttu-id="64dc7-167">**New-AzApplicationGatewayPathRuleConfig** non accetta l'input da pipeline.</span><span class="sxs-lookup"><span data-stu-id="64dc7-167">**New-AzApplicationGatewayPathRuleConfig** does not accept pipelined input.</span></span>

## <span data-ttu-id="64dc7-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="64dc7-168">OUTPUTS</span></span>

###  
<span data-ttu-id="64dc7-169">**New-AzApplicationGatewayPathRuleConfig** crea nuove istanze dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPathRule** .</span><span class="sxs-lookup"><span data-stu-id="64dc7-169">**New-AzApplicationGatewayPathRuleConfig** creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule** object.</span></span>

## <span data-ttu-id="64dc7-170">Note</span><span class="sxs-lookup"><span data-stu-id="64dc7-170">NOTES</span></span>

## <span data-ttu-id="64dc7-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="64dc7-171">RELATED LINKS</span></span>

[<span data-ttu-id="64dc7-172">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="64dc7-172">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="64dc7-173">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="64dc7-173">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="64dc7-174">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="64dc7-174">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="64dc7-175">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="64dc7-175">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="64dc7-176">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="64dc7-176">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="64dc7-177">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64dc7-177">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="64dc7-178">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="64dc7-178">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="64dc7-179">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="64dc7-179">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="64dc7-180">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="64dc7-180">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


