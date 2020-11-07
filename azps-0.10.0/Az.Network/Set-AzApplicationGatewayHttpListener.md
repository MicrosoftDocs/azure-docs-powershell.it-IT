---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: ea07f3b9f2dd1e79f59b3369f3f8d3a8c1434deb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862842"
---
# <span data-ttu-id="55b06-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="55b06-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="55b06-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="55b06-102">SYNOPSIS</span></span>
<span data-ttu-id="55b06-103">Modifica un listener HTTP per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="55b06-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="55b06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55b06-104">SYNTAX</span></span>

### <span data-ttu-id="55b06-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="55b06-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55b06-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="55b06-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55b06-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55b06-107">DESCRIPTION</span></span>
<span data-ttu-id="55b06-108">Il cmdlet **set-AzApplicationGatewayHttpListener** modifica un listener HTTP per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="55b06-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="55b06-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55b06-109">EXAMPLES</span></span>

### <span data-ttu-id="55b06-110">Esempio 1: impostare un listener HTTP</span><span class="sxs-lookup"><span data-stu-id="55b06-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="55b06-111">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="55b06-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="55b06-112">Il secondo comando imposta il listener HTTP per il gateway per l'uso della configurazione front-end archiviata in $FIP 01 con il protocollo HTTP sulla porta 80.</span><span class="sxs-lookup"><span data-stu-id="55b06-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="55b06-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="55b06-113">PARAMETERS</span></span>

### <span data-ttu-id="55b06-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="55b06-114">-ApplicationGateway</span></span>
<span data-ttu-id="55b06-115">Specifica il gateway dell'applicazione con cui questo cmdlet associa il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="55b06-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="55b06-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55b06-116">-DefaultProfile</span></span>
<span data-ttu-id="55b06-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="55b06-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55b06-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="55b06-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="55b06-119">Specifica l'indirizzo IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="55b06-119">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="55b06-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="55b06-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="55b06-121">Specifica l'ID dell'indirizzo IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="55b06-121">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="55b06-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="55b06-122">-FrontendPort</span></span>
<span data-ttu-id="55b06-123">Specifica la porta di front-end gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="55b06-123">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="55b06-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="55b06-124">-FrontendPortId</span></span>
<span data-ttu-id="55b06-125">Specifica l'ID della porta del gateway dell'applicazione front-end.</span><span class="sxs-lookup"><span data-stu-id="55b06-125">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="55b06-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="55b06-126">-HostName</span></span>
<span data-ttu-id="55b06-127">Specifica il nome host a cui questo cmdlet invia il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="55b06-127">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="55b06-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="55b06-128">-Name</span></span>
<span data-ttu-id="55b06-129">Specifica il nome del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="55b06-129">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="55b06-130">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="55b06-130">-Protocol</span></span>
<span data-ttu-id="55b06-131">Specifica il protocollo usato dal listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="55b06-131">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="55b06-132">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="55b06-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="55b06-133">Http</span><span class="sxs-lookup"><span data-stu-id="55b06-133">Http</span></span>
- <span data-ttu-id="55b06-134">Https</span><span class="sxs-lookup"><span data-stu-id="55b06-134">Https</span></span>

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

### <span data-ttu-id="55b06-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="55b06-135">-RequireServerNameIndication</span></span>
<span data-ttu-id="55b06-136">Specifica se il cmdlet richiede l'indicazione del nome del server.</span><span class="sxs-lookup"><span data-stu-id="55b06-136">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="55b06-137">I valori accettabili per questo parametro sono: vero o falso.</span><span class="sxs-lookup"><span data-stu-id="55b06-137">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="55b06-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="55b06-138">-SslCertificate</span></span>
<span data-ttu-id="55b06-139">Specifica il certificato SSL del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="55b06-139">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="55b06-140">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="55b06-140">-SslCertificateId</span></span>
<span data-ttu-id="55b06-141">Specifica l'ID del certificato SSL (Secure Socket Layer) del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="55b06-141">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="55b06-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55b06-142">CommonParameters</span></span>
<span data-ttu-id="55b06-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55b06-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55b06-144">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55b06-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55b06-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="55b06-145">INPUTS</span></span>

### <span data-ttu-id="55b06-146">System. String</span><span class="sxs-lookup"><span data-stu-id="55b06-146">System.String</span></span>

## <span data-ttu-id="55b06-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55b06-147">OUTPUTS</span></span>

### <span data-ttu-id="55b06-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="55b06-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="55b06-149">Note</span><span class="sxs-lookup"><span data-stu-id="55b06-149">NOTES</span></span>

## <span data-ttu-id="55b06-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55b06-150">RELATED LINKS</span></span>

[<span data-ttu-id="55b06-151">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="55b06-151">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="55b06-152">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="55b06-152">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="55b06-153">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="55b06-153">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="55b06-154">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="55b06-154">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


