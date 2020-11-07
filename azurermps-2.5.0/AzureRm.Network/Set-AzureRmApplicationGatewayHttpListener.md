---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayhttplistener
schema: 2.0.0
ms.openlocfilehash: 7b3d38b8f55c93c4527d92969ec64ce792bca44b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865745"
---
# <span data-ttu-id="6dc5f-101">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6dc5f-101">Set-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="6dc5f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6dc5f-102">SYNOPSIS</span></span>
<span data-ttu-id="6dc5f-103">Modifica un listener HTTP per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6dc5f-103">Modifies an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6dc5f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6dc5f-104">SYNTAX</span></span>

### <span data-ttu-id="6dc5f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6dc5f-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dc5f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6dc5f-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dc5f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6dc5f-107">DESCRIPTION</span></span>
<span data-ttu-id="6dc5f-108">Il cmdlet **set-AzureRmApplicationGatewayHttpListener** modifica un listener HTTP per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="6dc5f-108">The **Set-AzureRmApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="6dc5f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6dc5f-109">EXAMPLES</span></span>

### <span data-ttu-id="6dc5f-110">Esempio 1: impostare un listener HTTP</span><span class="sxs-lookup"><span data-stu-id="6dc5f-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="6dc5f-111">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="6dc5f-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="6dc5f-112">Il secondo comando imposta il listener HTTP per il gateway per l'uso della configurazione front-end archiviata in $FIP 01 con il protocollo HTTP sulla porta 80.</span><span class="sxs-lookup"><span data-stu-id="6dc5f-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="6dc5f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6dc5f-113">PARAMETERS</span></span>

### <span data-ttu-id="6dc5f-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6dc5f-114">-ApplicationGateway</span></span>
<span data-ttu-id="6dc5f-115">Specifica il gateway dell'applicazione con cui questo cmdlet associa il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="6dc5f-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="6dc5f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dc5f-116">-DefaultProfile</span></span>
<span data-ttu-id="6dc5f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6dc5f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6dc5f-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6dc5f-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="6dc5f-119">Specifica l'indirizzo IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6dc5f-119">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="6dc5f-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6dc5f-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="6dc5f-121">Specifica l'ID dell'indirizzo IP front-end del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6dc5f-121">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="6dc5f-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="6dc5f-122">-FrontendPort</span></span>
<span data-ttu-id="6dc5f-123">Specifica la porta di front-end gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6dc5f-123">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="6dc5f-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="6dc5f-124">-FrontendPortId</span></span>
<span data-ttu-id="6dc5f-125">Specifica l'ID della porta del gateway dell'applicazione front-end.</span><span class="sxs-lookup"><span data-stu-id="6dc5f-125">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="6dc5f-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="6dc5f-126">-HostName</span></span>
<span data-ttu-id="6dc5f-127">Specifica il nome host a cui questo cmdlet invia il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="6dc5f-127">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="6dc5f-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="6dc5f-128">-Name</span></span>
<span data-ttu-id="6dc5f-129">Specifica il nome del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="6dc5f-129">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="6dc5f-130">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="6dc5f-130">-Protocol</span></span>
<span data-ttu-id="6dc5f-131">Specifica il protocollo usato dal listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="6dc5f-131">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="6dc5f-132">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6dc5f-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6dc5f-133">Http</span><span class="sxs-lookup"><span data-stu-id="6dc5f-133">Http</span></span>
- <span data-ttu-id="6dc5f-134">Https</span><span class="sxs-lookup"><span data-stu-id="6dc5f-134">Https</span></span>

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

### <span data-ttu-id="6dc5f-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="6dc5f-135">-RequireServerNameIndication</span></span>
<span data-ttu-id="6dc5f-136">Specifica se il cmdlet richiede l'indicazione del nome del server.</span><span class="sxs-lookup"><span data-stu-id="6dc5f-136">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="6dc5f-137">I valori accettabili per questo parametro sono: vero o falso.</span><span class="sxs-lookup"><span data-stu-id="6dc5f-137">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="6dc5f-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="6dc5f-138">-SslCertificate</span></span>
<span data-ttu-id="6dc5f-139">Specifica il certificato SSL del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="6dc5f-139">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="6dc5f-140">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="6dc5f-140">-SslCertificateId</span></span>
<span data-ttu-id="6dc5f-141">Specifica l'ID del certificato SSL (Secure Socket Layer) del listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="6dc5f-141">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="6dc5f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dc5f-142">CommonParameters</span></span>
<span data-ttu-id="6dc5f-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dc5f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dc5f-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dc5f-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dc5f-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6dc5f-145">INPUTS</span></span>

### <span data-ttu-id="6dc5f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="6dc5f-146">System.String</span></span>

## <span data-ttu-id="6dc5f-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6dc5f-147">OUTPUTS</span></span>

### <span data-ttu-id="6dc5f-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6dc5f-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6dc5f-149">Note</span><span class="sxs-lookup"><span data-stu-id="6dc5f-149">NOTES</span></span>

## <span data-ttu-id="6dc5f-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6dc5f-150">RELATED LINKS</span></span>

[<span data-ttu-id="6dc5f-151">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6dc5f-151">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="6dc5f-152">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6dc5f-152">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="6dc5f-153">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6dc5f-153">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="6dc5f-154">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6dc5f-154">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)


