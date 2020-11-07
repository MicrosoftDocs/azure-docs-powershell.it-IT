---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 11a416e237ff4a12dc3aafbd161e1ae77faab732
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854165"
---
# <span data-ttu-id="73ba7-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="73ba7-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="73ba7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="73ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="73ba7-103">Modifica un listener HTTP per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="73ba7-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="73ba7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73ba7-104">SYNTAX</span></span>

### <span data-ttu-id="73ba7-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="73ba7-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="73ba7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="73ba7-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73ba7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73ba7-107">DESCRIPTION</span></span>
<span data-ttu-id="73ba7-108">Il cmdlet **set-AzApplicationGatewayHttpListener** modifica un listener HTTP per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="73ba7-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="73ba7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73ba7-109">EXAMPLES</span></span>

### <span data-ttu-id="73ba7-110">Esempio 1: impostare un listener HTTP</span><span class="sxs-lookup"><span data-stu-id="73ba7-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="73ba7-111">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="73ba7-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="73ba7-112">Il secondo comando imposta il listener HTTP per il gateway per l'uso della configurazione front-end archiviata in $FIP 01 con il protocollo HTTP sulla porta 80.</span><span class="sxs-lookup"><span data-stu-id="73ba7-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="73ba7-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="73ba7-113">PARAMETERS</span></span>

### <span data-ttu-id="73ba7-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73ba7-114">-ApplicationGateway</span></span>
<span data-ttu-id="73ba7-115">Specifica il gateway dell'applicazione con cui questo cmdlet associa il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="73ba7-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="73ba7-116">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="73ba7-116">-CustomErrorConfiguration</span></span>
<span data-ttu-id="73ba7-117">Errore del cliente di un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="73ba7-117">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="73ba7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73ba7-118">-DefaultProfile</span></span>
<span data-ttu-id="73ba7-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="73ba7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73ba7-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="73ba7-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="73ba7-121">Specifica l'indirizzo IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="73ba7-121">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="73ba7-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="73ba7-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="73ba7-123">Specifica l'ID dell'indirizzo IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="73ba7-123">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="73ba7-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="73ba7-124">-FrontendPort</span></span>
<span data-ttu-id="73ba7-125">Specifica la porta di front-end gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="73ba7-125">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="73ba7-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="73ba7-126">-FrontendPortId</span></span>
<span data-ttu-id="73ba7-127">Specifica l'ID della porta del gateway dell'applicazione front-end.</span><span class="sxs-lookup"><span data-stu-id="73ba7-127">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="73ba7-128">-HostName</span><span class="sxs-lookup"><span data-stu-id="73ba7-128">-HostName</span></span>
<span data-ttu-id="73ba7-129">Specifica il nome host a cui questo cmdlet invia il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="73ba7-129">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="73ba7-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="73ba7-130">-Name</span></span>
<span data-ttu-id="73ba7-131">Specifica il nome del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="73ba7-131">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="73ba7-132">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="73ba7-132">-Protocol</span></span>
<span data-ttu-id="73ba7-133">Specifica il protocollo usato dal listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="73ba7-133">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="73ba7-134">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="73ba7-134">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="73ba7-135">Http</span><span class="sxs-lookup"><span data-stu-id="73ba7-135">Http</span></span>
- <span data-ttu-id="73ba7-136">Https</span><span class="sxs-lookup"><span data-stu-id="73ba7-136">Https</span></span>

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

### <span data-ttu-id="73ba7-137">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="73ba7-137">-RequireServerNameIndication</span></span>
<span data-ttu-id="73ba7-138">Specifica se il cmdlet richiede l'indicazione del nome del server.</span><span class="sxs-lookup"><span data-stu-id="73ba7-138">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="73ba7-139">I valori accettabili per questo parametro sono: vero o falso.</span><span class="sxs-lookup"><span data-stu-id="73ba7-139">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="73ba7-140">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="73ba7-140">-SslCertificate</span></span>
<span data-ttu-id="73ba7-141">Specifica il certificato SSL del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="73ba7-141">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="73ba7-142">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="73ba7-142">-SslCertificateId</span></span>
<span data-ttu-id="73ba7-143">Specifica l'ID del certificato SSL (Secure Socket Layer) del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="73ba7-143">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="73ba7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73ba7-144">CommonParameters</span></span>
<span data-ttu-id="73ba7-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73ba7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73ba7-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73ba7-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73ba7-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="73ba7-147">INPUTS</span></span>

### <span data-ttu-id="73ba7-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73ba7-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="73ba7-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73ba7-149">OUTPUTS</span></span>

### <span data-ttu-id="73ba7-150">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73ba7-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="73ba7-151">Note</span><span class="sxs-lookup"><span data-stu-id="73ba7-151">NOTES</span></span>

## <span data-ttu-id="73ba7-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73ba7-152">RELATED LINKS</span></span>

[<span data-ttu-id="73ba7-153">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="73ba7-153">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="73ba7-154">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="73ba7-154">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="73ba7-155">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="73ba7-155">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="73ba7-156">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="73ba7-156">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


