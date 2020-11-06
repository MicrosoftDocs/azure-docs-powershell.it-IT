---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 07820860f1a6a43f51f8436fa3ba28d6238de087
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520187"
---
# <span data-ttu-id="68fe9-101">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="68fe9-101">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="68fe9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68fe9-102">SYNOPSIS</span></span>
<span data-ttu-id="68fe9-103">Aggiunge le impostazioni HTTP di back-end a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="68fe9-103">Adds back-end HTTP settings to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68fe9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68fe9-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-TrustedRootCertificate <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68fe9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68fe9-105">DESCRIPTION</span></span>
<span data-ttu-id="68fe9-106">Il cmdlet Add-AzureRmApplicationGatewayBackendHttpSettings aggiunge le impostazioni HTTP di back-end a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="68fe9-106">The Add-AzureRmApplicationGatewayBackendHttpSettings cmdlet adds back-end HTTP settings to an application gateway.</span></span>
<span data-ttu-id="68fe9-107">Le impostazioni HTTP di back-end vengono applicate a tutti i server back-end nel pool.</span><span class="sxs-lookup"><span data-stu-id="68fe9-107">Back-end HTTP settings are applied to all back-end servers in the pool.</span></span>

## <span data-ttu-id="68fe9-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68fe9-108">EXAMPLES</span></span>

### <span data-ttu-id="68fe9-109">Esempio 1: aggiungere le impostazioni HTTP di back-end a un gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="68fe9-109">Example 1: Add back-end HTTP settings to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "HTTP" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="68fe9-110">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw. Il secondo comando aggiunge le impostazioni HTTP di back-end al gateway dell'applicazione, impostando la porta su 88 e il protocollo su HTTP e denominando le impostazioni Setting02.</span><span class="sxs-lookup"><span data-stu-id="68fe9-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.The second command adds back-end HTTP settings to the application gateway, setting the port to 88 and the protocol to HTTP and names the settings Setting02.</span></span>

## <span data-ttu-id="68fe9-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68fe9-111">PARAMETERS</span></span>

### <span data-ttu-id="68fe9-112">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="68fe9-112">-AffinityCookieName</span></span>
<span data-ttu-id="68fe9-113">Nome del cookie da usare per il cookie di affinità</span><span class="sxs-lookup"><span data-stu-id="68fe9-113">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="68fe9-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68fe9-114">-ApplicationGateway</span></span>
<span data-ttu-id="68fe9-115">Specifica il nome del gateway dell'applicazione per cui questo cmdlet aggiunge le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="68fe9-115">Specifies the name of application gateway for which this cmdlet adds settings.</span></span>

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

### <span data-ttu-id="68fe9-116">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="68fe9-116">-AuthenticationCertificates</span></span>
<span data-ttu-id="68fe9-117">Specifica i certificati di autenticazione per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="68fe9-117">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68fe9-118">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="68fe9-118">-ConnectionDraining</span></span>
<span data-ttu-id="68fe9-119">Connessione che svuota la risorsa delle impostazioni http di backend.</span><span class="sxs-lookup"><span data-stu-id="68fe9-119">Connection draining of the backend http settings resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68fe9-120">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="68fe9-120">-CookieBasedAffinity</span></span>
<span data-ttu-id="68fe9-121">Specifica se l'affinità basata su cookie deve essere abilitata o disabilitata per il pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="68fe9-121">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="68fe9-122">I valori accettabili per questo parametro sono: disabled, Enabled.</span><span class="sxs-lookup"><span data-stu-id="68fe9-122">The acceptable values for this parameter are: Disabled, Enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68fe9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68fe9-123">-DefaultProfile</span></span>
<span data-ttu-id="68fe9-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="68fe9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68fe9-125">-HostName</span><span class="sxs-lookup"><span data-stu-id="68fe9-125">-HostName</span></span>
<span data-ttu-id="68fe9-126">Imposta l'intestazione host da inviare ai server back-end.</span><span class="sxs-lookup"><span data-stu-id="68fe9-126">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="68fe9-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="68fe9-127">-Name</span></span>
<span data-ttu-id="68fe9-128">Specifica il nome delle impostazioni HTTP di back-end aggiunte da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68fe9-128">Specifies the name of the back-end HTTP settings which this cmdlet adds.</span></span>

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

