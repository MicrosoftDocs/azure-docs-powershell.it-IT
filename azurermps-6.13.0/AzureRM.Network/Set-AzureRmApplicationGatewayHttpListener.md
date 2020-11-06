---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 231ee3dc8d66d3960f0416cb410b6747b25ae278
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520895"
---
# <span data-ttu-id="17bc0-101">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="17bc0-101">Set-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="17bc0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="17bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="17bc0-103">Modifica un listener HTTP per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="17bc0-103">Modifies an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17bc0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="17bc0-104">SYNTAX</span></span>

### <span data-ttu-id="17bc0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="17bc0-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17bc0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="17bc0-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17bc0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17bc0-107">DESCRIPTION</span></span>
<span data-ttu-id="17bc0-108">Il cmdlet **set-AzureRmApplicationGatewayHttpListener** modifica un listener HTTP per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="17bc0-108">The **Set-AzureRmApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="17bc0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="17bc0-109">EXAMPLES</span></span>

### <span data-ttu-id="17bc0-110">Esempio 1: impostare un listener HTTP</span><span class="sxs-lookup"><span data-stu-id="17bc0-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="17bc0-111">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="17bc0-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="17bc0-112">Il secondo comando imposta il listener HTTP per il gateway per l'uso della configurazione front-end archiviata in $FIP 01 con il protocollo HTTP sulla porta 80.</span><span class="sxs-lookup"><span data-stu-id="17bc0-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="17bc0-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="17bc0-113">PARAMETERS</span></span>

### <span data-ttu-id="17bc0-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="17bc0-114">-ApplicationGateway</span></span>
<span data-ttu-id="17bc0-115">Specifica il gateway dell'applicazione con cui questo cmdlet associa il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="17bc0-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="17bc0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17bc0-116">-DefaultProfile</span></span>
<span data-ttu-id="17bc0-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="17bc0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17bc0-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="17bc0-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="17bc0-119">Specifica l'indirizzo IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="17bc0-119">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="17bc0-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="17bc0-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="17bc0-121">Specifica l'ID dell'indirizzo IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="17bc0-121">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="17bc0-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="17bc0-122">-FrontendPort</span></span>
<span data-ttu-id="17bc0-123">Specifica la porta di front-end gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="17bc0-123">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="17bc0-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="17bc0-124">-FrontendPortId</span></span>
<span data-ttu-id="17bc0-125">Specifica l'ID della porta del gateway dell'applicazione front-end.</span><span class="sxs-lookup"><span data-stu-id="17bc0-125">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="17bc0-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="17bc0-126">-HostName</span></span>
<span data-ttu-id="17bc0-127">Specifica il nome host a cui questo cmdlet invia il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="17bc0-127">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="17bc0-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="17bc0-128">-Name</span></span>
<span data-ttu-id="17bc0-129">Specifica il nome del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="17bc0-129">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="17bc0-130">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="17bc0-130">-Protocol</span></span>
<span data-ttu-id="17bc0-131">Specifica il protocollo usato dal listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="17bc0-131">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="17bc0-132">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="17bc0-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="17bc0-133">Http</span><span class="sxs-lookup"><span data-stu-id="17bc0-133">Http</span></span>
- <span data-ttu-id="17bc0-134">Https</span><span class="sxs-lookup"><span data-stu-id="17bc0-134">Https</span></span>

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

### <span data-ttu-id="17bc0-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="17bc0-135">-RequireServerNameIndication</span></span>
<span data-ttu-id="17bc0-136">Specifica se il cmdlet richiede l'indicazione del nome del server.</span><span class="sxs-lookup"><span data-stu-id="17bc0-136">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="17bc0-137">I valori accettabili per questo parametro sono: vero o falso.</span><span class="sxs-lookup"><span data-stu-id="17bc0-137">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="17bc0-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="17bc0-138">-SslCertificate</span></span>
<span data-ttu-id="17bc0-139">Specifica il certificato SSL del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="17bc0-139">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="17bc0-140">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="17bc0-140">-SslCertificateId</span></span>
<span data-ttu-id="17bc0-141">Specifica l'ID del certificato SSL (Secure Socket Layer) del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="17bc0-141">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="17bc0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17bc0-142">CommonParameters</span></span>
<span data-ttu-id="17bc0-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17bc0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17bc0-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17bc0-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17bc0-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="17bc0-145">INPUTS</span></span>

### <span data-ttu-id="17bc0-146">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="17bc0-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="17bc0-147">Parametri: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="17bc0-147">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="17bc0-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="17bc0-148">OUTPUTS</span></span>

### <span data-ttu-id="17bc0-149">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="17bc0-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="17bc0-150">Note</span><span class="sxs-lookup"><span data-stu-id="17bc0-150">NOTES</span></span>

## <span data-ttu-id="17bc0-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="17bc0-151">RELATED LINKS</span></span>

[<span data-ttu-id="17bc0-152">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="17bc0-152">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="17bc0-153">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="17bc0-153">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="17bc0-154">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="17bc0-154">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="17bc0-155">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="17bc0-155">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)


