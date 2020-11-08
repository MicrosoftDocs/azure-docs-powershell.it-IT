---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: d3434a650eb09391aa7505f288667aa130401e26
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031185"
---
# <span data-ttu-id="3f3c7-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3f3c7-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="3f3c7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3f3c7-102">SYNOPSIS</span></span>
<span data-ttu-id="3f3c7-103">Aggiunge un listener HTTP a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="3f3c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3f3c7-104">SYNTAX</span></span>

### <span data-ttu-id="3f3c7-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3f3c7-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f3c7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3f3c7-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f3c7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f3c7-107">DESCRIPTION</span></span>
<span data-ttu-id="3f3c7-108">Il cmdlet **Add-AzApplicationGatewayHttpListener** aggiunge un listener HTTP a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="3f3c7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3f3c7-109">EXAMPLES</span></span>

### <span data-ttu-id="3f3c7-110">Esempio 1: aggiungere un listener HTTP</span><span class="sxs-lookup"><span data-stu-id="3f3c7-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="3f3c7-111">Il primo comando ottiene il gateway dell'applicazione e lo archivia nella variabile $AppGw. Il secondo comando aggiunge il listener HTTP al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="3f3c7-112">Esempio 2: aggiungere un listener HTTPS con SSL</span><span class="sxs-lookup"><span data-stu-id="3f3c7-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="3f3c7-113">Il primo comando ottiene il gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3f3c7-114">Il secondo comando aggiunge il listener, che usa il protocollo HTTPS, al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

### <span data-ttu-id="3f3c7-115">Esempio 3: aggiungere un listener HTTPS con SSL e nomi host</span><span class="sxs-lookup"><span data-stu-id="3f3c7-115">Example 3: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="3f3c7-116">Il primo comando ottiene il gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-116">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3f3c7-117">Il secondo comando aggiunge il listener, che usa il protocollo HTTPS, con i certificati SSL e i nomi host, al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-117">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="3f3c7-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3f3c7-118">PARAMETERS</span></span>

### <span data-ttu-id="3f3c7-119">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3f3c7-119">-ApplicationGateway</span></span>
<span data-ttu-id="3f3c7-120">Specifica il gateway dell'applicazione a cui questo cmdlet aggiunge un listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-120">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="3f3c7-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f3c7-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="3f3c7-122">Errore del cliente di un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="3f3c7-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="3f3c7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f3c7-123">-DefaultProfile</span></span>
<span data-ttu-id="3f3c7-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f3c7-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="3f3c7-125">-FirewallPolicy</span></span>
<span data-ttu-id="3f3c7-126">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="3f3c7-126">FirewallPolicy</span></span>

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

### <span data-ttu-id="3f3c7-127">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="3f3c7-127">-FirewallPolicyId</span></span>
<span data-ttu-id="3f3c7-128">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="3f3c7-128">FirewallPolicyId</span></span>

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

### <span data-ttu-id="3f3c7-129">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f3c7-129">-FrontendIPConfiguration</span></span>
<span data-ttu-id="3f3c7-130">Specifica l'oggetto risorsa IP front-end dell'applicazione gateway.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-130">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="3f3c7-131">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="3f3c7-131">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="3f3c7-132">Specifica l'ID IP front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-132">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="3f3c7-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="3f3c7-133">-FrontendPort</span></span>
<span data-ttu-id="3f3c7-134">Specifica l'oggetto della porta front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-134">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="3f3c7-135">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="3f3c7-135">-FrontendPortId</span></span>
<span data-ttu-id="3f3c7-136">Specifica l'ID della porta del gateway dell'applicazione front-end.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-136">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="3f3c7-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="3f3c7-137">-HostName</span></span>
<span data-ttu-id="3f3c7-138">Specifica il nome host a cui questo cmdlet aggiunge un listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-138">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="3f3c7-139">-HostName</span><span class="sxs-lookup"><span data-stu-id="3f3c7-139">-HostNames</span></span>
<span data-ttu-id="3f3c7-140">Nomi host</span><span class="sxs-lookup"><span data-stu-id="3f3c7-140">Host names</span></span>

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

### <span data-ttu-id="3f3c7-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f3c7-141">-Name</span></span>
<span data-ttu-id="3f3c7-142">Specifica il nome della porta front-end aggiunta da questo comando.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-142">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="3f3c7-143">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="3f3c7-143">-Protocol</span></span>
<span data-ttu-id="3f3c7-144">Specifica il protocollo del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-144">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="3f3c7-145">Sono supportati sia HTTP che HTTPS.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-145">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="3f3c7-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="3f3c7-146">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="3f3c7-147">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="3f3c7-147">-SslCertificate</span></span>
<span data-ttu-id="3f3c7-148">Specifica il certificato SSL del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-148">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="3f3c7-149">Deve essere specificato se HTTPS viene scelto come protocollo listener.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-149">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="3f3c7-150">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="3f3c7-150">-SslCertificateId</span></span>
<span data-ttu-id="3f3c7-151">Specifica l'ID del certificato SSL del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-151">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="3f3c7-152">Deve essere specificato se HTTPS viene scelto come protocollo listener.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-152">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="3f3c7-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f3c7-153">CommonParameters</span></span>
<span data-ttu-id="3f3c7-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f3c7-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f3c7-155">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f3c7-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f3c7-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3f3c7-156">INPUTS</span></span>

### <span data-ttu-id="3f3c7-157">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3f3c7-157">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3f3c7-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3f3c7-158">OUTPUTS</span></span>

### <span data-ttu-id="3f3c7-159">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3f3c7-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3f3c7-160">Note</span><span class="sxs-lookup"><span data-stu-id="3f3c7-160">NOTES</span></span>

## <span data-ttu-id="3f3c7-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3f3c7-161">RELATED LINKS</span></span>

[<span data-ttu-id="3f3c7-162">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3f3c7-162">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="3f3c7-163">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3f3c7-163">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="3f3c7-164">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3f3c7-164">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="3f3c7-165">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3f3c7-165">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