### <span data-ttu-id="68fe9-129">-Path</span><span class="sxs-lookup"><span data-stu-id="68fe9-129">-Path</span></span>
<span data-ttu-id="68fe9-130">Percorso che deve essere usato come prefisso per tutte le richieste HTTP.</span><span class="sxs-lookup"><span data-stu-id="68fe9-130">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="68fe9-131">Se per questo parametro non viene specificato alcun valore, non verrà preceduto alcun percorso.</span><span class="sxs-lookup"><span data-stu-id="68fe9-131">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="68fe9-132">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="68fe9-132">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="68fe9-133">Contrassegna se l'intestazione host deve essere selezionata dal nome host del server back-end.</span><span class="sxs-lookup"><span data-stu-id="68fe9-133">Flag if host header should be picked from the host name of the backend server.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68fe9-134">-Porta</span><span class="sxs-lookup"><span data-stu-id="68fe9-134">-Port</span></span>
<span data-ttu-id="68fe9-135">Specifica la porta del pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="68fe9-135">Specifies the port of the back-end server pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68fe9-136">-Probe</span><span class="sxs-lookup"><span data-stu-id="68fe9-136">-Probe</span></span>
<span data-ttu-id="68fe9-137">Specifica una sonda da associare a un server back-end.</span><span class="sxs-lookup"><span data-stu-id="68fe9-137">Specifies a probe to associate with a back-end server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68fe9-138">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="68fe9-138">-ProbeId</span></span>
<span data-ttu-id="68fe9-139">Specifica l'ID del Probe da associare al server back-end.</span><span class="sxs-lookup"><span data-stu-id="68fe9-139">Specifies the ID of the probe to associate with the back-end server.</span></span>

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

### <span data-ttu-id="68fe9-140">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="68fe9-140">-Protocol</span></span>
<span data-ttu-id="68fe9-141">Specifica il protocollo per la comunicazione tra il gateway dell'applicazione e i server back-end.</span><span class="sxs-lookup"><span data-stu-id="68fe9-141">Specifies the protocol for communication between application gateway and back-end servers.</span></span>
<span data-ttu-id="68fe9-142">I valori accettabili per questo parametro sono: http e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="68fe9-142">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="68fe9-143">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="68fe9-143">-RequestTimeout</span></span>
<span data-ttu-id="68fe9-144">Specifica il valore di timeout della richiesta.</span><span class="sxs-lookup"><span data-stu-id="68fe9-144">Specifies the request time-out value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68fe9-145">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="68fe9-145">-TrustedRootCertificate</span></span>
<span data-ttu-id="68fe9-146">Certificati radice attendibili del gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="68fe9-146">Application gateway Trusted Root Certificates</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68fe9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68fe9-147">CommonParameters</span></span>
<span data-ttu-id="68fe9-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68fe9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68fe9-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68fe9-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68fe9-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68fe9-150">INPUTS</span></span>

### <span data-ttu-id="68fe9-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68fe9-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="68fe9-152">Parametri: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="68fe9-152">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="68fe9-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68fe9-153">OUTPUTS</span></span>

### <span data-ttu-id="68fe9-154">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68fe9-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="68fe9-155">Note</span><span class="sxs-lookup"><span data-stu-id="68fe9-155">NOTES</span></span>

## <span data-ttu-id="68fe9-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68fe9-156">RELATED LINKS</span></span>

[<span data-ttu-id="68fe9-157">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="68fe9-157">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="68fe9-158">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="68fe9-158">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="68fe9-159">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="68fe9-159">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="68fe9-160">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="68fe9-160">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

