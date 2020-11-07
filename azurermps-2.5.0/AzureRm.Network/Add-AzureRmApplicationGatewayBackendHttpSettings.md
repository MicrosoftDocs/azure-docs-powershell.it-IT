---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
ms.openlocfilehash: f283b40e7e40285a221eb436495d54820884003f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866506"
---
# <span data-ttu-id="f5601-101">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f5601-101">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="f5601-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f5601-102">SYNOPSIS</span></span>
<span data-ttu-id="f5601-103">Aggiunge le impostazioni HTTP di back-end a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f5601-103">Adds back-end HTTP settings to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5601-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f5601-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5601-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5601-105">DESCRIPTION</span></span>
<span data-ttu-id="f5601-106">Il cmdlet Add-AzureRmApplicationGatewayBackendHttpSettings aggiunge le impostazioni HTTP di back-end a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f5601-106">The Add-AzureRmApplicationGatewayBackendHttpSettings cmdlet adds back-end HTTP settings to an application gateway.</span></span>

<span data-ttu-id="f5601-107">Le impostazioni HTTP di back-end vengono applicate a tutti i server back-end nel pool.</span><span class="sxs-lookup"><span data-stu-id="f5601-107">Back-end HTTP settings are applied to all back-end servers in the pool.</span></span>

## <span data-ttu-id="f5601-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f5601-108">EXAMPLES</span></span>

### <span data-ttu-id="f5601-109">Esempio 1: aggiungere le impostazioni HTTP di back-end a un gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="f5601-109">Example 1: Add back-end HTTP settings to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "HTTP" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="f5601-110">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw. Il secondo comando aggiunge le impostazioni HTTP di back-end al gateway dell'applicazione, impostando la porta su 88 e il protocollo su HTTP e denominando le impostazioni Setting02.</span><span class="sxs-lookup"><span data-stu-id="f5601-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.The second command adds back-end HTTP settings to the application gateway, setting the port to 88 and the protocol to HTTP and names the settings Setting02.</span></span>

## <span data-ttu-id="f5601-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f5601-111">PARAMETERS</span></span>

### <span data-ttu-id="f5601-112">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="f5601-112">-AffinityCookieName</span></span>
<span data-ttu-id="f5601-113">Nome del cookie da usare per il cookie di affinità</span><span class="sxs-lookup"><span data-stu-id="f5601-113">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="f5601-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5601-114">-ApplicationGateway</span></span>
<span data-ttu-id="f5601-115">Specifica il nome del gateway dell'applicazione per cui questo cmdlet aggiunge le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="f5601-115">Specifies the name of application gateway for which this cmdlet adds settings.</span></span>

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

### <span data-ttu-id="f5601-116">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="f5601-116">-AuthenticationCertificates</span></span>
<span data-ttu-id="f5601-117">Specifica i certificati di autenticazione per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f5601-117">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="f5601-118">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f5601-118">-ConnectionDraining</span></span>
<span data-ttu-id="f5601-119">Connessione che svuota la risorsa delle impostazioni http di backend.</span><span class="sxs-lookup"><span data-stu-id="f5601-119">Connection draining of the backend http settings resource.</span></span>

