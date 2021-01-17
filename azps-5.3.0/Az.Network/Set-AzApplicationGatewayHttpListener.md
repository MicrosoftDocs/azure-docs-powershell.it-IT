---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 8ce5d01d78b8b434e062b0f33ee41a4cbbce20ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378710"
---
# <span data-ttu-id="c52dc-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c52dc-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="c52dc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c52dc-102">SYNOPSIS</span></span>
<span data-ttu-id="c52dc-103">Modifica un listener HTTP per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c52dc-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="c52dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c52dc-104">SYNTAX</span></span>

### <span data-ttu-id="c52dc-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c52dc-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-SslProfileId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c52dc-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c52dc-106">SetByResource</span></span>
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

## <span data-ttu-id="c52dc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c52dc-107">DESCRIPTION</span></span>
<span data-ttu-id="c52dc-108">Il cmdlet **set-AzApplicationGatewayHttpListener** modifica un listener HTTP per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="c52dc-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="c52dc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c52dc-109">EXAMPLES</span></span>

### <span data-ttu-id="c52dc-110">Esempio 1: impostare un listener HTTP</span><span class="sxs-lookup"><span data-stu-id="c52dc-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="c52dc-111">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c52dc-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c52dc-112">Il secondo comando imposta il listener HTTP per il gateway per l'uso della configurazione front-end archiviata in $FIP 01 con il protocollo HTTP sulla porta 80.</span><span class="sxs-lookup"><span data-stu-id="c52dc-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

### <span data-ttu-id="c52dc-113">Esempio 2: aggiungere un listener HTTPS con SSL e nomi host</span><span class="sxs-lookup"><span data-stu-id="c52dc-113">Example 2: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="c52dc-114">Il primo comando ottiene il gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="c52dc-114">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c52dc-115">Il secondo comando aggiunge il listener, che usa il protocollo HTTPS, con i certificati SSL e i nomi host, al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c52dc-115">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="c52dc-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c52dc-116">PARAMETERS</span></span>

### <span data-ttu-id="c52dc-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c52dc-117">-ApplicationGateway</span></span>
<span data-ttu-id="c52dc-118">Specifica il gateway dell'applicazione con cui questo cmdlet associa il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="c52dc-118">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="c52dc-119">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="c52dc-119">-CustomErrorConfiguration</span></span>
<span data-ttu-id="c52dc-120">Errore del cliente di un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="c52dc-120">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="c52dc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c52dc-121">-DefaultProfile</span></span>
<span data-ttu-id="c52dc-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c52dc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c52dc-123">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="c52dc-123">-FirewallPolicy</span></span>
<span data-ttu-id="c52dc-124">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="c52dc-124">FirewallPolicy</span></span>

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

### <span data-ttu-id="c52dc-125">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="c52dc-125">-FirewallPolicyId</span></span>
<span data-ttu-id="c52dc-126">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="c52dc-126">FirewallPolicyId</span></span>

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

### <span data-ttu-id="c52dc-127">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c52dc-127">-FrontendIPConfiguration</span></span>
<span data-ttu-id="c52dc-128">Specifica l'indirizzo IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c52dc-128">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="c52dc-129">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c52dc-129">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="c52dc-130">Specifica l'ID dell'indirizzo IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c52dc-130">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="c52dc-131">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="c52dc-131">-FrontendPort</span></span>
<span data-ttu-id="c52dc-132">Specifica la porta di front-end gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c52dc-132">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="c52dc-133">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="c52dc-133">-FrontendPortId</span></span>
<span data-ttu-id="c52dc-134">Specifica l'ID della porta del gateway dell'applicazione front-end.</span><span class="sxs-lookup"><span data-stu-id="c52dc-134">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="c52dc-135">-HostName</span><span class="sxs-lookup"><span data-stu-id="c52dc-135">-HostName</span></span>
<span data-ttu-id="c52dc-136">Specifica il nome host a cui questo cmdlet invia il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="c52dc-136">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="c52dc-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="c52dc-137">-HostNames</span></span>
<span data-ttu-id="c52dc-138">Nomi host</span><span class="sxs-lookup"><span data-stu-id="c52dc-138">Host names</span></span>

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

### <span data-ttu-id="c52dc-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="c52dc-139">-Name</span></span>
<span data-ttu-id="c52dc-140">Specifica il nome del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="c52dc-140">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="c52dc-141">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="c52dc-141">-Protocol</span></span>
<span data-ttu-id="c52dc-142">Specifica il protocollo usato dal listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="c52dc-142">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="c52dc-143">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c52dc-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c52dc-144">Http</span><span class="sxs-lookup"><span data-stu-id="c52dc-144">Http</span></span>
- <span data-ttu-id="c52dc-145">Https</span><span class="sxs-lookup"><span data-stu-id="c52dc-145">Https</span></span>

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

### <span data-ttu-id="c52dc-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="c52dc-146">-RequireServerNameIndication</span></span>
<span data-ttu-id="c52dc-147">Specifica se il cmdlet richiede l'indicazione del nome del server.</span><span class="sxs-lookup"><span data-stu-id="c52dc-147">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="c52dc-148">I valori accettabili per questo parametro sono: vero o falso.</span><span class="sxs-lookup"><span data-stu-id="c52dc-148">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="c52dc-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="c52dc-149">-SslCertificate</span></span>
<span data-ttu-id="c52dc-150">Specifica il certificato SSL del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="c52dc-150">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="c52dc-151">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="c52dc-151">-SslCertificateId</span></span>
<span data-ttu-id="c52dc-152">Specifica l'ID del certificato SSL (Secure Socket Layer) del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="c52dc-152">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="c52dc-153">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="c52dc-153">-SslProfile</span></span>
<span data-ttu-id="c52dc-154">SslProfile</span><span class="sxs-lookup"><span data-stu-id="c52dc-154">SslProfile</span></span>

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

### <span data-ttu-id="c52dc-155">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="c52dc-155">-SslProfileId</span></span>
<span data-ttu-id="c52dc-156">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="c52dc-156">SslProfileId</span></span>

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

### <span data-ttu-id="c52dc-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c52dc-157">CommonParameters</span></span>
<span data-ttu-id="c52dc-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c52dc-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c52dc-159">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c52dc-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c52dc-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c52dc-160">INPUTS</span></span>

### <span data-ttu-id="c52dc-161">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c52dc-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c52dc-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c52dc-162">OUTPUTS</span></span>

### <span data-ttu-id="c52dc-163">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c52dc-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c52dc-164">Note</span><span class="sxs-lookup"><span data-stu-id="c52dc-164">NOTES</span></span>

## <span data-ttu-id="c52dc-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c52dc-165">RELATED LINKS</span></span>

[<span data-ttu-id="c52dc-166">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c52dc-166">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="c52dc-167">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c52dc-167">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="c52dc-168">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c52dc-168">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="c52dc-169">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c52dc-169">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


