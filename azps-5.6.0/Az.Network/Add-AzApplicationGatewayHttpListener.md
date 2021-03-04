---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 51d85ffa9c1181b45f7ea4aa45484a814759a953
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982637"
---
# <span data-ttu-id="6892f-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6892f-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="6892f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6892f-102">SYNOPSIS</span></span>
<span data-ttu-id="6892f-103">Aggiunge un listener HTTP a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6892f-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="6892f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6892f-104">SYNTAX</span></span>

### <span data-ttu-id="6892f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6892f-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-SslProfileId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6892f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6892f-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6892f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6892f-107">DESCRIPTION</span></span>
<span data-ttu-id="6892f-108">Il cmdlet **Add-AzApplicationGatewayHttpHttpHttp Listener aggiunge** un listener HTTP a un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6892f-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="6892f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6892f-109">EXAMPLES</span></span>

### <span data-ttu-id="6892f-110">Esempio 1: Aggiungere un listener HTTP</span><span class="sxs-lookup"><span data-stu-id="6892f-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="6892f-111">Il primo comando recupera il gateway applicazione e lo archivia nella $AppGw variabile. Il secondo comando aggiunge il listener HTTP al gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6892f-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="6892f-112">Esempio 2: Aggiungere un listener HTTPS con SSL</span><span class="sxs-lookup"><span data-stu-id="6892f-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="6892f-113">Il primo comando recupera il gateway applicazione e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="6892f-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6892f-114">Il secondo comando aggiunge il listener, che usa il protocollo HTTPS, al gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6892f-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

### <span data-ttu-id="6892f-115">Esempio 3: Aggiungere un listener HTTPS con SSL e HostNames</span><span class="sxs-lookup"><span data-stu-id="6892f-115">Example 3: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com","www.microsoft.com"
```

<span data-ttu-id="6892f-116">Il primo comando recupera il gateway applicazione e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="6892f-116">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6892f-117">Il secondo comando aggiunge il listener, che usa il protocollo HTTPS, con certificati SSL e nomi host, al gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6892f-117">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="6892f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6892f-118">PARAMETERS</span></span>

### <span data-ttu-id="6892f-119">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6892f-119">-ApplicationGateway</span></span>
<span data-ttu-id="6892f-120">Specifica il gateway applicazione a cui questo cmdlet aggiunge un listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="6892f-120">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6892f-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="6892f-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="6892f-122">Errore del cliente di un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="6892f-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="6892f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6892f-123">-DefaultProfile</span></span>
<span data-ttu-id="6892f-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6892f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6892f-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="6892f-125">-FirewallPolicy</span></span>
<span data-ttu-id="6892f-126">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="6892f-126">FirewallPolicy</span></span>

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

### <span data-ttu-id="6892f-127">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="6892f-127">-FirewallPolicyId</span></span>
<span data-ttu-id="6892f-128">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="6892f-128">FirewallPolicyId</span></span>

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

### <span data-ttu-id="6892f-129">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6892f-129">-FrontendIPConfiguration</span></span>
<span data-ttu-id="6892f-130">Specifica l'oggetto risorsa IP front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6892f-130">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="6892f-131">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6892f-131">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="6892f-132">Specifica l'ID IP front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6892f-132">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="6892f-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="6892f-133">-FrontendPort</span></span>
<span data-ttu-id="6892f-134">Specifica l'oggetto porta front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6892f-134">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="6892f-135">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="6892f-135">-FrontendPortId</span></span>
<span data-ttu-id="6892f-136">Specifica l'ID porta front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="6892f-136">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="6892f-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="6892f-137">-HostName</span></span>
<span data-ttu-id="6892f-138">Specifica il nome host a cui il cmdlet aggiunge un listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="6892f-138">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="6892f-139">-HostNames</span><span class="sxs-lookup"><span data-stu-id="6892f-139">-HostNames</span></span>
<span data-ttu-id="6892f-140">Nomi host</span><span class="sxs-lookup"><span data-stu-id="6892f-140">Host names</span></span>

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

### <span data-ttu-id="6892f-141">-Name</span><span class="sxs-lookup"><span data-stu-id="6892f-141">-Name</span></span>
<span data-ttu-id="6892f-142">Specifica il nome della porta front-end aggiunta dal comando.</span><span class="sxs-lookup"><span data-stu-id="6892f-142">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="6892f-143">-Protocol</span><span class="sxs-lookup"><span data-stu-id="6892f-143">-Protocol</span></span>
<span data-ttu-id="6892f-144">Specifica il protocollo del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="6892f-144">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="6892f-145">Sono supportati sia HTTP che HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6892f-145">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="6892f-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="6892f-146">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6892f-147">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="6892f-147">-SslCertificate</span></span>
<span data-ttu-id="6892f-148">Specifica il certificato SSL del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="6892f-148">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="6892f-149">Deve essere specificato se https è scelto come protocollo listener.</span><span class="sxs-lookup"><span data-stu-id="6892f-149">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="6892f-150">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="6892f-150">-SslCertificateId</span></span>
<span data-ttu-id="6892f-151">Specifica l'ID certificato SSL del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="6892f-151">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="6892f-152">Deve essere specificato se https è scelto come protocollo listener.</span><span class="sxs-lookup"><span data-stu-id="6892f-152">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="6892f-153">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="6892f-153">-SslProfile</span></span>
<span data-ttu-id="6892f-154">SslProfile</span><span class="sxs-lookup"><span data-stu-id="6892f-154">SslProfile</span></span>

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

### <span data-ttu-id="6892f-155">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="6892f-155">-SslProfileId</span></span>
<span data-ttu-id="6892f-156">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="6892f-156">SslProfileId</span></span>

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

### <span data-ttu-id="6892f-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6892f-157">CommonParameters</span></span>
<span data-ttu-id="6892f-158">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6892f-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6892f-159">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6892f-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6892f-160">INPUT</span><span class="sxs-lookup"><span data-stu-id="6892f-160">INPUTS</span></span>

### <span data-ttu-id="6892f-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6892f-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6892f-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6892f-162">OUTPUTS</span></span>

### <span data-ttu-id="6892f-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6892f-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6892f-164">NOTE</span><span class="sxs-lookup"><span data-stu-id="6892f-164">NOTES</span></span>

## <span data-ttu-id="6892f-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6892f-165">RELATED LINKS</span></span>

[<span data-ttu-id="6892f-166">Get-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="6892f-166">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="6892f-167">New-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="6892f-167">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="6892f-168">Remove-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="6892f-168">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="6892f-169">Set-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="6892f-169">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


