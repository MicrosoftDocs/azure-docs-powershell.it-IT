---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 1399dba141cb885e0ad184a588707e7c4f4efe7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997245"
---
# <span data-ttu-id="f552f-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f552f-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f552f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f552f-102">SYNOPSIS</span></span>
<span data-ttu-id="f552f-103">Crea un listener HTTP per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="f552f-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="f552f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f552f-104">SYNTAX</span></span>

### <span data-ttu-id="f552f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f552f-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-FirewallPolicyId <String>] [-SslProfileId <String>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f552f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f552f-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f552f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f552f-107">DESCRIPTION</span></span>
<span data-ttu-id="f552f-108">Il cmdlet **New-AzApplicationGatewayHttpHttpHttp Listener crea** un listener HTTP per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f552f-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="f552f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f552f-109">EXAMPLES</span></span>

### <span data-ttu-id="f552f-110">Esempio 1: Creare un listener HTTP</span><span class="sxs-lookup"><span data-stu-id="f552f-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="f552f-111">Questo comando crea un listener HTTP denominato Listener01 e archivia il risultato nella variabile $Listener.</span><span class="sxs-lookup"><span data-stu-id="f552f-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="f552f-112">Esempio 2: Creare un listener HTTP con SSL</span><span class="sxs-lookup"><span data-stu-id="f552f-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="f552f-113">Questo comando crea un listener HTTP che usa l'offload SSL e fornisce il certificato SSL nella variabile $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="f552f-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="f552f-114">Il comando archivia il risultato nella variabile denominata $Listener.</span><span class="sxs-lookup"><span data-stu-id="f552f-114">The command stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="f552f-115">Esempio 3: Creare un listener HTTP con criteri firewall</span><span class="sxs-lookup"><span data-stu-id="f552f-115">Example 3: Create an HTTP listener with firewall-policy</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="f552f-116">Questo comando crea un listener HTTP denominato Listener01, FirewallPolicy $firewallPolicy e archivia il risultato nella variabile $Listener.</span><span class="sxs-lookup"><span data-stu-id="f552f-116">This command creates an HTTP listener named Listener01, FirewallPolicy as $firewallPolicy and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="f552f-117">Esempio 4: Aggiungere un listener HTTPS con SSL e HostNames</span><span class="sxs-lookup"><span data-stu-id="f552f-117">Example 4: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="f552f-118">Questo comando crea un listener HTTP che usa l'offload SSL e fornisce il certificato SSL nella variabile $SSLCert 01 insieme a due HostNames.</span><span class="sxs-lookup"><span data-stu-id="f552f-118">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable along with two HostNames.</span></span>
<span data-ttu-id="f552f-119">Il comando archivia il risultato nella variabile denominata $Listener.</span><span class="sxs-lookup"><span data-stu-id="f552f-119">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="f552f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f552f-120">PARAMETERS</span></span>

### <span data-ttu-id="f552f-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="f552f-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="f552f-122">Errore del cliente di un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="f552f-122">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f552f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f552f-123">-DefaultProfile</span></span>
<span data-ttu-id="f552f-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f552f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f552f-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f552f-125">-FirewallPolicy</span></span>
<span data-ttu-id="f552f-126">Specifica il riferimento all'oggetto a un criterio firewall di primo livello.</span><span class="sxs-lookup"><span data-stu-id="f552f-126">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="f552f-127">Il riferimento all'oggetto può essere creato usando New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f552f-127">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="f552f-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" Un criterio firewall creato con il commandlet riportato sopra può essere indicato a livello di regola del percorso.</span><span class="sxs-lookup"><span data-stu-id="f552f-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="f552f-129">Il comando precedente crea impostazioni dei criteri predefinite e regole gestite.</span><span class="sxs-lookup"><span data-stu-id="f552f-129">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="f552f-130">Invece dei valori predefiniti, gli utenti possono specificare PolicySettings e ManagedRules usando rispettivamente New-AzApplicationGatewayFirewallPolicySettings e New-AzApplicationGatewayFirewallPolicyManagedRules predefiniti.</span><span class="sxs-lookup"><span data-stu-id="f552f-130">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f552f-131">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="f552f-131">-FirewallPolicyId</span></span>
<span data-ttu-id="f552f-132">Specifica l'ID di una risorsa firewall dell'applicazione Web di primo livello esistente.</span><span class="sxs-lookup"><span data-stu-id="f552f-132">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="f552f-133">Gli ID dei criteri del firewall possono essere restituiti usando il cmdlet Get-AzApplicationGatewayWebApplicationFirewallPolicy firewall.</span><span class="sxs-lookup"><span data-stu-id="f552f-133">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="f552f-134">Una volta fornito l'ID, è possibile usare il *parametro FirewallPolicyId* invece del *parametro FirewallPolicy.*</span><span class="sxs-lookup"><span data-stu-id="f552f-134">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="f552f-135">Ad esempio: -FirewallPolicyId /subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName></span><span class="sxs-lookup"><span data-stu-id="f552f-135">For instance: -FirewallPolicyId  �/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>�</span></span>

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