```yaml
Type: PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5601-120">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="f5601-120">-CookieBasedAffinity</span></span>
<span data-ttu-id="f5601-121">Specifica se l'affinità basata su cookie deve essere abilitata o disabilitata per il pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="f5601-121">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="f5601-122">I valori accettabili per questo parametro sono: disabled, Enabled.</span><span class="sxs-lookup"><span data-stu-id="f5601-122">The acceptable values for this parameter are: Disabled, Enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5601-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5601-123">-DefaultProfile</span></span>
<span data-ttu-id="f5601-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f5601-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5601-125">-HostName</span><span class="sxs-lookup"><span data-stu-id="f5601-125">-HostName</span></span>
<span data-ttu-id="f5601-126">Imposta l'intestazione host da inviare ai server back-end.</span><span class="sxs-lookup"><span data-stu-id="f5601-126">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="f5601-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5601-127">-Name</span></span>
<span data-ttu-id="f5601-128">Specifica il nome delle impostazioni HTTP di back-end aggiunte da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5601-128">Specifies the name of the back-end HTTP settings which this cmdlet adds.</span></span>

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

### <span data-ttu-id="f5601-129">-Path</span><span class="sxs-lookup"><span data-stu-id="f5601-129">-Path</span></span>
<span data-ttu-id="f5601-130">Percorso che deve essere usato come prefisso per tutte le richieste HTTP.</span><span class="sxs-lookup"><span data-stu-id="f5601-130">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="f5601-131">Se per questo parametro non viene specificato alcun valore, non verrà preceduto alcun percorso.</span><span class="sxs-lookup"><span data-stu-id="f5601-131">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="f5601-132">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="f5601-132">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="f5601-133">Contrassegna se l'intestazione host deve essere selezionata dal nome host del server back-end.</span><span class="sxs-lookup"><span data-stu-id="f5601-133">Flag if host header should be picked from the host name of the backend server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5601-134">-Porta</span><span class="sxs-lookup"><span data-stu-id="f5601-134">-Port</span></span>
<span data-ttu-id="f5601-135">Specifica la porta del pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="f5601-135">Specifies the port of the back-end server pool.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5601-136">-Probe</span><span class="sxs-lookup"><span data-stu-id="f5601-136">-Probe</span></span>
<span data-ttu-id="f5601-137">Specifica una sonda da associare a un server back-end.</span><span class="sxs-lookup"><span data-stu-id="f5601-137">Specifies a probe to associate with a back-end server.</span></span>

```yaml
Type: PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5601-138">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="f5601-138">-ProbeEnabled</span></span>
<span data-ttu-id="f5601-139">Contrassegno se la sonda deve essere abilitata.</span><span class="sxs-lookup"><span data-stu-id="f5601-139">Flag if probe should be enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5601-140">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="f5601-140">-ProbeId</span></span>
<span data-ttu-id="f5601-141">Specifica l'ID del Probe da associare al server back-end.</span><span class="sxs-lookup"><span data-stu-id="f5601-141">Specifies the ID of the probe to associate with the back-end server.</span></span>

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

### <span data-ttu-id="f5601-142">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="f5601-142">-Protocol</span></span>
<span data-ttu-id="f5601-143">Specifica il protocollo per la comunicazione tra il gateway dell'applicazione e i server back-end.</span><span class="sxs-lookup"><span data-stu-id="f5601-143">Specifies the protocol for communication between application gateway and back-end servers.</span></span>
<span data-ttu-id="f5601-144">I valori accettabili per questo parametro sono: http e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f5601-144">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="f5601-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="f5601-145">-RequestTimeout</span></span>
<span data-ttu-id="f5601-146">Specifica il valore di timeout della richiesta.</span><span class="sxs-lookup"><span data-stu-id="f5601-146">Specifies the request time-out value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5601-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5601-147">CommonParameters</span></span>
<span data-ttu-id="f5601-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5601-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5601-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5601-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5601-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f5601-150">INPUTS</span></span>

### <span data-ttu-id="f5601-151">System. String</span><span class="sxs-lookup"><span data-stu-id="f5601-151">System.String</span></span>

## <span data-ttu-id="f5601-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f5601-152">OUTPUTS</span></span>

### <span data-ttu-id="f5601-153">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5601-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f5601-154">Note</span><span class="sxs-lookup"><span data-stu-id="f5601-154">NOTES</span></span>

## <span data-ttu-id="f5601-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f5601-155">RELATED LINKS</span></span>

[<span data-ttu-id="f5601-156">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f5601-156">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="f5601-157">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f5601-157">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="f5601-158">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f5601-158">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="f5601-159">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f5601-159">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

