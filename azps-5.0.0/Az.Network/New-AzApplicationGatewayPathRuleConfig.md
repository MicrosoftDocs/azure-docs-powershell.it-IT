---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: c36cb832034535f13cbcb49805531c64ee906c60
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203136"
---
# <span data-ttu-id="4e958-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4e958-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="4e958-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e958-102">SYNOPSIS</span></span>
<span data-ttu-id="4e958-103">Crea una regola di percorso del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="4e958-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="4e958-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e958-104">SYNTAX</span></span>

### <span data-ttu-id="4e958-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4e958-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e958-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4e958-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e958-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e958-107">DESCRIPTION</span></span>
<span data-ttu-id="4e958-108">Il cmdlet **New-AzApplicationGatewayPathRuleConfig** crea una regola di percorso del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4e958-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="4e958-109">Le regole create da questo cmdlet possono essere aggiunte a una raccolta di impostazioni di configurazione della mappa percorso URL e quindi assegnate a un gateway.</span><span class="sxs-lookup"><span data-stu-id="4e958-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="4e958-110">Le impostazioni di configurazione della mappa percorso vengono usate in bilanciamento del carico del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="4e958-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="4e958-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e958-111">EXAMPLES</span></span>

### <span data-ttu-id="4e958-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4e958-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="4e958-113">Questi comandi creano una nuova regola di percorso del gateway applicazione e quindi usano il cmdlet **Add-AzApplicationGatewayUrlPathMapConfig** per assegnare la regola a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4e958-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="4e958-114">A questo scopo, il primo comando crea un riferimento a un oggetto al gateway ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="4e958-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="4e958-115">Questo riferimento oggetto è archiviato in una variabile denominata $Gateway.</span><span class="sxs-lookup"><span data-stu-id="4e958-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="4e958-116">I due comandi successivi creano un pool di indirizzi back-end e un oggetto impostazioni HTTP back-end; questi oggetti (archiviati nelle variabili $AddressPool e $HttpSettings) sono necessari per creare un oggetto regola di percorso.</span><span class="sxs-lookup"><span data-stu-id="4e958-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="4e958-117">Il quarto comando crea l'oggetto della regola di percorso e viene archiviato in una variabile denominata $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="4e958-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="4e958-118">Il quinto comando USA **Add-AzApplicationGatewayUrlPathMapConfig** per aggiungere le impostazioni di configurazione e la nuova regola di percorso contenuta in tali impostazioni in ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="4e958-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

### <span data-ttu-id="4e958-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4e958-119">Example 2</span></span>
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="4e958-120">Questo comando crea una regola di percorso con il nome "base", Paths come "/base", BackendAddressPool come $AddressPool, BackendHttpSettings come $HttpSettings e FirewallPolicy come $firewallPolicy. NGS e la nuova regola di percorso contenuta in tali impostazioni in ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="4e958-120">These command creates a path-rule with the Name as "base", Paths as "/base", BackendAddressPool as $AddressPool, BackendHttpSettings as $HttpSettings and FirewallPolicy as $firewallPolicy.ngs and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="4e958-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e958-121">PARAMETERS</span></span>