### <span data-ttu-id="f552f-136">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f552f-136">-FrontendIPConfiguration</span></span>
<span data-ttu-id="f552f-137">Specifica l'oggetto di configurazione IP front-end per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="f552f-137">Specifies front-end IP configuration object for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f552f-138">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f552f-138">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="f552f-139">Specifica l'ID della configurazione IP front-end per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="f552f-139">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="f552f-140">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="f552f-140">-FrontendPort</span></span>
<span data-ttu-id="f552f-141">Specifica la porta front-end per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="f552f-141">Specifies the front-end port for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f552f-142">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="f552f-142">-FrontendPortId</span></span>
<span data-ttu-id="f552f-143">Specifica l'ID dell'oggetto porta front-end per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="f552f-143">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="f552f-144">-HostName</span><span class="sxs-lookup"><span data-stu-id="f552f-144">-HostName</span></span>
<span data-ttu-id="f552f-145">Specifica il nome host del listener HTTP del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="f552f-145">Specifies the host name of the application gateway HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f552f-146">-HostNames</span><span class="sxs-lookup"><span data-stu-id="f552f-146">-HostNames</span></span>
<span data-ttu-id="f552f-147">Nomi host</span><span class="sxs-lookup"><span data-stu-id="f552f-147">Host names</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f552f-148">-Name</span><span class="sxs-lookup"><span data-stu-id="f552f-148">-Name</span></span>
<span data-ttu-id="f552f-149">Specifica il nome del listener HTTP creato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f552f-149">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f552f-150">-Protocol</span><span class="sxs-lookup"><span data-stu-id="f552f-150">-Protocol</span></span>
<span data-ttu-id="f552f-151">Specifica il protocollo utilizzato dal listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="f552f-151">Specifies the protocol that the HTTP listener uses.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f552f-152">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="f552f-152">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: true
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f552f-153">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="f552f-153">-SslCertificate</span></span>
<span data-ttu-id="f552f-154">Specifica l'oggetto certificato SSL per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="f552f-154">Specifies the SSL certificate object for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f552f-155">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="f552f-155">-SslCertificateId</span></span>
<span data-ttu-id="f552f-156">Specifica l'ID del certificato SSL per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="f552f-156">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="f552f-157">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="f552f-157">-SslProfile</span></span>
<span data-ttu-id="f552f-158">SslProfile</span><span class="sxs-lookup"><span data-stu-id="f552f-158">SslProfile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f552f-159">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="f552f-159">-SslProfileId</span></span>
<span data-ttu-id="f552f-160">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="f552f-160">SslProfileId</span></span>

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

### <span data-ttu-id="f552f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f552f-161">CommonParameters</span></span>
<span data-ttu-id="f552f-162">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f552f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f552f-163">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f552f-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f552f-164">INPUT</span><span class="sxs-lookup"><span data-stu-id="f552f-164">INPUTS</span></span>

### <span data-ttu-id="f552f-165">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f552f-165">None</span></span>

## <span data-ttu-id="f552f-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f552f-166">OUTPUTS</span></span>

### <span data-ttu-id="f552f-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpHttpApplication</span><span class="sxs-lookup"><span data-stu-id="f552f-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f552f-168">NOTE</span><span class="sxs-lookup"><span data-stu-id="f552f-168">NOTES</span></span>

## <span data-ttu-id="f552f-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f552f-169">RELATED LINKS</span></span>

[<span data-ttu-id="f552f-170">Add-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="f552f-170">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="f552f-171">Get-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="f552f-171">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="f552f-172">Remove-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="f552f-172">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="f552f-173">Set-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="f552f-173">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


