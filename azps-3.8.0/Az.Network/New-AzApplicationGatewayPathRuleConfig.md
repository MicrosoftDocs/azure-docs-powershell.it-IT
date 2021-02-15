---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: f06dbac5e7c7a67acc38c5357351905fab0ed141
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402559"
---
# <span data-ttu-id="2838d-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2838d-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="2838d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2838d-102">SYNOPSIS</span></span>
<span data-ttu-id="2838d-103">Crea una regola percorso gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="2838d-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="2838d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2838d-104">SYNTAX</span></span>

### <span data-ttu-id="2838d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2838d-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2838d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2838d-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2838d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2838d-107">DESCRIPTION</span></span>
<span data-ttu-id="2838d-108">Il cmdlet **New-AzApplicationGatewayPathRuleConfig crea** una regola per il percorso del gateway di applicazione.</span><span class="sxs-lookup"><span data-stu-id="2838d-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="2838d-109">Le regole create da questo cmdlet possono essere aggiunte a una raccolta di impostazioni di configurazione della mappa del percorso URL e quindi assegnate a un gateway.</span><span class="sxs-lookup"><span data-stu-id="2838d-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="2838d-110">Le impostazioni di configurazione della mappa del percorso vengono usate nel bilanciamento del carico del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="2838d-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="2838d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2838d-111">EXAMPLES</span></span>

### <span data-ttu-id="2838d-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2838d-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="2838d-113">Questi comandi creano una nuova regola di percorso del gateway applicazione e quindi usano il cmdlet **Add-AzApplicationGatewayUrlPathMapConfig** per assegnare la regola a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="2838d-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="2838d-114">A questo scopo, il primo comando crea un riferimento a un oggetto al gateway ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="2838d-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="2838d-115">Questo riferimento all'oggetto è archiviato in una variabile denominata $Gateway.</span><span class="sxs-lookup"><span data-stu-id="2838d-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="2838d-116">I due comandi successivi creano un pool di indirizzi back-end e un oggetto impostazioni HTTP back-end; questi oggetti ( archiviati nelle variabili $AddressPool e $HttpSettings) sono necessari per creare un oggetto regola di percorso.</span><span class="sxs-lookup"><span data-stu-id="2838d-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="2838d-117">Il quarto comando crea l'oggetto regola percorso e viene archiviato in una variabile $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="2838d-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="2838d-118">Il quinto comando usa **Add-AzApplicationGatewayUrlPathMapConfig** per aggiungere le impostazioni di configurazione e la nuova regola del percorso contenuta in tali impostazioni a ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="2838d-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

### <span data-ttu-id="2838d-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2838d-119">Example 2</span></span>
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="2838d-120">Questo comando crea una regola percorso con il nome "base", i percorsi "/base", BackendAddressPool as $AddressPool, BackendHttpSettings come $HttpSettings e FirewallPolicy come $firewallPolicy.ngs e la nuova regola del percorso contenuta in queste impostazioni in ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="2838d-120">These command creates a path-rule with the Name as "base", Paths as "/base", BackendAddressPool as $AddressPool, BackendHttpSettings as $HttpSettings and FirewallPolicy as $firewallPolicy.ngs and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="2838d-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2838d-121">PARAMETERS</span></span>

