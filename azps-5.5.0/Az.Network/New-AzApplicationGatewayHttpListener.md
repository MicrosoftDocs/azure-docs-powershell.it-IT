---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: a6fc3eb16cc82f7a0964e8cd0c1697a083771016
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202929"
---
# <span data-ttu-id="bfc2d-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bfc2d-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="bfc2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfc2d-102">SYNOPSIS</span></span>
<span data-ttu-id="bfc2d-103">Crea un listener HTTP per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="bfc2d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bfc2d-104">SYNTAX</span></span>

### <span data-ttu-id="bfc2d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bfc2d-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-FirewallPolicyId <String>] [-SslProfileId <String>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bfc2d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bfc2d-106">SetByResource</span></span>
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

## <span data-ttu-id="bfc2d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bfc2d-107">DESCRIPTION</span></span>
<span data-ttu-id="bfc2d-108">Il cmdlet **New-AzApplicationGatewayHttpHttpHttp Listener crea** un listener HTTP per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="bfc2d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bfc2d-109">EXAMPLES</span></span>

### <span data-ttu-id="bfc2d-110">Esempio 1: Creare un listener HTTP</span><span class="sxs-lookup"><span data-stu-id="bfc2d-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="bfc2d-111">Questo comando crea un listener HTTP denominato Listener01 e archivia il risultato nella variabile $Listener.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="bfc2d-112">Esempio 2: Creare un listener HTTP con SSL</span><span class="sxs-lookup"><span data-stu-id="bfc2d-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="bfc2d-113">Questo comando crea un listener HTTP che usa l'offload SSL e fornisce il certificato SSL nella variabile $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="bfc2d-114">Il comando archivia il risultato nella variabile denominata $Listener.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-114">The command stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="bfc2d-115">Esempio 3: Creare un listener HTTP con criteri firewall</span><span class="sxs-lookup"><span data-stu-id="bfc2d-115">Example 3: Create an HTTP listener with firewall-policy</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="bfc2d-116">Questo comando crea un listener HTTP denominato Listener01, FirewallPolicy $firewallPolicy e archivia il risultato nella variabile $Listener.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-116">This command creates an HTTP listener named Listener01, FirewallPolicy as $firewallPolicy and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="bfc2d-117">Esempio 4: Aggiungere un listener HTTPS con SSL e HostNames</span><span class="sxs-lookup"><span data-stu-id="bfc2d-117">Example 4: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="bfc2d-118">Questo comando crea un listener HTTP che usa l'offload SSL e fornisce il certificato SSL nella variabile $SSLCert 01 insieme a due HostNames.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-118">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable along with two HostNames.</span></span>
<span data-ttu-id="bfc2d-119">Il comando archivia il risultato nella variabile denominata $Listener.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-119">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="bfc2d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfc2d-120">PARAMETERS</span></span>

### <span data-ttu-id="bfc2d-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfc2d-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="bfc2d-122">Errore del cliente di un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="bfc2d-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="bfc2d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfc2d-123">-DefaultProfile</span></span>
<span data-ttu-id="bfc2d-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfc2d-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="bfc2d-125">-FirewallPolicy</span></span>
<span data-ttu-id="bfc2d-126">Specifica il riferimento all'oggetto a un criterio firewall di primo livello.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-126">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="bfc2d-127">Il riferimento all'oggetto può essere creato usando New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-127">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="bfc2d-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" Un criterio firewall creato con il commandlet riportato sopra può essere indicato a livello di regola del percorso.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="bfc2d-129">Il comando precedente crea impostazioni dei criteri predefinite e regole gestite.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-129">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="bfc2d-130">Invece dei valori predefiniti, gli utenti possono specificare PolicySettings e ManagedRules usando rispettivamente New-AzApplicationGatewayFirewallPolicySettings e New-AzApplicationGatewayFirewallPolicyManagedRules predefiniti.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-130">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

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

