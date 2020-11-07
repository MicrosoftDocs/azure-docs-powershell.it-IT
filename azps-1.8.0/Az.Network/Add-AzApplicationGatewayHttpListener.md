---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 5648bb1cb7497517afb5ff461674294e426c0131
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678703"
---
# <span data-ttu-id="41855-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="41855-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="41855-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="41855-102">SYNOPSIS</span></span>
<span data-ttu-id="41855-103">Aggiunge un listener HTTP a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="41855-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="41855-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41855-104">SYNTAX</span></span>

### <span data-ttu-id="41855-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="41855-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="41855-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="41855-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41855-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41855-107">DESCRIPTION</span></span>
<span data-ttu-id="41855-108">Il cmdlet **Add-AzApplicationGatewayHttpListener** aggiunge un listener HTTP a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="41855-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="41855-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41855-109">EXAMPLES</span></span>

### <span data-ttu-id="41855-110">Esempio 1: aggiungere un listener HTTP</span><span class="sxs-lookup"><span data-stu-id="41855-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="41855-111">Il primo comando ottiene il gateway dell'applicazione e lo archivia nella variabile $AppGw. Il secondo comando aggiunge il listener HTTP al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="41855-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="41855-112">Esempio 2: aggiungere un listener HTTPS con SSL</span><span class="sxs-lookup"><span data-stu-id="41855-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="41855-113">Il primo comando ottiene il gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="41855-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="41855-114">Il secondo comando aggiunge il listener, che usa il protocollo HTTPS, al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="41855-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="41855-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="41855-115">PARAMETERS</span></span>

### <span data-ttu-id="41855-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="41855-116">-ApplicationGateway</span></span>
<span data-ttu-id="41855-117">Specifica il gateway dell'applicazione a cui questo cmdlet aggiunge un listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="41855-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="41855-118">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="41855-118">-CustomErrorConfiguration</span></span>
<span data-ttu-id="41855-119">Errore del cliente di un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="41855-119">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="41855-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41855-120">-DefaultProfile</span></span>
<span data-ttu-id="41855-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="41855-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41855-122">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="41855-122">-FrontendIPConfiguration</span></span>
<span data-ttu-id="41855-123">Specifica l'oggetto risorsa IP front-end dell'applicazione gateway.</span><span class="sxs-lookup"><span data-stu-id="41855-123">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="41855-124">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="41855-124">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="41855-125">Specifica l'ID IP front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="41855-125">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="41855-126">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="41855-126">-FrontendPort</span></span>
<span data-ttu-id="41855-127">Specifica l'oggetto della porta front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="41855-127">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="41855-128">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="41855-128">-FrontendPortId</span></span>
<span data-ttu-id="41855-129">Specifica l'ID della porta del gateway dell'applicazione front-end.</span><span class="sxs-lookup"><span data-stu-id="41855-129">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="41855-130">-HostName</span><span class="sxs-lookup"><span data-stu-id="41855-130">-HostName</span></span>
<span data-ttu-id="41855-131">Specifica il nome host a cui questo cmdlet aggiunge un listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="41855-131">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="41855-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="41855-132">-Name</span></span>
<span data-ttu-id="41855-133">Specifica il nome della porta front-end aggiunta da questo comando.</span><span class="sxs-lookup"><span data-stu-id="41855-133">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="41855-134">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="41855-134">-Protocol</span></span>
<span data-ttu-id="41855-135">Specifica il protocollo del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="41855-135">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="41855-136">Sono supportati sia HTTP che HTTPS.</span><span class="sxs-lookup"><span data-stu-id="41855-136">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="41855-137">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="41855-137">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="41855-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="41855-138">-SslCertificate</span></span>
<span data-ttu-id="41855-139">Specifica il certificato SSL del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="41855-139">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="41855-140">Deve essere specificato se HTTPS viene scelto come protocollo listener.</span><span class="sxs-lookup"><span data-stu-id="41855-140">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="41855-141">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="41855-141">-SslCertificateId</span></span>
<span data-ttu-id="41855-142">Specifica l'ID del certificato SSL del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="41855-142">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="41855-143">Deve essere specificato se HTTPS viene scelto come protocollo listener.</span><span class="sxs-lookup"><span data-stu-id="41855-143">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="41855-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41855-144">CommonParameters</span></span>
<span data-ttu-id="41855-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41855-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41855-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41855-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41855-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="41855-147">INPUTS</span></span>

### <span data-ttu-id="41855-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="41855-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="41855-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41855-149">OUTPUTS</span></span>

### <span data-ttu-id="41855-150">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="41855-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="41855-151">Note</span><span class="sxs-lookup"><span data-stu-id="41855-151">NOTES</span></span>

## <span data-ttu-id="41855-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41855-152">RELATED LINKS</span></span>

[<span data-ttu-id="41855-153">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="41855-153">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="41855-154">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="41855-154">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="41855-155">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="41855-155">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="41855-156">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="41855-156">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


