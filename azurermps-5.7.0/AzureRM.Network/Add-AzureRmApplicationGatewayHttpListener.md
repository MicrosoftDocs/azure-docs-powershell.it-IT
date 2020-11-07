---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 34c40e17ca1ae297677c05ffc198c7580ef7c4a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686098"
---
# <span data-ttu-id="f8080-101">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f8080-101">Add-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="f8080-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8080-102">SYNOPSIS</span></span>
<span data-ttu-id="f8080-103">Aggiunge un listener HTTP a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f8080-103">Adds an HTTP listener to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8080-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8080-104">SYNTAX</span></span>

### <span data-ttu-id="f8080-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f8080-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8080-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f8080-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8080-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8080-107">DESCRIPTION</span></span>
<span data-ttu-id="f8080-108">Il cmdlet **Add-AzureRmApplicationGatewayHttpListener** aggiunge un listener HTTP a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f8080-108">The **Add-AzureRmApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="f8080-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8080-109">EXAMPLES</span></span>

### <span data-ttu-id="f8080-110">Esempio 1: aggiungere un listener HTTP</span><span class="sxs-lookup"><span data-stu-id="f8080-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="f8080-111">Il primo comando ottiene il gateway dell'applicazione e lo archivia nella variabile $AppGw. Il secondo comando aggiunge il listener HTTP al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f8080-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="f8080-112">Esempio 2: aggiungere un listener HTTPS con SSL</span><span class="sxs-lookup"><span data-stu-id="f8080-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="f8080-113">Il primo comando ottiene il gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f8080-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f8080-114">Il secondo comando aggiunge il listener, che usa il protocollo HTTPS, al gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f8080-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="f8080-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8080-115">PARAMETERS</span></span>

### <span data-ttu-id="f8080-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f8080-116">-ApplicationGateway</span></span>
<span data-ttu-id="f8080-117">Specifica il gateway dell'applicazione a cui questo cmdlet aggiunge un listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="f8080-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8080-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8080-118">-DefaultProfile</span></span>
<span data-ttu-id="f8080-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f8080-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8080-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8080-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="f8080-121">Specifica l'oggetto risorsa IP front-end dell'applicazione gateway.</span><span class="sxs-lookup"><span data-stu-id="f8080-121">Specifies the application gateway front-end IP resource object.</span></span>

```yaml
Type: PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8080-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f8080-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="f8080-123">Specifica l'ID IP front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="f8080-123">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="f8080-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="f8080-124">-FrontendPort</span></span>
<span data-ttu-id="f8080-125">Specifica l'oggetto della porta front-end del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="f8080-125">Specifies the application gateway front-end port object.</span></span>

```yaml
Type: PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8080-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="f8080-126">-FrontendPortId</span></span>
<span data-ttu-id="f8080-127">Specifica l'ID della porta del gateway dell'applicazione front-end.</span><span class="sxs-lookup"><span data-stu-id="f8080-127">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="f8080-128">-HostName</span><span class="sxs-lookup"><span data-stu-id="f8080-128">-HostName</span></span>
<span data-ttu-id="f8080-129">Specifica il nome host a cui questo cmdlet aggiunge un listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="f8080-129">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8080-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8080-130">-Name</span></span>
<span data-ttu-id="f8080-131">Specifica il nome della porta front-end aggiunta da questo comando.</span><span class="sxs-lookup"><span data-stu-id="f8080-131">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="f8080-132">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="f8080-132">-Protocol</span></span>
<span data-ttu-id="f8080-133">Specifica il protocollo del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="f8080-133">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="f8080-134">Sono supportati sia HTTP che HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f8080-134">Both HTTP and HTTPS are supported.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8080-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="f8080-135">-RequireServerNameIndication</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8080-136">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="f8080-136">-SslCertificate</span></span>
<span data-ttu-id="f8080-137">Specifica il certificato SSL del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="f8080-137">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="f8080-138">Deve essere specificato se HTTPS viene scelto come protocollo listener.</span><span class="sxs-lookup"><span data-stu-id="f8080-138">Must be specified if HTTPS is chosen as listener protocol.</span></span>

```yaml
Type: PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8080-139">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="f8080-139">-SslCertificateId</span></span>
<span data-ttu-id="f8080-140">Specifica l'ID del certificato SSL del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="f8080-140">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="f8080-141">Deve essere specificato se HTTPS viene scelto come protocollo listener.</span><span class="sxs-lookup"><span data-stu-id="f8080-141">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="f8080-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8080-142">CommonParameters</span></span>
<span data-ttu-id="f8080-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8080-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8080-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8080-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8080-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8080-145">INPUTS</span></span>

### <span data-ttu-id="f8080-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f8080-146">System.String</span></span>

## <span data-ttu-id="f8080-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8080-147">OUTPUTS</span></span>

### <span data-ttu-id="f8080-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f8080-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f8080-149">Note</span><span class="sxs-lookup"><span data-stu-id="f8080-149">NOTES</span></span>

## <span data-ttu-id="f8080-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8080-150">RELATED LINKS</span></span>

[<span data-ttu-id="f8080-151">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f8080-151">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="f8080-152">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f8080-152">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="f8080-153">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f8080-153">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="f8080-154">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="f8080-154">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)