### <span data-ttu-id="bfc2d-131">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="bfc2d-131">-FirewallPolicyId</span></span>
<span data-ttu-id="bfc2d-132">Specifica l'ID di una risorsa firewall dell'applicazione Web di primo livello esistente.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-132">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="bfc2d-133">Gli ID dei criteri del firewall possono essere restituiti usando il cmdlet Get-AzApplicationGatewayWebApplicationFirewallPolicy firewall.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-133">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="bfc2d-134">Una volta fornito l'ID, è possibile usare il *parametro FirewallPolicyId* invece del *parametro FirewallPolicy.*</span><span class="sxs-lookup"><span data-stu-id="bfc2d-134">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="bfc2d-135">Ad esempio: -FirewallPolicyId /subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName></span><span class="sxs-lookup"><span data-stu-id="bfc2d-135">For instance: -FirewallPolicyId  �/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>�</span></span>

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

### <span data-ttu-id="bfc2d-136">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfc2d-136">-FrontendIPConfiguration</span></span>
<span data-ttu-id="bfc2d-137">Specifica l'oggetto di configurazione IP front-end per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-137">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="bfc2d-138">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="bfc2d-138">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="bfc2d-139">Specifica l'ID della configurazione IP front-end per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-139">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="bfc2d-140">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="bfc2d-140">-FrontendPort</span></span>
<span data-ttu-id="bfc2d-141">Specifica la porta front-end per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-141">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="bfc2d-142">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="bfc2d-142">-FrontendPortId</span></span>
<span data-ttu-id="bfc2d-143">Specifica l'ID dell'oggetto porta front-end per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-143">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="bfc2d-144">-HostName</span><span class="sxs-lookup"><span data-stu-id="bfc2d-144">-HostName</span></span>
<span data-ttu-id="bfc2d-145">Specifica il nome host del listener HTTP del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-145">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="bfc2d-146">-HostNames</span><span class="sxs-lookup"><span data-stu-id="bfc2d-146">-HostNames</span></span>
<span data-ttu-id="bfc2d-147">Nomi host</span><span class="sxs-lookup"><span data-stu-id="bfc2d-147">Host names</span></span>

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

### <span data-ttu-id="bfc2d-148">-Name</span><span class="sxs-lookup"><span data-stu-id="bfc2d-148">-Name</span></span>
<span data-ttu-id="bfc2d-149">Specifica il nome del listener HTTP creato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-149">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="bfc2d-150">-Protocol</span><span class="sxs-lookup"><span data-stu-id="bfc2d-150">-Protocol</span></span>
<span data-ttu-id="bfc2d-151">Specifica il protocollo utilizzato dal listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-151">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="bfc2d-152">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="bfc2d-152">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="bfc2d-153">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="bfc2d-153">-SslCertificate</span></span>
<span data-ttu-id="bfc2d-154">Specifica l'oggetto certificato SSL per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-154">Specifies the SSL certificate object for the HTTP listener.</span></span>

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

### <span data-ttu-id="bfc2d-155">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="bfc2d-155">-SslCertificateId</span></span>
<span data-ttu-id="bfc2d-156">Specifica l'ID del certificato SSL per il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-156">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="bfc2d-157">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="bfc2d-157">-SslProfile</span></span>
<span data-ttu-id="bfc2d-158">SslProfile</span><span class="sxs-lookup"><span data-stu-id="bfc2d-158">SslProfile</span></span>

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

### <span data-ttu-id="bfc2d-159">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="bfc2d-159">-SslProfileId</span></span>
<span data-ttu-id="bfc2d-160">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="bfc2d-160">SslProfileId</span></span>

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

### <span data-ttu-id="bfc2d-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfc2d-161">CommonParameters</span></span>
<span data-ttu-id="bfc2d-162">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfc2d-163">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bfc2d-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfc2d-164">INPUT</span><span class="sxs-lookup"><span data-stu-id="bfc2d-164">INPUTS</span></span>

### <span data-ttu-id="bfc2d-165">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bfc2d-165">None</span></span>

## <span data-ttu-id="bfc2d-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bfc2d-166">OUTPUTS</span></span>

### <span data-ttu-id="bfc2d-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="bfc2d-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="bfc2d-168">NOTE</span><span class="sxs-lookup"><span data-stu-id="bfc2d-168">NOTES</span></span>

## <span data-ttu-id="bfc2d-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bfc2d-169">RELATED LINKS</span></span>

[<span data-ttu-id="bfc2d-170">Add-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="bfc2d-170">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="bfc2d-171">Get-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="bfc2d-171">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="bfc2d-172">Remove-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="bfc2d-172">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="bfc2d-173">Set-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="bfc2d-173">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