### <span data-ttu-id="2838d-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2838d-122">-BackendAddressPool</span></span>
<span data-ttu-id="2838d-123">Specifica un riferimento a un oggetto a una raccolta di impostazioni del pool di indirizzi back-end da aggiungere alle impostazioni di configurazione delle regole per i percorsi del gateway.</span><span class="sxs-lookup"><span data-stu-id="2838d-123">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="2838d-124">È possibile creare questo riferimento all'oggetto usando il cmdlet New-AzApplicationGatewayBackendAddressPool e una sintassi simile alla seguente: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="2838d-124">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="2838d-125">Il comando precedente aggiunge due indirizzi IP (192.16.1.1 e 192.168.1.2) al pool di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="2838d-125">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="2838d-126">Si noti che l'indirizzo IP è racchiuso tra virgolette e separato da virgole.</span><span class="sxs-lookup"><span data-stu-id="2838d-126">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="2838d-127">La variabile risultante, $AddressPool, può essere usata come valore del parametro *DefaultBackendAddressPool.*</span><span class="sxs-lookup"><span data-stu-id="2838d-127">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="2838d-128">Il pool di indirizzi back-end rappresenta gli indirizzi IP nei server back-end.</span><span class="sxs-lookup"><span data-stu-id="2838d-128">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="2838d-129">Questi indirizzi IP devono appartenere alla subnet della rete virtuale o devono essere indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="2838d-129">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="2838d-130">Se si usa questo parametro, non è possibile usare il parametro *DefaultBackendAddressPoolId* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="2838d-130">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="2838d-131">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="2838d-131">-BackendAddressPoolId</span></span>
<span data-ttu-id="2838d-132">Specifica l'ID di un pool di indirizzi back-end esistente che è possibile aggiungere alle impostazioni di configurazione delle regole del percorso del gateway.</span><span class="sxs-lookup"><span data-stu-id="2838d-132">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="2838d-133">Gli ID pool di indirizzi possono essere restituiti usando il cmdlet Get-AzApplicationGatewayBackendAddressPool indirizzi.</span><span class="sxs-lookup"><span data-stu-id="2838d-133">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="2838d-134">Dopo aver impostato l'ID, è possibile usare il parametro *DefaultBackendAddressPoolId* invece del parametro *DefaultBackendAddressPool.*</span><span class="sxs-lookup"><span data-stu-id="2838d-134">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="2838d-135">Ad esempio: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" Il pool di indirizzi back-end rappresenta gli indirizzi IP nei server back-end.</span><span class="sxs-lookup"><span data-stu-id="2838d-135">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="2838d-136">Questi indirizzi IP devono appartenere alla subnet della rete virtuale o devono essere indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="2838d-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="2838d-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2838d-137">-BackendHttpSettings</span></span>
<span data-ttu-id="2838d-138">Specifica un riferimento a un oggetto a una raccolta di impostazioni HTTP back-end da aggiungere alle impostazioni di configurazione delle regole del percorso del gateway.</span><span class="sxs-lookup"><span data-stu-id="2838d-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="2838d-139">È possibile creare questo riferimento all'oggetto usando il cmdlet New-AzApplicationGatewayBackendHttpSettings e una sintassi simile alla seguente: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" La variabile risultante, $HttpSettings può quindi essere usato come valore del parametro *DefaultBackendAddressPool:* -DefaultBackendHttpSettings $HttpSettings Le impostazioni HTTP back-end configurano proprietà come porta, protocollo e affinità basata su cookie per un pool back-end.</span><span class="sxs-lookup"><span data-stu-id="2838d-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="2838d-140">Se si usa questo parametro, non è possibile usare il parametro *DefaultBackendHttpSettingsId* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="2838d-140">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="2838d-141">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="2838d-141">-BackendHttpSettingsId</span></span>
<span data-ttu-id="2838d-142">Specifica l'ID di una raccolta di impostazioni HTTP back-end esistente che è possibile aggiungere alle impostazioni di configurazione delle regole del percorso del gateway.</span><span class="sxs-lookup"><span data-stu-id="2838d-142">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="2838d-143">Gli ID delle impostazioni HTTP possono essere restituiti usando il cmdlet Get-AzApplicationGatewayBackendHttpSettings HTTP.</span><span class="sxs-lookup"><span data-stu-id="2838d-143">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="2838d-144">Dopo aver impostato l'ID, è possibile usare il parametro *DefaultBackendHttpSettingsId* invece del parametro *DefaultBackendHttpSettings.*</span><span class="sxs-lookup"><span data-stu-id="2838d-144">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="2838d-145">Ad esempio: -DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" Le impostazioni HTTP back-end configurano proprietà come la porta, protocollo e affinità basata su cookie per un pool back-end.</span><span class="sxs-lookup"><span data-stu-id="2838d-145">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="2838d-146">Se si usa questo parametro, non è possibile usare il parametro *DefaultBackendHttpSettings* nello stesso comando.</span><span class="sxs-lookup"><span data-stu-id="2838d-146">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="2838d-147">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="2838d-147">-FirewallPolicy</span></span>
<span data-ttu-id="2838d-148">Specifica il riferimento all'oggetto a un criterio firewall di primo livello.</span><span class="sxs-lookup"><span data-stu-id="2838d-148">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="2838d-149">Il riferimento all'oggetto può essere creato usando New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2838d-149">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="2838d-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" Un criterio firewall creato con il commandlet riportato sopra può essere indicato a livello di regola del percorso.</span><span class="sxs-lookup"><span data-stu-id="2838d-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="2838d-151">Il comando precedente crea impostazioni dei criteri predefinite e regole gestite.</span><span class="sxs-lookup"><span data-stu-id="2838d-151">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="2838d-152">Invece dei valori predefiniti, gli utenti possono specificare PolicySettings e ManagedRules usando rispettivamente New-AzApplicationGatewayFirewallPolicySettings e New-AzApplicationGatewayFirewallPolicyManagedRules predefiniti.</span><span class="sxs-lookup"><span data-stu-id="2838d-152">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2838d-153">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="2838d-153">-FirewallPolicyId</span></span>
<span data-ttu-id="2838d-154">Specifica l'ID di una risorsa firewall dell'applicazione Web di primo livello esistente.</span><span class="sxs-lookup"><span data-stu-id="2838d-154">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="2838d-155">Gli ID dei criteri del firewall possono essere restituiti usando il cmdlet Get-AzApplicationGatewayWebApplicationFirewallPolicy firewall.</span><span class="sxs-lookup"><span data-stu-id="2838d-155">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="2838d-156">Una volta fornito l'ID, è possibile usare il *parametro FirewallPolicyId* invece del *parametro FirewallPolicy.*</span><span class="sxs-lookup"><span data-stu-id="2838d-156">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="2838d-157">Ad esempio: -FirewallPolicyId "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "</span><span class="sxs-lookup"><span data-stu-id="2838d-157">For instance: -FirewallPolicyId  "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>"</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2838d-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2838d-158">-DefaultProfile</span></span>
<span data-ttu-id="2838d-159">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2838d-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2838d-160">-Name</span><span class="sxs-lookup"><span data-stu-id="2838d-160">-Name</span></span>
<span data-ttu-id="2838d-161">Specifica il nome della configurazione della regola del percorso creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2838d-161">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2838d-162">-Paths</span><span class="sxs-lookup"><span data-stu-id="2838d-162">-Paths</span></span>
<span data-ttu-id="2838d-163">Specifica una o più regole per il percorso del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="2838d-163">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="2838d-164">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2838d-164">-RedirectConfiguration</span></span>
<span data-ttu-id="2838d-165">RedirectConfiguration del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="2838d-165">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="2838d-166">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2838d-166">-RedirectConfigurationId</span></span>
<span data-ttu-id="2838d-167">ID del gateway applicazione RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2838d-167">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="2838d-168">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2838d-168">-RewriteRuleSet</span></span>
<span data-ttu-id="2838d-169">RewriteRuleSet del gateway di applicazione</span><span class="sxs-lookup"><span data-stu-id="2838d-169">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="2838d-170">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="2838d-170">-RewriteRuleSetId</span></span>
<span data-ttu-id="2838d-171">ID del gateway applicazione RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2838d-171">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="2838d-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2838d-172">CommonParameters</span></span>
<span data-ttu-id="2838d-173">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2838d-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2838d-174">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2838d-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2838d-175">INPUT</span><span class="sxs-lookup"><span data-stu-id="2838d-175">INPUTS</span></span>

### <span data-ttu-id="2838d-176">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2838d-176">None</span></span>

## <span data-ttu-id="2838d-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2838d-177">OUTPUTS</span></span>

### <span data-ttu-id="2838d-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="2838d-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="2838d-179">NOTE</span><span class="sxs-lookup"><span data-stu-id="2838d-179">NOTES</span></span>

## <span data-ttu-id="2838d-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2838d-180">RELATED LINKS</span></span>

[<span data-ttu-id="2838d-181">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2838d-181">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2838d-182">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2838d-182">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="2838d-183">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2838d-183">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2838d-184">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2838d-184">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)


[<span data-ttu-id="2838d-185">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2838d-185">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="2838d-186">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2838d-186">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2838d-187">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2838d-187">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2838d-188">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2838d-188">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