### <span data-ttu-id="4e958-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4e958-122">-BackendAddressPool</span></span>
<span data-ttu-id="4e958-123">Specifica un riferimento a un oggetto a una raccolta di impostazioni del pool di indirizzi di backend da aggiungere alle impostazioni di configurazione delle regole del percorso gateway.</span><span class="sxs-lookup"><span data-stu-id="4e958-123">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="4e958-124">Puoi creare questo riferimento di oggetto usando il cmdlet New-AzApplicationGatewayBackendAddressPool e la sintassi simile alla seguente: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="4e958-124">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="4e958-125">Il comando precedente aggiunge due indirizzi IP (192.16.1.1 e 192.168.1.2) al pool di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="4e958-125">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="4e958-126">Tieni presente che l'indirizzo IP è racchiuso tra virgolette e separato tramite virgole.</span><span class="sxs-lookup"><span data-stu-id="4e958-126">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="4e958-127">La variabile risultante, $AddressPool, può quindi essere usata come valore di parametro per il parametro *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="4e958-127">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="4e958-128">Il pool di indirizzi di backend rappresenta gli indirizzi IP nei server back-end.</span><span class="sxs-lookup"><span data-stu-id="4e958-128">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="4e958-129">Questi indirizzi IP dovrebbero appartenere alla subnet della rete virtuale o devono essere indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="4e958-129">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="4e958-130">Se si usa questo parametro, non è possibile usare il parametro *DefaultBackendAddressPoolId* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="4e958-130">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="4e958-131">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="4e958-131">-BackendAddressPoolId</span></span>
<span data-ttu-id="4e958-132">Specifica l'ID di un pool di indirizzi di backend esistente che può essere aggiunto alle impostazioni di configurazione della regola del percorso gateway.</span><span class="sxs-lookup"><span data-stu-id="4e958-132">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="4e958-133">Gli ID del pool di indirizzi possono essere restituiti tramite il cmdlet Get-AzApplicationGatewayBackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="4e958-133">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="4e958-134">Dopo aver ottenuto l'ID, puoi usare il parametro *DefaultBackendAddressPoolId* invece del parametro *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="4e958-134">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="4e958-135">Ad esempio:-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" il pool di indirizzi back-end rappresenta gli indirizzi IP nei server back-end.</span><span class="sxs-lookup"><span data-stu-id="4e958-135">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="4e958-136">Questi indirizzi IP dovrebbero appartenere alla subnet della rete virtuale o devono essere indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="4e958-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="4e958-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4e958-137">-BackendHttpSettings</span></span>
<span data-ttu-id="4e958-138">Specifica un riferimento a un oggetto a una raccolta di impostazioni HTTP di backend da aggiungere alle impostazioni di configurazione della regola del percorso del gateway.</span><span class="sxs-lookup"><span data-stu-id="4e958-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="4e958-139">Puoi creare questo riferimento di oggetto usando il cmdlet New-AzApplicationGatewayBackendHttpSettings e la sintassi simile alla seguente: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings-Name "ContosoHttpSettings"-Port 80-Protocol "http"-CookieBasedAffinity "disabled" la variabile risultante, $HttpSettings, può quindi essere usata come valore di parametro per il parametro *DefaultBackendAddressPool* :-DefaultBackendHttpSettings $HttpSettings le impostazioni http di backend consentono di configurare proprietà come la porta, il protocollo e l'affinità basata su cookie per un pool di back-end.</span><span class="sxs-lookup"><span data-stu-id="4e958-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="4e958-140">Se si usa questo parametro, non è possibile usare il parametro *DefaultBackendHttpSettingsId* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="4e958-140">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="4e958-141">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="4e958-141">-BackendHttpSettingsId</span></span>
<span data-ttu-id="4e958-142">Specifica l'ID di una raccolta di impostazioni HTTP di backend esistente che può essere aggiunta alle impostazioni di configurazione della regola del percorso del gateway.</span><span class="sxs-lookup"><span data-stu-id="4e958-142">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="4e958-143">Gli ID delle impostazioni HTTP possono essere restituiti usando il cmdlet Get-AzApplicationGatewayBackendHttpSettings.</span><span class="sxs-lookup"><span data-stu-id="4e958-143">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="4e958-144">Dopo aver ottenuto l'ID, puoi usare il parametro *DefaultBackendHttpSettingsId* invece del parametro *DefaultBackendHttpSettings* .</span><span class="sxs-lookup"><span data-stu-id="4e958-144">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="4e958-145">Ad esempio:-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" le impostazioni HTTP di backend configurano proprietà come la porta, il protocollo e l'affinità basata su cookie per un pool di backend.</span><span class="sxs-lookup"><span data-stu-id="4e958-145">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="4e958-146">Se si usa questo parametro, non è possibile usare il parametro *DefaultBackendHttpSettings* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="4e958-146">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="4e958-147">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="4e958-147">-FirewallPolicy</span></span>
<span data-ttu-id="4e958-148">Specifica il riferimento all'oggetto a un criterio firewall di primo livello.</span><span class="sxs-lookup"><span data-stu-id="4e958-148">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="4e958-149">Il riferimento all'oggetto può essere creato usando il cmdlet New-AzApplicationGatewayWebApplicationFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="4e958-149">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="4e958-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy-Name "wafPolicy1"-ResourceGroup "rgName" un criterio firewall creato usando il unifiedgroup precedente può essere riferito a un livello di regola di percorso.</span><span class="sxs-lookup"><span data-stu-id="4e958-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="4e958-151">sopra il comando creerebbe le impostazioni dei criteri e le regole gestite predefinite.</span><span class="sxs-lookup"><span data-stu-id="4e958-151">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="4e958-152">Invece dei valori predefiniti, gli utenti possono specificare PolicySettings, ManagedRules usando New-AzApplicationGatewayFirewallPolicySettings e New-AzApplicationGatewayFirewallPolicyManagedRules rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="4e958-152">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e958-153">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="4e958-153">-FirewallPolicyId</span></span>
<span data-ttu-id="4e958-154">Specifica l'ID di una risorsa di firewall applicazione Web di primo livello esistente.</span><span class="sxs-lookup"><span data-stu-id="4e958-154">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="4e958-155">Gli ID dei criteri del firewall possono essere restituiti tramite il cmdlet Get-AzApplicationGatewayWebApplicationFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="4e958-155">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="4e958-156">Dopo aver ottenuto l'ID, puoi usare il parametro *FirewallPolicyId* invece del parametro *firewallpolicy* .</span><span class="sxs-lookup"><span data-stu-id="4e958-156">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="4e958-157">Ad esempio:-FirewallPolicyId "/subscriptions/<Subscription-ID>/resourceGroups/<Resource-Group-ID>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "</span><span class="sxs-lookup"><span data-stu-id="4e958-157">For instance: -FirewallPolicyId  "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>"</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e958-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e958-158">-DefaultProfile</span></span>
<span data-ttu-id="4e958-159">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e958-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e958-160">-Nome</span><span class="sxs-lookup"><span data-stu-id="4e958-160">-Name</span></span>
<span data-ttu-id="4e958-161">Specifica il nome della configurazione della regola di percorso creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e958-161">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4e958-162">-Percorsi</span><span class="sxs-lookup"><span data-stu-id="4e958-162">-Paths</span></span>
<span data-ttu-id="4e958-163">Specifica una o più regole di percorso del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="4e958-163">Specifies one or more application gateway path rules.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e958-164">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e958-164">-RedirectConfiguration</span></span>
<span data-ttu-id="4e958-165">App gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e958-165">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="4e958-166">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4e958-166">-RedirectConfigurationId</span></span>
<span data-ttu-id="4e958-167">ID dell'applicazione gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e958-167">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="4e958-168">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4e958-168">-RewriteRuleSet</span></span>
<span data-ttu-id="4e958-169">App gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4e958-169">Application gateway RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e958-170">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="4e958-170">-RewriteRuleSetId</span></span>
<span data-ttu-id="4e958-171">ID dell'applicazione gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4e958-171">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="4e958-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e958-172">CommonParameters</span></span>
<span data-ttu-id="4e958-173">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e958-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e958-174">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e958-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e958-175">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e958-175">INPUTS</span></span>

### <span data-ttu-id="4e958-176">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4e958-176">None</span></span>

## <span data-ttu-id="4e958-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e958-177">OUTPUTS</span></span>

### <span data-ttu-id="4e958-178">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="4e958-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="4e958-179">Note</span><span class="sxs-lookup"><span data-stu-id="4e958-179">NOTES</span></span>

## <span data-ttu-id="4e958-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e958-180">RELATED LINKS</span></span>

[<span data-ttu-id="4e958-181">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4e958-181">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4e958-182">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4e958-182">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="4e958-183">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4e958-183">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4e958-184">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4e958-184">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4e958-185">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="4e958-185">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="4e958-186">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4e958-186">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="4e958-187">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4e958-187">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4e958-188">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4e958-188">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4e958-189">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4e958-189">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


