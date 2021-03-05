---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 91e8aef2e5d12a13648132a1c8d6ece9dc4d21cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992513"
---
# <span data-ttu-id="e9b3d-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e9b3d-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="e9b3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b3d-103">Modifica un listener HTTP per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="e9b3d-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="e9b3d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9b3d-104">SYNTAX</span></span>

### <span data-ttu-id="e9b3d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e9b3d-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-SslProfileId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9b3d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e9b3d-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9b3d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e9b3d-107">DESCRIPTION</span></span>
<span data-ttu-id="e9b3d-108">Il cmdlet **Set-AzApplicationGatewayHttpHttp Listener** modifica un listener HTTP per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e9b3d-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="e9b3d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9b3d-109">EXAMPLES</span></span>

### <span data-ttu-id="e9b3d-110">Esempio 1: Impostare un listener HTTP</span><span class="sxs-lookup"><span data-stu-id="e9b3d-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="e9b3d-111">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="e9b3d-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e9b3d-112">Il secondo comando imposta il listener HTTP in modo che il gateway usi la configurazione front-end archiviata in $FIP 01 con il protocollo HTTP sulla porta 80.</span><span class="sxs-lookup"><span data-stu-id="e9b3d-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

### <span data-ttu-id="e9b3d-113">Esempio 2: Aggiungere un listener HTTPS con SSL e HostNames</span><span class="sxs-lookup"><span data-stu-id="e9b3d-113">Example 2: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="e9b3d-114">Il primo comando recupera il gateway applicazione e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="e9b3d-114">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e9b3d-115">Il secondo comando aggiunge il listener, che usa il protocollo HTTPS, con certificati SSL e nomi host, al gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="e9b3d-115">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="e9b3d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9b3d-116">PARAMETERS</span></span>

### <span data-ttu-id="e9b3d-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9b3d-117">-ApplicationGateway</span></span>
<span data-ttu-id="e9b3d-118">Specifica il gateway applicazione a cui questo cmdlet associa il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="e9b3d-118">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="e9b3d-119">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9b3d-119">-CustomErrorConfiguration</span></span>
<span data-ttu-id="e9b3d-120">Errore del cliente di un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="e9b3d-120">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="e9b3d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9b3d-121">-DefaultProfile</span></span>
<span data-ttu-id="e9b3d-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e9b3d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9b3d-123">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e9b3d-123">-FirewallPolicy</span></span>
<span data-ttu-id="e9b3d-124">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e9b3d-124">FirewallPolicy</span></span>

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

### <span data-ttu-id="e9b3d-125">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="e9b3d-125">-FirewallPolicyId</span></span>
<span data-ttu-id="e9b3d-126">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="e9b3d-126">FirewallPolicyId</span></span>

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

### <span data-ttu-id="e9b3d-127">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9b3d-127">-FrontendIPConfiguration</span></span>
<span data-ttu-id="e9b3d-128">Specifica l'indirizzo IP front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="e9b3d-128">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="e9b3d-129">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e9b3d-129">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="e9b3d-130">Specifica l'ID dell'indirizzo IP front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="e9b3d-130">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="e9b3d-131">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="e9b3d-131">-FrontendPort</span></span>
<span data-ttu-id="e9b3d-132">Specifica la porta front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="e9b3d-132">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="e9b3d-133">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="e9b3d-133">-FrontendPortId</span></span>
<span data-ttu-id="e9b3d-134">Specifica l'ID porta front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="e9b3d-134">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="e9b3d-135">-HostName</span><span class="sxs-lookup"><span data-stu-id="e9b3d-135">-HostName</span></span>
<span data-ttu-id="e9b3d-136">Specifica il nome host a cui il cmdlet invia il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="e9b3d-136">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="e9b3d-137">-HostNames</span><span class="sxs-lookup"><span data-stu-id="e9b3d-137">-HostNames</span></span>
<span data-ttu-id="e9b3d-138">Nomi host</span><span class="sxs-lookup"><span data-stu-id="e9b3d-138">Host names</span></span>

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

### <span data-ttu-id="e9b3d-139">-Name</span><span class="sxs-lookup"><span data-stu-id="e9b3d-139">-Name</span></span>
<span data-ttu-id="e9b3d-140">Specifica il nome del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="e9b3d-140">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="e9b3d-141">-Protocol</span><span class="sxs-lookup"><span data-stu-id="e9b3d-141">-Protocol</span></span>
<span data-ttu-id="e9b3d-142">Specifica il protocollo utilizzato dal listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="e9b3d-142">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="e9b3d-143">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="e9b3d-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e9b3d-144">Http (http)</span><span class="sxs-lookup"><span data-stu-id="e9b3d-144">Http</span></span>
- <span data-ttu-id="e9b3d-145">Https</span><span class="sxs-lookup"><span data-stu-id="e9b3d-145">Https</span></span>

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

### <span data-ttu-id="e9b3d-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="e9b3d-146">-RequireServerNameIndication</span></span>
<span data-ttu-id="e9b3d-147">Specifica se il cmdlet richiede un'indicazione del nome del server.</span><span class="sxs-lookup"><span data-stu-id="e9b3d-147">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="e9b3d-148">I valori accettabili per questo parametro sono: true o false.</span><span class="sxs-lookup"><span data-stu-id="e9b3d-148">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="e9b3d-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="e9b3d-149">-SslCertificate</span></span>
<span data-ttu-id="e9b3d-150">Specifica il certificato SSL del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="e9b3d-150">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="e9b3d-151">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="e9b3d-151">-SslCertificateId</span></span>
<span data-ttu-id="e9b3d-152">Specifica l'ID certificato SSL (Secure Sockets Layer) del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="e9b3d-152">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="e9b3d-153">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="e9b3d-153">-SslProfile</span></span>
<span data-ttu-id="e9b3d-154">SslProfile</span><span class="sxs-lookup"><span data-stu-id="e9b3d-154">SslProfile</span></span>

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

### <span data-ttu-id="e9b3d-155">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="e9b3d-155">-SslProfileId</span></span>
<span data-ttu-id="e9b3d-156">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="e9b3d-156">SslProfileId</span></span>

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

### <span data-ttu-id="e9b3d-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b3d-157">CommonParameters</span></span>
<span data-ttu-id="e9b3d-158">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9b3d-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b3d-159">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e9b3d-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b3d-160">INPUT</span><span class="sxs-lookup"><span data-stu-id="e9b3d-160">INPUTS</span></span>

### <span data-ttu-id="e9b3d-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9b3d-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e9b3d-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9b3d-162">OUTPUTS</span></span>

### <span data-ttu-id="e9b3d-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9b3d-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e9b3d-164">NOTE</span><span class="sxs-lookup"><span data-stu-id="e9b3d-164">NOTES</span></span>

## <span data-ttu-id="e9b3d-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9b3d-165">RELATED LINKS</span></span>

[<span data-ttu-id="e9b3d-166">Add-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="e9b3d-166">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="e9b3d-167">Get-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="e9b3d-167">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="e9b3d-168">New-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="e9b3d-168">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="e9b3d-169">Remove-AzApplicationGatewayHttpHttp Più</span><span class="sxs-lookup"><span data-stu-id="e9b3d-169">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


